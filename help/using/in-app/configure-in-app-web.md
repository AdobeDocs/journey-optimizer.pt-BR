---
title: Criar uma mensagem no aplicativo da Web no Journey Optimizer
description: Saiba como criar uma mensagem no aplicativo da Web no Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: no aplicativo, mensagem, criação, iniciar
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 2%

---


# Configurar o canal da Web no aplicativo {#configure-in-app-web}

## Pré-requisitos {#prerequisites}

* Verifique se você está usando a versão mais recente para o seu **Adobe Experience Platform Web SDK** extensão.

* Instale o **Adobe Experience Platform Web SDK** extensão no seu **Propriedades da tag** e habilite o **Armazenamento de personalização** opção.

  Essa configuração é essencial para armazenar históricos de eventos no cliente, um pré-requisito para a implementação de Regras de frequência no construtor de regras. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Configurar regra Enviar dados para plataforma {#configure-sent-data-trigger}

1. Acessar o **Coleta de dados do Adobe Experience Platform** e navegue até **Propriedades da tag** configurado com o **Adobe Experience Platform Web SDK** extensão.

1. No **Criação** selecione **Regras** depois **Criar nova regra** ou **Adicionar regra**.

   ![](assets/configure_web_inapp_2.png)

1. No **Eventos** clique em **Adicionar** e configure-a da seguinte maneira:

   * **Extensão**: Principal

   * **Tipo de evento**: Biblioteca carregada (início da página).

   ![](assets/configure_web_inapp_3.png)

1. Clique em **Manter alterações** para salvar a configuração do Evento.

1. No **Ações** clique em **Adicionar** e configure-a da seguinte maneira:

   * **Extensão**: Adobe Experience Platform Web SDK

   * **Tipo de ação**: Enviar evento

   ![](assets/configure_web_inapp_4.png)

1. No **Personalização** seção do seu **Ação** digite, ative a opção **Renderizar decisões de personalização visual** opção.

   ![](assets/configure_web_inapp_5.png)

1. No **Contexto de decisão** defina o **Chave** e **Valor** pares que determinam qual experiência fornecer.

   ![](assets/configure_web_inapp_6.png)

1. Salve seu **Ação** configuração clicando em **Manter alterações**.

1. Navegue até a **Fluxo de publicação** menu. Criar um novo **Biblioteca** ou selecione um existente **Biblioteca** e adicione seu recém-criado **Regra** a ele. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Do seu **Biblioteca**, selecione **Salvar e criar no desenvolvimento**.

   ![](assets/configure_web_inapp_7.png)

## Configurar regra manual {#configure-manual-trigger}

1. Acessar o **Coleta de dados do Adobe Experience Platform** e navegue até **Propriedades da tag** configurado com o **Adobe Experience Platform Web SDK** extensão.

1. No **Criação** selecione **Regras** depois **Criar nova regra** ou **Adicionar regra**.

   ![](assets/configure_web_inapp_8.png)

1. No **Eventos** clique em **Adicionar** e configure-a da seguinte maneira:

   * **Extensão**: Principal

   * **Tipo de evento**: Clique

   ![](assets/configure_web_inapp_9.png)

1. No **Clique em configuração**, defina o **Seletor** que serão avaliados.

   ![](assets/configure_web_inapp_10.png)

1. Clique em **Manter alterações** para salvar o **Evento** configuração.

1. No **Ações** clique em **Adicionar** e configure-a da seguinte maneira:

   * **Extensão**: Adobe Experience Platform Web SDK

   * **Tipo de ação**: Avaliar conjuntos de regras

   ![](assets/configure_web_inapp_11.png)

1. No **Avaliar ação de conjuntos de regras** seção do seu **Ação** digite, ative a opção **Renderizar decisões de personalização visual** opção.

   ![](assets/configure_web_inapp_13.png)

1. No **Contexto de decisão** defina o **Chave** e **Valor** pares que determinam qual experiência fornecer.

1. Acesse o **Fluxo de publicação** , crie um novo **Biblioteca** ou selecione um existente **Biblioteca** e adicione seu recém-criado **Regra**. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Do seu **Biblioteca**, selecione **Salvar e criar no desenvolvimento**.

   ![](assets/configure_web_inapp_14.png)

