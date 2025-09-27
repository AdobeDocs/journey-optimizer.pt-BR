---
title: Cálculos estatísticos usados no relatório de experimentação
description: Saiba mais sobre Teste A/B versus bandit multiarmado
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
source-git-commit: 4b0355c4e871e89c1b3eeea978959a2d97fa475d
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 2%

---

# Experimentos de A/B vs Multi-armed bandit {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

Esta página fornece uma comparação detalhada dos experimentos do **A/B** e do **Multi-Armed Bandit**, explicando suas respectivas forças, limitações e os cenários nos quais cada abordagem é mais eficaz.

## A/B {#ab-test}

O experimento A/B tradicional envolve dividir o tráfego igualmente entre os tratamentos e manter essa alocação até que o experimento seja concluído. Uma vez atingida a significância estatística, o tratamento vencedor é identificado e subsequentemente dimensionado.

### Vantagens

Os principais pontos fortes do experimento A/B tradicional são:

* **Rigor Estatístico**

  O design fixo fornece taxas de erro e intervalos de confiança bem definidos.

  Estruturas de teste de hipótese, por exemplo, 95% de confiança, são mais fáceis de aplicar e interpretar.

  Experimentos adequadamente potencializados reduzem a probabilidade de falsos positivos.

* **Simplicidade**

  A metodologia é simples de projetar e executar.

  Os resultados podem ser comunicados claramente às partes interessadas não técnicas.

* **Coleta de dados abrangente**

  Cada tratamento recebe exposição adequada, permitindo a análise não só da variante vencedora, mas também de alternativas com baixo desempenho.

  Essas informações adicionais podem informar as decisões estratégicas de longo prazo.

* **Controle de Bias**

  A alocação fixa reduz a susceptibilidade a vieses como &quot;maldição do vencedor&quot; ou regressão à média.

### Limitações

As principais limitações do experimento A/B tradicional são:

* **Custo da oportunidade**

  Uma parte substancial do tráfego é direcionada a tratamentos inferiores, reduzindo potencialmente as conversões ou a receita durante o teste.

  O tratamento vencedor não pode ser implementado até que o experimento seja concluído.

* **Requisito de Duração Fixa**

  Os testes devem geralmente ser executados para o seu horizonte pré-especificado, mesmo que as condições externas, por exemplo, sazonalidade, mudanças de mercado, se alterem a meio caminho.

  A adaptação durante o experimento é limitada.

## Multi-armed bandit {#mab-experiment}

Os algoritmos de bandit multi-armados usam alocação adaptável: à medida que a evidência se acumula, mais tráfego é direcionado para tratamentos de melhor desempenho. O objetivo é maximizar a recompensa cumulativa durante o experimento, em vez de se concentrar apenas no resultado final.

### Vantagens

Os principais pontos fortes dos métodos Multi-armed bandit são:

* **Otimização mais rápida**

  Tratamentos promissores são priorizados mais cedo, melhorando o desempenho geral durante o teste.

* **Adaptividade**

  As alocações são atualizadas continuamente à medida que os dados são coletados, tornando o Multi-armed bandit adequado a ambientes dinâmicos.

* **Custo de oportunidade reduzido**

  Tratamentos inadequados são eliminados rapidamente, minimizando o desperdício de tráfego.

* **Adequação para teste contínuo**

  Eficaz para experimentação contínua ou contextos em que o tráfego é caro.

### Limitações

As principais limitações dos métodos Multi-armed bandit são:

* **Garantias estatísticas mais fracas**

  O teste de hipótese tradicional é mais difícil de aplicar e a interrupção das regras é menos clara.

* **Transparência Reduzida**

  A alocação adaptável pode ser difícil de explicar às partes interessadas.

* **Informações limitadas sobre tratamentos com baixo desempenho**

  Tratamentos fracos recebem pouca exposição, limitando a insight diagnóstica.

* **Complexidade de implementação**

  Requer algoritmos e infraestrutura avançados, com maior potencial para erro de configuração.

## Quando usar A/B vs Multi-armed bandit

| Cenário | Método recomendado |
|-|-|
| Você está executando testes exploratórios ou orientados por pesquisa | A/B |
| Você está executando campanhas contínuas, por exemplo, anúncios, recomendações | Multi-Armed Bandit |
| Você deseja maximizar as conversões durante o teste | Multi-Armed Bandit |
| Você quer insights claros e confiantes | A/B |
| Você precisa se adaptar rapidamente, por exemplo, mudanças sazonais | Multi-Armed Bandit |
| Você tem tráfego limitado e deseja otimizar o Retorno do investimento rapidamente | Multi-Armed Bandit |
| Você tem alto tráfego e pode arcar com a aprendizagem mais lenta | A/B |
| As partes interessadas precisam de pontos de decisão claros | A/B |
