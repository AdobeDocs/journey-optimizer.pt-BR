---
title: Configurações técnicas
description: Saiba mais sobre administração e diretrizes de configurações
hidefromtoc: true
hide: true
source-git-commit: 8a94c63b4a0cba1014e9778caa24720fb975ae52
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 7%

---

# Configurações técnicas

![](../assets/do-not-localize/badge.png)

## Configurar parâmetros de marca{#cjm-branding}

Cada empresa tem diretrizes técnicas e visuais da marca. Você pode definir um conjunto de especificações para apresentar uma marca consistente aos seus clientes, de logotipos a aspectos técnicos, como remetente de email, o domínio do URL das mirror pages ou as configurações de rastreamento de mensagem.
As marcas não podem ser criadas ou modificadas pelos usuários finais: essa configuração é gerenciada pelo Adobe.

Para configurar parâmetros de marca para sua instância [!DNL Journey Optimizer], você precisa entrar em contato com o Adobe e compartilhar os seguintes detalhes:

* Nome da empresa

* Endereço de email do remetente (de)

* Nome (De) do Remetente

* Endereço para resposta

Após configurar os parâmetros da marca, você poderá selecioná-los ao criar mensagens.

Após configurar os parâmetros da marca, você poderá selecioná-los ao criar mensagens na lista **[!UICONTROL Presets]**. [Saiba mais sobre a criação](../create-message.md) de conteúdo.

## Configurar o canal de notificação por push

Saiba como configurar o canal de push nesta [seção](../create-push.md).

## Delegação de subdomínio

Para qualquer novo subdomínio a ser usado em [!DNL Journey Optimizer], a primeira etapa será delegá-lo. É necessário entrar em contato com o contato técnico do Adobe.

Ao implementar uma solução, há requisitos para componentes voltados para o exterior: isso inclui configurar links e páginas da Web a serem rastreadas, exibir mirror pages, etc.

Embora esses requisitos estejam sendo gerenciados por meio de componentes hospedados pelo Adobe e pelo cliente, eles incluem URLs que podem ser vistos pelos recipients dos emails.  Para evitar URLs que indicam a solução técnica subjacente ou o provedor de hospedagem, os subdomínios podem ser configurados para tornar isso transparente para os recipients dos emails.

Na sequência destas delegações, a infraestrutura criada pela Adobe garante que os seguintes serviços sejam executados para cada domínio de envio delegado ou com alias CNAME:

* Criação de caixas de entrada postmaster@ e abusivas@

* Configuração de loops de comentários para o domínio delegado

* Configuração básica do registro DMARC

Os parâmetros estabelecidos pelo Adobe só são válidos a partir do momento em que a delegação foi concluída e depois verificada pelo Adobe, e permanecem funcionais.

[Saiba mais sobre Delegação](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=pt-BR) de domínio.


## Criar fontes de dados, eventos e ações

Use a seção **[!UICONTROL Admin]** para gerenciar **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

### Fontes de dados

A configuração da Fonte de Dados permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas.

Saiba mais sobre Fontes de dados nesta seção [](../datasource/about-data-sources.md)

### Eventos

Os eventos permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada.

Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são normalizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de assimilação de streaming para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK).

Saiba mais sobre eventos nesta [seção](../event/about-events.md)

### Ações

[!DNL Journey Optimizer] os recursos de mensagem são incorporados: você só precisa criar o conteúdo e publicar a mensagem. Se você estiver usando um sistema de terceiros para enviar mensagens, é possível criar uma ação personalizada.

Saiba mais sobre ações nesta [seção](../action/action.md)
