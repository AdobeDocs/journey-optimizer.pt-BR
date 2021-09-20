---
title: Sintaxe de personalização
description: Saiba como usar a sintaxe de personalização
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 395ce682c52880bc67234b254f3ff55fae07f82e
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 4%

---

# Sintaxe de personalização {#personalization-syntax}

A personalização em [!DNL Journey Optimizer] é baseada na sintaxe de modelo chamada Handlebars.
Para obter uma descrição completa da sintaxe Handlebars, consulte a [HandlebarsJS documentation](https://handlebarsjs.com/).

Ele usa um modelo e um objeto de entrada para gerar HTML ou outros formatos de texto. Os modelos Handlebars se parecem com um texto regular com expressões Handlebars incorporadas.

Exemplo de expressão simples:

`{{profile.person.name}}`

em que:

* `profile` é um namespace.
* `person.name` é um token composto por atributos. A estrutura de atributos é definida em um Esquema XDM da Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

## Regras gerais de sintaxe

Os identificadores podem ser qualquer caractere unicode, exceto o seguinte:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

A sintaxe diferencia maiúsculas e minúsculas.

As palavras **true**, **false**, **null** e **undefined** só são permitidas na primeira parte de uma expressão de caminho.

Nos Handlebars, os valores retornados pela {{expression}} são **HTML-escaped**. Se a expressão contiver `&`, a saída de escape de HTML retornada será gerada como `&amp;`. Se você não quiser que o Handlebars escape um valor, use o &quot;traço triplo&quot;.

## Perfil

Este namespace permite fazer referência a todos os atributos definidos no esquema de perfil descrito na [documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

Os atributos precisam ser definidos no schema antes de serem referenciados em um bloco de personalização [!DNL Journey Optimizer].

>[!NOTE]
>
>Saiba como aproveitar os atributos de perfil em condições em [esta seção](functions/helpers.md#if-function).

**Referências de exemplo:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segmentos{#perso-segments}

Saiba como aproveitar os atributos de perfil em condições em [esta seção](functions/helpers.md#if-function).

>[!NOTE]
>Para saber mais sobre o serviço de segmentação e segmentação, consulte [esta seção](../segment/about-segments.md).

## Ofertas

Esse namespace permite fazer referência às decisões de ofertas existentes.
Para fazer referência a uma oferta, você precisa declarar um caminho com as diferentes informações que definem uma oferta.

Esse caminho tem a seguinte estrutura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

em que:

* `offers` identifica a expressão de caminho pertencente ao namespace de oferta
* `Type`  determina o tipo de representação da oferta. Os valores possíveis são: `image`, `html` e `text`
* `Placement Id` e  `Activity Id` são identificadores de inserção e atividade
* `Attributes` são atributos específicos da oferta que dependem do tipo de oferta. Exemplo: `deliveryUrl` para imagens

Para obter mais informações sobre a API de decisões e a Representação de ofertas, consulte [esta página](../../using/offers/api-reference/decisions-api/deliver-offers.md)

Todas as referências são validadas em relação ao Esquema de ofertas com um mecanismo de validação descrito em [esta página](personalization-validation.md)

**Referências de exemplo:**

* Local onde a imagem está hospedada:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL de destino ao clicar na imagem:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Conteúdo de texto da oferta proveniente do mecanismo de decisão:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Conteúdo HTML da oferta proveniente do mecanismo de decisão:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Auxiliares{#helpers-all}

Um Handlebars helper é um identificador simples que pode ser seguido por parâmetros.
Cada parâmetro é uma expressão Handlebars. Essas ajuda podem ser acessadas de qualquer contexto em um modelo.

Esses ajudantes de bloco são identificados por um # anterior ao nome do auxiliar e exigem um fechamento /, correspondente do mesmo nome.
Blocos são expressões que têm um bloco abrindo ({{# }}) e fechando ({{/}}).


>[!NOTE]
>
>As funções de ajuda são detalhadas em [nesta seção](functions/helpers.md).

## Tipos literais

[!DNL Adobe Journey Optimizer] O suporta os seguintes tipos literais:

| Literal | Definição |
| ------- | ---------- |
| String | Um tipo de dados composto por caracteres entre aspas duplas. <br>Exemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Um tipo de dados verdadeiro ou falso. |
| Número inteiro | Um tipo de dados que representa um número inteiro. Pode ser positivo, negativo ou zero. <br>Exemplos: `-201`, `0`, `412` |
| Matriz | Um tipo de dados que é composto como um grupo de outros valores literais. Ele usa colchetes para agrupar e vírgulas para delimitar entre valores diferentes. <br> **Observação:** não é possível acessar diretamente as propriedades dos itens em uma matriz. <br> Exemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>O uso da variável **xEvent** não está disponível em expressões de personalização. Qualquer referência ao xEvent resultará em falhas de validação.

## Personalização de URL{#perso-urls}

O Journey Orchestration permite personalizar um ou vários URLs na mensagem, adicionando campos de personalização a eles. Para fazer isso:

* Crie um link no seu conteúdo de email ou push. Para saber mais sobre a criação de links, consulte [esta página](../message-tracking#insert-links)).
* Clique no ícone de personalização. Este ícone está disponível para estes tipos específicos de links: **Link externo**, **Link de cancelamento de subscrição** e **Opt-Out**.

![](assets/perso-url.png)

>[!NOTE]
>
>No editor de expressão, ao editar um URL personalizado, as funções de ajuda e a associação de segmentos são desativadas por motivos de segurança.

** Exemplos de URLs personalizados **

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

