---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao experimento de conteúdo
description: Saiba mais sobre o experimento de conteúdo no Journey Optimizer
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: introdução, início, conteúdo, experimento
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '2013'
ht-degree: 2%

---

# Introdução a experimentos de conteúdo {#get-started-experiment}

>[!BEGINSHADEBOX]

O que você encontrará nesta documentação:

* **[Introdução ao experimento de conteúdo](get-started-experiment.md)**
* [Criar um experimento de conteúdo](content-experiment.md)
* [Compreender cálculos estatísticos](experiment-calculations.md)
* [Configurar relatórios de experimentação](reporting-configuration.md)
* [Cálculos estatísticos no relatório de Experimentação](experiment-report-calculations.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>No momento, o recurso Experimento de conteúdo está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.

## O que é um experimento de conteúdo?

Experimentos de conteúdo permitem otimizar o conteúdo para as ações em suas Campanhas.

Os experimentos são um conjunto de testes aleatórios, o que, no contexto de testes online, significa que alguns usuários selecionados aleatoriamente são expostos a uma determinada variação de uma mensagem e outro conjunto de usuários selecionado aleatoriamente a outro tratamento. Após enviar a mensagem, você pode medir as métricas de resultado em que está interessado, por exemplo, abertura de emails ou cliques.

## Por que executar experimentos?

![](assets/content_experiment_schema.png)

Experimentos permitem isolar as alterações que resultam em melhorias nas métricas. Como ilustrado na imagem acima: alguns usuários selecionados aleatoriamente são expostos a cada grupo de tratamento, o que significa que, em média, os grupos compartilharão as mesmas características. Assim, qualquer diferença nos resultados pode ser interpretada como sendo devido às diferenças nos tratamentos recebidos, ou seja, você é capaz de estabelecer uma relação causal entre as alterações que você fez e os resultados em que você está interessado.

Isso permite tomar decisões orientadas por dados na otimização de suas metas de negócios.

Para experimentos de conteúdo no Adobe Journey Optimizer, você pode testar ideias como:

* **Linha de assunto**: Qual pode ser o impacto de uma alteração no tom ou no grau de personalização de uma linha de assunto?
* **Conteúdo da mensagem**: a alteração do layout visual de um email resultará em mais cliques no email?

## Como funciona o experimento de conteúdo? {#content-experiment-work}

### Atribuição aleatória

A experimentação de conteúdo no Adobe Journey Optimizer usa um hash pseudo-aleatório da identidade do visitante para executar a atribuição aleatória de usuários no público-alvo para um dos tratamentos definidos. O mecanismo de hash garante que, em cenários em que o visitante entra em uma campanha várias vezes, ele receberá deterministicamente o mesmo tratamento.

Em detalhes, o algoritmo MumurHash3 de 32 bits é usado para executar o hash da string de identidade do usuário em um dos 10.000 buckets. Em um experimento de conteúdo com 50% do tráfego atribuído a cada tratamento, os usuários que caírem em compartimentos de 1 a 5.000 receberão o primeiro tratamento, enquanto os usuários nos compartimentos de 5.001 a 10.000 receberão o segundo tratamento. Como o hash pseudo-aleatório é usado, as divisões de visitante observadas podem não ser exatamente 50-50; no entanto, a divisão será estatisticamente equivalente à porcentagem de divisão de destino.

Observe que, como parte da configuração de cada campanha com um experimento de conteúdo, você deve escolher um namespace de identidade do qual a userId será selecionada para o algoritmo de aleatoriedade. Isso é independente do [endereços de execução](../configuration/primary-email-addresses.md).

### Coleta e análise de dados

No momento da atribuição, ou seja, quando a mensagem é enviada em canais de saída ou quando o usuário insere a campanha em canais de entrada, um &quot;registro de atribuição&quot; é registrado no conjunto de dados do sistema apropriado. Isso registrará a qual tratamento o usuário foi atribuído, juntamente com identificadores de experimento e campanha.

As métricas de objetivo podem ser agrupadas em duas classes principais:

* Métricas diretas, em que o usuário reage diretamente ao tratamento; por exemplo, ao abrir um email ou clicar em um link.
* Métricas indiretas ou &quot;parte inferior do funil&quot;, que acontecem após o usuário ser exposto ao tratamento.

Para métricas de objetivo direto nas quais o Adobe Journey Optimizer rastreia suas mensagens, os eventos de resposta dos usuários finais são marcados automaticamente com os identificadores de campanha e tratamento, permitindo a associação direta da métrica de resposta a um tratamento. [Saiba mais sobre rastreamento](../email/message-tracking.md).

![](assets/technote_2.png)

Para objetivos indiretos ou de &quot;fundo de funil&quot;, como compras, os eventos de resposta dos usuários finais não são marcados com identificadores de campanha e tratamento, ou seja, um evento de compra ocorre após a exposição a um tratamento, não há associação direta dessa compra com uma atribuição de tratamento anterior. Para essas métricas, o Adobe associará o tratamento à parte inferior do evento de conversão de funil se:

* A identidade do usuário é a mesma na atribuição e no tempo do evento de conversão.
* A conversão ocorre dentro de sete dias da atribuição do tratamento.

![](assets/technote_3.png)

O Adobe Journey Optimizer usa métodos estatísticos avançados &quot;válidos a qualquer momento&quot; para interpretar esses dados brutos de relatório, o que permite interpretar os relatórios de experimentação. Para obter mais informações, consulte [esta página](../campaigns/experiment-calculations.md).

## Dicas para executar experimentos

Ao executar experimentos, é importante seguir determinadas práticas recomendadas. Estas são algumas dicas para executar esses experimentos:

+++Isole as variáveis que você está tentando testar

Formule alguma hipótese que você pretende testar e restrinja-a ao menor número de alterações possível para determinar o que causou impacto em seu delivery.

Por exemplo, uma boa hipótese pode ser se a personalização nas linhas de assunto do email direciona melhores taxas de abertura. No entanto, também adicionar uma alteração no conteúdo da mensagem ou nas imagens pode resultar em uma conclusão confusa.
+++

+++Verifique se você está usando a métrica correta

Determine a métrica que deseja direcionar e se as alterações que está fazendo podem ter algum impacto direto nessa métrica.

Por exemplo, é improvável que a alteração do conteúdo do corpo da mensagem afete as taxas de abertura de email.
+++

+++Execute seu teste no tamanho correto do público ou por tempo suficiente

Se você executar seus testes por mais tempo, será capaz de detectar diferenças menores na métrica de meta entre tratamentos. No entanto, se o valor da linha de base da sua métrica de meta for pequeno, você precisará de amostras maiores.
O número de usuários que devem ser incluídos no experimento depende do tamanho do efeito que você deseja detectar, da variação ou propagação da métrica de objetivo, bem como da sua tolerância para erros falso-positivos e falso-negativos. Em Experimentos clássicos, você pode usar um [calculadora de tamanho de amostra](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=pt-BR){_blank} para determinar por quanto tempo você deve executar seu teste.
+++

+++Compreenda a incerteza estatística

Se você estiver executando um experimento em que 1000 usuários viram um tratamento e a taxa de conversão estiver definida como 5%. Esse seria o índice de conversão real se todos os usuários fossem incluídos? Qual seria a verdadeira taxa de conversão?
Métodos estatísticos nos dão uma forma de formalizar essa incerteza. Um dos conceitos mais importantes para entender ao executar experimentos on-line é que as taxas de conversão observadas são consistentes com uma variedade de taxas de conversão verdadeiras subjacentes, o que significa que você deve esperar até que essas estimativas sejam precisas o suficiente antes de tentar tirar uma conclusão. Intervalos de confiança e confiança nos ajudam a quantificar essa incerteza.
+++

+++Forme novas hipóteses e teste continuamente

Para obter insights comerciais verdadeiros, você deve se ater a apenas um Experimento. Em vez disso, acompanhe experimentos formulando novas hipóteses e executando novos testes com alterações diferentes, em segmentos diferentes e examinando o impacto nas diferentes métricas.
+++

## Interpretar os resultados dos seus experimentos {#interpret-results}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_summary"
>title="Widget de Resumo"
>abstract="O widget Resumo fornece uma visão geral dos resultados do experimento, incluindo se são conclusivos ou não. Ele oferece uma maneira rápida e fácil de entender o resultado do seu experimento."

![](assets/experimentation_report_3.png)

Esta seção descreve os relatórios de Experimento e como entender as várias quantidades estatísticas apresentadas.

Estas são algumas diretrizes para interpretar os resultados do seu experimento de conteúdo.

Observe que uma descrição completa dos resultados deve considerar todas as evidências disponíveis (ou seja, tamanhos de amostra, taxas de conversão, intervalos de confiança etc.) e não apenas a declaração de conclusivo ou não. Mesmo quando um resultado ainda não é conclusivo, ainda pode haver evidências convincentes de que um tratamento seja diferente de outro.

Para entender cálculos estatísticos, consulte esta [página](../campaigns/experiment-calculations.md).

### 1. Comparar métricas normalizadas {#normalized-metrics}

Ao comparar o desempenho de dois tratamentos, você sempre deve comparar as métricas normalizadas para levar em conta quaisquer diferenças no número de perfis expostos a cada tratamento.

Por exemplo, se o objetivo do experimento estiver definido como **[!UICONTROL Aberturas únicas]**, e um determinado tratamento foi mostrado a 10.000 perfis com 200 aberturas únicas registradas, isso representa um **[!UICONTROL Índice de conversão]** 2%. Para métricas não exclusivas, por exemplo, Abrir métrica, a métrica normalizada é mostrada como uma **[!UICONTROL Contagem por perfil]**, enquanto para métricas contínuas como Preço total, a métrica normalizada é mostrada como um **[!UICONTROL Total por perfil]**.

### 2. Foco nos intervalos de confiança {#confidence-intervals}

Quando você executa experimentos em amostras de seus perfis, a taxa de conversão observada para um determinado tratamento representa uma estimativa da verdadeira taxa de conversão subjacente.

Por exemplo, se o Tratamento A tiver um **[!UICONTROL Índice de conversão]** de 3%, enquanto o tratamento B tem uma **[!UICONTROL Índice de conversão]** de 2%, o Tratamento A tem melhor desempenho que o Tratamento B? Para responder a isto, devemos primeiro quantificar a incerteza destas taxas de conversão observadas.

Os intervalos de confiança ajudam a quantificar a quantidade de incerteza nas taxas de conversão estimadas, mas intervalos de confiança mais amplos implicam mais incerteza. À medida que mais perfis são adicionados ao experimento, os intervalos se tornam menores, representando uma estimativa mais precisa. O intervalo de confiança representa um intervalo de taxas de conversão compatíveis com os dados observados.

Se os intervalos de confiança para dois tratamentos se sobrepõem com dificuldade, isso significa que os dois tratamentos têm taxas de conversão diferentes. Mas, se houver muita sobreposição entre os intervalos de confiança para dois tratamentos, então é mais provável que os dois tratamentos tenham a mesma taxa de conversão.

O Adobe usa 95% de Intervalos de confiança válidos a qualquer momento ou Sequências de confiança, o que significa que os resultados podem ser visualizados com segurança a qualquer momento durante o experimento.

### 3. Entender o aumento {#understand-lift}

O resumo do relatório de Experimento mostra as **[!UICONTROL Aumento sobre a linha de base]**, que é uma medida da melhora percentual na taxa de conversão de um determinado tratamento em relação à linha de base. Para definir com precisão, é a diferença no desempenho entre um determinado tratamento e a linha de base, dividida pelo desempenho da linha de base expresso como uma porcentagem.

### 3. Compreender a confiança {#understand-confidence}

Embora você deva se concentrar principalmente no **[!UICONTROL Intervalo de confiança]** para o desempenho de cada tratamento, Adobe também mostra a Confiança, que é uma medida probabilística de quanta evidência existe de que um determinado tratamento é o mesmo que o tratamento de linha de base. Uma maior confiança indica menos evidência para o pressuposto de que os tratamentos basais e não basais têm desempenho igual. Mais precisamente, a confiança exibida é uma probabilidade (expressa como uma porcentagem) que teríamos observado uma diferença menor nos índices de conversão entre um determinado tratamento e a linha de base, se na realidade não houver diferença nos verdadeiros índices de conversão subjacentes. Em termos de valores-p, a confiança exibida é de 1 - valor-p.

O Adobe usa os valores de p &quot;Validável a qualquer momento&quot; e &quot;Válido a qualquer momento&quot; que são consistentes com as Sequências de confiança descritas acima.

### 4. Significância estatística

Ao executar experimentos, um resultado é considerado estatisticamente significativo se for muito improvável que seja observado, dada a hipótese nula de que um determinado tratamento e a linha de base têm taxas/desempenho de conversão verdadeiros idênticos.

O Adobe declara que um experimento é conclusivo quando a Confiança está acima de 95%.

## O que fazer depois de executar um experimento

Depois de executar o experimento, há várias ações de acompanhamento possíveis:

* **Implantar ideias vencedoras**

   Com um resultado inequívoco, é possível implantar essa ideia vencedora, enviando o tratamento com melhor desempenho para todos os clientes ou criando novas campanhas onde a estrutura do tratamento com melhor desempenho é replicada.
   </br>Observe que, em um ambiente dinâmico, o que funciona bem de uma vez pode não funcionar bem posteriormente.

* **Executar testes de acompanhamento**

   Às vezes, os resultados dos seus experimentos podem ser inconclusivos, seja porque não houve perfis suficientes incluídos para detectar qualquer diferença nos tratamentos, ou porque os tratamentos que você definiu não foram suficientemente diferentes.

   Se a hipótese que você estava testando ainda for relevante, executar um teste de acompanhamento em um público-alvo maior ou diferente, ou modificar os tratamentos para que haja diferenças mais claras, pode ser a melhor ação de acompanhamento.

* **Fazer análises mais detalhadas**

   O tratamento que funciona bem para um público às vezes pode não ser o melhor tratamento para outro público. Fazer análises mais profundas sobre como os tratamentos se comportaram para segmentos diferentes ajuda a gerar ideias para novos testes.

   Da mesma forma, estudar o desempenho de cada tratamento com métricas diferentes também pode fornecer uma visualização mais abrangente dos Experimentos.

   >[!CAUTION]
   >
   >Mais análises significam maior chance de detectar um efeito espúrio ou falso positivo.
