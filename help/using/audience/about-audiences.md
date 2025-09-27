---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos-alvo da Adobe Experience Platform
description: Saiba como trabalhar com públicos-alvo da Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: d87f33c80cc85b1d1a87150687f6d7c9a268a016
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 19%

---


# Introdução aos públicos-alvo {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Público-alvo"
>abstract="Ao aproveitar os dados do perfil do cliente em tempo real, a Adobe Experience Platform permite criar facilmente definições de segmento para criar públicos-alvo que capturam as preferências e os comportamentos exclusivos dos clientes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selecione o público-alvo da campanha"
>abstract="Esta lista exibe todos os públicos-alvo disponíveis na Adobe Experience Platform. Selecione o público-alvo a ser direcionado pela campanha. A mensagem configurada na campanha será enviada a todas as pessoas pertencentes ao público-alvo selecionado. [Saiba mais sobre públicos-alvo](../audience/about-audiences.md)."

Públicos são coleções de pessoas que compartilham comportamentos e/ou características semelhantes. Eles são configurados e mantidos de forma centralizada no Adobe Experience Platform usando o Serviço de segmentação da Adobe Experience Platform e prontamente acessíveis no Journey Optimizer para serem ativados em suas jornadas e campanhas.

O Adobe Journey Optimizer fornece ferramentas robustas para criar, gerenciar e enriquecer públicos para aprimorar os esforços de marketing. Quando combinado com o Adobe Real-Time Customer Data Platform, o Journey Optimizer permite criar camadas de públicos para segmentações mais complexas e compartilhar públicos bidirecionalmente com outras soluções da Adobe Experience Cloud.

À medida que ocorrem fluxos de dados em tempo real ou uploads em lote, os conjuntos de dados são atualizados e o Journey Optimizer move dinamicamente os indivíduos para dentro e para fora dos públicos-alvo e jornadas em tempo real.

>[!BEGINSHADEBOX]

Esta documentação fornece informações sobre como trabalhar com públicos no [!DNL Adobe Journey Optimizer]. Informações detalhadas sobre o Portal de público-alvo e públicos-alvo estão disponíveis na documentação do Serviço de segmentação do Adobe Experience Platform. Consulte estas seções para obter mais detalhes:

* [Guia da interface do usuário do Serviço de segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/overview){target="_blank"}

* [Serviço de segmentação - Perguntas frequentes](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/faq){target="_blank"}

>[!ENDSHADEBOX]

## Procurar públicos-alvo {#browse}

Os públicos estão disponíveis no menu **[!UICONTROL Cliente]** > **[!UICONTROL Públicos-alvo]**.

Um painel mostra visualmente as sobreposições entre públicos importantes e oferece suporte à exploração de tendências de público valiosas. Por exemplo, as alterações de tamanho de público em um determinado período ou os picos repentinos nos públicos podem destacar eventos ou ações que fizeram com que um público diminuísse ou aumentasse, como uma oferta bem-sucedida.

![](assets/audiences-overview.png)

No Portal de público-alvo, você pode gerenciar, encontrar e explorar públicos-alvo facilmente com rótulos padronizados, controles de governança, pastas pesquisáveis e tags.

Para obter mais informações sobre como trabalhar com públicos no Portal de público, consulte a [documentação do Serviço de segmentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.

## Tipos de públicos {#types}

Os públicos-alvo podem ser gerados usando métodos diferentes:

* **Definições de segmento**: crie uma nova definição de público-alvo usando o Serviço de Segmentação da Adobe Experience Platform. Os públicos-alvo são gerados a partir das definições de segmento e atualizados em momentos diferentes, dependendo do tipo de avaliação.

   * Segmentação de transmissão: os públicos-alvo são atualizados em tempo real, à medida que novos dados fluem no, garantindo relevância contínua com base na atividade do usuário.
   * Segmentação em lote: os públicos-alvo são atualizados a cada 24 horas, capturando um instantâneo dos perfis em um intervalo fixo.
   * Segmentação do Edge: os públicos-alvo são avaliados instantaneamente na borda, permitindo personalização em tempo real.

[Saiba como criar definições de segmento](creating-a-segment-definition.md)

* **Upload personalizado**: importe um público usando um arquivo CSV. [Saiba como criar públicos-alvo de carregamento personalizado](custom-upload.md)

* **Composição de público-alvo**: crie um fluxo de trabalho de composição para combinar públicos-alvo existentes em uma tela visual e aplicar ações como classificação, divisão, junção para criar novos públicos-alvo. [Saiba como trabalhar com a composição de público-alvo](get-started-audience-orchestration.md)

* **Composição de Público-Alvo Federado**: federe conjuntos de dados diretamente do data warehouse existente para compilar e enriquecer públicos-alvo e atributos da Adobe Experience Platform, tudo em um único sistema. [Saiba como trabalhar com a Composição de Público Federado](federated-audience-composition.md).

## Vídeo tutorial {#video}

Saiba mais sobre perfis e públicos-alvo unificados do cliente no Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
