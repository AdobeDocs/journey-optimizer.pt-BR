---
solution: Journey Optimizer
product: journey optimizer
title: Criar modelos de conteúdo
description: Saiba como criar modelos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 08d842a877ed52349eef5a901aaf9c75187c69d3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 4%

---

# Trabalhar com modelos de conteúdo {#content-templates}

Para um processo de design acelerado e aprimorado, você pode criar modelos independentes para reutilizar facilmente o conteúdo personalizado em [!DNL Journey Optimizer] campanhas e jornadas.

Essa funcionalidade permite que usuários orientados ao conteúdo trabalhem em modelos fora de campanhas ou jornadas. Os usuários de marketing podem então reutilizar e adaptar esses modelos de conteúdo independente em suas próprias jornadas ou campanhas.

Por exemplo, um usuário em sua empresa é responsável apenas pelo conteúdo e, portanto, não tem acesso a campanhas ou jornadas. No entanto, esse usuário pode criar um modelo de email que os profissionais de marketing de sua organização poderão selecionar para uso em todos os emails como ponto de partida.

➡️ [Saiba como criar e usar modelos neste vídeo](#video-templates)

>[!CAUTION]
>
>Para criar, editar e excluir modelos de conteúdo, você deve ter a variável **[!DNL Manage Library Items]** permissão incluída no **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

## Acessar e gerenciar modelos {#access-manage-templates}

Para acessar a lista de templates de conteúdo, selecione **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** no menu esquerdo.

![](assets/content-template-list.png)

Todos os modelos que foram criados na sandbox atual - de uma jornada ou campanha usando a variável [Salvar como modelo](#save-as-template) da opção **[!UICONTROL Modelos de conteúdo]** são exibidos.

Você pode classificar modelos de conteúdo por data de criação ou modificação. Também é possível optar por exibir apenas os itens que você criou ou modificou.

![](assets/content-template-list-filters.png)

Para editar um conteúdo de modelo, clique no item desejado na lista e selecione **[!UICONTROL Editar conteúdo]**.

![](assets/content-template-list-edit.png)

Para excluir um modelo, selecione o ícone de lixeira ao lado do modelo desejado.

![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Quando um modelo é editado ou excluído, campanhas ou jornadas, incluindo emails criados com esse modelo, não são afetadas.

## Criar modelos de conteúdo {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definir seu próprio modelo de conteúdo"
>abstract="Crie um modelo personalizado independente do zero para tornar seu conteúdo reutilizável em várias jornadas e campanhas."

Há duas maneiras de criar modelos de conteúdo:

* Crie um modelo de conteúdo do zero, usando o painel esquerdo **[!UICONTROL Modelos de conteúdo]** menu. [Saiba como](#create-template-from-scratch)

* Ao criar um email em uma campanha ou jornada, salve o conteúdo do email como template. [Saiba como](#save-as-template)

Depois de salvo, seu template de conteúdo fica disponível para uso em uma campanha ou jornada. Quer tenha sido criado do zero ou de um email anterior, agora é possível usar esse modelo ao criar qualquer [email](get-started-email-design.md) within [!DNL Journey Optimizer]. [Saiba como](email-templates.md)

>[!NOTE]
>
>* As alterações feitas em modelos de conteúdo não são propagadas em campanhas ou jornadas, sejam em tempo real ou em rascunho.
>
>* Da mesma forma, quando os modelos são usados em uma campanha ou jornada, as edições feitas no conteúdo da campanha e da jornada não afetam o modelo de conteúdo usado anteriormente.


### Criar modelo do zero {#create-template-from-scratch}

Para criar um template de conteúdo do zero, siga as etapas abaixo.

1. Acesse a lista de modelos de conteúdo por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** menu à esquerda.

   ![](assets/content-template-list.png)

1. Selecionar **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do template.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Atualmente, somente o **Email** canal e **HTML** são compatíveis.

1. Para atribuir rótulos de uso de dados personalizados ou principais ao modelo, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o Controle de Acesso no Nível do Objeto (OLAC)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]** e escolha como deseja criar seu email a partir das diferentes opções:

   * [Crie seu email do zero](content-from-scratch.md) por meio da interface do Designer de email.

   * [Código ou copie e cole HTML bruto](code-content.md) diretamente no Designer de email.

   * [Importar conteúdo HTML existente](existing-content.md) de um arquivo ou uma pasta .zip.

   * Use conteúdo existente de uma lista de modelos incorporados ou personalizados. As etapas para usar um template de conteúdo em um email estão descritas em [esta seção](email-templates.md).

   ![](assets/content-template-design.png)

1. O [Email Designer](get-started-email-design.md) será exibido. Edite seu conteúdo conforme necessário, da mesma forma que faria com qualquer email dentro de uma jornada ou campanha, de acordo com a opção selecionada.

   ![](assets/content-template-designer.png)

1. Você pode testar seu conteúdo, se necessário. [Saiba como](#test-template)

1. Quando o template estiver pronto, clique em **[!UICONTROL Salvar]**.

1. Se necessário, clique na seta ao lado do nome do modelo para retornar ao **[!UICONTROL Detalhes]** e edite seu modelo.

   ![](assets/content-template-designer-back.png)

Esse template está pronto para ser usado ao criar qualquer email no [!DNL Journey Optimizer]. [Saiba como](email-templates.md)

### Salvar como modelo {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Saiba como migrar suas mensagens"
>abstract="Em 25 de julho de 2022, o menu Mensagens desapareceu e as mensagens agora são criadas diretamente de uma Jornada. Se você quiser reutilizar suas mensagens herdadas no jornada, é necessário salvá-las como modelos."

Ao projetar uma [email](get-started-email-design.md) em uma campanha ou jornada, você pode salvar seu conteúdo de email para futura reutilização. Para fazer isso, siga as etapas abaixo.

1. No Designer de email, clique nas reticências na parte superior direita da tela.

1. Selecionar **[!UICONTROL Salvar como modelo de conteúdo]** no menu suspenso.

   ![](assets/email_designer-save-template.png)

1. Adicione um nome e uma descrição para este modelo.

   ![](assets/email_designer-template-name.png)

1. Clique em **[!UICONTROL Salvar]**.

1. O modelo é salvo no **[!UICONTROL Modelos de conteúdo]** , acessível na [!DNL Journey Optimizer] menu dedicado. Ele se torna um modelo de conteúdo independente que pode ser acessado, editado e excluído como qualquer outro item nessa lista. [Saiba mais](#access-manage-templates)

Agora você pode usar esse modelo ao criar qualquer [email](get-started-email-design.md) within [!DNL Journey Optimizer]. [Saiba como](email-templates.md)

>[!NOTE]
>
>Qualquer alteração nesse novo modelo não é propagada para o email de onde vem. Da mesma forma, quando o conteúdo original é editado nesse email, o novo modelo não é modificado.

## Testar seu modelo de conteúdo {#test-template}

Você pode testar a renderização de qualquer template de conteúdo de email, seja ele criado do zero ou de um email. Para isso, siga as etapas abaixo.

>[!CAUTION]
>
>Para simular o conteúdo, é necessário ter a variável **[!DNL Manage Simulate Content]** permissão incluída no **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

1. Acesse a lista de modelos de conteúdo por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** e selecione qualquer modelo.

1. Clique em **[!UICONTROL Editar conteúdo]** do **[!UICONTROL Propriedades do template]**.

1. Clique em **[!UICONTROL Simular conteúdo]** e selecione um perfil de teste para verificar a renderização de email. Você pode escolher a área de trabalho ou exibição móvel. [Saiba mais](preview.md)

   ![](assets/content-template-stimulate.png)

1. Você pode enviar uma prova para testar seu conteúdo e fazer com que ele seja aprovado por alguns usuários internos antes de usá-lo em uma jornada ou campanha.

   * Para fazer isso, clique no botão **[!UICONTROL Enviar prova]** e siga as etapas descritas em [esta seção](preview.md#send-proofs).

   * Antes de enviar a prova, você deve selecionar a variável [superfície do email](../configuration/channel-surfaces.md) que será usada para testar seu conteúdo.

      ![](assets/content-template-stimulate-proof-surface.png)

## Vídeo tutorial {#video-templates}

Saiba como criar, editar e usar modelos de conteúdo em [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)