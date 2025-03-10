---
title: Introdução às funções Auxiliares
description: Biblioteca de funções do Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 78c1464ccddec75e4827cbb1877d8fab5ac08b90
workflow-type: tm+mt
source-wordcount: '2388'
ht-degree: 27%

---

# Introdução às funções Auxiliares{#functions}

Use a linguagem de modelo [!DNL Journey Optimizer] para executar operações em dados, como cálculos, formatação ou conversões de dados, condições e manipulá-las no contexto da personalização. Saiba mais sobre as diretrizes da sintaxe de personalização em [esta página](../personalization-syntax.md).

➡️ [Saiba como usar funções auxiliares neste vídeo](#video)

A linguagem de modelo é utilizada em funções auxiliares disponíveis na lista suspensa de personalização do editor de personalização, conforme abaixo:

![](../assets/access-helper-functions.png)

>[!NOTE]
>
>As funções e os recursos disponíveis no editor de personalização são diferentes daqueles disponíveis no [editor de expressão avançado do Jornada](../../building-journeys/expression/expressionadvanced.md).

No editor de personalização [!DNL Journey Optimizer], as funções auxiliares são agrupadas em três categorias: [Funções](#functions-helper), [Auxiliares](#helper-helper) e [Operadores](#operators-helper).

Selecione uma categoria para acessar subcategorias e funções.

Acesso às subcategorias clicando no ícone `>`. Selecione uma função ao clicar no ícone `+`: a função é adicionada automaticamente à tela de personalização.

Clique no ícone `...` para exibir a descrição da função e adicioná-la aos favoritos. [Saiba mais](../personalize.md#fav)

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
        <td><a href="arrays-list.md#in">Em</a></td><td>Esta função é usada para determinar se um item é membro de uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclui</a></td><td>Esta função determina se uma matriz ou lista contém um determinado item.</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersecta</a></td><td>Esta função determina se duas matrizes ou listas têm pelo menos um membro comum.</td>
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
        <td><a href="aggregation.md#sum">Somar</a></td><td>Esta função retorna a soma de todos os valores selecionados na matriz.</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superconjunto de</a></td><td>Esta função determina se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B), isto é, se essa matriz A contém todos os elementos na matriz B</td>
    </tr>
</table>

### Funções de data e hora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">Adicionar dias</a></td><td>Esta função ajusta uma determinada data por um número especificado de dias, usando valores positivos para incrementar e valores negativos para diminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">Adicionar horas</a></td><td>Esta função ajusta uma determinada data por um número especificado de horas, usando valores positivos para incrementar e valores negativos para diminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">Adicionar minutos</a></td><td>Esta função ajusta uma determinada data por um número especificado de minutos, usando valores positivos para incrementar e valores negativos para diminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">Adicionar meses</a></td><td>Esta função ajusta uma determinada data por um número especificado de meses, usando valores positivos para incrementar e valores negativos para diminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">Adicionar segundos</a></td><td>Esta função ajusta uma determinada data por um número especificado de segundos, usando valores positivos para incrementar e valores negativos para diminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">Adicionar anos</a></td><td>Esta função ajusta uma determinada data por um número especificado de anos, usando valores positivos para incrementar e valores negativos para diminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">Idade</a></td><td>Esta função recupera a idade de uma determinada data.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">Idade em dias</a></td><td>Essa função calcula a idade de uma determinada data em dias, ou seja, o número de dias decorridos entre a data especificada e a data atual, negativo para datas futuras e positivo para datas passadas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">Idade em meses</a></td><td>Essa função calcula a idade de uma determinada data em meses, ou seja, o número de meses decorridos entre a data especificada e a data atual , negativo para datas futuras e positivo para datas passadas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">Comparar datas</a></td><td>Esta função compara a primeira data de entrada com a outra. Retorna 0 se date1 for igual a date2, -1 se date1 for anterior a date2, e 1 se date1 for posterior a date2.</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">Converter ZonedDateTime</a></td><td>Esta função converte uma data-hora em um determinado fuso horário.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Hora atual em milissegundos</a></td><td>Esta função recupera a hora atual em milissegundos da época.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Diferença de data</a></td><td>Esta função recupera a diferença entre duas datas em número de dias.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">Dia do mês</a></td><td>Esta função retorna o número que representa o dia do mês.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Dia da semana</a></td><td>Esta função recupera o dia da semana.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Dia do ano</a></td><td>Esta função recupera o dia do ano.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">Diferença em segundos</a></td><td>Esta função retorna a diferença entre duas datas em segundos.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">Extrair horas</a></td><td>Esta função extrai o componente de hora de um determinado carimbo de data e hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">Extrair minutos</a></td><td>Esta função extrai o componente de minutos de um determinado carimbo de data e hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">Extrair meses</a></td><td>Esta função extrai o componente de mês de um determinado carimbo de data e hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">Extrair segundos</a></td><td>Esta função extrai o componente de segundos de um determinado carimbo de data e hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Formatar data</a></td><td>Essa função formata um valor de data e hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Formatar data com suporte local</a></td><td>Essa função formata um valor de data e hora em sua representação sensível a idioma correspondente, ou seja, em um local desejado.</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">Obter CurrentZonedDateTime</a></td><td>Esta função retorna a data e a hora atuais com informações de fuso horário.</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">Diferença em horas</a></td><td>Esta função retorna a diferença entre duas datas em termos de horas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">Diferença em minutos</a></td><td>Esta função retorna a diferença entre duas datas em termos de minutos.</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">Diferença em meses</a></td><td>Esta função retorna a diferença entre duas datas em termos de meses.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Definir dias</a></td><td>Esta função define o dia do mês para a data-hora especificada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Definir horas</a></td><td>Esta função define a hora da data-hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">Para data hora</a></td><td>Esta função converte a sequência de caracteres em data. Retorna a data da época como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">Para UTC</a></td><td>Esta função converte um datetime em UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">Vincular ao início do dia</a></td><td>Esta função modifica uma determinada data/hora, definindo-a como o início do dia com a hora definida como 0h00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">truncateToStartOfQuarter</a></td><td>Essa função trunca uma data-hora para o primeiro dia de seu trimestre (por exemplo, Jan 1, Abr 1, Jul 1, Out 1) às 00:00.
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">truncateToStartOfWeek</a></td><td>Esta função modifica uma determinada data/hora, definindo-a como o início da semana (segunda-feira, às 0h00).</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">truncateToStartOfYear</a></td><td>Esta função modifica uma determinada data/hora, vinculando-a ao primeiro dia do ano (1.º de janeiro), às 0h00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semana do ano</a></td><td>Esta função retorna a semana do ano.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">Diferença em anos</a></td><td>Esta função retorna a diferença entre duas datas em termos de anos.</td>
    </tr>
</table>
</table>

### Mapear funções {#map-functions}

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
        <td><a href="math.md#absolute">Absoluto</a></td><td>Essa função formata qualquer número em sua representação sensível a linguagem.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">Formatar número</a></td><td>Essa função formata qualquer número em sua representação sensível a linguagem.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Aleatória</a></td><td>Esta função retorna um valor aleatório entre 0 e 1.</td>
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
    <td><a href="math.md#to-int">ToInt</a></td><td>Converte qualquer um desses tipos (número, duplo, int, longo, flutuante, curto, byte, booleano, string) em um inteiro.</td>
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

### Funções de strings {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Esta função é usada para colocar a primeira letra de cada palavra de uma sequência de caracteres em maiúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">Código de caractere em</a></td><td>Essa função retorna o valor ASCII de um caractere, como a função charCodeAt no JavaScript</td>
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
        <td><a href="string.md#doesNotStartWith">Não inicia com</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não inicia com uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codificação 64</a></td><td>Esta função é usada para codificar uma sequência de caracteres.</td>
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
        <td><a href="string.md#get-url-path">Obter caminho de URL</a></td><td>Esta função é usada para obter o caminho do URL</td>
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
        <td><a href="string.md#is-not-empty">Não está vazio</a></td><td>Esta função retorna verdadeiro se a string no parâmetro não estiver vazia.</td>
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
        <td><a href="string.md#mask">Mascarar</a></td><td>Esta função é usada para substituir uma parte de uma sequência de caracteres por caracteres "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Corresponde</a></td><td>Esta função é usada para determinar se uma sequência de caracteres corresponde a uma expressão regular específica.</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Esta função retorna o hash md5 da string de entrada.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Não é igual a</a></td><td>Esta função é usada para determinar se uma sequência de caracteres não é igual à sequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Não é igual a sem diferenciar maiúsculas e minúsculas</a></td><td>Esta função compara duas strings ignorando maiúsculas e minúsculas.</td>
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
        <td><a href="string.md#startsWith">Inicia com</a></td><td>Esta função é usada para determinar se uma sequência de caracteres inicia com uma subsequência especificada.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">String para data</a></td><td>Esta função converte um valor de sequência de caracteres em um valor de data-hora.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">String para número inteiro</a></td><td>Esta função converte um valor de string em um valor inteiro.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">String para número</a></td><td>Esta função é usada para converter uma string em número. Ela retorna a mesma string como saída para entrada inválida.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Substring</a></td><td>Esta função retorna a substring da expressão de string entre o índice inicial e o índice final.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Primeira letra da palavra maiúscula</a></td><td>Esta função é usada para colocar em maiúsculas as primeiras letras de cada palavra de uma sequência de caracteres.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">Para booleano</a></td><td>Esta função converte um valor de argumento em um valor booleano, dependendo de seu tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Para data hora</a></td><td>Esta função é usada para converter uma string em data. Ela retorna a data da época como saída para entrada inválida.</td>
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
        <td><a href="string.md#url-decode">Decodificação de URL</a></td><td>Esta função é usada para decodificar uma string codificada em URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Codificação de URL</a></td><td>Esta função é usada para codificar uma string em URL.</td>
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
        <td><a href="helpers.md#unless">Unless</a></td><td>Esta função é usada para definir um bloco condicional - se a expressão evaluation retornar false, o bloco será renderizado</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>Esta função é usada para alterar o token de avaliação da parte do modelo</td>
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

## Vídeo tutorial{#video}

Saiba como transformar valores de personalização usando funções de ajuda de personalização e entenda diferentes casos de uso para funções de ajuda.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
