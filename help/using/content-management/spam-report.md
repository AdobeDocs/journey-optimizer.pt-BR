---
title: Usar relatório de spam por email
description: Saiba como usar o relatório de spam por email.
feature: Preview
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: d0973e623de8f26b4e9dc5809251f9705333adb9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 2%

---

# Relatório de spam por email {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="Relatório de spam por email"
>abstract="O relatório Spam permite verificar sua pontuação de spam no conteúdo de email. Essa pontuação indica se os ISPs ou provedores de caixa de correio considerarão sua mensagem como spam ou não. Quanto menor a pontuação, melhor. Se a pontuação do seu conteúdo de email for superior a 2, você deve considerar a correção de problemas que estão causando a falha dos testes."

Você pode verificar sua pontuação de spam no conteúdo de e-mail em um relatório dedicado de spam. Usar [SpamAssassin](https://spamassassin.apache.org/){target="_blank"}, o Adobe Journey Optimizer pode testar seu conteúdo de email e atribuir uma pontuação para indicar se os ISPs ou provedores de caixa de correio o considerarão como spam ou não.

>[!AVAILABILITY]
>
>No momento, esse recurso está na versão beta e só está disponível para clientes beta. Para participar do programa beta, entre em contato com o atendimento ao cliente da Adobe.

Ao editar ou visualizar seu conteúdo de email, a variável **[!UICONTROL Relatório de spam]** O botão fornece uma pontuação e conselhos para melhorar as pontuações de cada item individual listado.

Esse recurso permite determinar se uma mensagem pode ser considerada spam pelas ferramentas antisspam usadas no recebimento e tomar medidas, se for o caso. Muitos provedores de caixa de entrada de email usam ferramentas como parte de seu processo de filtragem de spam. O envio de emails com uma pontuação inválida pode afetar seriamente sua capacidade de entrega.

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

   Quanto menor a pontuação, melhor. Se a pontuação for superior a 5, um aviso será exibido: indica que algumas mensagens podem ser bloqueadas ou marcadas como spam quando recebidas. A prática recomendada é ter uma pontuação inferior a 2.

1. Com base nessa pontuação, se você considerar que alguns elementos podem ser melhorados, edite o conteúdo na [Email Designer](../email/content-from-scratch.md) e faça as atualizações necessárias.

1. Quando as alterações forem concluídas, volte para a **[!UICONTROL Relatório de spam]** para garantir que sua pontuação tenha melhorado.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
