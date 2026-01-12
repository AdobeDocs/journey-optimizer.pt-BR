---
solution: Journey Optimizer
product: journey optimizer
title: Usar direcionamento na otimização de mensagens
description: Saiba como aproveitar as regras de direcionamento para fornecer conteúdo personalizado a segmentos específicos de público-alvo.
role: User
level: Intermediate
keywords: direcionamento, otimização, público-alvo, personalização, regras
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 8%

---

# Usar direcionamento {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_content_targeting_fallback"
>title="O que é conteúdo de substituição?"
>abstract="O conteúdo de substituição permite que o público-alvo receba um conteúdo padrão quando nenhuma regra de direcionamento for qualificada.</br>Se não selecionar essa opção, qualquer público-alvo que não se qualifique para uma regra de direcionamento definida acima não receberá conteúdo."

O direcionamento fornece conteúdo personalizado para segmentos de público-alvo específicos com base em atributos de perfil do usuário ou atributos contextuais.

Ao contrário da experimentação, que é uma atribuição aleatória do conteúdo de uma mensagem, o direcionamento é determinístico em termos de entrega do conteúdo para o público-alvo correto.

Com o direcionamento, regras específicas podem ser definidas com base em:

* **Atributos de perfil de usuário**, como localização (por exemplo, geolocalização), idade ou preferências. Por exemplo, os usuários nos EUA veem uma promoção &quot;Golden Gate&quot;, enquanto os usuários na França veem uma promoção &quot;Torre Eiffel&quot;.

* **Dados contextuais**, como tipo de dispositivo (por exemplo, direcionamento de dispositivo), hora do dia ou detalhes da sessão. Por exemplo, os usuários de desktop recebem conteúdo otimizado para desktop, enquanto os usuários móveis recebem conteúdo otimizado para dispositivos móveis.

* **Públicos-alvo** que podem ser usados para incluir ou excluir perfis que tenham uma associação de público-alvo específica.

Para configurar o direcionamento, siga as etapas abaixo.

1. Crie uma [jornada](../building-journeys/journey-gs.md#jo-build) ou uma [campanha](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Se você estiver em uma jornada, adicione uma atividade de **[!UICONTROL Ação]**, escolha uma atividade de canal e selecione **[!UICONTROL Configurar ação]**. [Saiba mais](../building-journeys/journey-action.md#add-action)

1. Na guia **[!UICONTROL Ações]**, selecione pelo menos uma ação.

1. Na seção **[!UICONTROL Otimização]**, selecione **[!UICONTROL Criar regra de direcionamento]**.

   ![](../campaigns/assets/msg-optimization-select-targeting.png){width=85%}

1. Clique em **[!UICONTROL Criar regra]** > **[!UICONTROL Criar novo]** e use o construtor de regras para definir seus critérios onde você for.

   ![](../campaigns/assets/msg-optimization-create-rule.png){width=100%}

   Por exemplo, defina uma regra para residentes dos EUA, uma regra para residentes da França e uma regra para residentes da Índia.

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. Você também pode clicar em **[!UICONTROL Criar regra]** > **[!UICONTROL Selecionar regra]** para selecionar uma regra de direcionamento existente criada no menu **[!UICONTROL Regras]**. [Saiba mais](../experience-decisioning/rules.md)

   ![](../campaigns/assets/msg-optimization-select-rule.png){width=70%}

   Nesse caso, a fórmula que compõe a regra é simplesmente copiada para a jornada ou campanha. Quaisquer alterações subsequentes dessa regra no menu **[!UICONTROL Regras]** não afetarão a jornada ou a cópia da campanha.

   >[!AVAILABILITY]
   >
   >[A criação de regras de direcionamento](../experience-decisioning/rules.md#create) pelo menu dedicado [!DNL Journey Optimizer] está disponível no momento para organizações que compraram a oferta complementar do Decisioning e estão disponíveis sob demanda para as outras organizações (Disponibilidade limitada).
   >
   >Essa capacidade será implantada progressivamente para todos os clientes. Enquanto isso, entre em contato com o representante da Adobe para obter acesso.

1. Depois de adicionar uma regra, você ainda pode modificá-la. Escolha **[!UICONTROL Editar em linha]** para atualizá-la em movimento usando o construtor de regras ou **[!UICONTROL Selecione a regra]** para escolher outra regra existente.

   ![](../campaigns/assets/msg-optimization-modify-rule.png){width=100%}

   >[!NOTE]
   >
   >Editar uma regra em linha não afeta a regra existente da qual ela se origina.

1. Selecione a opção **[!UICONTROL Habilitar conteúdo de fallback]**, conforme necessário. O conteúdo de fallback permite que o público receba um conteúdo padrão quando nenhuma regra de direcionamento for qualificada.

   >[!NOTE]
   >
   >Se você não selecionar essa opção, qualquer público-alvo que não se qualifique para uma regra de direcionamento definida acima não receberá conteúdo.

1. Salve as configurações da regra de direcionamento.

1. De volta à guia **[!UICONTROL Ações]**, selecione **[!UICONTROL Editar conteúdo]**.

1. Crie o conteúdo apropriado para cada grupo definido pelas suas configurações de regra de direcionamento.

   ![](../campaigns/assets/msg-optimization-targeting-design.png){width=85%}

   Neste exemplo, crie um conteúdo específico para residentes dos EUA, um conteúdo diferente para residentes da França e outro conteúdo para residentes da Índia.

1. [Ative](review-activate-campaign.md) sua jornada ou campanha.

Uma vez que a jornada/campanha esteja ativa, o conteúdo personalizado para cada target é enviado para que os residentes dos EUA recebam uma mensagem específica, os residentes da França recebam uma mensagem diferente e assim por diante.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

