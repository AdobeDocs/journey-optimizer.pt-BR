---
product: journey optimizer
title: Funções de string
description: Saiba mais sobre funções de string
feature: Journeys
role: Developer
level: Experienced
keywords: string, funções, expressão, jornada, texto, manipulação
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 15%

---

# Funções de string {#string-functions}

As funções de string permitem manipular e trabalhar com valores de texto nas expressões de jornada. Essas funções são essenciais para o processamento, validação, transformação e análise de texto nas jornadas do cliente.

Use funções de string quando precisar:

* Concatenar e combinar vários valores de texto ([concat](#concat))
* Pesquisar padrões ou subcadeias de texto específicos ([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp))
* Comparar cadeias de caracteres com correspondência que diferencia maiúsculas de minúsculas ou que não diferencia maiúsculas de minúsculas ([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase))
* A verificação da cadeia de caracteres inicia e termina ([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase))
* Extrair partes do texto usando operações de subcadeia de caracteres ([substr](#substr))
* Transformar texto em maiúsculas ou minúsculas ([upper](#upper), [lower](#lower), [trim](#trim))
* Verifique se as cadeias de caracteres estão vazias ou contêm valores específicos ([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty))
* Substituir padrões de texto por novos valores ([replace](#replace), [replaceAll](#replaceAll))
* Dividir cadeias de caracteres em matrizes para processamento adicional ([split](#split))
* Obter comprimento da cadeia de caracteres ([length](#length)) ou gerar identificadores exclusivos ([uuid](#uuid))

As funções de sequência fornecem recursos abrangentes de manipulação de texto, permitindo um processamento sofisticado de dados e uma lógica condicional baseada no conteúdo do texto nas expressões de jornada.

## concat {#concat}

Concatena dois parâmetros de string ou uma lista de strings.

+++Sintaxe

`concat(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| Lista | listString |
| sequência de caracteres | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`concat(<string>,<string>)`

`concat(<listString>)`

Retorna uma string.

+++

+++Exemplos

`concat("Hello","World")`

Retorna &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Retorna &quot;Olá, Mundo&quot;.

+++

## contain {#contain}

Verifica se a segunda cadeia de caracteres do argumento está contida na primeira cadeia de caracteres do argumento.

+++Sintaxe

`contain(<parameters>)`

+++

+++Parâmetros

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`contain(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`contain("rowing is great", "great")`

Retorna verdadeiro.

+++

## containIgnoreCase {#containIgnoreCase}

Verifica se a segunda cadeia de caracteres do argumento está contida na primeira cadeia de caracteres do argumento, sem levar em conta maiúsculas e minúsculas.

+++Sintaxe

`containIgnoreCase(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sequência de caracteres pesquisada | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`containIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`containIgnoreCase("rowing is great", "GREAT")`

Retorna verdadeiro.

+++

## endWith {#endWith}

Retornará true se o segundo parâmetro for um sufixo do primeiro.

+++Sintaxe

`endWith(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sufixo | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`endWith(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`endWith("Hello World", "World")`

Retorna verdadeiro.

`endWith("Hello World", "Hello")`

Retorna falso.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

Verifica se a primeira sequência de argumento termina com uma sequência específica (segunda sequência de argumento), sem levar em conta maiúsculas e minúsculas.

+++Sintaxe

`endWithIgnoreCase(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |
| sufixo | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`endWithIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`endWithIgnoreCase("rowing is great", "AT")`

Retorna verdadeiro.

+++

## equalIgnoreCase {#equalIgnoreCase}

Compara a primeira sequência de argumento com a segunda sequência de argumento, ignorando considerações de maiúsculas e minúsculas.

+++Sintaxe

`equalIgnoreCase(<parameters>)`

+++

+++Parâmetros

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`equalIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

Retorna verdadeiro.

+++

## indexOf {#indexOf}

Retorna a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

+++Sintaxe

`indexOf(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | String |
| valor especificado | String |

+++

+++Assinatura e tipo retornado

`indexOf(<string>,<string>)`

Retorna um inteiro.

+++

+++Exemplos

`indexOf("Hello", "l")`

Retorna 2.

Explicação:

Em &quot;Olá&quot;, a primeira ocorrência de &quot;l&quot; está na posição 2.

+++

## isEmpty {#isEmpty}

Retornará true se a cadeia de caracteres no parâmetro não tiver caractere.

+++Sintaxe

`isEmpty(<parameters>)`

+++

+++Parâmetros

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`isEmpty(<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`isEmpty("")`

Retorna verdadeiro.

`isEmpty("Hello World")`

Retorna falso.

+++

## isNotEmpty {#isNotEmpty}

Retorna verdadeiro se a string no parâmetro não estiver vazia.

+++Sintaxe

`isNotEmpty(<parameters>)`

+++

+++Parâmetros

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`isNotEmpty(<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`isNotEmpty("")`

Retorna falso.

`isNotEmpty("hello")`

Retorna verdadeiro.

+++

## lastIndexOf {#lastIndexOf}

Retorna a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.

+++Sintaxe

`lastIndexOf(<parameters>)`

+++

+++Parâmetro

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | String |
| valor especificado | String |

+++

+++Assinatura e tipo retornado

`lastIndexOf(<string>,<string>)`

Retorna um inteiro.

+++

+++Exemplos

`lastIndexOf("Hello", "l")`

Retorna 3.

Explicação:

Em &quot;Olá&quot;, a última ocorrência de &quot;l&quot; está na posição 3.

+++

## comprimento {#length}

Retorna o número de caracteres da expressão de cadeia de caracteres no parâmetro.

+++Sintaxe

`length(<parameters>)`

+++

+++Parâmetro

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`length(<string>)`

Retorna um inteiro.

+++

+++Exemplos

`length("Hello World")`

Retorna 11.

+++

## lower {#lower}

Retorna uma versão em minúsculas do parâmetro.

+++Sintaxe

`lower(<parameter>)`

+++

+++Parâmetro

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`lower(<string>)`

Retorna uma string.

+++

+++Exemplos

`lower("A")`

Retorna &quot;a&quot;.

+++

## matchRegExp {#matchRegExp}

Retornará true se a cadeia de caracteres no primeiro parâmetro corresponder à expressão regular no segundo parâmetro. Para obter mais informações, consulte [esta página](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Sintaxe

`matchRegExp(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|--- |--- |
| sequência de caracteres | sequência de caracteres |
| regexp | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`matchRegExp(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`matchRegExp("12345", "\\d+")`

Retorna verdadeiro.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

Verifique se a primeira string do argumento com a segunda string do argumento é diferente, ignorando as considerações sobre maiúsculas e minúsculas.

+++Sintaxe

`notEqualIgnoreCase(<parameters>)`

+++

+++Parâmetros

* sequência de caracteres

+++

+++Assinatura e tipo retornado

`notEqualIgnoreCase(<string>,<string>)`

Retorna um valor booleano.

+++

+++Exemplos

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

Substitui a primeira ocorrência correspondente à string de destino pela string de substituição na string de base.

A substituição continua do início da string até o fim. Por exemplo, substituir &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

+++Sintaxe

`replace(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|--------------|
| base | sequência de caracteres |
| destino | string (RegExp) |
| substituição | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`replace(<base>,<target>,<replacement>)`

Retorna uma string.

+++

+++Exemplos

`replace("Hello World", "l", "x")`

Retorna &quot;Hexlo World&quot;.

**Exemplo com RegExp:**

Como o parâmetro de destino é um RegExp, dependendo da cadeia de caracteres que você deseja substituir, talvez seja necessário usar escape em alguns caracteres. Exemplo:

* cadeia de caracteres a ser avaliada: `|OFFER_A|OFFER_B`
* fornecido por um atributo de perfil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Cadeia de caracteres a ser substituída: `|OFFER_A`
* Cadeia de caracteres substituída por: `''`
* É necessário adicionar `\\` antes do caractere `|`.

A expressão é:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

A cadeia de caracteres retornada é: `|OFFER_B`

Também é possível criar a cadeia de caracteres a ser substituída a partir de um determinado atributo:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Substitui todas as ocorrências correspondentes à cadeia de caracteres de destino pela cadeia de caracteres de substituição na cadeia de caracteres base.

A substituição continua do início da string até o fim. Por exemplo, substituir &quot;aa&quot; por &quot;b&quot; na string &quot;aaa&quot; resultará em &quot;ba&quot; em vez de &quot;ab&quot;.

+++Sintaxe

`replaceAll(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|--------------|
| base | sequência de caracteres |
| destino | string (RegExp) |
| substituição | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Retorna uma string.

+++

+++Exemplos

`replaceAll("Hello World", "l", "x")`

Retorna &quot;Hexxo Worxd&quot;.

Como o parâmetro de destino é um RegExp, dependendo da cadeia de caracteres que você deseja substituir, talvez seja necessário usar escape em alguns caracteres. Consulte o exemplo na função [replace](#replace).

+++

## split {#split}

Divide a primeira sequência de argumento com uma sequência de separador (segunda sequência de argumento, que pode ser uma expressão regular) para produzir uma lista de sequências de caracteres (tokens).

+++Sintaxe

`split(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-----------|------------------|
| string de entrada | sequência de caracteres |
| sequência de caracteres separadora | sequência de caracteres |

+++

+++Assinaturas e tipo retornado

`split(<input string>, <separator string>)`

Retorna uma listString.

+++

+++Exemplos

`split("A_B_C", "_")`

Retorna `["A","B","C"]`

Exemplo com um campo de evento &quot;event.appVersion&quot; com valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Retorna `["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

Retornará true se o segundo parâmetro for um prefixo do primeiro.

+++Sintaxe

`startWith(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-------------|--------|
| sequência de caracteres | sequência de caracteres |
| prefixo | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`startWith(<string>,<string>)`

Retornar um booleano.

+++

+++Exemplos

`startWith("Hello World", "Hello")`

Retorna verdadeiro.

`startWith("Hello World", "World")`

Retorna falso.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Retornará true se o segundo parâmetro for um prefixo do primeiro sem considerar letras maiúsculas e minúsculas.

+++Sintaxe

`startWithIgnoreCase(<parameters>)`

+++

+++Parâmetros

| Parâmetro | Tipo |
|-------------|--------|
| sequência de caracteres | sequência de caracteres |
| prefixo | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`startWithIgnoreCase(<string>,<string>)`

Retornar um booleano.

+++

+++Exemplos

`startWithIgnoreCase("rowing is great", "RO")`

Retorna verdadeiro.

+++

## substr {#substr}

Retorna a subcadeia de caracteres da expressão de cadeia de caracteres entre o índice inicial e o índice final. Se o índice final não estiver definido, ele será entre o índice inicial e o final.

+++Sintaxe

`substr(<parameters>)`

+++

+++Parâmetros

| Parâmetro | tipo |
|-------------|----------|
| sequência de caracteres | sequência de caracteres |
| beginIndex | inteiro |
| endIndex | inteiro |

+++

+++Assinatura e tipo retornado

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Retorna uma string.

+++

+++Exemplos

`substr("Hello World",6)`

Retorna &quot;Mundo&quot;.

`substr("Hello World", 0, 5)`

Retorna &quot;Olá&quot;.

+++

## trim {#trim}

Remove espaços iniciais e finais.

+++Sintaxe

`trim(<parameters>)`

+++

+++Parâmetro

| Parâmetro | Tipo |
|-----------|------------------|
| sequência de caracteres | sequência de caracteres |

+++

+++Assinatura e tipo retornado

`trim(<string>)`

Retorna uma string.

+++

+++Exemplos

`trim(" Hello ")`

Retorna &quot;Olá&quot;.

+++

## upper {#upper}

Retorna uma versão em maiúsculas do parâmetro.

+++Sintaxe

`upper(<parameters>)`

+++

+++Assinatura e tipo retornado

`upper(<string>)`

Retorna uma string.

+++

+++Exemplos

`upper("b")`

Retorna &quot;B&quot;.

+++

## uuid {#uuid}

Gera um UUID aleatório (Identificador exclusivo universal).

+++Sintaxe

`uuid()`

+++

+++Parâmetros 

Esta função não requer parâmetros.

+++

+++Assinatura e tipo retornado

`uuid()`

Retorna uma string.

+++

+++Exemplos

`uuid()`

Retorna &quot;79e70b7f-8a85-400b-97a1-9f9826121553&quot;.

+++

