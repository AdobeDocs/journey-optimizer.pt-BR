---
solution: Journey Optimizer
product: journey optimizer
title: Cálculos estatísticos usados pela Experimentação do Adobe Journey Optimizer
description: Saiba mais sobre os cálculos estatísticos usados ao executar experimentos
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 3%

---

# Compreender cálculos estatísticos {#experiment-calculations}

>[!AVAILABILITY]
>
>O **Experiência de conteúdo** No momento, o recurso está disponível somente para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

Este artigo descreve os cálculos estatísticos usados ao executar Experimentos no Adobe Journey Optimizer.

A experiência usa métodos estatísticos avançados para calcular **Sequências de confiança** e **Confiança**, que permitem executar seus experimentos enquanto for necessário, e monitorar seus resultados continuamente.

Este artigo descreve como a Experimentação funciona e fornece uma introdução intuitiva ao Adobe **Sequências de confiança válidas a qualquer momento**.

Para usuários especialistas, os detalhes técnicos e as referências são detalhados em [esta página](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Testes estatísticos e controle de erros {#statistical-testing}

![](assets/technote_1.png)

Como ilustrado no quadro acima, muitas metodologias de inferência estatística foram projetadas para controlar dois tipos de erros:

* **Falsos positivos (erros do tipo I)**: é uma rejeição incorreta da hipótese nula, quando na verdade é verdadeira. No contexto de Experiências online, isso significa que concluímos falsamente que a métrica de resultado é diferente entre cada tratamento, embora fosse a mesma.
   </br>Antes de executar o experimento, geralmente escolhemos um limite `\alpha`. Depois que o experimento tiver corrido, a `p-value` é computado e rejeitamos a variável `null if p < \alpha`. Um limite comumente usado é `\alpha = 0.05`, o que significa que, a longo prazo, esperamos que 5 de cada 100 experimentos sejam falsos positivos.

* **Falsos negativos (erros do tipo II)**: significa que não rejeitamos a hipótese nula, embora seja falsa. Para Experiências, isso significa que não rejeitamos a hipótese nula, quando, de fato, ela é diferente. Para controlar esse tipo de erro, geralmente precisamos ter usuários suficientes em nosso experimento para garantir um certo Poder, definido como `1 - \beta`(isto é, um menos a probabilidade de um erro de tipo II).

A maioria das técnicas de inferência estatística exigirá que você corrija o tamanho da amostra antecipadamente, com base no tamanho do efeito que deseja determinar, bem como a tolerância a erros (`\alpha` e `\beta`) com antecedência. No entanto, a metodologia Adobe Journey Optimizer foi criada para permitir que você veja continuamente seus resultados, para qualquer tamanho de amostra.

## Metodologia estatística: Sequências de confiança válidas a qualquer momento

A **Sequência de confiança** é um análogo sequencial de um **Intervalo de confiança**, por exemplo, se você repetir seus experimentos cem vezes e calcular uma estimativa da métrica média e sua sequência de confiança de 95% associada para cada novo usuário que entrar no experimento. Uma Sequência de confiança de 95% incluirá o valor real da métrica em 95 dos 100 experimentos executados. Um intervalo de confiança de 95% só pode ser calculado uma vez por experimento a fim de dar a mesma garantia de cobertura de 95%; não com cada novo usuário. As Sequências de confiança, portanto, permitem monitorar continuamente os experimentos, sem aumentar as taxas de erro Falso positivo.

A diferença entre as sequências de confiança e os intervalos de confiança para um único experimento é mostrada na animação abaixo:

![](assets/technote_2.gif)

**Sequências de confiança** mude o foco das Experiências para estimativa em vez de teste de hipótese, ou seja, focando na estimativa precisa da diferença entre as maneiras, em vez de rejeitar ou não uma hipótese nula com base em um limite de significância estatística.

Mas de modo semelhante à relação entre `p-values`ou **Confiança** e **Intervalos de confiança**, também há uma relação entre **Sequências de confiança** e qualquer hora válida `p-values`, ou qualquer tempo de confiança válida. Dada a familiaridade de quantidades como a Confiança, o Adobe fornece os dois **Sequências de confiança** e qualquer momento de confiança válida em seus relatórios.

As fundações teóricas de **Sequências de confiança** vêm do estudo de sequências de variáveis aleatórias conhecidas como martingales. Abaixo estão incluídos alguns resultados principais para leitores especialistas, mas as contratações de profissionais são claras:

>[!NOTE]
>
>As sequências de confiança podem ser interpretadas como analogias sequenciais seguras de intervalos de confiança. Você pode examinar e interpretar dados em seus Experimentos sempre que desejar e parar com segurança ou continuar experimentos. A Confiança válida Qualquer Hora ou `p-value`, também é seguro interpretar.

É importante notar que, uma vez que as sequências de confiança são &quot;válidas em qualquer momento&quot;, serão mais conservadoras do que uma metodologia de horizonte fixo usada no mesmo tamanho de amostra. Os limites da sequência de confiança são geralmente maiores do que um cálculo de intervalo de confiança, enquanto que qualquer confiança válida de tempo será menor do que um cálculo de confiança de horizonte fixo. O benefício desse conservadorismo é que você pode interpretar seus resultados com segurança em todas as ocasiões.

## Declarando uma experiência como conclusiva

![](assets/experimentation_report_2.png)

Cada vez que você visualiza o relatório de experimentação, o Adobe analisa os dados acumulados no experimento até o momento e vai declarar um experimento como &quot;Conclusivo&quot; quando a confiança válida a qualquer momento ultrapassar um limite de 95% para pelo menos um dos tratamentos.

Neste ponto, o tratamento que está tendo o melhor desempenho (com base na taxa de conversão ou valor de métrica normalizado por perfil) será destacado na parte superior da tela do relatório e indicado por uma estrela no relatório tabular. Nesta determinação são considerados apenas os tratamentos que tenham uma confiança superior a 95%, juntamente com a linha de base.

Quando há mais de dois tratamentos, o link de correção de Bonferroni é usado para corrigir vários problemas de comparação e controla a taxa de erro em relação à família. Nesse cenário, também é possível que haja vários tratamentos cuja confiança é maior que 95% e cujos intervalos de confiança se sobrepõem. Nesse caso, a Adobe Journey Optimizer declarará o com a maior taxa de conversão (ou valor de métrica normalizado por perfil) como o melhor desempenho.
