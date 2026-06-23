---
product: journey optimizer
title: Funções de strings
description: Saiba mais sobre funções de string
feature: Journeys
role: Developer
level: Experienced
keywords: string, funções, expressão, jornada, texto, manipulação
version: Journey Orchestration
exl-id: 8186c564-56fa-417a-afd3-8e479e5b23b9
TQID: https://experienceleague.adobe.com/wrP3c7l3uHzN6w3l-fXBQOSb5Tx2NuW-6iyogKpDPc8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1668
ht-degree: 10%

---

# Funções de strings {#string-functions}

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

`isEmpty(<null>)`

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
| target | string (RegExp) |
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
| target | string (RegExp) |
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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página documenta todas as funções de cadeia de caracteres disponíveis nas expressões de jornada do AJO, abrangendo pesquisa de texto, comparação, transformação, extração, validação, substituição, divisão e geração de identificador exclusivo.

**Intenções:**
* Concatenar duas ou mais cadeias de caracteres usando `concat`
* Pesquisar uma subcadeia de caracteres em uma cadeia de caracteres (diferencia maiúsculas de minúsculas ou não diferencia maiúsculas de minúsculas) usando `contain` ou `containIgnoreCase`
* Comparar duas cadeias de caracteres ao ignorar maiúsculas e minúsculas usando `equalIgnoreCase` ou `notEqualIgnoreCase`
* Verifique se uma cadeia de caracteres começa ou termina com um prefixo ou sufixo específico usando `startWith`, `endWith` e suas variantes que não diferenciam maiúsculas de minúsculas
* Extrair uma subcadeia de caracteres por posições de índice usando `substr`
* Substituir a primeira ou todas as ocorrências de um padrão em uma cadeia de caracteres usando `replace` ou `replaceAll`
* Dividir uma cadeia de caracteres em uma lista de tokens por um separador usando `split`
* Gerar uma UUID aleatória para as necessidades de identificador exclusivo usando `uuid`
* Verifique se a cadeia de caracteres está vazia ou não usando `isEmpty` ou `isNotEmpty`

**Glossário:**
* **RegExp**: um padrão de expressão regular usado como parâmetro de destino em `replace`, `replaceAll` e `matchRegExp` — caracteres especiais devem ter escape com `\\`
* **UUID**: Identificador Exclusivo Universal — um identificador de cadeia de caracteres gerado aleatoriamente e retornado por `uuid()`
* **substr**: extrai uma parte de uma cadeia de caracteres especificando um índice inicial e um índice final opcional (baseado em zero)

**Medidas de Proteção:**
* O parâmetro `target` em `replace` e `replaceAll` é tratado como um RegExp; caracteres especiais (por exemplo, `|`, `.`) devem ser evitados com `\\`
* `replace` substitui somente a primeira ocorrência correspondente; use `replaceAll` para substituir cada ocorrência
* `isEmpty` retorna falso para valores nulos (não verdadeiro); nulo não é considerado uma cadeia de caracteres vazia
* `indexOf` e `lastIndexOf` retornam -1 quando nenhuma correspondência for encontrada
* As posições do índice de string são baseadas em zero (o primeiro caractere está na posição 0)

**Terminologia:**
* Nome canônico: Funções de string — Acrônimo: none — variantes: funções de texto, funções de manipulação de string
* Sinônimos: &quot;contain&quot; = &quot;substring check&quot;; &quot;split&quot; = &quot;tokenize string&quot;; &quot;trim&quot; = &quot;strip whitespace&quot;
* Não confunda: &quot;replace&quot; (apenas a primeira ocorrência) ≠ &quot;replaceAll&quot; (todas as ocorrências)
* Não confundir: &quot;indexOf&quot; (primeira posição de ocorrência) ≠ &quot;lastIndexOf&quot; (última posição de ocorrência)
* Não confunda: &quot;isEmpty&quot; (true somente para cadeia de caracteres de comprimento zero) ≠ verificação nula (isEmpty retorna false para nulo)
* Não confunda: &quot;equalIgnoreCase&quot; (retorna true quando ignora maiúsculas e minúsculas de igual ignorância) ≠ &quot;notEqualIgnoreCase&quot; (retorna true quando ignora maiúsculas e minúsculas de diferente ignorância)

**Perguntas frequentes:**
* **P: Como verificar se uma cadeia de caracteres contém uma subsequência, independentemente de caracteres maiúsculos ou minúsculos?** — Use `containIgnoreCase("myString", "searchTerm")`, que retornará true se o termo de pesquisa for encontrado em qualquer caso.
* **P: Qual é a diferença entre `replace` e `replaceAll`?** — `replace` substitui somente a primeira ocorrência correspondente; `replaceAll` substitui cada ocorrência na cadeia de caracteres.
* **P: Por que preciso usar o caractere `|` como escape em `replace`?** — O parâmetro de destino é tratado como uma expressão regular; `|` é um caractere RegExp especial e deve ter escape como `\\|` para ser tratado como um pipe literal.
* **P: `isEmpty` retorna verdadeiro para nulo?** — Não, `isEmpty` retorna falso para nulo; ele só retorna verdadeiro para uma cadeia de caracteres de comprimento zero `""`.
* **P: Como extrair o número da versão principal de uma cadeia de caracteres de versão como &quot;20.45.2.3434&quot;?** — Use `getListItem(split(@event{event.appVersion}, "\\."), 0)` para dividir por ponto e recuperar o primeiro elemento.
* **P: Como faço para gerar um identificador exclusivo em uma expressão de jornada?** — Use `uuid()`, que retorna uma cadeia de caracteres UUID gerada aleatoriamente sem parâmetros necessários.

+++
