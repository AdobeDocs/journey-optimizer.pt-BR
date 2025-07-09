---
title: Enviar mensagens de correspondência direta com o jornada
description: Saiba como criar e enviar mensagens de correspondência direta com o jornada.
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
robots: noindex
googlebot: noindex
keywords: correspondência direta, mensagem, campanha
exl-id: 44886355-ee3a-4323-899a-35d967487924
source-git-commit: ca6e2834f92585094d3316e9259e3370cfad22fc
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 19%

---

# Enviar mensagens de correspondência direta com o jornada {#direct-mail-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="Atividade de término"
>abstract="Correspondência direta é um canal offline que permite personalizar e gerar os arquivos de extração exigidos por provedores de correspondência direta de terceiros para o envio a clientes."

Correspondência direta é um canal offline que permite personalizar e gerar os arquivos de extração exigidos por provedores de correspondência direta de terceiros para o envio a clientes.

Ao criar uma mensagem de correspondência direta, o [!DNL Journey Optimizer] gera automaticamente um arquivo contendo todos os perfis direcionados e dados selecionados, como endereços postais e atributos de perfil. Esse arquivo é enviado ao servidor de sua escolha para que possa ser acessado pelo provedor de correspondência direta de terceiros escolhido, o qual realizará o processo de envio para você.

Você precisa trabalhar com o provedor de correspondência direta de terceiros escolhido para obter os consentimentos necessários de seus clientes, se aplicável, para que seus clientes possam receber emails. Seu uso dos serviços de mala direta está sujeito a termos e condições adicionais do provedor de correspondência direta de terceiros aplicável. A Adobe não controla e não se responsabiliza pelo uso de produtos de terceiros. Para qualquer problema ou solicitação de assistência relacionada ao correio de sua mensagem de correspondência direta, entre em contato com o provedor de correspondência direta de terceiros escolhido.

>[!NOTE]
>
>Esta página detalha o processo de criação e envio de mensagens de correspondência direta com o jornada. Para obter mais informações sobre o canal de correspondência direta e como criar campanhas de correspondência direta, consulte esta seção: [Introdução à correspondência direta](../direct-mail/get-started-direct-mail.md).

## Criar uma configuração de roteamento de arquivo

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_frequency"
>title="Escolha a região do AWS"
>abstract="Se a configuração de roteamento de arquivos for enviada usando o jornada, você poderá especificar a frequência com que o arquivo será enviado ao servidor."

Antes de criar uma mensagem de mala direta, verifique se você configurou um roteamento de arquivo que especifica o servidor onde o arquivo de extração deve ser carregado e armazenado. Para fazer isso, siga estes passos:

1. Acesse o menu **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configurações de correspondência direta]** > **[!UICONTROL Roteamento de arquivos]** e clique em **[!UICONTROL Criar configuração de roteamento de arquivos]**.

1. Defina as propriedades de configuração de roteamento de arquivos, como o nome e o tipo de servidor a ser usado. Informações detalhadas sobre como definir uma configuração de roteamento de arquivo estão disponíveis na seção [Configuração de correspondência direta](../direct-mail/direct-mail-configuration.md#file-routing-configuration).

   Se a configuração de roteamento de arquivos for enviada usando o jornada, você poderá especificar a frequência com que o arquivo será enviado ao servidor.

   ![](assets/file-routing-journey.png)

1. Clique em **[!UICONTROL Enviar]** para confirmar a criação da configuração de roteamento de arquivo. A configuração foi criada com o status **[!UICONTROL Ativo]**. Agora ele está pronto para ser referenciado em uma configuração de correspondência direta.

## Criar uma configuração de correspondência direta {#direct-mail-surface}

Uma configuração de correspondência direta contém as configurações para a formatação do arquivo que contém os dados do público-alvo e será usada pelo provedor de email. Você também deve definir para onde o arquivo será exportado selecionando a configuração de roteamento do arquivo. Informações detalhadas sobre como criar uma configuração de correspondência direta estão disponíveis na seção [Configuração de correspondência direta](../direct-mail/direct-mail-configuration.md#file-routing-configuration).

Quando a configuração de correspondência direta estiver pronta, você poderá adicionar uma ação de correspondência direta na jornada.

## Adicione uma ação de Correspondência direta à jornada

Para adicionar uma ação de correspondência direta em uma jornada, siga estas etapas:

1. Abra a jornada e arraste e solte uma atividade de **[!UICONTROL Correspondência direta]** da seção **Ações** da paleta.

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a configuração de mensagem a ser usada. O campo **[!UICONTROL configuração]** é preenchido previamente, por padrão, com a última configuração usada para esse canal pelo usuário. Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

1. Configure o arquivo de extração para enviar ao seu provedor de correspondência direta. Para fazer isso, clique no botão **[!UICONTROL Editar conteúdo]**.

   ![](assets/direct-mail-add-journey.png)

1. Ajuste as propriedades do arquivo de extração, como o nome do arquivo, ou as colunas a serem exibidas. Para obter mais informações sobre como configurar as propriedades do arquivo de extração, consulte esta seção: [Criar uma mensagem de correspondência direta](../direct-mail/create-direct-mail.md#extraction-file).

   ![](assets/direct-mail-journey-content.png)

1. Depois que o conteúdo do arquivo de extração for definido, você poderá usar perfis de teste para visualizá-lo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

   Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste para verificar como é a renderização do arquivo de extração usando os dados do perfil de teste. Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

Quando o arquivo de extração estiver pronto, conclua a configuração da [jornada](../building-journeys/journey-gs.md) para enviá-lo.
