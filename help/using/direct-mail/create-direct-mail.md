---
title: Criar uma mensagem de correspondência direta
description: Saiba como criar uma mensagem de correspondência direta no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: correspondência direta, mensagem, campanha
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 25e1680c54fc1cebada7c4e8e5e4d84061248528
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 10%

---

# Criar uma mensagem de correspondência direta {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Criação de correspondência direta"
>abstract="Crie mensagens de correspondência direta em campanhas programadas e crie os arquivos de extração exigidos pelos provedores de correspondência direta para enviar para seus clientes."

## Criar uma campanha de correspondência direta{#create-dm-campaign}

1. Crie uma nova campanha agendada e escolha **[!UICONTROL Correspondência direta]** como a ação.

1. Selecione o **[!UICONTROL Superfície da correspondência direta]** para usar e clique em **[!UICONTROL Criar]**. [Saiba como criar uma superfície de correspondência direta](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. No **[!UICONTROL Propriedades]** edite o da sua campanha **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

1. Para definir seu público-alvo, clique no link **[!UICONTROL Selecionar público]** e escolha entre os públicos-alvo da Adobe Experience Platform disponíveis. [Saiba mais](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >Por enquanto, a seleção de público está restrita a 3 milhões de perfis. Essa limitação pode ser removida mediante solicitação ao representante da Adobe.

1. No **[!UICONTROL Namespace de identidade]** selecione o namespace apropriado para identificar indivíduos no público-alvo escolhido. [Saiba mais](../event/about-creating.md#select-the-namespace).

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. As campanhas podem ser agendadas para uma data específica ou definidas para recorrentes em intervalos regulares. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

Agora você pode começar a configurar o arquivo de extração para enviar ao seu provedor de correspondência direta.

## Configurar o arquivo de extração {#extraction-file}

1. Na tela de configuração da campanha, clique no link **[!UICONTROL Editar conteúdo]** botão para configurar o conteúdo do arquivo de extração.

1. Ajuste as propriedades do arquivo de extração:

   1. Especifique o desejado **[!UICONTROL Nome do arquivo]** para o arquivo de extração.

   1. Como opção, ative a opção **[!UICONTROL Acrescentar carimbo de data/hora ao nome do arquivo de exportação]** opção se quiser adicionar um carimbo de data e hora automático ao nome de arquivo especificado.

   1. Às vezes, pode ser necessário adicionar informações ao início ou final do arquivo de extração. Para fazer isso, use o **[!UICONTROL Notas]** e especifique se deseja incluir a nota como cabeçalho ou rodapé.

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. Configure as colunas e as informações a serem exibidas no arquivo de extração:

   1. Clique em **[!UICONTROL Adicionar]** botão para criar uma nova coluna.

   1. A variável **[!UICONTROL Formatação]** é exibido no lado direito, permitindo que você configure a coluna selecionada. Especificar um **[!UICONTROL Rótulo]** para a coluna.

   1. No **[!UICONTROL Dados]** selecione os atributos de perfil a serem exibidos usando o [Editor de expressão](../personalization/personalization-build-expressions.md).

   1. Para classificar o arquivo de extração usando uma coluna, selecione a coluna e alterne no **[!UICONTROL Classificar por]** opção. A variável **[!UICONTROL Classificar por]** O ícone é exibido ao lado do rótulo da coluna na **[!UICONTROL Campos de dados]** seção.

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. Repita essas etapas para adicionar quantas colunas forem necessárias para o arquivo de extração. Observe que você pode adicionar até 50 colunas.

      Para alterar a posição de uma coluna, arraste-a e solte-a no local desejado na **[!UICONTROL Campo de dados]** seção. Para excluir uma coluna, selecione-a e clique no **[!UICONTROL Remover]** botão na caixa **[!UICONTROL Formatação]** painel.

Agora você pode testar sua mensagem de correspondência direta e enviá-la ao seu público-alvo. [Saiba como testar e enviar mensagens de correspondência direta](test-send-direct-mail.md)
