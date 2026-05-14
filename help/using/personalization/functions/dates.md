---
title: Biblioteca de funções de Data e hora
description: Biblioteca de funções de Data e hora
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
TQID: https://experienceleague.adobe.com/J-aZtYitBu8T4oSwTwKNNDeA-7tA4l8Wi5YZ1WLcT3E
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c5ecc28ec44a9c608f4fe5011e061cad62d92e2b
workflow-type: tm+mt
source-wordcount: 1762
ht-degree: 5%

---

# Funções de data e hora{#date-time}

As funções de data e hora são usadas para executar operações de data e hora em valores dentro do Journey Optimizer.

>[!NOTE]
>
>A função `now()` não está disponível no editor de personalização. Use `getCurrentZonedDateTime()` ou `currentTimeInMillis()` como alternativa para os valores atuais de data/hora. [Saiba mais](../../email/code-content.md#date-time-limitations)

## Adicionar dias {#add-days}

A função `addDays` ajusta uma determinada data por um número especificado de dias, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addDays(date, number) %}
```

+++Exemplo

* Entrada: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Saída: `2024-11-11T17:19:51Z`

+++

## Adicionar Horas {#add-hours}

A função `addHours` ajusta uma determinada data por um número especificado de horas, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addHours(date, number) %}
```

+++Exemplo

* Entrada: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Saída: `2024-11-01T18:19:51Z`

+++

## Adicionar Minutos {#add-minutes}

A função `addMinutes` ajusta uma determinada data por um número especificado de minutos, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addMinutes(date, number) %}
```

+++Exemplo

* Entrada: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Saída: `2024-11-01T18:09:51Z`

+++

## Adicionar meses {#add-months}

A função `addMonths` ajusta uma determinada data por um número especificado de meses, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addMonths(date, number) %}
```

+++Exemplo

* Entrada: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Saída: `2025-01-01T17:19:51Z`

+++

## Adicionar segundos {#add-seconds}

A função `addSeconds` ajusta uma determinada data por um número especificado de segundos, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addSeconds(date, number) %}
```

+++Exemplo

* Entrada: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Saída: `2024-11-01T17:20:01Z`

+++

## Adicionar anos {#add-years}

A função `addYears` ajusta uma determinada data por um número especificado de anos, usando valores positivos para incrementar e valores negativos para decrementar.

**Sintaxe**

```sql
{%= addYears(date, number) %}
```

+++Exemplo

* Entrada: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Saída: `2026-11-01T17:19:51Z`

+++

## Idade{#age}

A função `age` é usada para recuperar a idade de uma determinada data.

**Sintaxe**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Idade (em dias) {#age-days}

A função `ageInDays` calcula a idade de uma determinada data em dias, ou seja, o número de dias decorridos entre a determinada data e a data atual, negativo para datas futuras e positivo para datas passadas.

**Sintaxe**

```sql
{%= ageInDays(date) %}
```

+++Exemplo

currentDate = 2025-01-07T12:17:10.720122+05:30 (Ásia/Calcutá)

* Entrada: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Saída: `5`

+++

## Idade em meses {#age-months}

A função `ageInMonths` calcula a idade de uma determinada data em meses, ou seja, o número de meses decorridos entre a determinada data e a data atual , negativo para datas futuras e positivo para datas passadas.

**Sintaxe**

```sql
{%= ageInMonths(date) %}
```

+++Exemplo

currentDate = 2025-01-07T12:22:46.993748+05:30(Ásia/Calcutá)

* Entrada: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Saída: `12`

+++

## Comparar datas {#compare-dates}

A função `compareDates` compara a primeira data de entrada com a outra. Retorna 0 se data1 for igual a data2, -1 se data1 for anterior a data2 e 1 se data1 for posterior a data2.

**Sintaxe**

```sql
{%= compareDates(date1, date2) %}
```

+++Exemplo

* Entrada: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Saída: `-1`

+++

## Converter ZonedDateTime {#convert-zoned-date-time}

A função `convertZonedDateTime` converte uma data-hora em um determinado fuso horário.

**Sintaxe**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Exemplo

* Entrada: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Saída: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## Tempo atual em milissegundos{#current-time}

A função `currentTimeInMillis` é usada para recuperar a hora atual em milissegundos da época.

**Sintaxe**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Diferença de data{#date-diff}

A função `dateDiff` é usada para recuperar a diferença entre duas datas em número de dias.

**Sintaxe**

```sql
{%= dateDiff(datetime,datetime) %}
```

+++Exemplo — Dias restantes até um evento

A operação a seguir retorna o número de dias entre hoje e uma data futura armazenada no perfil (por exemplo, uma data de término de assinatura ou uma data de evento):

```sql
{%= dateDiff(getCurrentZonedDateTime(), stringToDate(profile.events.subscriptionEndDate)) %}
```

+++

+++Exemplo do mundo real — Contagem regressiva na linha de assunto

Use `dateDiff` para criar uma contagem regressiva dinâmica para linhas de assunto ou conteúdo do email:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%} — use them before they're gone!
{%else%}
Your points have expired.
{%/if%}
```

Saída (exemplo): `Your points expire in 7 days — use them before they're gone!`

+++

## Dia do mês {#day-month}

`dayOfMonth` retorna o número que representa o dia do mês.

**Sintaxe**

```sql
{%= dayOfMonth(datetime) %}
```

+++Exemplo

* Entrada: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Saída: `5`

+++


## Dia da semana {#day-week}

A função `dayOfWeek` é usada para recuperar o dia da semana. Ele retorna um número inteiro de 1 (segunda-feira) a 7 (domingo) seguindo o padrão ISO-8601.

**Sintaxe**

```sql
{%= dayOfWeek(datetime) %}
```

+++Exemplo — Detectar fins de semana em conteúdo personalizado

Use essa função no email ou no conteúdo para adaptar as mensagens com base no dia. O operador de comparação no PQL é `=` (único igual a, não `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — your request will be processed on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

| Day | Valor retornado |
|-----|----------------|
| Segunda-feira | 1 |
| Terça-feira | 2 |
| Quarta-feira | 3 |
| Quinta-feira | 4 |
| Sexta-feira | 5 |
| Sábado | 6 |
| Domingo | 7 |

+++

>[!NOTE]
>
>`dayOfWeek()` foi criado para **personalização de conteúdo** (por exemplo, adaptando o texto do corpo do email com base no dia). Se você precisar **rotear perfis de forma diferente em uma jornada** com base no dia da semana (por exemplo, ignorar fins de semana para uma atividade Wait), use a opção interna **Condição de tempo → Dia da semana**, disponível diretamente na atividade jornada Condition. [Saiba mais](../../building-journeys/condition-activity.md#date_condition)

## Dia do ano{#day-year}

A função `dayOfYear` é usada para recuperar o dia do ano.

**Sintaxe**

```sql
{%= dayOfYear(datetime) %}
```

+++Exemplo

* Entrada: `{%= dayOfYear(stringToDate("2024-03-15T00:00:00Z")) %}`
* Saída: `75`

+++

## Diferença em segundos {#diff-seconds}

A função `diffInSeconds` retorna a diferença entre duas datas em termos de segundos.

**Sintaxe**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Saída: `50`

+++

## Extrair horas {#extract-hours}

A função `extractHours` extrai o componente de hora de um determinado carimbo de data/hora.

**Sintaxe**

```sql
{%= extractHours(date) %}
```

+++Exemplo

* Entrada: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `17`

+++

## Extrair Minutos {#extract-minutes}

A função `extractMinutes` extrai o componente de minuto de um carimbo de data/hora especificado.

**Sintaxe**

```sql
{%= extractMinutes(date) %}
```

+++Exemplo

* Entrada: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `19`

+++

+++Exemplo do mundo real — Exibir hora atual como HH:MM apenas

Combine `extractHours` e `extractMinutes` para renderizar apenas a porção de tempo sem data, dia ou ano:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is confirmed for {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Saída (exemplo): `Your appointment is confirmed for 14:05.`

A proteção zero à esquerda (`{%#if m < 10%}0{%/if%}`) garante que os minutos abaixo de 10 sejam exibidos como dois dígitos (por exemplo, `09` em vez de `9`).

+++

## Extrair meses {#extract-months}

A função `extractMonth` extrai o componente de mês de um determinado carimbo de data/hora.

**Sintaxe**

```sql
{%= extractMonths(date) %}
```

+++Exemplo

* Entrada: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `11`

+++

## Extrair segundos {#extract-seconds}

A função `extractSeconds` extrai o segundo componente de um determinado carimbo de data/hora.

**Sintaxe**

```sql
{%= extractSeconds(date) %}
```

+++Exemplo

* Entrada: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `51`

+++

## Formatar data{#format-date}

A função `formatDate` é usada para formatar um valor de data e hora. O formato deve ser um padrão DateTimeFormat do Java válido.

**Sintaxe**

```sql
{%= formatDate(datetime, format) %}
```

Onde o primeiro parâmetro é o atributo date-time e o segundo valor é como você gostaria que a data fosse convertida e exibida.

>[!NOTE]
>
> A função `formatDate` requer um tipo de campo **data-hora** como entrada, não uma cadeia de caracteres. Se o campo estiver armazenado como um tipo de sequência no esquema XDM, primeiro converta-o para data e hora usando uma função de conversão como `stringToDate()` ou `toDateTime()`. Veja os exemplos abaixo.
>
> Se um padrão de data for inválido, a data fallback será para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido na [documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Exemplos**

+++Formatação de um campo de data e hora

A operação a seguir formata um campo de data e hora para o formato MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

+++Primeiro converter uma cadeia de caracteres em data

Se o campo estiver armazenado como uma cadeia de caracteres, você deverá primeiro convertê-lo em data e hora usando `stringToDate()` antes de formatá-lo.

```sql
{%= formatDate(stringToDate(profile.person.birthDayAndMonth), "MM/DD/YY") %}
```

+++

+++Formato de data completo com nome do dia

A operação a seguir retorna um formato de data completo com nome do dia, nome do mês, dia e ano.

```sql
{%= formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy") %}
```

Saída: `Wednesday January 01 2020`

+++

+++Data dinâmica com base na hora do sistema

Você pode formatar a hora atual do sistema para gerar datas dinâmicas. A operação a seguir retorna a data atual no formato MM/dd/AAAA.

```sql
{%= formatDate(getCurrentZonedDateTime(), "MM/dd/YYYY") %}
```

Saída (em 30 de janeiro de 2026): `01/30/2026`

+++

+++Formato de dia da semana

Você pode extrair o dia da semana em forma abreviada.

```sql
{%= formatDate(getCurrentZonedDateTime(), "EEE") %}
```

Saída: `Sun` (para domingo), `Mon` (para segunda-feira), `Tue` (para terça-feira), etc.

Para saída em minúsculas, combine com a função `lowerCase`:

```sql
{%= lowerCase(formatDate(getCurrentZonedDateTime(), "EEE")) %}
```

Saída: `sun`, `mon`, `tue`, etc.

+++

+++Formatação de um carimbo de data e hora a partir de um evento de contexto

Ao usar um carimbo de data e hora de um atributo de contexto de evento de jornada, dois requisitos se aplicam:

* **Vincular o carimbo de data/hora a`toDateTime()`** — os carimbos de data/hora do evento de contexto não são reconhecidos automaticamente como valores de data/hora por `formatDate()`.
* **Quebrar IDs de evento numéricas em acentos graves** — se a ID de evento for um número (por exemplo, `1697323153`), ela deverá ser evitada com acentos graves no caminho da expressão, caso contrário, o editor gerará um erro de sintaxe do PQL.
* **Use `{% let %}` ou `{%= %}` sintaxe** — você pode atribuir o resultado a uma variável com `{% let %}` e renderizá-lo com `{{varName}}` ou usar a sintaxe `{%= %}` embutida diretamente.

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
{{appointmentDate}}
```

Saída (exemplo): `18/03/2026 14:30`

+++

>[!CAUTION]
>
>**Erro comum: &quot;entrada incompatível &#39;(&#39; esperando \&lt;EOF\>&quot;**
>
>Este erro de sintaxe do PQL ocorre ao usar `formatDate()` com um carimbo de data/hora de evento de contexto embutido (`{%= formatDate(...) %}`). As causas mais comuns são uma ID de evento numérica que não está encapsulada em acentos graves (`` ` ``) ou um campo de carimbo de data/hora passado diretamente para `formatDate()` sem primeiro encapsulá-lo em `toDateTime()`. Para corrigir ambos os problemas, use o padrão de atribuição `{% let %}` mostrado no exemplo acima.

### Caracteres padrão {#pattern-characters}

Algumas letras de padrão podem parecer semelhantes, mas representam conceitos diferentes.

| Padrão | Significado | Exemplo (para `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Ano civil (ano padrão) | `2023` |
| `Y` | Ano com base em semana (ISO 8601). Pode diferir nos limites do ano. | `2024` (desde 31 de dezembro de 2023 cai na primeira semana de 2024) |
| `M` | Mês do ano (1-12 ou texto como `Jan`, `January`) | `12` ou `Dec` |
| `m` | Minuto da hora (0-59) | `15` |
| `d` | Dia do mês (1-31) | `31` |
| `D` | Dia do ano (1-366) | `365` |

### Formatar data com suporte local{#format-date-locale}

A função `formatDate` pode ser usada para formatar um valor de data e hora em sua representação sensível a idioma correspondente, ou seja, em um local desejado. O formato deve ser um padrão DateTimeFormat do Java válido.

**Sintaxe**

```sql
{%= formatDate(datetime, format, locale) %}
```

Onde a primeira string é o atributo de data, o segundo valor é como você gostaria que a data fosse convertida e exibida, e o terceiro valor representa o local no formato de string.

>[!NOTE]
>
> Se um padrão de data for inválido, a data fallback será para o formato padrão ISO.
>
> Você pode usar as funções de formatação de data Java conforme resumido na [documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Você pode usar formatação e localidades válidas conforme resumido em [Documentação do Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) e [Localidades com suporte](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Exemplo**

A operação a seguir retornará a data no seguinte formato: MM/dd/AA e localidade FRANÇA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

## Obter CurrentZonedDateTime {#get-current-zoned-date-time}

A função `getCurrentZonedDateTime` retorna a data e a hora atuais com informações de fuso horário.

**Sintaxe**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Exemplo

* Entrada: `{%= getCurrentZonedDateTime() %}`
* Saída: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Diferença de Horas {#hours-difference}

A função `diffInHours` retorna a diferença entre duas datas em termos de horas.

**Sintaxe**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Saída: `10`

+++

## Diferença de Minutos{#diff-minutes}

A função `diffInMinutes` é usada para retornar a diferença entre duas datas em termos de minutos.

**Sintaxe**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Saída: `60`

+++

## Diferença de meses {#months-difference}

A função `diffInMonths` retorna a diferença entre duas datas em termos de meses.

**Sintaxe**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Exemplo

* Entrada: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Saída: `3`

+++

## Definir dias{#set-days}

A função `setDays` é usada para definir o dia do mês para a data-hora especificada.

**Sintaxe**

```sql
{%= setDays(datetime, day) %}
```

+++Exemplo

Defina o dia do mês como 1º:

* Entrada: `{%= setDays(stringToDate("2024-11-15T17:19:51Z"), 1) %}`
* Saída: `2024-11-01T17:19:51Z`

+++

## Definir horas{#set-hours}

A função `setHours` é usada para definir a hora da data-hora.

**Sintaxe**

```sql
{%= setHours(datetime, hour) %}
```

+++Exemplo — Definir um date-time para uma hora específica

* Entrada: `{%= setHours(stringToDate("2024-11-01T17:19:51Z"), 0) %}`
* Saída: `2024-11-01T00:19:51Z`

+++

+++Exemplo real — X dias antes de uma data final dinâmica

Para direcionar um perfil X dias antes de uma data armazenada no perfil (por exemplo, expiração de assinatura), use `addDays` com um valor negativo:

```sql
{%= addDays(stringToDate(profile.subscription.endDate), -7) %}
```

Para normalizar também o tempo para uma hora fixa (por exemplo, 9h), combine com `setHours`:

```sql
{%= setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9) %}
```

+++

## Para data hora {#to-date-time}

A função `ToDateTime` converte a cadeia de caracteres em data. Retorna a data da época como saída para entrada inválida.

**Sintaxe**

```sql
{%= toDateTime(string, string) %}
```

+++Exemplo

* Entrada: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Saída: `2024-11-01T17:19:51Z`

+++

## Para UTC{#to-utc}

A função `toUTC` é usada para converter um datetime em UTC.

**Sintaxe**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Truncar para o início do dia {#truncate-day}

A função `truncateToStartOfDay` é usada para modificar uma determinada data-hora definindo-a como o início do dia com a hora definida como 00:00.

**Sintaxe**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Exemplo

* Entrada: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Saída: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

A função `truncateToStartOfQuarter` é usada para truncar uma data-hora para o primeiro dia de seu trimestre (por exemplo, 1º de janeiro, 1º de abril, 1º de julho, 1º de outubro) em 00:00.

**Sintaxe**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Exemplo

* Entrada: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

A função `truncateToStartOfWeek` modifica uma determinada data-hora definindo-a para o início da semana (segunda-feira às 00:00).

**Sintaxe**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Exemplo

* Entrada: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Saída: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

A função `truncateToStartOfYear` é usada para modificar uma determinada data-hora, truncando-a para o primeiro dia do ano (1º de janeiro) em 00:00.

**Sintaxe**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Exemplo

* Entrada: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Saída: `2024-01-01T00:00Z`

+++

## Semana do ano {#week-of-year}

A função `weekOfYear` é usada para recuperar a semana do ano.

**Sintaxe**

```sql
{%= weekOfYear(datetime) %}
```

+++Exemplo

* Entrada: `{%= weekOfYear(stringToDate("2024-11-01T17:19:51Z")) %}`
* Saída: `44`

+++

## Diferença de anos {#diff-years}

A função `diffInYears` é usada para retornar a diferença entre duas datas em termos de anos.

**Sintaxe**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Exemplo

* Entrada: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Saída: `5`

+++
