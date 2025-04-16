---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o editor de expressão avançado
description: Saiba como criar expressões avançadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: editor de expressão, dados, jornada
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 57%

---

# Trabalhar com o editor de expressão avançado {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Sobre o editor de expressão avançado"
>abstract="Use o editor de expressão avançado para criar expressões avançadas em várias telas da interface. Por exemplo, você pode criar expressões ao configurar e usar jornadas e ao definir uma condição de fonte de dados."

Use o editor de expressão avançado do Jornada para criar expressões avançadas em várias telas da interface. Por exemplo, você pode criar expressões ao configurar e usar jornadas e ao definir uma condição de fonte de dados.

Ele também está disponível sempre que for necessário definir parâmetros de ação que exijam manipulações de dados específicos. Você pode usar os dados provenientes dos eventos ou informações adicionais recuperadas da fonte de dados. Em uma jornada, a lista exibida de campos de evento é contextual e varia de acordo com os eventos adicionados na jornada.

![](../assets/journey65.png)


O editor de expressão avançado oferece um conjunto de funções e operadores integrados, permitindo manipular valores e definir uma expressão que se ajuste especificamente às suas necessidades. O editor de expressão avançado também permite definir os valores do parâmetro de fonte de dados externa, manipular campos de mapa e coleções, como eventos de experiência.

>[!NOTE]
>
>As funções e os recursos disponíveis no editor de expressão avançado do Jornada diferem daqueles disponíveis no [editor de personalização](../../personalization/functions/functions.md).

## Acessar o editor de expressão avançado {#accessing-the-advanced-expression-editor}

O editor avançado de expressões pode ser usado para:

* criar [condições avançadas](../condition-activity.md#about_condition) em fontes de dados e informações do evento
* definir [atividades de espera](../wait-activity.md#custom) personalizadas
* definir mapeamento de parâmetros de ação

Quando possível, você pode alternar entre os dois modos usando o botão **[!UICONTROL Modo avançado]** / **[!UICONTROL Modo simples]**. O modo simples é descrito [aqui](../condition-activity.md#about_condition).

>[!NOTE]
>
>* As condições podem ser definidas no editor de expressão simples ou avançado. Eles sempre retornam um tipo booleano.
>
>* Parâmetros de ações podem ser definidos selecionando campos ou por meio do editor de expressão avançado. Eles retornam um tipo de dados específico de acordo com a expressão.

Você pode acessar o editor de expressão avançado de diferentes maneiras:

* Ao criar uma condição de fonte de dados, você pode acessar o editor avançado clicando em **[!UICONTROL Modo avançado]**.

  ![](../assets/journeyuc2_33.png)

* Ao criar um temporizador personalizado, o editor avançado será exibido diretamente.
* Ao mapear o parâmetro de ação, clique em **[!UICONTROL Modo avançado]**.

## Conheça a interface {#discovering-the-interface}

Nesta tela você pode escrever manualmente a expressão.

![](../assets/journey70.png)

Na parte esquerda da tela são exibidos os campos e as funções disponíveis:

* **[!UICONTROL Eventos]**: escolha um dos campos recebidos do evento de entrada. A lista exibida de campos de evento é contextual e varia de acordo com os eventos adicionados na jornada. [Leia mais](../../event/about-events.md)

  >[!CAUTION]
  >
  >O uso de eventos de experiência em expressões/condições de jornada é suportado, mas não recomendado. Se o seu caso de uso exigir o uso de eventos de experiência, considere métodos alternativos, como [atributos computados](../../audience/computed-attributes.md), ou criar um segmento usando os eventos e incorporar esse segmento em [`inAudience` expressões](../../building-journeys/functions/functioninaudience.md).

* **[!UICONTROL Públicos-alvo]**: se você tiver descartado um evento de **[!UICONTROL Qualificação de público-alvo]**, escolha o público-alvo que deseja usar na expressão. [Leia mais](../condition-activity.md#using-a-segment)
* **[!UICONTROL Fontes de dados]**: escolha na lista de campos disponíveis nos grupos de campos de suas fontes de dados. [Leia mais](../../datasource/about-data-sources.md)
* **[!UICONTROL Propriedades da Jornada]**: esta seção reagrupa os campos técnicos relacionados à jornada de um determinado perfil. [Leia mais](journey-properties.md)
* **[!UICONTROL Funções]**: escolha entre uma lista de funções integradas que permitem fazer uma filtragem complexa. As funções são organizadas por categorias. [Leia mais](functions.md)

![](../assets/journey65.png)

Um mecanismo de autopreenchimento exibe sugestões contextuais.

![](../assets/journey68.png)

Um mecanismo de validação de sintaxe verifica a integridade do código. Erros são exibidos na parte superior do editor.

![](../assets/journey69.png)


>[!TIP]
>
>Ao criar condições no editor de expressão avançado, certifique-se de que suas expressões não contenham caracteres ocultos ou não imprimíveis. Além disso, use expressões de linha única para evitar erros de análise.


**Necessidade de parâmetros ao criar condições com o editor de expressão avançado**

Se você selecionar um campo de uma fonte externa de dados que requer um parâmetro para ser chamado (consulte [esta página](../../datasource/external-data-sources.md)), uma nova guia aparecerá à direita para permitir a especificação desse parâmetro. O valor do parâmetro pode vir dos eventos posicionados na jornada ou na fonte de dados do Experience Platform (e não de outras fontes de dados externas). Por exemplo, em uma fonte de dados relacionada ao clima, um parâmetro frequentemente usado será &quot;cidade&quot;. Como resultado, você deve selecionar onde deseja obter o parâmetro cidade. As funções também podem ser aplicadas aos parâmetros para executar alterações de formato ou concatenações.

![](../assets/journeyuc2_19.png)

Para casos de uso mais complexos, caso queira incluir os parâmetros da fonte de dados na expressão principal, é possível definir os valores usando a palavra-chave &quot;params&quot;. Consulte [esta página](../expression/field-references.md).
