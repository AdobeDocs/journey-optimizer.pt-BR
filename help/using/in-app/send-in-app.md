---
title: Verificação e envio da notificação no aplicativo
description: Saiba como verificar e enviar uma mensagem no aplicativo no Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: no aplicativo, mensagem, criação, iniciar
exl-id: 9e9c235a-b78c-4669-af82-822b6f1e6fca
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 11%

---

# Marque e envie sua notificação no aplicativo {#create-in-app}

## Visualização no dispositivo {#preview-device}

Se você quiser obter uma prévia da Notificação no aplicativo antes que ela entre em vigor para todos os usuários, é possível visualizá-la em um dispositivo específico. Essa funcionalidade permite garantir que a notificação tenha a aparência e funcione conforme pretendido no dispositivo escolhido, fornecendo uma melhor experiência ao usuário para seu público-alvo.

Para fazer isso, siga as etapas abaixo:

1. Clique em **[!UICONTROL Visualizar no dispositivo]**.

   ![](assets/in_app_create_6.png)

1. Na janela **[!UICONTROL Conectar ao dispositivo]**, clique em **[!UICONTROL Iniciar]**.

1. Insira a **[!UICONTROL URL Base]** do seu aplicativo e clique em **[!UICONTROL Avançar]**.

   ![](assets/in_app_create_7.png)

1. Digitalize o código QR com seu dispositivo e insira o código PIN exibido.

A mensagem no aplicativo agora pode ser acionada diretamente no dispositivo, permitindo que você visualize e revise a mensagem em um dispositivo real.

## Visualizar com perfis de teste {#simulate}

Depois que a mensagem no aplicativo for definida, você poderá usar perfis de teste para visualizá-la. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste para verificar sua mensagem usando os dados do perfil de teste.

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

## Revisar e ativar a notificação no aplicativo{#in-app-review}

>[!IMPORTANT]
>
> Se a campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para enviar a notificação no aplicativo. [Saiba mais](../test-approve/gs-approval.md)

Depois que a mensagem no aplicativo for criada e o conteúdo definido e personalizado, você poderá revisá-la e ativá-la.

Para fazer isso, siga as etapas abaixo:

1. Use o botão **[!UICONTROL Revisar para ativar]** para exibir um resumo da sua mensagem.

   O resumo permite modificar a campanha, se necessário, e verificar se algum parâmetro está incorreto ou ausente.

   ![](assets/in_app_create_5.png)

1. Verifique se a campanha está configurada corretamente e clique em **[!UICONTROL Ativar]**.

Sua campanha agora está ativada. A notificação no aplicativo configurada na campanha é enviada imediatamente ou na data especificada.

Depois de enviado, você pode medir o impacto das mensagens no aplicativo nos relatórios do Campaign ou do Jornada. Para obter mais informações sobre relatórios, consulte [esta seção](../reports/campaign-global-report-cja-inapp.md).

**Tópicos relacionados:**

* [Criação de uma mensagem no aplicativo](create-in-app.md)
* [Criar mensagem no aplicativo](design-in-app.md)
* [Relatório no aplicativo](../reports/campaign-global-report-cja-inapp.md)
* [Configuração no aplicativo](inapp-configuration.md)
