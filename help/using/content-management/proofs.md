---
title: Envio de provas de email
description: Saiba como enviar provas de email.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 83da97926138c867ea2dacca6e5cf5e40c926eda
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 16%

---

# Envio de provas de email {#send-proofs}

>[!PREREQUISITES]
>
>Para enviar provas, os usuários devem ter **permissões Aprovar e publicar** para o recurso, campanha ou jornada específica, associada ao email. [Saiba mais sobre permissões](../administration/ootb-permissions.md)

Uma prova é uma mensagem específica que permite testar uma mensagem antes de enviá-la ao público-alvo principal. Os destinatários da prova são responsáveis pela aprovação da mensagem: renderização, conteúdo, configurações de personalização, configuração.

Observe que [!DNL Journey optimizer] também permite que você teste diferentes variantes do seu conteúdo visualizando-o e enviando provas usando dados de entrada de exemplo carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba como testar seu conteúdo usando dados de entrada de exemplo](../test-approve/simulate-sample-input.md)

Para enviar provas de email depois que [perfis de teste](test-profiles.md) forem selecionados, siga estas etapas:

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
>Na prova enviada, o link para a mirror page não está ativo. Ele só é ativado nas mensagens finais.
