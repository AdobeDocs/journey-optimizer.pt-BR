---
title: Envio de provas de email
description: Saiba como enviar provas de email.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: f874456748a8bd7fce69c7ad2a7e69380d5336a6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 10%

---

# Enviar provas usando dados de perfis de teste {#send-proofs}

Uma prova é uma mensagem específica que permite testar uma mensagem antes de enviá-la ao público-alvo principal. Os destinatários da prova são responsáveis pela aprovação da mensagem: renderização, conteúdo, configurações de personalização, configuração.

>[!NOTE]
>
>O [!DNL Journey Optimizer] também permite que você teste diferentes variantes do seu conteúdo visualizando-o e enviando provas usando dados de entrada de exemplo carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba como simular variações de conteúdo](../test-approve/simulate-sample-input.md)

## Leitura obrigatória {#must-read}

**Regras de limite de frequência** - Todas as regras de limite de frequência existentes se aplicam a provas. Se você definiu [regras de limite de frequência](../conflict-prioritization/channel-capping.md) (por exemplo, máximo de envios por perfil), esses limites também se aplicam ao envio de provas. Se um perfil de teste já tiver atingido o limite de frequência, as provas serão exibidas como concluídas, mas nenhum email será entregue. Para testes repetidos, considere usar perfis de teste exclusivos ou ajustar limites de frequência para cenários de prova, conforme necessário.

**Mirror page** - Na prova enviada, o link para a mirror page não está ativo. Ele só é ativado nas mensagens finais.

**Assets** - Assets e imagens têm regras de acessibilidade específicas:

* O Assets/Images pode ser acessado em conteúdo entregue ou conteúdo de prova por até 2 anos (730 dias) desde sua primeira publicação em qualquer fragmento/mensagem em linha.
* A republicação é necessária após esse período de expiração (a qualquer momento após 730 dias) para mantê-las acessíveis por mais 2 anos.
* Qualquer republicação feita dentro de 730 dias da primeira publicação não estenderá a expiração de ativos/imagens para os próximos 730 dias.

## Enviar provas {#send-proofs-steps}

Para enviar provas por email usando dados de perfis de teste, primeiro selecione [perfis de teste](test-profiles.md). Em seguida, siga estas etapas:

1. Na tela **[!UICONTROL Simular]**, clique no botão **[!UICONTROL Enviar prova]**.

   ![Botão Enviar prova na tela de simulação](../email/assets/send-proof-button.png)

1. Na janela **[!UICONTROL Enviar prova]**, digite o email do destinatário e clique em **[!UICONTROL Adicionar]** para enviar a prova para você mesmo ou para os membros de sua organização.

   Observe que você pode adicionar até dez recipients para o delivery de prova.

   ![Adicionar recipients à entrega de prova](../email/assets/send-proof-add.png)

1. Selecione os **Perfis de teste** a serem usados para personalizar o conteúdo da mensagem.

   Cada recipient da prova recebe tantas mensagens quanto o número de perfis de teste selecionados. Por exemplo, se você adicionou cinco emails de recipients e selecionou dez perfis de teste, enviará cinquenta mensagens de prova. Cada recipient receberá dez deles.

1. Você pode adicionar um prefixo à linha de assunto da prova, se necessário. Somente caracteres alfanuméricos e caracteres especiais como . - _ ( ) [ ] são permitidos como prefixo da linha de assunto.

1. Clique em **[!UICONTROL Enviar prova]**.

   ![Selecione perfis de teste e envie a prova](../email/assets/send-proof-select.png)

1. De volta à tela **[!UICONTROL Simular]**, clique no botão **[!UICONTROL Exibir provas]** para verificar o status.

   ![Botão Exibir provas para verificar o status da entrega](../email/assets/send-proof-view.png)

É recomendável enviar provas após cada modificação no conteúdo da mensagem.
