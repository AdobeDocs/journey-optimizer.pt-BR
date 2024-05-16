---
title: Usar relatório de spam
description: Saiba como usar o relatório de spam.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 8dacf28f4c3217a57e648b3c80e1724d9794c9ea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Relatório de spam por email {#spam-report}

[!DNL Journey Optimizer] permite que você verifique o desempenho do seu conteúdo em relação à filtragem de spam e certifique-se de que suas mensagens cheguem às caixas de entrada de seus clientes, não ao spam.

Ao editar ou visualizar seu conteúdo de email, a variável **[!UICONTROL Relatório de spam]** A opção fornece uma pontuação e conselhos para melhorar as pontuações de cada item individual listado.

Isso permite determinar se uma mensagem corre o risco de ser considerada spam pelas ferramentas antisspam usadas no recebimento e tomar medidas se não for o caso. Muitos provedores de caixa de entrada de email usam ferramentas como parte de seu processo de filtragem de spam. O envio de emails com uma pontuação inválida pode afetar seriamente sua capacidade de entrega.


>[!CAUTION]
>
>* No momento, esse recurso está disponível apenas como um beta privado.
>
>* Por enquanto, a análise do relatório de spam só pode ser executada para conteúdo em inglês.
>
>* >
>O relatório de spam é informativo e não impede o envio de mensagens com uma pontuação inválida.

Para acessar o **[!UICONTROL Relatório de spam]**, siga as etapas abaixo.

1. No **[!UICONTROL Simular]** clique na guia **[!UICONTROL Relatório de spam]** botão.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Uma verificação antisspam é executada automaticamente e o **[!UICONTROL Relatório de spam]** exibe os resultados. Ele mostra como o conteúdo está se saindo em termos de layout de corpo, estrutura, tamanho da imagem, palavras de acionamento de spam, se houver, etc.

   ![](assets/spam-report-high-score.png)

1. Verifique as pontuações e descrições de cada item.

   Quanto menor a pontuação, melhor. Se a pontuação for superior a 5, um aviso será exibido: indica que algumas mensagens podem ser bloqueadas ou marcadas como spam quando recebidas.

1. Com base nessa pontuação, se você considerar que alguns elementos podem ser melhorados, edite o conteúdo na [Email Designer](../email/content-from-scratch.md) e faça as atualizações necessárias.

1. Quando as alterações forem concluídas, volte para a **[!UICONTROL Relatório de spam]** para garantir que sua pontuação tenha melhorado.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
