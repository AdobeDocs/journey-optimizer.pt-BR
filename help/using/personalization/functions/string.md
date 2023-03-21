---
title: Biblioteca de funções da string
description: Biblioteca de funções da string
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: db7c57ce9f5c46d8beb6ff0037a8854fd136cb4a
workflow-type: tm+mt
source-wordcount: '1868'
ht-degree: 7%

---

# Funções de string {#string}

Saiba como usar funções de String no Editor de expressão.

## Camel Case {#camelCase}

O `camelCase` maiúscula a primeira letra de cada palavra de uma string.

**Sintaxe**

```sql
{%= camelCase(string)%}
```

**Exemplo**

A função a seguir capitalizará a primeira letra de palavra no endereço de rua do perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Código de barras em {#char-code-at}

O `charCodeAt` retorna o valor ASCII de um caractere, como a função charCodeAt no JavaScript. Pega uma string e um inteiro (definindo a posição do caractere) como argumentos de entrada e retorna seu valor ASCII correspondente.

**Sintaxe**

```sql
{%= charCodeAt(string,int) %}: int
```

**Exemplo**

A função a seguir retorna o valor ASCII de o, ou seja, 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

O `concat` combina duas strings em uma.

**Sintaxe**

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

**Sintaxe**

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

**Sintaxe**

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

**Sintaxe**

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

**Sintaxe**

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

**Sintaxe**

```sql
{%= encode64(string) %}
```

## Termina com{#endsWith}

O `endsWith` é usada para determinar se uma string termina com uma substring especificada.

**Sintaxe**

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

**Sintaxe**

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

**Sintaxe**

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

**Sintaxe**

```sql
{%= extractEmailDomain(string) %}
```

**Exemplo**

A consulta a seguir extrai o domínio de email do endereço de email pessoal.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Formatar moeda {#format-currency}

O `formatCurrency` é usada para converter qualquer número em sua representação de moeda sensível ao idioma correspondente, dependendo da localidade passada como uma string no segundo argumento.

**Sintaxe**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Exemplo**

Este query retorna £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Obter host de url {#get-url-host}

O `getUrlHost` é usada para recuperar o nome do host de um URL.

**Sintaxe**

```sql
{%= getUrlHost(string) %}: string
```

**Exemplo**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

Retorna &quot;www.myurl.com&quot;

## Obter caminho de url {#get-url-path}

O `getUrlPath` é usada para recuperar o caminho após o nome de domínio de um URL.

**Sintaxe**

```sql
{%= getUrlPath(string) %}: string
```

**Exemplo**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

Retorna &quot;/contact.html&quot;

## Obter protocolo de url {#get-url-protocol}

O `getUrlProtocol` é usada para recuperar o protocolo de um URL.

**Sintaxe**

```sql
{%= getUrlProtocol(string) %}: string
```

**Exemplo**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

Retorna &quot;http&quot;

## Índice De {#index-of}

O `indexOf` é usada para retornar a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

**Sintaxe**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser pesquisada no primeiro parâmetro |

**Exemplo**

```sql
{%= indexOf("hello world","world" ) %}
```

Retorna 6.

## Is empty {#isEmpty}

O `isEmpty` é usada para determinar se uma string está vazia.

**Sintaxe**

```sql
{%= isEmpty(string) %}
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil estiver vazio. Caso contrário, retornará &#39;false&#39;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Is Not Empty {#is-not-empty}

O `isNotEmpty` é usada para determinar se uma string não está vazia.

**Sintaxe**

```sql
{= isNotEmpty(string) %}: boolean
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil não estiver vazio. Caso contrário, retornará &#39;false&#39;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Último Índice De {#last-index-of}

O `lastIndexOf` é usada para retornar a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

**Sintaxe**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser pesquisada no primeiro parâmetro |

**Exemplo**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Retorna 7.

## Aparar à esquerda {#leftTrim}

O `leftTrim` é usada para remover espaços em branco do início de uma string.

**Sintaxe**

```sql
{%= leftTrim(string) %}
```

## Comprimento {#length}

O `length` é usada para obter o número de caracteres em uma string ou expressão.

**Sintaxe**

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

**Sintaxe**

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

## Corresponde {#matches}

O `matches` é usada para determinar se uma string corresponde a uma expressão regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obter mais informações sobre padrões correspondentes em expressões regulares.

**Sintaxe**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Máscara {#mask}

O `Mask` é usada para substituir uma parte de uma string por caracteres &quot;X&quot;.

**Sintaxe**

```sql
{%= mask(string,integer,integer) %}
```

**Exemplo**

O query a seguir substitui a string &quot;123456789&quot; por caracteres &quot;X&quot;, exceto o primeiro e os últimos 2 caracteres.

```sql
{%= mask("123456789",1,2) %}
```

O query retorna `1XXXXXX89`.

## MD5 {#md5}

O `md5` é usada para calcular e retornar o hash md5 de uma string.

**Sintaxe**

```sql
{%= md5(string) %}: string
```

**Exemplo**

```sql
{%= md5("hello world") %}
```

Retorna &quot;5eb63bbbe01eed093cb22bb8f5acdc3&quot;

## Not equal to{#notEqualTo}

O `notEqualTo` é usada para determinar se uma string não é igual à string especificada.

**Sintaxe**

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

## Diferente de Ignorar maiúsculas e minúsculas {#not-equal-with-ignore-case}

O `notEqualWithIgnoreCase` é usada para comparar duas strings que ignoram letras maiúsculas e minúsculas.

**Sintaxe**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser comparada com a primeira string. |

**Exemplo**

A consulta a seguir determina se o nome da pessoa não é &quot;john&quot;, sem distinção entre maiúsculas e minúsculas.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Grupo de expressões regulares{#regexGroup}

O `Group` é usada para extrair informações específicas, com base na expressão regular fornecida.

**Sintaxe**

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
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Substituir {#replace}

O `replace` é usada para substituir uma determinada substring em uma string por outra substring.

**Sintaxe**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual a substring deve ser substituída. |
| `{STRING_2}` | A substring a ser substituída. |
| `{STRING_3}` | A substring de substituição. |

**Exemplo**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Retorna &quot;Hello Mark, aqui está seu boletim informativo mensal!&quot;

## Substituir tudo{#replaceAll}

O `replaceAll` é usada para substituir todas as subsequências de um texto que corresponde à expressão &quot;regex&quot; pela sequência literal de &quot;substituição&quot; especificada. O Regex tem tratamento especial de &quot;\&quot; e &quot;+&quot; e todas as expressões regex seguem a estratégia de escape PQL. A substituição prossegue do início da string para o final, por exemplo, a substituição de &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

**Sintaxe**

```sql
{%= replaceAll(string,string,string) %}
```
>[!NOTE]
>
> Se a expressão regex considerada como segundo argumento for um caractere regex especial, precisamos usar barra invertida dupla (`//`) para lidar com tais casos.
>
> Lista de caracteres regex especiais [., +, *, ?, ^, $, (, ), [, ], {, }, |, \.]
> 
> Isso é resumido em [Documentação do oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}

## Aparar à direita {#rightTrim}

O `rightTrim` é usada para remover espaços em branco do final de uma string.

**Sintaxe**

```sql
{%= rightTrim(string) %}
```

## Dividir {#split}

O `split` é usada para dividir uma string por um determinado caractere.

**Sintaxe**

```sql
{%= split(string,string) %}
```

## Começa com{#startsWith}

O `startsWith` é usada para determinar se uma string começa com uma substring especificada.

**Sintaxe**

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

## Sequência de caracteres para data {#string-to-date}

O `stringToDate` converte um valor de string em um valor de data e hora. São necessários dois argumentos: representação de string de uma representação de data e hora e string do formatador.

**Sintaxe**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## String to integer {#string-to-integer}

O `string_to_integer` é usada para converter um valor de string em um valor inteiro.

**Sintaxe**

```sql
{= string_to_integer(string) %}: int
```

## String para número {#string-to-number}

O `stringToNumber` é usada para converter uma string em número. Retorna a mesma cadeia de caracteres da saída para entrada inválida.

**Sintaxe**

```sql
{%= stringToNumber(string) %}: double
```

## Sub string {#sub-string}

O `Count string` é usada para retornar a substring da expressão da string entre o índice begin e o índice end.
**Sintaxe**

```sql
{= substr(string, integer, integer) %}: string
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

## Para Bool {#to-bool}

O `toBool` é usada para converter um valor de argumento em um valor booleano, dependendo de seu tipo.

**Sintaxe**

```sql
{= toBool(string) %}: boolean
```

## Hora da Data Final {#to-date-time}

O `toDateTime` é usada para converter a string em data. Retorna a data da época como saída para entrada inválida.

**Sintaxe**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Somente Data/Hora {#to-date-time-only}

O `toDateTimeOnly` é usada para converter um valor de argumento em um valor somente de data e hora. Retorna a data da época como saída para entrada inválida. Essa função aceita tipos de campos string, date, long e int.

**Sintaxe**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Aparar {#trim}

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

## Decodificação de URL {#url-decode}

O `urlDecode` é usada para decodificar uma string codificada em url.

**Sintaxe**

```sql
{%= urlDecode(string) %}: string
```

## Codificação de URL {#url-encode}

O `Count only null` é usada para codificar uma string no url.

**Sintaxe**

```sql
{%= urlEncode(string) %}: string
```
