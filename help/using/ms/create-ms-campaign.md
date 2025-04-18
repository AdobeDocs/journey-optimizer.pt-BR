---
solution: Journey Optimizer
product: journey optimizer
title: Criar campanhas orquestradas com o Journey Optimizer
description: Saiba como criar uma campanha orquestrada com o Adobe Journey Optimizer
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 2%

---

# Criar uma campanha orquestrada {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campanhas orquestradas"
>abstract="A guia **várias etapas** lista todas as campanhas orquestradas. Clique no nome de uma campanha orquestrada para editá-la. Use o botão **Criar campanha orquestrada** para adicionar uma nova campanha orquestrada."

## Pré-requisitos

### Permissões

### Configurações

Visão geral de novas configurações de administração> esquemas, campos de execução e política de mesclagem. [Saiba mais](ms-schemas.md)


## Etapas de criação

Para criar uma campanha orquestrada, siga estas etapas:

1. Para criar uma **campanha orquestrada**, navegue até o menu **Campanhas**.

1. Clique no botão **[!UICONTROL Criar campanha orquestrada]**, no canto superior direito da tela.

1. Na caixa de diálogo **Propriedades** da campanha orquestrada, selecione o modelo a ser usado para criar a campanha orquestrada (você também pode usar o modelo interno padrão). [Saiba mais sobre modelos de campanha orquestradas](#campaign-templates).

1. Insira um rótulo para a campanha orquestrada. Além disso, recomendamos que você adicione uma descrição à sua campanha orquestrada, no campo dedicado da seção **[!UICONTROL Opções adicionais]** da tela.

1. Expanda a seção **[!UICONTROL Opções adicionais]** para definir mais configurações para a campanha orquestrada.

1. Clique no botão **[!UICONTROL Criar campanha orquestrada]** para confirmar a criação da campanha orquestrada.

Sua campanha orquestrada agora está criada e disponível na lista de workflows. Agora é possível acessar a tela visual e começar a adicionar, configurar e orquestrar as tarefas que serão executadas. [Saiba como organizar atividades de campanha orquestradas](orchestrate-activities.md).

## Trabalhar com modelos de campanha orquestradas {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modelos de campanha orquestradas"
>abstract="Os templates de campanha orquestrados contêm configurações e atividades pré-configuradas que podem ser reutilizadas para criar uma nova campanha orquestrada."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Propriedades da campanha orquestrada"
>abstract="Os templates de campanha orquestrados contêm configurações e atividades predefinidas que podem ser reutilizadas para criar novas campanhas orquestradas. Nesta tela, insira o rótulo do template de campanha orquestrada e defina as configurações, como o nome interno, a pasta e as pastas de execução, o fuso horário e o grupo supervisor."

Os templates de campanha orquestrados contêm configurações e atividades predefinidas que podem ser reutilizadas para criar novas campanhas orquestradas. Você pode selecionar o template da sua campanha orquestrada nas propriedades da campanha orquestrada, ao criar uma campanha orquestrada. Um template vazio é fornecido por padrão.

Você pode criar um modelo a partir de uma campanha orquestrada existente ou criar um novo modelo do zero. Ambos os métodos são detalhados abaixo.

>[!BEGINTABS]

>[!TAB Criar um modelo a partir de uma campanha orquestrada existente]

Para criar um template de campanha orquestrada a partir de uma campanha orquestrada existente, siga estas etapas:

1. Abra o menu **Campanha** e navegue até a campanha orquestrada para salvar como um modelo.
1. Clique nos três pontos à direita do nome da campanha orquestrada e escolha **Copiar como modelo**.
1. Na janela pop-up, confirme a criação do template.
1. Na tela do template de campanha orquestrada, verifique, adicione e configure as atividades conforme necessário.
1. Navegue até as configurações, no botão **Configurações**, para alterar o nome do modelo de campanha orquestrada e insira uma descrição.
1. Selecione a **pasta** e a **pasta de execução** do modelo. A pasta é o local onde o template de campanha orquestrada é salvo. A pasta de execução é a pasta onde as campanhas orquestradas criadas com base nesse template são salvas.
1. Salve as alterações.

O template de campanha orquestrada agora está disponível na lista de templates. Você pode criar uma campanha orquestrada com base nesse template. Essa campanha orquestrada será pré-configurada com as configurações e atividades definidas no template.


>[!TAB Criar um modelo do zero]


Para criar um template de campanha orquestrado do zero, siga estas etapas:

1. Abra o menu **Campanha** e navegue até a guia **Modelos**. Você pode ver a lista de templates de campanha orquestrada disponíveis.
1. Clique no botão **[!UICONTROL Criar modelo]** no canto superior direito da tela.
1. Insira o rótulo e abra as opções adicionais para inserir uma descrição do template de campanha orquestrada.
1. Selecione a pasta e a pasta de execução do modelo. A pasta é o local onde o template de campanha orquestrada é salvo. A pasta de execução é a pasta onde as campanhas orquestradas criadas com base nesse template são salvas.
1. Clique no botão **Criar** para confirmar suas configurações.
1. Na tela do template de campanha orquestrada, adicione e configure as atividades conforme necessário.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Salve as alterações.

O template de campanha orquestrada agora está disponível na lista de templates. Você pode criar uma campanha orquestrada com base nesse template. Essa campanha orquestrada será pré-configurada com as configurações e atividades definidas no template.

>[!ENDTABS]
