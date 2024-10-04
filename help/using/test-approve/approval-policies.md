---
title: Criar e gerenciar políticas de aprovação
description: Saiba como criar e gerenciar políticas de aprovação.
role: User
level: Beginner
feature: Approval
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 94114fac56b68aa0940ae9843f672823d64c19df
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 5%

---


# Criar e gerenciar políticas de aprovação {#approval-policies}

>[!AVAILABILITY]
>
> No momento, as políticas de aprovação estão disponíveis apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.

As políticas de aprovação permitem que os administradores estabeleçam um processo de validação para jornadas e campanhas. Este sistema descreve condições específicas que determinam se uma jornada ou campanha precisa de aprovação. Essas políticas podem variar em complexidade, desde simplesmente exigir que todas as campanhas sejam revisadas por um usuário ou equipe específica até estabelecer critérios com base em quem criou a campanha.

## Criar políticas de aprovação {#create-policies}

1. No menu **[!UICONTROL Administração]**, acesse **[!UICONTROL Permissões]** e **[!UICONTROL Políticas]**.

   ![](assets/policy_create_1.png)

1. Clique em **[!UICONTROL Criar]** na guia **[!UICONTROL Política de Aprovação]**, escolha **[!UICONTROL Política de Aprovação]** e clique em **[!UICONTROL Confirmar]**.

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** para a política.

1. Selecione se a política se aplicará a **[!UICONTROL Jornadas]** ou **[!UICONTROL Campanhas]**.

   ![](assets/policy_create_2.png)

Agora você pode refinar as condições para especificar quem iniciará a solicitação de aprovação e quem a validará.

## Definir condições para políticas de aprovação {#conditions}

1. Acesse sua **[!UICONTROL Política de aprovação]**.

1. No menu **[!UICONTROL If]**, clique em **[!UICONTROL Adicionar condição]** para definir qual objeto ou usuário acionará uma solicitação de aprovação.

1. Escolha a **[!UICONTROL Categoria]**, a **[!UICONTROL Regra de Correspondência]** e as **[!UICONTROL Opções]** apropriadas.

   Por exemplo, &quot;se a ação corresponder a qualquer correspondência direta&quot; ou &quot;Se o nome de usuário do solicitante corresponder a John Doe&quot;.

   ![](assets/policy_condition_1.png)

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
    <td>Acionado pela API (Marketing)</td>
    </tr>
    <tr>
    <td>Acionado pela API (Transacional)</td>
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

   ![](assets/policy_condition_2.png)

1. Para adicionar mais critérios, clique em **[!UICONTROL Adicionar condição]** para definir regras adicionais e selecione **[!UICONTROL And]** ou **[!UICONTROL Or]** para especificar como as condições são conectadas.

1. Depois que a política estiver totalmente configurada, clique em **[!UICONTROL Salvar]**.

Agora você pode ativar sua política de aprovação para aplicá-la.

## Ativar e gerenciar políticas de aprovação {#activate-policies}

1. Acesse sua **[!UICONTROL Política de aprovação]**.

1. Em seguida, clique em **[!UICONTROL Ativar]** para aplicar as condições configuradas ao seu ambiente.

   >[!NOTE]
   >
   >Uma vez ativadas, as políticas não podem ser editadas. Para modificar condições, desative a política primeiro.

   ![](assets/policy_activate_1.png)

1. No menu **[!UICONTROL Política]**, abra as opções avançadas para **[!UICONTROL Editar]**, **[!UICONTROL Desativar]** ou **[!UICONTROL Duplicar]** a política, conforme necessário.

   ![](assets/policy_activate_2.png)

