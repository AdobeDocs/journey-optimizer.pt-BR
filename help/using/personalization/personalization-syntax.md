---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxe de personalização
description: Saiba como usar a sintaxe de personalização.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, sintaxe, personalização
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 10%

---

# Sintaxe de personalização {#personalization-syntax}

Personalização no [!DNL Journey Optimizer] é baseado na sintaxe de modelo chamada Handlebars.
Para obter uma descrição completa da sintaxe Handlebars, consulte [Documentação do HandlebarsJS](https://handlebarsjs.com/).

Ele usa um modelo e um objeto de entrada para gerar HTML ou outros formatos de texto. Os modelos de Handlebars parecem texto regular com expressões Handlebars incorporadas.

Exemplo de expressão simples:

`{{profile.person.name}}`

em que:

* `profile` é um namespace.
* `person.name` é um token composto por atributos. A estrutura de atributos é definida em um Esquema XDM do Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

## Regras gerais de sintaxe {#general-rules}

Os identificadores podem ser qualquer caractere unicode, exceto para o seguinte:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

A sintaxe diferencia maiúsculas de minúsculas.

As palavras **true**, **false**, **null** e **indefinido** são permitidos somente na primeira parte de uma expressão de caminho.

Em Handlebars, os valores retornados pela variável {{expression}} são **HTML-escaped**. Se a expressão contiver `&`, a saída HTML-escaped retornada será gerada como `&amp;`. Se você não quiser que o Handlebars escape um valor, use o &quot;triple-stash&quot;.

Em relação a argumentos de funções literais, o analisador de linguagem de modelo não suporta barra invertida sem escape única (`\`). Esse caractere deve ser evitado com uma barra invertida adicional (`\`). Exemplo :

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Perfil

Este namespace permite fazer referência a todos os atributos definidos no esquema de perfil descrito em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

Os atributos precisam ser definidos no esquema antes de serem referenciados em um [!DNL Journey Optimizer] bloco de personalização.

>[!NOTE]
>
>Saiba como aproveitar os atributos de perfil nas condições do [nesta seção](functions/helpers.md#if-function).

**Exemplos de referências:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Públicos-alvo{#perso-segments}

Saiba como aproveitar os atributos de perfil nas condições do [nesta seção](functions/helpers.md#if-function).

>[!NOTE]
>Para saber mais sobre o serviço de segmentação, consulte [esta documentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.

## Ofertas {#offers-syntax}

Esse namespace permite fazer referência às decisões de ofertas existentes.
Para fazer referência a uma oferta, é necessário declarar um caminho com as diferentes informações que definem uma oferta.

Esse caminho tem a seguinte estrutura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

em que:

* `offers` identifica a expressão de caminho pertencente ao namespace da oferta
* `Type`  determina o tipo de representação da oferta. Os valores possíveis são: `image`, `html` e `text`
* `Placement Id` e `Activity Id` são identificadores de posicionamento e atividade
* `Attributes` são atributos específicos da oferta que dependem do tipo de oferta. Exemplo: `deliveryUrl` para imagens

Para obter mais informações sobre a API de Decisões e a Representação de ofertas, consulte [esta página](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Todas as referências são validadas em relação ao Esquema de ofertas com um mecanismo de validação descrito em [esta página](personalization-validation.md)

**Exemplos de referências:**

* Local onde a imagem está hospedada:

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL do Target ao clicar na imagem:

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Conteúdo de texto da oferta proveniente do mecanismo de decisão:

  `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Conteúdo HTML da oferta proveniente do mecanismo de decisão:

  `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Auxiliares{#helpers-all}

Um auxiliar do Handlebars é um identificador simples que pode ser seguido por parâmetros.
Cada parâmetro é uma expressão Handlebars. Esses auxiliares podem ser acessados de qualquer contexto em um modelo.

Esses auxiliares de bloco são identificados por um # precedendo o nome do auxiliar e exigem um / de fechamento correspondente, do mesmo nome.
Blocos são expressões que têm uma abertura de bloco ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>As funções auxiliares são detalhadas em [nesta seção](functions/helpers.md).
>

## Tipos literais {#literal-types}

[!DNL Adobe Journey Optimizer] O é compatível com os seguintes tipos literais:

| Literal | Definição |
| ------- | ---------- |
| String | Um tipo de dados composto de caracteres entre aspas duplas. <br>Exemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Um tipo de dados que é verdadeiro ou falso. |
| Número inteiro | Um tipo de dados que representa um número inteiro. Pode ser positivo, negativo ou zero. <br>Exemplos: `-201`, `0`, `412` |
| Matriz | Um tipo de dados que é composto como um grupo de outros valores literais. Ela usa colchetes para agrupar e vírgulas para delimitar entre valores diferentes. <br> **Nota:** Não é possível acessar diretamente as propriedades dos itens em uma matriz. <br> Exemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>A utilização de **xEvent** não está disponível em expressões de personalização. Qualquer referência a xEvent resultará em falhas de validação.

## Personalização de URL{#perso-urls}

Os URLs personalizados levam os recipients para páginas específicas de um site ou para um microsite personalizado, dependendo dos atributos do perfil. No Adobe Journey Optimizer, você pode adicionar personalização a URLs no conteúdo da mensagem. A personalização de URLs pode ser aplicada ao texto e às imagens, e usar dados do perfil ou dados contextuais.

O Journey Optimizer permite personalizar um ou vários URLs em sua mensagem adicionando campos de personalização a eles. Para personalizar um URL, siga as etapas abaixo:

1. Crie um link no conteúdo da mensagem. [Saiba mais](../email/message-tracking.md#insert-links)
1. No ícone de personalização, selecione os atributos. O ícone de personalização só está disponível para estes tipos de links: **Link externo**, **Link de cancelamento de subscrição** e **Recusar**.

   ![](assets/perso-url.png)

>[!NOTE]
>
>No editor de expressão, ao editar um URL personalizado, as funções auxiliares e a associação de públicos-alvo são desabilitadas por motivos de segurança.
>

**Amostras de URLs personalizados**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Não há suporte para espaços nos tokens de personalização usados em urls.
