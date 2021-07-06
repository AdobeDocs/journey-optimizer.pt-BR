---
title: Biblioteca de funções de ajuda
description: Biblioteca de funções do Journey Optimizer Helper
feature: Personalização
topic: Personalização
role: Data Engineer
level: Experienced
source-git-commit: d09eedce833b41037452bb46bc748e7e9f477d0a
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 3%

---


# Biblioteca de funções de ajuda{#functionsL}

Use a linguagem de modelo [!DNL Journey Optimizer] para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto da personalização. Saiba mais sobre as diretrizes da sintaxe de personalização em [this page](../personalization-syntax.md).

➡️ [Descubra como usar funções de ajuda](#video) (vídeo)

A linguagem de modelo é usada em funções de ajuda disponíveis na lista suspensa de personalização do Editor de expressão, conforme abaixo:

![](../assets/access-helper-functions.png)



No [!DNL Journey Optimizer] Editor de expressão, as funções de ajuda são agrupadas em três categorias: [Funções](#functions-helper), [Ajuda](#helper-helper) e [Operadores](#operators-helper).

## Funções{#functions-helper}

**Funções da matriz**

<table>
    <tr>
        <td><a href="aggregation.md#average">Média</a></td><td>Essa função retorna a média aritmética de todos os valores selecionados na matriz</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">Em</a></td><td>Essa função é usada para determinar se um item é membro de uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Mínimo</a></td><td>Essa função retorna o menor de todos os valores selecionados na matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Contagem</a></td><td>Essa função retorna o número de elementos dentro da matriz específica</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Inclui</a></td><td>Essa função determina se uma matriz ou lista contém um determinado item</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Não está em</a></td><td>Essa função determina se um item não é membro de uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Essa função obtém valores de uma matriz ou lista com valores duplicados removidos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersetos</a></td><td>Essa função determina se duas matrizes ou listas têm pelo menos um membro comum</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subconjunto de</a></td><td>Essa função determina se uma matriz específica (matriz A) é um subconjunto de outra matriz (matriz B), ou seja, se todos os elementos na matriz A são elementos da matriz B</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primeiro item</a></td><td>Essa função retorna o primeiro item em uma matriz ou lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Último n na matriz</a></td><td>Essa função retorna os últimos "N" itens em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Essa função retorna a soma de todos os valores selecionados na matriz</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primeiro n na matriz</a></td><td>Essa função retorna os primeiros itens "N" em uma matriz, quando classificados em ordem crescente com base na expressão numérica fornecida</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Máximo</a></td><td>Essa função retorna o maior de todos os valores selecionados em uma matriz</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superconjunto de</a></td><td>Essa função determina se uma matriz específica (matriz A) é um superconjunto de outra matriz (matriz B), ou seja, se essa matriz A contém todos os elementos na matriz B</td>
    </tr>
</table>


**Mapear funções**

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

**Funções do objeto**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Não é nulo</a></td><td>Essa função é usada para determinar se existe uma referência de objeto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">É nulo</a></td><td>Essa função é usada para determinar se uma referência de objeto não existe</td>
    </tr>
</table>

**Funções de string**

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
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Essa função é usada para verificar se uma string ou expressão está vazia.</td>
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
        <td><a href="string.md#matches">Corresponde</a></td><td>Essa função é usada para determinar se uma string corresponde a uma expressão regular específica</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Não é igual a</a></td><td>Essa função é usada para determinar se uma string não é igual à string especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Grupo de expressões regulares</a></td><td>Essa função é usada para extrair informações específicas, com base na expressão regular fornecida</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a></td><td>Essa função substitui determinada substring em uma string por outra substring</td>
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
        <td><a href="string.md#titleCase">Caso de título</a></td><td>Essa função é usada para capitalizar as primeiras letras de cada palavra de uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Aparar</a></td><td>Essa função remove espaços em branco do início e do fim de uma string</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Maiúscula</a></td><td>Essa função converte uma string em letras maiúsculas</td>
    </tr>
</table>


## Auxiliares{#helper-helper}

Os ajuda são detalhados em [this page](helpers.md).


<table>
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


### Funções booleanas

As funções booleanas são usadas para executar lógica booleana em elementos diferentes.

<table>
    <tr>
        <td><a href="operators.md#and">E</a></td><td>Esse operador cria uma conjunção lógica</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Se</a></td><td>Esse operador resolve uma expressão dependendo se uma condição especificada é verdadeira</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Não</a></td><td>Esse operador cria uma negação lógica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Ou</a></td><td>Esse operador cria uma disjunção lógica</td>
    </tr>
</table>


### Funções de comparação

As funções de comparação são usadas para comparar diferentes expressões e valores, retornando verdadeiro ou falso de acordo.

<table>
    <tr>
        <td><a href="operators.md#and">Igual a</a></td><td>Esta operação verifica se os valores são iguais</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>Esse operador verifica se o primeiro valor é maior que o segundo</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Maior ou igual a</a></td><td>Esse operador verifica se o primeiro valor é maior ou igual ao segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Não é igual a</a></td><td>Esse operador verifica se determinada expressão não é igual a fornecer valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Menor que ou igual a</a> </td><td>Esse operador verifica se o primeiro valor é menor ou igual ao segundo valor</td>
    </tr>
</table>

## Vídeo tutorial{#video}

Saiba como transformar valores de personalização usando funções de ajuda de personalização e entender casos de uso diferentes para funções de ajuda.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)