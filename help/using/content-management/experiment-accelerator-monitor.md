---
solution: Journey Optimizer
product: journey optimizer
title: Monitor do Experimentation Accelerator
description: Melhore sua capacidade de conduzir experimentos com eficiência e gerar insights
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: conteúdo, experimento, vários, público-alvo, tratamento
hide: true
hidefromtoc: true
source-git-commit: c28a322ec13de2a23ab5cffb4785b14425e4e6e9
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 1%

---

# Acompanhe seus experimentos {#monitor}

>[!BEGINSHADEBOX]

* [Introdução à Experimentation Accelerator](experiment-accelerator.md)
* [Uso de dados na IA com o Experimentation Accelerator](experiment-accelerator-security.md)
* [Práticas recomendadas do Experimentation Accelerator](experiment-accelerator-best-practices.md)
* **[Monitorar experimentos](experiment-accelerator-monitor.md)**
* [Métricas de experimentação](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

A guia **[!UICONTROL Experimentos]** centraliza o rastreamento e a análise de testes do Adobe Journey Optimizer e do Adobe Target. Você pode exibir todos os experimentos, revisar KPIs e filtrar ou pesquisar para localizar testes específicos.

## Painel {#dashboard}

Ao acessar a guia Experimentos, todos os experimentos disponíveis do Journey Optimizer e do Adobe Target são listados em uma exibição consolidada. Isso permite revisar e comparar experimentos rapidamente em ambas as plataformas em um único local.
A lista de Experimentos inclui:

* Experimentos do Journey Optimizer criados em Campanhas ou Jornadas.

* Experimentos do Adobe Target disponíveis na sandbox padrão de produção do Journey Optimizer vinculada à mesma organização IMS.

A seção KPI fornece métricas principais, incluindo o número total de experimentos criados e o número atualmente em andamento, oferecendo um instantâneo da atividade geral de experimentação

Acesse filtros clicando em ![](assets/do-not-localize/Smock_Filter_18_N.svg), que oferece opções específicas de contexto, como filtragem por **[!UICONTROL Tipo]**, **[!UICONTROL Iniciado]**, **[!UICONTROL Status]** ou **[!UICONTROL Source]**. Por exemplo, você pode filtrar para mostrar somente experimentos ativos do Journey Optimizer.

Como alternativa, localize rapidamente o experimento digitando o nome na barra de pesquisa.

![](assets/experiment-monitor-dashboard.png)

## Monitore seus experimentos {#monitor-page}

Para acessar e monitorar seus experimentos, selecione o experimento configurado anteriormente na lista de experimentos da guia **[!UICONTROL Experimentos]** ou use o menu avançado para **[!UICONTROL Exibir detalhes]** ou **[!UICONTROL Abrir na origem]**.

![](assets/experiment-accelerator-1.png)

A página de detalhes do experimento está dividida na seguinte seção:

* [Resultado do experimento](#experiment-outcome)
* [Hipótese](#hypothesis)
* [Detalhes](#details)
* [Oportunidades](#opportunities)
* [Resultados](#results)
* [Insights de experimentação](#insights)

### Resultado do experimento {#experiment-outcome}

![](assets/experiment-monitor-outcome.png)

O **[!UICONTROL resultado do experimento]** fornece uma visão rápida da variação vencedora no seu experimento.

### Configuração {#set-up}

A **[!UICONTROL Hipótese]** captura as alterações planejadas a serem testadas e documenta o impacto esperado na métrica primária. Definir uma **[!UICONTROL Hipótese]** clara garante que cada experimento tenha um objetivo mensurável, tornando mais fácil avaliar os resultados e determinar se as alterações levam a melhorias significativas.

Observe que para que os [insights do experimento](#insights) sejam gerados, é necessário confirmar os detalhes da hipótese e do tratamento e a significância estatística a ser atingida.

1. Clique em **[!UICONTROL Adicionar]** para criar uma **[!UICONTROL Hipótese]** para seu experimento.

   ![](assets/experiment-monitor-setup-1.png)

1. Digite sua **[!UICONTROL Hipótese]** detalhando as alterações feitas e como elas afetarão a métrica primária.

   Clique em **[!UICONTROL Salvar]**.

1. Clique em **[!UICONTROL Revisar]** para adicionar ou substituir a imagem para cada Tratamento.

   ![](assets/experiment-monitor-setup-2.png)

1. As imagens de tratamento são geradas automaticamente, mas se necessário, você pode selecionar **[!UICONTROL Adicionar imagem]** ou **[!UICONTROL Substituir imagem]** para carregar uma captura de tela preferencial de seus arquivos locais para seus **[!UICONTROL Tratamentos]**.

   Observe que a captura de tela deve capturar a página inteira.

1. Clique no ícone ![](assets/do-not-localize/Smock_Edit_18_N.svg) para atualizar sua **[!UICONTROL Hipótese]**, se necessário.

Depois de concluir a configuração da **[!UICONTROL Hipótese]**, você precisará obter [Insights](#insights) e [Oportunidades](#opportunities) valiosos.

### Detalhes {#details}

![](assets/experiment-monitor-details.png)

O widget **[!UICONTROL Efeito do experimento]** fornece uma visão detalhada de como seu experimento influenciou os segmentos de público-alvo direcionados. Ele apresenta os principais indicadores de desempenho que ajudam a avaliar o engajamento e o comportamento, incluindo:

* **[!UICONTROL Métrica de sucesso]** da Journey Optimizer ou a **[!UICONTROL métrica primária]** da Adobe Target, dependendo do que foi configurado durante a criação do experimento.

* **[!UICONTROL Visitantes]**: o número total de visitantes únicos expostos ao experimento.

Você também pode ver um instantâneo em tempo real do desempenho do tratamento líder por meio das seguintes métricas:

* **[!UICONTROL Líder Atual]**: identifica o tratamento que atualmente oferece o melhor desempenho.

* **[!UICONTROL Aumento sobre a Linha de Base]**: mede a melhora da porcentagem do tratamento líder em comparação ao controle ou à linha de base.

* **[!UICONTROL Métrica de sucesso]** da Journey Optimizer ou a **[!UICONTROL métrica primária]** da Adobe Target, dependendo do que foi configurado durante a criação do experimento.

Na parte inferior do widget, você pode encontrar um resumo da sua configuração de experimento, incluindo:

* **[!UICONTROL Métrica de sucesso]** da Journey Optimizer ou a **[!UICONTROL métrica primária]** da Adobe Target, dependendo do que foi configurado durante a criação do experimento.

* **[!UICONTROL Número de Tratamentos]**: o número total de variações testadas.

* **[!UICONTROL Público-alvo]**: os segmentos de usuários definidos direcionados durante o experimento.

### Oportunidades {#opportunities}

>[!AVAILABILITY]
>
>O recurso Oportunidades é limitado a experimentos com alterações baseadas em texto.

O painel **[!UICONTROL Oportunidades]** exibe recomendações geradas por IA projetadas para aprimorar o desempenho do teste e alinhar-se a objetivos de negócios mais amplos e KPIs.

Observe que para que as oportunidades de Experimento sejam geradas, primeiro é necessário [confirmar a hipótese e os detalhes de tratamento](#set-up).

1. Navegue pela oportunidade sugerida e clique em **[!UICONTROL Exibir oportunidade]**.

   ![](assets/experiment-monitor-opportunities.png)

1. Selecionar uma oportunidade abre a janela **Detalhes da oportunidade**, que descreve um tratamento ou variação específica sugerida pela Experimentation Accelerator. Essa visualização inclui:

   * **[!UICONTROL Hipótese]**: uma hipótese gerada por IA que explica o resultado esperado do tratamento sugerido.

   * **[!UICONTROL Razão]**: uma explicação de por que a Experimentation Accelerator sugeriu esta oportunidade.

   * **[!UICONTROL Avaliação da oportunidade]**: uma avaliação dupla da recomendação com base em:

      * **[!UICONTROL Potencial de aprendizado]**: uma estimativa de quanto novo insight a oportunidade pode oferecer, com base no quão diferente é do que foi testado anteriormente.

      * **[!UICONTROL Potencial de conversão]**: uma estimativa da probabilidade da oportunidade de superar os tratamentos atuais, com base em semelhanças com estratégias que historicamente têm funcionado bem.
   <!--
   * **[!UICONTROL New text treatment example]**: Words or phrases that demonstrate the style the AI recommends using.
   -->

   ![](assets/experiment-monitor-opportunities-2.png)

1. Você pode adicioná-lo diretamente ao seu experimento selecionando **[!UICONTROL Abrir experimento]**.

1. Se o experimento original foi criado e gerenciado no Adobe Journey Optimizer, esta ação abrirá o **[!UICONTROL Painel de experimentação de conteúdo]** dentro dessa campanha.

   Para experimentos originados de **[!DNL Adobe Target]**, as alterações sugeridas serão carregadas no fluxo de trabalho de experimentação de **[!DNL Adobe Target]**.

   ➡️ [Saiba mais na documentação do Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/activities/abtest/test-ab)

1. Na exibição de experimento, as mesmas **[!UICONTROL Oportunidades de experimentação]** da IA apresentadas pela Experimentation Accelerator são acessíveis.

   Selecione **[!UICONTROL Exibir]** para abrir os detalhes da oportunidade.

1. Para aplicar as alterações sugeridas, selecionar **[!UICONTROL Modificar Experimento]** permite a edição direta do experimento existente.

### Resultados {#results}

![](assets/experiment-monitor-results.png)

A tabela **[!UICONTROL Resultados]** fornece uma análise detalhada do desempenho de cada tratamento de um experimento. Esses indicadores ajudam a avaliar a eficácia, o engajamento do usuário e o impacto geral nos principais resultados de negócios:

* **[!UICONTROL Local]**: posição de classificação do tratamento com base no desempenho, indicando como ele se compara a outros tratamentos.

* **[!UICONTROL Métrica de sucesso]** da Journey Optimizer ou a **[!UICONTROL métrica primária]** da Adobe Target, dependendo do que foi configurado durante a criação do experimento.

* **[!UICONTROL Pessoas]**: número de perfis de usuário qualificados como perfis de destino para suas mensagens.

* **[!UICONTROL Aumento]**: medida da melhora da porcentagem na taxa de conversão de um determinado tratamento em relação à linha de base.

* **[!UICONTROL Confiança]**: evidência de que um determinado tratamento é igual ao tratamento de linha de base. [Saiba mais](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Taxa de conversão]**: porcentagem de perfis que concluíram a ação desejada (por exemplo, compra, inscrição) após verem o tratamento.

### Insights do experimento {#insights}

>[!AVAILABILITY]
>
>O recurso Insights de experimentação é limitado a experimentos com alterações baseadas em texto.

**[!UICONTROL Insights de experimento]** são aprendizados gerados por IA derivados deste experimento. Esses insights ficam disponíveis assim que o experimento atinge significância estatística e fornece compreensão contextual do que contribuiu para seu sucesso. Eles destacam os principais atributos presentes no tratamento vencedor, distintos do controle, que provavelmente influenciaram o resultado.

Observe que para que os insights do experimento sejam gerados, primeiro é necessário [confirmar os detalhes da hipótese e do tratamento](#set-up) e a significância estatística a ser atingida.

Clique em **[!UICONTROL Exibir detalhes]** para saber mais sobre cada insights.

</br>

![](assets/experiment-monitor-insights.png)
