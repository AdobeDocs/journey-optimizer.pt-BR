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
source-git-commit: 59e85eb7a14f88d95b2ef97e3ace11a65f115b75
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 1%

---

# Perguntas frequentes sobre decisão {#decisioning-faq}

Esta página fornece respostas a perguntas frequentes sobre os recursos do Decisioning no Adobe Journey Optimizer.

## Regras de limite {#capping-rules}

+++**O que acontece quando você cria mais de uma regra de limitação para uma oferta? Deixaremos de mostrar a oferta quando correspondermos a alguma ou todas as regras de limitação?**

A oferta é limitada assim que **uma condição é atendida**. Isso significa que qualquer uma das regras de limitação impedirá a exibição da oferta quando o limite for atingido.

Por exemplo, se você tiver duas regras de limitação:
* 5 vezes por perfil por semana
* 100 vezes o total em todos os usuários

A oferta deixará de ser exibida para um usuário depois de tê-la visto 5 vezes em uma semana, mesmo que o limite total de 100 ainda não tenha sido atingido. Da mesma forma, quando o total de 100 impressões é atingido, a oferta deixa de ser exibida para todos os usuários.

Saiba mais sobre [regras de limitação](items.md#capping).

+++

## Fórmulas de classificação {#ranking-formulas}

+++**Por que adicionaria um público-alvo a um modelo de IA? Qual é o benefício de adicionar públicos-alvo em relação a um conjunto de dados completo? Ele restringirá ou expandirá o modelo?**

Ao trabalhar com modelos de IA (especificamente [modelos de otimização personalizados](ranking/personalized-optimization-model.md)):

* **Conjuntos de dados** são adicionados para coletar os eventos de conversão (cliques, pedidos, receita). Esses são os resultados para os quais o modelo tenta otimizar.
* **Públicos-alvo** são adicionados para serem usados como variáveis de previsão no modelo. Eles ajudam a personalizar previsões para tentar prever cliques, pedidos ou receita para diferentes segmentos de clientes.

Os conjuntos de dados e os públicos-alvo são necessários para que o modelo de otimização personalizado funcione com eficiência. Os públicos-alvo **não restringem nem expandem** o modelo; em vez disso, fornecem contexto adicional que ajuda o modelo a tomar decisões mais personalizadas.

Saiba mais sobre [modelos de IA](ranking/ai-models.md).

+++

+++**A adição ou remoção de ofertas em uma coleção terá algum impacto no modelo se eu estiver usando modelos de otimização automática ou personalizados?**

Ambos os modelos fornecerão o tráfego para a próxima melhor oferta disponível com base nos dados de tráfego dos últimos 30 dias.

Se várias ofertas forem removidas de uma vez e as ofertas restantes tiverem recebido muito pouco tráfego nos últimos 30 dias, a distribuição da oferta poderá se comportar inesperadamente. Isso pode resultar em distribuição aleatória ou tendência a determinadas ofertas que têm uma taxa de conversão mais alta com base em apenas algumas impressões.

**Prática recomendada**: ao fazer alterações significativas em coleções de ofertas, verifique se as ofertas restantes têm dados históricos de desempenho suficientes para manter o desempenho ideal do modelo.

+++

+++**Quanto tempo leva para os modelos de IA entenderem que há novo conteúdo adicionado e começarem a adicioná-lo à combinação?**

Ambos os modelos de IA identificarão ofertas recém-disponíveis na próxima execução de treinamento:

* **Otimização automática**: execuções diárias de treinamento
* **Otimização personalizada**: execuções de treinamento semanais

Uma vez identificados, ambos os modelos começarão a distribuir as novas ofertas para alguns visitantes imediatamente, a fim de testar seu desempenho e coletar dados sobre sua eficácia.

Saiba mais sobre [otimização automática](ranking/auto-optimization-model.md) e [otimização personalizada](ranking/personalized-optimization-model.md) modelos.

+++

+++**Se não tivermos grupos de controle nos modelos de IA, estamos aprendendo e otimizando todo o tráfego ao mesmo tempo?**

Sim. Ambos os modelos de IA (otimização automática e otimização personalizada) usam uma abordagem de &quot;exploração e exploração&quot;:

* Inicialmente, ambos os modelos são **100% de exploração**, o que significa que eles testam diferentes ofertas para coletar dados de desempenho.
* Com o tempo, os modelos **gerenciam automaticamente a compensação de explorar/explorar** à medida que eventos comportamentais são coletados e as previsões melhoram.
* Os modelos gradualmente deslocam mais tráfego para ofertas de melhor desempenho, enquanto continuam a explorar e testar outras opções.

Isso garante aprendizagem e otimização contínuas em todo o tráfego, sem a necessidade de grupos de controle separados.

+++

+++**Quantos eventos de otimização precisamos ter significância estatística? Existe um limite mínimo de tráfego para uma superfície?**

Para garantir o desempenho ideal do modelo, a Adobe recomenda os seguintes mínimos:

**Mínimos recomendados (por semana):**
* Pelo menos **1.000 impressões** por oferta/item
* Pelo menos **100 eventos de conversão** por oferta/item

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Por padrão, o sistema não tentará criar modelos personalizados para ofertas/itens com menos de 1.000 impressões ou 50 eventos de conversão.

**Importante**: na prática, alguns clientes têm muitas ofertas (~300) em um único modelo e algumas ofertas podem ter regras de negócios muito restritivas. Os mínimos absolutos (250 impressões / 25 conversões por 30 dias) representam o limite mais baixo que o sistema pode suportar para construir modelos.

Saiba mais sobre [requisitos de coleta de dados](data-collection/data-collection.md).

+++

+++**O conteúdo das ofertas precisa ser claramente diferenciado para que os modelos de IA funcionem bem? O que acontece se eu tiver várias ofertas muito semelhantes?**

De modo geral, o modelo de IA terá mais probabilidade de gerar benefícios de personalização quando **as ofertas forem adequadas a diferentes tipos de clientes**.

Quando as ofertas são muito semelhantes, um dos dois resultados é provável:

* **Desempenho semelhante**: as ofertas terão desempenho idêntico e receberão uma parte relativamente uniforme do tráfego.
* **Domínio**: pequenas diferenças podem fazer com que uma oferta domine as outras em todos os tipos de clientes e ela receberá a maior parte do tráfego.

>[!NOTE]
>
>As diferenças nas ofertas não são uma garantia de que uma oferta não dominará as outras. Por exemplo, uma oferta de 100€ de desconto quase sempre terá um desempenho melhor que uma oferta de 50€ de desconto em todos os tipos de clientes, independentemente da personalização.

**Prática recomendada**: certifique-se de que suas ofertas forneçam diferenciação significativa que possa atrair diferentes segmentos de clientes para obter o desempenho ideal do modelo de IA.

+++

+++**O que acontece com o modelo se houver uma anomalia de tráfego, como um grande pico de tráfego? Isso causará problemas ou causará estranheza?**

Um pico de tráfego seria incluído na modelagem proporcionalmente a outro tráfego nos últimos 30 dias.

Por exemplo, um pico de tráfego diário 2x terá um efeito relativamente modesto no modelo geral, porque há 29 dias de tráfego normal que representam significativamente mais dos dados comportamentais gerais.

**Ponto-chave**: a janela contínua de 30 dias ajuda o modelo a manter a estabilidade durante anomalias temporárias de tráfego. Picos ou declínios de curto prazo não interromperão significativamente o desempenho do modelo.

+++

## Tópicos relacionados {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Criar itens de decisão](items.md)
* [Visão geral dos modelos de IA](ranking/ai-models.md)
* [Medidas de proteção e limitações do serviço de decisão](decisioning-guardrails.md)

