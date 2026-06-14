---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Mudar dimensão
description: Saiba como usar a atividade Mudar dimensão
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/yN2RlYom4xpdiG0G8pt3U4MeY0C1JjDudDqYg-HPv1w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: 
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 77cddc86596959e06b20154c1e51c6b84375b39b
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 46%

---

# Mudar dimensão {#change-dimension}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a atividade Change dimension para mudar o targeting dimension em uma campanha Orquestrada, por exemplo, alternando de listas de desejos para os recipients vinculados a elas.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Gerar um complemento"
>abstract="É possível gerar uma transição de saída adicional com a população restante, que foi excluída como uma duplicata. Para fazer isso, ative a opção **Gerar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Atividade Mudar dimensão"
>abstract="Essa atividade permite alterar a dimensão de direcionamento à medida que você constrói um público-alvo. Ela desloca o eixo dependendo do modelo de dados e da dimensão de entrada. Por exemplo, você pode mudar da dimensão “contratos” para a dimensão “clientes”."

Como profissional de marketing, você pode aprimorar a segmentação de público mudando de uma entidade de dados para uma relacionada em uma campanha orquestrada. Isso permite ir além dos perfis de usuários e concentrar-se em comportamentos específicos, como compras, reservas ou outras interações.

Para isso, use a atividade **[!UICONTROL Mudar dimensão]**. Ele permite ajustar o targeting dimension durante a campanha Orquestrada.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.
-->

## Configurar a atividade Mudar dimensão {#configure}

Siga estas etapas para configurar a atividade **[!UICONTROL Mudar dimensão]**:

1. Adicione uma atividade **[!UICONTROL Change dimension]** à sua campanha Orquestrada.

   ![](../assets/orchestrated-change-dimension.png)

1. Defina a **[!UICONTROL Nova dimensão de público-alvo]**. A etapa Change dimension usa uma associação externa: todos os registros da população de entrada passam, incluindo aqueles sem entrada correspondente na nova dimensão.

   >[!IMPORTANT]
   >
   >Os registros que não têm perfil correspondente na nova dimensão de direcionamento são **silenciosamente excluídos no momento da entrega da mensagem**. No momento, essa exclusão não é refletida nos logs de exclusão. Para identificar antecipadamente os registros não correspondentes, use a opção **Visualizar resultados** na transição após a etapa Alterar dimensão e verifique se as contagens de registros estão alinhadas às suas expectativas antes de continuar.


## Exemplo {#example}

Este caso de uso foca-se no envio de um SMS a perfis que criaram uma lista de desejos no mês passado.

Comece com uma atividade **[!UICONTROL Criar público-alvo]**, usando a dimensão de direcionamento **[!UICONTROL Lista de desejos]** para identificar todas as listas de desejos relevantes.

Em seguida, adicione uma atividade **[!UICONTROL Change dimension]** para alternar o targeting dimension de **[!UICONTROL Wishlist]** para **[!UICONTROL Recipient].** Essa etapa garante que a campanha Orquestrada segmente os perfis corretos vinculados a essas listas de desejos, permitindo que o SMS seja enviado aos perfis pretendidos.

![](../assets/orchestrated-change-dimension-example.png)
