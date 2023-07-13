---
title: Auxiliares
description: Auxiliares
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 4%

---

# Auxiliares {#gs-helpers}

## Valor de fallback padrão{#default-value}

A variável `Default Fallback Value` o auxiliar é usado para retornar um valor de fallback padrão se um atributo estiver vazio ou for nulo. Esse mecanismo funciona para atributos de Perfil e eventos de Jornada.

**Sintaxe**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

Neste exemplo, o valor `there` é exibido se a variável `firstName` o atributo deste perfil está vazio ou é nulo.

## Condições{#if-function}

A variável `if` o auxiliar é usado para definir um bloco condicional.
Se a expressão evaluation retornar true, o bloco será renderizado, caso contrário, será ignorado.

**Sintaxe**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Na sequência da `if` auxiliar, você pode inserir um `else` para especificar um bloco de código a ser executado, se a mesma condição for falsa.
A variável `elseif` especificará uma nova condição para testar se a primeira declaração retorna false.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Exemplos**

1. **Renderizar diferentes links de armazenamento com base em expressões condicionais**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Determinar extensão de endereço de email**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Adicionar um link condicional**

   A operação a seguir adicionará um link para o site &#39;www.adobe.com/academia&#39; para perfis com endereços de email &#39;.edu&#39; somente, para o site &#39;www.adobe.com/org&#39; para perfis com endereços de email &#39;.org&#39; e o URL padrão &#39;www.adobe.com/users&#39; para todos os outros perfis:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Conteúdo condicional com base na associação do público-alvo**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Para saber mais sobre públicos-alvo e o serviço de segmentação, consulte este [seção](../../audience/about-audiences.md).


## A menos que{#unless}

A variável `unless` o auxiliar é usado para definir um bloco condicional. Em oposição ao The `if`  helper, se a expressão evaluation retornar false, o bloco será renderizado.

**Sintaxe**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exemplo**

Renderize algum conteúdo com base na extensão de endereço de email:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Each{#each}

A variável `each` o auxiliar é usado para iterar sobre uma matriz.
A sintaxe do auxiliar é ```{{#each ArrayName}}``` SeuConteúdo {{/each}}
Podemos consultar os itens de matriz individuais usando a palavra-chave **este** dentro do bloco. O índice do elemento da matriz pode ser renderizado usando {{@index}}.

**Sintaxe**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**Exemplo**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Exemplo**

Renderize uma lista de produtos que este usuário tem em seu carrinho:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## Com{#with}

A variável `with` o auxiliar é usado para alterar o token de avaliação da parte do modelo.

**Sintaxe**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

A variável `with` O auxiliar também é útil para definir uma variável de atalho.

**Exemplo**

Use com para suavizar nomes de variáveis longos para nomes mais curtos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

A variável `let` permite que uma expressão seja armazenada como uma variável a ser usada posteriormente em uma query.

**Sintaxe**

```sql
{% let variable = expression %} {{variable}}
```

**Exemplo**

O exemplo a seguir permite que todas as somas de totais de produtos com a transação em USD onde a soma é maior que $100 e menor que $1000.

```sql
{% let variable = expression %} {{variable}}
```
