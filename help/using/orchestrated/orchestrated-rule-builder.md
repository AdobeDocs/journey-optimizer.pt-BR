---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o construtor de regras
description: Saiba como criar regras para suas campanhas orquestradas
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 450f83eb53068df10a63d39d1a43483ad3c7e803
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 4%

---


# Trabalhar com o construtor de regras {#orchestrated-rule-builder}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Iniciar sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Etapas principais para a criação de campanhas orquestradas](gs-campaign-creation.md) | [Criar uma campanha orquestrada](create-orchestrated-campaign.md)<br/><br/>[Configurações de campanhas orquestradas](orchestrated-campaign-settings.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Enviar mensagens com campanhas orquestradas](send-messages.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | <b>[Trabalhar com o construtor de regras](orchestrated-rule-builder.md)</b><br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Eliminação de Duplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

As campanhas orquestradas vêm com um construtor de regras que simplifica o processo de filtragem do banco de dados com base em vários critérios. O construtor de regras gerencia consultas muito complexas e longas com eficiência, oferecendo flexibilidade e precisão aprimoradas.

Também oferece suporte a filtros predefinidos em condições, permitindo que os usuários refinem consultas com facilidade enquanto utilizam expressões e operadores avançados para estratégias abrangentes de direcionamento e segmentação de público.

## Acessar o construtor de regras

O construtor de regras está disponível ao criar uma consulta em uma atividade **[!UICONTROL Criar público-alvo]** para direcionar um público-alvo. Ele permite que você especifique a população que deseja direcionar e crie facilmente novos públicos-alvo personalizados para suas necessidades.

![imagem mostrando uma atividade de compilação de público-alvo](assets/rule-builder-query.png)

## Interface do construtor de regras {#interface}

O construtor de regras fornece uma tela central onde você cria sua consulta e um painel de propriedades que fornece informações sobre a regra.

![Imagem mostrando a interface do construtor de regras](assets/rule-builder-interface.png)

* A **tela central** é onde você adiciona e combina os diferentes componentes para criar sua regra. [Saiba como criar uma regra](../orchestrated/build-query.md)

* O painel **[!UICONTROL Propriedades da regra]** fornece informações sobre a regra. Ele permite executar várias operações para verificar a regra e garantir que ela atenda às suas necessidades.

  Este painel é exibido ao criar uma consulta para criar um público-alvo. [Saiba como verificar e validar sua consulta](build-query.md#check-and-validate-your-query)
