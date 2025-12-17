---
title: Introdução às APIs de decisão
description: Saiba como começar a usar as APIs de decisão para gerenciar programaticamente itens de decisão e fornecer ofertas personalizadas.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: e46ab0637a0fa4a2b4b8b6ff3b8ab3eb5d38e0f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 4%

---

# Guia do desenvolvedor da API de decisão {#decisioning-api-developer-guide}

As APIs de decisão permitem criar e gerenciar programaticamente os componentes usados para fornecer ofertas personalizadas aos clientes. Essas APIs RESTful fornecem operações CRUD (Criar, Ler, Atualizar, Excluir) completas para itens de decisão, estratégias de seleção, regras de elegibilidade e outros componentes de decisão.

## Autenticação {#authentication}

Antes de usar APIs de decisão, você deve configurar a autenticação para acessar os endpoints da API. Você pode consultar o [guia de autenticação do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para obter instruções passo a passo.

## Operações de API disponíveis {#available-operations}

As APIs de decisão fornecem recursos abrangentes de gerenciamento para componentes de decisão. As seguintes categorias de operações estão disponíveis:

* **Itens de decisão** - Crie, leia, atualize, exclua e liste itens de decisão que representem as ofertas ou o conteúdo que você deseja entregar aos clientes.

  ➡️ [Saiba como gerenciar itens de decisão](decisions-items/create.md)

* **Coleções de itens** - Organize itens de decisão em coleções para facilitar o gerenciamento e o direcionamento usando regras de qualificação.

  ➡️ [Saiba como gerenciar coleções de itens](items-collections/create.md)

* **Estratégias de seleção** - Defina como os itens de decisão são selecionados e classificados quando vários itens se qualificam para entrega.

  ➡️ [Saiba como gerenciar estratégias de seleção](selection-strategies/create.md)

* **Regras de elegibilidade** - Defina condições que determinam quais perfis estão qualificados para receber itens de decisão específicos.

  ➡️ [Saiba como gerenciar regras de qualificação](eligibility-rules/create.md)

* **Fórmulas de classificação** - Crie uma lógica de classificação personalizada para determinar a ordem em que os itens de decisão são apresentados.

  ➡️ [Saiba como gerenciar fórmulas de classificação](ranking-formulas/create.md)

* **Posicionamentos** - Defina os locais ou contextos em que os itens de decisão podem ser exibidos em suas experiências.

  ➡️ [Saiba como gerenciar posicionamentos](exd-placements/create.md)

## Próximas etapas {#next-steps}

Agora que você entende as noções básicas das APIs de decisão, é possível prosseguir para as operações específicas:

* [Criar itens de decisão](decisions-items/create.md)
* [Listar itens de decisão](decisions-items/decision-items-list.md)
* [Criar estratégias de seleção](selection-strategies/create.md)
* [Criar regras de elegibilidade](eligibility-rules/create.md)

Para obter mais informações sobre como usar a decisão em suas campanhas e jornadas, consulte a [documentação sobre decisões](../gs-experience-decisioning.md).
