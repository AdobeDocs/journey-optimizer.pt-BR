---
title: Introdução às funções Auxiliares
description: Biblioteca de funções do Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 2444d8fbe3a86feb0497d754b4f57f234fa29e49
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 2%

---

# Introdução às funções Auxiliares{#functions}

Uso [!DNL Journey Optimizer] linguagem de modelo para executar operações em dados, como cálculos, formatação ou conversões de dados, condições e manipulá-los no contexto de personalização. Saiba mais sobre as diretrizes da sintaxe de personalização no [esta página](../personalization-syntax.md).

➡️ [Saiba como usar funções auxiliares neste vídeo](#video)

A linguagem de modelo é utilizada em funções auxiliares disponíveis na lista suspensa de personalização do Editor de expressão, conforme abaixo:

![](../assets/access-helper-functions.png)

No [!DNL Journey Optimizer] No Editor de expressão, as funções auxiliares são agrupadas em três categorias: [Funções](#functions-helper), [Auxiliares](#helper-helper) e [Operadores](#operators-helper).

Selecione uma categoria para acessar subcategorias e funções.

Acesso a subcategorias clicando no ícone `>` ícone. Selecione uma função clicando no ícone `+` ícone: a função é adicionada automaticamente à tela de personalização.

Clique em `...` ícone para exibir a descrição da função e adicioná-la aos favoritos. [Saiba mais](../personalize.md#fav)

## Funções{#functions-helper}

### Funções de agregação e array

<table>
    <tr>
        <td><a href="aggregation.md#average">Média</a></td><td>Esta função retorna a média aritmética de todos os valores selecionados dentro da matriz.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Contagem</a></td><td>Esta função retorna o número de elementos dentro da matriz especificada.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Somente contagem nula</a></td><td>Esta função conta o número de valores nulos na lista.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Contagem com nulo</a></td><td>Esta função conta todos os elementos da lista, incluindo valores nulos.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinto</a></td><td>Esta função obtém valores de uma matriz ou lista com valores duplicados removidos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Contagem distinta com nulo</a></td><td>Esta função conta o número de valores diferentes, incluindo os valores nulos.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primeiro item</a></td><td>Esta função retorna o primeiro item em uma matriz ou lista.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primeiro N na matriz</a></td><td>Esta função retorna os primeiros itens "N" em uma matriz quando classificados em ordem crescente com base na expressão numérica fornecida</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Entrada</a></td><td>Esta função é usada para determinar se um item é membro de uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclui</a></td><td>Esta função determina se uma matriz ou lista contém um determinado item.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Interseta</a></td><td>Esta função determina se duas matrizes ou listas têm pelo menos um membro comum.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Último N na matriz</a></td><td>Esta função retorna os últimos itens "N" em uma matriz quando classificados em ordem crescente com base na expressão numérica fornecida</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Máximo</a></td><td>Esta função retorna o maior valor dentro de uma matriz.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Mínimo</a></td><td>Esta função retorna o menor valor dentro da matriz.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Não está em</a></td><td>Esta função determina se um item não é membro de uma matriz ou lista.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subconjunto de</a></td><td>Esta função determina se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B), isto é, se todos os elementos na matriz A são elementos da matriz B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Esta função retorna a soma de todos os valores selecionados na matriz.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superconjunto de</a></td><td>Esta função determina se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B), isto é, se essa matriz A contém todos os elementos na matriz B</td>
    </tr>
</table>

### Funções de data e hora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Idade</a></td><td>Esta função recupera a idade de uma determinada data.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Tempo atual em milissegundos</a></td><td>Esta função recupera a hora atual em milissegundos da época</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Diferença de data</a></td><td>Esta função recupera a diferença entre duas datas em número de dias.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Dia da semana</a></td><td>Esta função recupera o dia da semana.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Dia do ano</a></td><td>Esta função recupera o dia do ano.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Formatar data</a></td><td>Esta função formata um valor de data e hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Formatar data com suporte local</a></td><td>Essa função formata um valor de data e hora em sua representação sensível a idioma correspondente, ou seja, em um local desejado.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Definir dias</a></td><td>Esta função define o dia do mês para a data-hora especificada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Definir horas</a></td><td>Esta função define a hora da data-hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">Para UTC</a></td><td>Esta função converte um datetime em UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semana do ano</a></td><td>Esta função retorna a semana do ano.</td>
    </tr>
</table>
</table>

### Mapear Funções {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Obter</a></td><td>Esta função é usada para recuperar o valor de um mapa para uma determinada chave.</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Chaves</a></td><td>Esta função é usada para recuperar todas as chaves de um determinado mapa</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valores</a></td><td>Esta função recupera todos os valores de um determinado mapa.</td>
    </tr>
</table>

### Funções matemáticas {#math-functions}

<table>
    <tr>
        <td><a href="math.md#absolute">Absoluto   </a></td><td>Essa função formata qualquer número em sua representação sensível a linguagem.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">Formatar número</a></td><td>Essa função formata qualquer número em sua representação sensível a linguagem.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Aleatório</a></td><td>Esta função retorna um valor aleatório entre 0 e 1.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">Arredondar para baixo</a></td><td>Esta função arredonda um número para baixo.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Arredondar para cima</a></td><td>Esta função arredonda um número para cima.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">Para hex string</a></td><td>converte qualquer número em sua cadeia de caracteres hexadecimal.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">Para porcentagem</a></td><td>Esta função converte um número em porcentagem.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">Para precisão</a></td><td>Esta função converte um número para a precisão necessária.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">Para string</a></td><td>Esta função converte qualquer número em sua representação de sequência de caracteres. </td>
    </tr>
</table>

### Funções do objeto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Não é nulo</a></td><td>Esta função é usada para determinar se existe uma referência de objeto.</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">É nulo</a></td><td>Esta função é usada para determinar se uma referência de objeto não existe.</td>
    </tr>
</table>

### Funções de string {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Esta função é usada para colocar a primeira letra de cada palavra de uma sequência de caracteres em maiúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">Código de caractere em</a></td><td>Esta função retorna o valor ASCII de um caractere, como a função charCodeAt no JavaScript</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Esta função é usada para combinar duas strings em uma</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>Esta função é usada para determinar se uma sequência de caracteres contém uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Não contém</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não contém uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Não termina com</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não termina com uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Não começa com</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não inicia com uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codificação 64</a></td><td>Esta função é usada para codificar ou decodificar uma string.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Termina com</a></td><td>Esta função é usada para determinar se uma sequência de caracteres termina com uma subsequência especificada.</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Igual a</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não inicia com uma subsequência especificada, diferencia maiúsculas de minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Ignorar maiúsculas e minúsculas é igual a</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não inicia com uma subsequência especificada, sem diferenciar maiúsculas de minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extrair domínio de email</a></td><td>Esta função é usada para extrair o domínio de um endereço de email.</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">Formatar moeda</a></td><td>Essa função converte qualquer número em sua representação de moeda correspondente sensível ao idioma, dependendo da localidade transmitida como uma string no segundo argumento</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Obter host de URL</a></td><td>Esta função é usada para obter o host de URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Obter caminho do URL</a></td><td>Esta função é usada para obter o caminho do URL</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Obter protocolo de URL</a></td><td>Esta função é usada para obter o protocolo de URL</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Índice de</a></td><td>Esta função retorna a posição (no primeiro argumento) da primeira ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Esta função é usada para verificar se uma sequência de caracteres ou expressão está vazia.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">Não Está Vazio</a></td><td>Esta função retorna verdadeiro se a sequência de caracteres no parâmetro não estiver vazia.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Último índice de</a></td><td>Esta função retorna a posição (no primeiro argumento) da última ocorrência do segundo parâmetro. Retorna -1 se não houver correspondência.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Cortar à esquerda</a></td><td>Esta função remove os espaços em branco do início de uma sequência de caracteres.</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Comprimento</a></td><td>Esta função é usada para obter o número de caracteres em uma sequência ou expressão</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Curtir</a></td><td>Esta função é usada para determinar se uma sequência de caracteres corresponde a um padrão especificado.</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minúsculas</a></td><td>Esta função converte uma sequência de caracteres em letras minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Máscara</a></td><td>Esta função é usada para substituir uma parte de uma sequência de caracteres por caracteres "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Corresponde </a></td><td>Esta função é usada para determinar se uma sequência de caracteres corresponde a uma expressão regular específica</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Esta função retorna o hash md5 da sequência de caracteres de entrada.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Diferente de</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não é igual à sequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Diferente de Ignorar Maiúsculas e Minúsculas</a></td><td>Esta função compara duas sequências de caracteres ignorando maiúsculas e minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Grupo de expressão regular</a></td><td>Esta função é usada para extrair informações específicas com base na expressão regular fornecida.</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Substituir</a></td><td>Esta função substitui uma determinada subsequência de caracteres em uma sequência de caracteres por outra subsequência.</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Substituir tudo</a></td><td>Esta função substitui todas as subsequências de um texto que corresponde ao "destino" pela sequência literal de "substituição" especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Cortar à direita</a></td><td>Esta função remove os espaços em branco do final de uma sequência de caracteres. </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Divisão</a></td><td>Esta função é usada para dividir uma sequência de caracteres por um determinado caractere.</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Começa com</a></td><td>Esta função é usada para determinar se uma sequência de caracteres inicia com uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Sequência de caracteres para data</a></td><td>Esta função converte um valor de sequência de caracteres em um valor de data-hora.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Sequência de caracteres para inteiro</a></td><td>Esta função converte um valor de sequência de caracteres em um valor inteiro.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Sequência de caracteres para número</a></td><td>Esta função é usada para converter uma sequência de caracteres em número. Ele retorna a mesma string que a saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Substring</a></td><td>Esta função retorna a subsequência de caracteres da expressão de sequência de caracteres entre o índice inicial e o índice final.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Primeira letra da palavra maiúscula</a></td><td>Esta função é usada para colocar em maiúsculas as primeiras letras de cada palavra de uma sequência de caracteres.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">Para booleano</a></td><td>Esta função converte um valor de argumento em um valor booleano, dependendo de seu tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Para data hora</a></td><td>Esta função é usada para converter sequência de caracteres em data. Retorna a data da época como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Somente para data e hora</a></td><td>Esta função converte um valor de argumento em um valor somente de data e hora. Retorna a data da época como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Aparar</a></td><td>Esta função remove os espaços em branco do início e do fim de uma sequência de caracteres.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Maiúscula</a></td><td>Esta função converte uma sequência de caracteres em letras maiúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Decodificação de URL</a></td><td>Esta função é usada para decodificar uma sequência de caracteres codificada em URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Codificação de URL</a></td><td>Esta função é usada para codificar uma sequência de caracteres em URL.</td>
    </tr>
</table>


## Auxiliares{#helper-helper}

Os auxiliares estão detalhados em [esta página](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valor de fallback padrão</a></td><td>Esta função é usada para renderizar uma variável com o padrão</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>Esta função é usada para iterar em uma matriz.</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Se</a></td><td>Esta função é usada para definir um bloco condicional - se a expressão evaluation retornar true, o bloco será renderizado</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Essa função permite que uma expressão seja armazenada como uma variável a ser usada posteriormente em uma consulta</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">A menos que</a></td><td>Esta função é usada para definir um bloco condicional - se a expressão evaluation retornar false, o bloco será renderizado</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">Com</a></td><td>Esta função é usada para alterar o token de avaliação da parte do modelo</td>
    </tr>
</table>

## Operadores{#operators-helper}

### Funções aritméticas {#arithmetic-helper}

Funções aritméticas são usadas para realizar cálculos básicos em valores.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Adição</a></td><td>Este operador é usado para encontrar a soma de duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Divisão</a></td><td>Este operador é usado para encontrar o quociente de duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplicação</a></td><td>Este operador é usado para encontrar o produto de duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Restante</a> </td><td>Este operador é usado para encontrar o restante após dividir as duas expressões de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Subtração</a> </td><td>Este operador encontra a diferença entre duas expressões</td>
    </tr>
</table>


### Funções booleanas {#boolean-functions}

Funções booleanas são usadas para executar lógica booleana em elementos diferentes.

<table>
    <tr>
        <td><a href="operators.md#and">E</a></td><td>Este operador cria uma conjunção lógica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Ou</a></td><td>Este operador cria uma disjunção lógica</td>
    </tr>
</table>


### Funções de comparação {#comparison-functions}

As funções de comparação são usadas para comparar entre diferentes expressões e valores, retornando verdadeiro ou falso de acordo.

<table>
    <tr>
        <td><a href="operators.md#equals">Igual a</a></td><td>Esta operação verifica se os valores são iguais</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Maior que</a></td><td>Este operador verifica se o primeiro valor é maior que o segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Maior ou igual a</a></td><td>Este operador verifica se o primeiro valor é maior ou igual ao segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Menor que ou igual a</a> </td><td>Este operador verifica se o primeiro valor é menor ou igual ao segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Não é igual a</a></td><td>Este operador verifica se determinada expressão não é igual a determinado valor</td>
    </tr>
</table>

## Vídeo explicativo{#video}

Saiba como transformar valores de personalização usando funções de ajuda de personalização e entenda diferentes casos de uso para funções de ajuda.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
