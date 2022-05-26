---
title: Biblioteca de funções da string
description: Biblioteca de funções da string
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: b9ebacf410f268e19bbaf1d43ee98f5376d0913f
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 7%

---

# Funções de string {#string}

Saiba como usar funções de String no Editor de expressão.

## Camel Case {#camelCase}

O `camelCase` maiúscula a primeira letra de cada palavra de uma string.

**Formato**

```sql
{%= camelCase(string)%}
```

**Exemplo**

A função a seguir capitalizará a primeira letra de palavra no endereço de rua do perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

O `concat` combina duas strings em uma.

**Formato**

```sql
{%= concat(string,string) %}
```

**Exemplo**

A função a seguir combinará a cidade e o país do perfil em uma única string.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

O `contains` é usada para determinar se uma string contém uma substring especificada.

**Formato**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `STRING_1` | A string na qual executar a verificação. |
| `STRING_2` | A string a ser procurada na primeira string. |
| `CASE_SENSITIVE` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplos**

* A função a seguir verificará se o nome do perfil contém a letra A (em maiúsculas ou minúsculas). Se esse for o caso, ele retornará &#39;true&#39;, caso contrário, retornará &#39;false&#39;.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa contém a string &quot;2010@gm&quot;.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## Não contém{#doesNotContain}

O `doesNotContain` é usada para determinar se uma string não contém uma substring especificada.

**Formato**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `STRING_1` | A string na qual executar a verificação. |
| `STRING_2` | A string a ser procurada na primeira string. |
| `CASE_SENSITIVE` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa não contém a string &quot;2010@gm&quot;.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Não termina com{#doesNotEndWith}

O `doesNotEndWith` é usada para determinar se uma string não termina com uma substring especificada.

**Formato**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa não termina com &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Does not start with{#doesNotStartWith}

O `doesNotStartWith` é usada para determinar se uma string não inicia com uma substring especificada.

**Formato**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não inicia com &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codificação 64{#encode64}

O `encode64` é usada para codificar uma string para preservar as Informações pessoais (PI), caso deseje ser incluída, por exemplo, em um URL.

**Formato**

```sql
{%= encode64(string) %}
```

## Termina com{#endsWith}

O `endsWith` é usada para determinar se uma string termina com uma substring especificada.

**Formato**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa termina com &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Igual a{#equals}

O `equals` é usada para determinar se uma string é igual à string especificada, com diferenciação entre maiúsculas e minúsculas.

**Formato**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser comparada com a primeira string. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa é &quot;John&quot;.

```sql
{%=equals(profile.person.name,"John") %}
```

## Igual a Ignorar Maiúsculas e Minúsculas{#equalsIgnoreCase}

O `equalsIgnoreCase` é usada para determinar se uma string é igual à string especificada, sem diferenciação entre maiúsculas e minúsculas.

**Formato**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser comparada com a primeira string. |

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa é &quot;John&quot;.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Extrair domínio de email {#extractEmailDomain}

O `extractEmailDomain` é usada para extrair o domínio de um endereço de email.

**Formato**

```sql
{%= extractEmailDomain(string) %}
```

**Exemplo**

A consulta a seguir extrai o domínio de email do endereço de email pessoal.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Is empty {#isEmpty}

O `isEmpty` é usada para determinar se uma string está vazia.

**Formato**

```sql
{%= isEmpty(string) %}
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil estiver vazio. Caso contrário, retornará &#39;false&#39;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Aparar à esquerda {#leftTrim}

O `leftTrim` é usada para remover espaços em branco do início de uma string.

**Formato**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

O `length` é usada para obter o número de caracteres em uma string ou expressão.

**Formato**

```sql
{%= length(string) %}
```

**Exemplo**

A função a seguir retorna o comprimento do nome da cidade do perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Like{#like}

O `like` é usada para determinar se uma string corresponde a um padrão especificado.

**Formato**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A expressão a ser comparada com a primeira string. Há dois caracteres especiais compatíveis para criar uma expressão: `%` e `_`. <ul><li>`%` é usada para representar zero ou mais caracteres.</li><li>`_` é usada para representar exatamente um caractere.</li></ul> |

**Exemplo**

O query a seguir recupera todas as cidades em que os perfis vivem contendo o padrão &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Minúsculas{#lower}

O `lowerCase` converte uma string em letras minúsculas.

**Sintaxe**

```sql
{%= lowerCase(string) %}
```

**Exemplo**

Essa função converte o nome do perfil em letras minúsculas.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Corresponde{#matches}

O `matches` é usada para determinar se uma string corresponde a uma expressão regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obter mais informações sobre padrões correspondentes em expressões regulares.

**Formato**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Máscara (#mask)

O `Mask` é usada para substituir uma parte de uma string por caracteres &quot;X&quot;.

**Formato**

```sql
{%= mask(string,integer,integer) %}
```

**Exemplo**

O query a seguir substitui a string &quot;123456789&quot; por caracteres &quot;X&quot;, exceto o primeiro e os últimos 2 caracteres.

```sql
{%= mask("123456789",1,2) %}
```

O query retorna `1XXXXXX89`.

## Not equal to{#notEqualTo}

O `notEqualTo` é usada para determinar se uma string não é igual à string especificada.

**Formato**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser comparada com a primeira string. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não é &quot;John&quot;.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Grupo de expressões regulares{#regexGroup}

O `Group` é usada para extrair informações específicas, com base na expressão regular fornecida.

**Formato**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING}` | A string na qual executar a verificação. |
| `{EXPRESSION}` | A expressão regular que deve corresponder à primeira string. |
| `{GROUP}` | Grupo de expressões para corresponder. |

**Exemplo**

A consulta a seguir é usada para extrair o nome de domínio de um endereço de email.

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Substituir {#replace}

O `replace` é usada para substituir uma determinada substring em uma string por outra substring.

**Formato**

```sql
{%= replace(string,string,string) %}
```

**Exemplo**

A seguinte função .

```sql

```


## Substituir tudo{#replaceAll}

O `replaceAll` é usada para substituir todas as subsequências de texto que correspondem ao &quot;target&quot; pela sequência literal de &quot;substituição&quot; especificada. A substituição prossegue do início da string para o final, por exemplo, a substituição de &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

**Formato**

```sql
{%= replaceAll(string,string,string) %}
```


## Aparar à direita {#rightTrim}

O `rightTrim` é usada para remover espaços em branco do final de uma string.


**Formato**

```sql
{%= rightTrim(string) %}
```

## Dividir {#split}

O `split` é usada para dividir uma string por um determinado caractere.

**Formato**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## Começa com{#startsWith}

O `startsWith` é usada para determinar se uma string começa com uma substring especificada.

**Formato**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;Joe&quot;.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Caso de título{#titleCase}

O **titleCase** é usada para capitalizar as primeiras letras de cada palavra de uma string.

**Sintaxe**

```sql
{%= titleCase(string) %}
```

**Exemplo**

Se a pessoa vive na rua alta de Washington, essa função retornará a Rua Alta de Washington.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Aparar{#trim}

O **trim** remove todos os espaços em branco do início e do final de uma string.

**Sintaxe**

```sql
{%= trim(string) %}
```

## Maiúscula{#upper}

O **upperCase** converte uma string em letras maiúsculas.

**Sintaxe**

```sql
{%= upperCase(string) %}
```

**Exemplo**

Essa função converte o sobrenome do perfil em letras maiúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
