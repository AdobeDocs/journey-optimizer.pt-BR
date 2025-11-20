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
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
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
