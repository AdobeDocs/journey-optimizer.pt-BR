---
solution: Journey Optimizer
product: journey optimizer
title: Usar ações personalizadas
description: Saiba como usar ações personalizadas
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: action, custom, API, jornada, configuration, service
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Sw-hR0cfAG8Lk8YbhJKj53UqG-er2bC3-7Ijih0PF44
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1024
ht-degree: 8%

---

# Usar ações personalizadas {#use-custom-actions}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar ações personalizadas para conectar uma jornada a um sistema de terceiros por meio de uma chamada de API REST com uma carga JSON, ao mesmo tempo em que aplica políticas de consentimento e governança de dados.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Ações personalizadas"
>abstract="As ações personalizadas permitem configurar a conexão de um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON."

Use ações personalizadas para habilitar a conexão com um sistema de terceiros para enviar mensagens ou chamadas de API. Uma ação pode ser configurada com qualquer serviço de qualquer provedor que possa ser chamado por meio de uma REST API com conteúdo formatado em JSON.

Saiba mais sobre ações personalizadas em [esta seção](../action/action.md).

Saiba como criar e configurar uma ação personalizada em [esta página](../action/about-custom-action-configuration.md).

Saiba como usar respostas de chamada de API de ações personalizadas para personalização em [esta página](../action/action-response.md).

## Consentimento e governança de dados {#privacy}

No Journey Optimizer, você pode aplicar políticas de consentimento e governança de dados às ações personalizadas para impedir que campos específicos sejam exportados para sistemas de terceiros ou excluir clientes que não consentiram em receber comunicações por email, push ou SMS. Para obter mais informações, consulte as seguintes páginas:

* [Governança de dados](../action/action-privacy.md).
* [Consentimento](../action/consent.md).

## Configurar o URL

O painel de configuração da atividade **Ação personalizada** mostra os parâmetros de configuração de URL e os parâmetros de autenticação configurados para a ação personalizada. Não é possível definir a parte estática do URL na jornada, mas na configuração global da ação personalizada. [Saiba mais](../action/about-custom-action-configuration.md).

### Caminho dinâmico

Se a URL incluir um caminho dinâmico, especifique o caminho no campo **[!UICONTROL Caminho]**.

Para concatenar campos e cadeias de caracteres de texto sem formatação, use as funções String ou o sinal de adição (+) no editor de expressão avançado. Coloque cadeias de texto sem formatação entre aspas simples (&#39;) ou entre aspas duplas (&quot;). [Saiba mais](expression/expressionadvanced.md).

Esta tabela mostra um exemplo de configuração:

| Campo | Valor |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Caminho | `The _id + '/messages'` |

O URL concatenado tem este formato:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![Configuração de URL de ação personalizada com mapeamento de parâmetro dinâmico](assets/journey-custom-action-url.png)

### Cabeçalhos e parâmetros de consulta {#headers}

A seção **[!UICONTROL Configuração de URL]** mostra os campos de cabeçalho dinâmico e parâmetro de consulta, mas não os campos constantes. Os campos de parâmetro de cabeçalho e consulta dinâmicos são definidos como variáveis na tela de configuração de ação. [Saiba mais](../action/about-custom-action-configuration.md#url-configuration)

Para especificar o valor dos campos de cabeçalho dinâmico e parâmetro de consulta, clique dentro do campo ou no ícone de lápis e selecione o campo desejado.

![Configuração do campo de cabeçalho dinâmico na ação personalizada](assets/journey-dynamicheaderfield.png)

## Parâmetros de ação

Na seção **[!UICONTROL Parâmetros de ação]**, você verá os parâmetros de mensagem definidos como _&quot;Variável&quot;_. Para esses parâmetros, você pode definir onde obter essas informações (por exemplo: eventos, fontes de dados), transmitir valores manualmente ou usar o editor de expressão avançado para casos de uso avançados. Casos de uso avançados podem ser manipulação de dados e outro uso de função. Consulte esta [página](expression/expressionadvanced.md).

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página explica como adicionar e configurar uma atividade de ação personalizada em uma jornada para chamar uma API REST de terceiros com uma carga JSON, incluindo configuração de URL, mapeamento de parâmetro de cabeçalho/consulta, mapeamento de parâmetro de ação e aplicação de políticas de consentimento e governança de dados.

**Intenções:**

* Adicione uma atividade de ação personalizada a uma jornada para enviar dados a um sistema de terceiros por meio da API REST
* Configure um caminho de URL dinâmico concatenando campos e texto estático no editor de expressão
* Mapear valores de parâmetro de consulta e cabeçalho dinâmico a partir de eventos de jornada ou fontes de dados
* Mapear parâmetros de ação (definidos como Variável) para campos de evento, campos de fonte de dados ou valores estáticos
* Aplicar políticas de consentimento e governança de dados para controlar quais dados são exportados por meio de ações personalizadas

**Glossário:**

* **Ação personalizada**: uma atividade de ação de jornada que chama um ponto de extremidade de API REST externo com uma carga de formato JSON para integrar sistemas de terceiros *(específico do produto)*
* **Caminho dinâmico**: a parte variável da URL de ação personalizada que é definida por execução usando campos do contexto de jornada *(específico do produto)*
* **Parâmetros de ação**: campos de carga de mensagem definidos como &quot;Variável&quot; na configuração de ação personalizada, mapeados para dados de jornada no nível de jornada *(específico do produto)*

**Medidas de Proteção:**

* A parte estática do URL não pode ser modificada na jornada; ele deve ser definido na configuração de ação personalizada global.
* Os campos de parâmetro de cabeçalho e consulta dinâmicos são definidos como variáveis na tela de configuração da ação, não na jornada.
* As políticas de consentimento e governança de dados podem ser aplicadas para impedir que campos específicos sejam exportados ou para excluir clientes não consentidos.

**Terminologia:**

* Nome canônico: Ação personalizada — Acrônimo: none — variantes: ações personalizadas, ação de terceiros
* Sinônimos: &quot;parâmetros de ação&quot; = &quot;parâmetros de mensagem definidos como Variável&quot;
* Não confunda: &quot;parte estática do URL&quot; (definida na configuração de ação global, não editável no jornada) ≠ &quot;caminho dinâmico&quot; (definido no jornada por execução)

**Perguntas frequentes:**

* **P: Posso alterar a URL base de uma ação personalizada dentro da jornada?** — Não, somente a parte do caminho dinâmico pode ser definida na jornada; a parte estática do URL é configurada na configuração de ação personalizada global.
* **P: Como criar um caminho de URL dinâmico que inclua uma ID de perfil?** — Use o campo Path com o editor de expressão avançado para concatenar o campo de ID com cadeias de caracteres estáticas, por exemplo: `_id + '/messages'`.
* **P: Como aplicar regras de consentimento a uma ação personalizada?** — configure políticas de consentimento sobre a ação personalizada para excluir clientes que não consentiram em receber a comunicação relevante; consulte a página Consentimento para obter detalhes.
* **P: Onde mapear os valores para cabeçalhos dinâmicos?** — Na seção Configuração de URL do painel de atividades, clique dentro do campo de cabeçalho dinâmico ou use o ícone de lápis para selecionar o campo desejado a partir de eventos ou fontes de dados.
* **P: Que tipos de valores posso atribuir aos parâmetros de ação?** — É possível mapear parâmetros para campos de evento, campos de origem de dados, transmitir valores manualmente ou usar o editor de expressão avançado para manipulação de dados.

+++
