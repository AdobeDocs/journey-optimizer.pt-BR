---
solution: Journey Optimizer
product: journey optimizer
title: Governança de dados
description: Defina uma política de governança vinculada a um rótulo e uma ação de marketing
feature: Journeys, Actions, Custom Actions, Privacy
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: dados, governança, DULE, rótulos, rotulagem, plataforma, política
exl-id: be3efd3b-35d5-4cf7-9015-29d1e305355d
source-git-commit: f5df65a0225754ab66fb2ffa33c5130f7137b644
workflow-type: tm+mt
source-wordcount: '1292'
ht-degree: 100%

---

# Governança de dados {#restrict-fields}

>[!CONTEXTUALHELP]
>id="ajo_data_governance_policy_violation"
>title="Violação da política de governança de dados"
>abstract="Se o sistema identificar um campo restrito em uma jornada/campanha ou uma ação personalizada, um erro será exibido, impedindo que você a publique. Use o diagrama de linhagem de dados nesta caixa de diálogo para entender quais outras alterações de configuração precisam ser feitas antes que você possa ativar sua jornada ou campanha."

## Introdução às políticas de governança de dados {#gs}

Com sua estrutura de [governança DULE (Aplicação e rotulagem de uso de dados)](https://experienceleague.adobe.com/docs/experience-platform/data-governance/home.html?lang=pt-BR){target="_blank"}, a Adobe Experience Platform permite gerenciar e aplicar políticas de governança de dados em seus canais **rotulando os campos** e criando **ações de marketing** para cada canal.

Depois que os rótulos e as ações de marketing forem definidos, você poderá criar **políticas de governança de dados** que vinculam esses dois elementos. Por exemplo, você pode configurar uma política que associe um rótulo “ePHI” a uma ação de marketing de “direcionamento por email”, garantindo que os campos rotulados como “ePHI” não sejam usados para personalizar mensagens de email. [Saiba como criar políticas de governança de dados](#governance-policies)

Depois de criar as políticas de governança, você pode aplicar as ações de marketing às suas jornadas/campanhas e ações personalizadas das jornadas.
[Saiba como aplicar ações de marketing no Journey Optimizer](#apply-marketing-actions)

Ao criar uma jornada ou campanha, após selecionar uma configuração de canais ou uma ação personalizada, o sistema verifica se a ação de marketing na configuração do canal de mensagem ou na ação personalizada faz parte de uma política de governança de dados. Se sim, o sistema verifica se algum campo do público-alvo ou da personalização da mensagem está rotulado e restrito pela política. Se esse rótulo for detectado, a publicação da jornada ou campanha será bloqueada. [Saiba como detectar uma violação da política de governança de dados](#violation)

## Criar rótulos e ações de marketing {#labels-marketing-actions}

A primeira etapa para aplicar a política de governança de dados é criar rótulos e anexá-los a campos nos quais você deseja restringir o uso, bem como criar ações de marketing para cada um de seus canais.

1. No menu esquerdo, em **Privacidade**, clique em **Políticas**.

1. Selecione a guia **Rótulos** e clique em **Criar rótulo**.

1. Defina um nome e um nome amigável para este rótulo. Por exemplo, _ePHI1_.

1. No menu esquerdo, em **Gestão de dados**, clique em **Esquemas** e clique no botão **Aplicar rótulos de acesso e de governança de dados**. Selecione o esquema e campo (por exemplo, “tipo sanguíneo”) e selecione o rótulo criado anteriormente, _ePHI1_ em nosso exemplo.

   ![](assets/action-privacy3.png)

1. Volte para o menu **Políticas**, selecione a guia **Ação de marketing** e clique em **Criar ação de marketing**. Recomendamos que você crie uma ação de marketing para cada canal e ação personalizada de terceiros usada em suas jornadas. Por exemplo, vamos criar uma _ação de marketing do Slack_ que será usada em sua ação personalizada do Slack.

   ![](assets/action-privacy4.png)

## Criar uma política de governança de dados {#policy}

Agora que os rótulos e as ações de marketing foram criados, você pode vinculá-los em políticas de governança de dados. Para fazer isso, selecione a guia **Navegar**, clique em **Criar política** e selecione **Política de governança de dados**. Selecione seu rótulo (_ePHI1_) e a ação de marketing (_Ação de marketing Slack_).

![](assets/action-privacy5.png)

Em uma jornada, quando você usar sua ação personalizada de Slack configurada com a variável _Ação de marketing Slack_, a política associada será utilizada.

## Aplicar ações de marketing no Journey Optimizer {#apply-marketing-actions}

Para que as políticas de governança de dados sejam aplicadas no Journey Optimizer, é necessário aplicar ações de marketing a suas jornadas, campanhas ou ações personalizadas.

### Aplicar ações de marketing a jornadas e campanhas {#journeys-campaigns}

Depois de criar políticas de governança, você deve aplicar as ações de marketing relevantes nas **configurações de canal** do Journey Optimizer. Para fazer isso, siga estes passos:

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]**.

1. Abra uma configuração de canais existente ou crie uma nova.

1. No campo **[!UICONTROL Ação de marketing]**, selecione as ações de marketing a serem associadas às jornadas e campanhas que usam essa configuração. Todas as políticas de consentimento e governança de dados associadas à ação de marketing são utilizadas, a fim de respeitar as preferências dos clientes e as restrições configuradas para campos confidenciais. [Saiba mais](../action/consent.md#surface-marketing-actions)

   ![](../privacy/assets/governance-channel-configuration.png)

1. Conclua a configuração de canais e salve-a. [Saiba como definir a configuração de canais](../configuration/channel-surfaces.md).

1. Ao criar uma mensagem na jornada ou campanha, selecione a configuração de canais relevante. Complete a configuração da jornada ou campanha e salve-a.

Antes de ativar a jornada ou campanha, o sistema verifica se a ação de marketing na configuração de canais selecionada faz parte de uma política de governança de dados. Se sim, o sistema verifica se algum campo do público-alvo ou da personalização da mensagem está rotulado e restrito pela política.

Se identificar um campo restrito, o sistema exibe um erro, impedindo a publicação da jornada ou da campanha. [Saiba como detectar violações de política de governança](#violation)

![](assets/governance-policy-schema.png){zoomable="yes"}

*Etapas de análise de violação de política em jornadas e campanhas*

### Aplicar ação de marketing a ações personalizadas {#custom-actions}

>[!NOTE]
>
>As ações de jornada do Campaign v7/v8 e do Campaign Standard não são compatíveis.

Vamos ver o exemplo do campo de tipo sanguíneo que você precisa restringir de ser exportado para terceiros usando ações personalizadas. Para fazer isso, você precisa aplicar a ação de marketing à sua ação personalizada, criar sua jornada e adicionar sua ação personalizada nela.

1. No menu esquerdo, em **Administração**, clique em **Configurações** e selecione **Ações**.

1. Abra sua ação personalizada de Slack. Ao configurar uma ação personalizada, dois campos podem ser usados para a governança de dados.

   ![](assets/action-privacy6.png)

   * O campo **Canal** permite selecionar o canal relacionado a esta ação personalizada. O campo **Ação de marketing necessária** será preenchido previamente com a ação de marketing padrão do canal selecionado. Se você selecionar **outros**, nenhuma ação de marketing será definida por padrão. No nosso exemplo, selecionamos o canal **other**.

   * A **Ação de marketing necessária** permite definir a ação de marketing relacionada à sua ação personalizada. Por exemplo, se você usar essa ação personalizada para enviar emails usando um terceiro, você pode selecionar **Direcionamento de email**. No nosso exemplo, selecionamos a variável _Ação de marketing Slack_. As políticas de governança associadas a essa ação de marketing são recuperadas e aproveitadas.

   As outras etapas para configurar uma ação personalizada estão detalhadas [nesta seção](../action/about-custom-action-configuration.md#consent-management).

1. No menu à esquerda, em **Gerenciamento de jornada**, clique em **Jornadas**.

1. Crie a jornada e adicione a ação personalizada. Ao adicionar a ação personalizada em uma jornada, há várias opções que permitem gerenciar a governança de dados. Clique em **Mostrar campos somente leitura** para exibir todos os parâmetros.

   ![](assets/action-privacy7.png)

   * O **Canal** e a **Ação de marketing necessária**, definidos ao configurar a ação personalizada, são exibidos na parte superior da tela. Não é possível modificar esses campos.

   * Você pode configurar uma **Ação de marketing adicional** para definir o tipo de ação personalizada. Isso permite definir a finalidade da ação personalizada nesta jornada. Além da ação de marketing necessária, que geralmente é específica de um canal, é possível definir uma ação de marketing adicional que será específica para a ação personalizada desta jornada. Por exemplo: um comunicado de treino, um boletim informativo, um comunicado de fitness etc. A ação de marketing necessária e a ação de marketing adicional serão aplicadas. No nosso exemplo, não usamos uma ação de marketing adicional.

Se um dos campos rotulados como _ePHI1_ (o campo de tipo sanguíneo no exemplo) for detectado nos parâmetros de ação, um erro será exibido e a jornada não poderá ser publicada. [Saiba como detectar violações de política de governança](#violation)

![](assets/governance-policy-custom-action-schema.png){zoomable="yes"}

*Etapas de análise de violação de política em ações personalizadas de jornadas*

## Detectar violação de política {#violation}

Ao identificar um campo restrito em uma jornada, campanha ou ação personalizada, o sistema exibirá um erro, impedindo que você a publique. 

Os erros são visíveis no botão **[!UICONTROL Alertas]**. Clique no erro para exibir informações detalhadas sobre a violação da política de governança de dados.

![](assets/action-privacy8.png)

Esta caixa de diálogo indica que a configuração atual da jornada ou campanha viola uma política de governança de dados existente. Use o diagrama de linhagem de dados para entender quais outras alterações de configuração precisam ser feitas antes que você possa ativar sua jornada ou campanha.

Para obter informações detalhadas, acesse a [documentação de violação da política de uso de dados](https://experienceleague.adobe.com/pt-br/docs/experience-platform/data-governance/enforcement/auto-enforcement#data-usage-violation){_blank}.
