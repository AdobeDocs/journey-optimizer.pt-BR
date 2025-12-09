---
solution: Journey Optimizer
product: journey optimizer
title: Critérios de entrada e saída da jornada
description: Saiba como gerenciar com eficiência o momento em que perfis entram e saem das jornadas com exemplos reais e práticas recomendadas
feature: Journeys, Profiles
role: User
level: Intermediate
hide: true
hidefromtoc: true
keywords: entrada, saída, critérios, jornada, perfil, reentrada, práticas recomendadas
version: Journey Orchestration
source-git-commit: 9e5b85dec8a58a4d008ab63337589352c0fa5ee6
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 1%

---


# Trabalhar com os critérios de entrada e saída da jornada {#entry-exit-criteria-guide}

Na organização da experiência do cliente, a entrega da mensagem certa no momento certo requer controle preciso sobre quando os clientes entram e saem das jornadas. Entender e configurar corretamente os critérios de entrada e saída pode fazer a diferença entre uma campanha bem-sucedida e envolvente e oportunidades perdidas ou fadiga da mensagem.

Este guia fornece orientação prática, exemplos reais e práticas recomendadas para gerenciar os critérios de entrada e saída do jornada no Adobe Journey Optimizer.

## Quais são os critérios de entrada e saída? {#what-are-criteria}

**Os critérios de entrada** determinam as condições sob as quais um [perfil de cliente](../audience/get-started-profiles.md) se qualifica para inserir uma jornada específica. Os perfis podem ser inseridos com base em:

* **[Comportamento do cliente](../event/about-events.md)** - As ações realizadas pelos clientes acionam a entrada da jornada em tempo real, como fazer uma compra, abandonar um carrinho ou abrir o aplicativo móvel.

* **[Atributos do perfil](../audience/get-started-profiles.md)** - As características do cliente determinam a qualificação com base nos dados armazenados em seu perfil, como nível de fidelidade, local, idade ou preferências de comunicação.

* **[Eventos externos](../event/about-creating-business.md)** - Acionadores comerciais ou ambientais que afetam vários clientes simultaneamente, como alertas de baixo inventário, condições meteorológicas ou alterações de preço.

* **[Associação de público-alvo](../audience/about-audiences.md)** - Pertencer a um segmento de público específico habilita jornadas direcionadas para grupos como clientes de alto valor, usuários inativos ou assinantes novos.

**Critérios de saída** definem quando e como um perfil sai ou é removido de uma jornada:

* **Conclusão da Jornada** - Os perfis são encerrados automaticamente ao atingirem o [fim de todos os caminhos de jornada](end-journey.md), concluindo a experiência projetada.

* **Conquista da métrica de sucesso** - Os perfis são encerrados quando concluem o [objetivo de jornada](success-metrics.md), como comprar ou baixar um aplicativo, eliminando comunicações de acompanhamento desnecessárias.

* **Baseado em condição** - Perfis saem quando [condições específicas](condition-activity.md) são atendidas, como inatividade em um período definido ou alterações nos atributos de perfil.

* **Baseado em evento** - Perfis são encerrados quando [eventos específicos ocorrem](../event/about-events.md), como cancelamento de assinatura ou devolução de produto.

* **Desqualificação de público-alvo** - Os perfis são encerrados quando não atendem mais aos [critérios de público-alvo](../audience/about-audiences.md), garantindo que as mensagens permaneçam relevantes.

## Por que os critérios de entrada e saída são importantes {#why-they-matter}

A definição adequada dos critérios de entrada e saída agrega um valor significativo aos negócios:

* **Relevância**: somente os clientes certos entram na jornada, aumentando as taxas de engajamento e conversão ao direcionar o público mais apropriado no momento ideal.

* **Eficiência**: impede que os clientes permaneçam em jornadas irrelevantes, reduzindo comunicações desnecessárias, custos operacionais e inconvenientes para o cliente.

* **Personalization**: permite a personalização dinâmica de experiências com base em dados e comportamento em tempo real, criando interações mais significativas com o cliente.

* **Conformidade**: ajuda a gerenciar o limite de frequência e a evitar a comunicação excessiva, respeitando as preferências do cliente e os requisitos normativos e, ao mesmo tempo, mantendo a reputação da marca.

## Exemplos reais de entrada e saída de jornadas {#real-world-examples}

Estes são cenários comuns que demonstram como os critérios de entrada e saída funcionam na prática:

**Campanha de boas-vindas para novos assinantes**

* **Entrada**: perfis entram na jornada quando assinam um boletim informativo
* **Sair**: os perfis são encerrados após concluírem uma série de emails de boas-vindas ou após um tempo definido, caso não sejam envolvidos
* **Benefício**: garante que novos assinantes recebam a integração em tempo hábil, evitando mensagens repetitivas

**Recuperação do carrinho abandonada**

* **Entrada**: os clientes inserem a jornada se adicionarem itens ao carrinho, mas não concluírem o check-out em 24 horas
* **Saída**: os perfis são encerrados ao concluírem a compra ou após 7 dias se nenhuma compra for feita
* **Benefício**: impulsiona conversões através de lembretes oportunos sem enviar spam para clientes desinteressados

**Participação no programa de fidelidade**

* **Entrada**: os clientes ingressam na jornada depois de atingir um determinado limite de pontos de fidelidade
* **Saída**: os perfis são encerrados após resgatar recompensas ou se ficarem inativos por 60 dias
* **Benefício**: mantém clientes de alto valor envolvidos com ofertas personalizadas e evita a fadiga da comunicação

**Coleção de comentários sobre o produto**

* **Entrada**: os clientes entram na jornada depois de receberem um evento de confirmação de entrega de produto
* **Sair**: os perfis são encerrados assim que o feedback é enviado ou após 10 dias se nenhuma resposta
* **Benefício**: captura comentários valiosos prontamente sem incomodar os clientes com solicitações persistentes

## Como configurar os critérios de entrada do jornada {#configure-entry}

>[!BEGINSHADEBOX]

**Saiba tudo o que precisa saber sobre o Critério de Entrada aqui:**

* **[Acionadores com base em eventos](../event/about-events.md)**: use eventos como &quot;criação de perfil&quot;, &quot;transação concluída&quot; ou eventos personalizados para iniciar uma jornada. [Configure os eventos](../event/about-creating.md) em **[!UICONTROL Administration]** > **[!UICONTROL Events]**, defina o [esquema de eventos e os campos](../event/experience-event-schema.md) e adicione o evento da paleta **[!UICONTROL Events]** no [designer do jornada](using-the-journey-designer.md).

* **[Entrada baseada em público-alvo](read-audience.md)**: jornadas de direcionamento para perfis que pertencem a públicos-alvo específicos, como um lote único ou em um agendamento recorrente. [Criar públicos-alvo](../audience/creating-a-segment-definition.md) no menu **[!UICONTROL Públicos-alvo]**, adicionar uma atividade **[!UICONTROL Ler público-alvo]** e [configurar o agendamento](journey-properties.md#schedule).

* **[Entrada de qualificação de público-alvo](audience-qualification-events.md)**: acione jornadas quando os perfis se qualificarem para públicos-alvo específicos em tempo real ou saírem deles. Defina [públicos-alvo de streaming](../audience/about-audiences.md), adicione um evento **[!UICONTROL Qualificação de público-alvo]** da paleta **[!UICONTROL Eventos]** e escolha o tipo de gatilho.

* **[Filtros de Atributo](condition-activity.md)**: refine os critérios de entrada combinando eventos ou públicos-alvo com atributos de perfil e contexto usando a lógica E/OU. Use [condições](conditions.md) para fazer referência a [atributos de perfil](../audience/get-started-profiles.md), eventos ou [dados externos](../datasource/about-data-sources.md).

* **[Janelas de Tempo e Agendamento](journey-properties.md#schedule)**: defina restrições temporais para manter as jornadas oportunas e relevantes. Configure [agendas em atividades Read Audience](read-audience.md), use [atividades Wait](wait-activity.md) e adicione [condições baseadas em tempo](conditions.md) para controlar o tempo.

>[!ENDSHADEBOX]

## Como configurar os critérios de saída do jornada {#configure-exit}

>[!BEGINSHADEBOX]

**Saiba tudo o que precisa saber sobre o Critério de Saída aqui:**

* **[Conclusão da Jornada](end-journey.md)**: os perfis são encerrados automaticamente depois de atingirem a etapa final de jornada. Crie caminhos de jornada para terminar em **[!UICONTROL Fim]** atividades.

* **[Atingimento da métrica de sucesso](journey-properties.md#exit-criteria)**: defina métricas de sucesso (como compra ou assinatura) e perfis de saída após a conclusão. Clique no ícone **[!UICONTROL Mostrar critérios de saída]**, selecione **[!UICONTROL Adicionar critérios de saída]** e escolha um [Evento](../event/about-events.md) ou [Público](../audience/about-audiences.md) como acionador de saída.

* **[Tempos limite de inatividade](wait-activity.md)**: sai de perfis se não ocorrer nenhum envolvimento dentro de um período de tempo definido. Use [Critério de saída](journey-properties.md#exit-criteria) com públicos-alvo que verificam a última data de envolvimento, definem [atividades de espera](wait-activity.md) com durações definidas e usam [condições](condition-activity.md) para verificar a existência de atividade.

* **[Regras de Reentrada](entry-management.md)**: decida se os perfis podem entrar novamente na jornada várias vezes ou apenas uma vez, dependendo da sua estratégia de campanha. Defina as configurações de **[!UICONTROL Reentrada]** na jornada **[!UICONTROL Propriedades]** para definir períodos de espera, habilitar a reentrada forçada ou usar [identificadores complementares](supplemental-identifier.md) para reentrada específica de contexto.

>[!ENDSHADEBOX]

## Exemplos detalhados de jornada {#journey-examples}

Para obter orientação de implementação passo a passo com detalhes técnicos completos, explore estes casos de uso documentados:

* **[jornada de integração do cliente](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** - Crie experiências de boas-vindas personalizadas com qualificação de público-alvo, tempo limite do evento e saídas baseadas em metas

* **[Recuperação do carrinho abandonado](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** - Recupere vendas perdidas com jornadas, manuais e roteamento de canais acionados por eventos

* **[Campanhas de reengajamento](https://experienceleague.adobe.com/pt-br/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** - Conquiste clientes inativos com definição de metas comportamentais e ativação de mídia paga

* **[Enviar mensagens aos assinantes](message-to-subscribers-uc.md)** - Direcionar listas de assinaturas com Audiência de Leitura e conteúdo personalizado

* **[Enviar mensagens de vários canais](journeys-uc.md)** - Combinar email e push com eventos de reação e lógica de vários caminhos

* **[Enviar emails somente em dias da semana](weekday-email-uc.md)** - Agendar comunicações usando condições baseadas em tempo e fórmulas de espera

>[!TIP]
>
>Procure todos os casos de uso disponíveis na [biblioteca de casos de uso do Jornada](jo-use-cases.md) para mais padrões e implementações, incluindo [aumentar as entregas](ramp-up-deliveries-uc.md), [padrões de evento de experiência](exp-event-lookup.md) e [remoção de perfis do jornada live](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Práticas recomendadas para gerenciar entrada e saída {#best-practices}

**Limpar definição**

* Documente a lógica de entrada e saída antes de criar jornadas para alinhar equipes de marketing e análise
* Criar fluxogramas mostrando pontos de entrada, caminhos de jornada e condições de saída
* Defina as regras de negócios com clareza: &quot;Perfis são encerrados quando X ocorre OU após Y dias&quot;
* Use rótulos descritivos: &quot;Saída - Compra concluída&quot; não &quot;Saída 1&quot;
* [Marque jornadas](../start/search-filter-categorize.md#tags) de forma consistente para relatórios e filtragem

**Evitar jornadas sobrepostas**

* [Auditoria de jornadas ativas](journey-ui.md) antes de iniciar outras semelhantes para evitar conflitos
* Aproveite o [gerenciamento de conflitos](../conflict-prioritization/conflicts.md) e as [pontuações de prioridade](../conflict-prioritization/priority-scores.md) para resolver sobreposições e priorizar jornadas
* Projetar jornadas que se complementam em vez de competir entre si

>[!NOTE]
>
>Para cenários avançados, como a remoção automática de perfis quando eles se qualificam para jornadas de prioridade mais alta, use o [limite de jornada e arbitragem](../conflict-prioritization/journey-capping.md) em vez dos critérios de saída.

**Monitorar e otimizar**

* Rastreie a taxa de entrada, a taxa de saída e a taxa de conclusão de cada jornada usando os [relatórios de jornada](../reports/journey-global-report-cja.md)
* Monitorar [métricas de sucesso](success-metrics.md): porcentagem de saída por conclusão de métrica de sucesso vs. tempo limite
* [Testar os critérios de entrada e saída](testing-the-journey.md) com vários cenários de perfil antes de iniciar
* Ajustar com base nos dados: se houver altas saídas antecipadas, revise a relevância dos critérios de entrada; se houver baixa conclusão de métrica de sucesso, analise o conteúdo e o tempo
* Revisar todas as jornadas ativas trimestralmente

**Respeitar limites de frequência**

* Defina [períodos de espera de reentrada](entry-management.md) apropriados ou desabilite a reentrada para jornadas únicas
* Use as [regras de limite de frequência](../conflict-prioritization/rule-sets.md) para evitar comunicação excessiva
* Monitorar métricas de frequência nos relatórios para garantir a conformidade

>[!NOTE]
>
>Para gerenciar limites de frequência e limites de entrada de jornada em várias jornadas, use [limite e arbitragem de jornada](../conflict-prioritization/journey-capping.md) e [limite de frequência por canal](../conflict-prioritization/channel-capping.md).

## Conclusão {#conclusion}

Os critérios de entrada e saída da jornada são fundamentais para fornecer experiências personalizadas, oportunas e eficazes ao cliente com o Adobe Journey Optimizer. Ao criar cuidadosamente essas condições, os profissionais de marketing podem aumentar o engajamento, reduzir o atrito e fortalecer os relacionamentos com os clientes.

Comece mapeando claramente os acionadores do cliente e os pontos de saída, teste completamente e monitore os resultados para refinar continuamente a orquestração de jornadas.

## Recursos relacionados {#related-resources}

**Documentação técnica**

* [Gerenciamento de entrada de perfil](entry-management.md) - Guia técnico detalhado para controles de entrada
* [Propriedades de Jornada e critérios de saída](journey-properties.md) - Referência de configuração completa
* [Como o jornada termina](end-journey.md) - Gerenciamento do ciclo de vida da Jornada
* [Identificadores complementares](supplemental-identifier.md) - Cenários de reentrada avançados
* [Designer de Jornadas](using-the-journey-designer.md) - jornadas de compilação e design

**Tutoriais e exemplos**

* [Casos de uso de Jornada](jo-use-cases.md) - Exemplos e padrões de jornada completos
* [Vídeo de integração do cliente](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* [Vídeo de carrinho abandonado](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* [Blog da comunidade: Critérios de entrada e saída](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958?profile.language=pt)

**Recursos relacionados**

* [Eventos de qualificação de público-alvo](audience-qualification-events.md)
* [Métricas de sucesso e metas](success-metrics.md)
* [Gerenciamento de conflitos](../conflict-prioritization/conflicts.md)
* [Limite de frequência](../conflict-prioritization/rule-sets.md)
* [Jornadas de teste](testing-the-journey.md)
* [Atividade de condição](condition-activity.md)
* [Eventos de reação](reaction-events.md)
* [Atividade aguardar](wait-activity.md)
