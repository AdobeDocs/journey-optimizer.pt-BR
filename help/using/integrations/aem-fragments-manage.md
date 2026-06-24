---
solution: Journey Optimizer
product: journey optimizer
title: Fragmentos de conteúdo do AEM
description: Saiba como gerenciar fragmentos de conteúdo do AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: ce34eb885d85c6c0f81b477e155cb81547d53e03
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Gerenciar os fragmentos de conteúdo do Adobe Experience Manager {#aem-fragments}

>[!BEGINSHADEBOX]

**Nesta página:** Gerencie fragmentos de conteúdo do AEM na lista de fragmentos de gerenciamento de conteúdo para monitorar o status e os metadados, veja onde os fragmentos são usados em jornadas e campanhas, sincronize atualizações publicadas do Experience Manager e abra fragmentos para edição sem sair do Journey Optimizer.

>[!ENDSHADEBOX]

Ao integrar o Adobe Experience Manager as a Cloud Service ou o Managed Services com o Adobe Journey Optimizer, é possível usar os Fragmentos de conteúdo do AEM no conteúdo e verificar os status dos Fragmentos sem sair do Journey Optimizer.

Ao republicar um fragmento já usado em uma Jornada ou campanha, o cronômetro de sincronização é iniciado depois que o fragmento é **publicado** no Adobe Experience Manager. Normalmente, o conteúdo atualizado está disponível no Journey Optimizer em cerca de **5 minutos** para jornadas e campanhas unitárias. Para entregas em lote, a alteração aparece no **próximo lote de processamento**. Consulte [Trabalhar com fragmentos de conteúdo do Adobe Experience Manager](aem-fragments.md). Se ocorrerem atrasos, você poderá sincronizar manualmente esse fragmento do Journey Optimizer para obter a versão publicada mais recente.

## Acessar fragmentos de conteúdo do AEM {#access-aem-fragments}

1. No menu **[!UICONTROL Gerenciamento de conteúdo]**, selecione **[!UICONTROL Fragmentos]**.

1. Abra a guia **[!UICONTROL Fragmentos do AEM]** para exibir os Fragmentos de conteúdo disponíveis no Adobe Experience Manager.

1. Na lista Fragmento, clique em ![menu avançado](assets/do-not-localize/Smock_FolderSearch_18_N.svg) para **[!UICONTROL Explorar referências]**.

   ![](assets/fragment-list-1.png)

1. Selecione um Fragmento para revisar seu status e ações disponíveis:

   * **[!UICONTROL Explore referências]**: consulte as Jornadas, Campanhas, Campanhas orquestradas e Modelos que usam o fragmento.
   * **[!UICONTROL Abrir no AEM]**: abrir o fragmento no Adobe Experience Manager para editá-lo ou republicá-lo.
   * **[!UICONTROL Sincronizar]**: extraia a última versão publicada do Adobe Experience Manager para o Journey Optimizer, por exemplo, quando o conteúdo republicado não tiver aparecido após a janela de sincronização normal. Se o controle estiver desativado, o fragmento já corresponderá à versão publicada no Experience Manager.

     ![](assets/fragment-list-2.png)

1. O menu **[!UICONTROL Detalhes]** permite revisar metadados e visualizar a carga sincronizada:

   * **[!UICONTROL Nome]**: título do fragmento de conteúdo importado do Adobe Experience Manager.
   * **[!UICONTROL Descrição]**: descrição importada do Adobe Experience Manager.
   * **[!UICONTROL Variação]**: variação publicada atualmente representada para este fragmento.
   * **[!UICONTROL Id do repositório]**: identificador do repositório para o fragmento no Adobe Experience Manager.
   * **[!UICONTROL ID do fragmento do AEM]**: identificador exclusivo do fragmento de conteúdo no Adobe Experience Manager.
   * **[!UICONTROL Marcas]**: marcas atribuídas na Adobe Experience Manager, incluindo marcas de habilitação da Journey Optimizer que determinam se o Fragmento aparece nos seletores de sua organização e sandbox. [Saiba como criar e atribuir tags](aem-fragments.md#create-tag)
   * **[!UICONTROL Visualização JSON]**: estrutura JSON somente leitura do conteúdo de fragmento que o Journey Optimizer usa.

1. Em **[!UICONTROL Explorar referências]**, use as guias para ver jornadas, campanhas, campanhas orquestradas e modelos que fazem referência ao Fragmento.

   ![](assets/fragment-list-3.png)

➡️ [Saiba mais sobre o Fragmento de Conteúdo](aem-fragments.md)


