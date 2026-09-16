---
solution: Journey Optimizer
product: journey optimizer
title: Colaborador para gerenciamento de conteúdo
description: Descubra as ferramentas de gerenciamento de conteúdo do CX Enterprise Coworker disponíveis para descobrir, criar e gerenciar ativos de conteúdo do Journey Optimizer, com orientação detalhada e prompts de amostra.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 2e8b79e40abe397222b76c2a7b1ff4dcfcc90292
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%
---

# Colaborador para gerenciamento de conteúdo {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**Nesta página:** Descubra as ferramentas de gerenciamento de conteúdo do CX Enterprise Coworker disponíveis no Adobe Journey Optimizer — para navegar, criar, atualizar, clonar e publicar modelos de conteúdo, fragmentos, páginas de aterrissagem e conteúdo integrado de jornada/campanha — com orientações detalhadas, prompts de exemplo e práticas recomendadas.

Saiba mais:

* [Habilidades de colega de trabalho para o Journey Optimizer](../start/ai-features.md#cx-coworker-skills) — visão geral das habilidades de colega em Jornadas, Fidelidade e Gerenciamento de Conteúdo no Journey Optimizer.
* [Documentação do colaborador](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — visão geral dos recursos de Campanhas, Chat e Projetos do colaborador.
* [Guia da interface de Chat do Colaborador](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — como acessar e navegar pelo Chat do Colaborador.

>[!ENDSHADEBOX]

## Ferramentas de gerenciamento de conteúdo {#content-management}

>[!AVAILABILITY]
>
>O Gerenciamento de conteúdo está disponível para todos os clientes que têm acesso ao Colaborador.

Os usuários do Journey Optimizer podem descobrir e gerenciar ativos de conteúdo — modelos de conteúdo, fragmentos, páginas de aterrissagem e conteúdo de mensagem em linha de jornada/campanha — diretamente do Colaborador usando prompts de linguagem natural. Ela permite ir de &quot;me falar sobre meu conteúdo&quot; a &quot;criar, atualizar e publicar&quot;, sem sair da conversa. Esse recurso é alimentado por 15 ferramentas de MCP com capacidade de leitura e gravação para conteúdo do Journey Optimizer.

### Principais casos de uso

1. **Procurar e inspecionar conteúdo**

   * Liste os modelos de conteúdo, fragmentos ou páginas de aterrissagem disponíveis e recupere sua estrutura, metadados e status.
   * Recupere o conteúdo da mensagem em linha configurado em um nó de ação de campanha ou do jornada.

   Exemplos de prompts:
   * &quot;Listar meus modelos de conteúdo de email.&quot;
   * &quot;Mostre-me os fragmentos disponíveis para minha campanha de verão.&quot;
   * &quot;Obtenha os detalhes da landing page-123.&quot;
   * &quot;Qual conteúdo está configurado para a variante de email do nó de ação no campaign camp-789?&quot;

1. **Criar modelos de conteúdo**

   * Crie um novo modelo de conteúdo para qualquer canal.

   Exemplos de prompts:
   * &quot;Crie um modelo de email chamado Vendas de verão com este conteúdo do HTML.&quot;
   * &quot;Crie um novo modelo de SMS chamado Alerta Flash.&quot;

1. **Atualizar modelos de conteúdo**

   * Substituir totalmente o conteúdo de um template existente.

   Exemplos de prompts:
   * &quot;Atualize o template abc-123 com este novo corpo do HTML.&quot;

1. **Criar, atualizar, clonar e publicar fragmentos**

   * Crie um novo fragmento de HTML ou expressão.
   * Atualize o conteúdo ou os metadados de um fragmento existente.
   * Clonar um fragmento existente com um novo nome.
   * Enviar um fragmento de rascunho para publicação.

   Exemplos de prompts:
   * &quot;Crie um fragmento do HTML chamado Banner promocional com esta marcação.&quot;
   * &quot;Atualize o fragmento frag-456 para alterar seu nome para Banner promocional V2.&quot;
   * &quot;Clonar fragmento abc-123 como Banner promocional - Verão (Variante B).&quot;
   * &quot;Publicar fragmento frag-456.&quot;

1. **Atualizar conteúdo da mensagem integrada**

   * Substituir uma variante de canal em uma mensagem em linha do nó de ação de campanha ou jornada.
   * Liste as variantes de canal definidas em um nó de ação de jornada ou campanha.

   Exemplos de prompts:
   * &quot;Atualize a variante de email do nó de ação no campaign camp-789 com este novo conteúdo.&quot;
   * &quot;Quais variantes de canal são definidas neste nó de ação?&quot;

### No escopo

Os seguintes recursos são compatíveis com o gerenciamento de conteúdo:

* **Listar e obter modelos de conteúdo**: procure modelos de conteúdo e recupere sua estrutura e metadados.
* **Listar e obter fragmentos**: procure fragmentos de conteúdo e expressão e recupere seus detalhes.
* **Listar e obter páginas de aterrissagem**: procure páginas de aterrissagem e recupere seus metadados e conteúdo da página.
* **Obter conteúdo embutido de campanha/jornada**: recupere o conteúdo da mensagem embutida configurado em um nó de ação de campanha ou jornada, incluindo variantes multilíngues.
* **Criar modelos de conteúdo**: crie um novo modelo para qualquer canal.
* **Atualizar modelos de conteúdo**: substituir totalmente o conteúdo de um modelo existente.
* **Criar, atualizar, clonar e publicar fragmentos**: crie novos fragmentos, atualize os existentes, clone um fragmento com um novo nome e envie um fragmento de rascunho para publicação.
* **Atualizar conteúdo da mensagem embutida**: substitua uma variante de canal em uma mensagem embutida de nó de ação de campanha/jornada, incluindo variantes multilíngues, e liste as variantes de canal definidas em um nó de ação.

### Fora do escopo

As seguintes funcionalidades não são compatíveis no momento:

* **Pesquisa de texto completo entre modelos ou fragmentos**
* **Validação de modelo ou fragmento** (referências órfãs, links corrompidos, componentes obsoletos)
* **Criando ou publicando páginas de aterrissagem**
* **Excluindo modelos de conteúdo, fragmentos ou páginas de aterrissagem**

### Solicitação de práticas recomendadas

1. **IDs de referência quando conhecidas**: forneça o modelo, fragmento, página de aterrissagem ou ID de campanha/jornada ao solicitar a obtenção, atualização, clonagem ou publicação de um ativo específico.
1. **Seja explícito sobre o canal**: ao criar um modelo ou fragmento, especifique o canal ou o tipo de conteúdo (email, fragmento de HTML, fragmento de expressão).
1. **Confirmar antes de publicar**: revise o conteúdo de um fragmento depois de criá-lo ou atualizá-lo antes de solicitar que o Co-worker o publique.
1. **Forneça o conteúdo de substituição completo**: as operações de atualização substituem o conteúdo na íntegra, portanto, inclua o conteúdo completo do corpo ou da variante do HTML no prompt.

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
