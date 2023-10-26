---
title: Usar relatório de spam
description: Saiba como usar o relatório de spam.
feature: Preview
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b6872806b3961bb2afbfc03999d984384492cc6d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---

# Usar relatório de spam {#spam-report}

>[!AVAILABILITY]
>
>O recurso de relatório de spam está disponível no momento como uma versão beta somente para usuários selecionados. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

[!DNL Journey Optimizer] permite que você verifique o desempenho do seu conteúdo em relação à filtragem de spam e certifique-se de que suas mensagens cheguem às caixas de entrada de seus clientes, não ao spam.

>[!CAUTION]
>
>* No momento, esse recurso está disponível apenas para o canal de email.
>
>* Por enquanto, a análise do relatório de spam só pode ser executada para conteúdo em inglês.

Ao editar ou visualizar seu conteúdo, a variável **[!UICONTROL Relatório de spam]** A opção fornece uma pontuação e conselhos para melhorar as pontuações de cada item individual listado.

Isso permite determinar se uma mensagem corre o risco de ser considerada spam pelas ferramentas antisspam usadas no recebimento e tomar medidas se não for o caso.

>[!CAUTION]
>
>O relatório de spam fornece apenas indicações e avisos. Observe que você não será impedido de enviar mensagens se o relatório de Spam indicar que seu conteúdo é considerado spam. É sua escolha agir de acordo com a pontuação e as melhorias sugeridas.

Para usar o **[!UICONTROL Relatório de spam]** siga as etapas abaixo.

<!--For example spam scoring tool can tell that there are too many Images compared to the text. Retailers tend to do this even though the spam score gets worse because the content is more engaging.-->

<!--Michael, who is a marketer with NIKE works along with Tara from testing team to ensure that the emails being sent as part of the campaign/journey don't get categorised as SPAM.

They need an integration within AJO's marketing system to show how the curated content is doing against different SPAM compliance pillars like for SPAM trigger words, HTML Body content and layout, subject line etc.

They should be able to get scores for each individual items as shown by market standard SPAM filtering tools like Spam Assassin, Symantec etc.

They should also get suggestions on how to improve the score better to be confident that the messages don't get categorised as spam.-->

1. No **[!UICONTROL Simular]** clique na guia **[!UICONTROL Relatório de spam]** botão.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Uma verificação antisspam é executada automaticamente e o **[!UICONTROL Relatório de spam]** exibe os resultados. Ele mostra como o conteúdo está se saindo em termos de layout de corpo, estrutura, tamanho da imagem, palavras de acionamento de spam, se houver, etc.

   ![](assets/spam-report-high-score.png)

1. Verifique as pontuações e descrições de cada item.

   Se a pontuação for superior a 5, um aviso será exibido. Ele indica que algumas mensagens podem ser bloqueadas ou marcadas como spam pelas ferramentas antisspam quando recebidas.

1. Com base nessa pontuação, se você considerar que alguns elementos podem ser melhorados, acesse o seu conteúdo usando o [Email Designer](../email/content-from-scratch.md) e faça as atualizações necessárias.

1. Depois que as alterações forem concluídas, volte para a **[!UICONTROL Relatório de spam]** para garantir que sua pontuação tenha melhorado.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->



