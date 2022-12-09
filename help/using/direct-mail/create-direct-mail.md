---
title: Criar uma mensagem de correspondência direta
description: Saiba como criar uma mensagem de correspondência direta no Journey Otimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Criar uma mensagem de correspondência direta {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Criação de correspondência direta"
>abstract="Crie mensagens de mala direta em campanhas programadas e crie os arquivos de extração exigidos pelos provedores de mala direta para enviar mala para seus clientes."

A mala direta é um canal offline que permite personalizar e gerar os arquivos de extração exigidos por provedores de mala direta para enviar mala para seus clientes.

Quando você cria uma correspondência direta, o Journey Otimizer gera um arquivo incluindo todos os perfis direcionados e os dados escolhidos (endereço postal, atributos de perfil, por exemplo). Seu provedor de correspondência direta poderá recuperar esse arquivo e cuidar do envio real.

As mensagens de correspondência direta só podem ser criadas no contexto de campanhas programadas. Eles não estão disponíveis para uso em campanhas acionadas por API ou em jornadas.

>[!IMPORTANT]
>
>Antes de enviar uma mensagem de mala direta, verifique se você configurou:
>
>1. A [configuração de roteamento de arquivos](../direct-mail/direct-mail-configuration.md#file-routing-configuration) que especifica o servidor onde o arquivo de extração deve ser carregado e armazenado,
>1. A [superfície da mensagem de correspondência direta](../direct-mail/direct-mail-configuration.md#direct-mail-surface) que referenciará a configuração de roteamento de arquivos.


## Criar a mensagem de mala direta {#create}

As etapas para criar e enviar uma mensagem de mala direta são as seguintes:

1. Crie uma nova campanha agendada, selecione **[!UICONTROL Direct mail]** como sua ação e escolha a superfície do canal a ser usada. [Saiba como criar uma superfície de correspondência direta](../direct-mail/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. Clique em **[!UICONTROL Create]** em seguida, defina as informações básicas sobre sua campanha (nome, descrição). [Saiba como configurar uma campanha](../campaigns/create-campaign.md)

   ![](assets/direct-mail-edit.png)

1. Clique no botão **[!UICONTROL Edit content]** para configurar o arquivo de extração a ser enviado ao seu provedor de correspondência direta.

1. Defina o nome do arquivo de extração no **[!UICONTROL Filename]** campo.

   Às vezes, pode ser necessário adicionar informações no início ou no final do arquivo de extração. Para fazer isso, use o **[!UICONTROL Notes]** em seguida, especifique se deseja incluir a nota como cabeçalho ou rodapé.

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. Use a área à esquerda para definir as informações a serem exibidas como colunas no arquivo de extração:

   1. Clique no botão **[!UICONTROL Add]** para adicionar uma nova coluna e, em seguida, selecione-a na lista.

   1. No **[!UICONTROL Formatting]** , especifique um rótulo para a coluna e defina os atributos de perfil a serem exibidos usando o [Editor de expressão](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. Para classificar o arquivo de extração usando a coluna selecionada, alterne a **[!UICONTROL Sort by]** ativada. O **[!UICONTROL Sort By]** será exibido ao lado do rótulo da coluna na estrutura do arquivo.

1. Repita essas etapas para adicionar quantas colunas forem necessárias para criar seu arquivo de extração. Observe que é possível adicionar até 50 colunas.

   ![](assets/direct-mail-complete.png)

   É possível excluir uma coluna a qualquer momento selecionando-a e clicando no botão **[!UICONTROL Remove]** do botão **[!UICONTROL Formatting]** seção.

1. Após definir o conteúdo da correspondência direta, conclua a configuração da campanha.

   Quando a campanha for iniciada, o arquivo de extração será gerado e exportado automaticamente para o servidor especificado em [configuração de roteamento de arquivos](../direct-mail/direct-mail-configuration.md).
