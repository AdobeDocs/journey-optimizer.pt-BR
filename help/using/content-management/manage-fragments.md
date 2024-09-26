---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar fragmentos
description: Saiba como gerenciar os fragmentos de conteúdo
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 25%

---

# Gerenciar fragmentos {#manage-fragments}

Para gerenciar os fragmentos, acesse a lista de fragmentos do menu esquerdo **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**.

Todos os fragmentos criados na sandbox atual - [no menu **[!UICONTROL Fragmentos]**](#create-fragments), usando a opção [Salvar como fragmento](#save-as-fragment) - são exibidos.

![](assets/fragment-list-filters.png)

Você pode filtrar fragmentos em:

* Status (Rascunho ou Ativo)
* Tipo (visual ou expressão)
* Data de criação ou modificação
* Estado (arquivado ou não)
* Tags

Você também pode optar por mostrar todos os fragmentos ou somente os itens que o usuário atual criou ou modificou.

No botão **[!UICONTROL Mais ações]** ao lado de cada fragmento, é possível:

* Duplique um fragmento.
* Use a opção **[!UICONTROL Explorar referências]** para ver as jornadas, campanhas ou modelos em que é usado. [Saiba mais](#explore-references)
* Arquivar um fragmento. [Saiba mais](#archive-fragments)
* Edite as marcas de um fragmento [Saiba como trabalhar com marcas unificadas](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Status dos fragmentos

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Novos status de fragmentos"
>abstract="Como os status **Rascunho** e **Ativo** foram introduzidos com a versão de junho do Journey Optimizer, todos os fragmentos criados antes desta versão têm o status “Rascunho”, mesmo se forem usados em uma jornada ou campanha. Ao fazer qualquer alteração nesses fragmentos, será necessário publicá-los para torná-los “Ativos” e propagar as alterações para as campanhas e jornadas associadas. Também é necessário criar uma nova versão da jornada/campanha e publicá-la. <br/>A publicação requer a permissão de usuário <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Fragmento de publicação</a>."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Saiba mais sobre permissões de fragmentos de conteúdo"

Os fragmentos podem ter vários status:

* **[!UICONTROL Rascunho]**: O fragmento está sendo editado e não foi aprovado.

* **[!UICONTROL Live]**: o fragmento foi aprovado e está ativo. [Saiba como publicar um fragmento](../content-management/create-fragments.md#publish)

  Quando um fragmento em tempo real está sendo editado, um ícone específico ao lado do status é exibido. Clique nesse ícone para abrir a versão de rascunho do fragmento.

* **[!UICONTROL Publicação]**: o fragmento foi aprovado e está sendo publicado.
* **[!UICONTROL Arquivado]**: o fragmento foi arquivado. [Saiba como arquivar fragmentos](#archive-fragments)

>[!CAUTION]
>
>Como os status **Rascunho** e **Ativo** foram introduzidos com a versão de junho do Journey Optimizer, todos os fragmentos criados antes desta versão têm o status “Rascunho”, mesmo se forem usados em uma jornada ou campanha. Ao fazer qualquer alteração nesses fragmentos, será necessário publicá-los para torná-los “Ativos” e propagar as alterações para as campanhas e jornadas associadas. Também é necessário criar uma nova versão da jornada/campanha e publicá-la. A publicação requer a permissão de usuário [Fragmento de Publish](../administration/ootb-product-profiles.md#content-library-manager).

## Editar fragmentos {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Atualização de fragmentos em campanhas"
>abstract="Esta campanha não será atualizada se você publicar alterações no fragmento. Ela requer que uma nova versão seja publicada para que a funcionalidade de atualização do fragmento seja compatível."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Atualização de fragmentos em jornadas"
>abstract="Essa jornada não será atualizada se você publicar as alterações no fragmento. Ela requer que uma nova versão seja publicada para que a funcionalidade de atualização do fragmento seja compatível."

Para editar um fragmento, siga as etapas abaixo.

1. Clique no fragmento desejado na lista **[!UICONTROL Fragmentos]**.

1. As propriedades do fragmento são abertas com uma visualização de seu conteúdo.

1. Se o fragmento que está sendo editado tiver o status **Ativo**, clique no botão **Modificar** para criar uma versão de rascunho do fragmento. A versão atual do fragmento continuará ativa, até que você publique a versão de rascunho.

1. Faça as alterações desejadas no fragmento. Para editar o conteúdo, clique no botão **Editar** e edite o conteúdo da mesma maneira que faria ao criar um fragmento do zero. [Saiba como criar um fragmento](#create-from-scratch)

   >[!NOTE]
   >
   >Ao editar um fragmento de expressão, você pode remover qualquer campo de personalização, mas não pode adicionar novos ao conteúdo do fragmento. Se quiser adicionar campos de personalização, duplique o fragmento para criar um novo.

   Você também pode verificar a lista de jornadas, campanhas e modelos de conteúdo em que o fragmento está sendo usado no momento selecionando a opção **Referências do Explorer**. [Saiba mais](#explore-references)

   ![](assets/fragment-edit.png)

1. Quando as alterações estiverem prontas, clique no botão **Publish** para ativar as modificações.

Ao editar um fragmento, as alterações são propagadas automaticamente para todo o conteúdo usando esse fragmento, incluindo jornadas e campanhas ativas, com exceção do conteúdo em que você interrompeu a herança do fragmento original. Saiba como interromper a herança nas seções [Adicionar fragmentos visuais aos seus emails](../email/use-visual-fragments.md#break-inheritance) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md#break-inheritance).

## Explorar referências {#explore-references}

Você pode exibir a lista de jornadas, campanhas e modelos de conteúdo que estão usando um fragmento no momento. Para fazer isso, selecione **[!UICONTROL Explorar referências]** no menu **[!UICONTROL Mais ações]** da lista de fragmentos ou na tela de propriedades do fragmento.

![](assets/fragment-explore-references.png)

Selecione uma guia para alternar entre jornadas, campanhas, modelos e fragmentos. Você pode ver o status e clicar em um nome a ser redirecionado para o item correspondente onde o fragmento é referenciado.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Se o fragmento for usado em uma jornada, campanha ou modelo que tenha um rótulo que o impeça de acessá-lo, você verá uma mensagem de alerta na parte superior da guia selecionada. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md)

## Arquivar fragmentos {#archive-fragments}

Você pode limpar a lista de fragmentos dos itens que não são mais relevantes para sua marca.

Para fazer isso, clique no botão **[!UICONTROL Mais ações]** ao lado do fragmento desejado e selecione **[!UICONTROL Arquivar]**. Ele desaparecerá da lista de fragmentos, o que impede que os usuários o usem em emails ou modelos futuros.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Se você arquivar um fragmento usado em um conteúdo, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->esse conteúdo não será afetado.

Para desarquivar um fragmento, filtre os itens **[!UICONTROL Arquivados]** e selecione **[!UICONTROL Desarquivar]** no menu **[!UICONTROL Mais ações]**. Agora ele pode ser acessado novamente na lista de fragmentos e pode ser usado em qualquer email ou modelo.

![](assets/fragment-list-unarchive.png)

## Exportar fragmentos para outra sandbox {#export}

O Journey Optimizer permite copiar um fragmento de uma sandbox para outra. Por exemplo, você pode copiar um fragmento do ambiente de sandbox do Stage para a sandbox de produção.

O processo de cópia é realizado por meio de uma **exportação e importação de pacotes** entre as sandboxes de origem e destino. Informações detalhadas sobre como exportar objetos e importá-los para uma sandbox de destino estão disponíveis nesta seção: [Copiar objetos para outra sandbox](../configuration/copy-objects-to-sandbox.md)
