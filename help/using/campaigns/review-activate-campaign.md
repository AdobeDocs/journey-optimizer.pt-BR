---
solution: Journey Optimizer
product: journey optimizer
title: Revisar e ativar uma campanha de Ação
description: Saiba como revisar e ativar campanhas de Ação no [!DNL Journey Optimizer].
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaign, review, validation, ativating, ativating, otimizer
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
TQID: https://experienceleague.adobe.com/BKGXccq-kwZJA-cZ4SAyf3zJBIvyJnr5V01xmbQgwmo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 3%

---

# Revisar e ativar a campanha de Ação {#action-campaign-review}

Depois que a campanha Action for configurada, é necessário revisar o parâmetro e o conteúdo antes de ativá-la. Para fazer isso, siga estes passos:

>[!IMPORTANT]
>
> Se a campanha estiver sujeita a uma política de aprovação, é necessário solicitar aprovação para enviar a campanha. [Saiba mais](../test-approve/gs-approval.md)

1. Na tela de configuração da campanha, clique em **[!UICONTROL Revisar para ativar]** para exibir um resumo da campanha.

   ![](assets/campaign-review.png)

1. Um resumo da configuração da campanha é exibido, permitindo verificar se algum parâmetro está incorreto ou ausente e modificar sua campanha, se necessário.

   No caso de erros, não é possível ativar a campanha. Resolva os erros antes de continuar.

   ![](assets/create-campaign-alerts.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Ativar]**.

1. A campanha é ativada. Seu status é **[!UICONTROL Ativo]** ou **[!UICONTROL Agendado]** se você inseriu uma data de início. A mensagem configurada na campanha é enviada imediatamente ou na data especificada.

   O status **[!UICONTROL Concluído]** é atribuído automaticamente à campanha três dias após sua ativação ou na data final da campanha, se ela tiver uma execução recorrente. [Saiba mais sobre os status das campanhas](manage-campaigns.md#statuses).

   Se nenhuma data final tiver sido especificada, a campanha manterá o status **[!UICONTROL Ativo]**. Para alterá-la, é necessário interromper a campanha manualmente. [Saiba como interromper uma campanha](manage-campaigns.md)

1. Depois que uma campanha é ativada, você pode verificar as informações a qualquer momento abrindo-a. O resumo permite obter estatísticas sobre o número de perfis segmentados e ações entregues e com falha.

   Você também pode obter estatísticas adicionais em relatórios dedicados clicando no botão **[!UICONTROL Relatórios]**. [Saiba mais](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)
