---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Change dimension
description: Saiba como usar a atividade Change dimension
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 22%

---

# Mudar dimensão {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Essa atividade permite alterar o targeting dimension à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e da dimensão de entrada. Por exemplo, você pode mudar da dimensão “contratos” para a dimensão “clientes”."

A atividade **Change dimension** é uma atividade **Targeting**. Essa atividade permite alterar o targeting dimension à medida que você constrói sua campanha orquestrada. Ele desloca o eixo dependendo do template de dados e da dimensão de entrada.

Por exemplo, você pode alternar o targeting dimension de uma campanha orquestrada de &quot;Recipients&quot; para &quot;Subscribers application&quot; para enviar notificações por push aos recipients direcionados.

>[!IMPORTANT]
>
>Observe que as atividades **[!UICONTROL Alterar Dimensão]** e **[!UICONTROL Alterar Fonte de Dados]** não devem ser adicionadas em uma linha. Se você precisar usar ambas as atividades consecutivamente, certifique-se de incluir uma atividade **[!UICONTROL Enriquecimento]** entre elas. Isso garante a execução adequada e evita possíveis conflitos ou erros.

## Configurar a atividade Change dimension {#configure}

Siga estas etapas para configurar a atividade **Alterar dimensão**:

1. Adicione uma atividade **Change dimension** à sua campanha orquestrada.

   ![](../assets/workflow-change-dimension.png)

1. Defina a **Nova dimensão de destino**. Durante a alteração de dimensão, todos os registros são mantidos. Outras opções ainda não estão disponíveis.

1. Execute a campanha orquestrada para ver o resultado. Compare os dados nas tabelas antes e depois da atividade de alteração de dimensão e compare a estrutura das tabelas de campanha orquestradas.

## Exemplo {#example}

Neste exemplo, queremos enviar um delivery de SMS para todos os perfis que fizeram uma compra. Para fazer isso, primeiro usamos uma atividade **[!UICONTROL Build audience]** vinculada a uma dimensão de direcionamento &quot;Purchase&quot; personalizada para direcionar todas as compras que ocorreram.

Em seguida, usamos uma atividade **[!UICONTROL Change dimension]** para alternar a targeting dimension de campanha orquestrada para &quot;Recipients&quot;. Isso nos permite direcionar os recipients que correspondem ao query.

![](../assets/workflow-change-dimension-example.png)
