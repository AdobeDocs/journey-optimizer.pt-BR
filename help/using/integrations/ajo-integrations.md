---
solution: Journey Optimizer
product: journey optimizer
title: Integrar a outras soluções
description: Saiba mais sobre como integrar o Journey Optimizer a outras soluções
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 64e225cdc8615e51655ef550866b67ca249a7572
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 87%

---

# Integrações com outras soluções {#integration}

Com o Adobe Journey Optimizer, você pode gerenciar, manter e exportar facilmente esses dados para plataformas ou sistemas que fazem parte de sua pilha de tecnologia. Essas integrações ajudam a resolver casos de uso específicos e a expandir o escopo funcional do Adobe Journey Optimizer.

>[!NOTE]
>
> Criada na Adobe Experience Platform, a Adobe Journey Optimizer está conectada nativamente ao [Perfil de cliente em tempo real do Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}. Essa fonte de dados integrada é pré-configurada e projetada para recuperar e usar dados do Perfil do cliente em tempo real (por exemplo, verificar se a pessoa que entrou em uma jornada é um cliente ou não). Ela permite usar os dados de Perfil e de Eventos de experiência. [Saiba mais](../datasource/adobe-experience-platform-data-source.md).
>

## Adobe Customer Journey Analytics {#integration-cja}

Você pode usar o Customer Journey Analytics para executar análises avançadas em dados gerados pelo Journey Optimizer.

O Journey Optimizer armazena dados na Adobe Experience Platform e, junto com o Customer Journey Analytics, fornece uma visualização integral de todas as jornadas, campanhas e ofertas com distribuição automatizada de relatórios e visualizações personalizadas dos dados.

Depois de criar sua jornada no Journey Optimizer, o Customer Journey Analytics pode assimilar os dados da plataforma para iniciar os relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

Saiba mais sobre o [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics {#integration-aa}

Você pode aproveitar todos os dados de evento comportamentais do Adobe Analytics que já estão sendo capturados e transmitidos à Adobe Experience Platform para acionar jornadas em tempo real e automatizar as experiências de seus clientes. Esses dados também podem ser usados para criar públicos-alvo que podem ser engajados usando o Journey Optimizer.

Saiba mais sobre o [Journey Optimizer + Analytics](../event/about-analytics.md).


## Adobe Experience Manager Assets {#integration-assets}

Junte os fluxos de trabalho de marketing e de criação usando o [!DNL Adobe Experience Manager Assets]. Integrado nativamente no [!DNL Adobe Journey Optimizer], acesse o [!DNL Adobe Experience Manager Assets] para armazenar, gerenciar, descobrir e distribuir ativos digitais. Ele fornece um repositório único e centralizado de ativos que você pode usar para preencher suas mensagens.

O [!DNL Adobe Experience Manager Assets] pode ser acessado diretamente a partir do [!DNL Adobe Journey Optimizer], através da seção **[!UICONTROL Ativos]** no menu esquerdo.

Saiba mais sobre o [Journey Optimizer e Adobe Experience Manager Assets](../integrations/assets.md).


## Adobe Stock {#integration-stock}

O plug-in de integração do Designer de email para o [!DNL Adobe Stock] e [!DNL Adobe Journey Optimizer] fornece aos clientes uma maneira fácil de navegar, licenciar e salvar imagens para uso na criação de mensagens.

Com o [!DNL Adobe Journey Optimizer], você pode fazer upload de imagens para seus emails diretamente do [!DNL Adobe Stock] e adicioná-las à pasta **[!UICONTROL Ativos]** usando a opção **[!UICONTROL Encontrar fotos do Adobe Stock]**. Além disso, a opção **[!UICONTROL Encontrar fotos semelhantes do Stock]** ajuda a encontrar imagens que correspondam ao conteúdo, à cor e à composição do ativo usado na entrega.

Saiba mais sobre o [Journey Optimizer + Stock](../integrations/stock.md).


## Serviços inteligentes da Adobe {#integration-intelligent-service}

Os Serviços inteligentes da Adobe, nativos da Plataforma de dados do cliente em tempo real, permitem aproveitar o potencial da inteligência artificial e do aprendizado de máquina em casos de uso de experiência do cliente. Isso permite que os analistas de marketing estabeleçam previsões específicas para as necessidades de uma empresa usando configurações de nível empresarial, sem a necessidade de uma especialização em ciência de dados.

A IA do cliente permite que as marcas criem pontuações de conversão ou cancelamento baseadas em aprendizado de máquina, que estarão disponíveis como atributos de perfil na Adobe Experience Platform e poderão ser usadas para personalizar uma jornada.

[Saiba mais](../building-journeys/ai-services-overview.md).


## Adobe Campaign {#integration-ac}

Uma integração está disponível se você utilizar o Adobe Campaign v7 ou v8. Use essa integração para enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign.

Saiba mais sobre o [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Você também pode configurar uma integração com o Adobe Campaign Standard para enviar mensagens em suas jornadas.

Saiba mais sobre o [Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).


## Adobe Workfront {#integration-workfront}

Use os módulos do Adobe Journey Optimizer no Adobe Workfront para criar, ler, atualizar ou excluir registros, ou executar uma chamada de API personalizada para a API do Adobe Journey Optimizer.

Uma visão geral da principal etapa dessa integração está disponível [nesta publicação do blog](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/accelerating-go-to-market-how-workfront-workfront-fusion-aep-and/ba-p/653685?profile.language=pt){target="_blank"}.

Saiba mais sobre o Journey Optimizer + Adobe Workfront [na documentação do Adobe Workfront](https://experienceleague.adobe.com/docs/workfront/using/adobe-workfront-fusion/fusion-apps-and-modules/adobe-journey-optimizer-modules.html?lang=pt-BR){target="_blank"}.

## Canais personalizados {#integration-custom}

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que as jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para se conectar à sua jornada. Por exemplo, você pode conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas aos profissionais de marketing. Uma vez configuradas, elas são exibidas na paleta esquerda da jornada na categoria **[!UICONTROL Ação]**. Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

Saiba mais sobre [Ações personalizadas](../action/about-custom-action-configuration.md).

## Fontes de dados externas {#integration-external-systems}

O Journey Optimizer permite configurar conexões com sistemas externos por meio de fontes de dados personalizadas e ações personalizadas. Isso permite, por exemplo, enriquecer suas jornadas com dados provenientes de um sistema de reservas externo.

Saiba como usar fontes de dados externas para estabelecer uma conexão com um sistema de terceiros [nesta seção](../datasource/external-data-sources.md).
