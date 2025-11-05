---
solution: Journey Optimizer
product: journey optimizer
title: Funções
description: Saiba mais sobre funções em expressões de jornada
feature: Journeys
role: Developer
level: Experienced
keywords: função, expressões, editor, jornada, dados, manipulação
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 9%

---

# Funções {#functions}

As funções são os blocos fundamentais das expressões de jornada dinâmica no Adobe Journey Optimizer. Eles permitem transformar, calcular, validar e manipular dados em tempo real para criar experiências personalizadas para o cliente. Com mais de 60 funções organizadas em categorias intuitivas, você pode criar condições sofisticadas, realizar cálculos complexos e tomar decisões orientadas por dados em cada etapa da jornada do cliente.

## Noções básicas sobre funções

As funções em expressões de jornada seguem um padrão de sintaxe consistente:

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**Características-chave:**

* **Várias assinaturas**: uma função pode ter diferentes assinaturas (diferentes conjuntos de parâmetros ordenados) para acomodar vários casos de uso
* **Retornos específicos de tipo**: cada função tem um tipo específico retornado (cadeia de caracteres, inteiro, booleano, data, lista, etc.)
* **Parâmetros de zero a N**: as funções podem aceitar expressões de 0 a N como parâmetros ordenados, proporcionando flexibilidade na maneira como você as usa

## Por que usar funções?

As funções permitem que você:

* **Criar condições dinâmicas** - Caminhos de jornada de ramificação com base na avaliação de dados em tempo real
* **Personalizar em escala** - Personalizar conteúdo e experiências usando dados do cliente e insights comportamentais
* **Automatizar decisões** - Criar lógica inteligente sem intervenção manual
* **Transformar dados** - Converter, formatar e manipular tipos de dados para garantir a compatibilidade
* **Realizar cálculos** - Executar operações matemáticas e análises estatísticas
* **Validar entradas** - Verifique a qualidade e a integridade dos dados antes de executar uma ação

## Funções por categoria

Procure funções organizadas por seu objetivo principal para encontrar rapidamente a ferramenta certa para suas necessidades.

### Adobe Experience Platform {#aep-functions}

**Segmentação e direcionamento de público-alvo**

Avalie a associação de público-alvo para criar caminhos de jornada personalizados com base nos segmentos de clientes definidos no Adobe Experience Platform.

| Função | Descrição |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Verificar se um indivíduo pertence a um público específico |

[Exibir detalhes da função Adobe Experience Platform →](../functions/functioninaudience.md)

### Funções de agregação {#aggregation-functions}

**Cálculos estatísticos e resumo de dados**

Execute cálculos em conjuntos de valores para obter insights, como médias, contagens, somas e valores mín/máx. Essencial para a tomada de decisões orientadas por dados.

| Função | Descrição |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Calcular valor médio |
| [count](../functions/aggregation-functions.md#count) | Contar elementos não nulos |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Contar apenas valores nulos |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Contar todos os elementos, incluindo nulos |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Contar valores não nulos exclusivos |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Contar valores únicos incluindo nulos |
| [max](../functions/aggregation-functions.md#max) | Localizar valor máximo |
| [min](../functions/aggregation-functions.md#min) | Localizar valor mínimo |
| [sum](../functions/aggregation-functions.md#sum) | Calcular soma total |

[Ver todas as funções de agregação →](../functions/aggregation-functions.md)

### Funções de conversão {#conversion-functions}

**Transformação de tipo de dados**

Converta dados entre diferentes tipos (string, número inteiro, decimal, booleano, data, duração) para garantir a compatibilidade entre operações e fontes de dados.

| Função | Descrição |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Converter para booleano |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Converter apenas para data (sem hora) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Converter para data com hora |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Converter para data e hora sem fuso horário |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Converter para número decimal |
| [toDuration](../functions/conversion-functions.md#toDuration) | Converter em duração |
| [toInteger](../functions/conversion-functions.md#toInteger) | Converter em número inteiro |
| [toString](../functions/conversion-functions.md#toString) | Converter em sequência |

[Ver todas as funções de conversão →](../functions/conversion-functions.md)

### Funções de data {#date-functions}

**Manipulação de data e hora**

Trabalhe com datas, horas e fusos horários para criar condições baseadas em tempo, agendar ações e realizar cálculos temporais.

| Função | Descrição |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Obter a hora atual em milissegundos |
| [inLastDays](../functions/date-functions.md#inLastDays) | Verificar se a data está nos últimos N dias |
| [inLastHours](../functions/date-functions.md#inLastHours) | Verificar se a data está nas últimas N horas |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Verificar se a data está nos últimos N meses |
| [inLastYears](../functions/date-functions.md#inLastYears) | Verificar se a data está nos últimos N anos |
| [inNextDays](../functions/date-functions.md#inNextDays) | Verificar se a data está nos próximos N dias |
| [inNextHours](../functions/date-functions.md#inNextHours) | Verificar se a data está dentro das próximas N horas |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Verificar se a data está nos próximos N meses |
| [inNextYears](../functions/date-functions.md#inNextYears) | Verificar se a data está nos próximos N anos |
| [now](../functions/date-functions.md#now) | Obter data-hora atual |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Obter hora atual com deslocamento |
| [setHours](../functions/date-functions.md#setHours) | Definir horas específicas em data-hora |
| [setDays](../functions/date-functions.md#setDays) | Definir dias específicos em data e hora |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Atualizar fuso horário de data-hora |

[Ver todas as funções de data →](../functions/date-functions.md)

### Listar funções {#list-functions}

**Manipulação e análise de coleção**

Filtre, classifique, transforme e analise matrizes e listas para trabalhar com estruturas de dados complexas e executar operações definidas.

| Função | Descrição |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Obter valores únicos (exclui nulos) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Obter valores únicos (inclui nulos) |
| [filtro](../functions/list-functions.md#filter) | Filtrar lista com base em critérios |
| [getListItem](../functions/list-functions.md#getListItem) | Obter item em índice específico |
| [in](../functions/list-functions.md#in) | Verificar se o valor existe na lista |
| [interseção](../functions/list-functions.md#intersect) | Encontrar elementos comuns entre listas |
| [limite](../functions/list-functions.md#limit) | Limitar número de itens retornados |
| [listSize](../functions/list-functions.md#listSize) | Obter tamanho da lista |
| [serializeList](../functions/list-functions.md#serializeList) | Converter lista em sequência de caracteres |
| [sort](../functions/list-functions.md#sort) | Classificar elementos da lista |

[Ver todas as funções de lista →](../functions/list-functions.md)

### Funções matemáticas {#math-functions}

**Operações matemáticas**

Execute cálculos e transformações numéricas para processamento de dados e lógica de negócios.

| Função | Descrição |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Gerar número aleatório (0-1) |
| [round](../functions/math-functions.md#round) | Arredondar para o número inteiro mais próximo |

[Ver todas as funções matemáticas →](../functions/math-functions.md)

### Funções de string {#string-functions}

**Manipulação e validação de texto**

Processe, transforme, pesquise e valide dados de texto para a criação de conteúdo dinâmico e lógica condicional.

| Função | Descrição |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Concatenar strings |
| [contain](../functions/string-functions.md#contain) | Verificar se a cadeia de caracteres contém subcadeia de caracteres |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | Verificar contém (não diferencia maiúsculas de minúsculas) |
| [endWith](../functions/string-functions.md#endWith) | Verificar se a cadeia de caracteres termina com o sufixo |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | A verificação termina com (não diferencia maiúsculas de minúsculas) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Comparar cadeias de caracteres (não diferencia maiúsculas de minúsculas) |
| [indexOf](../functions/string-functions.md#indexOf) | Localizar primeira posição de ocorrência |
| [isEmpty](../functions/string-functions.md#isEmpty) | Verificar se a cadeia de caracteres está vazia |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Verificar se a cadeia de caracteres não está vazia |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Localizar posição da última ocorrência |
| [length](../functions/string-functions.md#length) | Obter comprimento da sequência de caracteres |
| [lower](../functions/string-functions.md#lower) | Converter para minúsculas |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Corresponder expressão regular |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Verificar diferente de (não diferencia maiúsculas de minúsculas) |
| [replace](../functions/string-functions.md#replace) | Substituir primeira ocorrência |
| [replaceAll](../functions/string-functions.md#replaceAll) | Substituir todas as ocorrências |
| [split](../functions/string-functions.md#split) | Dividir cadeia de caracteres em matriz |
| [startWith](../functions/string-functions.md#startWith) | Verificar se a cadeia de caracteres inicia com o prefixo |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | A verificação começa com (não diferencia maiúsculas de minúsculas) |
| [substr](../functions/string-functions.md#substr) | Extrair subsequência de caracteres |
| [trim](../functions/string-functions.md#trim) | Remover espaços à esquerda/direita |
| [upper](../functions/string-functions.md#upper) | Converter para maiúsculas |
| [uuid](../functions/string-functions.md#uuid) | Gerar UUID |

[Ver todas as funções de string →](../functions/string-functions.md)

## Próximas etapas

Agora que você entende as funções disponíveis, explore:

* **[Editor de expressão avançado](expressionadvanced.md)** - Saiba como criar expressões complexas usando o editor avançado
* **[Sintaxe de expressão](generalities.md)** - Domine as regras de sintaxe para gravar expressões de jornada
* **[Operadores](operators.md)** - Descubra operadores que você pode usar com funções para criar lógica
* **[Referências de campo](field-references.md)** - Entenda como fazer referência a campos de dados em suas expressões
