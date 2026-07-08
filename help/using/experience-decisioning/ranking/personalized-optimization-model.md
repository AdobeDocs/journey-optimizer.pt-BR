---
solution: Journey Optimizer
product: Journey Optimizer
title: Modelo de otimização personalizado
description: Entenda como o modelo de IA de otimização personalizada aprende com os dados do cliente e da oferta para classificar ofertas personalizadas e maximizar o KPI escolhido.
feature: Ranking, Decisioning
role: User
level: Experienced
exl-id: 1c7bcffe-5a25-444f-8a95-057b7a07f252
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ytq-DaCojPLwO0ReHyA6oYnAzepr02rthWrZwU-lehY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eb30f47f-d87a-400f-8f78-63ce7979ff56
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: d52c60bd4741153c42d7df9db43a5daf58ddf0d0
workflow-type: tm+mt
source-wordcount: 2297
ht-degree: 0%

---

# Modelo de otimização personalizado {#personalized-optimization-model}

>[!BEGINSHADEBOX]

**Nesta página:** entenda como o modelo de otimização personalizado usa o aprendizado de máquina para aprender com o cliente, a oferta e os dados contextuais, incluindo seus casos de uso, componentes do modelo de conjunto, requisitos do conjunto de dados, premissas e comportamento de inicialização imediata, para que você possa decidir quando usá-lo para fornecer ofertas personalizadas e maximizar seus KPIs.

>[!ENDSHADEBOX]

Ao aproveitar as tecnologias de ponta em aprendizagem de máquina e aprendizagem profunda supervisionadas, a otimização personalizada permite que um usuário empresarial (profissional de marketing) defina metas de negócios e utilize os dados de clientes para treinar modelos orientados a negócios a fim de fornecer ofertas personalizadas e maximizar KPIs.

Diferentemente da classificação não personalizada que é otimizada com base no desempenho global de cada oferta, a otimização personalizada aprende a relação entre os atributos de um cliente individual e as ofertas com maior probabilidade de direcionar o KPI escolhido para esse cliente. O resultado é uma seleção de ofertas personalizada para cada perfil em vez de uma única melhor oferta entregue a todos.

## Casos de uso e benefícios {#use-cases}

A otimização personalizada é adequada para cenários de decisão em que clientes diferentes respondem de forma diferente às ofertas disponíveis e em que o catálogo de ofertas é diferenciado de forma significativa e não é alterado com frequência. Casos de uso comuns incluem:

* **Seleção da próxima melhor oferta**: escolher qual das várias ofertas ou promoções concorrentes apresentar a cada cliente em tempo real.
* **Personalização de conteúdo**: escolha de qual parte do conteúdo (por exemplo, banner, criativo) ou mensagem para cada cliente na Web, celular, email e outros canais.
* **Personalização com reconhecimento de público-alvo**: incorporando associação de público-alvo e sinais contextuais para que as recomendações reflitam quem é o cliente e o contexto da interação.
* **Otimização de receita e valor**: otimizar em direção a resultados contínuos, como receita ou valor vitalício do cliente, além de resultados binários, como cliques e conversões.

Principais benefícios:

* Maximiza o KPI de negócios selecionado, disponibilizando a oferta para a qual cada cliente tem maior probabilidade de responder, em vez de uma única oferta globalmente ideal.
* Adapta-se continuamente à medida que chegam novos dados de interação, equilibrando a exploração de ofertas subtestadas com a exploração de executores comprovados.
* Suporta métricas de otimização binárias e contínuas, com pontuações de classificação que podem ser usadas diretamente em expressões do construtor de fórmulas de modelo de IA.
* Reduz o esforço manual de teste A/B e criação de regras, aprendendo o ajuste da oferta ao cliente automaticamente.

## Requisitos do conjunto de dados {#dataset}

Para treinar um modelo de otimização personalizado, o conjunto de dados deve ter pelo menos duas ofertas com pelo menos 250 eventos de exibição (por exemplo, impressões) e um evento bem-sucedido (por exemplo, clique ou conversão) nos últimos 30 dias.

Ofertas com menos de 250 eventos de exibição e/ou nenhum evento bem-sucedido nos últimos 30 dias permanecerão qualificadas para inclusão no tráfego de exploração. Eles também estarão qualificados para inclusão no tráfego de personalização, mas serão tratados como equivalentes à oferta prevista de pior pontuação na decisão, até que atendam aos eventos mínimos de exibição/sucesso necessários e o modelo seja retreinado.

Até a primeira vez que um modelo de otimização personalizado for treinado, as ofertas em uma estratégia de seleção que utilizam um modelo de otimização personalizado serão atendidas aleatoriamente.

## Como funciona {#how}

O modelo aprende interações de recursos complexos entre ofertas, informações dos usuários e informações contextuais para recomendar ofertas personalizadas aos usuários finais. Os recursos são entradas no modelo.

Há três tipos de recursos:

| Tipos de recursos | Como adicionar recursos aos modelos |
|--------------|----------------------------|
| Objetos de decisão (placementID, activityID, decisionScopeID) | Parte dos comentários da gestão de decisões que os eventos de experiência enviaram para a AEP |
| Públicos-alvo | De 0 a 50 públicos-alvo podem ser adicionados como recursos ao criar o modelo de IA de classificação |
| Dados de contexto | Parte dos Eventos de experiência de feedback de decisão enviados para a AEP. Dados de contexto disponíveis para adicionar ao esquema: Detalhes do Commerce, Detalhes do canal, Detalhes do aplicativo, Detalhes da Web, Detalhes do ambiente, Detalhes do dispositivo, placeContext |

O modelo tem duas fases:

* Na fase **treinamento de modelo offline**, um modelo é treinado ao aprender e memorizar interações de recursos em dados históricos.
* Na fase **inferência online**, as ofertas candidatas são classificadas com base nas pontuações em tempo real geradas pelo modelo. Ao contrário das técnicas tradicionais de filtragem colaborativa, com as quais é difícil incluir recursos para usuários e ofertas, a otimização personalizada é um método de recomendação baseado em deep learning, e é capaz de incluir e aprender padrões de interação de recursos complexos e não lineares.

O modelo oferece suporte à otimização de variáveis contínuas (como receita e valor vitalício do cliente), além de variáveis binárias (como cliques e conversões). Os valores previstos para uma métrica binária, como cliques, sempre estarão entre 0 e 1. Os valores previstos para uma métrica contínua, como valor de pedido, sempre serão um número maior ou igual a zero. As pontuações de classificação são normalizadas para garantir comportamento consistente em ambos os tipos de métricas quando usadas em fórmulas ou comparações.

## Exemplo ilustrativo {#illustrative-example}

### Resposta binária (conversão) {#binary-response}

Considere um conjunto de dados simplificado de interações históricas entre usuários e ofertas. Cada linha registra uma oferta exibida, dois sinais do cliente — nível de fidelidade (alto = 1) e se o cliente abriu um email recente (sim = 1) — e se o cliente converteu (sim = 1).

Para a Oferta A, a conversão é mais provável quando ambos os sinais estão de acordo (ambos altos ou baixos). Para a Oferta B, a conversão é mais provável quando o email foi aberto, independentemente do nível de fidelidade. Com base no padrão aprendido, o modelo pode prever a melhor oferta para cada cliente com base em seus sinais.

![Respostas de conversão binária para a Oferta A e a Oferta B com base nos sinais do cliente](../assets/perso-ranking-binary-response.png)

*Figura 1: na linha incompatível realçada, a Oferta A era exibida quando os sinais discordavam e não eram convertidos. Com base no padrão aprendido, a Oferta B seria a melhor recomendação para esse cliente da próxima vez.*

Essa é a essência da abordagem: aprender e memorizar interações de recursos históricos e aplicá-las para gerar previsões personalizadas para cada cliente.

### Resposta contínua (receita) {#continuous-response}

A mesma ideia se estende aos resultados contínuos. Em vez de prever se um cliente converte, o modelo prevê um valor contínuo (receita esperada) para cada oferta e segmento de cliente e classifica as ofertas por esse valor previsto.

![Receita prevista para duas ofertas em quatro segmentos de clientes](../assets/perso-ranking-continuous-response.png)

*Figura 2: receita prevista para duas ofertas em quatro segmentos de clientes. Para clientes de alta fidelidade que abriram o email, espera-se que a Oferta A gere mais receita; para clientes de baixa fidelidade que abriram o email, a Oferta B é a melhor opção. O modelo seleciona a oferta com o maior valor previsto para cada segmento, em vez de aplicar uma regra a todos os clientes.*

## Componentes do modelo de conjunto {#ensemble}

A otimização personalizada é fornecida como um modelo de conjunto — vários braços de modelo complementares são executados juntos e uma camada de supervisão decide quanto tráfego direto cada braço recebe. Esse design permite que o sistema persiga dois objetivos ao mesmo tempo: saber quais ofertas têm o melhor desempenho (exploração) e oferecer as ofertas com desempenho já conhecido (exploração).

**Balanceando a exploração**

Cada sistema de decisão enfrenta uma compensação entre explorar ofertas subtestadas para coletar informações e explorar ofertas comprovadas para maximizar o retorno imediato. Reservar muito pouco tráfego para exploração deixa ofertas de alto potencial desconhecidas; reservar muitos sacrifícios aumenta as ofertas que já estão em execução. O conjunto gerencia esse equilíbrio automaticamente, mantendo um piso mínimo de exploração enquanto desloca o tráfego restante para os braços personalizados de melhor desempenho ao longo do tempo.

O conjunto é composto por quatro braços de tráfego:

### Aleatório uniforme (braço de exploração) {#uniform-random}

O braço aleatório uniforme atribui ofertas a clientes aleatoriamente de entre as ofertas elegíveis. Como não favorece nenhuma oferta, produz dados imparciais sobre como os clientes respondem em todo o catálogo — a matéria-prima com a qual as armas personalizadas aprendem. É o único braço ativo antes do primeiro modelo ser treinado, e depois ele continua a manter um piso de exploração mínimo para que o sistema continue aprendendo.

* Na inicialização: 100% do tráfego.
* Após a primeira execução de treinamento bem-sucedida: um mínimo de 5 a 20% de tráfego dependendo do número de eventos de impressão e conversão observados por oferta, até um máximo de 85%.

### Rede neural (braço personalizado) {#neural-network}

A rede neural é um braço personalizado que prevê a melhor oferta para um determinado cliente com base em seus atributos e associações de público-alvo. Ele aprende interações complexas e não lineares entre ofertas, recursos do cliente e contexto, e é bem adequado para capturar padrões sutis em vários recursos.

* Na inicialização: 0% do tráfego.
* Após a primeira execução de treinamento bem-sucedida: um mínimo de 5% de tráfego, até um máximo de 85%.

### Bandit contextual (braço personalizado) {#contextual-bandit}

O bandit contextual é um segundo braço personalizado que também prevê a melhor oferta para cada cliente com base em suas associações de público, usando uma abordagem de bandit que equilibra continuamente o aprendizado e o desempenho à medida que ele serve. Executá-lo ao lado da rede neural permite que o conjunto se baseie nas forças de dois métodos personalizados distintos.

* Na inicialização: 0% do tráfego.
* Após a primeira execução de treinamento bem-sucedida: um mínimo de 5% de tráfego, até um máximo de 85%.

### Novo booster de oferta (braço não personalizado) {#new-offer-booster}

O novo impulsionador de ofertas é um bandido Thompson Sampling vencedor geral (não personalizado) que faz suposições otimistas sobre o desempenho de novas ofertas — aquelas com poucos eventos de impressão registrados dentro do período de retrospectiva do modelo. Isso dá às novas ofertas promissoras a exposição antecipada de que precisam para provar a si mesmas, abordando uma deficiência conhecida de início frio em que o modelo, de outra forma, lutava para direcionar tráfego suficiente para ofertas novas ou de alto desempenho, mas restritivamente elegíveis.

* À medida que dados de impressão e conversão verdadeiros são coletados, o desempenho estimado de cada oferta se aproxima rapidamente de seu verdadeiro desempenho subjacente, e o impacto dos pressupostos otimistas cai para quase zero.
* Quando nenhuma oferta é relativamente nova — por exemplo, quando todas as ofertas têm um número semelhante de impressões ou todas têm mais de 1.000 impressões — o efeito otimista é próximo de zero e esse braço se comporta, de fato, como um modelo não personalizado de vencedor geral.
* Na inicialização: 0% do tráfego.
* Após a primeira execução bem-sucedida do treinamento: 5% do tráfego.

### Como o tráfego é alocado entre os braços {#traffic-allocation}

Na inicialização, nenhum modelo foi treinado ainda, portanto, 100% do tráfego vai para a linha de base aleatória uniforme — o único braço com uma distribuição aprendida da qual obter uma amostra. Após a primeira execução bem-sucedida do treinamento, cada braço recebe um mínimo de tráfego (5%) e o bandit de supervisão aloca o tráfego restante com base no desempenho observado. À medida que o modelo treina em rodadas sucessivas, o tráfego converge para os braços de maior desempenho com uma alocação máxima possível de 85% de tráfego.

![Alocação de tráfego entre os quatro braços do conjunto em sucessivas rodadas de treinamento](../assets/perso-ranking-traffic-allocation.png)

*Figura 3: uma possível trajetória de alocação de tráfego entre os quatro braços do conjunto na inicialização e em rodadas de treinamento sucessivas. Na inicialização, todo o tráfego flui para a linha de base aleatória. Após cada execução de treinamento, o supervisor Thompson Sampling bandit muda a alocação para braços com melhor desempenho, mantendo no mínimo 5% de tráfego. A alocação real varia de acordo com o desempenho do braço observado.*

## Principais premissas e limitações do modelo {#key}

Para maximizar a vantagem de usar a otimização personalizada, há algumas suposições e limitações importantes a serem observadas.

* **As ofertas são diferentes o suficiente para que os usuários tenham preferências diferentes entre as ofertas em consideração**. Se as ofertas forem muito semelhantes, um modelo resultante terá menos impacto, pois as respostas são aparentemente aleatórias.Por exemplo, se um banco tiver duas ofertas de cartões de crédito com a única diferença sendo a cor, pode não importar qual cartão é recomendado, mas se cada cartão tiver termos diferentes, isso fornece uma explicação para por que determinados clientes escolheriam um e forneceriam diferença suficiente entre as ofertas para criar um modelo mais impactante.
* **A composição do tráfego de usuário está estável**. Se a composição do tráfego do usuário mudar drasticamente durante o treinamento e a previsão do modelo, o desempenho do modelo poderá diminuir. Por exemplo, suponha que, na fase de treinamento do modelo, apenas os dados para usuários no público-alvo A estejam disponíveis, mas o modelo treinado seja usado para gerar previsões para usuários no público-alvo B, então o desempenho do modelo pode ser afetado.
* **O desempenho das ofertas não é alterado drasticamente em um curto período**, pois esse modelo é atualizado semanalmente e as alterações no desempenho são transmitidas como as atualizações do modelo. Por exemplo, um produto era muito popular antes, mas um relatório público identifica o produto como prejudicial à nossa saúde, e esse produto se torna impopular extremamente rápido. Nesse cenário, o modelo pode continuar a prever esse produto até que o modelo seja atualizado com alterações no comportamento do usuário.

## Problema de inicialização a frio {#cold-start}

Problemas de inicialização a frio ocorrem quando não há dados suficientes para fazer recomendações. Para otimização personalizada, há quatro tipos de problemas de inicialização a frio.

* **Depois de criar um novo modelo de IA sem dados históricos**, as ofertas serão fornecidas aleatoriamente por um período para coletar os dados necessários, que serão usados para treinar o primeiro modelo.
* **Depois que o primeiro modelo de IA for lançado**, uma parte do tráfego total será alocada para exploração aleatória uniforme, enquanto o restante será usado para recomendações de modelo. A distribuição do tráfego nos componentes de exploração e exploração do bandit é ajustada automaticamente com base em fatores como o número de ofertas e seus limites de desempenho.
* **Depois que novas ofertas forem adicionadas à coleção de ofertas** selecionada na estratégia associada ao modelo de classificação de IA, essas ofertas se tornarão candidatas à exploração pelos braços do modelo de reforço de oferta uniforme aleatório e novo (em 60 minutos). Durante a próxima execução de novo treinamento agendada, o desempenho estimado da oferta será atualizado no novo braço do modelo de reforço da oferta e a oferta se tornará qualificada para inclusão nos braços do modelo personalizado se atender à impressão e ao limite de cliques.
* **Depois que novos perfis são adicionados ao conjunto de públicos-alvo existente** associado à estratégia de seleção associada ao modelo de classificação de IA, eles herdam atributos de personalização do próprio conjunto de públicos-alvo. Assim, eles começarão a receber ofertas personalizadas com base nesses atributos desde o início, sem nenhum problema de inicialização imediata.

## Retreinamento {#re-training}

Os modelos serão treinados novamente para aprender as interações de recursos mais recentes e atenuar a degradação do desempenho do modelo semanalmente. Para monitorar o status do treinamento e o desempenho do modelo, consulte [Monitoramento do modelo de IA](ai-model-observability.md).
