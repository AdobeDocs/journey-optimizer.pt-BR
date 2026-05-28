---
solution: Journey Optimizer
product: journey optimizer
title: Definir a configuração do SMS
description: Saiba como definir a configuração de SMS/RCS/MMS para enviar mensagens para dispositivos móveis com o Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
TQID: https://experienceleague.adobe.com/J5h64ccVVJUTCIk7FMMolKfEZy6rjEn-jwj1dEntnRM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 5%

---

# Criar uma configuração de mensagem para dispositivo móvel {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definição da categoria da mensagem"
>abstract="Selecione o tipo de mensagem móvel usando essa configuração: marketing para mensagens promocionais, que exigem consentimento do usuário, ou transacional para mensagens não comerciais, como redefinição de senha."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=pt-BR#sms-opt-out-management" text="Recusar em mensagens móveis de marketing"

Depois que o canal de mensagens móveis for configurado, você deverá criar uma configuração de canal para enviar mensagens SMS, RCS e MMS do **[!DNL Journey Optimizer]**.

Para criar uma configuração de canal, siga estas etapas:

1. No painel à esquerda, vá para **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]**. Clique no botão **[!UICONTROL Criar configuração de canal]**.

   ![](assets/preset-create.png)

1. Digite um nome e uma descrição (opcional) para a configuração e selecione o Canal móvel.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar os caracteres de sublinhado `_`, ponto `.` e hífen `-`.

1. Selecione o **[!UICONTROL Tipo de SMS]** para esta configuração:

   * **[!UICONTROL Marketing]**: para mensagens promocionais que exigem consentimento do usuário.
   * **[!UICONTROL Transacional]**: para mensagens não comerciais, como confirmações de pedidos, redefinições de senha ou atualizações de entrega.

   >[!CAUTION]
   >
   >As mensagens **Transacionais** podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing, mas somente em contextos específicos.

   ![](assets/sms-surface-settings.png){width=80%}

1. Selecione a **[!UICONTROL Configuração móvel]** para associar à configuração.

   Para obter mais informações sobre como configurar seu ambiente para enviar mensagens para dispositivos móveis, consulte [esta seção](#create-api).

1. Digite o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

1. Se você quiser usar a função de redução de URL em suas mensagens móveis, selecione um item na lista **[!UICONTROL Subdomínio]**.

   >[!NOTE]
   >
   >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio SMS/RCS/MMS. [Saiba como](mobile-subdomains.md)

1. Na seção **[!UICONTROL Execution dimension]**, use o **[!UICONTROL SMS Execution Field]** para selecionar entre os atributos do perfil o número de telefone que você deseja usar em prioridade se vários números estiverem disponíveis no banco de dados. [Saiba mais](../configuration/primary-email-addresses.md#override-execution-address-channel-config)

   >[!NOTE]
   >
   >Por padrão, [!DNL Journey Optimizer] usa o número de telefone especificado nas [configurações gerais](../configuration/primary-email-addresses.md) no nível da sandbox. Atualizar esse campo substitui o valor padrão para as jornadas e campanhas que usam essa configuração.

1. Selecione **[!UICONTROL Usar conjunto de dados personalizado para entrada]** para rotear o SMS de entrada desta credencial para um conjunto de dados pré-criado que você escolher na lista suspensa. [Saiba mais sobre como usar um conjunto de dados personalizado para palavras-chave de entrada](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >O esquema do conjunto de dados deve ser **[!UICONTROL XDM ExperienceEvent]** e incluir pelo menos estes grupos de campos:
   >* Adobe CJM ExperienceEvent - Detalhes de interação da mensagem
   >* Adobe CJM ExperienceEvent - Detalhes da execução da mensagem
   >* Adobe CJM ExperienceEvent - Detalhes do perfil da mensagem
   >
   >O esquema e o conjunto de dados devem ser habilitados para o Perfil.

1. Depois que todos os parâmetros tiverem sido configurados, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a configuração do canal como rascunho e retomar a configuração posteriormente.

   ![](assets/sms-submit-surface.png)

1. Depois que a configuração do canal é criada, ela é exibida na lista com o status **[!UICONTROL Processando]**.

   >[!NOTE]
   >
   >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha em [esta seção](../configuration/channel-surfaces.md).

1. Depois que as verificações forem bem-sucedidas, a configuração do canal obterá o status **[!UICONTROL Ativo]**. Ele está pronto para ser usado para enviar mensagens.

   ![](assets/preset-active.png)

Agora você está pronto para enviar mensagens móveis com o Journey Optimizer.
