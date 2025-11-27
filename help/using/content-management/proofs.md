---
title: Envio de provas de email
description: Saiba como enviar provas de email.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 01ab3f5236acb914c3efe71ffe3d5281d1126589
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 13%

---

# Enviar provas usando dados de perfis de teste {#send-proofs}

Uma prova é uma mensagem específica que permite testar uma mensagem antes de enviá-la ao público-alvo principal. Os destinatários da prova são responsáveis pela aprovação da mensagem: renderização, conteúdo, configurações de personalização, configuração.

>[!NOTE]
>
>O [!DNL Journey optimizer] também permite que você teste diferentes variantes do seu conteúdo visualizando-o e enviando provas usando dados de entrada de exemplo carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba como simular variações de conteúdo](../test-approve/simulate-sample-input.md)

Para enviar provas por email usando dados de perfis de teste, primeiro selecione [perfis de teste](test-profiles.md). Em seguida, siga estas etapas:

1. Na tela **[!UICONTROL Simular]**, clique no botão **[!UICONTROL Enviar prova]**.

   ![](../email/assets/send-proof-button.png)

1. Na janela **[!UICONTROL Enviar prova]**, digite o email do destinatário e clique em **[!UICONTROL Adicionar]** para enviar a prova para você mesmo ou para membros de suas organizações.

   Observe que você pode adicionar até dez recipients para o delivery de prova.

   ![](../email/assets/send-proof-add.png)

1. Selecione os **Perfis de teste** a serem usados para personalizar o conteúdo da mensagem.

   Cada recipient da prova recebe tantas mensagens quanto o número de perfis de teste selecionados. Por exemplo, se você adicionou cinco emails de recipient e selecionou dez perfis de teste, enviará cinquenta mensagens de prova e cada recipient receberá dez deles.

1. Você pode adicionar um prefixo à linha de assunto da prova, se necessário. Somente caracteres alfanuméricos e caracteres especiais como . - _ ( ) [ ] são permitidos como prefixo da linha de assunto.

1. Clique em **[!UICONTROL Enviar prova]**.

   ![](../email/assets/send-proof-select.png)

1. De volta à tela **[!UICONTROL Simular]**, clique no botão **[!UICONTROL Exibir provas]** para verificar o status.

   ![](../email/assets/send-proof-view.png)

É recomendável enviar provas após cada modificação no conteúdo da mensagem.

>[!NOTE]
>
>* Na prova enviada, o link para a mirror page não está ativo. Ele só é ativado nas mensagens finais.
>
>* O Assets/Images pode ser acessado em conteúdo entregue ou conteúdo de prova por até 2 anos (730 dias) desde sua primeira publicação em qualquer fragmento/mensagem em linha. A republicação é necessária após esse período de expiração (a qualquer momento após 730 dias) para mantê-las acessíveis por mais 2 anos. Qualquer republicação feita dentro de 730 dias da primeira publicação não estenderá a expiração de ativos/imagens para os próximos 730 dias.
