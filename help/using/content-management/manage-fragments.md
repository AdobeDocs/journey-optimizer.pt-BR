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
source-git-commit: 09287aaa41664cc497060df9a10a7d46985e4ae4
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 15%

---

# Gerenciar fragmentos {#manage-fragments}

Para gerenciar os fragmentos, acesse a lista de fragmentos na **[!UICONTROL Gestão de conteúdo]** > **[!UICONTROL Fragmentos]** menu esquerdo.

Todos os fragmentos criados na sandbox atual - ou [do **[!UICONTROL Fragmentos]** menu](#create-fragments), utilizando o [Salvar como fragmento](#save-as-fragment) opção - são exibidas.

![](assets/fragment-list-filters.png)

Você pode filtrar fragmentos em:

* Status (Rascunho ou Ativo)
* Tipo (visual ou expressão)
* Data de criação ou modificação
* Estado (arquivado ou não)
* Tags

Você também pode optar por mostrar todos os fragmentos ou somente os itens que o usuário atual criou ou modificou.

No **[!UICONTROL Mais ações]** ao lado de cada fragmento, é possível:

* Duplique um fragmento.
* Use o **[!UICONTROL Explorar referências]** opção para ver as jornadas, campanhas ou templates onde são usados. [Saiba mais](#explore-references)
* Arquivar um fragmento. [Saiba mais](#archive-fragments)
* Editar as tags de um fragmento [Saiba como trabalhar com tags unificadas](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Status dos fragmentos

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Novos status de fragmentos"
>abstract="Como os status **Rascunho** e **Ativo** foram introduzidos com a versão de junho do Journey Optimizer, todos os fragmentos criados antes desta versão têm o status “Rascunho”, mesmo se forem usados em uma jornada ou campanha. Ao fazer qualquer alteração nesses fragmentos, será necessário publicá-los para torná-los “Ativos” e propagar as alterações para as campanhas e jornadas associadas. Também é necessário criar uma nova versão da jornada/campanha e publicá-la. A publicação requer a permissão do usuário &quot;Fragmento do Publish&quot;."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="Saiba mais sobre permissões de fragmentos de conteúdo"

>[!AVAILABILITY]
>
> Observe que os status dos fragmentos estão sendo implantados gradualmente durante vários dias após a versão de junho do Journey Optimizer. Embora alguns usuários tenham acesso imediato, outros podem enfrentar um atraso antes que ele se torne disponível em seus ambientes. Se esse aprimoramento ainda não estiver disponível em seu ambiente, observe que o fragmento não precisa ser **Ao vivo** para ser usado em suas jornadas e campanhas.

Os fragmentos podem ter vários status:

* **[!UICONTROL Rascunho]**: O fragmento está sendo editado e não foi aprovado.

* **[!UICONTROL Ao vivo]**: o fragmento foi aprovado e está ativo. [Saiba como publicar um fragmento](../content-management/create-fragments.md#publish)

  Quando um fragmento em tempo real está sendo editado, um ícone específico ao lado do status é exibido. Clique nesse ícone para abrir a versão de rascunho do fragmento.

* **[!UICONTROL Publicação]**: O fragmento foi aprovado e está sendo publicado.
* **[!UICONTROL Arquivado]**: O fragmento foi arquivado. [Saiba como arquivar fragmentos](#archive-fragments)

>[!CAUTION]
>
>Como os status **Rascunho** e **Ativo** foram introduzidos com a versão de junho do Journey Optimizer, todos os fragmentos criados antes desta versão têm o status “Rascunho”, mesmo se forem usados em uma jornada ou campanha. Ao fazer qualquer alteração nesses fragmentos, será necessário publicá-los para torná-los “Ativos” e propagar as alterações para as campanhas e jornadas associadas. Também é necessário criar uma nova versão da jornada/campanha e publicá-la. A publicação requer o [Fragmento do Publish](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager)** permissão de usuário.

## Editar fragmentos {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Atualização de fragmentos em campanhas"
>abstract="Esta campanha não será atualizada se você publicar alterações no fragmento. Ela requer que uma nova versão seja publicada, para que a funcionalidade de atualização do fragmento possa ser compatível."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Atualização de fragmentos no jornada"
>abstract="Essa jornada não será atualizada se você publicar alterações no fragmento. Ela requer que uma nova versão seja publicada, para que a funcionalidade de atualização do fragmento possa ser compatível."

Para editar um fragmento, siga as etapas abaixo.

1. Clique no fragmento desejado na guia **[!UICONTROL Fragmentos]** lista.

1. As propriedades do fragmento são abertas com uma visualização de seu conteúdo.

1. Se o fragmento que está sendo editado tiver a **Ao vivo** , clique no link **Modificar** botão para criar uma versão de rascunho do fragmento. A versão atual do fragmento continuará ativa, até que você publique a versão de rascunho.

1. Faça as alterações desejadas no fragmento. Para editar o conteúdo, clique no link **Editar** e, em seguida, edite o conteúdo da mesma maneira que faria ao criar um fragmento do zero. [Saiba como criar um fragmento](#create-from-scratch)

   >[!NOTE]
   >
   >Ao editar um fragmento de expressão, você pode remover qualquer campo de personalização, mas não pode adicionar novos ao conteúdo do fragmento. Se quiser adicionar campos de personalização, duplique o fragmento para criar um novo.

   Você também pode verificar a lista de jornadas, campanhas e modelos de conteúdo em que o fragmento está sendo usado no momento selecionando o **Referências do Explorer** opção. [Saiba mais](#explore-references)

   ![](assets/fragment-edit.png)

1. Quando as alterações estiverem prontas, clique no link **Publish** botão para ativar as modificações.

Ao editar um fragmento, as alterações são propagadas automaticamente para todo o conteúdo usando esse fragmento, incluindo jornadas e campanhas ativas, com exceção do conteúdo em que você interrompeu a herança do fragmento original. Saiba como interromper a herança no [Adicionar fragmentos visuais aos seus emails](../email/use-visual-fragments.md#break-inheritance) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md#break-inheritance) seções.

>[!AVAILABILITY]
>
>Observe que a propagação de alterações de fragmentos em jornadas e campanhas ativas está sendo distribuída gradualmente ao longo de vários dias após o lançamento do Journey Optimizer em junho. Embora alguns usuários tenham acesso imediato, outros podem enfrentar um atraso antes que ele se torne disponível em seus ambientes. Se esse aprimoramento ainda não estiver disponível em seu ambiente, suas alterações não serão propagadas para o conteúdo usado em jornadas ou campanhas ativas.

## Explorar referências {#explore-references}

Você pode exibir a lista de jornadas, campanhas e modelos de conteúdo que estão usando um fragmento no momento. Para fazer isso, selecione **[!UICONTROL Explorar referências]** na caixa **[!UICONTROL Mais ações]** na lista de fragmentos ou na tela propriedades do fragmento.

![](assets/fragment-explore-references.png)

Selecione uma guia para alternar entre jornadas, campanhas, modelos e fragmentos. Você pode ver o status e clicar em um nome a ser redirecionado para o item correspondente onde o fragmento é referenciado.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Se o fragmento for usado em uma jornada, campanha ou modelo que tenha um rótulo que o impeça de acessá-lo, você verá uma mensagem de alerta na parte superior da guia selecionada. [Saiba mais sobre o OLAC (Object Level Access Control)](../administration/object-based-access.md)

## Arquivar fragmentos {#archive-fragments}

Você pode limpar a lista de fragmentos dos itens que não são mais relevantes para sua marca.

Para fazer isso, clique no link **[!UICONTROL Mais ações]** ao lado do fragmento desejado e selecione **[!UICONTROL Arquivar]**. Ele desaparecerá da lista de fragmentos, o que impede que os usuários o usem em emails ou modelos futuros.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Se você arquivar um fragmento usado em um conteúdo, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->que o conteúdo não será afetado.

Para desarquivar um fragmento, filtre na variável **[!UICONTROL Arquivado]** itens e selecione **[!UICONTROL Desarquivar]** do **[!UICONTROL Mais ações]** menu. Agora ele pode ser acessado novamente na lista de fragmentos e pode ser usado em qualquer email ou modelo.

![](assets/fragment-list-unarchive.png)
