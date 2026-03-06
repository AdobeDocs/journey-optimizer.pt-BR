---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar modelos de conteúdo
description: Saiba como acessar e gerenciar modelos de conteúdo
topic: Content Management
role: User
level: Beginner
exl-id: ef6110c4-1aa6-4835-b0b0-b3c4fe0e7024
source-git-commit: 9fc43f2e17c256d33f73f21b6b30c4b593087a28
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 3%

---

# Acessar e gerenciar modelos de conteúdo {#access-manage-templates}

## Pré-requisitos {#prerequisites}

Para acessar e gerenciar modelos de conteúdo, verifique o seguinte:

* **Permissão de Modelos de Conteúdo** — Sua função deve incluir a permissão **[!UICONTROL Gerenciar modelos de conteúdo]** (no recurso **Gerenciamento de Conteúdo**). Sem ele, o menu **Modelos de conteúdo** não fica visível na navegação à esquerda. [Saiba como gerenciar permissões](../administration/permissions.md)
* **Escopo da sandbox** — os modelos de conteúdo são específicos da sandbox. Os modelos criados em uma sandbox não estão disponíveis em outra. Verifique se você está na sandbox correta antes de pesquisar um modelo.
* **Modelos do HTML (obsoletos)** — A partir de março de 2025, os modelos de conteúdo do tipo HTML serão descontinuados. Os modelos do HTML existentes permanecem acessíveis, mas não é possível criar novos.

## Acessar modelos de conteúdo {#access}

Para acessar a lista de modelos de conteúdo, selecione **[!UICONTROL Content Management]** > **[!UICONTROL Content Templates]** no menu esquerdo.

![](assets/content-template-list.png)

Todos os modelos criados na sandbox atual—de uma jornada ou campanha usando a opção **[!UICONTROL Salvar como modelo]**, ou do menu **[!UICONTROL Modelos de conteúdo]**—são exibidos. [Saiba como criar modelos](#create-content-templates)

O painel à esquerda permite organizar modelos de conteúdo em pastas. Por padrão, todos os modelos são exibidos. Ao selecionar uma pasta, somente os modelos e as pastas incluídos na pasta selecionada são exibidos. [Saiba mais](#folders)

![](assets/content-template-list-folders.png)

Para localizar um item específico, comece digitando um nome no campo de pesquisa. Quando uma [pasta](#folders) é selecionada, a pesquisa se aplica a todos os modelos de conteúdo ou pastas no primeiro nível de hierarquia dessa pasta<!--(not nested items)-->.

Você pode classificar modelos de conteúdo por:

* Tipo
* Canal
* Data de criação ou modificação
* Marcas - [Saiba mais sobre marcas](../start/search-filter-categorize.md#tags)

Você também pode optar por exibir somente os itens criados ou modificados por você.

![](assets/content-template-list-filters.png)

>[!NOTE]
>
>A partir de março de 2025, os modelos de conteúdo do tipo HTML serão descontinuados. Você ainda pode acessar modelos de conteúdo HTML existentes criados anteriormente no [!DNL Journey Optimizer].

## Usar pastas para gerenciar modelos de conteúdo {#folders}

Para navegar facilmente pelos modelos de conteúdo, use pastas para organizá-los com mais eficiência em uma hierarquia estruturada. Isso permite categorizar e gerenciar os itens de acordo com as necessidades da organização.

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

1. Navegue até a pasta que acabou de criar. Cada novo modelo de conteúdo que você [cria](create-content-templates.md) daqui é salvo na pasta atual.

   ![](assets/content-template-folder-create.png)

## Editar e excluir modelos de conteúdo {#edit}

* Para editar o conteúdo de um modelo, clique no item desejado na lista e faça as alterações desejadas. Também é possível editar as propriedades do template de conteúdo clicando no botão de edição ao lado do nome do template.

  ![](assets/content-template-edit.png)

* Para excluir um modelo, selecione o botão **[!UICONTROL Mais ações]** ao lado do modelo desejado e selecione **[!UICONTROL Excluir]**.

  ![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Quando um modelo é editado ou excluído, as campanhas ou jornadas, incluindo o conteúdo criado usando esse modelo, não são afetadas.

## [!BADGE Disponibilidade limitada]{type=Informative} Exibir modelos como miniaturas {#template-thumbnails}

Selecione o modo de **[!UICONTROL exibição de grade]** para exibir cada modelo como uma miniatura.

>[!AVAILABILITY]
>
>Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno grupo de clientes.

![](assets/content-template-grid-view.png)

>[!NOTE]
>
>Miniaturas apropriadas só podem ser geradas para modelos de conteúdo de email do tipo HTML.

Ao atualizar o conteúdo, aguarde alguns segundos para que as alterações sejam refletidas na miniatura.

## Solução de problemas {#troubleshooting}

+++Não consigo ver o menu Modelos de conteúdo na navegação à esquerda

Sua função não tem a permissão **Gerenciar modelos de conteúdo**. Peça ao administrador para adicionar o recurso **Gerenciamento de conteúdo** com a permissão **Gerenciar modelos de conteúdo** à sua função. [Saiba mais](../administration/permissions.md)

+++

+++Um modelo que criei não é exibido na lista

Verifique se você está na sandbox correta — os modelos são específicos da sandbox. Verifique também se uma pasta está selecionada no painel esquerdo; quando uma pasta é selecionada, somente os modelos dentro dessa pasta são exibidos. Clique em **[!UICONTROL Todos os modelos de conteúdo]** para exibir todos os modelos independentemente da pasta.

+++

+++Editei um template, mas meu conteúdo de campanha ou jornada não foi atualizado

A edição ou exclusão de um template não atualiza retroativamente campanhas ou jornadas que foram criadas com ele. O conteúdo é copiado no momento do uso. Para atualizar o conteúdo existente, edite a campanha ou a jornada diretamente.

+++

## Exportar modelos de conteúdo para outra sandbox {#export}

O Journey Optimizer permite copiar um modelo de conteúdo de uma sandbox para outra. Por exemplo, você pode copiar um modelo do seu ambiente de sandbox de Preparo para a sua sandbox de Produção.

O processo de cópia é realizado por meio de uma **exportação e importação de pacotes** entre as sandboxes de origem e destino. Informações detalhadas sobre como exportar objetos e importá-los para uma sandbox de destino estão disponíveis nesta seção: [Copiar objetos para outra sandbox](../configuration/copy-objects-to-sandbox.md)

