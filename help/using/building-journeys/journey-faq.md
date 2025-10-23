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
source-git-commit: 4afd8e455ca0d61ad860ec735c30f1b36bb54e1b
workflow-type: tm+mt
source-wordcount: '4526'
ht-degree: 0%

---


# Perguntas frequentes {#faq-journeys}

Você encontrará abaixo as Perguntas frequentes sobre o Adobe Journey Optimizer Jornada.

Precisa de mais detalhes? Use as opções de feedback na parte inferior desta página para fazer sua pergunta ou conecte-se com a [comunidade Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## Conceitos gerais

+++ O que é uma jornada no Adobe Journey Optimizer?

Uma jornada é uma orquestração de várias etapas que permite projetar e executar experiências do cliente em tempo real em vários canais. As jornadas combinam eventos, atividades de orquestração, ações e mensagens para criar experiências personalizadas e contextuais com base no comportamento do cliente e em eventos comerciais.

Saiba mais sobre [jornadas](journey.md).

+++

+++ Quais são os diferentes tipos de jornadas?

O Adobe Journey Optimizer é compatível com quatro tipos de jornadas:

* **jornadas Unitárias**: acionadas individualmente por um evento (por exemplo, uma compra, entrada no aplicativo). Os perfis são inseridos um de cada vez na jornada quando o evento ocorre.
* **Ler jornadas de Público-Alvo**: Inicie com um público-alvo do Adobe Experience Platform e envie mensagens em lote para todos os perfis desse público-alvo.
* **jornadas de qualificação de público-alvo**: acionadas quando os perfis se qualificam para (ou saem de) um segmento de público-alvo específico. Os perfis entram na jornada conforme atendem aos critérios de público-alvo.
* **jornadas de eventos comerciais**: acionadas por eventos comerciais (por exemplo, atualizações de ações, alertas meteorológicos) que afetam vários perfis simultaneamente.

Saiba mais sobre [tipos de jornada](entry-management.md#types-of-journeys).

+++

+++ Qual é a diferença entre uma jornada e uma campanha?

jornada **[As](journey.md)** são orquestrações de várias etapas que reagem a eventos ou públicos-alvo, permitindo lógica complexa, condições, tempos de espera e vários pontos de contato ao longo do ciclo de vida do cliente.

**[Campanhas](../campaigns/get-started-with-campaigns.md)** vêm em três tipos:

* **[Campanhas de ação](../campaigns/create-campaign.md)**: comunicações únicas ou recorrentes enviadas a um público específico, ideais para mensagens autônomas, como anúncios promocionais ou boletins informativos.
* **[Campanhas acionadas por API](../campaigns/api-triggered-campaigns.md)**: campanhas acionadas por meio de chamadas de API, permitindo a integração com sistemas externos para enviar mensagens com base em eventos em tempo real ou lógica de negócios.
* **[Campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md)**: campanhas baseadas em público, em várias etapas, criadas em uma tela que pode incluir condições, tempos de espera e várias ações para criar experiências programadas e coordenadas.

**Prática recomendada**: use o [jornada](journey.md) para envolvimento complexo acionado por eventos com orquestração avançada; [campanhas de ação](../campaigns/create-campaign.md) para comunicações agendadas baseadas em público; [campanhas acionadas por API](../campaigns/api-triggered-campaigns.md) para acionamento programático de sistemas externos; e [campanhas orquestradas](../orchestrated/gs-orchestrated-campaigns.md) para comunicações em várias etapas com requisitos específicos de campanha.

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

+++ Como posso escolher entre uma jornada unitária e uma jornada de público-alvo de leitura?

Usar **jornadas unitárias** quando:

* Você precisa reagir às ações individuais do cliente em tempo real (por exemplo, confirmação de compra, abandono do carrinho)
* Cada cliente deve seguir seu próprio ritmo
* Acione com base em eventos específicos

Usar **jornadas de leitura de público-alvo** quando:

* Você está enviando comunicações em lote para um grupo (por exemplo, informativo mensal, campanhas promocionais)
* Todos os clientes devem receber a mensagem quase ao mesmo tempo
* Você está direcionando um segmento de público-alvo predefinido

+++

## Criação de jornadas

+++ Como começar a criar minha primeira jornada?

Siga estas etapas principais:

1. **Configurar pré-requisitos**: configure eventos, fontes de dados e ações conforme necessário
2. **Criar a jornada**: navegue até o menu Jornadas e clique em &quot;Criar Jornada&quot;
3. **Definir propriedades da jornada**: Defina o nome, a descrição e outras configurações da jornada
4. **Criar a jornada**: arraste e solte atividades da paleta na tela
5. **Testar a jornada**: use o modo de teste para validar a lógica de jornada
6. **Dry run da jornada**: use Dry run para testar a jornada usando dados de produção reais sem entrar em contato com clientes reais ou atualizar informações de perfil
7. **Publicar a jornada**: ative a jornada para ativá-la

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

Sim, há várias abordagens para aproveitar dados externos:

**Práticas recomendadas**:

* **Ações personalizadas**: chame APIs externas por meio de ações personalizadas para recuperar ou enviar dados para sistemas de terceiros. Essa é a abordagem recomendada para interações em tempo real com sistemas externos.
* **Pesquisa de conjunto de dados**: se você puder carregar dados de sistemas externos na Adobe Experience Platform, use o recurso de pesquisa de conjunto de dados para recuperar informações armazenadas em conjuntos de dados do Experience Platform.
* **Fontes de dados externas**: configure-as para recuperar informações de serviços de API de terceiros (menos recomendado do que as abordagens acima).

Essas opções permitem enriquecer a experiência do cliente com dados do seu CRM, sistemas de fidelidade, serviços meteorológicos ou outras plataformas externas.

Saiba mais sobre [ações personalizadas](using-custom-actions.md) e [pesquisa de conjunto de dados](dataset-lookup.md).

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

Para canais sem suporte nativo, você pode usar **ações personalizadas** para integrar-se a plataformas de mensagens externas e enviar mensagens por meio de qualquer canal de terceiros.

Saiba mais sobre [mensagens no jornada](journeys-message.md) e [ações personalizadas](using-custom-actions.md).

+++

+++ Como faço para esperar um horário ou evento específico em uma jornada?

Use a **Atividade de espera** para pausar a jornada por uma duração especificada ou até uma data/hora específica. As atividades de espera são úteis para:

* Envio de mensagens de acompanhamento após um atraso (por exemplo, 3 dias após a compra)
* Criar campanhas de gotejamento com intervalos de tempo
* Combinação com condições para criar cenários de tempo limite

Saiba mais sobre [atividades de espera](wait-activity.md).

+++

+++ Posso atualizar as informações de perfil em uma jornada?

Sim. Use a atividade **Atualizar Perfil** para modificar atributos de perfil no Adobe Experience Platform com base em eventos ou condições de jornada. Isso é útil para atualizar pontos de fidelidade, registrar marcos de jornada, alterar configurações de preferências ou rastrear pontuações de engajamento do cliente.

Saiba mais sobre [atualizações de perfil](update-profiles.md).

+++

+++ Como faço para enviar um email imediatamente depois que alguém faz uma compra?

Criar uma **jornada unitária acionada por evento**:

1. Configurar um evento de &quot;Compra&quot; com os detalhes do pedido
2. Adicione o evento como ponto de entrada de jornada
3. Siga imediatamente com uma ação de Email
4. Projete o email de confirmação do pedido com detalhes personalizados do pedido
5. Publicar a jornada

A jornada será acionada automaticamente sempre que um evento de compra for recebido, enviando o email de confirmação em tempo real.

Saiba mais sobre [configuração de evento](../event/about-events.md) e [ações de email](journeys-message.md).

+++

+++ Posso reenviar uma mensagem se alguém não abrir ou clicar nela?

Sim. Usar um **Evento de reação** com um **Tempo limite**:

1. Após enviar a mensagem, adicione um evento de reação que escuta aberturas ou cliques de email
2. Configurar um período de tempo limite (por exemplo, 3 dias) no evento de reação
3. Criar dois caminhos:
   * **Se aberto/clicado**: continuar com as próximas etapas ou finalizar a jornada
   * **Caminho de tempo limite (não aberto/clicado)**: envia um email de lembrete com outra linha de assunto

**Prática recomendada**: limitar o número de reenvios para evitar a exibição de spam (normalmente, um a dois lembretes no máximo).

Saiba mais sobre [eventos de reação](reaction-events.md).

+++

+++ Como criar uma jornada de abandono de carrinho?

Criar uma jornada acionada por evento usando um evento de reação com um tempo limite:

1. **Configurar um evento &quot;Carrinho Abandonado&quot;**: disparado quando itens são adicionados, mas o check-out não é concluído em um período
2. **Adicionar um evento de reação**: configure-o para ouvir um evento de compra
3. **Definir um período de tempo limite**: defina um tempo limite (por exemplo, 1-2 horas) no evento Reação para dar ao cliente tempo para concluir naturalmente
4. **Criar dois caminhos**:
   * **Se o evento de compra ocorrer**: encerre a jornada ou continue com o fluxo pós-compra
   * **Caminho de tempo limite (sem compra)**: envia um email de lembrete de abandono com o conteúdo do carrinho
5. **Opcional**: adicione outro evento de Reação com tempo limite (24 horas) e envie um segundo lembrete com um incentivo (por exemplo, desconto de 10%)

Saiba mais sobre [casos de uso do jornada](jo-use-cases.md) e [eventos de reação](reaction-events.md).

+++

+++ Como dividir clientes em caminhos diferentes com base em seu histórico de compras?

Use uma **Atividade de condição** com associação de público-alvo ou atributos de perfil:

1. Adicionar uma atividade de Condição à jornada
2. Criar vários caminhos com base em critérios:
   * **Caminho 1**: clientes de alto valor (compras totais > $1000)
   * **Caminho 2**: Clientes comuns (compras totais de US$ 100 a US$ 1.000)
   * **Caminho 3**: novos clientes (total de compras &lt; US$ 100)
3. Adicionar mensagens ou ofertas diferentes para cada caminho

Saiba mais sobre [condições](condition-activity.md) e [qualificação de público-alvo](audience-qualification-events.md).

+++

+++ Como gerenciar fusos horários diferentes na jornada?

O Journey Optimizer fornece várias opções para o gerenciamento de fuso horário:

* **Fuso horário do perfil**: as mensagens são enviadas com base no fuso horário de cada indivíduo armazenado em seu perfil
* **Fuso horário fixo**: todas as mensagens usam um fuso horário específico definido por você

Saiba mais sobre o [gerenciamento de fuso horário](timezone-management.md).

+++

+++ Por quanto tempo devo esperar entre mensagens na minha jornada?

**Práticas recomendadas para tempos de espera**:

* **Mensagens transacionais** (confirmações de pedidos): enviar imediatamente
* **Série de boas-vindas**: 1 a 3 dias entre emails
* **Conteúdo educacional**: 3 a 7 dias entre mensagens
* **Campanhas promocionais**: pelo menos 7 dias entre ofertas
* **Reengajamento**: 14 a 30 dias para usuários inativos

**Fatores a serem considerados**:

* Padrões do setor e expectativas dos clientes
* Urgência e importância da mensagem
* Sua frequência geral de mensagens em todos os canais
* Padrões de engajamento do cliente

**Dica**: use as regras de limite de jornada para limitar o número total de mensagens recebidas por um cliente em todas as jornadas.

Saiba mais sobre [atividades de espera](wait-activity.md) e [limite de jornada](../conflict-prioritization/journey-capping.md).

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

* A jornada fica **Ativa** e pronta para aceitar novos perfis
* Perfis podem ser inseridos com base nos critérios de entrada (evento ou público)
* Mensagens e ações começam a ser executadas para perfis que se movem pela jornada
* Você só pode editar itens limitados em uma jornada publicada (é necessário criar uma nova versão se desejar editar mais)

Saiba mais sobre [publicação de jornadas](publishing-the-journey.md).

+++

+++ Posso modificar uma jornada já publicada?

Sim, mas com limitações. É possível editar determinados elementos de uma jornada em tempo real:

**O que você pode editar**:

* Jornada propriedades (nome, descrição)
* Conteúdo da mensagem em atividades de mensagem existentes
* Algumas configurações de jornada

**O que você não pode editar**:

* Estrutura de jornada (adição/remoção de atividades)
* Condições de entrada
* Jornada lógica da tela

**Para fazer alterações estruturais**:

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
* **Pausar**: interromper temporariamente a jornada e retomá-la mais tarde

Saiba mais sobre o [encerramento de jornadas](end-journey.md).

+++

+++ Qual é a diferença entre &quot;Fechar para novas entradas&quot; e &quot;Parar&quot;?

**Fechar para novas entradas**:

* Novos perfis não podem entrar na jornada
* Os perfis que já estão na jornada continuam e concluem o caminho
* Use isso quando quiser direcionar uma jornada
* Exemplo: uma campanha sazonal que terminou, mas você deseja que os clientes existentes concluam sua experiência

**Parar**:

* Encerra imediatamente a jornada para todos os perfis
* Todos os perfis que estão na jornada foram encerrados
* Use isso para situações urgentes ou erros críticos
* Exemplo: recall de produto exigindo interrupção imediata das mensagens promocionais

Saiba mais sobre [como encerrar jornadas](end-journey.md) e [como publicar jornadas](publishing-the-journey.md).

+++

## Execução e monitoramento do Jornada

+++ Como posso rastrear o progresso do perfil em uma jornada?

É possível monitorar a execução da jornada usando:

* **Relatório ao vivo da Jornada**: visualize métricas e KPIs em tempo real para sua jornada. Você também pode analisar os resultados da execução do teste de simulação aqui.
* **Relatório de Tempo Total de Jornada**: analise o desempenho da jornada usando o Customer Journey Analytics. Você também pode analisar os resultados da execução do teste de simulação aqui.
* **Eventos de Etapa de Jornada**: acesse dados de execução detalhados para relatórios personalizados

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
* **Modo de simulação**: teste a jornada usando dados de produção reais sem entrar em contato com os clientes para validar o direcionamento e a execução
* **Relatórios de Jornada**: revise as métricas de execução para encontrar afunilamentos ou erros
* **Jornada eventos de etapa**: analise dados de execução detalhados para entender o comportamento do perfil

**Problemas comuns**:

* Eventos ou públicos configurados incorretamente
* Conexões de fonte de dados ausentes
* Expressões inválidas em condições ou personalização
* Configurações de tempo limite muito curtas

Saiba mais sobre [jornadas de solução de problemas](troubleshooting.md).

+++

<!--
+++ What happens if an action fails in a journey?

When an action fails (e.g., API call timeout, message delivery error), the journey continues by default unless configured otherwise. You can define condition activities to handle failure scenarios, and errors are logged in journey reports and step events for monitoring.

**Best practice**: Set appropriate timeout values for external actions and define alternative paths for critical failure scenarios.

Learn more about [action responses](../action/action-response.md).

+++
-->

+++ Posso ver quem está atualmente na minha jornada?

Sim. Use o **Relatório de Jornada ao Vivo** para exibir:

* Número de perfis atualmente na jornada
* Número de perfis em cada atividade
* Perfis que entraram nas últimas 24 horas
* Métricas de execução em tempo real

Para ver perfis individuais, use **jornada eventos de etapa** no Customer Journey Analytics ou consultar os conjuntos de dados de evento de etapa diretamente.

Saiba mais sobre o [jornada live reporting](report-journey.md).

+++

+++ Por que minhas mensagens não estão sendo enviadas na minha jornada?

**Razões e soluções comuns**:

* **Problemas de consentimento**: os destinatários não optaram por receber comunicações
Solução: verifique as políticas de consentimento e o status de aceitação

* **Lista de supressão**: endereços de email estão na lista de supressão
Solução: revise a lista de supressão para devoluções ou reclamações

* **Informações de contato inválidas**: endereços de email/números de telefone ausentes ou malformados
Solução: valide a qualidade dos dados do perfil

* **Jornada não publicada**: a jornada ainda está no modo de rascunho
Solução: publique a jornada para ativá-la

<!-- 
* **Message not approved**: Message content requires approval before sending
  Solution: Submit for approval or check approval status-->

* **Problema de configuração de canal**: a configuração de email/SMS está incorreta
Solução: verifique as configurações e a autenticação do canal

Saiba mais sobre [solução de problemas](troubleshooting.md) e [gerenciamento de consentimento](../action/consent.md).

+++

+++ Como personalizar mensagens na minha jornada?

Você pode personalizar mensagens usando o **editor de personalização**:

**Dados de personalização disponíveis**:

* **Atributos do perfil**: nome, sobrenome, email, campos personalizados
* **Dados do evento**: detalhes da compra, comportamento de navegação, atividade do aplicativo
* **Dados contextuais**: variáveis de Jornada, dados de API externos
* **Associação de público-alvo**: qualificações de segmento
* **Atributos computados**: valores pré-calculados

**Exemplo de personalização**:

* &quot;Olá `{{profile.firstName}}`, obrigado pela sua compra do `{{event.productName}}`&quot;
* &quot;Com base no seu nível de fidelidade (`{{profile.loyaltyTier}}`), esta é uma oferta especial&quot;
* Blocos de conteúdo dinâmico que mudam com base nas preferências do cliente

Saiba mais sobre a [personalização](../personalization/personalize.md).

+++

+++ Posso enviar mensagens diferentes com base no canal preferido?

Sim. Use uma **[Atividade de condição](condition-activity.md)** para rotear perfis com base em seu canal preferido:

1. Adicione uma [Atividade de condição](condition-activity.md) à sua jornada
2. Crie um caminho para cada canal verificando o atributo de perfil de canal preferido (por exemplo, `profile.preferredChannel`)
3. Configurar caminhos específicos do canal:
   * **Caminho de email**: adicionar uma [ação de email](../email/create-email.md) com conteúdo otimizado para email
   * **Caminho do SMS**: adicionar uma [ação de SMS](../sms/create-sms.md) com mensagens concisas
   * **Caminho de push**: adicionar uma [ação de notificação por push](../push/create-push.md) com conteúdo curto e acionável
   * **Caminho no aplicativo**: adicionar uma [ação de mensagem no aplicativo](../in-app/create-in-app.md) para usuários engajados do aplicativo
4. Adicione um caminho padrão para perfis sem uma preferência, roteando-os para o canal principal

**Práticas recomendadas**:

* Verifique se os dados do seu perfil incluem preferências de canal precisas
* Projete o conteúdo apropriado para os pontos fortes e limitações de cada canal
* Usar [superfícies de canal](../configuration/channel-surfaces.md) para gerenciar configurações de canal
* Testar todos os caminhos para garantir a entrega adequada da mensagem

Saiba mais sobre [condições](condition-activity.md), [ações de mensagem](journeys-message.md) e [seleção de canal](../channels/gs-channels.md).

+++

+++ Posso excluir determinados clientes da minha jornada?

Sim, há várias maneiras de excluir clientes:

**Na entrada da jornada**:

* Usar [definições de público-alvo](../audience/creating-a-segment-definition.md) com regras de exclusão
* Adicionar [condições de entrada](entry-management.md) que filtram perfis específicos
* Configure [o atributo de perfil com base nos critérios de saída](journey-properties.md) nas propriedades do jornada para excluir automaticamente perfis com base em atributos específicos

**Na jornada**:

* Adicione uma [Atividade de condição](condition-activity.md) no início da jornada para sair de perfis indesejados
* Verificar atributos de exclusão (por exemplo, status do VIP, contas de teste)
* Use a [qualificação de público-alvo](audience-qualification-events.md) para identificar perfis a serem excluídos

**Exemplo de cenários de exclusão**:

* Excluir clientes que compraram recentemente
* Excluir clientes do VIP de promoções padrão
* Excluir funcionários e contas de teste
* Excluir clientes em regiões específicas

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
* **Identificador complementar**: use uma ID complementar para permitir que os perfis insiram novamente a jornada várias vezes para entidades diferentes (por exemplo, pedidos, reservas ou transações diferentes), mesmo que já estejam na jornada

**Prática recomendada**: usar regras de reentrada para evitar a fadiga da mensagem e garantir o ritmo apropriado. Considere o uso de identificadores complementares para jornadas transacionais em que os perfis precisam inserir várias vezes para transações diferentes.

Saiba mais sobre [gerenciamento de entradas](entry-management.md) e [identificadores suplementares](supplemental-identifier.md).

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

O **limite de Jornada** permite controlar como os perfis interagem com o jornada, evitando a fadiga da mensagem e garantindo uma experiência ideal para o cliente:

* **Limite de entrada**: limitar o número de vezes que um perfil pode inserir jornadas dentro de um período de tempo especificado
* **Limite de simultaneidade**: limitar o número de jornadas que um perfil pode ter simultaneamente

Você pode definir o máximo de entradas ou simultaneidade por perfil em jornadas ou jornadas específicas, definir janelas de tempo (diariamente, semanalmente, mensalmente) e priorizar jornadas quando várias jornadas competem pelo mesmo perfil.

Saiba mais sobre [limite de jornada](../conflict-prioritization/journey-capping.md).

+++

+++ Posso integrar minha jornada a sistemas externos?

Sim. Use **ações personalizadas** para chamar APIs de terceiros (CRM, automação de marketing, sistemas de fidelidade), enviar dados para sistemas externos, recuperar informações em tempo real para decisões e acionar fluxos de trabalho em plataformas externas.

As ações personalizadas oferecem suporte à autenticação (chave de API, autenticação personalizada), personalização de carga de solicitação/resposta, tratamento de erros e tempos limite e parâmetros dinâmicos do contexto de jornada.

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

+++ Como criar uma jornada de série de boas-vindas?

Uma série de boas-vindas típica inclui vários pontos de contato ao longo de vários dias:

**Exemplo de estrutura**:

1. **Entrada**: Público-alvo de novos assinantes ou evento quando alguém se inscrever
2. **Email 1 - Boas-vindas imediatas**: obrigado e introdução
3. **Aguardar**: 2 dias
4. **Email 2 - Introdução**: tutorial ou guia do produto
5. **Aguardar**: 3 dias
6. **Condição**: o cliente fez uma compra?
   * **Sim**: encerrar ou mover para a jornada do cliente
   * **Não**: continuar série de boas-vindas
7. **Email 3 - Incentivo**: desconto especial para compradores pela primeira vez
8. **Aguardar**: 5 dias
9. **Email 4 - Envolvimento**: best-sellers ou conteúdo popular

**Práticas recomendadas**:

* Mantenha-o em 3-5 emails em 2-3 semanas
* Cada email deve ter uma finalidade clara e o call-to-action
* Monitore as taxas de abertura e ajuste o tempo/conteúdo de acordo
* Saia dos clientes antecipadamente se eles se converterem ou se engajarem profundamente

Saiba mais sobre [casos de uso do jornada](jo-use-cases.md).

+++

+++ Posso testar caminhos diferentes A/B na minha jornada?

Sim. Use a **Atividade Otimizar** (Disponibilidade Limitada) ou crie manualmente divisões de teste:

**Usando a atividade Otimize** com o método Experiment:

* Divide aleatoriamente o tráfego entre caminhos diferentes para determinar qual tem o melhor desempenho
* Testa diferentes mensagens, ofertas, tempos de espera ou caminhos de jornada inteiros
* Mede o desempenho com base em métricas de sucesso predefinidas e declara um vencedor

**Usando a atividade Otimize** com o método de condição da fonte de dados:

* Criar uma condição que divide aleatoriamente os perfis (por exemplo, usando uma função de número aleatório)
* Enviar experiências diferentes para cada divisão
* Medir resultados usando relatórios de jornada

**O que você pode testar**:

* Diferentes linhas de assunto de email
* Conteúdo alternativo da mensagem
* Diferentes tempos de espera
* Várias ofertas ou incentivos
* Caminhos de jornada totalmente diferentes

Saiba mais sobre [otimizar atividade](optimize.md) e [experimentos de conteúdo](../content-management/content-experiment.md).

+++

+++ Como faço para acionar uma jornada quando o inventário está baixo?

Criar uma **jornada de eventos comerciais**:

1. **Configurar um evento comercial**: configure um evento acionado pelo sistema de inventário quando o estoque ficar abaixo de um limite
2. **Selecionar público-alvo**: escolha perfis para notificar (por exemplo, clientes que visualizaram o produto, assinantes para reabastecer alertas)
3. **Adicionar ação de mensagem**: enviar email de notificação ou push
4. **Personalizar conteúdo**: incluir detalhes do produto, nível de estoque atual, mensagens de urgência

**Exemplo de eventos comerciais**:

* Alerta de baixo inventário
* Notificação de queda de preço
* Produto em estoque
* Anúncio de venda do Flash
* Promoções baseadas no clima

Saiba mais sobre [eventos comerciais](general-events.md).

+++

+++ O que são políticas de mesclagem e como elas afetam as jornadas?

As **políticas de mesclagem** determinam como o Adobe Experience Platform combina dados de várias fontes para criar uma exibição de perfil unificada. Eles definem regras para a priorização de dados e a identificação quando fragmentos de perfil existem em diferentes conjuntos de dados.

**Impacto no jornada**:

* As jornadas usam a política de mesclagem associada ao público ou evento para determinar quais dados de perfil estão disponíveis
* A política de mesclagem afeta quais atributos e identidades estão acessíveis em condições de jornada, personalização e ações
* Diferentes políticas de mesclagem podem resultar na utilização de diferentes dados de perfil na jornada

**Práticas recomendadas**:

* Verifique se a política de mesclagem usada pela jornada está alinhada aos requisitos de governança de dados
* Entenda quais conjuntos de dados estão incluídos em sua política de mesclagem para saber quais dados estão disponíveis
* Use políticas de mesclagem consistentes em públicos-alvo e jornadas relacionados para obter resultados previsíveis

Saiba mais sobre [políticas de mesclagem](../audience/get-started-profiles.md) e [gerenciamento de identidade](../audience/get-started-identity.md).

+++

+++ Qual é a diferença entre uma Condição e uma atividade de Espera?

| | **Atividade de Condição** | **Atividade de espera** |
|---|---|---|
| **Propósito** | Cria caminhos diferentes com base na lógica (if/then) | Pausa a jornada por um período |
| **Função** | Avalia dados e roteia perfis de acordo | Mantém os perfis em um ponto específico antes de continuar |
| **Caso de uso** | Segmentar clientes, verificar status, ramificação com base em comportamento | Tempo entre mensagens, espera pelo horário comercial, criação de atrasos |
| **Exemplo** | Se o cliente for a VIP, enviar oferta premium; caso contrário, enviar oferta padrão | Aguardar 3 dias após o email de boas-vindas antes de enviar a próxima mensagem |

**Eles trabalham juntos**:

* Aguarde um período e use uma Condição para verificar se algo aconteceu durante a espera
* Exemplo: aguarde 7 dias e, em seguida, verifique se o cliente fez uma compra

Saiba mais sobre [condições](condition-activity.md) e [atividades de espera](wait-activity.md).

+++

## Práticas recomendadas e limitações

+++ Quais são as principais limitações que eu devo conhecer?

As medidas de proteção importantes incluem:

* **Complexidade da Jornada**: máximo de atividades, caminhos e níveis de aninhamento
* **Taxa de transferência**: taxas de envio de mensagem e limites de chamada de API
* **Vida útil**: duração máxima da jornada (por exemplo, 91 dias)
* **Tamanho do público-alvo**: limites nos tamanhos de lote de públicos-alvo de leitura
* **Complexidade de expressão**: limites de caracteres em condições e personalização

Exibir [medidas de proteção e limitações](../start/guardrails.md) concluídas.

+++

+++ Quais são as práticas recomendadas para o design de jornadas?

**Estrutura e organização**:

* Mantenha o foco das jornadas em casos de uso específicos
* Usar nomenclatura descritiva para atividades
* Adicionar descrições e rótulos para lógica complexa
* Agrupar jornadas relacionadas com tags

**Desempenho**:

* Otimizar os tempos de espera para equilibrar o envolvimento e o volume
* Limitar chamadas de API externas a casos de uso essenciais
* Usar regras de limite para evitar a fadiga da mensagem
* Monitorar métricas de jornada regularmente

**Testando**:

* Sempre testar jornadas antes de publicar
* Usar o modo de teste para validar a lógica da jornada e percorrer a jornada
* Use o modo de simulação para testar com dados reais de produção sem entrar em contato com os clientes
* Testar todos os caminhos e cenários condicionais
* Usar perfis de teste realistas
* Validar personalização e conteúdo dinâmico

**Manutenção**:

* Analisar regularmente o desempenho da jornada
* Parar ou fechar jornadas não usadas
* Lógica de jornada de documentos e regras de negócios
* Plano para controle de versão do jornada

Saiba mais sobre [práticas recomendadas de design do jornada](using-the-journey-designer.md).

+++

+++ Quantas atividades posso adicionar a uma jornada?

As jornadas são limitadas a no máximo 50 atividades. No entanto, recomendamos manter suas jornadas mais simples para melhorar a capacidade de manutenção e o desempenho.

À medida que as jornadas se aproximam de 50 atividades, elas podem se tornar muito complexas e difíceis de manter, solucionar problemas e entender. Grandes jornadas com muitas ramificações e condições também podem afetar o tempo de processamento, a legibilidade e a colaboração em equipe.

**Prática recomendada**: mantenha suas jornadas concentradas e gerenciáveis. Se sua jornada estiver se tornando complexa, considere:

* Dividindo-o em várias jornadas usando a atividade Jump
* Criação de padrões reutilizáveis em jornadas mais simples
* Simplificação da lógica com condições mais eficientes
* Verificar se todas as atividades são necessárias

Saiba mais sobre [design do jornada](using-the-journey-designer.md) e [medidas de proteção e limitações](../start/guardrails.md).

+++

+++ Como garantir que minha jornada tenha bom desempenho em escala?

**Considerações sobre o design**:

* Use [entrada baseada em público-alvo](read-audience.md) para comunicações em lote em vez de eventos individuais
* Implementar os [tempos de espera](wait-activity.md) apropriados para difundir o volume de mensagens
* Aproveite as [regras de limitação](../conflict-prioritization/journey-capping.md) para evitar sobrecarga do sistema
* Otimizar a [lógica de condição](condition-activity.md) para reduzir a complexidade do processamento

**Monitoramento**:

* Rastrear [métricas de jornada](report-journey.md) regularmente
* Monitorar o desempenho da API para [ações personalizadas](using-custom-actions.md)
* Revise taxas de erro e ocorrências de tempo limite usando [ferramentas de solução de problemas](troubleshooting.md)
* Assinar [alertas de jornada](../reports/alerts.md) falhas críticas de jornada

**Otimização**:

* Use o [modo de teste](testing-the-journey.md) e a [execução a seco](journey-dry-run.md) para validar o desempenho antes da publicação
* Minimize chamadas de API externas por meio de [ações personalizadas](using-custom-actions.md) para evitar latência e dependência em sistemas de terceiros
* Armazene dados usados com frequência no Adobe Experience Platform usando [pesquisa de conjunto de dados](dataset-lookup.md) em vez de fazer chamadas externas, quando possível
* Revisar e otimizar o desempenho da [entrega de mensagens](journeys-message.md)

Saiba mais sobre [medidas de proteção e limitações](../start/guardrails.md).

+++

## Recursos adicionais

Para obter mais informações e atualizações, explore os seguintes recursos:

* [Introdução às jornadas](journey.md)
* [Criar a primeira jornada](journey-gs.md)
* [Guias de solução de problemas](troubleshooting.md)
* [Jornada casos de uso](jo-use-cases.md)
* [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
