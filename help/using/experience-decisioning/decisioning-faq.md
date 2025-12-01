---
title: Perguntas frequentes sobre decisão
description: Obtenha respostas para perguntas comuns sobre os recursos do Decisioning
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: e42640e791e6bec3bfd09a3095bad5e44e2ab128
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 1%

---

# Perguntas frequentes sobre decisão {#decisioning-faq}

Esta página fornece respostas a perguntas frequentes sobre os recursos do Decisioning no Adobe Journey Optimizer.

## Regras de limite {#capping-rules}

+++**O que acontece quando várias regras de limitação são aplicadas a uma única oferta?**

Uma oferta é limitada assim que **qualquer única condição for atendida**. Quando existem várias regras de limite, a oferta para de ser exibida assim que qualquer regra atinge seu limite.

**Exemplo:**
Se você definir duas regras de limitação para uma oferta:
* 5 vezes por perfil por semana
* 100 vezes o total em todos os usuários

A oferta deixará de ser exibida para um usuário depois de tê-la visto 5 vezes em uma semana, mesmo que o limite total de 100 ainda não tenha sido atingido. Da mesma forma, quando o total de 100 impressões é atingido, a oferta deixa de ser exibida para todos os usuários.

Saiba mais sobre [regras de limitação](items.md#capping).

+++

## Fórmulas de classificação {#ranking-formulas}

+++**Qual é a função dos públicos-alvo nos modelos de IA?**

Ao configurar [modelos de otimização personalizados](ranking/personalized-optimization-model.md), os conjuntos de dados e os públicos-alvo atendem a diferentes objetivos:

* **Conjuntos de dados**: capture eventos de conversão (cliques, pedidos, receita) que sirvam como destinos de otimização para o modelo.
* **Públicos-alvo**: Função como variáveis preditoras que permitem que o modelo personalize recomendações com base na associação do segmento do cliente.

Os públicos-alvo não restringem ou expandem o escopo do modelo. Em vez disso, eles fornecem atributos contextuais que melhoram a capacidade do modelo de fazer previsões personalizadas em diferentes segmentos de clientes.

Ambos os componentes são necessários para um desempenho eficaz do modelo de otimização personalizado. Saiba mais sobre [modelos de IA](ranking/ai-models.md).

+++

+++**Como as alterações nas coleções de ofertas afetam os modelos de IA ao usar a otimização automática ou modelos de otimização personalizados?**

Ambos os modelos fornecerão o tráfego para a próxima melhor oferta disponível com base nos dados de tráfego dos últimos 30 dias.

Quando várias ofertas são removidas simultaneamente e as demais ofertas têm dados de tráfego mínimos na janela de 30 dias, o modelo pode apresentar um comportamento abaixo do ideal, incluindo:
* Padrões de distribuição aleatória
* Tendência a ofertas com taxas de conversão mais altas com base em dados de impressão limitados

**Prática recomendada**: ao modificar coleções de ofertas significativamente, verifique se as ofertas restantes têm dados históricos de desempenho suficientes para manter a eficácia do modelo.

+++

+++**Com que rapidez os modelos de IA incorporam novas ofertas?**

Os modelos de IA identificam e começam a testar as ofertas recém-disponíveis em seu próximo ciclo de treinamento:

* **Otimização automática**: execuções diárias de treinamento
* **Otimização personalizada**: execuções de treinamento semanais

Uma vez identificados, ambos os modelos começarão a distribuir as novas ofertas para alguns visitantes imediatamente, a fim de testar seu desempenho e coletar dados sobre sua eficácia.

Saiba mais sobre [otimização automática](ranking/auto-optimization-model.md) e [otimização personalizada](ranking/personalized-optimization-model.md) modelos.

+++

+++**Como os modelos de IA otimizam sem grupos de controle?**

Os modelos de otimização automática e personalizada empregam uma estratégia de exploração/exploração que elimina a necessidade de grupos de controle dedicados:

* **Fase inicial**: os modelos começam com 100% de exploração, testando diferentes ofertas para estabelecer dados de desempenho da linha de base.
* **Otimização adaptável**: à medida que os eventos comportamentais se acumulam e a precisão da previsão melhora, os modelos equilibram automaticamente a exploração e a exploração.
* **Aprendizado contínuo**: o sistema aloca progressivamente mais tráfego para ofertas de alto desempenho, enquanto continua testando alternativas.

Isso garante aprendizagem e otimização contínuas em todo o tráfego, sem a necessidade de grupos de controle separados.

+++

+++**Quais são os requisitos mínimos de tráfego para o desempenho ideal do modelo de IA?**

A Adobe recomenda os seguintes limites mínimos para garantir o desempenho eficaz do modelo:

**Mínimos recomendados (por semana):**
* 1.000 impressões por oferta/item
* 100 eventos de conversão por oferta/item

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Por padrão, o sistema não tentará criar modelos personalizados para ofertas/itens com menos de 1.000 impressões ou 50 eventos de conversão.

>[!NOTE]
>
>Em ambientes de produção com grandes catálogos de ofertas (cerca de 300 ofertas) e regras comerciais restritivas, algumas ofertas podem se aproximar de limites absolutos mais baixos (250 impressões e 25 conversões por 30 dias). Estes representam os requisitos mínimos de dados para o treinamento de modelos, mas podem não garantir o desempenho ideal.

Saiba mais sobre [requisitos de coleta de dados](data-collection/data-collection.md).

+++

+++**Como a similaridade da oferta afeta o desempenho do modelo de IA?**

Os modelos de IA geram maiores benefícios de personalização quando as ofertas atraem segmentos de clientes distintos. Quando as ofertas são altamente semelhantes, dois resultados são típicos:

* **Desempenho equivalente**: as ofertas têm desempenho idêntico e recebem distribuição de tráfego aproximadamente igual.
* **Oferta dominante**: pequenas diferenças fazem com que uma oferta tenha um desempenho melhor que outras em todos os segmentos, capturando a maioria do tráfego.

>[!NOTE]
>
>A diferenciação da oferta não garante uma distribuição de tráfego equilibrada. As ofertas com propostas de valor objetivamente superiores (por exemplo, desconto de 100 € versus desconto de 50 €) normalmente dominarão todos os segmentos de clientes, independentemente dos esforços de personalização.

**Prática recomendada**: crie ofertas com diferenciação significativa que se alinhem a preferências de segmentos de clientes distintos para maximizar a eficácia do modelo de IA.

+++

+++**Como as anomalias de tráfego afetam o desempenho do modelo de IA?**

As anomalias de tráfego são incorporadas ao modelo proporcionalmente na janela contínua de 30 dias.

**Avaliação de impacto:**
Um pico temporário de tráfego (por exemplo, o dobro do tráfego diário) tem efeito mínimo no desempenho geral do modelo porque o tráfego anômalo representa uma pequena fração do conjunto de dados de 30 dias.

**Key insight**: a janela de dados contínua de 30 dias fornece a estabilidade do modelo durante flutuações temporárias de tráfego. Picos ou quedas de curto prazo não interrompem significativamente as previsões ou o desempenho do modelo.

+++

## Tópicos relacionados {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Criar itens de decisão](items.md)
* [Visão geral dos modelos de IA](ranking/ai-models.md)
* [Medidas de proteção e limitações do serviço de decisão](decisioning-guardrails.md)

