---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao experimento de conteúdo
description: Saiba mais sobre experimento de conteúdo no Journey Optimizer
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: introdução, iniciar, conteúdo, experimento
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
source-git-commit: 64be9c41085dead10ff08711be1f39760a81ff95
workflow-type: ht
source-wordcount: '1961'
ht-degree: 100%

---

# Introdução aos experimentos de conteúdo {#get-started-experiment}

## O que é um experimento de conteúdo?

Os experimentos de conteúdo permitem otimizar o conteúdo para as ações em Campanhas.

Os experimentos são um conjunto de testes aleatórios, o que, no contexto de testes online, significa que alguns usuários selecionados aleatoriamente são expostos a uma determinada variação de uma mensagem e outro conjunto de usuários selecionado aleatoriamente recebe tratamento diverso. Depois de enviar a mensagem, você pode medir as métricas de resultado em que está interessado. Por exemplo, aberturas de emails ou cliques.

## Por que executar experimentos?

![](assets/content_experiment_schema.png)

Os experimentos permitem isolar as alterações que levam a melhorias nas métricas. Conforme ilustrado na imagem acima: alguns usuários selecionados aleatoriamente são expostos a cada grupo de tratamento, o que significa que, em média, os grupos partilharão as mesmas características. Assim, qualquer diferença nos resultados pode ser interpretada como sendo devida às diferenças nos tratamentos recebidos, ou seja, você pode estabelecer um nexo de causalidade entre as alterações que fez e os resultados em que está interessado.

Isso permite que você tome decisões orientadas por dados na otimização de suas metas de negócios.

Para Experimentos de conteúdo no Adobe Journey Optimizer, você pode testar ideias como:

* **Linha de assunto**: Qual poderia ser o impacto de uma mudança no tom ou no grau de personalização de uma linha de assunto?
* **Conteúdo da mensagem**: A alteração do layout visual de um email resultará em mais cliques no email?

## Como funciona o experimento de conteúdo? {#content-experiment-work}

### Atribuição aleatória

A experimentação de conteúdo no Adobe Journey Optimizer usa um hash pseudo-aleatório da identidade do visitante para executar a atribuição aleatória de usuários em seu público-alvo a um dos tratamentos que você definiu. O mecanismo de hash garante que, em cenários em que o visitante entra em uma campanha várias vezes, ele receba o mesmo tratamento deterministicamente.

Em detalhes, o algoritmo MumurHash3 de 32 bits é usado para hash da string de identidade do usuário em um dos 10.000 compartimentos. Em um experimento de conteúdo com 50% do tráfego atribuído a cada tratamento, os usuários que caírem nos compartimentos de 1- 5.000 receberão o primeiro tratamento, enquanto os usuários nos compartimentos de 5.001 a 10.000 receberão o segundo tratamento. Como o hash pseudo-aleatório é usado, as divisões de visitantes que você observa podem não ser exatamente 50-50; no entanto, a divisão será estatisticamente equivalente à porcentagem de divisão desejada.

Observe que, como parte da configuração de cada campanha com um experimento de conteúdo, você deve escolher um namespace de identidade a partir do qual a userId será selecionada para o algoritmo de aleatoriedade. Isso é independente dos [endereços de execução](../configuration/primary-email-addresses.md).

### Coleta e análise de dados

No momento da atribuição, ou seja, quando a mensagem é enviada em canais de saída, ou quando o usuário entra na campanha em canais de entrada, um &quot;registro de atribuição&quot; é registrado no conjunto de dados do sistema apropriado. Isso registrará a qual tratamento o usuário foi atribuído, juntamente com identificadores de experiência e campanha.

As métricas de objetivo podem ser agrupadas em duas classes principais:

* Métricas diretas, em que o usuário reage diretamente ao tratamento, por exemplo, abrir um email ou clicar em um link.
* Métricas indiretas ou de &quot;fundo de funil&quot;, que ocorrem após o usuário ter sido exposto ao tratamento.

Para métricas de objetivo direto em que o Adobe Journey Optimizer rastreia suas mensagens, os eventos de resposta dos usuários finais são automaticamente marcados com a campanha e os identificadores de tratamento, permitindo a associação direta da métrica de resposta a um tratamento. [Saiba mais sobre o rastreamento](../email/message-tracking.md).

![](assets/technote_2.png)

Para objetivos indiretos ou de &quot;fundo de funil&quot;, como compras, os eventos de resposta dos usuários finais não são marcados com identificadores de campanha e tratamento, ou seja, um evento de compra ocorre após a exposição a um tratamento, e não há associação direta dessa compra com uma atribuição de tratamento anterior. Para essas métricas, a Adobe associará o tratamento à parte inferior do evento de conversão de funil se:

* A identidade do usuário for a mesma no momento do evento de atribuição e conversão.
* A conversão acontece dentro de sete dias da atribuição do tratamento.

![](assets/technote_3.png)

O Adobe Journey Optimizer usa então métodos estatísticos avançados &quot;válidos a qualquer momento&quot; para interpretar esses dados brutos de relatórios, o que permite interpretar seus relatórios de experimentação. Para obter mais informações, consulte [esta página](../campaigns/experiment-calculations.md).

## Dicas para executar experimentos

Ao executar Experimentos, é importante seguir determinadas práticas recomendadas. Estas são algumas dicas para executar esses experimentos:

+++Isole as variáveis que você está tentando testar

Formule alguma hipótese que pretenda testar e restrinja essa hipótese ao menor número possível de alterações para determinar o que teve impacto para sua entrega.

Por exemplo, uma boa hipótese pode ser se a personalização em linhas de assunto do email direciona melhores taxas de abertura. No entanto, adicionar uma alteração no conteúdo da mensagem ou nas imagens pode resultar em uma conclusão confusa.
+++

+++Verifique se você está usando a métrica correta

Determine a métrica que você objetiva e se as alterações feitas podem ter algum impacto direto nessa métrica.

Por exemplo, é improvável que a alteração do conteúdo do corpo da mensagem afete as taxas de abertura de email.
+++

+++Execute o teste no tamanho correto do público ou por tempo suficiente

Se você executar seus testes por mais tempo, será possível detectar diferenças menores na métrica de meta entre os tratamentos. No entanto, se o valor da linha de base de sua métrica de meta for pequeno, você precisará de tamanhos de amostra maiores.
O número de usuários que devem ser incluídos em seu experimento depende do tamanho do efeito que você deseja detectar, da variação ou propagação de sua métrica de meta, bem como de sua tolerância para erros falsos positivos e falsos negativos. Em Experimentos clássicos, você pode usar uma [calculadora de tamanho da amostra](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=pt-BR){_blank} para determinar por quanto tempo deve executar o teste.
+++

+++Entender a incerteza estatística

Se você estiver executando um experimento em que 1.000 usuários viram um tratamento e a taxa de conversão é definida como 5%. Essa seria a taxa de conversão real se todos os seus usuários estivessem incluídos? Qual seria a taxa de conversão real?
Os métodos estatísticos nos fornecem uma maneira de formalizar essa incerteza. Um dos conceitos mais importantes a se entender ao executar experimentos online é que as taxas de conversão observadas são consistentes com uma gama de taxas de conversão verdadeiras subjacentes, o que significa que você deve esperar até que essas estimativas sejam precisas o suficiente, antes de tentar chegar a uma conclusão. Os Intervalos de confiança e Confiança nos ajudam a quantificar essa incerteza.
+++

+++Forme novas hipóteses e teste continuamente

Para obter insights de negócios verdadeiros, você deve se manter em apenas um Experimento. Em vez disso, acompanhe os experimentos formulando novas hipóteses e executando novos testes com alterações diferentes, em segmentos diferentes, e examinando o impacto nas diferentes métricas.
+++

## Interprete os resultados dos seus experimentos {#interpret-results}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_summary"
>title="Widget de resumo"
>abstract="O widget Resumo fornece uma visão geral dos resultados do experimento, incluindo se são conclusivos ou não. Ele oferece uma maneira rápida e fácil de entender o resultado do experimento."

![](assets/experimentation_report_3.png)

Esta seção descreve os relatórios de Experimento e como entender as várias quantidades estatísticas apresentadas.

Estas são algumas diretrizes para interpretar os resultados do seu Experimento de conteúdo.

Observe que uma descrição completa dos resultados deve considerar todas as evidências disponíveis (ou seja, tamanhos das amostras, taxas de conversão, intervalos de confiança etc.) e não apenas a declaração de conclusivo ou não. Mesmo quando um resultado ainda não é conclusivo, ainda pode haver provas convincentes de que um tratamento é diferente do outro.

Para entender os cálculos estatísticos, consulte esta [página](../campaigns/experiment-calculations.md).

### 1. Comparar métricas normalizadas {#normalized-metrics}

Ao comparar o desempenho de dois tratamentos, você deve sempre comparar as métricas normalizadas para levar em conta quaisquer diferenças no número de perfis expostos a cada tratamento.

Por exemplo, se o objetivo do experimento estiver definido como **[!UICONTROL Aberturas únicas]** e um determinado tratamento foi mostrado para 10.000 Perfis com 200 Aberturas únicas registradas, então isso representa uma **[!UICONTROL Taxa de conversão]** de 2%. Para métricas não exclusivas, por exemplo, métrica Aberturas, a métrica normalizada é mostrada como uma **[!UICONTROL Contagem por perfil]**, enquanto para métricas contínuas como Preço total, a métrica normalizada é mostrada como um **[!UICONTROL Total por Perfil]**.

### 2. Foco nos intervalos de confiança {#confidence-intervals}

Quando você executa experimentos em amostras de seus perfis, a taxa de conversão observada para um determinado tratamento representa uma estimativa da verdadeira taxa de conversão subjacente.

Por exemplo, se o Tratamento A tiver uma **[!UICONTROL Taxa de conversão]** de 3% enquanto que o Tratamento B tem uma **[!UICONTROL Taxa de conversão]** de 2%, o Tratamento A possui um melhor desempenho do que o Tratamento B? Para responder a isto, temos primeiro de quantificar a incerteza nestas taxas de conversão observadas.

Os Intervalos de confiança ajudam a quantificar o montante de incerteza nas taxas de conversão estimadas, mas intervalos de confiança mais amplos implicam mais incerteza. À medida que mais perfis forem adicionados ao experimento, os intervalos se tornarão menores, representando uma estimativa mais precisa. O intervalo de confiança representa uma gama de taxas de conversão compatíveis com os dados observados.

Se os intervalos de confiança para dois tratamentos mal se sobrepõem, isso significa que os dois tratamentos possuem taxas de conversão diferentes. Mas, se houver muita sobreposição entre os intervalos de confiança de dois tratamentos, então é mais provável que os dois tratamentos tenham a mesma taxa de conversão.

A Adobe usa intervalos de confiança válidos de 95% a qualquer momento, ou Sequências de confiança, o que significa que os resultados podem ser visualizados com segurança a qualquer momento durante o experimento.

### 3. Entenda o aumento {#understand-lift}

O resumo do relatório do Experimento mostra o **[!UICONTROL aumento em relação à linha de base]**, que é uma medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base. Para definir com precisão, é a diferença no desempenho entre um determinado tratamento e a linha de base, dividido pelo desempenho da linha de base expresso como uma porcentagem.

### 3. Compreenda a confiança {#understand-confidence}

Embora você deva se concentrar principalmente no **[!UICONTROL Intervalo de confiança]** para o desempenho de cada tratamento, a Adobe também mostra a Confiança, que é uma medida probabilística da quantidade de evidências de que um determinado tratamento é igual ao tratamento de linha de base. Uma confiança maior indica menos evidência para o pressuposto de que os tratamentos de linha de base e os que não são de linha de base têm desempenho igual. Mais precisamente, a confiança exibida é uma probabilidade (expressa como uma porcentagem) em que teríamos observado uma diferença menor nas taxas de conversão entre um determinado tratamento e a linha de base, se na realidade não houvesse diferença nas taxas de conversão subjacentes verdadeiras. Em termos de valores p, a confiança exibida é 1 - valor p.

A Adobe usa Confiança &quot;Válido a qualquer momento&quot; e valores p &quot;Válido a qualquer momento&quot; que são consistentes com as Sequências de Confiança descritas acima.

### 4. Significância estatística

Ao executar Experimentos, um resultado é considerado estatisticamente significativo se for muito improvável que tenha sido observado com uma hipótese nula de que um determinado tratamento e a linha de base têm taxas/desempenho de conversão subjacentes verdadeiros idênticos.

A Adobe declara um Experimento como conclusivo quando a Confiança estiver acima de 95%.

## O que fazer após executar um Experimento

Depois de executar seu Experimento, há várias ações de acompanhamento possíveis:

* **Implante ideias vencedoras**

   Com um resultado inequívoco, é possível implantar essa ideia vencedora, enviando o tratamento com melhor desempenho para todos os clientes ou criando novas campanhas nas quais a estrutura do tratamento com melhor desempenho é replicada.
   </br>Observe que em um ambiente dinâmico, o que funciona bem de uma vez, pode não funcionar bem mais tarde.

* **Executar testes de acompanhamento**

   Às vezes, os resultados de seus experimentos podem ser inconclusivos, seja porque não havia perfis suficientes incluídos para detectar qualquer diferença nos tratamentos, ou porque os tratamentos que você definiu não eram suficientemente diferentes.

   Se a hipótese que você estava testando ainda for relevante, executar um teste de acompanhamento em um público maior ou diferente, ou modificar seus tratamentos para que haja diferenças mais claras, pode ser a melhor ação de acompanhamento.

* **Fazer análises mais aprofundadas**

   O tratamento que funciona bem para um público pode, às vezes, não ser o melhor tratamento para outro público. Fazer análises mais aprofundadas sobre como os tratamentos se comportam para segmentos diferentes ajuda a gerar ideias para novos testes.

   Da mesma forma, estudar o desempenho de cada tratamento com métricas diferentes também pode oferecer uma visão mais abrangente dos seus Experimentos.

   >[!CAUTION]
   >
   >Mais análises significam maior chance de detectar um efeito espúrio ou falso positivo.
