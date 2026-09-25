---
solution: Journey Optimizer
product: journey optimizer
title: Colaborador na decisão
description: Descubra as habilidades do CX Enterprise Coworker disponíveis para decisões no Adobe Journey Optimizer, incluindo o Explicador de decisões e as habilidades em Regras e classificação, com orientação detalhada e prompts de amostra.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 8ac4ba8290929e31cd9f7494b63362bc2613d68c
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 1%
---

# Colaborador na decisão {#experience-decisioning-coworker-skills}

>[!BEGINSHADEBOX]

**Nesta página:** descubra as habilidades do CX Enterprise Coworker disponíveis para Decisão no Adobe Journey Optimizer — entender por que uma oferta foi ou não mostrada a um perfil ou segmento, e criar, explicar, simular e otimizar regras de qualificação e fórmulas de classificação — com orientação detalhada, prompts de exemplo e práticas recomendadas.

Saiba mais:

* [Habilidades de colega de trabalho para o Journey Optimizer](../start/ai-features.md#cx-coworker-skills) — visão geral das habilidades de colega em Jornadas, Fidelidade, Gerenciamento de conteúdo e Decisão no Journey Optimizer.
* [Documentação do colaborador](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — visão geral dos recursos de Campanhas, Chat e Projetos do colaborador.
* [Guia da interface de Chat do Colaborador](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — como acessar e navegar pelo Chat do Colaborador.

>[!ENDSHADEBOX]

## Explicador de decisão {#decisioning-explainer}

>[!AVAILABILITY]
>
>O Explicador de decisão está disponível para todos os clientes que têm acesso ao Colaborador e ao Decisioning.

O Decisioning Explainer responde, em linguagem natural, por que uma oferta específica foi ou não mostrada para um determinado perfil — ou, mais amplamente, por que um segmento de perfis não está vendo uma oferta. Ele percorre a pilha de decisão completa para o perfil (ou segmento) e a janela de tempo solicitados: quais ofertas eram elegíveis, qual regra de elegibilidade incluía ou excluía cada uma, se o limite de frequência ou fadiga suprimiu a oferta, as pontuações de classificação finais e qual estratégia ou modelo de IA as produziu e em qual pool candidato (coleção de itens) o perfil foi avaliado.

Isso aborda um desafio comum para os profissionais de marketing: explicar por que uma oferta ficou acima da outra ou por que uma decisão de oferta específica aconteceu da maneira que aconteceu. O Explicador de decisões é somente leitura — ele explica decisões, mas não modifica regras, fórmulas de classificação ou estratégias de seleção.

### Principais casos de uso

* **Por que uma oferta específica foi exibida ou não**

  Exemplos de prompts:
  * &quot;Por que o perfil 12345 viu a Oferta X em 15 de maio?&quot;
  * &quot;O perfil X não foi qualificado para esta oferta?&quot;
  * &quot;Qual regra de elegibilidade excluiu este cliente?&quot;
  * &quot;Mostre-me para quais ofertas o perfil X estava qualificado em 3 de junho.&quot;

* **Por que a visibilidade de uma oferta mudou com o tempo**

  Exemplos de prompts:
  * &quot;Por que a Oferta Y parou de mostrar para clientes recorrentes nos últimos sete dias?&quot;
  * &quot;Quantas vezes esse cliente viu essa oferta?&quot;
  * &quot;Esta oferta foi limitada ao perfil X?&quot;
  * &quot;Quais ofertas estão sendo suprimidas no momento para o perfil X devido a restrições de limite?&quot;

* **Como uma oferta foi classificada ou selecionada**

  Exemplos de prompts:
  * &quot;Mostre-me exatamente como a Oferta Z foi selecionada em relação às outras ofertas qualificadas para este perfil.&quot;
  * &quot;Qual foi a pontuação no ranking para cada oferta nesta decisão?&quot;
  * &quot;Por que a Oferta A ficou acima da Oferta B para este perfil?&quot;
  * &quot;Quais fatores mais influenciaram o resultado do ranking?&quot;

* **Explicações em nível de segmento**

  O Explicador de decisão pode agregar essa lógica em um segmento, em vez de um único perfil, identificando a razão dominante pela qual um grupo de perfis não está vendo uma oferta.

  Exemplos de prompts:
  * &quot;Para clientes neste público-alvo, qual é o motivo mais comum para serem excluídos?&quot;
  * &quot;Quais ofertas esse segmento está realmente recebendo?&quot;
  * &quot;Por que meu segmento de fidelidade não está vendo esta oferta?&quot;

### Solicitação de práticas recomendadas

* **IDs de referência quando conhecidas**: forneça a ID do perfil, o nome da oferta ou o nome do segmento para obter um rastreamento preciso em vez de uma resposta geral.
* **Incluir uma janela de tempo**: especifique uma data ou um intervalo de datas ao perguntar por que a visibilidade de uma oferta mudou; portanto, o Colaborador pode definir o escopo do rastreamento corretamente.
* **Solicitar o detalhamento da classificação diretamente**: se quiser detalhes de pontuação, peça explicitamente a pontuação da classificação ou os fatores que influenciaram o resultado.
* **Use perguntas no nível de segmento para tendências**: ao investigar por que um grupo de perfis não está vendo uma oferta, pergunte sobre o segmento em vez de um único perfil para obter o motivo dominante.

## Regras e classificação {#rules-ranking}

>[!AVAILABILITY]
>
>Regras e classificação está disponível para todos os clientes que têm acesso ao Colaborador e à Decisão.

Rules &amp; Ranking fornece aos profissionais de marketing assistência alimentada por IA para criar, entender e testar a lógica de decisão, sem precisar gravar ou validar manualmente a sintaxe do PQL. Ele abrange quatro recursos principais: criação de regras em linguagem natural, regra em inglês simples e explicação da fórmula de classificação, simulação com até três perfis de teste e otimização para PQL. Tem como escopo as regras de elegibilidade e as fórmulas de classificação — não cria ou edita estratégias de seleção ou políticas de decisão.

### Principais casos de uso

* **Criação da regra de linguagem natural**

  Transforme uma descrição em linguagem simples em sintaxe de regra de elegibilidade do PQL, para novas regras e edições de regras existentes.

  Exemplos de prompts:
  * &quot;Você consegue criar uma regra de elegibilidade que seja direcionada a usuários que atendem às condições XYZ?&quot;
  * &quot;Criar uma regra de elegibilidade direcionada a membros de fidelidade no nível 2 ou superior.&quot;
  * &quot;Escreva uma regra do PQL que exclui clientes que fizeram uma compra nos últimos sete dias.&quot;
  * &quot;Modifique esta regra para excluir também os clientes da lista de supressão.&quot;

* **Regra em inglês simples e explicação da fórmula**

  Explique o que uma regra de elegibilidade ou fórmula de classificação existente faz (o que inclui ou exclui e o que cada condição significa) sem precisar ler a sintaxe do PQL.

  Exemplos de prompts:
  * &quot;Você pode me explicar essa regra em linguagem natural?&quot;
  * &quot;O que esta fórmula de ranking realmente faz?&quot;
  * &quot;A quem esta regra de elegibilidade se destina e a quem ela exclui?&quot;
  * &quot;Resuma essa regra em uma frase.&quot;
  * &quot;Por que a Oferta A está acima da Oferta B para este cliente?&quot;
  * &quot;Essa regra é restritiva demais para uma ampla campanha de conscientização?&quot;
  * &quot;Qual condição nesta regra está filtrando a maioria dos perfis?&quot;

* **Simulação**

  Execute uma regra de elegibilidade ou fórmula de classificação em relação a até três perfis de teste — inseridos manualmente ou gerados por IA, incluindo casos de borda — e obtenha resultados de aprovação/falha com a condição de falha específica, ou uma lista classificada de ofertas com pontuações numéricas.

  Exemplos de prompts:
  * &quot;Simular esta regra com perfis de teste.&quot;
  * &quot;Essa regra é aprovada para um perfil em que fideltier = gold?&quot;
  * &quot;Quais perfis passam esta regra de qualificação: [perfil A, perfil B, perfil C]?&quot;
  * &quot;Por que esse perfil falhou na verificação de qualificação?&quot;
  * &quot;Gerar perfis de teste para esta regra de elegibilidade.&quot;
  * &quot;Gerar perfis de caso de borda que testam essa condição com stress.&quot;
  * &quot;Simular esta fórmula de classificação nessas ofertas e perfis.&quot;
  * &quot;Qual oferta seria a mais alta para esse perfil com essa fórmula?&quot;
  * &quot;Compare como essa regra de elegibilidade se comporta para um cliente de nível ouro versus prata versus básico.&quot;

* **Otimização do PQL**

  Substitua uma regra ou fórmula existente por uma sintaxe mais concisa para atender aos limites de tamanho do PQL da Journey Optimizer, sem alterar a lógica ou o resultado.

  Exemplos de prompts:
  * &quot;Otimizar esta regra do PQL para mim.&quot;
  * &quot;Essa regra está atingindo os limites de tamanho do PQL — é possível encurtá-la?&quot;

### Solicitação de práticas recomendadas

* **Forneça a condição de destino explicitamente**: ao criar ou modificar uma regra, indique a condição exata de público-alvo, atributo ou exclusão que você deseja.
* **Referenciar a regra ou fórmula diretamente**: ao solicitar uma explicação, simulação ou otimização, verifique se a regra ou fórmula desejada está aberta ou claramente identificada.
* **Solicitar casos de borda**: ao simular, peça ao Colaborador para gerar perfis de caso de borda para testar uma condição com stress, não apenas os típicos.
* **Revisar antes de publicar**: verifique a lógica e os resultados da simulação de uma regra gerada ou otimizada antes de publicá-la.

{{$include /help/_includes/do-not-localize/start/ai-augmented-experience-decisioning-coworker-skills.md}}
