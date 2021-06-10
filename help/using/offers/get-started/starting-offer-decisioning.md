---
title: Introdução ao Gerenciamento de decisão
description: Introdução ao Gerenciamento de decisão. Saiba mais sobre a arquitetura, as ofertas e as decisões, bem como casos de uso comuns que podem ser executados.
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: ht
source-wordcount: '494'
ht-degree: 100%

---


# Sobre o Gerenciamento de decisão {#about-offer-decision}

Use o [!DNL Journey Optimizer] para fornecer a melhor oferta e experiência aos seus clientes em todos os pontos de contato na hora certa. Depois de projetado, direcione os públicos com ofertas personalizadas.

A capacidade de gerenciamento de decisão consiste em dois componentes principais:

* A **Biblioteca de ofertas centralizada**, que é a interface na qual você cria e gerencia os diferentes elementos que compõem suas ofertas e define suas regras e restrições.
* O **mecanismo do Offer Decision**, que aproveita os dados da Adobe Experience Platform e perfis de clientes em tempo real, junto com a biblioteca de ofertas, para selecionar o momento, os clientes e os canais certos aos quais as ofertas serão entregues.

![](../../assets/architecture.png)

Os benefícios incluem:

* Melhor desempenho da campanha fornecendo ofertas personalizadas em vários canais,
* Workflows aprimorados: em vez de criar vários deliveries ou campanhas, as equipes de marketing podem aprimorar os workflows criando um único delivery e variar as ofertas em diferentes partes do modelo,
* Controle a quantidade de vezes que uma oferta é exibida em campanhas e clientes.

![](../../assets/do-not-localize/how-to-video.png) [Assista a estes tutoriais em vídeo](#tutorial-videos) para saber mais sobre o Gerenciamento de decisão.

## Sobre ofertas e decisões {#offers-offer-activities}

Uma **Oferta** é composta de conteúdo, regras de elegibilidade e restrições que definem as condições em que é apresentada aos clientes.

Ela é criada usando a **Biblioteca de ofertas**, que fornece um catálogo de ofertas central, em que você pode associar regras e restrições de elegibilidade a vários conteúdos para criar e publicar ofertas (consulte [Interface de usuário da Biblioteca de ofertas](../get-started/user-interface.md)).

![](../../assets/offer_structure.png)

Depois que a Biblioteca de ofertas foi enriquecida com ofertas, você pode integrar suas ofertas em **decisões** (antes conhecidas como &quot;atividades de oferta&quot;).

As decisões são containers para suas ofertas que aproveitarão o Mecanismo do Offer Decisioning para escolher a melhor oferta a ser entregue, dependendo do target da entrega.

## Casos de uso comuns

Os recursos e a integração do Gerenciamento de decisão com a Adobe Experience Platform permitem reunir vários casos de uso para ajudar você a aumentar o envolvimento e a conversão dos clientes.

* Exiba em seu site as ofertas da página inicial que corresponderão ao ponto de interesse do cliente visitante, com base nos dados da Adobe Experience Platform.

   ![](../../assets/website.png)

* Se os clientes se aproximarem de uma de suas lojas, envie a eles notificações por push lembrando as ofertas disponíveis de acordo com seus atributos (nível de fidelidade, sexo, compras anteriores...).

   ![](../../assets/push_sample.png)

* O Gerenciamento de decisão também ajuda você a aprimorar a experiência dos clientes ao entrar em contato com a equipe de suporte. As APIS do Gerenciamento de decisão permitem exibir no portal de agentes da central de atendimento informações sobre as melhores ofertas resgatadas do cliente e as próximas melhores ofertas.

   ![](../../assets/call-center.png)

## Tutoriais em vídeo {#tutorial-videos}

>[!NOTE]
>
>Esses vídeos se aplicam ao serviço de aplicativos do Offer Decisioning criado na Adobe Experience Platform e não são específicos do [!DNL Adobe Journey Optimizer]. No entanto, fornece orientação genérica para usar o Gerenciamento de decisão no contexto do [!DNL Journey Optimizer].

### O que é o Gerenciamento de decisão? {#what-is-offer-decisioning}

O vídeo abaixo fornece uma introdução aos principais recursos, arquitetura e casos de uso do Gerenciamento de decisão:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Definir e gerenciar ofertas {#use-offer-decisioning}

O vídeo abaixo mostra como usar o Gerenciamento de decisão para definir e gerenciar suas ofertas e aproveitar os dados do cliente em tempo real.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)
