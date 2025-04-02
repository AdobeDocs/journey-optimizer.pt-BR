---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar modelos de conteúdo
description: Saiba como acessar e gerenciar modelos de conteúdo
topic: Content Management
role: User
level: Beginner
exl-id: ef6110c4-1aa6-4835-b0b0-b3c4fe0e7024
source-git-commit: 67ebea8b1b46ee20735eee0680656e82f2839c41
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 3%

---

# Acessar e gerenciar modelos de conteúdo {#access-manage-templates}

## Acessar modelos de conteúdo {#access}

Para acessar a lista de modelos de conteúdo, selecione **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** no menu esquerdo.

![](assets/content-template-list.png)

Todos os modelos criados na sandbox atual - de uma jornada ou campanha usando a opção **[!UICONTROL Salvar como modelo]**, no menu **[!UICONTROL Modelos de conteúdo]** - são exibidos. [Saiba como criar modelos](#create-content-templates)

O painel à esquerda permite organizar modelos de conteúdo em pastas. Por padrão, todos os modelos são exibidos. Ao selecionar uma pasta, somente os modelos e as pastas incluídos na pasta selecionada são exibidos. [Saiba mais](#folders)

>[!NOTE]
>
>As pastas de modelo de conteúdo só estão disponíveis para um conjunto de organizações (Disponibilidade limitada) e serão gradualmente implantadas para mais usuários.

![](assets/content-template-list-folders.png)

Para localizar um item específico, comece digitando um nome no campo de pesquisa. Quando uma [pasta](#folders) é selecionada, a pesquisa se aplica a todos os modelos de conteúdo ou pastas no primeiro nível de hierarquia dessa pasta<!--(not nested items)-->.

Você pode classificar modelos de conteúdo por:
* Tipo
* Canal
* Data de criação ou modificação
* Marcas - [Saiba mais sobre marcas](../start/search-filter-categorize.md#tags)

Você também pode optar por exibir somente os itens que você mesmo criou ou modificou.

![](assets/content-template-list-filters.png)

## Usar pastas para gerenciar modelos de conteúdo {#folders}

>[!AVAILABILITY]
>
>As pastas de modelo de conteúdo só estão disponíveis para um conjunto de organizações (Disponibilidade limitada) e serão gradualmente implantadas para mais usuários.

Para navegar facilmente pelos modelos de conteúdo, você pode usar pastas para organizá-los com mais eficiência em uma hierarquia estruturada. Isso permite categorizar e gerenciar os itens de acordo com as necessidades da organização.

![](assets/content-template-folders.png)

1. Clique no botão **[!UICONTROL Todos os modelos de conteúdo]** para exibir todos os itens criados anteriormente sem o agrupamento de pastas.

1. Clique na pasta **[!UICONTROL Raiz]** para exibir todas as pastas criadas.

   >[!NOTE]
   >
   >Se você ainda não criou pastas, todos os modelos de conteúdo são exibidos.

1. Clique em qualquer pasta dentro da pasta **[!UICONTROL Raiz]** para exibir seu conteúdo.

1. Ao clicar na pasta **[!UICONTROL Raiz]** ou em qualquer outra pasta, o botão **[!DNL Create folder]** é exibido. Selecione-o.

   ![](assets/content-template-create-folder.png)

1. Digite um nome para a nova pasta e clique em **[!UICONTROL Salvar]**. A nova pasta é exibida na parte superior da lista de modelos de conteúdo dentro da pasta **[!UICONTROL Raiz]** ou dentro da pasta selecionada no momento.

1. Clique no botão **[!UICONTROL Mais ações]** para renomear ou excluir a pasta.

   ![](assets/content-template-folder-more-actions.png)

1. Usando o botão **[!UICONTROL Mais ações]**, você também pode mover o modelo de conteúdo para outra pasta existente.

   ![](assets/content-template-folder-moved.png)

1. Agora é possível navegar até a pasta que acabou de criar. Cada novo modelo de conteúdo que você [cria](create-content-templates.md) daqui é salvo na pasta atual.

   ![](assets/content-template-folder-create.png)

## Editar e excluir modelos de conteúdo {#edit}

* Para editar o conteúdo de um modelo, clique no item desejado na lista e faça as alterações desejadas. Também é possível editar as propriedades do template de conteúdo clicando no botão de edição ao lado do nome do template.

  ![](assets/content-template-edit.png)

* Para excluir um modelo, selecione o botão **[!UICONTROL Mais ações]** ao lado do modelo desejado e selecione **[!UICONTROL Excluir]**.

  ![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Quando um modelo é editado ou excluído, as campanhas ou jornadas, incluindo o conteúdo criado usando esse modelo, não são afetadas.

## [!BADGE Disponibilidade limitada]{type=Informative} Exibe modelos como miniaturas {#template-thumbnails}

Selecione o modo de **[!UICONTROL exibição de grade]** para exibir cada modelo como uma miniatura.

>[!AVAILABILITY]
>
Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno grupo de clientes.

![](assets/content-template-grid-view.png)

>[!NOTE]
>
Atualmente, as miniaturas adequadas só podem ser geradas para HTML email modelos de conteúdo.

Ao atualizar um conteúdo, talvez seja necessário aguardar alguns segundos antes que as alterações sejam refletidas na miniatura.

## Exportar modelos de conteúdo para outra sandbox {#export}

O Journey Optimizer permite copiar um modelo de conteúdo de uma sandbox para outra. Por exemplo, você pode copiar um modelo do seu ambiente de sandbox de Preparo para a sua sandbox de Produção.

O processo de cópia é realizado por meio de uma **exportação e importação de pacotes** entre as sandboxes de origem e destino. Informações detalhadas sobre como exportar objetos e importá-los para uma sandbox de destino estão disponíveis nesta seção: [Copiar objetos para outra sandbox](../configuration/copy-objects-to-sandbox.md)
