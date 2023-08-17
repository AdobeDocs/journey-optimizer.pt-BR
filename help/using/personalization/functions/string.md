---
title: Biblioteca de funções de string
description: Biblioteca de funções de string
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 118eddf540d1dfb3a30edb0b877189ca908944b1
workflow-type: tm+mt
source-wordcount: '1857'
ht-degree: 7%

---

# Funções de string {#string}

Saiba como usar funções de string no editor de expressão.

## Camel Case {#camelCase}

A variável `camelCase` A função coloca a primeira letra de cada palavra de uma string em maiúsculas.

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

A variável `charCodeAt` A função retorna o valor ASCII de um caractere, como a função charCodeAt no JavaScript. Ele pega uma string e um inteiro (definindo a posição do caractere) como argumentos de entrada e retorna seu valor ASCII correspondente.

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

A variável `concat` A função combina duas sequências de caracteres em uma.

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

A variável `contains` é usada para determinar se uma sequência de caracteres contém uma subsequência especificada.

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

A variável `doesNotContain` é usada para determinar se uma sequência de caracteres não contém uma subsequência especificada.

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

A variável `doesNotEndWith` é usada para determinar se uma sequência de caracteres não termina com uma subsequência especificada.

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

## Does not start with{#doesNotStartWith}

A variável `doesNotStartWith` é usada para determinar se uma sequência de caracteres não inicia com uma subsequência especificada.

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

A variável `encode64` Esta função é usada para codificar uma sequência de caracteres para preservar as informações pessoais (PI), se elas forem incluídas, por exemplo, em um URL.

**Sintaxe**

```sql
{%= encode64(string) %}
```

## Termina com{#endsWith}

A variável `endsWith` é usada para determinar se uma sequência de caracteres termina com uma subsequência especificada.

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

A variável `equals` A função é usada para determinar se uma sequência de caracteres é igual à sequência especificada, com distinção entre maiúsculas e minúsculas.

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

A variável `equalsIgnoreCase` A função é usada para determinar se uma sequência de caracteres é igual à sequência especificada, sem distinção entre maiúsculas e minúsculas.

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

A variável `extractEmailDomain` é usada para extrair o domínio de um endereço de email.

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

A variável `formatCurrency` é usada para converter qualquer número em sua representação de moeda sensível ao idioma correspondente, dependendo da localidade transmitida como uma string no segundo argumento.

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

A variável `getUrlHost` é usada para recuperar o nome de host de um URL.

**Sintaxe**

```sql
{%= getUrlHost(string) %}: string
```

**Exemplo**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Retorna &quot;www.myurl.com&quot;

## Obter caminho do URL {#get-url-path}

A variável `getUrlPath` é usada para recuperar o caminho após o nome de domínio de um URL.

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

A variável `getUrlProtocol` é usada para recuperar o protocolo de um URL.

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

A variável `indexOf` é usada para retornar a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

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

## Is empty {#isEmpty}

A variável `isEmpty` é usada para determinar se uma sequência de caracteres está vazia.

**Sintaxe**

```sql
{%= isEmpty(string) %}
```

**Exemplo**

A função a seguir retornará &#39;true&#39; se o número de telefone celular do perfil estiver vazio. Caso contrário, retornará &#39;false&#39;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Não Está Vazio {#is-not-empty}

A variável `isNotEmpty` é usada para determinar se uma sequência de caracteres não está vazia.

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

A variável `lastIndexOf` é usada para retornar a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

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

A variável `leftTrim` Esta função é usada para remover espaços em branco do início de uma sequência de caracteres.

**Sintaxe**

```sql
{%= leftTrim(string) %}
```

## Comprimento {#length}

A variável `length` é usada para obter o número de caracteres em uma cadeia de caracteres ou expressão.

**Sintaxe**

```sql
{%= length(string) %}
```

**Exemplo**

A função a seguir retorna o comprimento do nome da cidade do perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Curtir{#like}

A variável `like` é usada para determinar se uma sequência de caracteres corresponde a um padrão especificado.

**Sintaxe**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A sequência de caracteres a ser verificada. |
| `{STRING_2}` | A expressão que deve corresponder à primeira sequência. Há dois caracteres especiais suportados para criar uma expressão: `%` e `_`. <ul><li>`%` é usado para representar zero ou mais caracteres.</li><li>`_` é usado para representar exatamente um caractere.</li></ul> |

**Exemplo**

A consulta a seguir recupera todas as cidades em que os perfis vivem contendo o padrão &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Minúsculas{#lower}

A variável `lowerCase` converte uma string em letras minúsculas.

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

A variável `matches` é usada para determinar se uma sequência de caracteres corresponde a uma expressão regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obter mais informações sobre padrões correspondentes em expressões regulares.

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

A variável `Mask` é usada para substituir uma parte de uma string por caracteres &quot;X&quot;.

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

A variável `md5` é usada para calcular e retornar o hash md5 de uma sequência de caracteres.

**Sintaxe**

```sql
{%= md5(string) %}: string
```

**Exemplo**

```sql
{%= md5("hello world") %}
```

Retorna &quot;5eb63bbbbe01eed093cb22bb8f5acdc3&quot;

## Not equal to{#notEqualTo}

A variável `notEqualTo` é usada para determinar se uma sequência de caracteres não é igual à sequência especificada.

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

## Diferente de Ignorar Maiúsculas e Minúsculas {#not-equal-with-ignore-case}

A variável `notEqualWithIgnoreCase` é usada para comparar duas sequências de caracteres, ignorando maiúsculas e minúsculas.

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

A variável `Group` é usada para extrair informações específicas, com base na expressão regular fornecida.

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

A variável `replace` Esta função é usada para substituir uma determinada substring em uma string por outra substring.

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

A variável `replaceAll` A função é usada para substituir todas as subsequências de um texto que corresponde à expressão &quot;regex&quot; pela sequência literal &quot;replacement&quot; especificada. O Regex tem tratamento especial de &quot;\&quot; e &quot;+&quot; e todas as expressões regex seguem a estratégia de escape PQL. A substituição continua do início da string até o fim. Por exemplo, substituir &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

**Sintaxe**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Quando a expressão tomada como segundo argumento for um caractere regex especial, use barra invertida dupla (`//`).  Os caracteres de regex especiais são: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Saiba mais em [Documentação do Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Cortar à direita {#rightTrim}

A variável `rightTrim` Esta função remove espaços em branco do final de uma sequência de caracteres.

**Sintaxe**

```sql
{%= rightTrim(string) %}
```

## Dividir {#split}

A variável `split` é usada para dividir uma sequência de caracteres por um determinado caractere.

**Sintaxe**

```sql
{%= split(string,string) %}
```

## Começa com{#startsWith}

A variável `startsWith` é usada para determinar se uma sequência de caracteres inicia com uma subsequência especificada.

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

## Sequência de caracteres para data {#string-to-date}

A variável `stringToDate` converte um valor de string em um valor de data e hora. Leva dois argumentos: representação de string de uma representação de data-hora e representação de string do formatador.

**Sintaxe**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Sequência de caracteres para inteiro {#string-to-integer}

A variável `string_to_integer` é usada para converter um valor de sequência de caracteres em um valor inteiro.

**Sintaxe**

```sql
{= string_to_integer(string) %}: int
```

## Sequência de caracteres para número {#string-to-number}

A variável `stringToNumber` é usada para converter uma sequência de caracteres em número. Ele retorna a mesma string que a saída para entrada inválida.

**Sintaxe**

```sql
{%= stringToNumber(string) %}: double
```

## Substring {#sub-string}

A variável `Count string` Esta função é usada para retornar a subsequência de caracteres da expressão de sequência de caracteres entre o índice inicial e o índice final.
**Sintaxe**

```sql
{= substr(string, integer, integer) %}: string
```

## Primeira letra da palavra maiúscula{#titleCase}

A variável **titleCase** Esta função é usada para colocar as primeiras letras de cada palavra de uma sequência de caracteres em maiúsculas.

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

A variável `toBool` A função é usada para converter um valor de argumento em um valor booleano, dependendo de seu tipo.

**Sintaxe**

```sql
{= toBool(string) %}: boolean
```

## Para data hora {#to-date-time}

A variável `toDateTime` é usada para converter a sequência de caracteres em data. Retorna a data da época como saída para entrada inválida.

**Sintaxe**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Somente para data e hora {#to-date-time-only}

A variável `toDateTimeOnly` é usada para converter um valor de argumento em um valor somente de data e hora. Retorna a data da época como saída para entrada inválida. Esta função aceita os tipos de campo string, date, long e int.

**Sintaxe**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Aparar {#trim}

A variável **aparar** Esta função remove todos os espaços em branco do início e do fim de uma sequência de caracteres.

**Sintaxe**

```sql
{%= trim(string) %}
```

## Maiúscula{#upper}

A variável **upperCase** converte uma string em letras maiúsculas.

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

A variável `urlDecode` é usada para decodificar uma sequência de caracteres codificada em url.

**Sintaxe**

```sql
{%= urlDecode(string) %}: string
```

## Codificação de URL {#url-encode}

A variável `Count only null` é usada para codificar uma sequência de caracteres em url.

**Sintaxe**

```sql
{%= urlEncode(string) %}: string
```
