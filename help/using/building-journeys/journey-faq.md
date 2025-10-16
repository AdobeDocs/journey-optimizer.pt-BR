---
solution: Journey Optimizer
product: journey optimizer
title: Perguntas frequentes sobre o Jornada
description: Perguntas frequentes sobre o Journey Optimizer Jornada
feature: Journeys, Get Started
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: jornada, perguntas, respostas, solução de problemas, ajuda, guia
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: a7da542320a38dbc739ec42ee4926fce1dea1df0
workflow-type: tm+mt
source-wordcount: '2363'
ht-degree: 1%

---


# Perguntas frequentes {#faq-journeys}

Você encontrará abaixo as Perguntas frequentes sobre o Adobe Journey Optimizer Jornada.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}.

## Conceitos gerais

+++ O que é uma jornada no Adobe Journey Optimizer?

Uma jornada é uma orquestração de várias etapas que permite projetar e executar experiências do cliente em tempo real em vários canais. As jornadas combinam eventos, atividades de orquestração, ações e mensagens para criar experiências personalizadas e contextuais com base no comportamento do cliente e em eventos comerciais.

Saiba mais sobre [jornadas](journey.md).

+++

+++ Quais são os diferentes tipos de jornadas?

O Adobe Journey Optimizer oferece suporte a três tipos de jornadas:

* **jornadas Unitárias**: acionadas individualmente por um evento (por exemplo, uma compra, entrada no aplicativo). Os perfis são inseridos um de cada vez na jornada quando o evento ocorre.
* **Ler jornadas de Público-Alvo**: Inicie com um público-alvo do Adobe Experience Platform e envie mensagens em lote para todos os perfis desse público-alvo.
* **jornadas de eventos comerciais**: acionadas por eventos comerciais (por exemplo, atualizações de ações, alertas meteorológicos) que afetam vários perfis simultaneamente.

Saiba mais sobre [tipos de jornada](entry-management.md#types-of-journeys).

+++

+++ Qual é a diferença entre uma jornada e uma campanha?

jornada **As** são orquestrações de várias etapas que reagem a eventos ou públicos-alvo, permitindo lógica complexa, condições, tempos de espera e vários pontos de contato ao longo do ciclo de vida do cliente.

**Campanhas** são comunicações únicas ou recorrentes enviadas a um público específico, ideais para mensagens autônomas, como anúncios promocionais ou boletins informativos.

**Prática recomendada**: use jornadas para participação contínua em várias etapas e campanhas para comunicações autônomas direcionadas.

+++

+++ Quais são os principais componentes de uma jornada?

Uma jornada consiste em:

* **Eventos**: pontos de entrada que acionam a jornada (por exemplo, qualificação de perfil, eventos comerciais)
* **Atividades de orquestração**: componentes lógicos como condições, espera, lê público e termina
* **Ações**: atividades que executam tarefas, como enviar mensagens, atualizar perfis ou chamar APIs externas
* **Ações de canal integradas**: recursos de mensagens nativas para email, SMS, push e outros canais
* **Ações personalizadas**: integração com sistemas de terceiros

Saiba mais sobre [atividades de jornada](about-journey-activities.md).

+++

## Criação de jornadas

+++ Como começar a criar minha primeira jornada?

Siga estas etapas principais:

1. **Configurar pré-requisitos**: configure eventos, fontes de dados e ações conforme necessário
2. **Criar a jornada**: navegue até o menu Jornadas e clique em &quot;Criar Jornada&quot;
3. **Definir propriedades da jornada**: Defina o nome, a descrição, o namespace e outras configurações da jornada
4. **Criar a jornada**: arraste e solte atividades da paleta na tela
5. **Testar a jornada**: use o modo de teste para validar a lógica de jornada
6. **Publicar a jornada**: ative a jornada para ativá-la

Siga o [guia passo a passo](journey-gs.md).

+++

+++ Quais pré-requisitos são necessários antes de criar uma jornada?

Os pré-requisitos dependem do tipo de jornada:

* **jornadas acionadas por eventos**: configure eventos para definir quando os perfis devem entrar na jornada
* **jornadas baseadas em público-alvo**: criar públicos-alvo no Adobe Experience Platform
* **Enriquecimento de dados**: configure as fontes de dados para recuperar informações adicionais
* **Integrações de terceiros**: configurar ações personalizadas se estiver usando sistemas externos

Saiba mais sobre a [configuração do jornada](../configuration/about-data-sources-events-actions.md).

+++

+++ Posso usar dados de sistemas externos em minha jornada?

Sim. Você pode configurar **fontes de dados externas** para recuperar informações de serviços de API de terceiros e usá-las em condições de jornada, personalização ou ações. Isso permite enriquecer a experiência do cliente com dados em tempo real do seu CRM, sistemas de fidelidade, serviços meteorológicos ou outras plataformas externas.

Saiba mais sobre [fontes de dados externas](../datasource/external-data-sources.md).

+++

+++ Como adicionar condições à minha jornada?

Você pode adicionar condições usando a **Atividade de condição** da paleta de orquestração. As condições permitem:

* Criar condições simples ou avançadas usando o editor de expressão
* Dividir a jornada em vários caminhos com base em atributos de perfil, associação de público-alvo, eventos ou dados contextuais
* Definir caminhos de tempo limite para perfis que não atendem à condição em um tempo especificado

Saiba mais sobre [condições](condition-activity.md).

+++

+++ Posso enviar mensagens para perfis em uma jornada?

Sim. O Journey Optimizer inclui **ações de canal integradas** que permitem enviar mensagens por email, notificações por push, SMS/MMS/RCS, mensagens no aplicativo, experiências da Web, experiências baseadas em código, correspondência direta, cartões de conteúdo, WhatsApp e LINE. Você pode criar o conteúdo da mensagem diretamente no Journey Optimizer e adicioná-lo como atividades de ação em sua jornada.

Saiba mais sobre [mensagens no jornada](journeys-message.md).

+++

+++ Como faço para esperar um horário ou evento específico em uma jornada?

Use a **Atividade de espera** para pausar a jornada por uma duração especificada ou até uma data/hora específica. As atividades de espera são úteis para:

* Envio de mensagens de acompanhamento após um atraso (por exemplo, 3 dias após a compra)
* Aguardando o horário comercial antes de tomar uma ação
* Criar campanhas de gotejamento com intervalos de tempo
* Combinação com condições para criar cenários de tempo limite

Saiba mais sobre [atividades de espera](wait-activity.md).

+++

+++ Posso atualizar as informações de perfil em uma jornada?

Sim. Use a atividade **Atualizar Perfil** para modificar atributos de perfil no Adobe Experience Platform com base em eventos ou condições de jornada. Isso é útil para atualizar pontos de fidelidade, registrar marcos de jornada, alterar configurações de preferências ou rastrear pontuações de engajamento do cliente.

Saiba mais sobre [atualizações de perfil](update-profiles.md).

+++

## Teste e publicação

+++ Como faço para testar minha jornada antes de publicá-la?

A Journey Optimizer oferece duas abordagens de teste:

* **Modo de teste**: simular perfis individuais que se movem pela jornada passo a passo, permitindo que você verifique a lógica, as condições e as ações antes de entrar em funcionamento.
* **Modo de simulação**: execute a jornada usando dados de produção reais sem entrar em contato com clientes reais ou atualizar informações do perfil. Isso dá confiança no direcionamento de público-alvo e no design da jornada.

**Prática recomendada**: sempre teste as jornadas antes da publicação para garantir que elas funcionem conforme o esperado e para identificar quaisquer problemas antecipadamente.

Saiba mais sobre [modo de teste](testing-the-journey.md) e [simulação](journey-dry-run.md).

+++

+++ O que acontece quando eu publico uma jornada?

Ao publicar uma jornada:

* A jornada fica **ativa** e pronta para aceitar novos perfis
* Perfis podem ser inseridos com base nos critérios de entrada (evento ou público)
* Mensagens e ações começam a ser executadas para perfis que se movem pela jornada
* Não é possível editar diretamente uma jornada publicada (é necessário criar uma nova versão)

Saiba mais sobre [publicação de jornadas](publishing-the-journey.md).

+++

+++ Posso modificar uma jornada já publicada?

Não é possível editar diretamente uma jornada em tempo real. Para fazer alterações:

1. **Criar uma nova versão**: duplicar a jornada publicada para criar uma versão de rascunho
2. **Faça suas alterações**: edite a versão de rascunho conforme necessário
3. **Testar a nova versão**: usar o modo de teste para validar as alterações
4. **Publicar a nova versão**: isso fecha automaticamente a versão anterior e ativa a nova

Os perfis que já estão na jornada concluirão a versão original, enquanto os novos perfis entrarão na nova versão.

Saiba mais sobre [versões do jornada](journey-ui.md#journey-versions).

+++

+++ Como faço para interromper uma jornada?

É possível gerenciar a execução da jornada de várias maneiras:

* **Fechar para novas entradas**: impedir a entrada de novos perfis, permitindo que os perfis existentes concluam a jornada
* **Parar imediatamente**: encerra a jornada e sai de todos os perfis que estão nela no momento
* **Pausar**: interromper temporariamente a jornada e retomá-la mais tarde (disponível para tipos de jornada específicos)

Saiba mais sobre o [encerramento de jornadas](end-journey.md).

+++

## Execução e monitoramento do Jornada

+++ Como posso rastrear o progresso do perfil em uma jornada?

É possível monitorar a execução da jornada usando:

* **Relatório ao vivo da Jornada**: visualize métricas e KPIs em tempo real para sua jornada
* **Relatório de Tempo Total de Jornada**: analise o desempenho da jornada usando o Customer Journey Analytics
* **Eventos de Etapa de Jornada**: acesse dados de execução detalhados para relatórios personalizados
* **Painel de Jornada Dry Run**: revise os resultados da execução do teste antes de entrar em funcionamento

Saiba mais sobre [relatórios do jornada](report-journey.md).

+++

+++ Por que um perfil não entrou na minha jornada?

Motivos comuns para os perfis não entrarem em uma jornada:

* **Evento não recebido**: o evento de acionamento não foi enviado ou configurado corretamente
* **Critério de público-alvo não atendido**: o perfil não se qualifica para o público-alvo da entrada
* **Regras de reentrada**: o perfil concluiu recentemente a jornada e a reentrada está bloqueada
* **Jornada não publicada**: a jornada está no status de rascunho
* **Namespace inválido**: o namespace de jornada não corresponde à identidade do perfil
* **Jornada fechada**: a jornada não está mais aceitando novas entradas

Saiba mais sobre o [gerenciamento de entradas](entry-management.md).

+++

+++ O que são eventos de etapa de jornada e como posso usá-los?

Os eventos de etapa de Jornada são conjuntos de dados gerados automaticamente que capturam informações detalhadas sobre cada etapa que um perfil toma em uma jornada. Eles incluem eventos de entrada e saída, execução de ação (mensagens enviadas, ações personalizadas chamadas), transições de jornada (movimentação entre atividades) e erros e tempos limite.

**Casos de uso**:

* Criar relatórios personalizados nas ferramentas do Customer Journey Analytics ou BI
* Depurar problemas de execução do jornada
* Rastrear o comportamento detalhado do perfil
* Criar análises avançadas e modelos de atribuição

Saiba mais sobre [eventos de etapa do jornada](../reports/sharing-overview.md).

+++

+++ Como posso solucionar problemas de uma jornada que não está funcionando como esperado?

A Journey Optimizer fornece vários recursos de solução de problemas:

* **Indicadores de erro**: alertas visuais na tela de jornada realçam problemas de configuração
* **Modo de teste**: percorra a jornada para identificar onde ocorrem os problemas
* **Relatórios de Jornada**: revise as métricas de execução para encontrar afunilamentos ou erros
* **Jornada eventos de etapa**: analise dados de execução detalhados para entender o comportamento do perfil

**Problemas comuns**:

* Eventos ou públicos configurados incorretamente
* Conexões de fonte de dados ausentes
* Expressões inválidas em condições ou personalização
* Configurações de tempo limite muito curtas

Saiba mais sobre [jornadas de solução de problemas](troubleshooting.md).

+++

+++ O que acontece se uma ação falhar em uma jornada?

Quando uma ação falha (por exemplo, tempo limite da chamada da API, erro de delivery de mensagem), a jornada continua por padrão, a menos que configurado de outra forma. Você pode definir atividades de condição para lidar com cenários de falha, e erros são registrados em relatórios de jornada e eventos de etapa para monitoramento.

**Prática recomendada**: definir valores de tempo limite apropriados para ações externas e caminhos alternativos para cenários de falha críticos.

Saiba mais sobre [respostas da ação](../action/action-response.md).

+++

## Conceitos avançados

+++ O que é um namespace do jornada e por que ele é importante?

Um **namespace** é um tipo de identidade (por exemplo, email, ECID, número de telefone) que determina como os perfis são identificados na jornada. O namespace define qual identificador é usado para corresponder perfis, deve ser consistente em eventos, públicos e dados de perfil e afeta a entrada da jornada e o comportamento de reentrada.

**Prática recomendada**: escolha um namespace que identifique seus clientes de forma confiável em todos os pontos de contato.

Saiba mais sobre [namespaces de identidade](../audience/get-started-identity.md).

+++

+++ Os perfis podem inserir a mesma jornada várias vezes?

Sim, dependendo das **configurações de reentrada**:

* **Permitir reentrada**: perfis podem entrar na jornada várias vezes depois de concluí-la
* **Período de espera de reentrada**: defina um tempo mínimo entre as entradas de jornada (por exemplo, 7 dias)
* **Forçar reentrada no evento**: acione uma nova instância do jornada mesmo que o perfil já esteja na jornada

**Prática recomendada**: usar regras de reentrada para evitar a fadiga da mensagem e garantir o ritmo apropriado.

Saiba mais sobre o [gerenciamento de entradas](entry-management.md).

+++

+++ O que é otimização de tempo de envio?

A **Otimização de Tempo de Envio (STO)** usa a IA para prever o melhor momento para enviar uma mensagem para cada perfil individual, maximizando as taxas de abertura e o envolvimento. O STO analisa padrões históricos de engajamento para determinar quando cada recipient tem maior probabilidade de interagir com sua mensagem.

**Benefícios**:

* Taxas de abertura e de clique aprimoradas
* Melhor experiência do cliente por meio de mensagens com tempo ideal
* Taxas de cancelamento de inscrição reduzidas

Saiba mais sobre [otimização de tempo de envio](send-time-optimization.md).

+++

+++ O que são regras de limite de jornada?

O **limite de Jornada** permite limitar o número de vezes que um perfil pode entrar em jornadas em um período de tempo especificado, evitando a fadiga da mensagem e garantindo uma experiência ideal para o cliente. Você pode definir o máximo de entradas por perfil em jornadas ou jornadas específicas, definir janelas de tempo (diariamente, semanalmente, mensalmente) e priorizar jornadas quando várias jornadas competem pelo mesmo perfil.

Saiba mais sobre [limite de jornada](../conflict-prioritization/journey-capping.md).

+++

+++ Posso integrar minha jornada a sistemas externos?

Sim. Use **ações personalizadas** para chamar APIs de terceiros (CRM, automação de marketing, sistemas de fidelidade), enviar dados para sistemas externos, recuperar informações em tempo real para decisões e acionar fluxos de trabalho em plataformas externas.

As ações personalizadas oferecem suporte à autenticação (chave da API, OAuth 2.0), personalização de carga de solicitação/resposta, manipulação de erros e tempos limite e parâmetros dinâmicos do contexto de jornada.

Saiba mais sobre [Ações personalizadas](using-custom-actions.md).

+++

+++ Como posso usar o Adobe Campaign com jornada?

O Journey Optimizer integra-se nativamente com o Adobe Campaign para aproveitar seus recursos avançados:

* **Adobe Campaign Standard**: usar as ações do Campaign Standard para enviar mensagens transacionais
* **Adobe Campaign v7/v8**: acione fluxos de trabalho do Campaign e use a infraestrutura de entrega do Campaign

**Prática recomendada**: use essa integração se tiver modelos do Campaign, modelos de dados ou exigir recursos específicos do Campaign.

Saiba mais sobre a [integração do Campaign](ajo-ac.md).

+++

+++ O que é a atividade de salto?

A **Atividade de salto** permite a transição de perfis de uma jornada para outra, permitindo padrões de jornada reutilizáveis, orquestração de jornadas em várias jornadas, manutenção simplificada de jornadas e estratégias de envolvimento progressivo.

Quando um perfil atinge uma atividade Jump, ele sai da jornada atual e entra na jornada do target no ponto de partida.

Saiba mais sobre [a atividade de salto](jump.md).

+++

## Práticas recomendadas e limitações

+++ Quais são as principais limitações que eu devo conhecer?

As medidas de proteção importantes incluem:

* **Complexidade da Jornada**: máximo de atividades, caminhos e níveis de aninhamento
* **Taxa de transferência**: taxas de envio de mensagem e limites de chamada de API
* **Tempo de vida**: duração máxima da jornada (por exemplo, 91 dias para jornadas unitárias)
* **Tamanho do público-alvo**: limites nos tamanhos de lote de públicos-alvo de leitura
* **Complexidade de expressão**: limites de caracteres em condições e personalização

Exibir [medidas de proteção e limitações](../start/guardrails.md) concluídas.

+++

+++ Quais são as práticas recomendadas para o design de jornadas?

**Estrutura e organização**:

* Mantenha o foco das jornadas em casos de uso específicos
* Usar nomenclatura descritiva para atividades
* Adicionar notas e rótulos para lógica complexa
* Agrupar jornadas relacionadas com tags

**Desempenho**:

* Otimizar os tempos de espera para equilibrar o envolvimento e o volume
* Limitar chamadas de API externas a casos de uso essenciais
* Usar regras de limite para evitar a fadiga da mensagem
* Monitorar métricas de jornada regularmente

**Testando**:

* Sempre testar jornadas antes de publicar
* Testar todos os caminhos e cenários condicionais
* Usar perfis de teste realistas
* Validar personalização e conteúdo dinâmico

**Manutenção**:

* Analisar regularmente o desempenho da jornada
* Arquivar ou fechar jornadas não usadas
* Lógica de jornada de documentos e regras de negócios
* Plano para controle de versão do jornada

Saiba mais sobre [práticas recomendadas de design do jornada](using-the-journey-designer.md).

+++

+++ Quantas atividades posso adicionar a uma jornada?

Embora não haja um limite rigoroso no número de atividades, jornadas muito complexas (mais de 50 atividades) podem se tornar difíceis de manter e solucionar problemas. Grandes jornadas com muitas ramificações e condições podem afetar o tempo de processamento e a legibilidade.

**Prática recomendada**: se sua jornada se tornar muito complexa, considere dividi-la em várias jornadas usando a atividade de salto, criando subjornadas reutilizáveis ou simplificando a lógica com condições mais eficientes.

Saiba mais sobre [design do jornada](using-the-journey-designer.md).

+++

+++ Como garantir que minha jornada tenha bom desempenho em escala?

**Considerações sobre o design**:

* Usar entrada baseada em público para comunicações em lote em vez de eventos individuais
* Implementar tempos de espera adequados para distribuir o volume de mensagens
* Usar regras de limite para evitar sobrecarga do sistema
* Otimizar a lógica de condição para reduzir a complexidade do processamento

**Monitoramento**:

* Rastrear métricas de jornada regularmente
* Monitorar o desempenho da API para ações personalizadas
* Revisar taxas de erro e ocorrências de tempo limite
* Configurar alertas para falhas críticas de jornada

**Otimização**:

* Use o modo de teste e a simulação para validar o desempenho antes da publicação
* Limitar chamadas de fonte de dados externa a cenários essenciais
* Armazenar dados acessados com frequência em cache quando possível
* Revisar e otimizar o desempenho do delivery de mensagens

Saiba mais sobre [otimização de jornada](../start/guardrails.md).

+++

## Recursos adicionais

Para obter mais informações e atualizações, explore os seguintes recursos:

* [Introdução às jornadas](journey.md)
* [Criar a primeira jornada](journey-gs.md)
* [Guias de solução de problemas](troubleshooting.md)
* [Jornada casos de uso](jo-use-cases.md)
* [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
