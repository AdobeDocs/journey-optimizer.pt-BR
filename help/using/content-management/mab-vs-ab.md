---
title: Cálculos estatísticos usados no relatório de experimentação
description: Saiba mais sobre Teste A/B versus bandit multiarmado
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
TQID: https://experienceleague.adobe.com/47tFiWTUUsGUMeWhuJVQnakAIrgz1Ax1mO-u8pf27uc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2:
  - id: f29a52db-c90c-4345-902e-b586d1406d8d
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 658
ht-degree: 18%

---

# Comparação entre experimentos A/B e Multi-armed bandit {#mab-vs-ab}

>[!BEGINSHADEBOX]

**Nesta página:** compare experimentos A/B e de bandit multicampo no Adobe Journey Optimizer, incluindo suas forças, limitações e os cenários em que cada método de alocação de tráfego funciona melhor.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Tipo de experimento"
>abstract="O tipo de experimento determina como o tráfego é alocado entre os tratamentos durante o teste. Escolha o método que melhor se alinha às suas metas:</br><b>Experimento A/B</b>: divide o tráfego conforme definido entre os tratamentos e mede o desempenho até que os resultados sejam estatisticamente significativos. Ideal para identificar qual tratamento apresenta o melhor desempenho em uma comparação controlada.</br><b>Multi-armed Bandit</b>: direciona o tráfego para os tratamentos com melhor desempenho à medida que os dados são coletados, equilibrando rapidez e otimização. Útil para maximizar as conversões durante o experimento.</br><b>Use seu próprio Multi-armed Bandit</b>: Utilize o próprio algoritmo para definir a alocação de tráfego, oferecendo flexibilidade caso haja um modelo ou estratégia personalizados."

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
