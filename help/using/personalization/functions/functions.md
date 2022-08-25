---
title: Introdução às funções do Helper
description: Biblioteca de funções do Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 315c3e8c04b2e3944d0d5b2befb205acbe0ef7c9
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 3%

---

# Introdução às funções do Helper{#functions}

Use [!DNL Journey Optimizer] linguagem de modelo para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-los no contexto de personalização. Saiba mais sobre as diretrizes da sintaxe de personalização em [esta página](../personalization-syntax.md).

➡️ [Saiba como usar funções de ajuda neste vídeo](#video)

A linguagem de modelo é usada em funções de ajuda disponíveis na lista suspensa de personalização do Editor de expressão, conforme abaixo:

![](../assets/access-helper-functions.png)

No [!DNL Journey Optimizer] As funções de ajuda do editor de expressão são agrupadas em três categorias: [Funções](#functions-helper), [Ajudantes](#helper-helper) e [Operadores](#operators-helper).

Selecione uma categoria para acessar subcategorias e funções.

Acesso às subcategorias clicando no botão `>` ícone . Selecione uma função clicando no botão `+` ícone : a função é adicionada automaticamente à tela de personalização.

Clique no botão `...` para exibir a descrição da função e adicioná-la aos favoritos. [Saiba mais](../personalize.md#fav)

## Funções{#functions-helper}

### Funções de agregação e storage

<table>
    <tr>
        <td><a href="aggregation.md#average">Média</a></td><td>Essa função retorna a média aritmética de todos os valores selecionados na matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Contagem</a></td><td>Essa função retorna o número de elementos dentro da matriz específica</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Contar Somente Nulo</a></td><td>Essa função conta o número de valores nulos na lista.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Contar com Null</a></td><td>Essa função conta todos os elementos da lista, incluindo valores nulos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Essa função obtém valores de uma matriz ou lista com valores duplicados removidos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Contagem distinta com nulo</a></td><td>Essa função conta o número de valores diferentes, incluindo os valores nulos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primeiro item</a></td><td>Essa função retorna o primeiro item em uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primeiro n na matriz</a></td><td>Essa função retorna os primeiros itens "N" em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Em</a></td><td>Essa função é usada para determinar se um item é membro de uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclui</a></td><td>Essa função determina se uma matriz ou lista contém um determinado item</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersetos</a></td><td>Essa função determina se duas matrizes ou listas têm pelo menos um membro comum</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Último n na matriz</a></td><td>Essa função retorna os últimos "N" itens em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Máximo</a></td><td>Essa função retorna o maior de todos os valores selecionados em uma matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Mínimo</a></td><td>Essa função retorna o menor de todos os valores selecionados na matriz</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Não está em</a></td><td>Essa função determina se um item não é membro de uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subconjunto de</a></td><td>Essa função determina se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B), ou seja, se todos os elementos na matriz A são elementos da matriz B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Essa função retorna a soma de todos os valores selecionados na matriz</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superconjunto de</a></td><td>Essa função determina se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B), ou seja, se essa matriz A contém todos os elementos na matriz B</td>
    </tr>
</table>

### Funções de Data/Hora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Idade</a></td><td>Essa função recupera a idade de uma determinada data</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Hora atual em milissegundos</a></td><td>Essa função recupera o tempo atual em milissegundos de época</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Diferença de data</a></td><td>Essa função recupera a diferença entre duas datas em número de dias</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Dia da semana</a></td><td>Essa função recupera o dia da semana</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Dia do ano</a></td><td>Essa função recupera o dia do ano</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Data de formato</a></td><td>Essa função formata um valor de data e hora</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Definir Dias</a></td><td>Essa função define o dia do mês para a data e hora especificada</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Definir horas</a></td><td>Essa função define a hora da data e hora</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">Para UTC</a></td><td>Essa função converte um datetime em UTC</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semana do ano</a></td><td>Essa função retorna a semana do ano</td>
    </tr>
</table>
</table>

### Mapear funções {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Obtenha</a></td><td>Essa função é usada para recuperar o valor de um mapa para uma determinada chave</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Teclas</a></td><td>Essa função é usada para recuperar todas as chaves de um determinado mapa</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valores</a></td><td>Essa função recupera todos os valores de um determinado mapa</td>
    </tr>
</table>

### Funções matemáticas {#math-functions}

<table>
    <tr>
        <td><a href="objects.md#absolute">Absoluto   </a></td><td>Essa função converte um número em seu valor absoluto</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">Random</a></td><td>Essa função retorna um valor aleatório entre 0 e 1</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-down">Arredondar para baixo</a></td><td>Esta função arredonda um número</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-up">Arredondar para cima</a></td><td>Esta função arredonda um número</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-percentage">Porcentagem de destino</a></td><td>Essa função converte um número em porcentagem</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-precision">Para precisão</a></td><td>Essa função converte um número para a precisão necessária</td>
    </tr>
</table>

### Funções do objeto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Não é nulo</a></td><td>Essa função é usada para determinar se existe uma referência de objeto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">É nulo</a></td><td>Essa função é usada para determinar se uma referência de objeto não existe</td>
    </tr>
</table>

### Funções de string {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Essa função é usada para capitalizar a primeira letra de cada palavra de uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Essa função é usada para combinar duas strings em uma</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>Essa função é usada para determinar se uma string contém uma substring especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Não contém</a></td><td>Essa função é usada para determinar se uma string não contém uma substring especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Não termina com</a></td><td>Essa função é usada para determinar se uma string não termina com uma substring especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Does not start with</a></td><td>Essa função é usada para determinar se uma string não inicia com uma substring especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codificação 64</a></td><td>Essa função é usada para codificar ou decodificar uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Termina com</a></td><td>Essa função é usada para determinar se uma string termina com uma substring especificada</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Igual a</a></td><td>Essa função é usada para determinar se uma string não inicia com uma substring especificada, com diferenciação entre maiúsculas e minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Igual a Ignorar Maiúsculas e Minúsculas</a></td><td>Essa função é usada para determinar se uma string não inicia com uma substring especificada, sem diferenciação entre maiúsculas e minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extrair domínio de email</a></td><td>Essa função é usada para extrair o domínio de um endereço de email</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Obter host de url</a></td><td>Essa função é usada para obter o host do url.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Obter caminho de url</a></td><td>Essa função é usada para obter o caminho do url</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Obter protocolo de url</a></td><td>Essa função é usada para obter o protocolo url</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Índice De</a></td><td>Essa função retorna a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Essa função é usada para verificar se uma string ou expressão está vazia.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Is Not Empty</a></td><td>Essa função retornará true se a string no parâmetro não estiver vazia.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Último Índice De</a></td><td>Essa função retorna a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Aparar à esquerda</a></td><td>Essa função remove espaços em branco do início de uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Essa função é usada para obter o número de caracteres em uma string ou expressão</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Like</a></td><td>Essa função é usada para determinar se uma string corresponde a um padrão especificado</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minúsculas</a></td><td>Essa função converte uma string em letras minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Máscara</a></td><td>Essa função é usada para substituir uma parte de uma string por caracteres "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Corresponde</a></td><td>Essa função é usada para determinar se uma string corresponde a uma expressão regular específica</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Essa função retorna o hash md5 da string de entrada.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Not equal to</a></td><td>Essa função é usada para determinar se uma string não é igual à string especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Diferente de Ignorar maiúsculas e minúsculas</a></td><td>Essa função compara duas strings que ignoram letras maiúsculas e minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Grupo de expressões regulares</a></td><td>Essa função é usada para extrair informações específicas, com base na expressão regular fornecida</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Substituir</a></td><td>Essa função substitui determinada substring em uma string por outra substring</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Substituir tudo</a></td><td>Essa função substitui todas as subsequências de caracteres de um texto que corresponde ao "target" pela sequência de caracteres de "substituição" literal especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Aparar à direita</a></td><td>Essa função remove espaços em branco do final de uma string </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Dividir</a></td><td>Essa função é usada para dividir uma string por um determinado caractere</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Começa com</a></td><td>Essa função é usada para determinar se uma string começa com uma substring especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Sequência de caracteres para data</a></td><td>Essa função é usada para converter a string em data. Retorna a data da época como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">String to integer</a></td><td>Essa função Converte um valor de string em um valor inteiro.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">String para número</a></td><td>Essa função é usada para converter uma string em número. Retorna a mesma cadeia de caracteres da saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Sub string</a></td><td>Essa função retorna a substring da expressão da string entre o índice begin e o índice end.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Caso de título</a></td><td>Essa função é usada para capitalizar as primeiras letras de cada palavra de uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">Para Bool</a></td><td>Essa função Converte um valor de argumento em um valor booleano, dependendo do tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Hora da Data Final</a></td><td>Essa função é usada para converter a string em data. Retorna a data da época como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Somente Data/Hora</a></td><td>Essa função converte um valor de argumento em um valor somente de data e hora. Retorna a data da época como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Aparar</a></td><td>Essa função remove espaços em branco do início e do fim de uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Maiúscula</a></td><td>Essa função converte uma string em letras maiúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Decodificação de URL</a></td><td>Essa função é usada para decodificar uma string codificada em url.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Codificação de URL</a></td><td>Essa função é usada para codificar uma string no url.</td>
    </tr>
</table>


## Auxiliares{#helper-helper}

Os assistentes estão detalhados em [esta página](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valor de fallback padrão</a></td><td>Essa função permite renderizar uma variável com o padrão</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Cada</a></td><td>Essa função é usada para iterar sobre uma matriz</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Se</a></td><td>Essa função é usada para definir um bloco condicional - se a avaliação da expressão retornar true, o bloco será renderizado</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Essa função permite que uma expressão seja armazenada como uma variável para ser usada posteriormente em uma query</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Exceto</a></td><td>Essa função é usada para definir um bloco condicional - se a avaliação da expressão retornar false, o bloco será renderizado</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Com</a></td><td>Essa função é usada para alterar o token de avaliação da parte do template</td>
    </tr>
</table>

## Operadores{#operators-helper}

### Funções aritméticas {#arithmetic-helper}

As funções aritméticas são usadas para executar cálculos básicos em valores.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Adição</a></td><td>Esse operador é usado para localizar a soma de duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividir</a></td><td>Esse operador é usado para encontrar o quociente de duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplicação</a></td><td>Esse operador é usado para localizar o produto de duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Remanescente</a> </td><td>Esse operador é usado para localizar o restante após dividir as duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Subtração</a> </td><td>Esse operador encontra a diferença entre duas expressões</td>
    </tr>
</table>


### Funções booleanas {#boolean-functions}

As funções booleanas são usadas para executar lógica booleana em elementos diferentes.

<table>
    <tr>
        <td><a href="operators.md#and">E</a></td><td>Esse operador cria uma conjunção lógica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Ou</a></td><td>Esse operador cria uma disjunção lógica</td>
    </tr>
</table>


### Funções de comparação {#comparison-functions}

As funções de comparação são usadas para comparar diferentes expressões e valores, retornando verdadeiro ou falso de acordo.

<table>
    <tr>
        <td><a href="operators.md#equals">Igual a</a></td><td>Esta operação verifica se os valores são iguais</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>Esse operador verifica se o primeiro valor é maior que o segundo</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Maior ou igual a</a></td><td>Esse operador verifica se o primeiro valor é maior ou igual ao segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Menor que ou igual a</a> </td><td>Esse operador verifica se o primeiro valor é menor ou igual ao segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Não é igual a</a></td><td>Esse operador verifica se determinada expressão não é igual a fornecer valor</td>
    </tr>
</table>

## Vídeo tutorial{#video}

Saiba como transformar valores de personalização usando funções de ajuda de personalização e entenda diferentes casos de uso para funções de ajuda.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
