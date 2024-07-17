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

* Verifique se você está usando a versão mais recente da extensão **Adobe Experience Platform Web SDK**.

* Instale a extensão **Adobe Experience Platform Web SDK** nas **Propriedades da marca** e habilite a opção **Armazenamento do Personalization**.

  Essa configuração é essencial para armazenar históricos de eventos no cliente, um pré-requisito para a implementação de Regras de frequência no construtor de regras. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## Configurar regra Enviar dados para plataforma {#configure-sent-data-trigger}

1. Acesse a instância da **Coleção de dados do Adobe Experience Platform** e navegue até as **Propriedades da marca** configuradas com a extensão **SDK da Web da Adobe Experience Platform**.

1. No menu **Criação**, selecione **Regras** e **Criar nova regra** ou **Adicionar regra**.

   ![](assets/configure_web_inapp_2.png)

1. Na seção **Eventos**, clique em **Adicionar** e configure-a da seguinte maneira:

   * **Extensão**: principal

   * **Tipo De Evento**: Biblioteca Carregada (Início Da Página).

   ![](assets/configure_web_inapp_3.png)

1. Clique em **Manter alterações** para salvar a configuração do Evento.

1. Na seção **Actions**, clique em **Add** e configure-a da seguinte maneira:

   * **Extensão**: Adobe Experience Platform Web SDK

   * **Tipo de ação**: enviar evento

   ![](assets/configure_web_inapp_4.png)

1. Na seção **Personalization** do seu tipo **Ação**, habilite a opção **Renderizar decisões de personalização visual**.

   ![](assets/configure_web_inapp_5.png)

1. Na seção **Contexto de Decisão**, defina os pares **Chave** e **Valor** que determinam qual experiência fornecer.

   ![](assets/configure_web_inapp_6.png)

1. Salve sua configuração de **Ação** clicando em **Manter alterações**.

1. Navegue até o menu **Fluxo de publicação**. Crie uma nova **Biblioteca** ou selecione uma **Biblioteca** existente e adicione a **Regra** recém-criada a ela. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Na sua **Biblioteca**, selecione **Salvar e criar no desenvolvimento**.

   ![](assets/configure_web_inapp_7.png)

## Configurar regra manual {#configure-manual-trigger}

1. Acesse a instância da **Coleção de dados do Adobe Experience Platform** e navegue até as **Propriedades da marca** configuradas com a extensão **SDK da Web da Adobe Experience Platform**.

1. No menu **Criação**, selecione **Regras** e **Criar nova regra** ou **Adicionar regra**.

   ![](assets/configure_web_inapp_8.png)

1. Na seção **Eventos**, clique em **Adicionar** e configure-a da seguinte maneira:

   * **Extensão**: principal

   * **Tipo de evento**: clique

   ![](assets/configure_web_inapp_9.png)

1. Na **Configuração de clique**, defina o **Seletor** que será avaliado.

   ![](assets/configure_web_inapp_10.png)

1. Clique em **Manter alterações** para salvar a configuração de **Evento**.

1. Na seção **Actions**, clique em **Add** e configure-a da seguinte maneira:

   * **Extensão**: Adobe Experience Platform Web SDK

   * **Tipo de ação**: avaliar conjuntos de regras

   ![](assets/configure_web_inapp_11.png)

1. Na seção **Avaliar ação dos conjuntos de regras** do seu tipo de **Ação**, habilite a opção **Renderizar decisões de personalização visual**.

   ![](assets/configure_web_inapp_13.png)

1. Na seção **Contexto de Decisão**, defina os pares **Chave** e **Valor** que determinam qual experiência fornecer.

1. Acesse o menu **Fluxo de publicação**, crie uma nova **Biblioteca** ou selecione uma **Biblioteca** existente e adicione sua **Regra** recém-criada. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. Na sua **Biblioteca**, selecione **Salvar e criar no desenvolvimento**.

   ![](assets/configure_web_inapp_14.png)

