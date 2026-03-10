---
solution: Journey Optimizer
product: Journey Optimizer
title: Monitoramento do modelo de IA
description: Monitorar a integridade do modelo de classificação de IA, o status do treinamento e o desempenho para modelos de otimização personalizados
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
version: Journey Orchestration
source-git-commit: e329c221fa714747d50495e466d02e75bed2967c
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 2%

---

# Monitore modelos de IA {#ai-model-observability}

Seja você um profissional de marketing, cientista de dados ou administrador de decisões, entender como seus modelos de otimização personalizados funcionam e se comportam ajuda a selecionar as melhores ofertas para cada cliente que usa IA.

Para fazer isso, você pode monitorar a integridade, o status do treinamento e a evolução dos modelos de IA diretamente no [!DNL Journey Optimizer].

Isso fornece uma visão clara sobre se seu modelo está funcionando, quando foi treinado pela última vez, o que aconteceu durante o treinamento, como ele está impulsionando seu resultado comercial (por exemplo, conversões ou receita) e solucionar problemas quando não está funcionando<!-- (for example, unexpected decision item count, training data date range, or insufficient events)-->.

>[!AVAILABILITY]
>
>Atualmente, esse recurso tem suporte apenas para [modelos de otimização personalizados](personalized-optimization-model.md).

➡️ [Conheça este recurso no vídeo](#video)

## Exibir o status do treinamento {#from-ai-model-list}

Depois que um modelo é definido para ficar ativo, ele entra em um ciclo de vida contínuo: os dados são coletados e o modelo é retreinado periodicamente para otimizar a classificação das ofertas. Você pode verificar o status do treinamento de seus modelos de otimização personalizados na lista de modelos de IA.

1. Acesse **[!UICONTROL Decisão]** > **[!UICONTROL Configuração de estratégia]** > **[!UICONTROL Modelos de IA]** para abrir o inventário de modelos de IA.

1. Você pode visualizar todos os modelos de IA disponíveis e os status deles.

1. Para cada modelo de IA do **[!UICONTROL Live]** do tipo de otimização personalizado, duas colunas permitem que você veja:
   * quando o último trabalho de treinamento foi executado (**[!UICONTROL Último treinamento]**) e
   * se cada modelo foi treinado com êxito ou não (**[!UICONTROL Resultado do treinamento]**).

   ![](../assets/ai-model-list-training.png)

   Isso permite identificar rapidamente os modelos que precisam de mais investigação ou solução de problemas.

## Acessar um relatório de status de modelo {#access-ai-model-details}

Clique em um modelo de IA de otimização personalizado na lista. A partir daí, você pode visualizar os elementos listados abaixo:

* **[!UICONTROL Modelo implantado no momento]** - Essa seção mostra o modelo implantado no momento, quando ele foi implantado, qual intervalo de datas de dados ele usa, quantos itens de decisão (ofertas) são incluídos e personalizados e a alocação de tráfego atual entre submodelos<!-- (random exploration, new offer booster?, contextual bandit, neural network)-->.

  ![](../assets/ai-model-deployed-model.png)

  Neste exemplo, o modelo foi treinado em cinco itens de decisão e tem tráfego suficiente para desenvolver previsões personalizadas para três dos itens de decisão. Os restantes dois itens de decisão são notificados aleatoriamente.

  Você também pode ver que o modelo está alocando atualmente 40% do tráfego para a rede neural personalizada, 40% do tráfego para o bandit contextual e 20% do tráfego para exploração aleatória.

* **[!UICONTROL Último trabalho de treinamento]** - Esta seção mostra o status do último trabalho de treinamento, quando ele foi executado e todas as mensagens de erro. [Saiba mais sobre estados de erro](#check-for-error-states)

  ![](../assets/ai-model-last-training-job.png)

  Neste exemplo, você pode observar que o modelo implantado corresponde ao trabalho de treinamento conforme esperado.

* **[!UICONTROL Propriedades]** - Esta seção mostra as propriedades do modelo, como o conjunto de dados usado, a métrica de otimização e os públicos-alvo usados para treinar o modelo de otimização personalizado.

  ![](../assets/ai-model-properties.png)

  Clique em **[!UICONTROL Editar propriedades]** para modificar esses elementos. Você será redirecionado para a tela Criar modelo de IA. [Saiba mais](create-ai-models.md)

* **[!DNL Model performance]** - Esta seção mostra o desempenho de cada braço do modelo ao longo do tempo, como a alocação de tráfego e a taxa de conversão para cada submodelo. Você pode alternar entre **últimos 7 dias** e **últimos 30 dias**. O incentivo e a significância estatística são os principais indicadores para determinar se o modelo está realmente melhorando o resultado de marketing.

  ![](../assets/ai-model-performance.png)

  Neste exemplo, você pode ver que, nos últimos 30 dias, os submodelos personalizados estão fornecendo mais de 60% de aumento na taxa de conversão, e esse aumento é estatisticamente significativo, o que significa que esse modelo de IA está causando um impacto para sua empresa.

* **[!UICONTROL Alocação de tráfego de modelo ao longo do tempo]** - Esta seção mostra como o modelo evoluiu ao longo do tempo. Quando um modelo é implantado pela primeira vez, 100% do tráfego é aleatório porque nenhum dado de oferta foi coletado ainda. Após o primeiro treinamento, o tráfego geralmente muda para os braços personalizados.

  ![](../assets/ai-model-trafic-allocation.png)

  Neste exemplo, você pode ver que a alocação de tráfego mudou de exploração aleatória de 100% para rede neural e tráfego de bandit contextual à medida que o modelo foi retreinado ao longo do tempo.

## Entender os erros de treinamento {#check-for-error-states}

Para exibir detalhes de erros de um modelo de IA de otimização personalizado cujo último trabalho de treinamento falhou, siga as etapas abaixo.

1. Clique no modelo da lista. Os detalhes de status do modelo são exibidos.

   ![](../assets/ai-model-no-model-deployed.png){width="95%"}

   Neste exemplo, você pode ver que nenhum modelo está implantado porque o último trabalho de treinamento falhou.

   >[!NOTE]
   >
   >Quando nenhum modelo é implantado, as solicitações de decisão são atendidas usando a alocação uniforme de tráfego aleatório.

1. Veja os detalhes do erro na seção **[!UICONTROL Último trabalho de treinamento]**.

   ![](../assets/ai-model-training-job-failed.png){width="70%"}

   Um trabalho de treinamento geralmente falha quando não há eventos de feedback no conjunto de dados selecionado para esse modelo. Isso significa que você precisa preencher o conjunto de dados ou selecionar um novo conjunto de dados com eventos de conversão apropriados.

1. Você pode verificar qual conjunto de dados está selecionado nas **[!UICONTROL Propriedades]** do modelo. Clique em **[!UICONTROL Editar propriedades]** para selecionar outro conjunto de dados. [Saiba mais](create-ai-models.md)

   ![](../assets/ai-model-properties-edit-dataset.png){align="left" width="45%"}

## Perguntas frequentes {#faq}

+++ Quais modelos de IA posso monitorar?

Atualmente, o monitoramento do modelo de IA é suportado apenas para [modelos de otimização personalizados](personalized-optimization-model.md). Outros tipos de modelo de classificação ainda não expõem o relatório de status do modelo.
+++

+++ Por que o trabalho de treinamento do meu modelo falhou?

Os trabalhos de treinamento geralmente falham quando o conjunto de dados selecionado para o modelo tem poucos eventos de feedback (conversão) ou nenhum deles. Verifique a seção **[!UICONTROL Último trabalho de treinamento]** para obter os detalhes do erro e revise as **[!UICONTROL Propriedades]** do modelo para confirmar o conjunto de dados e a métrica de otimização. Preencha o conjunto de dados com os eventos corretos ou [selecione um conjunto de dados diferente](create-ai-models.md) com os dados de conversão apropriados.
+++

+++ Como o monitoramento do modelo de IA está relacionado aos relatórios de campanha e jornada?

O monitoramento do modelo de IA é diferente dos relatórios de campanha ou jornada. Um único modelo de IA pode ser usado em várias campanhas ou jornadas, e os relatórios de campanha ou jornada não mostram qual modelo foi usado para um determinado delivery. Use o monitoramento do status do modelo de IA para entender e monitorar o próprio modelo; use [relatórios de campanha](../../reports/campaign-global-report-cja.md) e [relatórios de jornada](../../reports/journey-global-report-cja.md) para métricas no nível da entrega.
+++

+++ Minha métrica de otimização é uma métrica contínua, como receita ou valor de pedido, não uma métrica binária, como cliques ou conversões. Como interpreto as conversões e os valores de taxa de conversão reportados?

Ao usar uma métrica contínua como receita ou valor de pedido, o modelo tenta prever o valor estimado associado à apresentação de uma determinada oferta (não a probabilidade de conversão). O valor &quot;Conversões&quot; relatado é a receita total (ou valor do pedido) associada às exibições de oferta registradas para cada braço de modelo. O &quot;Índice de conversão&quot; relatado é o valor de Conversões dividido pelo valor Exibições e pode exceder 100% no caso de métrica contínua.
+++

+++ Qual é o significado do aumento?

A significância do aumento é a significância estatística do aumento relatado versus a exploração aleatória. A significância é calculada usando um teste qui-quadrado de diferenças de proporção, que fornece um resultado idêntico ao cálculo de significância de um teste Z para duas proporções de população.
+++

+++ Qual é o índice de Gini modelo? O que é um valor &quot;bom&quot; do índice Gini?

O modelo de índice de Gini (também conhecido como coeficiente de Gini) é uma medida offline da potência preditiva de um modelo. O índice de Gini do modelo varia de 0 (sem energia preditiva) a 1 (prevê perfeitamente a conversão ou o valor da métrica para cada oferta para cada cliente). Não há valor de índice Gini universal &quot;bom&quot;, pois casos de uso de decisão diferentes resultam em um comportamento de usuário diferente e, portanto, em resultados de modelo diferentes. No mesmo caso de uso, valores maiores do índice de Gini indicam um modelo de qualidade mais alta.
+++

+++ Como é calculado o índice de Gini?

O índice de Gini para cada braço de modelo é calculado de forma diferente, dependendo se a métrica de otimização é binária ou contínua:

**Métrica de otimização binária** (por exemplo, cliques, pedidos): o índice de Gini é calculado com base na área sob a curva (AUC) da curva ROC (Receiver-Operating Characteristics), normalmente chamada de AUC ROC ou simplesmente AUC. A AUC do ROC varia de 0,5 (modelo aleatório com potência preditiva zero) a 1,0 (potência preditiva perfeita). A AUC do ROC é convertida em índice de Gini usando a fórmula Gini = 2 x (AUC do ROC) - 1.

**Métrica de otimização contínua** (por exemplo, receita, valor de pedido): o índice Gini é calculado com base na área sob a curva de Lorenz associada aos positivos cumulativos previstos do modelo versus os positivos reais cumulativos na população. A área abaixo da curva de Lorenz varia de 0,0 (potência preditiva perfeita) a 0,5 (modelo aleatório com potência preditiva zero). A AUC de Lorenz é convertida em índice de Gini utilizando a fórmula Gini = 1 - 2 x (AUC de Lorenz).
+++

+++ Qual é a melhor medida de qualidade do modelo: Índice de Gini ou importância do aumento/aumento?

Normalmente, as medidas online de qualidade do modelo, como significância de elevação e elevação, são consideradas o método &quot;padrão ouro&quot; para medir a qualidade do modelo. Os índices de Gini fornecem um ponto de dados adicional para as equipes de ciência de dados do cliente que avaliam modelos de decisão.
+++

<!--
## Understanding statuses and errors {#statuses-errors}

* **Success** – The latest training job completed successfully. The model is trained and deployed for ranking.
* **Failed** – The latest training job failed (for example, no events in the datasets). The UI shows an error message and a request ID; use these when troubleshooting or contacting support.
* **In progress** – A training job is running. Some metrics may be temporarily unavailable until it finishes.
* **Pending** – No result yet (for example, model recently activated or settings recently changed).

If no model has been successfully deployed yet, the "currently deployed model" section and some performance fields will be empty or show the initial-state messaging.-->

## Vídeo tutorial {#video}

Saiba como monitorar modelos de classificação de IA e interpretar o status e o desempenho do treinamento no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3479854?captions=por_br&quality=12)

## Documentação relacionada {#related}

* [Sobre modelos de IA](ai-models.md)
* [Modelo de otimização personalizado](personalized-optimization-model.md)
* [Criar modelos de IA](create-ai-models.md)
* [Criar um conjunto de dados para coletar eventos](../data-collection/create-dataset.md)
