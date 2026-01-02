---
title: Criar e gerenciar políticas de aprovação
description: Saiba como criar e gerenciar políticas de aprovação.
role: User
level: Beginner
feature: Approval
exl-id: e518cb3c-f361-43a4-b9a5-ec070c612e75
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 11%

---

# Criar e gerenciar políticas de aprovação {#approval-policies}

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_approval"
>title="Solicitar aprovação"
>abstract="Solicitar aprovação"

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_change"
>title="Solicitar alteração"
>abstract="Solicitar alteração"

>[!NOTE]
>
>Para criar políticas de aprovação, você deve ter privilégios de administrador do sistema ou do produto no Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/home)

As políticas de aprovação permitem que os administradores estabeleçam um processo de validação para jornadas e campanhas. Este sistema descreve condições específicas que determinam se uma jornada ou campanha precisa de aprovação. Essas políticas podem variar em complexidade. Eles podem simplesmente exigir que todas as campanhas sejam revisadas por um usuário ou equipe específica, ou estabelecer critérios com base em quem criou a campanha.

Você pode direcionar políticas de aprovação usando critérios flexíveis, como tags, nomes de campanhas/jornadas, tipos de canais ou informações do solicitante. Por exemplo, você pode exigir aprovação para todos os objetos marcados com &quot;alto risco&quot; ou para qualquer campanha que corresponda a um padrão de nomenclatura específico.

## Criar políticas de aprovação {#create-policies}

>[!CONTEXTUALHELP]
>id="ajo_permissions_approval_policy"
>title="Nova política de aprovação"
>abstract="Nesta tela, digite o nome e selecione o contexto da política de aprovação; em seguida, crie as condições para determinar quem pode iniciar a solicitação de aprovação e quem pode validar essa solicitação."

Para criar uma política de aprovação, siga estas etapas:

1. No menu **[!UICONTROL Administração]** em [!DNL Journey Optimizer], acesse **[!UICONTROL Permissões]** e **[!UICONTROL Políticas]**.

   ![Botão Criar política de aprovação no menu Permissões](assets/policy_create_1.png)

1. Clique em **[!UICONTROL Criar]** na guia **[!UICONTROL Política de Aprovação]**, escolha **[!UICONTROL Política de Aprovação]** e clique em **[!UICONTROL Confirmar]**.

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** para a política.

1. Selecione se a política se aplicará a **[!UICONTROL Jornadas]** ou **[!UICONTROL Campanhas]**.

<!--
1. Enable the **[!UICONTROL Block self-approval]** to prevent Journey/Campaign creators from approving their own objects.

    ![](assets/policy_create_2.png)
-->

Agora você pode refinar as condições para especificar quem pode iniciar a solicitação de aprovação e quem pode validá-la.

## Definir condições para políticas de aprovação {#conditions}

As políticas de aprovação oferecem opções flexíveis de direcionamento para atender às suas necessidades de governança. Você pode criar políticas de aprovação com base em vários critérios, incluindo:

* **Nomes de campanha/Jornadas**: direcionar objetos específicos por nome
* **Marcas**: aplique políticas a todas as campanhas ou jornadas com uma marca específica
* **Tipos de canal**: exigir aprovação para ações específicas (email, SMS, push etc.)
* **Tipos de campanha**: definir regras diferentes para [Campanhas acionadas por ação vs. API](../campaigns/get-started-with-campaigns.md#campaign-types)
* **Solicitantes**: defina políticas com base em quem cria a campanha ou a jornada

Para definir as condições associadas a uma política de aprovação, siga estas etapas:

1. Acesse sua **[!UICONTROL Política de aprovação]**.

1. No menu **[!UICONTROL If]**, clique em **[!UICONTROL Adicionar condição]** para definir qual objeto ou usuário acionará uma solicitação de aprovação.

1. Escolha a **[!UICONTROL Categoria]**, a **[!UICONTROL Regra de Correspondência]** e as **[!UICONTROL Opções]** apropriadas.

   Por exemplo, &quot;se a ação corresponder a qualquer correspondência direta&quot; ou &quot;Se o nome de usuário do solicitante corresponder a John Doe&quot;.

   ![Interface do construtor de condições da política de aprovação](assets/policy_condition_1.png)

   +++ Saiba mais sobre categorias e opções disponíveis
   <table>
    <tr>
      <th>Categoria</th>
      <th>Opção</th>
    </tr>
    <tr>
      <td rowspan="3">Tipo de campanha</td>
      <td>Agendado (Marketing)</td>
    </tr>
    <tr>
    <td>Acionada por API (Marketing)</td>
    </tr>
    <tr>
    <td>Acionada por API (Transacional)</td>
    </tr>
    <tr>
    <td rowspan="8">Ação</td>
    <td>No aplicativo</td>
    </tr>
    <tr>
    <td>Notificações por push</td>
   </tr>
    <tr>
    <td>SMS</td>
    </tr>
    <tr>
    <td>Email</td>
    </tr>
    <tr>
    <td>Correspondência direta</td>
    </tr>
    <tr>
    <td>Web</td>
    </tr>
    <tr>
    <td>Baseado em código</td>
    </tr>
    <tr>
    <td>Cartão de conteúdo</td>
    </tr>
    <tr>
    <td>Tags</td>
    <td>Nome da tag usada para organizar seus públicos. </td>
    </tr>
    <tr>
    <td>Nome do objeto</td>
    <td>Nome do objeto.</td>
    </tr>
    <tr>
    <td>Usuário do solicitante</td>
    <td>Nome e endereço de email do solicitante designado</td>
    </tr>
    <tr>
    <td>Grupo de usuários solicitante</td>
    <td>Nome do grupo de usuários dos solicitantes designados</td>
    </tr>
    </table>

1. Para adicionar mais critérios, clique em **[!UICONTROL Adicionar condição]** para definir regras adicionais e selecione **[!UICONTROL And]** ou **[!UICONTROL Or]** para especificar como as condições são conectadas.

1. No menu **[!UICONTROL Enviar solicitação de aprovação para]**, clique em **[!UICONTROL Adicionar condição]** para definir qual usuário pode aceitar a solicitação de aprovação.

1. No menu suspenso **[!UICONTROL Categoria]**, selecione se deseja escolher um Grupo de Usuários ou um Usuário individual.

1. Em seguida, no menu suspenso **[!UICONTROL Option]**, selecione o grupo de usuários ou usuário específico.

   O usuário ou grupo de usuários selecionado será responsável pela validação da solicitação de aprovação.

   ![Interface de seleção de destinatário de solicitação de aprovação](assets/policy_condition_2.png)

1. Para adicionar mais critérios, clique em **[!UICONTROL Adicionar condição]** para definir regras adicionais e selecione **[!UICONTROL And]** ou **[!UICONTROL Or]** para especificar como as condições são conectadas.

1. Depois que a política estiver totalmente configurada, clique em **[!UICONTROL Salvar]**.

Agora você pode ativar sua política de aprovação para aplicá-la.

## Ativar e gerenciar políticas de aprovação {#activate-policies}

Para aplicar sua política de aprovação, você deve ativá-la. Para fazer isso, siga estas etapas:

1. Acesse sua **[!UICONTROL Política de aprovação]**.

1. Em seguida, clique em **[!UICONTROL Ativar]** para aplicar as condições configuradas ao seu ambiente.

   >[!NOTE]
   >
   >Uma vez ativadas, as políticas não podem ser editadas. Para modificar condições, desative a política primeiro.

   ![Botão Ativar política de aprovação](assets/policy_activate_1.png)

1. No menu **[!UICONTROL Política]**, abra as opções avançadas para **[!UICONTROL Editar]**, **[!UICONTROL Desativar]** ou **[!UICONTROL Duplicar]** a política, conforme necessário.

   ![Menu de opções de gerenciamento de política de aprovação](assets/policy_activate_2.png)
