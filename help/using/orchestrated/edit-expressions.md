---
solution: Journey Optimizer
product: journey optimizer
title: Editar expressões
description: Saiba como editar expressões.
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '2034'
ht-degree: 100%

---


# Editar expressões {#edit-expressions}

>[!NOTE]
>
>A seção abaixo fornece informações sobre como trabalhar com o editor de expressão para criar regras. Lembre-se de que a sintaxe usada para criar regras é diferente da usada para adicionar personalização.

## Trabalhar com o editor de expressão {#edit}

A edição de uma expressão envolve a inserção manual de condições para formar uma regra. Este modo permite usar funções avançadas, que, por sua vez, permitem manipular os valores usados para realizar consultas específicas, como manipular datas, strings, campos numéricos e ordenação.

O editor de expressão está disponível por meio do botão **[!UICONTROL Editar expressão]** do construtor de regras, disponível para os campos **[!UICONTROL Atributo]** e **[!UICONTROL Valor]** ao configurar uma condição personalizada.

| Acesso a partir do campo **Atributo** | Acesso a partir do campo **Valor** |
| --- | --- |
| ![Editor de expressão para o campo “Atributo”](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![Editor de expressão para o campo “Valor”](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

O editor de expressão fornece:

* Um **campo de entrada (1)** no qual a expressão é definida.
* Uma lista de **campos (2)** disponíveis que podem ser usados na expressão e correspondem à dimensão de direcionamento da consulta.
* **Funções auxiliares (3)**, ordenadas por categoria.

Para editar a expressão, insira uma expressão diretamente no campo de entrada. Para adicionar um campo ou uma função auxiliar, coloque o cursor na expressão à qual deseja adicionar o campo e clique no botão +.

![Interface do editor de expressão](assets/rule-builder-expression-editor.png){zoomable="yes"}

## Funções de ajuda

A ferramenta de edição de consultas permite usar funções avançadas para fazer filtragens complexas, dependendo dos resultados desejados e dos tipos de dados manipulados. Os recursos abaixo estão disponíveis.

### Agregado

As funções de agregado efetuam cálculos para um conjunto de valores.

<table>
<tbody>
<tr>
<td><strong>Nome</strong></td>
<td><strong>Descrição</strong></td>
<td><strong>Sintaxe</strong></td>
</tr>
<tr>
<td><strong>Avg</strong></td>
<td>Retorna a média de uma coluna do tipo número</td>
<td>Avg(&lt;valor&gt;)</td>
</tr>
<tr>
<td><strong>Count</strong></td>
<td>Conta os valores não nulos de uma coluna</td>
<td>Count(&lt;valor&gt;)</td>
</tr>
<tr>
<td><strong>CountAll</strong></td>
<td>Conta os valores retornados (todos os campos)</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Countdistinct</strong></td>
<td>Conta os valores não nulos distintos de uma coluna</td>
<td>Countdistinct(&lt;valor&gt;)</td>
</tr>
<tr>
<td><strong>Max</strong></td>
<td>Retorna o valor máximo de uma coluna do tipo número, string ou data</td>
<td>Max(&lt;valor&gt;)</td>
</tr>
<tr>
<td><strong>Min</strong></td>
<td>Retorna o valor mínimo de uma coluna do tipo número, string ou data</td>
<td>Min(&lt;valor&gt;)</td>
</tr>
<tr>
<td><strong>StdDev</strong></td>
<td>Retorna o desvio padrão de uma coluna do tipo número, string ou data</td>
<td>StdDev(&lt;valor&gt;)</td>
</tr>
<tr>
<td><strong>StringAgg</strong></td>
<td>Retorna a concatenação dos valores de uma coluna do tipo string, separados pelo caractere no segundo argumento</td>
<td>StringAgg(&lt;valor&gt;, &lt;string&gt;)</td>
</tr>
<tr>
<td><strong>Sum</strong></td>
<td>Retorna a soma dos valores de uma coluna do tipo número, string ou data</td>
<td>Sum(&lt;valor&gt;)</td>
</tr>
</tbody>
</table>

### Data

As funções de data manipulam valores de data ou hora.

<table>
<tbody>
<tr>
<td><strong>Nome</strong></td>
<td><strong>Descrição</strong></td>
<td><strong>Sintaxe</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>Adiciona um número de dias a uma data</td>
<td>AddDays(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>Adiciona um número de horas a uma data</td>
<td>AddHours(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>Adiciona um número de minutos a uma data</td>
<td>AddMinutes(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>Adiciona um número de meses a uma data</td>
<td>AddMonths(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>Adiciona um número de segundos a uma data</td>
<td>AddSeconds(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>AddYears</strong></td>
<td>Adiciona um número de anos a uma data</td>
<td>AddYears(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>Converte o carimbo de data/hora NTZ (carimbo de data/hora sem fuso horário) em TZ (carimbo de data/hora com fuso horário), usando o fuso horário definido da sessão</td>
<td>ConvertNTZ(&lt;data+hora&gt;)</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>Compara duas datas</td>
<td>DateCmp(&lt;data&gt;, &lt;data&gt;)</td>
</tr>
<tr>
<td><strong>DateOnly</strong></td>
<td>Retorna somente a data (com a hora em 00:00)</td>
<td>DateOnly(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>Day</strong></td>
<td>Retorna o número que representa o dia da data</td>
<td>Day(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>Retorna o número do dia no ano da data</td>
<td>DayOfYear(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgo</strong></td>
<td>Retorna a data correspondente à data atual menos n dias</td>
<td>DaysAgo(&lt;número&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>Retorna a data (número inteiro aaaammdd) correspondente à data atual menos n dias</td>
<td>DaysAgoInt(&lt;número&gt;)</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>Retorna o número de dias entre duas datas</td>
<td>DaysDiff(&lt;data final&gt;, &lt;data inicial&gt;)</td>
</tr>
<tr>
<td><strong>DaysOld</strong></td>
<td>Retorna a idade em dias de uma data</td>
<td>DaysOld(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>Retorna a data atual do sistema do servidor</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>Hour</strong></td>
<td>Retorna a hora da data</td>
<td>Hour(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>Retorna o número de horas entre duas datas</td>
<td>HoursDiff(&lt;data final&gt;, &lt;data inicial&gt;)</td>
</tr>
<tr>
<td><strong>Minute</strong></td>
<td>Retorna os minutos da data</td>
<td>Minute(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>Retorna o número de minutos entre duas datas</td>
<td>MinutesDiff(&lt;data final&gt;, &lt;data inicial&gt;)</td>
</tr>
<tr>
<td><strong>Month</strong></td>
<td>Retorna o número que representa o mês da data</td>
<td>Month(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>Retorna a data correspondente à data atual menos n meses</td>
<td>MonthsAgo(&lt;número&gt;)</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>Retorna o número de meses entre duas datas</td>
<td>MonthsDiff(&lt;data final&gt;, &lt;data inicial&gt;)</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>Retorna a idade em meses de uma data</td>
<td>MonthsOld(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>Mais antiga</strong></td>
<td>Retorna a data mais antiga em um intervalo</td>
<td>Oldest(&lt;data, data&gt;)</td>
</tr>
<tr>
<td><strong>Second</strong></td>
<td>Retorna os segundos da data</td>
<td>Second(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>Retorna o número de segundos entre duas datas</td>
<td>SecondsDiff(&lt;data final&gt;, &lt;data inicial&gt;)</td>
</tr>
<tr>
<td><strong>SubDays</strong></td>
<td>Subtrai um número de dias de uma data</td>
<td>SubDays(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>SubHours</strong></td>
<td>Subtrai um número de horas de uma data</td>
<td>SubHours(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>SubMinutes</strong></td>
<td>Subtrai um número de minutos de uma data</td>
<td>SubMinutes(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>SubMonths</strong></td>
<td>Subtrai um número de meses de uma data</td>
<td>SubMonths(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>SubSeconds</strong></td>
<td>Subtrai um número de segundos de uma data</td>
<td>SubSeconds(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>SubYears</strong></td>
<td>Subtrai um número de anos de uma data</td>
<td>SubYears(&lt;data&gt;, &lt;número&gt;)</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>Converte uma data + hora em uma data</td>
<td>ToDate(&lt;data + hora&gt;)</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>Converte uma string em uma data + hora</td>
<td>ToDateTime(&lt;string&gt;)</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>Converte uma string em um carimbo de data e hora</td>
<td>ToTimestamp(&lt;string&gt;)</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>Converte uma data + hora em um fuso horário</td>
<td>ToTimeZone(&lt;data&gt;, &lt;fuso horário&gt;)</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>Arredonda uma data + hora para o segundo mais próximo</td>
<td>TruncDate(@lastModified, &lt;número de segundos&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>Arredonda uma data + hora com uma determinada precisão expressa em segundos</td>
<td>TruncDateTZ(&lt;data&gt;, &lt;número de segundos&gt;, &lt;fuso horário&gt;)</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>Arredonda uma data para o trimestre</td>
<td>TruncQuarter(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>TruncTime</strong></td>
<td>Arredonda a parte da hora para o próximo segundo</td>
<td>TruncTime(&lt;data&gt;, &lt;número de segundos&gt;)</td>
</tr>
<tr>
<td><strong>TruncWeek</strong></td>
<td>Arredonda uma data para a semana</td>
<td>TruncWeek(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>Arredonda uma data + hora para 1.º de janeiro do ano</td>
<td>TruncYear(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>Retorna o número que representa o dia da semana correspondente à data (0 = segunda-feira, 6 = domingo)</td>
<td>WeekDay(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>Year</strong></td>
<td>Retorna o número que representa o ano da data</td>
<td>Year(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>Retorna o número que representa o ano e o mês da data</td>
<td>YearAndMonth(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>YearsAgo</strong></td>
<td>Retorna o número de anos entre uma determinada data e a data atual</td>
<td>YearsAgo(&lt;data&gt;)</td>
</tr>
<tr>
<td><strong>YearsDiff</strong></td>
<td>Retorna o número de anos entre duas datas</td>
<td>YearsDiff(&lt;data final&gt;, &lt;data inicial&gt;)</td>
</tr>
<tr>
<td><strong>YearsOld</strong></td>
<td>Retorna a idade em anos de uma data</td>
<td>YearsOld(&lt;data&gt;)</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>Observe que a função **DateOnly** considera o fuso horário do servidor, não o do operador.


### Geomarketing

As funções de geomarketing são usadas para manipular valores geográficos.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrição</strong><br /> </td> 
   <td> <strong>Sintaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Retorna a distância entre dois pontos definidos por sua longitude e latitude, expresso em graus.<br /> </td> 
   <td> Distance(&lt;Longitude A&gt;, &lt;Latitude A&gt;, &lt;Longitude B&gt;, &lt;Latitude B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numérico

As funções numéricas são usadas para converter textos em números.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrição</strong><br /> </td> 
   <td> <strong>Sintaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Retorna o valor absoluto de um número<br /> </td> 
   <td> Abs(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Retorna o número inteiro mais baixo maior ou igual a um número<br /> </td> 
   <td> Ceil(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Retorna o maior inteiro maior ou igual a um número<br /> </td> 
   <td> Floor(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Retorna o maior número de dois números<br /> </td> 
   <td> Greatest(&lt;número 1&gt;, &lt;número 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Retorna o menor de dois números<br /> </td> 
   <td> Least(&lt;número 1&gt;, &lt;número 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Retorna o restante da divisão inteira de n1 por n2<br /> </td> 
   <td> Mod(&lt;número 1&gt;, &lt;número 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Retorna a proporção de dois números expressos como uma porcentagem<br /> </td> 
   <td> Percent(&lt;número 1&gt;, &lt;número 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Retorna o valor aleatório<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Arredonda um número para n decimais<br /> </td> 
   <td> Round(&lt;número&gt;, &lt;número de decimais&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Retorna o sinal do número<br /> </td> 
   <td> Sign(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Converte um inteiro em um flutuante<br /> </td> 
   <td> ToDouble(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Converte um flutuante em um inteiro de 64 bits<br /> </td> 
   <td> ToInt64(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Converte um flutuante em um inteiro<br /> </td> 
   <td> ToInteger(&lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Corta o n1 para que tenha n2 casas decimais<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Outros

Esta tabela contém as demais funções disponíveis.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrição</strong><br /> </td> 
   <td> <strong>Sintaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> String de criptografia fornecida no argumento<br /> </td> 
   <td> AESEncrypt(&lt;valor&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Retorna o valor 1 se a condição for verdadeira. Caso contrário, retornará o valor 2.<br /> </td> 
   <td> Case(When(&lt;condição&gt;, &lt;valor 1&gt;), Else(&lt;valor 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Exclui o Sinalizador no valor<br /> </td> 
   <td> ClearBit(&lt;identificador&gt;, &lt;sinalizador&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Retorna o valor 2 se o valor 1 for zero ou nulo, caso contrário retorna o valor 1<br /> </td> 
   <td> Coalesce(&lt;valor 1&gt;, &lt;valor 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Retorna o valor 3 se o valor 1 for igual ao valor 2. Caso contrário, retorna o valor 4.<br /> </td> 
   <td> Decode(&lt;valor 1&gt;, &lt;valor 2&gt;, &lt;valor 3&gt;, &lt;valor 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Retorna o valor 1 (só pode ser usado como parâmetro da função case)<br /> </td> 
   <td> Else(&lt;valor 1&gt;, &lt;valor 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extrai o domínio de um endereço de email<br /> </td> 
   <td> GetEmailDomain(&lt;valor&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Recupera o URL do servidor da mirror page<br /> </td> 
   <td> GetMirrorURL(&lt;valor&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Retorna o valor 1 se a expressão for verdadeira. Caso contrário, retorna o valor 2<br /> </td> 
   <td> Iif(&lt;condição&gt;, &lt;valor 1&gt;, &lt;valor 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Indica se o Sinalizador está no valor<br /> </td> 
   <td> IsBitSet(&lt;identificador&gt;, &lt;sinalizador&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Retorna o valor 2 se a string 1 estiver vazia, caso contrário, retorna o valor 3.<br /> </td> 
   <td> IsEmptyString(&lt;valor 1&gt;, &lt;valor 2&gt;, &lt;valor 3&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> Retorna um identificador exclusivo<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Retorna a string vazia se o argumento for NULL.<br /> </td> 
   <td> NoNull(&lt;valor&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Retorna o número da linha.<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Força o Sinalizador no valor.<br /> </td> 
   <td> SetBit(&lt;identificador&gt;, &lt;sinalizador&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Converte um número em um booleano<br /> </td> 
   <td> ToBoolean(&lt;número&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Retorna o valor 1 se a expressão for verdadeira. Se não, ele retorna o valor 2 (só pode ser usado como parâmetro da função case)<br /> </td> 
   <td> When(&lt;condição&gt;, &lt;valor 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### String

As funções de string são usadas para manipular um conjunto de strings.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrição</strong><br /> </td> 
   <td> <strong>Sintaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Indica se todos os parâmetros são não nulos e não estão vazios<br /> </td> 
   <td> AllNonNull2(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Indica se todos os parâmetros são não nulos e não estão vazios<br /> </td> 
   <td> AllNonNull3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Retorna o valor ASCII do primeiro caractere na string.<br /> </td> 
   <td> Ascii(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Retorna o caractere correspondente ao código ASCII 'n'<br /> </td> 
   <td> Char(&lt;número&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Retorna a posição da string 2 na string 1.<br /> </td> 
   <td> Charindex(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> Retorna o tamanho da string em bytes<br /> </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Retorna a enésima linha (de 1 a n) da string<br /> </td> 
   <td> GetLine(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Retorna o terceiro parâmetro se os dois primeiros parâmetros forem iguais. Caso contrário, retorna o último parâmetro<br /> </td> 
   <td> IfEquals(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Indica se o memo passado como parâmetro é nulo<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Concatena as strings transmitidas como parâmetros. Adiciona espaços entre as strings, se necessário.<br /> </td> 
   <td> JuxtWords(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Concatena as strings transmitidas como parâmetros. Adiciona espaços entre as strings, se necessário<br /> </td> 
   <td> JuxtWords3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Retorna os primeiros n caracteres da string<br /> </td> 
   <td> Left(&lt;string&gt;, &lt;número&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Retorna o comprimento da string<br /> </td> 
   <td> Length(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Linha</strong><br /> </td> 
   <td> Extrair linha n da string<br /> </td> 
   <td> Line(&lt;string&gt;,&lt;número&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Retorna a string em minúsculas<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Retorna a string concluída à esquerda<br /> </td> 
   <td> LPad (&lt;string&gt;, &lt;número&gt;, &lt;caractere&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Remove espaços à esquerda da string<br /> </td> 
   <td> Ltrim(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Retorna uma representação hexadecimal da chave MD5 de uma string<br /> </td> 
   <td> Md5Digest(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Especifica se o memo contém a string aprovada como um parâmetro<br /> </td> 
   <td> MemoContains(&lt;memo&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> Extrai o valor de um campo XML de seu XPath e dos dados do campo<br /> </td> 
   <td> NodeValue (&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Substitui todas as ocorrências do valor de uma string especificada pelo valor de outra string.<br /> </td> 
   <td> Replace(&lt;string&gt;,&lt;string&gt;,&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Retorna os últimos n caracteres da string<br /> </td> 
   <td> Right(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Retorna a string concluída à direita<br /> </td> 
   <td> RPad(&lt;string&gt;, &lt;número&gt;, &lt;caractere&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Remove espaços à direita da string<br /> </td> 
   <td> Rtrim(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Representação hexadecimal da chave SHA256 de uma string.<br /> </td> 
   <td> Sha256Digest (&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Representação hexadecimal da chave SHA512 de uma string.<br /> </td> 
   <td> Sha512Digest (&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Retorna a string com a primeira letra de cada palavra em maiúsculas<br /> </td> 
   <td> Smart(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extrai a substring iniciando no caractere n1 da string e com n2 de comprimento <br /> </td> 
   <td> Substring(&lt;string&gt;, &lt;deslocamento&gt;, &lt;comprimento&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Converte o número em uma string<br /> </td> 
   <td> ToString(&lt;número&gt;, &lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Retorna a string em maiúsculas<br /> </td> 
   <td> Upper(&lt;string&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Retorna a chave externa de um link passado como um parâmetro se os outros dois parâmetros forem iguais<br /> </td> 
   <td> VirtualLink(&lt;número&gt;, &lt;número&gt;, &lt;número&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Retorna a chave externa (texto) de um link passado como um parâmetro se os outros dois parâmetros forem iguais<br /> </td> 
   <td> VirtualLinkStr(&lt;string&gt;, &lt;número&gt;, &lt;número&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Janela

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nome</strong><br /> </td> 
   <td> <strong>Descrição</strong><br /> </td> 
   <td> <strong>Sintaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Execute a chamada da função SQL inserida como primeiro parâmetro, em “Partição” ou “Ordenar por” dos campos inseridos como segundo parâmetro<br /> </td> 
   <td> _Over_ (&lt;valor&gt;, &lt;valor&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Aplica uma classificação decrescente<br /> </td> 
   <td> Desc(&lt;valor 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Classifica o resultado dentro da partição<br /> </td> 
   <td> OrderBy(&lt;valor 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partições do resultado de um consulta em uma tabela<br /> </td> 
   <td> PartitionBy(&lt;valor 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Gera um número de linha com base na partição da tabela e em uma sequência de classificação.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;valor 1&gt;), OrderBy(&lt;valor 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
