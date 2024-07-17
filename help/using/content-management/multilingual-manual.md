---
solution: Journey Optimizer
product: journey optimizer
title: Criação do conteúdo multilíngue com tradução manual
description: Saiba como criar conteúdo multilíngue com tradução manual no Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introdução, iniciar, conteúdo, experimento
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 59dee15d2952438a074db57a94b3d896b38cd4f3
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 6%

---

# Criação do conteúdo multilíngue com tradução manual {#multilingual-manual}

>[!AVAILABILITY]
>
>No momento, o conteúdo multilíngue está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.

Usando o fluxo manual, você pode traduzir facilmente seu conteúdo diretamente em seu email, notificação por push ou campanha e jornada por SMS, fornecendo opções precisas de controle e personalização para suas mensagens multilíngues. Além disso, você pode importar facilmente conteúdo multilíngue pré-existente com a opção Importar HTML.

Siga estas etapas para criar conteúdo multilíngue usando tradução manual:

1. [Crie sua localidade](#create-locale).

1. [Criar configurações de idioma](#create-language-settings).

1. [Criar um conteúdo multilíngue](#create-a-multilingual-campaign).

## Criar localidade {#create-locale}

Ao definir as configurações de idioma, conforme descrito na seção [Criar configurações de idioma](#language-settings), se uma localidade específica não estiver disponível para o seu conteúdo multilíngue, você terá a flexibilidade de criar quantas novas localidades forem necessárias usando o menu **[!UICONTROL Tradução]**.

1. No menu **[!UICONTROL Gestão de conteúdo]**, acesse **[!UICONTROL Tradução]**.

1. Na guia **[!UICONTROL Dicionário de localidade]**, clique em **[!UICONTROL Adicionar localidade]**.

   ![](assets/locale_1.png)

1. Selecione o código de localidade na lista **[!UICONTROL Idioma]** e a **[!UICONTROL Região]** associada.

1. Clique em **[!UICONTROL Salvar]** para criar sua localidade.

   ![](assets/locale_2.png)

## Criar configurações de idioma {#language-settings}

Nesta seção, você pode definir o idioma principal e os locais associados para gerenciar o conteúdo multilíngue. Você também pode escolher o atributo que deseja usar para pesquisar informações relacionadas ao idioma do perfil

1. No menu **[!UICONTROL Administração]**, acesse **[!UICONTROL Canal]**.

1. No menu **[!UICONTROL Configurações de idioma]**, clique em **[!UICONTROL Criar configurações de idioma]**.

   ![](assets/multilingual-settings-1.png)

1. Digite o nome das **[!UICONTROL Configurações de idioma]**.

1. Selecione as **[!UICONTROL Localidades]** associadas a estas configurações. É possível adicionar no máximo 50 localidades.

   Se uma **[!UICONTROL Localidade]** estiver ausente, você poderá criá-la manualmente com antecedência a partir do menu **[!UICONTROL Tradução]** ou por API. Consulte [Criar uma nova Localidade](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. No menu **[!UICONTROL Preferência de envio]**, selecione o atributo que você deseja pesquisar para encontrar informações sobre idiomas de perfil.

   ![](assets/multilingual-settings-3.png)

1. Clique em **[!UICONTROL Editar]** ao lado da **[!UICONTROL Localidade]** para personalizá-la ainda mais e adicionar **[!UICONTROL Preferências de perfil]**.

   ![](assets/multilingual-settings-4.png)

1. Selecione outras **[!UICONTROL Localidades]** no menu suspenso de Preferências de perfil e clique em **[!UICONTROL Adicionar perfis]**.

1. Acesse o menu avançado da **[!UICONTROL Localidade]** para definir sua **[!UICONTROL Localidade primária]**, ou seja, o idioma padrão se o atributo de perfil não for especificado.

   Você também pode excluir seu local nesse menu avançado.

   ![](assets/multilingual-settings-5.png)

1. Clique em **[!UICONTROL Enviar]** para criar suas **[!UICONTROL configurações de idioma]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Criar um conteúdo multilíngue {#create-multilingual-campaign}

Depois de configurar seu conteúdo multilíngue, você está pronto para criar a campanha ou jornada e personalizar o conteúdo para cada uma das localidades selecionadas.

1. Comece criando e configurando sua [campanha](../campaigns/create-campaign.md) ou [jornada](../building-journeys/journeys-message.md) de email, SMS ou notificação por push de acordo com suas necessidades.

   >[!AVAILABILITY]
   >
   >Recomendamos incluir apenas um projeto de tradução por jornada.

1. Crie ou importe seu conteúdo original e personalize-o conforme necessário.

1. Depois que o conteúdo principal for criado, clique em **[!UICONTROL Salvar]** e volte para a tela de configuração da campanha.

   ![](assets/multilingual-campaign-2.png)

1. Clique em **[!UICONTROL Adicionar idiomas]** e selecione as **[!UICONTROL configurações de idioma]** criadas anteriormente. [Saiba mais](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Acesse as configurações avançadas do menu **[!UICONTROL Localidades]** e selecione **[!UICONTROL Copiar principal para todas as localidades]**.

   ![](assets/multilingual-campaign-4.png)

1. Agora que o conteúdo principal está duplicado em todas as **[!UICONTROL Localidades]** selecionadas, acesse cada localidade e clique em **[!UICONTROL Editar corpo de email]** para traduzir o conteúdo.

   ![](assets/multilingual-campaign-5.png)

1. Você pode optar por desabilitar ou habilitar localidades com o menu **[!UICONTROL Mais ação]** da Localidade selecionada.

   ![](assets/multilingual-campaign-6.png)

1. Para desativar sua configuração Multilíngue, clique em **[!UICONTROL Adicionar idiomas]** e selecione o idioma que deseja manter como idioma local.

   ![](assets/multilingual-campaign-7.png)

1. Clique em **[!UICONTROL Revisar para ativar]** para exibir um resumo da campanha.

   O resumo permite modificar a campanha, se necessário, e verificar se algum parâmetro está incorreto ou ausente.

1. Navegue pelo conteúdo multilíngue para ver a renderização em cada idioma.

   ![](assets/multilingual-campaign-8.png)

Agora você pode ativar sua campanha ou jornada. Depois de enviado, você pode medir o impacto da sua jornada ou campanha multilíngue nos relatórios.

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
