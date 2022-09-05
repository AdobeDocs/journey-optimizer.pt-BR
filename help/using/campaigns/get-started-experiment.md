---
title: Introdução ao experimento de conteúdo
description: Saiba mais sobre o experimento de conteúdo em [!DNL Journey Optimizer]
feature: Overview
topic: Content Management, A/B Testing
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
source-git-commit: 19c52b7c10659305bb729470bf5fa6b9b581bf82
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 1%

---

# Introdução a experimentos de conteúdo {#get-started-experiment}

>[!AVAILABILITY]
>
>O recurso Experimento de conteúdo está disponível atualmente apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

## O que é um experimento de conteúdo?

Os Experimentos de conteúdo permitem otimizar o conteúdo para as ações em suas Campanhas.

Os experimentos são um conjunto de testes aleatórios, o que, no contexto de testes online, significa que alguns usuários selecionados aleatoriamente são expostos a uma determinada variação de uma mensagem e outro conjunto selecionado aleatoriamente de usuários para outro tratamento. Depois de enviar a mensagem, você pode medir as métricas de resultado em que está interessado, por exemplo, aberturas de emails ou cliques.

## Por que executar experimentos?

![](assets/content_experiment_schema.png)

Os experimentos permitem isolar as alterações que levam a melhorias nas métricas. Conforme ilustrado na imagem acima: alguns utilizadores selecionados aleatoriamente são expostos a cada grupo de tratamento, o que significa que, em média, os grupos partilharão as mesmas características. Assim, qualquer diferença nos resultados pode ser interpretada como sendo devida às diferenças nos tratamentos recebidos, ou seja, é possível estabelecer um nexo de causalidade entre as alterações que efetuou e os resultados em que está interessado.

Isso permite que você tome decisões orientadas por dados na otimização de suas metas de negócios.

Para Experiências de conteúdo no Adobe Journey Optimizer, você pode testar ideias como:

* **Linha de assunto**: Qual pode ser o impacto de uma mudança no tom ou no grau de personalização de uma linha de assunto?
* **Conteúdo da mensagem**: A alteração do layout visual de um email resultará em mais cliques no email?

## Dicas para executar experimentos

Ao executar Experimentos, é importante seguir determinadas práticas recomendadas. Estas são algumas dicas para executar esses experimentos:

+++Isole as variáveis que você está tentando testar

Formule algumas hipóteses que pretende testar e restrinja essa hipótese ao menor número possível de alterações para determinar o que teve impacto no delivery.

Por exemplo, uma boa hipótese pode ser se a personalização em linhas de assunto de email direciona melhores taxas de abertura. No entanto, adicionar uma alteração no conteúdo da mensagem ou nas imagens pode resultar em uma conclusão confusa.
+++

+++Verifique se você está usando a métrica correta

Determine a métrica que deseja direcionar e se as alterações feitas podem ter algum impacto direto nessa métrica.

Por exemplo, é improvável que a alteração do conteúdo do corpo da mensagem afete as taxas de abertura do email.
+++

+++Execute o teste no tamanho do público-alvo correto ou por tempo suficiente

Se você executar seus testes por mais tempo, será possível detectar diferenças menores na métrica de meta entre os tratamentos. No entanto, se o valor da linha de base de sua métrica de meta for pequeno, você precisará de tamanhos de amostra maiores.
O número de usuários que devem ser incluídos em seu experimento depende do tamanho do efeito que você deseja detectar, da variação ou propagação de sua métrica de meta, bem como da tolerância para erros falsos positivos e falsos negativos. Em Experimentos clássicos, você pode usar um [calculadora de tamanho da amostra](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=pt-BR){_blank} para determinar por quanto tempo você deve executar o teste.
+++

+++Entender a incerteza estatística

Se você estiver executando um experimento em que 1000 usuários viram um tratamento, e a taxa de conversão é definida como 5%. Essa seria a taxa de conversão real se todos os seus usuários estivessem incluídos? Qual seria a taxa de conversão real?
Os métodos estatísticos dão-nos uma forma de formalizar essa incerteza. Um dos conceitos mais importantes a se entender ao executar experimentos online é que as taxas de conversão observadas são consistentes com uma gama de taxas de conversão verdadeiras subjacentes, o que significa que você deve esperar até que essas estimativas sejam precisas o suficiente, antes de tentar chegar a uma conclusão. Intervalos de confiança, e a confiança nos ajudam a quantificar essa incerteza.
+++

+++Formar nova hipótese e testar continuamente

Para obter insights de negócios verdadeiros, você deve se manter em apenas um Experimento. Em vez disso, acompanhe os experimentos formulando novas hipóteses e executando novos testes com alterações diferentes, em segmentos diferentes, e examinando o impacto nas diferentes métricas.
+++

## Interpretar os resultados dos seus experimentos {#interpret-results}

![](assets/experimentation_report_3.png)

Esta seção descreve os relatórios de Experimento e como entender as várias quantidades estatísticas apresentadas.

Estas são algumas diretrizes para interpretar os resultados do seu Experimento de conteúdo.

Note-se que uma descrição completa dos resultados deve considerar todos os elementos de prova disponíveis (por exemplo, dimensões das amostras, taxas de conversão, intervalos de confiança, etc.), e não apenas a declaração de resultados conclusivos ou não. Mesmo quando um resultado ainda não é conclusivo, ainda pode haver provas convincentes de que um tratamento é diferente do outro.

Para entender os cálculos estatísticos, consulte [página](../campaigns/experiment-calculations.md).

### 1. Comparar métricas normalizadas {#normalized-metrics}

Ao comparar o desempenho de dois tratamentos, você deve sempre comparar as métricas normalizadas para levar em conta quaisquer diferenças no número de perfis expostos a cada tratamento.

Por exemplo, se o objetivo da experiência estiver definido como **[!UICONTROL Unique Opens]** e um determinado tratamento foi mostrado para 10.000 Perfis com 200 Aberturas Únicas registradas, então isso representa uma **[!UICONTROL Conversion Rate]** de 2%. Para métricas não exclusivas, por exemplo, Abrir métrica, a métrica normalizada é mostrada como uma **[!UICONTROL Count per Profile]**, enquanto para métricas contínuas como Preço total, a métrica normalizada é mostrada como uma **[!UICONTROL Total per Profile]**.

### 2. Foco nos intervalos de confiança {#confidence-intervals}

Quando você executa experimentos em amostras de seus perfis, a taxa de conversão observada para um determinado tratamento representa uma estimativa da verdadeira taxa de conversão subjacente.

Por exemplo, se o Tratamento A tiver um **[!UICONTROL Conversion Rate]** de 3%, enquanto que o Tratamento B tem uma **[!UICONTROL Conversion Rate]** de 2%, o Tratamento A tem um melhor desempenho do que o Tratamento B? Para responder a isto, temos primeiro de quantificar a incerteza nestas taxas de conversão observadas.

Os intervalos de confiança ajudam a quantificar o montante de incerteza nas taxas de conversão estimadas, mas intervalos de confiança mais amplos implicam mais incerteza. À medida que mais perfis forem adicionados ao experimento, os intervalos se tornarão menores, representando uma estimativa mais precisa. O intervalo de confiança representa um intervalo de taxas de conversão compatíveis com os dados observados.

Se os intervalos de confiança para dois tratamentos mal estiverem sobrepostos, isso significa que os dois tratamentos têm taxas de conversão diferentes. Mas, se houver muita sobreposição entre os intervalos de confiança de dois tratamentos, então é mais provável que os dois tratamentos tenham a mesma taxa de conversão.

O Adobe usa intervalos de confiança válidos de 95% em qualquer momento, ou sequências de confiança, o que significa que os resultados podem ser visualizados com segurança a qualquer momento durante o experimento.

### 3. Entender o incentivo {#understand-lift}

O resumo do relatório de experiência mostra o **[!UICONTROL Lift over Baseline]**, que é uma medida da percentagem de melhoria na taxa de conversão de um determinado tratamento em relação à linha de base. Definida com precisão, é a diferença de desempenho entre um determinado tratamento e a linha de base, dividida pelo desempenho da linha de base, expressa em percentagem.

### 3. Compreender a confiança {#understand-confidence}

Embora você deva se concentrar principalmente na variável **[!UICONTROL Confidence interval]** para o desempenho de cada tratamento, o Adobe também mostra a Confiança, que é uma medida probabilística da quantidade de evidências de que um determinado tratamento é igual ao tratamento inicial. Uma confiança mais elevada indica menos evidência para o pressuposto de que os tratamentos de base e não basais têm um desempenho igual. Mais precisamente, a confiança que é mostrada é uma probabilidade (expressa como uma porcentagem) de que teríamos observado uma diferença menor nas taxas de conversão entre um determinado tratamento e a linha de base, se na realidade não houver diferença nas taxas de conversão subjacentes reais. Em termos de valores p, a confiança exibida é 1 - valor p.

O Adobe usa valores p &quot;Anytime Valid&quot; e &quot;Anytime Valid&quot; que são consistentes com as Sequências de confiança descritas acima.

### 4. Significância estatística

Ao executar Experimentos, um resultado é considerado estatisticamente significativo se for muito improvável que tenha sido observado com uma hipótese nula de que um determinado tratamento e a linha de base têm taxas/desempenho de conversão subjacentes verdadeiras idênticas.

O Adobe declara um Experimento como conclusivo quando a Confiança estiver acima de 95%.

## O que fazer após executar um Experimento

Depois de executar seu Experimento, há várias ações de acompanhamento possíveis:

* **Implantar ideias vencedoras**

   Com um resultado inequívoco, é possível implantar essa ideia vencedora, enviando o tratamento com melhor desempenho para todos os clientes ou criando novas campanhas nas quais a estrutura do tratamento com melhor desempenho é replicada.
   </br>Observe que em um ambiente dinâmico, o que funciona bem de uma vez, pode não funcionar bem mais tarde.

* **Executar testes de acompanhamento**

   Às vezes, os resultados de seus experimentos podem ser inconclusivos, seja porque não havia perfis suficientes incluídos para detectar qualquer diferença nos tratamentos, ou porque os tratamentos que você definiu não eram suficientemente diferentes.

   Se a hipótese que você estava testando ainda for relevante, executar um teste de acompanhamento em um público maior ou diferente, ou modificar seus tratamentos para que haja diferenças mais claras, pode ser a melhor ação de acompanhamento.

* **Fazer análises de mergulho mais profundas**

   O tratamento que funciona bem para um público-alvo pode, às vezes, não ser o melhor tratamento para outro público-alvo. Fazer análises mais aprofundadas sobre como os tratamentos se comportam para segmentos diferentes ajudam a gerar ideias para novos testes.

   Da mesma forma, estudar o desempenho de cada tratamento com métricas diferentes também pode oferecer uma visão mais abrangente dos seus Experimentos.

   >[!CAUTION]
   >
   >Mais análises significam maior chance de detectar um efeito espúrico ou falso positivo.
