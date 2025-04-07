---
solution: Journey Optimizer
product: journey optimizer
title: Usar ações personalizadas para gravar eventos de Jornada no AEP
description: Usar ações personalizadas para gravar eventos de Jornada no AEP
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Caso de uso: usar ações personalizadas para gravar eventos de Jornada no Experience Platform {#custom-action-aep}

Este caso de uso explica como gravar eventos personalizados no Adobe Experience Platform a partir do Jornada usando Ações personalizadas e Chamadas autenticadas.

## Configurar um projeto de E/S {#custom-action-aep-IO}

1. Na Adobe Developer Console, clique em **Projeto** e abra seu projeto IO.

1. Na seção **Credenciais**, clique em **Servidor para Servidor OAuth**.

   ![](assets/custom-action-aep-1.png)

1. Clique em **Exibir comando cURL**.

   ![](assets/custom-action-aep-2.png)

1. Copie o comando cURL e armazene client_id, client_secret, grant_type e scope.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>Depois de criar seu projeto no Adobe Developer Console, conceda ao desenvolvedor e ao API o controle de acesso com as permissões certas. Saiba mais na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}

## Configurar o Source usando a entrada da API HTTP

1. Crie um endpoint no Adobe Experience Platform para gravar os dados do jornada.

1. No Adobe Experience Platform, clique em **Fontes**, em **Conexões**, no menu esquerdo. Em **API HTTP**, clique em **Adicionar dados**.

   ![](assets/custom-action-aep-3.png)

1. Selecione **Nova conta** e habilite a autenticação. Clique em **Conectar-se ao Source**.

   ![](assets/custom-action-aep-4.png)

1. Clique em **Avançar** e selecione o Conjunto de Dados no qual deseja gravar os dados. Clique em **Avançar** e **Concluir**.

   ![](assets/custom-action-aep-5.png)

1. Abra o fluxo de dados recém-criado. Copie a carga do esquema e salve-a no bloco de notas.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## Configurar a ação personalizada {#custom-action-config}

A configuração de ação personalizada está detalhada em [esta página](../action/about-custom-action-configuration.md).

Para este exemplo, siga estas etapas:

1. Abra o Adobe Journey Optimizer e clique em **Configurações**, em **Administração** no menu esquerdo. Em **Ações**, clique em **Gerenciar** e em **Criar Ação**.

1. Defina o URL e selecione o método Post.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Verifique se os Cabeçalhos (Tipo de conteúdo, Conjunto de caracteres, nome da sandbox) estão configurados.

   ![](assets/custom-action-aep-7bis.png)

### Configurar a autenticação {#custom-action-aep-authentication}

1. Selecione o **Tipo** como **Personalizado** com a seguinte carga.

1. Cole client_secret, client_id, scope e grant_type (da carga útil do projeto IO usada anteriormente).

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. Use o botão **Clique para testar a autenticação** para testar a conexão.

   ![](assets/custom-action-aep-8.png)

### Configurar o conteúdo {#custom-action-aep-payload}

1. Nos campos **Solicitação** e **Resposta**, cole a carga da conexão de origem usada anteriormente.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. Altere a Configuração de Campo de **Constante** para **Variável** para campos que serão preenchidos dinamicamente.

1. Salve a ação personalizada.

## Jornada

1. Por fim, use essa ação personalizada em uma jornada para gravar os eventos de jornada personalizados.

1. Preencha a ID da versão do Jornada, a ID do nó, o Nome do nó e outros atributos de acordo com o caso de uso.

   ![](assets/custom-action-aep-9.png)
