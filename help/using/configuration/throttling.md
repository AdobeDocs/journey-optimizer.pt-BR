---
solution: Journey Optimizer
product: journey optimizer
title: API de limitação
description: Saiba como trabalhar com a API de limitação
feature: Journeys, API
role: User
level: Beginner
keywords: external, API, otimizer, capping
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: 847fb5dda4e8747ea61a2ffafb9adcddda1ddada
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 49%

---

# Trabalhar com a API de limitação

A API de limitação ajuda a criar, configurar e monitorar as configurações de limitação para limitar o número de eventos enviados por segundo.

Esta seção fornece informações globais sobre como trabalhar com a API. Uma descrição detalhada da API está disponível na [documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

## Leitura obrigatória

* **Uma configuração por organização:** No momento, apenas uma configuração é permitida por organização. Uma configuração deve ser definida em uma sandbox de produção (fornecida por meio de `x-sandbox-name` nos cabeçalhos).
* **Aplicativo de nível da organização:** uma configuração é aplicada no nível da organização.
* **Tratamento de limite de API:** quando o limite definido na API é atingido, mais eventos são enfileirados por até 6 horas. Este valor não pode ser modificado.
* **`maxHttpConnections`parâmetro:** O parâmetro &#39;maxHttpConnections&#39; é um parâmetro opcional disponível na API Capping que permite restringir apenas o número de conexões que o Journey Optimizer abrirá no sistema externo. [Saiba como trabalhar com a API de Limite](../configuration/capping.md)

  Se você quiser restringir o número de conexões, mas também limitar essas chamadas externas, poderá definir duas configurações, uma limitação e uma limitação, no mesmo endpoint. Ambas as configurações podem coexistir para um endpoint. Para definir &quot;maxHttpConnections&quot; para um ponto de extremidade limitado, use a API de limitação para definir o limite de limitação e a API de limitação para definir &quot;maxHttpConnections&quot;. Ao chamar a API de limitação, você pode definir o limite de limitação para algo mais alto que o limite de limitação, de modo que a regra de limitação nunca entre em vigor.

## Descrição da API de limitação e coleção do Postman {#description}

A tabela abaixo lista os comandos disponíveis para a API de limitação. Informações detalhadas, incluindo amostras de solicitações, parâmetros e formatos de resposta estão disponíveis na [documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Método | Caminho | Descrição |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | Obter uma lista das configurações de limitação |
| [!DNL POST] | /throttlingConfigs | Criar uma configuração de limitação |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | Implantar uma configuração de limitação |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | Desimplantar uma configuração de limitação |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | Verificar se uma configuração de limitação pode ser implantada ou não |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | Atualizar uma configuração de limitação |
| [!DNL GET] | /throttlingConfigs/`{uid}` | Recuperar uma configuração de limitação |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | Excluir uma configuração de limitação |

Além disso, uma coleção do Postman está disponível [aqui](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json) para ajudá-lo na configuração de teste.

Esta coleção foi configurada para compartilhar a coleção de Variáveis Postman gerada por meio das __[Integrações do Console Adobe I/O](https://console.adobe.io/integrations) > Experimente > Baixar para Postman__, que gera um arquivo de Ambiente Postman com os valores de integrações selecionados.

Após o download e o upload para o Postman, é necessário adicionar três variáveis: `{JO_HOST}`,`{BASE_PATH}` e `{SANDBOX_NAME}`.
* `{JO_HOST}` : [!DNL Journey Optimizer] URL do Gateway.
* `{BASE_PATH}` : ponto de entrada para a API.
* `{SANDBOX_NAME}` : o cabeçalho **x-sandbox-name** (por exemplo, “prod”) correspondente ao nome da sandbox na qual as operações da API ocorrerão. Consulte a [visão geral das sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=pt-BR) para obter mais informações.

## Configuração de limitação {#configuration}

Esta é a estrutura de uma configuração de limitação. Os atributos **name** e **description** são opcionais.

```
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

Exemplo:

```
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

## Erros

Ao criar ou atualizar uma configuração, o processo valida a configuração fornecida e retorna o status de validação, identificado por seu identificador exclusivo, como:

```
"ok" or "error"
```

>[!IMPORTANT]
>
>Os atributos **maxThroughput**, **urlPattern** e **methods** são obrigatórios.
>
>O valor de **maxThroughput** deve estar entre 200 a 5000.

Ao criar, excluir ou implantar a configuração de limitação, os seguintes erros podem ocorrer:

* **ERR_THROTTLING_CONFIG_100**: configuração de limitação: o `<mandatory attribute>` é obrigatório
* **ERR_THROTTLING_CONFIG_101**: configuração de limitação: o atributo maxThroughput é obrigatório e deve ser maior ou igual a 200 e menor ou igual a 5000
* **ERR_THROTTLING_CONFIG_104**: configuração de limitação: o atributo urlPattern está malformado
* **ERR_THROTTLING_CONFIG_105**: configuração de limitação: curingas não são permitidos na parte do host do urlPattern
* **ERR_THROTTLING_CONFIG_106**: configuração de limitação: conteúdo inválido
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**: “Não é possível excluir uma configuração de limitação implantada. Desimplante a configuração antes de excluí-la”
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**: “Não é possível excluir a configuração de limitação: ocorreu um erro inesperado”
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**: “Não é possível implantar a configuração de limitação: ocorreu um erro inesperado”
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**: “Não é possível desimplantar a configuração de limitação: ocorreu um erro inesperado”
* **THROTTLING_CONFIG_GET_ERROR: 1460**: “Não é possível obter a configuração de limitação: ocorreu erro inesperado”
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**: “Não é possível atualizar a configuração de limitação: a versão do tempo de execução não está ativa”
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**: “Não é possível atualizar a configuração de limitação: ocorreu um erro inesperado”
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**: “Operação não permitida na configuração de limitação: sandbox de não produção”
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**: “Não é possível criar a configuração de limitação: ocorreu um erro inesperado”
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**: “Não é possível criar a configuração de limitação: somente uma configuração é permitida por organização”
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466**: “Não é possível implantar a configuração de limitação: a configuração já foi implantada”
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467**: “Configuração de limitação não encontrada”
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468**: “Não é possível desimplantar a configuração de limitação: a configuração ainda não foi implantada”

**Exemplos de erros**

Ao tentar criar uma configuração em uma sandbox de não produção:

```
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

Caso a sandbox fornecida não exista:

```
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

Ao tentar criar outra configuração:

```
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## Ciclo de vida da configuração no nível do tempo de execução {#config}

Quando uma configuração é desimplantada, ela é marcada como inativa no nível do tempo de execução e os eventos pendentes continuam a ser processados durante 24 horas. Em seguida, ela é excluída no serviço do tempo de execução.

Após desimplantar uma configuração, é possível atualizá-la e reimplantá-la. Isso criará uma nova configuração de tempo de execução que será considerada na execução das ações futuras.

Ao atualizar uma configuração já implantada, os novos valores são considerados imediatamente. Os recursos do sistema subjacente são adaptados automaticamente. Isso é ideal se comparado ao processo de desimplantar e reimplantar a configuração.

## Exemplos de respostas {#responses}

**Criação - POST**

```
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**Atualizar - PUT**

```
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**Ler (após a atualização) - GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**Ler (após a implantação) - GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## Casos de uso {#uc}

Esta seção lista casos de uso importantes para gerenciar configurações de limitação no [!DNL Journey Optimizer] e os comandos de API associados necessários para implementar o caso de uso.

Detalhes sobre cada comando de API estão disponíveis na [descrição da API e coleção do Postman](#description).

+++Criação e implantação de uma nova configuração de limitação

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`create`** - Cria uma nova configuração.
1. **`candeploy`** - Verifica se a configuração pode ser implantada.
1. **`deploy`** - Implanta a configuração.

+++

+++Atualizar e implantar uma configuração de limitação (ainda não implantada)

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`get`** - Obtém detalhes de uma configuração específica.
1. **`update`** - Modifica a configuração.
1. **`candeploy`** - Verifica a qualificação da implantação.
1. **`deploy`** - Implanta a configuração.

+++

+++Desimplantar e excluir uma configuração de limitação implantada

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`undeploy`** - Desimplanta a configuração.
1. **`delete`** - Remove a configuração.

+++

+++Exclui uma configuração de limitação implantada

Em apenas uma chamada de API, você pode desimplantar e excluir a configuração usando o parâmetro `forceDelete`.

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`delete`(com parâmetro `forceDelete`)** - Força a exclusão de uma configuração implantada em uma única etapa.

+++

+++Atualiza uma configuração de limitação já implantada

>[!NOTE]
>
>Não é necessário desimplantar a configuração antes da atualização

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`get`** - Obtém detalhes de uma configuração específica.
1. **`update`** - Modifica a configuração.

+++
