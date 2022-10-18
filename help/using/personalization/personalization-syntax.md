---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxe de personalização
description: Saiba como usar a sintaxe de personalização.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 9%

---

# Sintaxe de personalização {#personalization-syntax}

Personalização no [!DNL Journey Optimizer] O é baseado na sintaxe de modelo chamada Handlebars.
Para obter uma descrição completa da sintaxe Handlebars, consulte [Documentação HandlebarsJS](https://handlebarsjs.com/).

Ele usa um modelo e um objeto de entrada para gerar HTML ou outros formatos de texto. Os modelos Handlebars se parecem com um texto regular com expressões Handlebars incorporadas.

Exemplo de expressão simples:

`{{profile.person.name}}`

em que:

* `profile` é um namespace.
* `person.name` é um token composto por atributos. A estrutura de atributos é definida em um Esquema XDM da Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

## Regras gerais de sintaxe {#general-rules}

Os identificadores podem ser qualquer caractere unicode, exceto o seguinte:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

A sintaxe diferencia maiúsculas e minúsculas.

As palavras **true**, **false**, **null** e **indefinido** são permitidas somente na primeira parte de uma expressão de caminho.

Em Handlebars, os valores retornados pela variável {{expression}} são **HTML-escaped**. Se a expressão contiver `&`, a saída HTML-escaped retornada é gerada como `&amp;`. Se você não quiser que o Handlebars escape um valor, use o &quot;traço triplo&quot;.

No que diz respeito aos argumentos de funções literais, o analisador de linguagem de modelo não suporta uma barra invertida única sem escape (`\`). Esse caractere deve ser evitado com uma barra invertida adicional (`\`). Exemplo :

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Perfil

Esse namespace permite fazer referência a todos os atributos definidos no esquema de perfil descrito em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

Os atributos precisam ser definidos no schema antes de serem referenciados em um [!DNL Journey Optimizer] bloco de personalização.

>[!NOTE]
>
>Saiba como aproveitar os atributos de perfil nas condições em [esta seção](functions/helpers.md#if-function).

**Referências de exemplo:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segmentos{#perso-segments}

Saiba como aproveitar os atributos de perfil nas condições em [esta seção](functions/helpers.md#if-function).

>[!NOTE]
>Para saber mais sobre o serviço de segmentação e segmentação, consulte [esta seção](../segment/about-segments.md).

## Ofertas {#offers-syntax}

Esse namespace permite fazer referência às decisões de ofertas existentes.
Para fazer referência a uma oferta, você precisa declarar um caminho com as diferentes informações que definem uma oferta.

Esse caminho tem a seguinte estrutura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

em que:

* `offers` identifica a expressão de caminho pertencente ao namespace de oferta
* `Type`  determina o tipo de representação da oferta. Os valores possíveis são: `image`, `html` e `text`
* `Placement Id` e `Activity Id` são identificadores de disposição e atividade
* `Attributes` são atributos específicos da oferta que dependem do tipo de oferta. Exemplo: `deliveryUrl` para imagens

Para obter mais informações sobre a API de decisões e a Representação de ofertas, consulte [esta página](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Todas as referências são validadas em relação ao Esquema de ofertas com um mecanismo de validação descrito em [esta página](personalization-validation.md)

**Referências de exemplo:**

* Local onde a imagem está hospedada:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL de destino ao clicar na imagem:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Conteúdo de texto da oferta proveniente do mecanismo de decisão:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML da oferta proveniente do mecanismo de decisão:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Auxiliares{#helpers-all}

Um Handlebars helper é um identificador simples que pode ser seguido por parâmetros.
Cada parâmetro é uma expressão Handlebars. Essas ajuda podem ser acessadas de qualquer contexto em um modelo.

Esses ajudantes de bloco são identificados por um # anterior ao nome do auxiliar e exigem um fechamento /, correspondente do mesmo nome.
Blocos são expressões que têm uma abertura de bloco ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>As funções de ajuda são detalhadas em [esta seção](functions/helpers.md).

## Tipos literais {#literal-types}

[!DNL Adobe Journey Optimizer] O suporta os seguintes tipos literais:

| Literal | Definição |
| ------- | ---------- |
| String | Um tipo de dados composto por caracteres entre aspas duplas. <br>Exemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Um tipo de dados verdadeiro ou falso. |
| Número inteiro | Um tipo de dados que representa um número inteiro. Pode ser positivo, negativo ou zero. <br>Exemplos: `-201`, `0`, `412` |
| Matriz | Um tipo de dados que é composto como um grupo de outros valores literais. Ele usa colchetes para agrupar e vírgulas para delimitar entre valores diferentes. <br> **Observação:** Não é possível acessar diretamente as propriedades dos itens em uma matriz. <br> Exemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>O uso de **xEvent** não está disponível em expressões de personalização. Qualquer referência ao xEvent resultará em falhas de validação.

## Personalização de URL{#perso-urls}

Os URLs personalizados levam os recipients para páginas específicas de um site ou para um microsite personalizado, dependendo dos atributos do perfil. No Adobe Journey Optimizer, é possível adicionar personalização a URLs no conteúdo da mensagem. A personalização de URLs pode ser aplicada ao texto e às imagens, e usar dados do perfil ou dados contextuais.

O Journey Optimizer permite personalizar um ou vários URLs na mensagem, adicionando campos de personalização a eles. Para personalizar um URL, siga as etapas abaixo:

1. Crie um link no conteúdo da mensagem. [Saiba mais](../design/message-tracking.md#insert-links)
1. No ícone de personalização, selecione os atributos. O ícone de personalização só está disponível para esses tipos de links: **Link externo**, **Link de cancelamento de assinatura** e **Opção de rejeição**.

![](assets/perso-url.png)

>[!NOTE]
>
>No editor de expressão, ao editar um URL personalizado, as funções de ajuda e a associação de segmentos são desativadas por motivos de segurança.

**Amostra de URLs personalizados**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Os espaços não são compatíveis com os tokens de personalização usados nos urls.
