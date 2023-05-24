---
solution: Journey Optimizer
product: journey optimizer
title: Cálculos estatísticos usados pela experimentação do Adobe Journey Optimizer
description: Saiba mais sobre cálculos estatísticos usados ao executar experimentos
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
keywords: conteúdo, experimento, estatístico, cálculo
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 6%

---

# Compreender cálculos estatísticos {#experiment-calculations}

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* [Introdução ao experimento de conteúdo](get-started-experiment.md)
* [Criar um experimento de conteúdo](content-experiment.md)
* **[Compreender cálculos estatísticos](experiment-calculations.md)**
* [Configurar relatórios de experimentação](reporting-configuration.md)
* [Cálculos estatísticos no relatório de Experimentação](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Este artigo descreve os cálculos estatísticos usados quando você executa experimentos no Adobe Journey Optimizer.

A experimentação usa métodos estatísticos avançados para calcular **Sequências de confiança** e **Confiança**, que permitem executar seus experimentos enquanto for necessário e monitorar continuamente os resultados.

Este artigo descreve como a Experimentação funciona e fornece uma introdução intuitiva ao Adobe verificação **Sequências de confiança válidas a qualquer momento**.

Para usuários especialistas, as referências e os detalhes técnicos são detalhados em [esta página](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Teste estatístico e controle de erros {#statistical-testing}

![](assets/technote_1.png)

Como ilustrado na tabela acima, muitas metodologias de inferência estatística foram projetadas para controlar dois tipos de erros:

* **Falsos positivos (erros de tipo I)**: é uma rejeição incorreta da hipótese nula, quando, na verdade, é verdadeira. No contexto de experimentos online, isso significa que concluímos falsamente que a métrica de resultado é diferente entre cada tratamento, embora seja a mesma.
   </br>Antes de executarmos o experimento, normalmente escolhemos um limite `\alpha`. Após a execução do experimento, a variável `p-value` é calculado e rejeitamos a variável `null if p < \alpha`. Um limite usado com frequência é `\alpha = 0.05`, o que significa que, a longo prazo, esperamos que 5 em cada 100 experimentos sejam falsos positivos.

* **Falsos negativos (erros tipo II)**: significa que não rejeitamos a hipótese nula, embora ela seja falsa. Para experimentos, isso significa que não rejeitamos a hipótese nula, quando na verdade ela é diferente. Para controlar esse tipo de erro, geralmente precisamos ter usuários suficientes em nosso experimento para garantir uma determinada Potência, definida como `1 - \beta`(isto é, um menos a probabilidade de um erro de tipo II).

A maioria das técnicas de inferência estatística exige que você corrija o tamanho da amostra antecipadamente, com base no tamanho do efeito que deseja determinar, bem como na tolerância a erros (`\alpha` e `\beta`) com antecedência. No entanto, a metodologia da Adobe Journey Optimizer foi projetada para permitir que você verifique continuamente seus resultados, para qualquer tamanho de amostra.

## Metodologia Estatística Do Adobe: Sequências De Confiança Válidas A Qualquer Momento

A **Sequência de confiança** é um análogo sequencial de um **Intervalo de confiança**, por exemplo, se você repetir seus experimentos cem vezes e calcular uma estimativa da métrica média e sua sequência associada de 95% de confiança para cada novo usuário que entra no experimento. Uma sequência de confiança de 95% incluirá o valor real da métrica em 95 dos 100 experimentos executados. Um intervalo de confiança de 95% só pode ser calculado uma vez por experimento a fim de dar a mesma garantia de cobertura de 95%; não com cada novo usuário. As Sequências de confiança permitem, portanto, monitorar continuamente os experimentos sem aumentar as taxas de erro de falso positivo.

A diferença entre as sequências de confiança e os intervalos de confiança para um único experimento é mostrada na animação abaixo:

![](assets/technote_2.gif)

**Sequências de confiança** mude o foco de experimentos para estimativa em vez de teste de hipótese, ou seja, focalizando na estimativa precisa da diferença nas médias entre tratamentos, em vez de rejeitar ou não uma hipótese nula com base em um limite de significância estatística.

No entanto, de forma semelhante à relação entre `p-values`ou **Confiança**, e **Intervalos de confiança** Além disso, existe também uma relação **Sequências de confiança** e em qualquer horário válido `p-values`ou qualquer Confiança válida. Dada a familiaridade de quantidades como o Confidence, o Adobe fornece tanto o **Sequências de confiança** e em qualquer momento válida Confiança em seus relatórios.

Os fundamentos teóricos da **Sequências de confiança** vêm do estudo de sequências de variáveis aleatórias conhecidas como martingales. Alguns resultados principais foram incluídos abaixo para leitores especialistas, mas os argumentos dos profissionais são claros:

>[!NOTE]
>
>As sequências de confiança podem ser interpretadas como análogos sequenciais seguros de intervalos de confiança. Você pode observar e interpretar dados em seus Experimentos a qualquer momento que desejar e parar ou continuar com experimentos com segurança. a confiança válida a qualquer momento correspondente, ou `p-value`, também é seguro de interpretar.

É importante observar que, como as sequências de confiança são &quot;válidas a qualquer momento&quot;, elas serão mais conservadoras do que uma metodologia de horizonte fixo usada no mesmo tamanho de amostra. Os limites da sequência de confiança geralmente são mais amplos do que um cálculo de intervalo de confiança, enquanto a confiança válida a qualquer momento será menor do que um cálculo de confiança de horizonte fixo. O benefício deste conservadorismo é que você pode interpretar com segurança seus resultados em todos os momentos.

## Declarar um experimento como conclusivo

![](assets/experimentation_report_2.png)

Toda vez que você visualiza o relatório de experimentação, o Adobe analisa os dados acumulados no experimento até o momento e declara um experimento como &quot;Conclusivo&quot; quando a confiança válida a qualquer momento ultrapassa um limite de 95% para pelo menos um dos tratamentos.

Neste ponto, o tratamento que está tendo o melhor desempenho (com base na taxa de conversão ou no valor da métrica normalizada do perfil) será destacado na parte superior da tela do relatório e indicado com uma estrela no relatório tabular. Somente tratamentos que tenham uma confiança maior que 95%, juntamente com a linha de base, são considerados nesta determinação.

Quando há mais de dois tratamentos, o link de correção de Bonferroni é usado para corrigir vários problemas de comparação e controla a taxa de erro na família. Nesse cenário também é possível que existam tratamentos múltiplos cuja confiança é maior que 95% e cujos intervalos de confiança se sobrepõem. Nesse caso, o Adobe Journey Optimizer declarará aquela com a taxa de conversão mais alta (ou valor de métrica normalizado por perfil) como o melhor desempenho.
