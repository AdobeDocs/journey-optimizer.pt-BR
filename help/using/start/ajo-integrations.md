---
solution: Journey Optimizer
product: journey optimizer
title: Integrar a outras soluções
description: Saiba mais sobre como integrar o Journey Optimizer a outras soluções
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 34d768502bfb2ce792beae8b1257fdddefc55ed7
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 5%

---

# Integrar a outras soluções {#integration}

Com o Adobe Journey Optimizer, você pode gerenciar, manter e exportar facilmente esses dados para plataformas ou sistemas que fazem parte de sua pilha de tecnologia. Essas integrações ajudam a resolver seus casos de uso específicos e estender o escopo funcional do Adobe Journey Optimizer.

>[!NOTE]
>
> Incorporada no Adobe Experience Platform, a Adobe Journey Optimizer é nativamente conectada ao [Perfil do cliente em tempo real do Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target=&quot;_blank&quot;}. Essa fonte de dados integrada é pré-configurada e foi projetada para recuperar e usar dados do Perfil do cliente em tempo real (por exemplo, verifique se a pessoa que inseriu uma jornada é um cliente ou não). Ela permite usar os dados de Perfil e os dados de Eventos de experiência.


## Relatórios{#integration-reporting}

### Adobe Customer Journey Analytics{#integration-cja}

É possível exportar dados gerados pelo Journey Optimizer para executar análise avançada no Customer Journey Analytics.

A integração do Journey Optimizer com o Customer Journey Analytics oferece uma visualização holística de todas as jornadas com distribuição automatizada de relatórios e visualizações personalizadas dos dados.

Depois de criar sua jornada no Journey Optimizer, você pode importar os dados do cliente para o Customer Journey Analytics para iniciar os relatórios e entender o impacto de cada interação que um cliente tem com suas jornadas.

Saiba mais sobre [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

### Adobe Analytics{#integration-aa}

Você pode aproveitar todos os dados de evento comportamental do Adobe Analytics que já estão sendo capturados e transmitidos no Adobe Experience Platform para acionar jornadas e automatizar experiências para seus clientes.

Saiba mais sobre [Journey Optimizer + Analytics](../event/about-analytics.md).

## Aprendizagem de máquina{#integration-intelligent-service}

A integração com os Serviços inteligentes do Adobe permite aproveitar o potencial da inteligência artificial e do aprendizado de máquina em casos de uso da experiência do cliente. Isso permite que os analistas de marketing configurem previsões específicas para as necessidades de uma empresa usando configurações de nível empresarial sem a necessidade de experiência em ciência de dados.

## Envio de mensagens {#integration-messages}

Você pode usar um sistema de terceiros para enviar mensagens.

### Adobe Campaign{#integration-ac}

Uma integração está disponível se você tiver o Adobe Campaign v7 ou v8. Use essa integração para enviar emails, notificações por push e SMS usando os recursos de Mensagens transacionais do Adobe Campaign.

Saiba mais sobre [Journey Optimizer + Campanha](../building-journeys/ajo-ac.md).

Você também pode configurar uma integração com o Adobe Campaign Standard para enviar mensagens em suas jornadas.

Saiba mais sobre [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

### Canais personalizados{#integration-custom}

Se você estiver usando um sistema de terceiros para enviar mensagens ou se quiser que o jornada envie chamadas de API para um sistema de terceiros, use ações personalizadas para configurar a conexão com a jornada. Por exemplo, você pode se conectar aos seguintes sistemas com ações personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase, etc.

As ações personalizadas são ações adicionais definidas por usuários técnicos e disponibilizadas para os profissionais de marketing. Depois de configuradas, elas são exibidas na paleta esquerda da jornada, no **[!UICONTROL Ação]** categoria . Saiba mais [nesta página](../building-journeys/about-journey-activities.md#action-activities).

Saiba mais sobre [ações personalizadas](../action/about-custom-action-configuration.md).

## Sistemas externos{#integration-external-systems}

O Journey Optimizer permite configurar conexões com sistemas externos por meio de fontes de dados personalizadas e ações personalizadas. Isso permite, por exemplo, enriquecer suas jornadas com dados provenientes de um sistema de reservas externo ou enviar mensagens usando um sistema de terceiros, como Epsilon ou Facebook.

Saiba como usar fontes de dados externas para definir uma conexão com um sistema de terceiros no [esta seção](../datasource/external-data-sources.md).
