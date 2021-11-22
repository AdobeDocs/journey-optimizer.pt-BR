---
title: Auxiliares
description: Auxiliares
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 5df4856c7be31a75116d906320ae50cd5dc6a2dc
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 4%

---

# Auxiliares {#gs-helpers}

## Valor de Fallback Padrão{#default-value}

O `Default Fallback Value` helper é usado para retornar um valor de fallback padrão se um atributo estiver vazio ou nulo. Esse mecanismo funciona para atributos de perfil e eventos do Jornada.

**Sintaxe**

```sql
Hello {%=profile.personalEmail.name.firstName ?: 'there' %}!
```

Neste exemplo, o valor `there` é exibido se a variável `firstName` deste perfil está vazio ou é nulo.

## Condições{#if-function}

O `if` helper é usado para definir um bloco condicional.
Se a avaliação da expressão retornar true, o bloco será renderizado, caso contrário, será ignorado.

**Sintaxe**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Seguindo `if` auxiliar, você pode inserir um `else` para especificar um bloco de código a ser executado, se a mesma condição for false.
O `elseif` especificará uma nova condição para testar se a primeira instrução retorna false.


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

1. **Determinar a extensão de endereço de email**

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

   A operação a seguir adicionará um link ao site &#39;www.adobe.com/academia&#39; somente para perfis com endereços de email &#39;.edu&#39;, ao site &#39;www.adobe.com/org&#39; para perfis com endereços de email &#39;.org&#39; e ao URL padrão &#39;www.adobe.com/users&#39; para todos os outros perfis:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Conteúdo condicional baseado na associação de segmento**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **Determine se um perfil já é membro**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Para saber mais sobre o serviço de segmentação e segmentação, consulte esta seção [seção](../../segment/about-segments.md).


## Exceto{#unless}

O `unless` helper é usado para definir um bloco condicional. Por oposição à `if`  auxiliar, se a avaliação da expressão retornar false, o bloco será renderizado.

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

## Cada{#each}

O `each` helper é usado para iterar sobre uma matriz.
A sintaxe do auxiliar é ```{{#each ArrayName}}``` SeuConteúdo {{/each}} Podemos fazer referência a itens de matriz individuais usando a palavra-chave **this** dentro do bloco. O índice do elemento da matriz pode ser renderizado usando {{@index}}.

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

O `with` helper é usado para alterar o token de avaliação da parte do modelo.

**Sintaxe**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

O `with` O helper é útil para definir uma variável de atalho também.

**Exemplo**

Use com para aliasing de nomes de variáveis longas para nomes mais curtos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

O `let` permite que uma expressão seja armazenada como uma variável para ser usada posteriormente em uma query.

**Sintaxe**

```sql
{% let variable = expression %} {{variable}}
```

**Exemplo**

O exemplo a seguir permite todos os totais de produtos com a transação em USD, onde a soma é maior que $100 e menor que $1000.

```sql
{% let variable = expression %} {{variable}}
```
