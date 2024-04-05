---
solution: Journey Optimizer
product: journey optimizer
title: Criar modelos de conteúdo
description: Saiba como criar modelos para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
source-git-commit: 3f844f65609f271e834ebf42749253fd64446a9a
workflow-type: tm+mt
source-wordcount: '1425'
ht-degree: 10%

---

# Trabalhar com modelos de conteúdo {#content-templates}

Para um processo de design acelerado e aprimorado, é possível criar modelos independentes para reutilizar facilmente o conteúdo personalizado em [!DNL Journey Optimizer] campanhas e jornadas.

Essa funcionalidade permite que usuários orientados a conteúdo trabalhem em modelos fora de campanhas ou jornadas. Os usuários de marketing podem então reutilizar e adaptar esses modelos de conteúdo independentes em suas próprias jornadas ou campanhas.

<!--![](../rn/assets/do-not-localize/content-template.gif)-->

>[!NOTE]
>
>Atualmente, os modelos de conteúdo não estão disponíveis para o canal da Web.

Por exemplo, um usuário em sua empresa é responsável apenas pelo conteúdo e, portanto, não tem acesso a campanhas ou jornadas. No entanto, esse usuário pode criar um modelo de email que os profissionais de marketing da sua organização poderão selecionar para uso em todos os emails como ponto de partida.

Você também pode criar e gerenciar modelos de conteúdo usando APIs. Para obter mais informações, consulte [Documentação das APIs do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

➡️ [Saiba como criar e usar modelos neste vídeo](#video-templates)

>[!CAUTION]
>
>Para criar, editar e excluir modelos de conteúdo, você deve ter a **[!DNL Manage library items]** permissão incluída na **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

## Acessar e gerenciar modelos  {#access-manage-templates}

Para acessar a lista de modelos de conteúdo, selecione **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** no menu esquerdo.

![](assets/content-template-list.png)

Todos os modelos criados na sandbox atual - de uma jornada ou campanha usando o **[!UICONTROL Salvar como modelo]** opção, seja a partir da variável **[!UICONTROL Modelos de conteúdo]** - são exibidos. [Saiba como criar modelos](#create-content-templates)

Você pode classificar modelos de conteúdo por:
* Tipo
* Canal
* Data de criação ou modificação
* Tags - [Saiba mais sobre tags](../start/search-filter-categorize.md#tags)

Você também pode optar por exibir somente os itens que você mesmo criou ou modificou.

![](assets/content-template-list-filters.png)

* Para editar o conteúdo de um modelo, clique no item desejado na lista e selecione **[!UICONTROL Editar conteúdo]**.

  ![](assets/content-template-edit.png)

* Para excluir um modelo, selecione a variável **[!UICONTROL Mais ações]** ao lado do modelo desejado e selecione **[!UICONTROL Excluir]**.

  ![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Quando um modelo é editado ou excluído, as campanhas ou jornadas, incluindo o conteúdo criado usando esse modelo, não são afetadas.

### Exibir modelos como miniaturas {#template-thumbnails}

Selecione o **[!UICONTROL Exibição em grade]** para exibir cada modelo como uma miniatura.

>[!AVAILABILITY]
>
>Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno conjunto de clientes.

![](assets/content-template-grid-view.png)

>[!NOTE]
>
>Atualmente, as miniaturas adequadas só podem ser geradas para modelos de conteúdo de email do tipo HTML.

Ao atualizar um conteúdo, talvez seja necessário aguardar alguns segundos antes que as alterações sejam refletidas na miniatura.

## Criar modelos de conteúdo {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definir seu próprio modelo de conteúdo"
>abstract="Crie um modelo personalizado independente partindo do zero para tornar seu conteúdo reutilizável em várias jornadas e campanhas."

Há duas maneiras de criar modelos de conteúdo:

* Criar um modelo de conteúdo do zero, usando o painel esquerdo **[!UICONTROL Modelos de conteúdo]** menu. [Saiba como](#create-template-from-scratch)

* Ao criar o conteúdo em uma campanha ou jornada, salve-o como template. [Saiba como](#save-as-template)

Depois de salvo, seu template de conteúdo fica disponível para uso em uma campanha ou jornada. Seja criado do zero ou de um conteúdo anterior, agora é possível usar esse modelo ao criar qualquer conteúdo dentro [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>* As alterações feitas em modelos de conteúdo não são propagadas para campanhas ou jornadas, estejam elas ativas ou em rascunho.
>
>* Da mesma forma, quando os modelos são usados em uma campanha ou jornada, as edições feitas na campanha e no conteúdo da jornada não afetam o modelo de conteúdo usado anteriormente.

### Criar modelo do zero {#create-template-from-scratch}

Para criar um template de conteúdo do zero, siga as etapas abaixo.

1. Acesse a lista de templates de conteúdo por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** menu esquerdo.

1. Selecionar **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do modelo e selecione o canal desejado.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Atualmente, todos os canais estão disponíveis, exceto a Web.

1. Escolha um **[!UICONTROL Tipo]** para o canal selecionado.

   ![](assets/content-template-type.png)

   * Para **[!UICONTROL E-mail]**, se você selecionar **[!UICONTROL Conteúdo]**, você pode definir a variável [Linha de assunto](../email/create-email.md#define-email-content) como parte do modelo. Se você selecionar **[!UICONTROL HTML]**, você só poderá definir o conteúdo do corpo do email.

   * Para **[!UICONTROL SMS]**, **[!UICONTROL Push]**, **[!UICONTROL No aplicativo]** e **[!UICONTROL Correspondência direta]**, somente o tipo padrão está disponível para o canal atual. Você ainda precisa selecioná-lo.

1. Selecione ou crie tags do Adobe Experience Platform na **[!UICONTROL Tags]** para categorizar seu modelo para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados personalizados ou principais ao modelo, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Criar]** e crie seu conteúdo conforme necessário, da mesma forma que faria com qualquer conteúdo de uma jornada ou campanha, de acordo com o canal selecionado.

   ![](assets/content-template-edition.png)

   Saiba como criar conteúdo para os diferentes canais nas seguintes seções:
   * [Definir conteúdo do email](../email/get-started-email-design.md)
   * [Definir conteúdo de push](../push/design-push.md)
   * [Definir conteúdo de SMS](../sms/create-sms.md#sms-content)
   * [Definir conteúdo da correspondência direta](../direct-mail/create-direct-mail.md)
   * [Definir conteúdo no aplicativo](../in-app/design-in-app.md)

1. Se você estiver criando uma **[!UICONTROL E-mail]** modelo com o **[!UICONTROL HTML]** digite, você pode testar o conteúdo. [Saiba como](#test-template)

1. Quando o modelo estiver pronto, clique em **[!UICONTROL Salvar]**.

1. Clique na seta ao lado do nome do modelo para voltar para a **[!UICONTROL Detalhes]** tela.

   ![](assets/content-template-back.png)

Este template agora está pronto para ser usado ao criar qualquer conteúdo dentro de [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

### Salvar como modelo {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Saiba como migrar as mensagens"
>abstract="Em 25 de julho de 2022, o menu Mensagens desapareceu e as mensagens agora são criadas diretamente na jornada. Se você quiser reutilizar as mensagens herdadas nas jornadas, é necessário salvá-las como modelos."

Ao criar qualquer conteúdo em uma campanha ou jornada, você pode salvá-lo para futura reutilização. Para fazer isso, siga as etapas abaixo.

1. Da mensagem **[!UICONTROL Editar conteúdo]** clique na guia **[!UICONTROL Modelo de conteúdo]** botão.

1. Selecionar **[!UICONTROL Salvar como modelo de conteúdo]** no menu suspenso.

   ![](assets/content-template-button-save.png)

   Se você estiver na [Email Designer](../email/get-started-email-design.md), você também pode selecionar essa opção na **[!UICONTROL Mais]** na parte superior direita da tela.

   ![](assets/content-template-more-button-save.png)

1. Adicione um nome e uma descrição para este template.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >O canal e o tipo atuais são preenchidos automaticamente e não podem ser editados. Para modelos de email criados na [Email Designer](../email/get-started-email-design.md), o **[!UICONTROL HTML]** O tipo é selecionado automaticamente.

1. Selecione ou crie uma tag do Adobe Experience Platform na **Tags** para categorizar seu modelo. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Para atribuir rótulos de uso de dados personalizados ou principais ao modelo, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais](../administration/object-based-access.md).

1. Clique em **[!UICONTROL Salvar]**.

1. O modelo é salvo na variável **[!UICONTROL Modelos de conteúdo]** , acessível na [!DNL Journey Optimizer] menu dedicado. Ele se torna um modelo de conteúdo independente que pode ser acessado, editado e excluído como qualquer outro item nessa lista. [Saiba mais](#access-manage-templates)

Agora você pode usar este template ao criar qualquer conteúdo dentro de [!DNL Journey Optimizer]. [Saiba como](#use-content-templates)

>[!NOTE]
>
>Qualquer alteração nesse novo modelo não será propagada para o conteúdo de onde vem. Da mesma forma, quando o conteúdo original é editado dentro desse conteúdo, o novo modelo não é modificado.

## Testar modelos de conteúdo de email {#test-template}

Você pode testar a renderização de alguns de seus modelos de email, sejam eles criados do zero ou de um conteúdo existente. Para isso, siga as etapas abaixo.

>[!CAUTION]
>
>No momento, os modelos de conteúdo de teste estão disponíveis apenas para **[!UICONTROL E-mail]** modelos com o **[!UICONTROL HTML]** tipo.

1. Acesse a lista de templates de conteúdo por meio da **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** e selecione qualquer template de email.

1. Clique em **[!UICONTROL Editar conteúdo]** do **[!UICONTROL Propriedades do modelo]**.

1. Clique em **[!UICONTROL Simular conteúdo]** e selecione um perfil de teste para verificar a renderização. [Saiba mais](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Você pode enviar uma prova para testar seu conteúdo e aprová-lo por alguns usuários internos antes de usá-lo em uma jornada ou campanha.

   * Para fazer isso, clique no link **[!UICONTROL Enviar prova]** e siga as etapas descritas em [nesta seção](../content-management/proofs.md).

   * Antes de enviar a prova, selecione a variável [superfície de email](../configuration/channel-surfaces.md) que serão usados para testar o conteúdo.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Atualmente, o rastreamento não é compatível ao testar modelos de conteúdo de email, o que significa que o rastreamento de eventos, parâmetros UTM e links de página de aterrissagem não será eficaz nas provas que estão sendo enviadas de um modelo. Para testar o rastreamento, [usar o modelo de conteúdo](../email/use-email-templates.md) em um email e [enviar uma prova](../content-management/preview-test.md#send-proofs).

## Usar modelos de conteúdo {#use-content-templates}

Ao criar conteúdo para qualquer canal (exceto Web) no [!DNL Journey Optimizer], é possível usar um modelo personalizado para que você:

* Criado do zero usando o **[!UICONTROL Modelos de conteúdo]** menu. [Saiba mais](#create-template-from-scratch)

* Salvo a partir de um conteúdo existente em uma jornada ou campanha usando o **[!UICONTROL Salvar como modelo de conteúdo]** opção. [Saiba mais](#save-as-template)

Para começar a criar o conteúdo com um desses modelos, siga as etapas abaixo.

1. Seja em uma campanha ou jornada, depois de selecionar **[!UICONTROL Editar conteúdo]**, clique no link **[!UICONTROL Modelo de conteúdo]** botão.

1. Selecionar **[!UICONTROL Aplicar modelo de conteúdo]**.

   ![](assets/content-template-button.png)

1. Selecione o template de sua escolha na lista. Somente os modelos compatíveis com o canal e/ou tipo selecionado são exibidos.

   ![](assets/content-template-select.png)

   >[!NOTE]
   >
   >Nessa tela, também é possível criar um novo template usando o botão dedicado, que abre uma nova guia.

1. Clique em **[!UICONTROL Confirmar o]**. O template é aplicado ao seu conteúdo.

1. Continue editando seu conteúdo conforme desejado.

>[!NOTE]
>
>Para começar a criar um email a partir de um modelo de conteúdo usando o [Email Designer](../email/get-started-email-design.md), siga as etapas descritas em [nesta seção](../email/use-email-templates.md).

## Vídeo tutorial {#video-templates}

Saiba como criar, editar e usar modelos de conteúdo no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)
