---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de criar público-alvo
description: Saiba como usar a atividade Criar público-alvo em uma campanha orquestrada
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/9hEr5kAHco1iq8arv-FddaG3vm54CS-cPFUA63soeAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 56%

---

# Criar público-alvo {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Atividade Criar público-alvo"
>abstract="A atividade **Criar público-alvo** permite definir o público-alvo que entrará na campanha orquestrada. Ao enviar mensagens no contexto de uma campanha orquestrada, o público-alvo da mensagem não é definido na atividade do canal, mas em uma Atividade **criar público-alvo**."

Como profissional de marketing, você pode criar segmentos complexos de público-alvo por meio de uma interface intuitiva, permitindo direcionar usuários com base em uma grande variedade de critérios e comportamentos para adaptar as suas campanhas com mais eficiência.

Para isso, use a atividade de direcionamento **[!UICONTROL Criar público-alvo]**. Essa atividade define o público-alvo que entra na campanha Orquestrada. Ao enviar mensagens como parte de uma campanha Orquestrada, o público-alvo é definido na atividade **[!UICONTROL Criar público-alvo]**, não dentro da campanha Orquestrada.

## Configurar a atividade Criar público-alvo {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Público-alvo"
>abstract="Selecione o público-alvo assim como faz ao criar uma nova entrega."

Siga estas etapas para configurar a atividade **[!UICONTROL Criar público-alvo]**:

1. Adicione uma atividade **[!UICONTROL Criar público-alvo]**.

   ![](../assets/build-audience.png)

1. Defina um **[!UICONTROL Rótulo]**.

1. Configure o seu público-alvo, seguindo as etapas detalhadas nas guias abaixo.

1. Escolha a **[!UICONTROL Dimensão de direcionamento]**. O targeting dimension permite definir o público alvo da operação: recipients, beneficiários de contrato, operadores, assinantes etc. Por padrão, o target é selecionado dos recipients.

1. Clique em **[!UICONTROL Continuar]**.

1. Use o construtor de regras para definir sua consulta. [Saiba mais sobre o Construtor de regras nesta seção](../orchestrated-rule-builder.md)

1. Especifique se uma transição de saída deve ser gerada quando o público-alvo estiver vazio.

## Exemplos{#build-audience-examples}

Este é um exemplo de uma campanha Orquestrada com duas atividades **[!UICONTROL Build audience]**. A primeira é direcionada a perfis que têm itens em seus carrinhos, seguida por uma entrega de email. A segunda é direcionada a perfis com uma lista de desejos, seguida por uma entrega de SMS.

![](../assets/build-audience-2.png)

No exemplo abaixo, a atividade **[!UICONTROL Criar público-alvo]** usa o construtor de regras para filtrar os perfis por seu plano de assinatura. Uma condição está definida no atributo `plan` para incluir apenas perfis em que `plan = "basic"`, restringindo o público-alvo aos assinantes da camada básica antes de passá-los para a próxima atividade.

![](../assets/build-audience-plan.png){width="50%" align="left"}
