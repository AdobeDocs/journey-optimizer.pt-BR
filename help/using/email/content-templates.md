---
solution: Journey Optimizer
product: journey optimizer
title: Criar modelos de conteúdo
description: Saiba como criar modelos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 1%

---

# Criar modelos de conteúdo {#content-templates}

>[!CONTEXTUALHELP]
>id="ajo_content_templates"
>title="Criar modelos de conteúdo"
>abstract="Crie modelos independentes para reutilizar conteúdo em jornadas e campanhas."

Para um processo de design aceito e aprimorado, você pode criar modelos independentes para reutilizar facilmente o conteúdo personalizado em [!DNL Journey Optimizer] campanhas e jornadas.

Essa funcionalidade permite que usuários orientados ao conteúdo trabalhem em modelos fora de campanhas ou jornadas. Os usuários de marketing podem então reutilizar e adaptar esses modelos de conteúdo independente em suas próprias jornadas ou campanhas.

>[!CAUTION]
>
>Para criar, editar e excluir modelos de conteúdo, você deve ter a variável **[!DNL Manage Library Items]** permissão incluída no **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

Por exemplo, um usuário em sua empresa é responsável apenas pelo conteúdo e, portanto, não tem acesso a campanhas ou jornadas. No entanto, esse usuário pode criar um modelo de email que os profissionais de marketing de sua organização poderão selecionar para uso em todos os emails como ponto de partida.

>[!NOTE]
>
>* As alterações feitas em modelos de conteúdo não são propagadas em campanhas ou jornadas, sejam em tempo real ou em rascunho.
>
>* Da mesma forma, quando os modelos são usados em uma campanha ou jornada, as edições feitas no conteúdo da campanha e da jornada não afetam o modelo de conteúdo usado anteriormente.


➡️ [Saiba como criar e usar modelos neste vídeo](#video-templates)

Para criar um template de conteúdo, siga as etapas abaixo.

1. Para acessar a lista de templates de conteúdo, selecione **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** no menu esquerdo.

   ![](assets/content-template-list.png)

1. Todos os modelos que foram criados na sandbox atual - seja de uma jornada, uma campanha ou da variável **[!UICONTROL Modelos de conteúdo]** são exibidos.

   >[!NOTE]
   >
   >Você pode classificar modelos de conteúdo por data de criação ou modificação.

1. Selecionar **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do template.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Atualmente, somente o **Email** canal e **HTML** são compatíveis.

1. Para atribuir rótulos de uso de dados personalizados ou principais ao modelo, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o Controle de Acesso no Nível do Objeto (OLAC)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]** e escolha como deseja criar seu email com as seguintes opções:

   * **[!UICONTROL Design do zero]**
   * **[!UICONTROL Codifique seu próprio]**
   * **[!UICONTROL Importar HTML]**
   * **[!UICONTROL Selecionar modelo de design]**

   ![](assets/content-template-design.png)

   >[!NOTE]
   >
   >Se você selecionar um modelo, será possível escolher entre **[!UICONTROL Modelos de exemplo]**, que são templates de email prontos para uso, e **[!UICONTROL Modelos salvos]**, que são os que foram criados a partir de uma jornada, uma campanha ou do **[!UICONTROL Modelos de conteúdo]** menu. [Saiba mais](email-templates.md#save-as-template)

1. O Designer de email é exibido. Edite seu conteúdo conforme necessário, da mesma forma que faria com qualquer email dentro de uma jornada ou campanha, de acordo com a opção selecionada:

   * [Crie seu email do zero](content-from-scratch.md) por meio da interface do designer e aproveite imagens de [Adobe Experience Manager Assets Essentials](assets-essentials.md).

   * [Código ou copie e cole HTML bruto](code-content.md) diretamente no Designer de email.

   * [Importar conteúdo HTML existente](existing-content.md) de um arquivo ou uma pasta .zip.

   * [Usar conteúdo existente](email-templates.md) em uma lista de modelos incorporados ou personalizados.

   ![](assets/content-template-designer.png)

1. Clique em **[!UICONTROL Simular conteúdo]** para verificar a renderização de email. Você pode escolher a área de trabalho ou exibição móvel. [Saiba mais](preview.md)

   >[!CAUTION]
   >
   >Para simular o conteúdo, é necessário ter a variável **[!DNL Manage Simulate Content]** permissão incluída no **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

   ![](assets/content-template-stimulate.png)

1. Você pode enviar uma prova para testar seu conteúdo e fazer com que ele seja aprovado por alguns usuários internos antes de usá-lo em uma jornada ou campanha.

   * Para fazer isso, clique no botão **[!UICONTROL Enviar prova]** e siga as etapas descritas em [esta seção](preview.md#send-proofs).

   * Antes de enviar a prova, você deve selecionar a variável [superfície do email](../configuration/channel-surfaces.md) que será usada para testar seu conteúdo.

      ![](assets/content-template-stimulate-proof-surface.png)

1. Quando o template estiver pronto, clique em **[!UICONTROL Salvar]**.

1. Se necessário, clique na seta ao lado do nome do modelo para retornar ao **[!UICONTROL Detalhes]** e edite seu modelo.

   ![](assets/content-template-designer-back.png)

1. Agora você pode usar esse modelo de conteúdo ao criar qualquer [email](get-started-email-design.md) within [!DNL Journey Optimizer]. Saiba mais sobre [usando um modelo salvo](email-templates.md#use-saved-template).

   ![](assets/email_designer-saved-templates.png)

## Vídeo tutorial{#video-templates}

Saiba como criar, editar e usar modelos de conteúdo em [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)