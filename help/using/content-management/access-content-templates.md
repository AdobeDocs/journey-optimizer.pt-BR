---
solution: Journey Optimizer
product: journey optimizer
title: Acessar e gerenciar modelos de conteúdo
description: Saiba como acessar e gerenciar modelos de conteúdo
topic: Content Management
role: User
level: Beginner
exl-id: ef6110c4-1aa6-4835-b0b0-b3c4fe0e7024
TQID: https://experienceleague.adobe.com/ForlM8q0qc7dVSLKtCdhHh7ZVEuprPYbqTLHuOUXo8I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 6c7377396eb135e310fc04dbc5946db467461e23
workflow-type: tm+mt
source-wordcount: 1018
ht-degree: 2%

---

# Acessar e gerenciar modelos de conteúdo {#access-manage-templates}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como acessar, pesquisar, organizar em pastas, editar, excluir e exportar modelos de conteúdo em sandboxes no Adobe Journey Optimizer.

>[!ENDSHADEBOX]

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

No botão **[!UICONTROL Mais ações]**, ao lado de cada modelo, você pode acessar os seguintes atalhos e ações:

* **[!UICONTROL Editar detalhes]** — Edite o nome, a descrição e as marcas do modelo.
* **[!UICONTROL Simular conteúdo]** — Visualize e teste o conteúdo do modelo.
* **[!UICONTROL Excluir]** — Exclua o modelo.

Para modelos de email, os seguintes atalhos adicionais estão disponíveis:

* **[!UICONTROL Editar linha de assunto]** — Atualize rapidamente a linha de assunto do email.
* **[!UICONTROL Editar corpo de email]** — Abra o designer de email para modificar o conteúdo do modelo.
* **[!UICONTROL Exibir prova]** — Exiba uma prova do modelo de email.
* **[!UICONTROL Enviar prova]** — Envie uma prova do modelo para os destinatários designados.
* **[!UICONTROL Relatório de spam]** — Analise o modelo em relação aos filtros de spam.
* **[!UICONTROL Renderizar email]** — Visualize como o email é renderizado em diferentes clientes de email.

![](assets/content-template-quick-launch.png)

Para editar o conteúdo completo de um modelo, clique no item desejado na lista e faça as alterações desejadas. Também é possível editar as propriedades do template de conteúdo clicando no botão de edição ao lado do nome do template.

    ![](assets/content-template-edit.png)

>[!NOTE]
>
>Quando um modelo é editado ou excluído, as campanhas ou jornadas, incluindo o conteúdo criado usando esse modelo, não são afetadas.

## Ações em massa {#bulk-actions-templates}

É possível selecionar vários modelos de uma só vez e aplicar operações em massa a todos eles. As operações disponíveis incluem adicionar itens a um pacote, movê-los para uma pasta, editar tags, gerenciar o acesso e arquivar. [Saiba mais sobre ações em massa →](../start/search-filter-categorize.md#bulk-actions)

Também é possível classificar a lista de modelos clicando na maioria dos cabeçalhos de coluna, e redimensionar colunas arrastando a borda da coluna para ajustar os dados necessários.

## [!BADGE Disponibilidade limitada]{type=Informative} exibe modelos como miniaturas {#template-thumbnails}

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

