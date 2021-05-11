---
title: Biblioteca de funções
description: Biblioteca de funções
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 8%

---

# Funções de string {#string}

![](../../assets/do-not-localize/badge.png)


Funções da string CJM TBC

## Like

A função `like` é usada para determinar se uma string corresponde a um padrão especificado.

**Formato**

```sql
like ({STRING_1},{STRING_2})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A expressão a ser comparada com a primeira string. Há dois caracteres especiais compatíveis para criar uma expressão: `%` e `_`. <ul><li>`%` é usada para representar zero ou mais caracteres.</li><li>`_` é usada para representar exatamente um caractere.</li></ul> |

**Exemplo**

A consulta a seguir recupera todas as cidades que contêm o padrão &quot;es&quot;.

```sql
like (city ,"%es%")
```

## Começa com

A função `startsWith` é usada para determinar se uma string começa com uma substring especificada.

**Formato**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{BOOLEAN}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;Joe&quot;.

```sql
startsWith(person.name,"Joe")
```

## Does not start with

A função `doesNotStartWith` é usada para determinar se uma string não inicia com uma substring especificada.

**Formato**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{BOOLEAN}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não inicia com &quot;Joe&quot;.

```sql
doesNotStartWith(person.name,"Joe")
```

## Termina com

A função `endsWith` é usada para determinar se uma string termina com uma substring especificada.

**Formato**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{BOOLEAN}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa termina com &quot;.com&quot;.

```sql
endsWith(person.emailAddress,".com")
```

## Não termina com

A função `doesNotEndWith` é usada para determinar se uma string não termina com uma substring especificada.

**Formato**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{BOOLEAN}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa não termina com &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contains

A função `contains` é usada para determinar se uma string contém uma substring especificada.

**Formato**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{BOOLEAN}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa contém a string &quot;2010@gm&quot;.

```sql
contains(person.emailAddress,"2010@gm")
```

## Não contém

A função `doesNotContain` é usada para determinar se uma string não contém uma substring especificada.

**Formato**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser procurada na primeira string. |
| `{BOOLEAN}` | Um parâmetro opcional para determinar se a verificação diferencia maiúsculas de minúsculas. Por padrão, isso é definido como true. |

**Exemplo**

A consulta a seguir determina, com diferenciação entre maiúsculas e minúsculas, se o endereço de email da pessoa não contém a string &quot;2010@gm&quot;.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## Igual a

A função `equals` é usada para determinar se uma string é igual à string especificada.

**Formato**

```sql
equals({STRING_1},{STRING_2})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser comparada com a primeira string. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa é &quot;John&quot;.

```sql
equals(person.name,"John")
```

## Not equal to

A função `notEqualTo` é usada para determinar se uma string não é igual à string especificada.

**Formato**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argumento | Descrição |
| --------- | ----------- |
| `{STRING_1}` | A string na qual executar a verificação. |
| `{STRING_2}` | A string a ser comparada com a primeira string. |

**Exemplo**

A consulta a seguir determina, com distinção entre maiúsculas e minúsculas, se o nome da pessoa não é &quot;John&quot;.

```sql
notEqualTo(person.name,"John")
```

## Corresponde

A função `matches` é usada para determinar se uma string corresponde a uma expressão regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obter mais informações sobre padrões correspondentes em expressões regulares.

**Formato**

```sql
matches({STRING_1},STRING_2})
```

**Exemplo**

A consulta a seguir determina, sem distinção entre maiúsculas e minúsculas, se o nome da pessoa começa com &quot;John&quot;.

```sql
matches(person.name.,"(?i)^John")
```

## Grupo de expressões regulares

A função `regexGroup` é usada para extrair informações específicas, com base na expressão regular fornecida.

**Formato**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Exemplo**

A consulta a seguir é usada para extrair o nome de domínio de um endereço de email.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
