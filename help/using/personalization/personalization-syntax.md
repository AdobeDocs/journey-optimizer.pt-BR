---
title: Sintaxe de personalização
description: Saiba como usar a sintaxe de personalização
translation-type: tm+mt
source-git-commit: e73b47ab6243b13f82aa1503bd8c751f976f29ee
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 3%

---

# Sintaxe de personalização {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## Introdução

A personalização no Journey Optimizer é baseada na sintaxe de modelo chamada Handlebars.
Para obter uma descrição completa da sintaxe Handlebars, consulte [HandlebarsJS](https://handlebarsjs.com/).

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

Nos Handlebars, os valores retornados pela {{expression}} são **HTML-escaped**. Se a expressão contiver &amp;, a saída de saída de HTML retornada será gerada como &amp;. Se você não quiser que o Handlebars escape um valor, use o &quot;traço triplo&quot;.

## Perfil

Esse namespace permite fazer referência a todos os atributos definidos no esquema de perfil descrito na [documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

Os atributos precisam ser definidos no schema antes de serem referenciados em um bloco de personalização do Journey Optimizer.

Todas as referências são validadas em relação ao Esquema de perfil com um mecanismo de validação descrito [aqui](personalization-validation.md).

**Referências de exemplo:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**Determine a extensão** do endereço de email:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## Segmentos

Para saber mais sobre o serviço de segmentação e segmentação, consulte esta [seção](../segment/about-segments.md).

**Renderizar conteúdo diferente com base na associação** de segmento:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**Determine se um perfil já é membro**:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## Ofertas

Esse namespace permite fazer referência às decisões de ofertas existentes.
Para fazer referência a uma oferta, você precisa declarar um caminho com as diferentes informações que definem uma oferta.

Esse caminho tem a seguinte estrutura:
0 - &#39;ofertas&#39; : identifica a expressão de caminho pertencente ao namespace de oferta
1 - Tipo : determina o tipo de representação da oferta. Os valores válidos são &#39;image&#39;, &#39;html&#39; e &#39;text&#39;
2 - Id De Disposição
3 - Id Da Atividade
4 - Atributos específicos da oferta. Dependendo do tipo de oferta, os atributos compatíveis podem ser usados. Por exemplo, para imagens `deliveryUrl`.

Para obter mais informações sobre a API de decisões, consulte esta [página](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api).

Para obter mais informações sobre Representação de ofertas, consulte esta [página](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

Todas as referências são validadas em relação ao Esquema de ofertas com um mecanismo de validação descrito [aqui](personalization-validation.md).

**Referências de exemplo:**

* Local onde a imagem está hospedada:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* URL de destino ao clicar na imagem:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Conteúdo de texto da oferta proveniente do mecanismo de decisão:

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* Conteúdo HTML da oferta proveniente do mecanismo de decisão:

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Ajudantes

Um Handlebars helper é um identificador simples que pode ser seguido por parâmetros.
Cada parâmetro é uma expressão Handlebars. Essas ajuda podem ser acessadas de qualquer contexto em um modelo.

Esses ajudantes de bloco são identificados por um # que precede o nome do auxiliar e requer um fechamento /, do mesmo nome correspondente.
Blocos são expressões que têm um bloco abrindo ({{# }}) e fechando ({{/}}).

### Se

O auxiliar **if** é usado para definir um bloco condicional.
Se a avaliação da expressão retornar true, o bloco será renderizado, caso contrário, será ignorado.

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Após o auxiliar **if**, você pode inserir uma instrução **else** para especificar um bloco de código a ser executado, se a mesma condição for falsa.
A instrução **else if** especificará uma nova condição para testar se a primeira instrução retornará false.

**Renderizar diferentes links de armazenamento com base em expressões** condicionais:

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### Exceto

**#** unless helper é usado para definir um bloco condicional. Por oposição ao auxiliar **#if**, se a avaliação da expressão retornar false, o bloco será renderizado.

**Renderize algum conteúdo com base na extensão** de endereço de email:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### Cada

O auxiliar **each** é usado para iterar sobre uma matriz.
A sintaxe do auxiliar é ```{{#each ArrayName}}``` YourContent {{/each}}
Podemos fazer referência aos itens de matriz individuais usando a palavra-chave **this** dentro do bloco. O índice do elemento da matriz pode ser renderizado usando {{@index}}.

Exemplo:

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Renderize uma lista de produtos que este usuário tem em seu carrinho**:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### Com

O auxiliar **#with** é usado para alterar o token de avaliação da parte do modelo.

Exemplo:

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

O auxiliar **#with** também é útil para definir uma variável de atalho.

**Use com para aliasing de nomes de variáveis longas para nomes** mais curtos:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## Limitações

* O uso da variável **xEvent** não está disponível em expressões de personalização. Qualquer referência ao xEvent resultará em falhas de validação.
