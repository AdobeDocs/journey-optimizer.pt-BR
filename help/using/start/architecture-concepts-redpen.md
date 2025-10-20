---
solution: Journey Optimizer
product: journey optimizer
title: Arquitetura do AJO
description: Arquitetura e relação com a AEP
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Arquitetura

## Visão geral: como o Adobe Journey Optimizer se encaixa

O Adobe Journey Optimizer (AJO) e o Adobe Experience Platform (AEP) trabalham juntos para permitir a personalização orientada por dados em escala. Esse ecossistema opera como um fluxo contínuo em que os dados são coletados, analisados e aplicados para criar jornadas personalizadas do cliente.

![](../assets/do-not-localize/get-started-big-picture.png)


### Foundation: Adobe Experience Platform (AEP)

O Adobe Experience Platform serve como backbone, permitindo que as marcas centralizem os dados dos clientes e os ativem para experiências personalizadas.

- **Plataforma de dados**: o AEP funciona como hub central para coletar, gerenciar e estruturar dados do cliente para garantir a consistência entre os sistemas.
- **Assimilação de dados (Fontes)**: as marcas importam dados de vários sistemas, como plataformas CRM, sites, aplicativos móveis e armazenamento na nuvem, usando conectores pré-criados. Por exemplo, um Conector do Source assimila dados de compra de uma plataforma de comércio eletrônico.
- **Perfil de cliente em tempo real**: esse recurso cria perfis unificados ao mesclar dados de várias fontes. Por exemplo, um perfil combina interações de email e compras na loja para fornecer uma visualização completa de um cliente.
- **Camada de governança**: essa camada controla o acesso aos dados, a conformidade com a privacidade e a segurança. Ela garante que as marcas utilizem com segurança os dados dos clientes, além de seguir as regulamentações.

### Mecanismo de orquestração: Adobe Journey Optimizer (AJO)

O Adobe Journey Optimizer aplica os dados e insights do AEP para fornecer experiências inteligentes e personalizadas aos clientes em vários canais.

- **Noções básicas do cliente**: os Perfis de clientes em tempo real permitem a segmentação em públicos para mensagens direcionadas. Por exemplo, um Público-alvo inclui compradores frequentes identificados por meio do histórico de compras.
- **Conteúdo e ofertas**:
   - **Gerenciamento de Conteúdo**: este recurso fornece ferramentas para criar, gerenciar e personalizar conteúdo entre canais. Por exemplo, você pode criar um Fragmento de conteúdo reutilizável para um cabeçalho de email promocional.
   - **Gerenciamento de decisão**: este sistema usa a lógica em tempo real para selecionar a melhor oferta ou mensagem para cada indivíduo. Por exemplo, um cliente elegível pode receber uma oferta de desconto com base em seu histórico de navegação.
- **Gerenciamento de Jornadas e Campanhas**: esse recurso automatiza sequências de interações (Jornadas) ou agenda mensagens direcionadas únicas (Campanhas). Por exemplo, uma Jornada aciona emails de acompanhamento após uma exibição de produto.
- **Entrega (Conexões)**:
   - **Canais**: esse recurso fornece mensagens e ofertas por meio de plataformas de comunicação, como email, SMS, notificações por push e correspondência direta.
   - **Destinos**: este recurso exporta dados de perfil e público-alvo para sistemas externos para ativação ou análise. Por exemplo, os dados do público são enviados para uma plataforma de mídia social para direcionamento de anúncios.
- **Medição e análise**: esse recurso acompanha o envolvimento do cliente e o desempenho da campanha com os relatórios. Esses insights permitem melhoria contínua.

## Ciclo de otimização contínua

Esse ecossistema opera como um ciclo de otimização contínuo. Os dados impulsionam a compreensão do cliente, que informa o conteúdo personalizado e as decisões. Eles são orquestrados em jornadas, distribuídos em canais, medidos para eficiência e refinados ao longo do tempo.

![](../assets/do-not-localize/get-started-flow.png)

## Arquitetura detalhada

![Arquitetura do Adobe Journey Optimizer](assets/ajo-architecture.png)


## Privacidade e segurança

As práticas de privacidade e segurança da Adobe Experience Cloud se aplicam ao Adobe Journey Optimizer. Essas medidas garantem a conformidade com as regulamentações de privacidade, permitindo que as marcas forneçam experiências personalizadas, mantendo a confiança do cliente.
