---
title: Biblioteca de funções de string
description: Biblioteca de funções de string
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 1f16b095b3b063f3fb881aee0b2a928644e19143
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 9%

---

# Funções de strings {#string}

Saiba como usar funções de string no editor de personalização.

## Camel Case {#camelCase}

A função `camelCase` coloca a primeira letra de cada palavra de uma cadeia de caracteres em maiúscula.

**Sintaxe**

```sql
{%= camelCase(string)%}
```

**Exemplo**

A função a seguir colocará a primeira letra da palavra em maiúscula no endereço do perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Código de caractere em {#char-code-at}

A função `charCodeAt` retorna o valor ASCII de um caractere, como a função charCodeAt no JavaScript. Ele pega uma string e um inteiro (definindo a posição do caractere) como argumentos de entrada e retorna seu valor ASCII correspondente.

**Sintaxe**

```sql
{%= charCodeAt(string,int) %}: int
```

**Exemplo**

A função a seguir retorna o valor ASCII de ou seja, 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

A função `concat` combina duas cadeias de caracteres em uma.

**Sintaxe**

```sql
{%= concat(string,string) %}
```

**Exemplo**

A função a seguir combinará a cidade e o país do perfil em uma única sequência.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

A função `contains` é usada para determinar se uma cadeia de caracteres contém uma subsequência especificada.

**Sintaxe**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `STRING_1` | A sequência de caracteres a ser verificada. |
| `STRING_2` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `CASE_SENSITIVE` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplos**

* A função a seguir verificará se o nome do perfil contém a letra A (em maiúsculas ou minúsculas). Nesse caso, retornará &#39;true&#39;, ou &#39;false&#39;.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o endereço de email da pessoa contém a cadeia de caracteres &quot;2010@gm&quot;.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## Não contém{#doesNotContain}

A função `doesNotContain` é usada para determinar se uma cadeia de caracteres não contém uma subsequência especificada.

**Sintaxe**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `STRING_1` | A sequência de caracteres a ser verificada. |
| `STRING_2` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `CASE_SENSITIVE` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o endereço de email da pessoa não contém a cadeia de caracteres &quot;2010@gm&quot;.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Não termina com{#doesNotEndWith}

A função `doesNotEndWith` é usada para determinar se uma cadeia de caracteres não termina com uma subsequência especificada.

**Sintaxe**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o endereço de email da pessoa não termina com &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Não inicia com{#doesNotStartWith}

A função `doesNotStartWith` é usada para determinar se uma cadeia de caracteres não inicia com uma subcadeia especificada.

**Sintaxe**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não começa com &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codificação 64{#encode64}

A função `encode64` é usada para codificar uma sequência de caracteres para preservar as Informações Pessoais (PI), se elas forem incluídas, por exemplo, em uma URL.

**Sintaxe**

```sql
{%= encode64(string) %}
```

## Termina com{#endsWith}

A função `endsWith` é usada para determinar se uma sequência de caracteres termina com uma subsequência especificada.

**Sintaxe**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Valores possíveis: true (padrão) / false. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o endereço de email da pessoa termina com &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Igual a{#equals}

A função `equals` é usada para determinar se uma cadeia de caracteres é igual à cadeia especificada, com distinção entre maiúsculas e minúsculas.

**Sintaxe**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa é &quot;John&quot;.

```sql
{%=equals(profile.person.name,"John") %}
```

## Ignorar maiúsculas e minúsculas é igual a{#equalsIgnoreCase}

A função `equalsIgnoreCase` é usada para determinar se uma cadeia de caracteres é igual à cadeia especificada, sem diferenciar maiúsculas de minúsculas.

**Sintaxe**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa é &quot;John&quot;.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Extrair domínio de email {#extractEmailDomain}

A função `extractEmailDomain` é usada para extrair o domínio de um endereço de email.

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

A função `formatCurrency` é usada para converter qualquer número em sua representação de moeda sensível ao idioma correspondente, dependendo da localidade transmitida como uma cadeia de caracteres no segundo argumento.

**Sintaxe**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Exemplo**

Esta consulta retorna £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Obter host de URL {#get-url-host}

A função `getUrlHost` é usada para recuperar o nome de host de uma URL.

**Sintaxe**

```sql
{%= getUrlHost(string) %}: string
```

**Exemplo**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Retorna &quot;www.myurl.com&quot;

## Obter caminho de URL {#get-url-path}

A função `getUrlPath` é usada para recuperar o caminho após o nome de domínio de uma URL.

**Sintaxe**

```sql
{%= getUrlPath(string) %}: string
```

**Exemplo**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Retorna &quot;/contact.html&quot;

## Obter protocolo de URL {#get-url-protocol}

A função `getUrlProtocol` é usada para recuperar o protocolo de uma URL.

**Sintaxe**

```sql
{%= getUrlProtocol(string) %}: string
```

**Exemplo**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Retorna &quot;http&quot;

## Índice de {#index-of}

A função `indexOf` é usada para retornar a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

**Sintaxe**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada no primeiro parâmetro |

**Exemplo**

```sql
{%= indexOf("hello world","world" ) %}
```

Retorna 6.

## Está vazio {#isEmpty}

A função `isEmpty` é usada para determinar se uma cadeia de caracteres está vazia.

**Sintaxe**

```sql
{%= isEmpty(string) %}
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil estiver vazio. Caso contrário, retornará &#39;false&#39;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Não está vazio {#is-not-empty}

A função `isNotEmpty` é usada para determinar se uma cadeia de caracteres não está vazia.

**Sintaxe**

```sql
{= isNotEmpty(string) %}: boolean
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil não estiver vazio. Caso contrário, retornará &#39;false&#39;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Último índice de {#last-index-of}

A função `lastIndexOf` é usada para retornar a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

**Sintaxe**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada no primeiro parâmetro |

**Exemplo**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Retorna 7.

## Cortar à esquerda {#leftTrim}

A função `leftTrim` é usada para remover espaços em branco do início de uma cadeia de caracteres.

**Sintaxe**

```sql
{%= leftTrim(string) %}
```

## Comprimento {#length}

A função `length` é usada para obter o número de caracteres em uma cadeia de caracteres ou expressão.

**Sintaxe**

```sql
{%= length(string) %}
```

**Exemplo**

A função a seguir retorna o comprimento do nome da cidade do perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

## É como{#like}

A função `like` é usada para determinar se uma cadeia de caracteres corresponde a um padrão especificado.

**Sintaxe**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A expressão que deve corresponder à primeira sequência. Há dois caracteres especiais suportados para a criação de uma expressão: `%` e `_`. <ul><li>`%` é usado para representar zero ou mais caracteres.</li><li>`_` é usado para representar exatamente um caractere.</li></ul> |

**Exemplo**

A consulta a seguir recupera todas as cidades em que os perfis vivem contendo o padrão &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Minúsculas{#lower}

A função `lowerCase` converte uma cadeia de caracteres em letras minúsculas.

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

A função `matches` é usada para determinar se uma sequência de caracteres corresponde a uma expressão regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obter mais informações sobre padrões correspondentes em expressões regulares.

**Sintaxe**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Mascarar {#mask}

A função `Mask` é usada para substituir uma parte de uma cadeia de caracteres por caracteres &quot;X&quot;.

**Sintaxe**

```sql
{%= mask(string,integer,integer) %}
```

**Exemplo**

A consulta a seguir substitui a sequência &quot;123456789&quot; por caracteres &quot;X&quot;, com exceção do primeiro e dos últimos 2 caracteres.

```sql
{%= mask("123456789",1,2) %}
```

A consulta retorna `1XXXXXX89`.

## MD5 {#md5}

A função `md5` é usada para calcular e retornar o hash md5 de uma cadeia de caracteres.

**Sintaxe**

```sql
{%= md5(string) %}: string
```

**Exemplo**

```sql
{%= md5("hello world") %}
```

Retorna &quot;5eb63bbbbe01eed093cb22bb8f5acdc3&quot;

## Não é igual a{#notEqualTo}

A função `notEqualTo` é usada para determinar se uma cadeia de caracteres não é igual à cadeia especificada.

**Sintaxe**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não é &quot;John&quot;.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Não é igual a sem diferenciar maiúsculas e minúsculas {#not-equal-with-ignore-case}

A função `notEqualWithIgnoreCase` é usada para comparar duas cadeias de caracteres ignorando maiúsculas e minúsculas.

**Sintaxe**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser comparada com a primeira sequência. |

**Exemplo**

A consulta a seguir determina se o nome da pessoa não é &quot;john&quot;, sem distinção entre maiúsculas e minúsculas.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Grupo de expressão regular{#regexGroup}

A função `Group` é usada para extrair informações específicas, com base na expressão regular fornecida.

**Sintaxe**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING}` | A sequência de caracteres a ser verificada. |
| `{EXPRESSION}` | A expressão regular que deve corresponder à primeira sequência. |
| `{GROUP}` | Grupo de expressão para correspondência. |

**Exemplo**

A consulta a seguir é usada para extrair o nome de domínio de um endereço de email.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Substituir {#replace}

A função `replace` é usada para substituir uma determinada substring em uma string por outra substring.

**Sintaxe**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A cadeia de caracteres em que a subcadeia de caracteres deve ser substituída. |
| `{STRING_2}` | A subcadeia de caracteres a ser substituída. |
| `{STRING_3}` | A substring de substituição. |

**Exemplo**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Retorna &quot;Olá Mark, aqui está seu informativo mensal!&quot;

## Substituir tudo{#replaceAll}

A função `replaceAll` é usada para substituir todas as subsequências de um texto que corresponde à expressão &quot;regex&quot; pela sequência literal &quot;replacement&quot; especificada. O Regex tem manipulação especial de &quot;\&quot; e &quot;+&quot; e todas as expressões regex seguem a estratégia de escape do PQL. A substituição continua do início da string até o fim. Por exemplo, substituir &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

**Sintaxe**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Quando a expressão usada como segundo argumento for um caractere regex especial, use barra invertida dupla (`//`).  Os caracteres de regex especiais são: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Saiba mais em [documentação do Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Cortar à direita {#rightTrim}

A função `rightTrim` remove espaços em branco do final de uma cadeia de caracteres.

**Sintaxe**

```sql
{%= rightTrim(string) %}
```

## SHA256 {#sha256}

A função `SHA256` calcula e retorna o hash sha256 de uma cadeia de caracteres.

**Sintaxe**

```sql
{%= sha256(string) %} : string
```

**Exemplo**

```sql
{%= sha256("Eliechxh")%}
```

retorna: `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

## Divisão {#split}

A função `split` é usada para dividir uma cadeia de caracteres por um determinado caractere.

**Sintaxe**

```sql
{%= split(string,string) %}
```

## Começa com{#startsWith}

A função `startsWith` é usada para determinar se uma sequência de caracteres inicia com uma subsequência especificada.

**Sintaxe**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A sequência de caracteres a ser pesquisada na primeira sequência. |
| `{CASE_SENSITIVE}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como verdadeiro. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;Joe&quot;.

```sql
{%= startsWith(person.name,"Joe") %}
```

## String para data {#string-to-date}

A função `stringToDate` converte um valor de cadeia de caracteres em um valor de data-hora. Leva dois argumentos: representação de string de uma representação de data-hora e representação de string do formatador.

**Sintaxe**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## String para número inteiro {#string-to-integer}

A função `string_to_integer` é usada para converter um valor de cadeia de caracteres em um valor inteiro.

**Sintaxe**

```sql
{= string_to_integer(string) %}: int
```

## String para número {#string-to-number}

A função `stringToNumber` é usada para converter uma cadeia de caracteres em número. Ele retorna a mesma string que a saída para entrada inválida.

**Sintaxe**

```sql
{%= stringToNumber(string) %}: double
```

## Substring {#sub-string}

A função `Count string` é usada para retornar a subcadeia de caracteres da expressão de cadeia de caracteres entre o índice inicial e o índice final.
**Sintaxe**

```sql
{= substr(string, integer, integer) %}: string
```

## Primeira letra da palavra maiúscula{#titleCase}

A função **titleCase** é usada para colocar as primeiras letras de cada palavra de uma cadeia de caracteres em maiúsculas.

**Sintaxe**

```sql
{%= titleCase(string) %}
```

**Exemplo**

Se a pessoa morar na Washington High Street, essa função retornará a Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Para booleano {#to-bool}

A função `toBool` é usada para converter um valor de argumento em um valor booleano, dependendo de seu tipo.

**Sintaxe**

```sql
{= toBool(string) %}: boolean
```

## Para data hora {#to-date-time}

A função `toDateTime` é usada para converter a cadeia de caracteres em data. Retorna a data da época como saída para entrada inválida.

**Sintaxe**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Somente para data e hora {#to-date-time-only}

A função `toDateTimeOnly` é usada para converter um valor de argumento em um valor somente de data e hora. Retorna a data da época como saída para entrada inválida. Esta função aceita os tipos de campo string, date, long e int.

**Sintaxe**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Aparar {#trim}

A função **trim** remove todos os espaços em branco do início e do fim de uma cadeia de caracteres.

**Sintaxe**

```sql
{%= trim(string) %}
```

## Maiúscula{#upper}

A função **upperCase** converte uma cadeia de caracteres em letras maiúsculas.

**Sintaxe**

```sql
{%= upperCase(string) %}
```

**Exemplo**

Esta função converte o sobrenome do perfil em letras maiúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## Decodificação de URL {#url-decode}

A função `urlDecode` é usada para decodificar uma cadeia de caracteres codificada em URL.

**Sintaxe**

```sql
{%= urlDecode(string) %}: string
```

## Codificação de URL {#url-encode}

A função `Count only null` é usada para codificar uma cadeia de caracteres em URL.

**Sintaxe**

```sql
{%= urlEncode(string) %}: string
```
