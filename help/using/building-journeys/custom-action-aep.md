---
solution: Journey Optimizer
product: journey optimizer
title: Usar ações personalizadas para gravar eventos de Jornada no AEP
description: Usar ações personalizadas para gravar eventos de Jornada no AEP
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/TbX3usHKfEM6WQPjFRjo2jCSb78rcbYEWWmV0tpGdj4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 3%

---

# Usar ações personalizadas para gravar eventos de jornada na Experience Platform {#custom-action-aep}

Este caso de uso explica como gravar eventos personalizados no [!DNL Adobe Experience Platform] a partir do Jornada usando Ações Personalizadas e Chamadas Autenticadas.

## Configurar um projeto do desenvolvedor {#custom-action-aep-IO}

1. Na Adobe Developer Console, clique em **Projeto** e abra seu projeto IO.

1. Na seção **Credenciais**, clique em **Servidor para Servidor OAuth**.

   ![Tela de configuração de ação personalizada com lista suspensa de tipo de ação](assets/custom-action-aep-1.png)

1. Clique em **Exibir comando cURL**.

   ![[!DNL Adobe Experience Platform] seleção do tipo de ação](assets/custom-action-aep-2.png)

1. Copie o comando cURL e armazene client_id, client_secret, grant_type e scope.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>Depois de criar seu projeto no Adobe Developer Console, conceda ao desenvolvedor e ao API o controle de acesso com as permissões certas. Saiba mais na [[!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}

## Configurar a fonte usando a entrada da API HTTP

1. Crie um ponto de extremidade em [!DNL Adobe Experience Platform] para gravar os dados do jornada.

1. Em [!DNL Adobe Experience Platform], clique em **Fontes**, em **Conexões**, no menu esquerdo. Em **API HTTP**, clique em **Adicionar dados**.

   ![Lista suspensa de seleção de sandbox para [!DNL Adobe Experience Platform]](assets/custom-action-aep-3.png)

1. Selecione **Nova conta** e habilite a autenticação. Selecione **Conectar ao Source**.

   ![Interface de seleção do conjunto de dados para transmissão de dados](assets/custom-action-aep-4.png)

1. Selecione **Avançar** e o Conjunto de Dados no qual você deseja gravar os dados. Clique em **Avançar** e **Concluir**.

   ![Campos de esquema XDM mapeados para parâmetros de ação](assets/custom-action-aep-5.png)

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

1. Abra [!DNL Adobe Journey Optimizer] e clique em **Configurações**, em **Administração**, no menu esquerdo. Em **Ações**, clique em **Gerenciar** e em **Criar Ação**.

1. Defina o URL e selecione o método Post.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Verifique se os Cabeçalhos (Tipo de conteúdo, Conjunto de caracteres, nome da sandbox) estão configurados.

   ![Ação personalizada na tela de jornada com o painel de configuração](assets/custom-action-aep-7bis.png)

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

   ![Interface de mapeamento de parâmetros com o editor de expressão](assets/custom-action-aep-8.png)

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

   ![Editor de modo avançado para mapeamento de campo complexo](assets/custom-action-aep-9.png)
