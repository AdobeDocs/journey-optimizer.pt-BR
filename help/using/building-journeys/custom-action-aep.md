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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62aid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1085
ht-degree: 1%

---

# Usar ações personalizadas para gravar eventos de jornada na Experience Platform {#custom-action-aep}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como gravar eventos de jornada personalizados no Adobe Experience Platform a partir de suas jornadas usando ações personalizadas e chamadas de API autenticadas.

>[!ENDSHADEBOX]

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
>Depois de criar seu projeto no Adobe Developer Console, conceda ao desenvolvedor e ao API o controle de acesso com as permissões certas. Saiba mais na [[!DNL Adobe Experience Platform] documentação](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

- **TL;DR:** Este caso de uso explica como configurar uma ação personalizada no Journey Optimizer que grava dados de eventos de jornada no Adobe Experience Platform usando uma entrada de API HTTP e chamadas autenticadas de servidor para servidor OAuth.

**Intenções:**
- Configurar um projeto do Adobe Developer Console IO com credenciais de servidor para servidor do OAuth para autenticação de API do AEP
- Crie uma fonte de entrada da API HTTP no Adobe Experience Platform para receber dados de evento de jornada de transmissão
- Configure uma ação personalizada no Journey Optimizer com o URL, os cabeçalhos e a autenticação personalizada de token do portador
- Mapear campos de jornada (ID de versão da jornada, ID do nó, ID do cliente) dinamicamente como variáveis na carga de ação personalizada
- Use a ação personalizada em uma jornada para gravar eventos personalizados em um conjunto de dados do AEP

**Glossário:**
- **Entrada de API HTTP**: um conector de origem Adobe Experience Platform que cria um ponto de extremidade de streaming para assimilar dados por meio de solicitações HTTP POST *(específico do produto)*
- **OAuth Server-to-Server**: um tipo de credencial de autenticação no Adobe Developer Console que gera tokens de Portador para chamadas de API de servidor para servidor sem interação do usuário *(específico do produto)*
- **Autorização personalizada**: um tipo de autenticação de ação personalizada do Journey Optimizer que busca um token de portador de um ponto de extremidade especificado e o armazena em cache por um período configurado *(específico do produto)*
- **Entidade XDM**: a estrutura da carga de dados em conformidade com o esquema do Modelo de Dados de Experiência, usada como o corpo ao gravar eventos no AEP por meio da entrada da API HTTP *(específico do produto)*
- **cacheDuration**: a configuração de cache de token na configuração de autorização personalizada que controla por quanto tempo o token do Portador buscado é reutilizado antes que um novo seja solicitado *(específico do produto)*

**Medidas de Proteção:**
- Depois de criar o projeto do Adobe Developer Console, as permissões de desenvolvedor e de controle de acesso à API devem ser concedidas explicitamente para que as credenciais possam ser usadas
- A fonte de entrada da API HTTP deve ser criada com autenticação habilitada; o URL do ponto de extremidade da conexão e a carga do esquema devem ser copiados e armazenados para uso na configuração de ação personalizada
- Os cabeçalhos de ação personalizados devem incluir Content-Type, Charset e sandbox-name
- Os campos que devem ser preenchidos dinamicamente no tempo de execução devem ser alterados de Constante para Variável na configuração de carga da ação personalizada

**Terminologia:**
- Nome canônico: Ação personalizada — Acrônimo: none — variantes: configuração de ação personalizada, ação personalizada de Journey Optimizer
- Nome canônico: Adobe Experience Platform — Acrônimo: AEP — variantes: Experience Platform, Platform
- Sinônimos: &quot;Entrada de API HTTP&quot; = &quot;ponto de extremidade de transmissão&quot; = &quot;Ponto de extremidade de coleção DCS&quot;
- Não confunda: &quot;OAuth Server-to-Server&quot; ≠ &quot;OAuth user authentication&quot; (Servidor-to-Server não requer um logon de usuário; ele usa credenciais do cliente)

**Perguntas frequentes:**
- **P: Que tipo de autenticação é usado para chamar a Entrada da API HTTP do AEP a partir de uma ação personalizada do Journey Optimizer?** — Autenticação de token do portador personalizado usando credenciais de cliente OAuth de servidor para servidor buscadas no endpoint do token do Adobe IMS.
- **P: Onde encontro os valores client_id, client_secret, grant_type e scope?** — Na seção Credenciais de servidor para servidor do OAuth do seu projeto do Adobe Developer Console IO, clicando em &quot;Exibir o comando cURL&quot;.
- **P: Como faço para tornar campos específicos da jornada (por exemplo, journeyVersionId, nodeId) dinâmicos na carga?** — Altere a configuração de campo de Constante para Variável na configuração de carga da ação personalizada para que sejam preenchidos no contexto de jornada no tempo de execução.
- **P: Quais permissões são necessárias para o projeto do Adobe Developer Console?** — O desenvolvedor e o controle de acesso da API devem receber as permissões certas após a criação do projeto, conforme descrito na documentação de autenticação da API do AEP.
- **P: Qual é a finalidade da configuração cacheDuration na carga de autenticação?** — Ele controla por quanto tempo o token do portador buscado é armazenado em cache e reutilizado (28.000 segundos no exemplo) antes da ação personalizada solicitar um novo token.

+++
