---
solution: Journey Optimizer
product: journey optimizer
title: Use a atividade Wait em campanhas orquestradas
description: Saiba como usar a atividade de espera em campanhas orquestradas
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/-AI0PuvH2o43jG3d6cpP9-IwD6LxL37nzFv19R-wkcQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 262
ht-degree: 49%

---

# Aguardar {#wait}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a atividade de controle de fluxo de espera para introduzir um atraso cronometrado entre duas atividades em uma campanha Orquestrada para acompanhamento mais bem cronometrado.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Atividade aguardar"
>abstract="A atividade **Aguardar** é usada para atrasar a transição de uma atividade para outra."

A atividade **[!UICONTROL Wait]** é um componente **[!UICONTROL Flow control]** usado para introduzir um atraso entre duas atividades em uma campanha Orquestrada. Isso ajuda a garantir que as atividades de acompanhamento sejam cronometradas melhor e mais relevantes para o engajamento do usuário.

Por exemplo, você pode aguardar alguns dias após a entrega de um email para rastrear aberturas e cliques antes de enviar uma mensagem de acompanhamento.

## Configuração{#wait-configuration}

>[!IMPORTANT]
>
>Os dados em tabelas temporárias não persistem além de **5 dias**. Quando você usar **[!UICONTROL Duração]** ou **[!UICONTROL Tempo fixo]** espera, verifique o tempo decorrido até que a próxima atividade seja concluída dentro desse limite para que os dados intermediários permaneçam disponíveis.

Siga estas etapas para configurar a atividade **[!UICONTROL Aguardar]**:

1. Adicione uma atividade **[!UICONTROL Wait]** à campanha Orquestrada.

1. Selecione o tipo de espera que melhor supre as suas necessidades:

   * **[!UICONTROL Duração]**: especifique um atraso em segundos, minutos, horas ou dias antes de prosseguir para a próxima atividade.

   * **[!UICONTROL Hora fixa]**: defina uma data e uma hora específicas após as quais a próxima atividade iniciará.

   ![](../assets/wait_activity.png)

## Exemplo{#wait-example}

O exemplo a seguir ilustra a atividade **[!UICONTROL Aguardar]** em um caso de uso típico.  Um email com um código promocional é enviado a perfis que estão comemorando seus aniversários. Após 2 dias, um SMS é enviado para o mesmo grupo como um lembrete de que o código promocional de aniversário está prestes a expirar.

![](../assets/wait-example.png)
