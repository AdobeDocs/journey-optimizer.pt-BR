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
source-git-commit: 89c03a4be653b39838ef8a7c77deb6a1781004a1
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 4%

---

# Criação do conteúdo multilíngue com tradução manual {#multilingual-manual}

>[!AVAILABILITY]
>
>No momento, o conteúdo multilíngue está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.

Usando o fluxo manual, você pode traduzir facilmente seu conteúdo diretamente em seu email, notificação por push ou campanha e jornada por SMS, fornecendo opções precisas de controle e personalização para suas mensagens multilíngues. Além disso, você pode importar facilmente conteúdo multilíngue pré-existente com a opção Importar HTML.

Siga estas etapas para criar conteúdo multilíngue usando tradução manual:

1. [Crie sua localidade](#create-locale).

1. [Criar configurações de idioma](#create-language-settings).

1. [Criar um conteúdo multilíngue](#create-a-multilingual-campaign).

## Criar localidade {#create-locale}

Ao definir as configurações de idioma, conforme descrito na seção [Criar suas configurações de idioma](#language-settings) seção, se um local específico não estiver disponível para seu conteúdo multilíngue, você terá a flexibilidade de criar quantos locais novos forem necessários usando o **[!UICONTROL Tradução]** menu.

1. No **[!UICONTROL Gestão de conteúdo]** menu, acesso **[!UICONTROL Tradução]**.

1. No **[!UICONTROL Dicionário de local]** clique em **[!UICONTROL Adicionar localidade]**.

   ![](assets/locale_1.png)

1. Selecione o código de localidade na **[!UICONTROL Idioma]** e a lista associada **[!UICONTROL Região]**.

1. Clique em **[!UICONTROL Salvar]** para criar a sua localidade.

   ![](assets/locale_2.png)

## Criar configurações de idioma {#language-settings}

Nesta seção, você pode definir o idioma principal e os locais associados para gerenciar o conteúdo multilíngue. Você também pode escolher o atributo que deseja usar para pesquisar informações relacionadas ao idioma do perfil

1. No **[!UICONTROL Administração]** menu, acesso **[!UICONTROL Canal]**.

1. No **[!UICONTROL Configurações de idioma]** clique em **[!UICONTROL Criar configurações de idioma]**.

   ![](assets/multilingual-settings-1.png)

1. Digite o nome do seu **[!UICONTROL Configurações de idioma]**.

1. Selecione o **[!UICONTROL Localidades]** associado a essas configurações. É possível adicionar no máximo 50 localidades.

   Se um **[!UICONTROL Localidade]** estiver ausente, você poderá criá-lo manualmente antes **[!UICONTROL Tradução]** ou por API. Consulte [Criar uma nova localidade](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. No **[!UICONTROL Preferência de envio]** selecione o atributo que deseja pesquisar para localizar informações sobre idiomas do perfil.

   ![](assets/multilingual-settings-3.png)

1. Clique em **[!UICONTROL Editar]** ao lado do seu **[!UICONTROL Localidade]** para personalizar ainda mais e adicionar **[!UICONTROL Preferências de perfil]**.

   ![](assets/multilingual-settings-4.png)

1. Selecionar outro **[!UICONTROL Localidades]** no menu suspenso Preferências de perfil e clique em **[!UICONTROL Adicionar perfis]**.

1. Acesse o menu avançado do **[!UICONTROL Localidade]** para definir o **[!UICONTROL Localidade principal]**, ou seja, o idioma padrão se o atributo de perfil não for especificado.

   Você também pode excluir seu local nesse menu avançado.

   ![](assets/multilingual-settings-5.png)

1. Clique em **[!UICONTROL Enviar]** para criar o **[!UICONTROL Configurações de idioma]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Criar um conteúdo multilíngue {#create-multilingual-campaign}

Depois de configurar seu conteúdo multilíngue, você está pronto para criar a campanha ou jornada e personalizar o conteúdo para cada uma das localidades selecionadas.

1. Comece criando e configurando seu email, SMS ou notificação por push [campaign](../campaigns/create-campaign.md) ou [jornada](../building-journeys/journeys-message.md) de acordo com suas necessidades.

   >[!AVAILABILITY]
   >
   >Recomendamos incluir apenas um projeto de tradução por jornada.

1. Crie ou importe seu conteúdo original e personalize-o conforme necessário.

1. Após criar o conteúdo principal, clique em **[!UICONTROL Salvar]** e volte para a tela de configuração do campaign.

   ![](assets/multilingual-campaign-2.png)

1. Clique em **[!UICONTROL Adicionar idiomas]** e selecione o criado anteriormente **[!UICONTROL Configurações de idioma]**. [Saiba mais](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Acesse as configurações avançadas do **[!UICONTROL Localidades]** e selecione **[!UICONTROL Copiar principal para todos os locais]**.

   ![](assets/multilingual-campaign-4.png)

1. Agora que o conteúdo principal foi duplicado em todo o conteúdo selecionado  **[!UICONTROL Localidades]**, acesse cada local e clique em **[!UICONTROL Editar corpo do email]** para traduzir o conteúdo.

   ![](assets/multilingual-campaign-5.png)

1. Você pode optar por desativar ou ativar códigos de idiomas com o **[!UICONTROL Mais ações]** do local selecionado.

   ![](assets/multilingual-campaign-6.png)

1. Para desativar a configuração multilíngue, clique em **[!UICONTROL Adicionar idiomas]** e selecione o idioma que deseja manter como idioma local.

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
