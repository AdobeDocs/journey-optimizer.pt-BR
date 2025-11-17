---
solution: Journey Optimizer
product: journey optimizer
title: Práticas recomendadas de SMS para otimização de custo
description: Saiba como otimizar os custos de mensagem SMS gerenciando limites de caracteres, codificação e personalização no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 7eaca4faf61431fa438afc7550ff4b89f95fa192
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Práticas recomendadas para otimização de custo de SMS {#sms-cost-optimization}

As mensagens SMS normalmente são cobradas por provedores com base em um limite de 160 caracteres por mensagem. O envio de mensagens SMS pode gerar custos adicionais se as mensagens forem divididas em várias partes.

Siga estas diretrizes para otimizar sua estratégia de mensagens e reduzir despesas.

## Manter mensagens curtas {#keep-messages-short}

O Journey Optimizer permite até 1.500 caracteres em um corpo de mensagem SMS. Um aviso é exibido quando você excede esse limite e as mensagens além dele acionarão um erro.

A maioria dos provedores de SMS é compatível com a codificação GSM de 7 bits, em que um único SMS pode conter até 160 caracteres. As mensagens que excedem esse comprimento são automaticamente divididas em várias partes do SMS (concatenação):

* **Menos de 160 caracteres**: 1 parte de SMS
* **161-306 caracteres**: 2 partes de SMS
* **307-459 caracteres**: 3 partes de SMS

**Para minimizar os custos**, tente manter as mensagens com menos de 160 caracteres para que sejam cobradas como uma única parte do SMS.

Por exemplo, uma mensagem de 1.600 caracteres pode consumir 10 créditos de SMS, mesmo que apareça como uma única mensagem no Journey Optimizer.

## Evite caracteres especiais que aumentem o comprimento {#avoid-special-characters}

Determinados caracteres, como `| ^ € { } [ ] ~ \`, são contados como dois caracteres na codificação GSM. A inclusão desses caracteres pode fazer com que sua mensagem exceda o **limite de 160 caracteres** mais rapidamente.

## Impedir codificação UCS-2 {#prevent-ucs2-encoding}

Se a mensagem incluir caracteres não GSM, como texto em chinês ou árabe, símbolos de marca registrada ou retornos rígidos de ferramentas de formatação avançada, a mensagem será codificada pelo provedor usando UCS-2, que suporta apenas 70 caracteres por SMS.

Usar a codificação UCS-2 pode aumentar a contagem de caracteres e, consequentemente, afetar o faturamento de mensagens com seu provedor de serviços.

Por exemplo, uma mensagem Unicode de 200 caracteres será entregue em 3 partes de SMS.

## Práticas recomendadas de criação {#authoring-best-practices}

Componha a mensagem SMS final diretamente no Journey Optimizer ou cole-a dos aplicativos de texto simples.

Evite usar aplicativos de rich text, pois eles podem introduzir caracteres ocultos ou quebras de linha que acionam a codificação UCS-2, aumentando potencialmente o número de partes do SMS e os custos associados.

## Verificar contagem de caracteres antes de enviar {#check-character-count}

Use aplicativos de texto simples ou o menu **[!UICONTROL Simular conteúdo]** do Journey Optimizer para verificar a contagem de caracteres.

Embora o Journey Optimizer exiba uma contagem de caracteres, incluindo espaços, durante a simulação de conteúdo, observe que:

* Ele **não** inclui caracteres gerados pela personalização dinâmica ou determinados caracteres especiais.

* A **x/1500 count** serve como um indicador visual do limite de carga técnica, não do limite por mensagem, por exemplo, o limite de 7 bits do GSM de 160 caracteres.

* O Adobe é compatível com a codificação UTF-8 no editor, que difere da codificação GSM-7-bit.

## Noções básicas sobre relatórios {#understanding-reporting}

**os relatórios do Journey Optimizer** contam a mensagem completa como um envio, independentemente das partes do SMS. Isso ajuda a reduzir a quantidade de perfis ativáveis.

**O relatório do provedor** mostra as partes reais do SMS para entrega e deve ser usado para determinar a cobrança e os excedentes.

## Considerações sobre o Personalization {#personalization-considerations}

A personalização dinâmica pode aumentar o comprimento de uma mensagem. Por exemplo, substituir uma variável por um nome longo pode adicionar caracteres.

## Recursos adicionais {#additional-resources}

Examine os caracteres com suporte e as regras de codificação no [Guia de Suporte ao Caractere de Sinch](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)

