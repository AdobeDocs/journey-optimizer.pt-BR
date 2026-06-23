---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar tags no jornada
description: Gerenciar tags no jornada
feature: Journeys, Tags
topic: Content Management
role: User
level: Intermediate
keywords: jornada, tags
exl-id: 44c255d1-121c-47d4-b407-161626ca3cb4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/O8Igbj-JJGr0aej8xbSvZ51xkcJq8LeJ9JiveyBjBqQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1152
ht-degree: 7%

---

# Gerenciar tags no jornada {#journey_tags}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como organizar jornadas com marcas e categorias de marcas para poder classificar, filtrar e encontrar suas jornadas com mais facilidade do que com convenções de nomenclatura.

>[!ENDSHADEBOX]

Como um profissional da Journey Optimizer, você pode organizar suas jornadas usando tags. As tags são uma maneira rápida e fácil de classificar objetos para melhorar a pesquisa.

## Tags versus convenções de nomenclatura {#tags-vs-naming}

As equipes geralmente dependem de convenções de nomenclatura complexas para armazenar metadados diretamente em nomes de jornadas — por exemplo: *Lifecycle Marketing - Educação - Integração do cliente V2 - Educação para aplicativos - 3º trimestre de 2025*. Embora bem-intencionada, essa abordagem tem um ponto fraco: à medida que o trabalho é dimensionado entre os membros da equipe, a convenção raramente é aplicada de forma consistente e as listas de jornadas se tornam difíceis de navegar.

**As categorias de marcas** no Journey Optimizer oferecem uma alternativa melhor. Em vez de codificar metadados no nome, você anexa tags categorizadas a cada jornada (por exemplo, equipe, objetivo, fase, trimestre) e usa filtros para localizá-las. Os nomes das jornadas podem então se concentrar no que realmente importa: o marco do cliente que está sendo conduzido.

Benefícios das categorias de tags em relação às convenções de nomenclatura:

* **Consistência** — as marcas são selecionadas em uma lista controlada, não são digitadas livremente.
* **Filterability** — qualquer combinação de valores de marca pode ser usada para dividir a lista de jornadas instantaneamente.
* **Clareza** — os nomes das jornadas permanecem curtos e focados em marcos.
* **Escalabilidade** — adicionar uma nova dimensão de metadados significa criar uma nova categoria de marca, e não regravar uma convenção de nomenclatura.

Para obter um fluxo de trabalho de configuração recomendado, consulte [Configurar categorias de marcas para gerenciamento de jornadas](#tags-setup) abaixo.

## Adicionar tags a uma jornada

O campo **Marcas**, nas propriedades da jornada, permite definir marcas para a jornada. É possível selecionar uma tag já existente ou criar uma nova. Comece a digitar o nome da tag desejada e selecione-a na lista. Se não estiver disponível, clique em **Criar** para criar um novo e adicioná-lo à jornada. É possível definir quantas tags forem necessárias.

![Painel de marcas nas propriedades de jornada para categorização e organização](assets/tags1.png)

A lista de tags definidas é exibida abaixo do campo **Tags**.

>[!NOTE]
>
> As tags não fazem distinção entre maiúsculas e minúsculas
> 
> Se você duplicar ou criar uma nova versão de uma jornada, as tags serão preservadas.

## Filtrar por tags

A lista de Jornadas exibe uma coluna dedicada para que você possa visualizar facilmente suas tags.

Um filtro também está disponível para exibir apenas jornadas com determinadas tags.

![Lista suspensa de seleção de marcas com marcas disponíveis para classificação de jornada](assets/tags2.png)

É possível adicionar ou remover tags de qualquer tipo de jornada (ativa, rascunho etc.). Clique no ícone **Mais ações** ao lado da jornada e selecione **Editar marcas**.

![Lista de Jornadas filtrada por marcas mostrando jornadas categorizadas](assets/tags3.png)

## Gerenciar tags

Os administradores podem excluir tags e organizá-las por categorias usando o menu **Tags** em **ADMINISTRAÇÃO**. Consulte esta [documentação](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=pt-BR).

>[!NOTE]
>
> As tags definidas no jornada são adicionadas à categoria &quot;Não categorizada&quot; integrada.

## Configurar categorias de tags para gerenciamento de jornadas {#tags-setup}

Siga estas etapas para substituir uma convenção de nomenclatura complexa por uma abordagem baseada em tags na sua equipe.

**Etapa 1 — Criar categorias de marca (Admin)**

Em **[!UICONTROL Administração]** > **[!UICONTROL Marcas]**, crie uma categoria para cada atributo de metadados que sua equipe codifica atualmente em nomes de jornadas — por exemplo: *Equipe*, *Objetivo de marketing*, *Campanha*, *Fase*, *Trimestre*.

**Etapa 2 — Preencher cada categoria com valores de marca (Admin)**

Em cada categoria, crie as tags que representam todos os valores possíveis. Por exemplo, a categoria *Fase* pode conter: *Percepção*, *Integração*, *Retenção*, *Win-back*.

**Etapa 3 — Aplicar marcas ao criar jornadas (Profissionais)**

Cada vez que uma nova jornada é criada, selecione a tag apropriada de cada categoria nas propriedades da jornada. Uma jornada normalmente carrega uma tag por categoria.

**Etapa 4 — jornadas de nome para o marco, filtrar por marcas**

Mantenha o nome da jornada focado no marco do cliente que ela direciona (por exemplo, *Primeira transação de fidelidade*). Use filtros de tags na lista de jornadas para localizar jornadas por qualquer combinação de metadados, sem depender da análise de nomes.

>[!TIP]
>
>Para uma discussão mais ampla desta abordagem e seus benefícios em escala, consulte [Práticas recomendadas para jornadas avançadas no Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como adicionar, filtrar e gerenciar tags em jornadas no Adobe Journey Optimizer e por que as categorias de tags são uma alternativa melhor às convenções complexas de nomenclatura para organizar listas grandes de jornadas.

**Intenções:**
* Adicionar tags a uma jornada a partir do campo Tags de propriedades da jornada
* Filtrar a lista de jornadas por uma ou mais tags para localizar jornadas específicas rapidamente
* Editar tags em jornadas existentes de qualquer status (ativo, rascunho etc.) por meio de Mais ações
* Criar e organizar categorias de tags como administrador para aplicar metadados consistentes
* Substitua uma convenção complexa de nomenclatura de jornadas por uma abordagem estruturada baseada em tags

**Glossário:**
* **Marcas**: rótulos anexados a jornadas para classificá-las e filtrá-las; não diferencia maiúsculas de minúsculas e é preservado quando uma jornada é duplicada ou tem versão *(específico do produto)*
* **Categorias de marcas**: agrupamentos de valores de marcas relacionados criados por administradores em Administração > Marcas, habilitando a classificação de metadados estruturados *(específico do produto)*
* **Categoria não categorizada**: a categoria padrão interna à qual as marcas criadas diretamente no jornada são atribuídas automaticamente *(específico do produto)*

**Medidas de Proteção:**
* As tags não diferenciam maiúsculas de minúsculas
* As tags definidas no jornada são adicionadas automaticamente à categoria &quot;Não categorizada&quot; integrada, a menos que um administrador as atribua a uma categoria nomeada
* Somente os administradores podem excluir tags e gerenciar categorias de tag no menu Administração > Tags
* As tags são preservadas quando uma jornada é duplicada ou uma nova versão é criada

**Terminologia:**
* Nome canônico: Tags — Acrônimo: none — variantes: tags de jornada, tags administrativas
* Nome canônico: Categorias de tags — Acrônimo: none — variantes: grupos de tags
* Não confunda: &quot;Tags&quot; (rótulos de classificação de jornada) ≠ &quot;convenções de nomenclatura&quot; (metadados codificados diretamente em nomes de jornada)

**Perguntas frequentes:**
* **P: Como adicionar uma marca a uma jornada?** — Nas propriedades da jornada, digite o nome da tag no campo Tags e selecione-o na lista ou clique em Criar para adicionar uma nova tag.
* **P: Posso adicionar tags a uma jornada em tempo real?** — Sim. Clique no ícone More actions ao lado da jornada na lista e selecione Edit tags para adicionar ou remover tags em qualquer jornada, independentemente do status.
* **P: As marcas diferenciam maiúsculas de minúsculas?** — Não. As tags não diferenciam maiúsculas de minúsculas.
* **P: O que acontece com as marcas quando eu duplicar uma jornada ou criar uma nova versão?** — As tags são preservadas na duplicata ou na nova versão.
* **P: Quem pode excluir marcas ou criar categorias de marcas?** — Somente os administradores podem excluir e gerenciar categorias de tags por meio do menu Administration > Tags.
* **P: Por que usar categorias de marcas em vez de convenções de nomenclatura?** — as categorias de tags reforçam a consistência por meio de uma lista controlada, permitem filtragem multidimensional instantânea, mantêm os nomes das jornadas curtos e focados em marcos e se dimensionam facilmente adicionando novas categorias sem reescrever regras de nomenclatura.

+++
