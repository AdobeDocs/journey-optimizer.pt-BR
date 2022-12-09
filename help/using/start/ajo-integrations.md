---
solution: Journey Optimizer
product: journey optimizer
title: Integrar com outras soluções
description: Saiba mais como integrar o Journey Otimizer a outras soluções
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 90d7d4d39fe04198707be3d5b24888cfe5bed308
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Integrar com outras soluções {#integration}

Com o Adobe Journey Otimizer, você pode gerenciar, manter e exportar facilmente esses dados para plataformas ou sistemas que fazem parte da sua pilha de tecnologia. Essas integrações ajudam a resolver seus casos de uso específicos e estender o escopo funcional do Adobe Journey Otimizer.

>[!NOTE]
>
> Criado na Adobe Experience Platform, o Adobe Journey Otimizer está conectado nativamente a [Perfil do cliente em tempo real da Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}. Essa fonte de dados integrada é pré-configurada e foi projetada para recuperar e usar dados do Perfil do cliente em tempo real (por exemplo, verifique se a pessoa que entrou em uma jornada é um cliente ou não). Ela permite usar os dados de Perfil e os dados de Eventos de experiência. [Saiba mais](../datasource/adobe-experience-platform-data-source.md).

## Adobe Customer Journey Analytics{#integration-cja}

Você pode usar o Customer Journey Analytics para executar análise avançada dos dados gerados pelo Journey Otimizer.

O Journey Otimizer armazena dados na Adobe Experience Platform e com o Customer Journey Analytics fornece uma visualização holística de todas as jornadas, campanhas e ofertas com distribuição automatizada de relatórios e visualizações personalizadas dos dados.

Depois de criar sua jornada no Journey Otimizer, o Customer Journey Analytics pode assimilar dados da plataforma para iniciar relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

Saiba mais sobre [Journey Otimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

Você pode aproveitar todos os dados de evento comportamental do Adobe Analytics que já estão sendo capturados e transmitidos na Adobe Experience Platform para acionar jornadas em tempo real e automatizar experiências para seus clientes. Esses dados também podem ser usados para criar segmentos que podem ser envolvidos usando o Journey Otimizer.

Saiba mais sobre [Journey Otimizer + Analytics](../event/about-analytics.md).

## Serviços inteligentes da Adobe{#integration-intelligent-service}

Os serviços inteligentes da Adobe, nativos da Plataforma de dados do cliente em tempo real, permitem aproveitar o potencial da inteligência artificial e do aprendizado de máquina em casos de uso da experiência do cliente. Isso permite que os analistas de marketing configurem previsões específicas para as necessidades de uma empresa usando configurações de nível empresarial sem a necessidade de experiência em ciência de dados.

O Customer AI permite que as marcas criem pontuações baseadas em aprendizado de máquina de conversão ou de rotatividade que estarão disponíveis como atributos de perfil na Adobe Experience Platform e que podem ser usadas para personalizar uma jornada.

[Saiba mais](../building-journeys/ai-services-overview.md).


## Adobe Campaign{#integration-ac}

Uma integração estará disponível se você tiver o Adobe Campaign v7 ou v8. Use essa integração para enviar emails, notificações por push e SMS usando os recursos de mensagens transacionais do Adobe Campaign.

Saiba mais sobre [Journey Otimizer + Campaign](../building-journeys/ajo-ac.md).

Você também pode configurar uma integração com o Adobe Campaign Standard para enviar mensagens em suas jornadas.

Saiba mais sobre [Journey Otimizer + Campaign Standard](../building-journeys/ajo-ac.md).

## Canais personalizados{#integration-custom}

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que jornadas enviem chamadas de API para um sistema de terceiros, use ações personalizadas para se conectar à sua jornada. Por exemplo, você pode se conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Desenvolvedor da Adobe](https://developer.adobe.com){target=&quot;_blank&quot;}, Firebase, etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas para os profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da sua jornada no **[!UICONTROL Action]** categoria . Saiba mais em [esta página](../building-journeys/about-journey-activities.md#action-activities).

Saiba mais sobre [ações personalizadas](../action/about-custom-action-configuration.md).

## Fontes de dados externas{#integration-external-systems}

O Journey Otimizer permite configurar conexões com sistemas externos por meio de fontes de dados personalizadas e ações personalizadas. Isso permite, por exemplo, enriquecer suas jornadas com dados provenientes de um sistema de reservas externo.

Saiba como usar fontes de dados externas para definir uma conexão com um sistema de terceiros no [esta seção](../datasource/external-data-sources.md).
