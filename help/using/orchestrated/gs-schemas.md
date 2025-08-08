---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar um esquema relacional no Adobe Experience Platform fazendo upload de uma DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 7fc03d15c63789a2c35e3d517ca0c63f93545d4c
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# Introdução a esquemas relacionais e conjuntos de dados{#gs-schemas}

Este guia orienta você pelo processo de criação de um esquema relacional, configuração de um conjunto de dados para campanhas orquestradas e assimilação de dados.

![](assets/do-not-localize/schema_admin.png)

1. Criar [esquema relacional manualmente](manual-schema.md) ou [usando um arquivo DDL](file-upload-schema.md)

   Defina a estrutura do modelo de dados, incluindo tabelas, atributos e relações. Opte por criar o esquema manualmente na interface do usuário ou fazer upload de um arquivo DDL para uma configuração mais rápida.

   Ao criar o esquema manualmente, o conjunto de dados também deve ser criado e ativado manualmente. Ao usar um arquivo DDL, a criação e a ativação do conjunto de dados são automáticas.

1. [Vincular esquema](file-upload-schema.md)

   Estabeleça relacionamentos entre seus esquemas para garantir a consistência dos dados e habilitar consultas entre entidades. Por exemplo, vincule transações de fidelidade a recipients ou recompensas a marcas.

1. [Assimilar dados](ingest-data.md)

   Traga dados para a Adobe Experience Platform a partir de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.

