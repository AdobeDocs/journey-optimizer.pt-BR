---
solution: Journey Optimizer
product: journey optimizer
title: API de limite
description: Saiba como trabalhar com a API de limite
feature: Journeys, API
role: User
level: Beginner
keywords: external, API, otimizer, capping
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 9f801b1fdcab38bffff851675eca5e2fb61dfbf9
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 6%

---

# Trabalhar com a API de limite {#work}

A API de limite ajuda a criar, configurar e monitorar as configurações de limite.

Esta seção fornece informações globais sobre como trabalhar com a API. Uma descrição detalhada da API está disponível na [documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

## Descrição da API de limite e coleção do Postman {#description}

A tabela abaixo lista os comandos disponíveis para a API de limitação. Informações detalhadas, incluindo amostras de solicitações, parâmetros e formatos de resposta estão disponíveis na [documentação das APIs do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Método | Caminho | Descrição |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Obter uma lista das configurações de limite de endpoint |
| [!DNL POST] | /endpointConfigs | Criar uma configuração de limite de endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Implantar uma configuração de limite de ponto de extremidade |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Desimplantar uma configuração de limite de endpoint |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Verificar se uma configuração de limite de ponto de extremidade pode ser implantada ou não |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Atualizar uma configuração de limite de ponto de extremidade |
| [!DNL GET] | /endpointConfigs/`{uid}` | Recuperar uma configuração de limite de ponto de extremidade |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Excluir uma configuração de limite de ponto de extremidade |

Quando uma configuração é criada ou atualizada, uma verificação é executada automaticamente para garantir a sintaxe e a integridade do payload.
Se ocorrerem alguns problemas, a operação retornará um aviso ou erros para ajudá-lo a corrigir a configuração.

Além disso, uma coleção do Postman está disponível [aqui](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) para ajudá-lo na configuração de teste.

Esta coleção foi configurada para compartilhar a coleção de Variáveis Postman gerada por meio das __[Integrações do Console Adobe I/O](https://console.adobe.io/integrations) > Experimente > Baixar para Postman__, que gera um arquivo de Ambiente Postman com os valores de integrações selecionados.

Após o download e o upload para o Postman, é necessário adicionar três variáveis: `{JO_HOST}`,`{BASE_PATH}` e `{SANDBOX_NAME}`.
* `{JO_HOST}` : [!DNL Journey Optimizer] URL do Gateway.
* `{BASE_PATH}` : ponto de entrada para a API.
* `{SANDBOX_NAME}` : o cabeçalho **x-sandbox-name** (por exemplo, “prod”) correspondente ao nome da sandbox na qual as operações da API ocorrerão. Consulte a [visão geral das sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=pt-BR) para obter mais informações.

## Configuração do endpoint

Esta é a estrutura básica de uma configuração de endpoint:

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>O parâmetro **maxHttpConnections** é opcional. Ela permite restringir o número de conexões que o Journey Optimizer abrirá com o sistema externo.
>
>O valor máximo que pode ser definido é 400. Se nada for especificado, o sistema poderá abrir até vários milhares de conexões, dependendo do dimensionamento dinâmico do sistema.
>
>Quando a configuração de limitação é implantada, se nenhum valor &quot;maxHttpConnection&quot; for fornecido, um &quot;maxHttpConnection = -1&quot; padrão será adicionado à configuração implantada, significando que o Journey Optimizer usará o valor do sistema padrão.

Exemplo:

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>A configuração só estará ativa depois de chamar o ponto de extremidade **deploy**.

## Aviso e erros

Quando um método **canDeploy** é chamado, o processo valida a configuração e retorna o status de validação identificado por sua Identificação Exclusiva:

```
"ok" or "error"
```

Os possíveis erros são:

* **ERR_ENDPOINTCONFIG_100**: configuração de limitação: url ausente ou inválida
* **ERR_ENDPOINTCONFIG_101**: configuração de limitação: url malformada
* **ERR_ENDPOINTCONFIG_102**: configuração de limitação: url malformada: caractere curinga em url não permitido em host:port
* **ERR_ENDPOINTCONFIG_103**: configuração de limitação: métodos HTTP ausentes
* **ERR_ENDPOINTCONFIG_104**: configuração de limitação: nenhuma classificação de chamada definida
* **ERR_ENDPOINTCONFIG_107**: configuração de limitação: contagem máxima inválida de chamadas (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: configuração de limitação: contagem máxima de chamadas inválida (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: configuração de limitação: não é possível criar a configuração de ponto de extremidade: carga inválida
* **ERR_ENDPOINTCONFIG_112**: configuração de limitação: não é possível criar a configuração de ponto de extremidade: esperando uma carga JSON
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: nome de serviço inválido `<!--<given value>-->`: deve ser &#39;dataSource&#39; ou &#39;action&#39;

O aviso potencial é:

**ERR_ENDPOINTCONFIG_106**: configuração de limitação: máximo de conexões HTTP não definidas: sem limitação por padrão

## Casos de uso

Esta seção lista casos de uso importantes para gerenciar configurações de limite no [!DNL Journey Optimizer] e os comandos de API associados necessários para implementar o caso de uso.

Detalhes sobre cada comando de API estão disponíveis na [descrição da API e coleção do Postman](#description).

+++Criar e implantar uma nova configuração de limitação

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

+++Desimplantar e excluir uma configuração de limite implantada

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`undeploy`** - Desimplanta a configuração.
1. **`delete`** - Remove a configuração.

+++

+++Exclui uma configuração de limite implantada em uma etapa

Em apenas uma chamada de API, você pode desimplantar e excluir a configuração usando o parâmetro `forceDelete`.

Chamadas de API a serem usadas:

1. **`list`** - Recupera as configurações existentes.
1. **`delete`(com parâmetro `forceDelete`)** - Força a exclusão de uma configuração implantada em uma única etapa.

+++

+++Atualizar uma configuração de limitação já implantada

>[!NOTE]
>
>Uma reimplantação é necessária após atualizar uma configuração já implantada.

Chamadas de API a serem usadas:
1. **`list`** - Recupera as configurações existentes.
1. **`get`** - Obtém detalhes de uma configuração específica.
1. **`update`** - Modifica a configuração.
1. **`undeploy`** - Desimplanta a configuração antes de aplicar as alterações.
1. **`candeploy`** - Verifica a qualificação da implantação.
1. **`deploy`** - Implanta a configuração atualizada.

+++
