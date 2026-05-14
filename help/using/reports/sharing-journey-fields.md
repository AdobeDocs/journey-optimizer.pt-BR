---
solution: Journey Optimizer
product: journey optimizer
title: campos de jornada
description: campos de jornada
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 6%

---

# Campos de jornada {#sharing-journey-fields}

Este grupo de campos é usado no esquema **jornada** (em relação a **journeyStepEvent**). Ele contém os campos listados abaixo.


>[!NOTE]
>
>Saiba mais sobre os atributos de propriedades de jornada [nesta seção](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## journeyID {#journeyid-field}

ID da jornada principal.

Tipo: sequência de caracteres

## journeyVersionID {#journeyversionid-field}

Id da versão do jornada. Essa id representa a identidade de uma jornada.

Tipo: sequência de caracteres

## name {#name-field}

Nome da jornada.

Tipo: sequência de caracteres

>[!NOTE]
>
>O nome da jornada é usado para vincular dados de execução da jornada com conjuntos de dados de relatórios. Se você renomear uma jornada, verifique se o novo nome corresponde ao nome no conjunto de dados de relatórios para manter a precisão dos relatórios. Uma incompatibilidade pode fazer com que os dados de relatório não apareçam conforme esperado. Saiba mais sobre [solução de problemas de dados de relatórios ausentes](../building-journeys/report-journey.md#troubleshooting-missing-data).

## descrição {#description-field}

Descrição da jornada.

Tipo: sequência de caracteres

## version {#version-field}

Versão, representada como `major`.`minor`

Tipo: sequência de caracteres
