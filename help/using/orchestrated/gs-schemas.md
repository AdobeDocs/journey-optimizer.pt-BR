---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar um esquema relacional no Adobe Experience Platform fazendo upload de uma DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 31%

---


# Introdução a esquemas relacionais e conjuntos de dados{#gs-schemas}

Este guia orienta você pelo processo de criação de um esquema relacional, configuração de um conjunto de dados para campanhas orquestradas e assimilação de dados.

![](assets/do-not-localize/schema_admin.png)

Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). Os dados assimilados com sucesso na Experience Platform são armazenados no data lake como conjuntos de dados.

Um esquema representa e valida a estrutura e o formato dos dados. Ele fornece uma definição abstrata de um objeto real (como uma pessoa) e descreve quais dados devem ser incluídos em cada instância desse objeto (como nome, data de nascimento e assim por diante).


1. Criar [esquema relacional manualmente](manual-schema.md) ou [usando um arquivo DDL](file-upload-schema.md)

   Defina a estrutura do modelo de dados, incluindo tabelas, atributos e relações. Opte por criar o esquema manualmente na interface do usuário ou fazer upload de um arquivo DDL para uma configuração mais rápida.

   Ao criar o esquema manualmente, o conjunto de dados também deve ser criado e ativado manualmente. Ao usar um arquivo DDL, a criação e a ativação do conjunto de dados são automáticas.

1. [Vincular esquema](file-upload-schema.md)

   Estabeleça relacionamentos entre seus esquemas para garantir a consistência dos dados e habilitar consultas entre entidades. Por exemplo, vincule transações de fidelidade a recipients ou recompensas a marcas.

1. [Assimilar dados](ingest-data.md)

   Traga dados para a Adobe Experience Platform a partir de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.

