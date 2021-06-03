---
title: Sintaxe de personalização
description: Saiba como usar a sintaxe de personalização
source-git-commit: 5b7f3f58e7376b45993b6a2edc6e96f824fa2f44
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 4%

---


# Sintaxe de personalização {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

A personalização em [!DNL Journey Optimizer] é baseada na sintaxe de modelo chamada Handlebars.
Para obter uma descrição completa da sintaxe Handlebars, consulte a [HandlebarsJS documentation](https://handlebarsjs.com/).

Ele usa um modelo e um objeto de entrada para gerar HTML ou outros formatos de texto. Os modelos Handlebars se parecem com um texto regular com expressões Handlebars incorporadas.

Exemplo de expressão simples:

```
{{profile.person.name}}
```

em que:

* **O perfil do**  é um namespace.
* **person.** name é um token composto por atributos. A estrutura de atributos é definida em um Esquema XDM da Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR).

## Regras gerais de sintaxe

Os identificadores podem ser qualquer caractere unicode, exceto o seguinte:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

A sintaxe diferencia maiúsculas e minúsculas.

As palavras **true**, **false**, **null** e **undefined** só são permitidas na primeira parte de uma expressão de caminho.

Nos Handlebars, os valores retornados pela {{expression}} são **HTML-escaped**. Se a expressão contiver `&`, a saída de escape de HTML retornada será gerada como `&amp;`. Se você não quiser que o Handlebars escape um valor, use o &quot;traço triplo&quot;.

## Perfil

Esse namespace permite fazer referência a todos os atributos definidos no esquema de perfil descrito na [documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

Os atributos precisam ser definidos no schema antes de serem referenciados em um bloco de personalização [!DNL Journey Optimizer].

>[!NOTE]
>
>Saiba como aproveitar os atributos de perfil em condições em [esta seção](functions/helpers.md#if-function).

**Referências de exemplo:**

```
{{profile.person.name.fullName}}
{{profile.person.name.firstName}}
{{profile.person.gender}}
{{profile.personalEmail.address}}
{{profile.mobilePhone.number}}
{{profile.homeAddress.city}}
{{profile.faxPhone.number}}
```

## Segmentos {#perso-segments}

Saiba como aproveitar os atributos de perfil em condições em [esta seção](functions/helpers.md#if-function).

>[!NOTE]
>Para saber mais sobre o serviço de segmentação e segmentação, consulte [esta seção](../segment/about-segments.md).


## Ofertas

Esse namespace permite fazer referência às decisões de ofertas existentes.
Para fazer referência a uma oferta, você precisa declarar um caminho com as diferentes informações que definem uma oferta.

Esse caminho tem a seguinte estrutura:

```
offers.Type.[Placement Id].[Activity Id].Attribute
```

em que:

* `offers` identifica a expressão de caminho pertencente ao namespace de oferta
* `Type`  determina o tipo de representação da oferta. Os valores possíveis são: `image`, `html` e `text`
* `Placement Id` e  `Activity Id` são identificadores de inserção e atividade
* `Attributes` são atributos específicos da oferta que dependem do tipo de oferta. Exemplo: `deliveryUrl` para imagens.

Para obter mais informações sobre a API de decisões e a Representação de ofertas, consulte [esta página](../../using/offers/api-reference/decisions-api/deliver-offers.md)

Todas as referências são validadas em relação ao Esquema de ofertas com um mecanismo de validação descrito em [this page](personalization-validation.md).

**Referências de exemplo:**

* Local onde a imagem está hospedada:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL de destino ao clicar na imagem:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Conteúdo de texto da oferta proveniente do mecanismo de decisão:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Conteúdo HTML da oferta proveniente do mecanismo de decisão:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Ajuda{#helpers-all}

Um Handlebars helper é um identificador simples que pode ser seguido por parâmetros.
Cada parâmetro é uma expressão Handlebars. Essas ajuda podem ser acessadas de qualquer contexto em um modelo.

Esses ajudantes de bloco são identificados por um # que precede o nome do auxiliar e requer um fechamento /, do mesmo nome correspondente.
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
