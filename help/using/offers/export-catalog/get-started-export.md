---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introdução à exportação do catálogo de ofertas
description: Saiba como exportar seu catálogo de ofertas como um conjunto de dados
badge: label="Legado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/71W86v7R-wgsa7JDTE3d6Lddc71MOcTxrY5l0Ts600o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# Introdução à exportação do catálogo de ofertas {#export-catalog}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

O Journey Optimizer permite exportar automaticamente seu catálogo de ofertas para a Adobe Experience Platform.

A exportação cria um conjunto de dados para cada objeto da Biblioteca de ofertas (consulte [Acessar conjuntos de dados exportados](../export-catalog/access-dataset.md)). O serviço inclui:

* Ofertas personalizadas
* Ofertas substitutas
* Posicionamentos
* Decisões

Cada vez que um desses objetos é modificado na Biblioteca de ofertas, um novo processo de exportação é executado automaticamente para atualizar os conjuntos de dados.

>[!NOTE]
>
>Esse serviço está habilitado por padrão. Não é necessária nenhuma etapa de ativação adicional para começar a usá-lo. Após habilitá-lo, os processos de exportação serão automatizados e não exigirão qualquer ação de sua parte.

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
