---
solution: Journey Optimizer
product: journey optimizer
title: Instrução condicional (if, then, else)
description: Saiba mais sobre instrução condicional
feature: Journeys
role: Developer
level: Experienced
keywords: avançado, condição, ação, jornada
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 0%

---

# Instrução condicional (if, then, else) {#conditional-instruction}

A instrução condicional (if, then, else) é compatível com o editor avançado. Ele permite definir expressões mais complexas. Ele é composto pelos seguintes elementos:

* **[!UICONTROL if]**: a condição a ser avaliada primeiro.
* **[!UICONTROL then]**: a expressão a ser avaliada caso o resultado da avaliação da condição seja verdadeiro.
* **[!UICONTROL else]**: a expressão a ser avaliada caso o resultado da avaliação da condição seja falso.

>[!NOTE]
>
>São necessários parênteses em todas as expressões.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` deve retornar um **booleano**.

`<expression2>` e `<expression3>` devem ter o mesmo tipo ou tipos compatíveis. As assinaturas compatíveis e os tipos retornados são:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Uso**

A instrução condicional permite otimizar o workflow de jornada reduzindo o número de atividades de condição. Por exemplo, na mesma atividade de ação, é possível especificar duas alternativas para uma definição de campo usando apenas uma expressão de condição.

Exemplo de uma atividade de ação (para um campo que espera uma string como o resultado da instrução condicional):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica a instrução condicional `if / then / else` disponível no editor de expressão avançado de Jornada, incluindo regras de sintaxe, combinações de tipo com suporte e um exemplo de uso prático.

**Intenções:**

* Grave uma expressão condicional usando `if`, `then` e `else` para retornar valores diferentes com base em uma condição booleana
* Reduzir o número de atividades de condição em uma jornada incorporando a lógica condicional em linha em uma única atividade de ação
* Determinar quais combinações de tipos de dados são válidas para as ramificações `then` e `else`
* Aplicar a instrução condicional para rotear tokens de notificação por push para o APNS ou o FCM com base no modelo do dispositivo

**Glossário:**

* **Instrução condicional**: uma construção de expressão `if / then / else` no editor avançado que avalia um booliano e retorna uma das duas expressões *(específica do produto)*
* **Editor de expressão avançado**: a interface Journey Optimizer para gravar expressões complexas usadas em condições, atividades de espera e mapeamento de parâmetros de ação *(específico do produto)*

**Medidas de Proteção:**

* Parênteses são necessários em todas as expressões nas cláusulas `if`, `then` e `else`
* A cláusula `if` (`<expression1>`) deve retornar um tipo booleano
* As expressões `then` e `else` (`<expression2>` e `<expression3>`) devem ter o mesmo tipo ou tipos compatíveis (por exemplo, `decimal` e `integer` são compatíveis, `string` e `integer` não são)
* Nem todas as combinações de tipo são suportadas — somente os pares listados na tabela de assinaturas suportadas são válidos

**Terminologia:**

* Nome canônico: instrução condicional — Acrônimo: none — variantes: if/then/else, condição de estilo ternário
* Sinônimos: &quot;instrução condicional&quot; = &quot;condição embutida&quot; = &quot;expressão if-then-else&quot;
* Não confundir: instrução condicional (expressão em linha) ≠ Atividade de condição (um nó da tela de jornada)

**Perguntas frequentes:**

* **P: A cláusula `if` precisa ser colocada entre parênteses?** — Sim, parênteses são necessários em todas as expressões, incluindo a condição na cláusula `if`.
* **P: Posso usar `if / then / else` para retornar um número de uma ramificação e uma sequência de caracteres de outra?** — Não; `<expression2>` e `<expression3>` devem ter tipos iguais ou compatíveis.
* **P: Como a instrução condicional reduz a complexidade da jornada?** — Permite especificar duas alternativas de valor de campo em uma única atividade de ação usando uma expressão, evitando um nó de atividade de Condição separado na tela.
* **P: Que tipo a instrução condicional retorna se ambas as ramificações forem cadeias de caracteres?** — Retorna um `string`.
* **P: `if / then / else` pode ser usado para selecionar um canal de notificação por push?** — Sim; por exemplo, avaliando o modelo de dispositivo para retornar `'apns'` para dispositivos Apple ou `'fcm'` para outros.

+++
