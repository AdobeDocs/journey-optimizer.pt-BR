---
solution: Journey Optimizer
product: journey optimizer
title: Etapas de configuração
description: Saiba como criar um esquema relacional no Adobe Experience Platform fazendo upload de uma DDL
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: 387aa023b4cb999ae4c27cbca4a2f7bcb5edf009
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 2%

---


# Introdução a esquemas relacionais e conjuntos de dados{#gs-schemas}

Este guia orienta você pelo processo de criação de um esquema relacional, configuração de um conjunto de dados para campanhas orquestradas e assimilação de dados.

![esquema](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## Principais conceitos

No contexto de campanhas orquestradas, um **conjunto de dados** é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). Os dados assimilados com sucesso na Experience Platform são armazenados no data lake como conjuntos de dados.

Um **esquema** representa e valida a estrutura e o formato dos dados. Ele fornece uma definição abstrata de um objeto do mundo real (como uma pessoa) e descreve quais dados devem ser incluídos em cada instância desse objeto (como nome, aniversário e assim por diante).

Um **modelo de dados** é o blueprint conceitual da normalização de seus dados

Ele descreve:

* As entidades (por exemplo, cliente, campanha, segmento)
* Os atributos dessas entidades (por exemplo, Nome do cliente, Data de início da campanha)
* Os relacionamentos entre entidades (por exemplo, Clientes pertencem a Segmentos, Campanhas visam Segmentos)

Um modelo de dados é lógico e conceitual, não está vinculado a uma implementação física no Orchestrated Campaign

Em um **Modelo de dados relacional**, os dados são organizados em tabelas relacionadas a outras tabelas.

* Cada tabela tem linhas (registros) e colunas (atributos)
* Cada tabela tem uma chave primária para identificar exclusivamente as linhas
* As relações entre tabelas são expressas usando chaves estrangeiras

Um **esquema relacional** é a definição formal do modelo de dados relacional.

Especifica:

* O conjunto de tabelas
* As colunas em cada tabela
* As restrições
* As relações entre tabelas

Organizar esquemas ou tabelas em um modelo de dados relacional significa estruturar seus dados em várias tabelas. Certifique-se de que cada tabela armazene um tipo de entidade/esquema

## Etapas de implementação {#implementation}

Para assimilar dados e criar esquema relacional, siga estas etapas:

1. Criar [esquema relacional manualmente](manual-schema.md) ou [usando um arquivo DDL](file-upload-schema.md)

   Defina a estrutura do modelo de dados, incluindo tabelas, atributos e relações. Opte por criar o esquema manualmente na interface do usuário ou fazer upload de um arquivo DDL para uma configuração mais rápida.

   Ao criar o esquema manualmente, o conjunto de dados também deve ser criado e ativado manualmente. Ao usar um arquivo DDL, a criação e a ativação do conjunto de dados são automáticas.

1. [Vincular esquema](file-upload-schema.md)

   Estabeleça relacionamentos entre seus esquemas para garantir a consistência dos dados e habilitar consultas entre entidades. Por exemplo, vincule transações de fidelidade a recipients ou recompensas a marcas.

1. [Criar conjunto de dados](manual-schema.md#dataset)

   Depois de definir seu esquema, você precisa criar um conjunto de dados com base nele. Esse conjunto de dados atua como o armazenamento para seus dados assimilados.

1. [Ativar campanha orquestrada](manual-schema.md#enable)

   O conjunto de dados armazena os dados assimilados e deve estar ativado para Campanhas orquestradas para garantir que esteja acessível no Adobe Journey Optimizer.

1. [Assimilar dados](ingest-data.md)

   Traga dados para a Adobe Experience Platform a partir de fontes compatíveis, como SFTP, armazenamento na nuvem ou bancos de dados.

