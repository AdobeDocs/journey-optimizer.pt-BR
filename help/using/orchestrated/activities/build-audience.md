---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade de criar público-alvo
description: Saiba como usar a atividade Criar público-alvo em uma campanha orquestrada
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 74%

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
>abstract="Selecione o público-alvo assim como faz ao criar uma nova entrega. "

Siga estas etapas para configurar a atividade **[!UICONTROL Criar público-alvo]**:

1. Adicione uma atividade **[!UICONTROL Criar público-alvo]**.

   ![](../assets/build-audience.png)

1. Defina um **[!UICONTROL Rótulo]**.

1. Configure o seu público-alvo, seguindo as etapas detalhadas nas guias abaixo.

1. Escolha a **[!UICONTROL Dimensão de direcionamento]**. A dimensão de direcionamento permite definir a população-alvo da operação: destinatários, beneficiários(as) de contrato, operadores(as), assinantes, etc. Por padrão, o público-alvo é selecionado entre os destinatários.

1. Clique em **[!UICONTROL Continuar]**.

1. Use o construtor de regras para definir sua consulta. [Saiba mais sobre o Construtor de regras nesta seção](../orchestrated-rule-builder.md)

1. Especifique se uma transição de saída deve ser gerada quando o público-alvo estiver vazio.

## Exemplos{#build-audience-examples}

Este é um exemplo de uma campanha Orquestrada com duas atividades **[!UICONTROL Build audience]**. A primeira é direcionada a perfis que têm itens em seus carrinhos, seguida por uma entrega de email. A segunda é direcionada a perfis com uma lista de desejos, seguida por uma entrega de SMS.

![](../assets/build-audience-2.png)
