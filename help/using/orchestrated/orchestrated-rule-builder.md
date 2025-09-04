---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o construtor de regras
description: Saiba como criar regras para suas campanhas orquestradas
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 76%

---


# Trabalhar com o construtor de regras {#orchestrated-rule-builder}

As campanhas orquestradas incluem um construtor de regras, que simplifica o processo de filtragem do banco de dados com base em vários critérios. O construtor de regras gerencia consultas muito complexas e longas com eficiência, oferecendo flexibilidade e precisão aprimoradas.

Ele também permite utilizar filtros predefinidos com condições, permitindo que você refine as consultas com facilidade enquanto usa expressões e operadores avançados para estratégias abrangentes de direcionamento e segmentação de públicos-alvo.

## Acessar o construtor de regras

O construtor de regras está disponível em todos os contextos nos quais você precisa definir regras para filtrar dados.

| Uso | Exemplo |
|  ---  |  ---  |
| **Criar públicos-alvo**: especifique a população que deseja direcionar em suas campanhas orquestradas usando uma atividade **[!UICONTROL Criar público-alvo]** e crie facilmente novos públicos-alvo adaptados às suas necessidades. [Saiba como criar públicos-alvo](../orchestrated/activities/build-audience.md) | ![Imagem mostrando como acessar a interface de criação de públicos-alvo](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Criar condição na tela da campanha**: aplique regras na tela da campanha, usando uma atividade **[!UICONTROL Divisão]** de acordo com os seus requisitos específicos. [Saiba como usar a atividade divisão](../orchestrated/activities/split.md) | ![Imagem mostrando como acessar as opções de personalização do fluxo de trabalho](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Criar filtros avançados**: crie regras para filtrar os dados exibidos em listas como logs de campanha ou dimensões de direcionamento. | ![Imagem mostrando como personalizar os filtros de lista](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interface do construtor de regras {#interface}

O construtor de regras fornece uma tela central para criar a sua consulta e um painel de propriedades que fornece informações sobre a regra.

![Imagem mostrando a interface do construtor de regras](assets/rule-builder-interface.png)

* A **tela central** é onde você adiciona e combina os diferentes componentes para criar a sua regra. [Saiba como criar uma regra](../orchestrated/build-query.md)

* O painel **[!UICONTROL Propriedades da regra]** fornece informações sobre a regra. Ele permite executar várias operações para verificar a regra e garantir que ela supra as suas necessidades.

  Esse painel é exibido ao construir uma consulta para criar um público-alvo. [Saiba como verificar e validar a sua consulta](build-query.md#check-and-validate-your-query)
