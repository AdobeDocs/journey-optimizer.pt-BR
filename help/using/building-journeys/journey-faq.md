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
source-git-commit: 32848633cdfb5683b45286fcdd22711a82d591b5
workflow-type: tm+mt
source-wordcount: '4094'
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

Sim. Use uma **atividade de condição** combinada com **atividades de espera**:

1. Adicionar uma atividade Wait (por exemplo, aguardar 3 dias)
2. Adicionar uma atividade de Condição verificando se o email foi aberto ou clicado
3. Criar dois caminhos:
   * **Se aberto/clicado**: encerre a jornada ou continue com as próximas etapas
   * **Se não for aberto/clicado**: enviar um email de lembrete com uma linha de assunto diferente

**Prática recomendada**: limitar o número de reenvios para evitar a exibição de spam (normalmente, um a dois lembretes no máximo).

Saiba mais sobre [eventos de reação](reaction-events.md).

+++

+++ Como criar uma jornada de abandono de carrinho?

Crie uma jornada acionada por eventos com lógica de espera e condição:

1. **Configurar um evento &quot;Carrinho Abandonado&quot;**: disparado quando itens são adicionados, mas o check-out não é concluído em um período
2. **Adicione uma atividade de espera**: aguarde de de 1 a 2 horas para dar ao cliente tempo para concluir naturalmente
3. **Adicionar uma Condição**: verifique se a compra foi concluída durante a espera
4. **Se não adquirido**: enviar um email de lembrete de abandono com conteúdo do carrinho
5. **Opcional**: adicione outra espera (24 horas) e envie um segundo lembrete com um incentivo (por exemplo, desconto de 10%)

Saiba mais sobre [casos de uso do jornada](jo-use-cases.md).

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
* **Aguardar até um horário específico**: use a atividade Aguardar para enviar mensagens em um horário específico no fuso horário local do recipient (por exemplo, 10 AM)

**Exemplo**: para enviar um email de &quot;Bom dia&quot; às 9h no fuso horário de cada cliente, use uma atividade de espera com &quot;Aguardar até uma data/hora fixa&quot; e habilite a opção de fuso horário.

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

Saiba mais sobre [opções de pausa de jornada](journey-pause.md).

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

* **Mensagem não aprovada**: o conteúdo da mensagem requer aprovação antes do envio
Solução: envie para aprovação ou verifique o status de aprovação

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

* &quot;Olá {{profile.firstName}}, obrigado pela sua compra do {{event.productName}}&quot;
* &quot;Com base no seu nível de fidelidade ({{profile.loyaltyTier}}), esta é uma oferta especial&quot;
* Blocos de conteúdo dinâmico que mudam com base nas preferências do cliente

Saiba mais sobre a [personalização](../personalization/personalize.md).

+++

+++ Posso enviar mensagens diferentes com base no canal preferido?

Sim. Use uma **Atividade de condição** para verificar o canal preferencial:

1. Adicionar uma condição verificando profile.preferredChannel
2. Crie caminhos separados para cada canal:
   * **Caminho de email**: enviar mensagem de email
   * **Caminho do SMS**: Enviar mensagem SMS
   * **Caminho de push**: enviar notificação por push
3. Adicionar um caminho padrão para perfis sem uma preferência

**Abordagem alternativa**: use **ações de vários canais** onde o Journey Optimizer seleciona automaticamente o melhor canal com base nas preferências e disponibilidade do perfil.

Saiba mais sobre [ações de canal](journeys-message.md).

+++

+++ Posso excluir determinados clientes da minha jornada?

Sim, há várias maneiras de excluir clientes:

**Na entrada da jornada**:

* Usar definições de público-alvo com regras de exclusão
* Adicionar condições de entrada que filtram perfis específicos
* Configurar requisitos de namespace

**Na jornada**:

* Adicione uma atividade de Condição no início da jornada para sair de perfis indesejados
* Verificar atributos de exclusão (por exemplo, status do VIP, contas de teste)
* Usar qualificação de público-alvo para identificar perfis a serem excluídos

**Exemplo de cenários de exclusão**:

* Excluir clientes que compraram recentemente
* Excluir clientes do VIP de promoções padrão
* Excluir funcionários e contas de teste
* Excluir clientes em regiões específicas

Saiba mais sobre [gerenciamento de entradas](entry-management.md) e [condições](condition-activity.md).

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

Sim. Use a **Atividade Otimizar** (disponível em pacotes Journey Optimizer específicos) ou crie divisões de teste manualmente:

**Usando a atividade Otimize**:

* Divide automaticamente o tráfego entre variantes
* Testa diferentes mensagens, ofertas ou caminhos de jornada inteiros
* Mede o desempenho e declara um vencedor

**Teste manual com Condição**:

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

+++ Posso pausar uma jornada para uma pessoa específica sem parar toda a jornada?

Embora não seja possível pausar uma jornada para perfis individuais diretamente, é possível obter resultados semelhantes:

**Opções**:

* **Adicionar ao público-alvo de exclusão**: crie um público-alvo de perfis para excluir e adicione uma condição verificando esse público-alvo em pontos estratégicos na jornada
* **Atualizar atributo de perfil**: Defina um sinalizador &quot;pausar&quot; no perfil e use condições para ignorar ações para perfis sinalizados
* **Ação personalizada**: use um sistema externo para rastrear perfis pausados e verificar o status por meio de uma chamada de API
* **Saída manual**: para casos urgentes, você pode remover perfis de teste manualmente

**Observação**: as alterações na Jornada afetam somente os novos participantes. Os perfis que já estão na jornada seguem o caminho original, a menos que a jornada seja totalmente interrompida.

+++

+++ Qual é a diferença entre uma Condição e uma atividade de Espera?

**Atividade de condição**:

* **Propósito**: cria caminhos diferentes com base na lógica (if/then)
* **Função**: avalia os dados e encaminha os perfis de acordo
* **Casos de uso**: segmentar clientes, verificar status, ramificação com base no comportamento
* **Exemplo**: se o cliente for o VIP, envie uma oferta premium; caso contrário, envie uma oferta padrão

**Atividade de espera**:

* **Propósito**: pausa a jornada por um período
* **Função**: mantém perfis em um ponto específico antes de continuar
* **Casos de uso**: intervalo entre mensagens, espera pelo horário comercial, criação de atrasos
* **Exemplo**: aguarde 3 dias após o email de boas-vindas antes de enviar a próxima mensagem

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
