---
solution: Journey Optimizer
product: journey optimizer
title: Acelerador de experimentação
description: Melhore sua capacidade de conduzir experimentos com eficiência e gerar insights
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: conteúdo, experimento, vários, público-alvo, tratamento
hide: true
hidefromtoc: true
source-git-commit: e4d5631701c5c270af7aec931f6b98a567b4ed29
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 1%

---

# Introdução à Experimentation Accelerator {#content-experiment}

>[!BEGINSHADEBOX]

* **[Introdução ao Experimentation Accelerator](experiment-accelerator.md)**
* [Guia Experimentos](experiment-accelerator-monitor.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
> No momento, o Experimentation Accelerator está na versão beta, com recursos sendo lançados progressivamente.

O **Experimentation Accelerator** é uma ferramenta poderosa criada para simplificar e aprimorar o processo de experimentação. Ao integrar com o Adobe Target e o Adobe Journey Optimizer, ele fornece uma plataforma centralizada para gerenciar, analisar e otimizar experimentos. Ao utilizar insights orientados por IA e testes adaptáveis, o Experimentation Accelerator capacita você a tomar decisões orientadas por dados, melhorar estratégias de marketing e gerar resultados mensuráveis.

Os principais benefícios incluem:

* **Experimentação mais rápida**: execute testes adaptáveis, sempre ativos, com modelos que se ajustam ao longo do tempo.

* **Plataforma Unificada**: gerencie todos os experimentos da Adobe Target e da Journey Optimizer em um único local.

* **Insights orientados por IA**: mostre automaticamente os principais resultados, impulsionadores de desempenho e novas oportunidades.

* **Direcionamento mais inteligente**: use dados comportamentais e de conteúdo para priorizar experimentos de alto impacto.

* **Monitoramento de KPI**: controle métricas como aumento, receita e confiança em experimentos.

* **Collaboration perfeito**: compartilhe resultados facilmente e gerencie funções de equipe com alertas em tempo real.

Depois de [criar e configurar seu experimento](content-experiment.md) e enviar suas campanhas ou jornadas aos seus perfis, você pode acessar o **[!UICONTROL Experimentation Accelerator]** para se aprofundar no desempenho do seu experimento.

Para acessar o **[!UICONTROL Experimentation Accelerator]**:

* No menu à esquerda, selecione **[!UICONTROL Experimentation Accelerator]** no menu suspenso **[!UICONTROL Experimentação]**.

* Como alternativa, selecione **[!UICONTROL Experimentation Accelerator]** no alternador de aplicativos.

Observe que os usuários somente com uma licença do Target podem acessá-la somente por meio do alternador de Aplicativos.

<!--
<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="Overview" href="experiment-accelerator-overview.md" src="assets/do-not-localize/experiments-2.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-overview.md">Overview</a></strong></p></div></td>
<td><img alt="Experiments" href="experiment-accelerator-monitor.md" src="assets/do-not-localize/experiment-overview.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-monitor.md">Experiments</a></strong></p></div></td>
<td><img alt="Metrics" href="experiment-accelerator-metrics.md" src="assets/do-not-localize/experiment-metrics.png">
<div align="center"><p><strong><a href="experiment-accelerator-metrics.md">Metrics</a></strong></p></div></td>
</tr></table>
-->

## O que é teste A/B?

O teste A/B é o processo de comparar duas ou mais versões de algo para determinar qual tem melhor desempenho em relação a uma meta definida.

Os participantes são atribuídos aleatoriamente a uma versão, conhecida como variante, e seu comportamento é rastreado. Os resultados mostram se uma versão supera estatisticamente as outras.

## Principal terminologia

| Termo | Definição |
|-|-|
| Controle | A versão original usada como linha de base para comparação. |
| Variante ou tratamento | Uma nova versão criada para testar o controle. |
| Hipótese | Uma previsão sobre qual mudança produzirá um resultado melhor e por quê. |
| Tamanho da amostra | O número de indivíduos ou sessões incluídos no teste. |
| Significância estatística | Uma medida de confiança de que os resultados não se devem a uma chance aleatória. |
| Aumento | A melhora ou o declínio percentual de uma variante em comparação ao controle. |
| Métrica principal | A principal medida usada para determinar o sucesso do teste. |
| Métricas secundárias | Métricas de suporte que oferecem insight adicional ou ajudam a monitorar efeitos não intencionais. |
| Intervalo de confiança | O intervalo estimado dentro do qual o efeito real é susceptível de cair. |
| Segmento | Um subconjunto específico do público-alvo analisado independentemente (por exemplo, novos usuários, visitantes móveis). |

## Práticas recomendadas para executar experimentos

* **Comece com uma hipótese clara**

  Uma forte hipótese inclui o que você está mudando, o que você espera que aconteça e por quê.
Exemplo: _Acreditamos que alterar X aumentará Y devido a Z._

* **Definir uma métrica de sucesso significativa**

  Escolha uma métrica que se alinhe às suas metas mais amplas. Evite métricas personalizadas que tenham boa aparência, mas que não reflitam o impacto real.

* **Testar uma alteração de cada vez (quando possível)**

  O isolamento de variáveis facilita a interpretação precisa dos resultados. Se você testar várias alterações de uma só vez, talvez não saiba o que causou o efeito.

* **Deixe o teste ser executado por tempo suficiente**

  Conclusões prematuras podem ser enganosas. Aguarde um tamanho de amostra estatisticamente significativo antes de agir.

* **Esteja ciente dos fatores externos**

  A sazonalidade, os feriados e outras alterações em seu ambiente podem distorcer os resultados. Documente qualquer item que possa influenciar o comportamento durante o teste.

* **Use a segmentação cuidadosamente**

  Detalhar os resultados por segmento de público-alvo pode revelar padrões ocultos, mas evitar a interpretação excessiva de pequenos tamanhos de amostra.

* **Documentar e compartilhar aprendizados**

  Mantenha um registro claro do que foi testado, por quê e o que você aprendeu. Isso constrói o conhecimento institucional e evita erros recorrentes.

## Métricas comuns

| Métrica | O que ele mede | Quando usar |
|-|-|-|
| Índice de conversão | A porcentagem de usuários que concluem uma ação desejada | Útil para rastrear o sucesso de uma experiência orientada por metas |
| Índice de click-through (CTR) | A porcentagem de usuários que clicam em um elemento específico | Indica o quão convincente é a experiência |
| Taxa de participação | O nível de interação dos usuários com a experiência | Bom para medir interesse ou atenção |
| Taxa de rejeição | A porcentagem de usuários que saem rapidamente sem realizar nenhuma ação | Pode indicar um ajuste inadequado ou uma experiência confusa |
| Tempo na página | O tempo que os usuários gastam em uma parte específica da experiência | Pode refletir profundidade de interesse ou complexidade |
| Receita por visitante (RPV) | Receita média ganha por usuário | Frequentemente usado em experimentos focados no comércio |
| Taxa de retenção | A porcentagem de usuários que retornam ou permanecem envolvidos ao longo do tempo | Útil para avaliações de longo prazo |

## O que faz um bom experimento?

Um bom experimento não apenas produz uma vitória, ele produz um aprendizado claro e acionável.
Veja o que procurar:

&amp;check; **Confiança estatística**: é improvável que a diferença entre as variantes seja devido ao acaso.
&amp;check; **Alinhamento com metas**: a métrica primária reflete o progresso significativo em direção a um objetivo comercial.
&amp;check; **Impacto Secundário**: nenhum efeito colateral negativo significativo em métricas relacionadas.
&amp;check; **Escalabilidade**: o resultado pode informar decisões futuras ou ser generalizado para outras áreas.
&amp;check; **Clareza**: a causa do resultado é razoavelmente isolada e compreendida.

Experimentação não é apenas encontrar a versão &quot;melhor&quot;, é sobre a construção de conhecimento através de testes e iteração. Quando bem feitos, os experimentos revelam insights que impulsionam decisões mais inteligentes, melhores experiências do usuário e resultados melhores.

>[!BEGINSHADEBOX]

**Exemplo:**

* **Empresa**: rede hoteleira
* **Hipótese**: se usarmos uma linguagem mais urgente na home page, ela resultará em mais reservas.
   * **Controle**: versão original
   * **Variante**: nova versão com urgência adicionada
   * **Métrica primária**: taxa de reserva
   * **Métricas secundárias**: taxa de rejeição, tempo no site
* **Resultado**: a variante produziu um aumento de 14% na taxa de reserva, sem alteração negativa em outras métricas.
* **Ação**: considere implantar a variante e executar experimentos de acompanhamento para testar abordagens semelhantes em outras áreas.

>[!ENDSHADEBOX]
