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
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '132'
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
* Disposições
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
