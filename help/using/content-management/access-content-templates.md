---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar modelos de conteúdo
description: Saiba como acessar e gerenciar modelos de conteúdo
topic: Content Management
role: User
level: Beginner
exl-id: ef6110c4-1aa6-4835-b0b0-b3c4fe0e7024
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 5%

---

# Acessar e gerenciar modelos de conteúdo {#access-manage-templates}

## Acessar modelos de conteúdo {#access}

Para acessar a lista de modelos de conteúdo, selecione **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** no menu esquerdo.

![](assets/content-template-list.png)

Todos os modelos criados na sandbox atual - de uma jornada ou campanha usando a opção **[!UICONTROL Salvar como modelo]**, no menu **[!UICONTROL Modelos de conteúdo]** - são exibidos. [Saiba como criar modelos](#create-content-templates)

Você pode classificar modelos de conteúdo por:
* Tipo
* Canal
* Data de criação ou modificação
* Marcas - [Saiba mais sobre marcas](../start/search-filter-categorize.md#tags)

Você também pode optar por exibir somente os itens que você mesmo criou ou modificou.

![](assets/content-template-list-filters.png)

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
