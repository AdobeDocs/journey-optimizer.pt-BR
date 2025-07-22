---
solution: Journey Optimizer
product: journey optimizer
title: Personalizar conteúdo usando dados de um endpoint externo
description: Saiba como buscar dados dinamicamente de um endpoint externo para personalizar o conteúdo de entrada.
badge: label="Disponibilidade limitada" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---


# Personalizar conteúdo usando dados de um endpoint externo {#data-endpoint}

>[!AVAILABILITY]
>
>Esse recurso só está disponível para algumas organizações (disponibilidade limitada).

O Journey Optimizer permite aproveitar dados de um endpoint externo para personalizar seu conteúdo em canais de entrada, como os canais de Experiência baseada em código, Web e Mensagens no aplicativo.

Para fazer isso, uma função auxiliar dedicada, `externalDataLookup`, está disponível no editor de personalização. Para usar o auxiliar, você deve primeiro definir uma [!DNL Journey Optimizer] **Ação** onde você configura os detalhes sobre o ponto de extremidade externo.

## Leitura obrigatória

### Execução em tempo de execução

Quando uma ação de entrada inclui um auxiliar externalDataLookup, o ponto de extremidade é chamado dinamicamente no momento em que a solicitação de personalização é recebida e processada pelo Edge Network [!DNL Adobe Experience Platform]. Isso significa que o endpoint externo precisa ser capaz de lidar com pelo menos a mesma carga e taxa de transferência simultâneas que o cliente está enviando para a superfície específica para o AEP Edge Network.

### Autenticação

Atualmente, as opções de autenticação na configuração Ação não são suportadas pelo auxiliar externalDataLookup.
Enquanto isso, para a autenticação baseada em chave de API ou outras chaves de autorização de texto sem formatação, você pode especificá-las como campos de cabeçalho na configuração Ação.
SOMENTE para endpoints internos do Adobe: entre em contato com a engenharia da AJO para ativar a autenticação baseada em token de serviço para um endpoint.

### Medidas de proteção e limitações

Consulte Ações personalizadas em Campanhas de canais de entrada do AJO e Jornada#GuardrailsandGuidelines também.

Por padrão, o AJO usa um tempo limite de 300 ms ao chamar um endpoint externo. Entre em contato com a Engenharia da AJO para aumentar esse tempo limite para um endpoint.
No Editor do Personalization, o AJO não permite navegar pelo esquema da resposta do endpoint ao inserir expressões e não valida referências a atributos JSON da resposta usada em expressões.
Os tipos de dados compatíveis com parâmetros de variáveis de carga útil a serem substituídos por meio do externalDataLookup helper são String, Integer, Decimal, Boolean, listString, listInt, listInteger, listDecimal
As alterações na configuração de uma Ação não são refletidas nas chamadas externalDataLookup correspondentes em campanhas e jornadas ativas. Para que uma alteração seja refletida, é necessário copiar ou modificar campanhas ou jornadas ativas que estejam usando a Ação em um auxiliar externalDataLookup.
O uso de variáveis ainda não é suportado nos parâmetros auxiliares da pesquisa de dados externos.
No momento, não há suporte para Caminho dinâmico de URL.  - Aprimoramentos de ações personalizadas de entrada#DynamicPathSegments

## Criar uma ação

Crie uma Ação para configurar o endpoint para a pesquisa. Isso só precisa ser feito uma vez para cada endpoint e deve ser feito por um usuário técnico. Consulte esta página.

A mesma Ação pode ser usada em uma atividade **[!UICONTROL Ação Personalizada]** para buscar conteúdo em uma jornada, e em uma função auxiliar `externalDataLookup` para buscar dados em uma ação de entrada em uma jornada ou campanha.

Navegue até o menu **[!UICONTROL Administração]** / **[!UICONTROL Configurações]**.

Anote a ID de ação e copie-a para uso na etapa 6.


## Personalizar o conteúdo usando dados buscados

### Adicionar a função auxiliar ao conteúdo

1. Crie uma campanha de entrada ou ação de jornada e edite o conteúdo.

1. Localize o conteúdo no qual deseja usar os dados obtidos do endpoint externo e acesse o editor de personalização.

1. Selecione o menu de funções Auxiliares e localize a função auxiliar `externalDataLookup`.

1. Selecione para inserir a sintaxe associada no código e substituir os valores de parâmetros `actionId` e `result` da seguinte maneira:

   * `actionId` : Colar a ID de ação copiada ao criar a Ação.
   * `result`: Defina este parâmetro com o nome de sua escolha. Você usará essa variável de resultado para acessar o conteúdo buscado.

1. Adicione quaisquer valores de parâmetro de variável que serão transmitidos como parte da chamada de endpoint. Por exemplo, veja como você pode passar um parâmetro de idioma e um parâmetro de número máximo de itens.

### Personalizar usando dados buscados

Para acessar os dados buscados de uma chamada de pesquisa de ponto de extremidade externo, você pode referenciar campos definidos na carga da resposta na definição Ação usando expressões de personalização e funções auxiliares.

Use a variável `result` para acessar os dados buscados e inseri-los no conteúdo da ação de entrada. Por exemplo, veja como você pode retornar uma matriz JSON de itens buscados no endpoint.

Vamos ver o exemplo abaixo, em que a carga de resposta na Ação foi configurada da seguinte maneira:

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Exemplo 1 do Personalization - Exibir a descrição do primeiro vídeo em uma ação do Experience HTML baseada em código:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Exemplo 2 do Personalization - Retornar uma matriz de itens em uma ação JSON de experiência baseada em código:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## Tempos limite e tratamento de erros

O AJO usa um tempo limite rigoroso ao chamar o endpoint externo para manter as características de desempenho de baixa latência e alta taxa de transferência do AEP Edge Network.

Se o ponto de extremidade atingir o tempo limite ou se houver qualquer outro tipo de erro que chegue ao ponto de extremidade, a variável resultante estará vazia. Nesse caso, todas as referências a atributos na variável result também estarão vazias. Se você estiver apenas exibindo o atributo no conteúdo, ele será exibido em branco. Se você estiver tentando percorrer um atributo de matriz no resultado, ele não retornará itens.

Se você quiser lidar com tempos limite ou erros de maneira mais adequada mostrando o conteúdo de fallback, poderá verificar se o resultado da pesquisa está vazio e exibir o conteúdo de fallback nesse caso.

Por exemplo, você pode mostrar um valor de fallback para um único atributo como este:

Descrição do primeiro vídeo: {%=result.videos[0].description ?: &quot;nenhum encontrado&quot; %}


ou você pode renderizar condicionalmente um bloco inteiro de conteúdo como este:

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if result%}
... faça algo com o resultado ...
{%else%}
... retornar conteúdo de fallback ...
{%/if%}
Depuração
Para ajudar na depuração, os detalhes de tempo limite e erro para pesquisas de dados externas são incluídos na visualização do Edge Delivery no AEP Assurance. Se você não estiver vendo os resultados esperados para um auxiliar externalDataLookup em uma ação de entrada, é possível iniciar uma sessão do Assurance, iniciar uma chamada do AJO a partir de uma implementação da Web ou móvel e usar a exibição do Edge Delivery para verificar os detalhes do tempo limite ou do erro.

Por exemplo:

Na seção Edge Delivery do rastreamento de garantia como parte dos detalhes de execução, um novo bloco customActions foi adicionado com

detalhes de solicitação e resposta semelhantes ao abaixo. A seção de erros deve ajudar na depuração se houver problemas ao executar uma ação personalizada

## Perguntas frequentes

+++Como passar um atributo contextual da solicitação como parâmetro para uma pesquisa de dados externa?

Use o menu Atributos contextuais > Sequência de dados > Evento para navegar pelo esquema do Evento de experiência que você está usando e insira o atributo relevante como um valor de parâmetro como este:

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++O AJO armazena em cache as respostas do endpoint externo?

No momento não. Esse recurso será compatível no futuro.

+++









Sintaxe
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



Parâmetros de envio
Quando o endpoint externo é chamado, todos os valores de cabeçalho constantes, parâmetros de consulta e valor de carga de solicitação definidos na Ação serão enviados com os valores fornecidos na configuração da Ação.

Para quaisquer valores de cabeçalho de variável, parâmetros de consulta/caminho ou valores de carga de solicitação, você pode transmitir valores dinamicamente usando parâmetros para o auxiliar externalDataLookup.

Nomes dos parâmetros:

Parâmetros de cabeçalho: cabeçalho.&lt;parameter-name>
Parâmetros de consulta: consulta.&lt;parameter-name>
Parâmetros de carga: carga.&lt;parameter-name>
Parâmetros de caminho: dynamic_path.&lt;parameter-name>
Por exemplo:

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
Os valores de parâmetro podem ser valores fixos ou personalizados referenciando campos de perfil ou outros atributos contextuais, por exemplo:

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
Parâmetros de carga podem ser fornecidos usando a notação de pontos para fazer referência a atributos JSON aninhados, por exemplo:

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}