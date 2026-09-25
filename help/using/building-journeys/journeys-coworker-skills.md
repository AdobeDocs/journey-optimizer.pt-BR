---
solution: Journey Optimizer
product: journey optimizer
title: Colaborador de jornadas
description: Descubra as habilidades do CX Enterprise Coworker disponíveis para criar, gerar conteúdo e analisar jornadas no Adobe Journey Optimizer, com orientação detalhada e prompts de amostra.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 932218c2-64c1-466e-afc4-120b6d8fe37f
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
    internal-label: Journey management
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
    internal-label: Journey design
source-git-commit: ccc5aca071477ef6ba6bd34cf609aeecaaae661c
workflow-type: tm+mt
source-wordcount: '2594'
ht-degree: 7%
---

# Colaborador de jornadas {#journeys-coworker-skills}

>[!BEGINSHADEBOX]

**Nesta página:** Descubra as habilidades do CX Enterprise Coworker disponíveis para jornadas no Adobe Journey Optimizer — criar jornadas a partir da linguagem natural, gerar conteúdo de canal e analisar o desempenho da jornada — com orientação detalhada, prompts de exemplo e práticas recomendadas para cada habilidade.

Saiba mais:

* [Habilidades de colega de trabalho para o Journey Optimizer](../start/ai-features.md#cx-coworker-skills) — visão geral das habilidades de colega em Jornadas, Fidelidade, Gerenciamento de conteúdo e Decisão no Journey Optimizer.
* [Documentação do colaborador](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — visão geral dos recursos de Campanhas, Chat e Projetos do colaborador.
* [Guia da interface de Chat do Colaborador](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — como acessar e navegar pelo Chat do Colaborador.

>[!ENDSHADEBOX]

## Criar jornada {#journey-create}

A Criação de jornadas permite que os usuários do Journey Optimizer criem e configurem jornadas de marketing usando uma interface de linguagem natural. Com a Criação de Jornadas, os profissionais podem criar jornadas rapidamente descrevendo seus requisitos em prompts de conversação. A habilidade orienta os usuários sobre as diferentes opções para criar uma jornada, permitindo que os profissionais de marketing se concentrem na estratégia em vez de na configuração técnica.

>[!AVAILABILITY]
>
>Você precisa das seguintes permissões para usar totalmente os recursos Criar do Jornada:
>
>**Gerenciar Jornadas**: esta permissão permite que você crie novas jornadas diretamente no Colaborador.
>
>**Exibir Eventos de Jornada, Fontes de Dados e Ações**: essa permissão garante que o Colaborador possa pesquisar por Eventos de Jornada e Ações Personalizadas.
>
>**Exibir segmentos**: essa permissão garante que o Colaborador possa pesquisar segmentos de público-alvo ao criar uma Jornada.
>
>**Gerenciar segmentos**: essa permissão permite que você crie novos públicos-alvo diretamente no Colaborador.

### Principais casos de uso

O Jornada Create oferece recursos que podem ser aproveitados para acelerar a execução de marketing:

* **Criação de jornada acionada por evento**

  * Crie jornadas que são ativadas com base em eventos específicos do cliente.
  * Projetar respostas automatizadas para ações do cliente em tempo real.
  * Crie fluxos de comunicação personalizados com base no comportamento do cliente.

  **jornada de visita à loja:**
  &quot;Crie uma jornada que começa quando um usuário entra no local da loja. Envie uma notificação por push para dar as boas-vindas aos usuários do armazenamento. Aguarde 2 dias e verifique se o usuário tem um endereço de email válido. Se o usuário tiver um endereço de email válido, envie uma pesquisa por email para perguntar sobre a experiência da loja. Se o usuário não tiver um endereço de email válido, envie uma notificação por push para solicitar o registro.&quot;

  **jornada pós-compra:**
  &quot;Crie uma jornada que começa quando um cliente faz uma compra online. Envie uma notificação por push para agradecer a compra. Em seguida, verifique se eles são membros do programa de fidelidade. Se o usuário for um membro do programa de fidelidade, envie uma segunda notificação por push com um código de desconto de 10%. Se o usuário não for um membro do programa de fidelidade, envie um push convidando-o a se inscrever no programa de fidelidade. Aguarde 2 dias e envie um push de acompanhamento com uma pesquisa sobre a experiência de compra deles.&quot;

  **Promoção baseada em eventos:**
  &quot;Criar uma jornada acionada quando a pontuação do jogo atingir 50. Envie uma mensagem SMS aos membros do programa de fidelidade dizendo que estão qualificados para receber uma fatia gratuita de pizza do patrocinador do parceiro.&quot;

* **Criação de jornada direcionada ao público-alvo**

  * Crie jornadas direcionadas a segmentos específicos do público-alvo.
  * Projete sequências de comunicação em várias etapas com tempo estratégico.

  **Campanha sazonal:**
  &quot;Eu quero criar uma jornada direcionada a um público de visitantes do dia. Quero enviar um email alertando esse público-alvo para minha próxima venda de fim de ano que inclui uma variedade de recursos básicos para caminhadas. Aguarde 3 dias após o envio do primeiro e-mail e envie um segundo e-mail que tenha um cupom de 15% com frete grátis. Aguarde 1 semana e envie uma 3ª mensagem de email para mostrar nosso novo saco de dormir e coleção de tendas. Programe a jornada para iniciar em 20/12.&quot;

  **Apreciação de fidelidade:**
  &quot;Crie uma jornada de apreciação de fidelidade para proprietários de SUVs, incluindo uma notificação por push de agradecimento com uma oferta gratuita de lavagem de carro e um lembrete de notificação por push de acompanhamento se a primeira notificação não tiver interação em até 1 dia.&quot;

* **Criação de jornada acionada por evento comercial**

  * Crie jornadas que são ativadas com base em um evento comercial específico e direcionem um público especificado (por exemplo, produto de volta ao estoque ou alteração de pontuação do jogo)
  * Acione mensagens oportunas e sensíveis ao contexto quando as condições dos negócios mudarem.

* **Criação de jornada de qualificação de público-alvo**

  * Crie jornadas que são ativadas quando os perfis entram ou saem de uma definição de segmento de público-alvo.
  * Automatize as mensagens de entrada e saída para oferecer suporte às metas de integração, retenção e retomada.

* **Fluxos de jornada condicionais**

  * Crie ramificações de decisão com base nos atributos do cliente.
  * Criar caminhos divididos que se adaptam às preferências do cliente.

* **Criar jornada a partir da imagem**

  * Carregue uma imagem de referência no Co-worker e peça para criar uma jornada usando a imagem como referência
  * A habilidade de criação de jornada extrairá um prompt editável da imagem de referência

Com essa habilidade, os requisitos de idioma natural são traduzidos em configurações de jornada estruturadas.

### Competências dentro do âmbito

Os seguintes recursos são compatíveis com a Criação de Jornada:

* **Criação de jornada de linguagem natural**: permite que os usuários descrevam o fluxo de jornada em linguagem de conversação.
* **jornadas baseadas em eventos e em público-alvo**: oferece suporte aos tipos de jornada baseados em acionadores e agendados, bem como à qualificação de eventos comerciais e públicos-alvo.
* **Lógica condicional**: lida com divisões de decisão e ramificações com base nos atributos do cliente.
* **Mensagens multicanais**: oferece suporte a notificações por push, email e canais SMS.
* **Agendamento de Jornada**: configura datas de início e tempo para jornadas agendadas.

### Habilidades fora do escopo

As seguintes funcionalidades não são compatíveis no momento:

* Análise de jornada avançada
* Orquestração entre jornadas
* Configuração de teste A/B
* Geração de expressão InAudience
* Nós de pesquisa do conjunto de dados
* Configurações de envio de onda
* Opções de recorrência do cronograma
* Seleção de namespace para públicos
* Mapeamento de campo de ação personalizada
* Transformações de dados complexas

### Solicitação de práticas recomendadas

Para maximizar a eficácia da Criação de Jornadas, siga estas práticas recomendadas:

* **Seja específico**: forneça detalhes claros sobre suas metas do jornada, público-alvo e ações desejadas. Inclua informações sobre canais, tempo e condições.
* **Especificar Tempo**: indique claramente os períodos de espera entre as ações e quando a jornada deve começar.
* **Definir condições**: ao usar a lógica condicional, explique os critérios para cada caminho de ramificação.
* **Incluir Canais**: especifique quais canais de comunicação você deseja usar (push, email, SMS).
* **Agendamento de menção**: para jornadas agendadas, forneça a data e a hora de início desejadas.
* **Ações personalizadas**: se você estiver usando ações personalizadas em seu fluxo de trabalho, será necessário especificar que você está usando uma ação personalizada, juntamente com o nome exato da ação personalizada. Exemplo:
Quando um usuário entrar no meu local de armazenamento, envie uma mensagem de boas-vindas usando a ação personalizada ExternalPush. Aguarde 2 dias e envie uma mensagem de acompanhamento usando a ação personalizada ExternalEmail com uma pesquisa em sua visita.
* **Validar expressões**: verifique e valide todas as expressões criadas pelas Habilidades do Jornada para garantir que os campos e valores corretos sejam usados.

### Configurar práticas recomendadas

* **Definir objetivos claros**: antes de criar jornadas, estabeleça metas claras (melhorar a retenção, gerar conversões, aumentar o engajamento).
* **Preparar públicos-alvo**: verifique se os públicos-alvo já foram criados e segmentados corretamente.
* **Conteúdo da Mensagem do Plano**: Defina sua estratégia de mensagens antes da criação da jornada.
* **Considere a Experiência do Cliente**: crie fluxos de jornada que respeitem as preferências do cliente e evitem a comunicação excessiva.

## Criação de conteúdo do canal {#channel-content-create}

>[!AVAILABILITY]
>
>Este recurso está disponível para todos os clientes com Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

A Criação de conteúdo de canal permite que os usuários do Journey Optimizer gerem, editem e gerenciem conteúdo específico de canal para jornada usando a geração de conteúdo habilitada por IA.

### Principais casos de uso

* **Geração de conteúdo específico do canal**: gere conteúdo para email, notificações por push, SMS e outros canais usando prompts de linguagem natural.

  &quot;Gerar conteúdo de email para minha jornada de boas-vindas. Crie um email de boas-vindas para novos clientes com um tom amigável e inclua uma oferta de desconto de 10%.&quot;

  &quot;Gerar uma notificação por push para minha jornada de visita à loja. Crie uma mensagem de boas-vindas que incentive os clientes a fazer o check-in e receber uma oferta especial.&quot;

  &quot;Gerar conteúdo de SMS para minha jornada acionada por evento. Crie uma mensagem curta notificando os clientes sobre uma venda rápida com um call-to-action.&quot;

* **Criação de conteúdo baseado em modelo**: procure e selecione entre os modelos disponíveis com recursos de visualização.

  &quot;Mostre-me os modelos de email disponíveis para a minha jornada de campanha sazonal.&quot;

  &quot;Selecione um modelo para meu email com um design moderno e limpo.&quot;

* **Gerenciamento de conteúdo multicanal**: gere e gerencie conteúdo para vários canais no mesmo fluxo de trabalho de jornada.

* **Edição de conteúdo em contexto**: abra o conteúdo gerado no Designer de Conteúdo para edição e refinamento.

  &quot;Abra o conteúdo do email no Designer de Conteúdo para que eu possa personalizar o design.&quot;

* **Refinamento e iteração de conteúdo**: gere novamente o conteúdo com tons ou estilos diferentes usando a ação Regenerar.

  &quot;Gere novamente o conteúdo da notificação por push com um tom mais casual.&quot;

  &quot;Atualize o conteúdo do email para incluir um código promocional.&quot;

* **Integração com a tela do Jornada**: selecione jornadas no inventário e exiba canais associados.

### Solicitação de práticas recomendadas

* **Seja específico**: forneça detalhes claros sobre o tipo de conteúdo, o tom, o público-alvo e as principais mensagens.
* **Especificar Canal**: indique claramente para qual canal você está criando conteúdo (email, push, SMS).
* **Definir Tom**: especifique o tom desejado (amigável, formal, casual, urgente).
* **Iterar e Refinar**: use a ação de regeneração para refinar o conteúdo até que ele atenda aos seus requisitos.

## Jornada análise {#journey-analyze}

As Habilidades de Jornada permitirão que os usuários do Journey Optimizer analisem e otimizem jornadas usando uma interface de linguagem natural. Com as Habilidades da Jornada, os profissionais podem identificar e resolver rapidamente conflitos de agendamento e/ou público-alvo, detectar pontos de abandono de usuários em uma jornada e fornecer insights ou recomendações. Ele capacita os profissionais a tomar decisões orientadas por dados, melhorar o envolvimento do cliente e simplificar a orquestração de jornadas.

>[!AVAILABILITY]
>
>As Habilidades de Jornada estão disponíveis para todos os clientes que têm acesso ao Colaborador. No entanto, você precisará das seguintes permissões para usar totalmente os recursos do Jornada Skills:
>
>**Exibir Jornadas**: essa permissão permite exibir insights sobre a jornada diretamente no Colaborador.
>
>**Gerenciar Jornadas**: esta permissão permite que você crie novas jornadas diretamente no Colaborador.
>
>**Exibir segmentos**: essa permissão permite que você visualize insights sobre os públicos-alvo diretamente no Colaborador.
>
>**Gerenciar segmentos**: essa permissão permite que você crie novos públicos-alvo diretamente no Colaborador.

### Principais casos de uso

O Jornada Analyze oferece uma variedade de funcionalidades que podem ser aproveitadas para otimizar esforços de marketing:

* **Análise de fallout da jornada**

  * Identifique onde e por que os clientes desistem durante uma jornada.
  * Detecte padrões no comportamento do cliente que levam ao desengajamento.
  * Use insights para refinar o design da jornada e melhorar a retenção.

  Exemplos de prompts:
  * &quot;Quero analisar o fallout por nó para a Campanha do jornada de 4 de julho.&quot;
  * &quot;Execute uma análise de fallout para a Campanha do jornada de 4 de julho.&quot;
  * &quot;O que é perda de perfil ao longo da Campanha de 4 de julho do jornada?&quot;
  * &quot;Mostrar onde os usuários estão saindo na Campanha do jornada de 4 de julho.&quot;

* **Análise de sobreposição de público-alvo da jornada**

  * Analise a sobreposição de público-alvo em diversas jornadas.
  * Evite a fadiga de público-alvo causada pelo excesso de direcionamento.
  * Otimize a segmentação para garantir um engajamento equilibrado.

  Exemplos de prompts:
  * &quot;Quais públicos-alvo são usados em mais de X jornadas?&quot;
  * &quot;Liste todas as jornadas usando o [nome do público-alvo].&quot;
  * &quot;Mostrar conflitos de sobreposição de público-alvo para a jornada [Nome da Jornada].&quot;
  * &quot;Mostrar públicos sobrepostos para a jornada [Nome da Jornada] e outras jornadas.&quot;

* **Análise de sobreposição de cronograma da jornada**

  * Detecte conflitos de data entre jornadas programadas que direcionam o mesmo público-alvo.
  * Evite o excesso de comunicação e melhore a eficiência do agendamento.
  * Maximize o impacto no público-alvo garantindo que as jornadas ocorram nos momentos ideais.

  Exemplos de prompts:
  * &quot;Há algum conflito de agendamento para a jornada [Nome da Jornada]?&quot;
  * &quot;Verifique se há conflitos de agendamento envolvendo o [Nome da Jornada] da jornada.&quot;
  * &quot;Destaque as sobreposições de agendamento entre a jornada [Nome da Jornada] e jornadas ativas.&quot;
  * &quot;A jornada [Nome da Jornada] está em conflito com alguma outra jornada?&quot;

* **Insights operacionais**

  * Insights do Jornada com base em prompts - Surja insights operacionais sobre o jornada, ou seja, &quot;mostrar todas as jornadas ativas para mim&quot;.

  Exemplos de prompts:
  * &quot;Quando o [Nome da Jornada] foi publicado?&quot;
  * &quot;Quando o [Nome da Jornada] foi interrompido?&quot;
  * &quot;Listar todas as jornadas atualmente no modo de teste&quot;
  * &quot;Quantas jornadas ao vivo eu tenho?&quot;
  * &quot;Forneça uma lista de todas as jornadas recorrentes agendadas e seus tempos de execução esperados.&quot;

* **Análise de Erro de Ação Personalizada de Jornada**

  * Identifique quando as ações personalizadas estão falhando ou quando as taxas de erro aumentam em uma jornada.
  * Diagnosticar as causas raiz antes que as falhas ocorram em uma interrupção mais ampla da jornada.
  * Use etapas de correção específicas para restaurar rapidamente a confiabilidade da ação personalizada.

  Exemplos de prompts:
  * &quot;Por que as ações personalizadas estão falhando na jornada [Nome da Jornada]?&quot;
  * &quot;Qual é a taxa de erro da ação personalizada [Nome da Ação Personalizada] na jornada [Nome da Jornada]?&quot;
  * &quot;Mostrar a causa raiz das falhas de ação personalizada na jornada [Nome da Jornada].&quot;
  * &quot;Há algum erro de ação personalizada afetando a jornada [Nome da Jornada] neste momento?&quot;

* **Analisar anomalias da Jornada**

  * Detecta picos, quedas ou linhas achatadas inesperados nas contagens de entrada, saída ou envio de mensagem de uma jornada em comparação às linhas de base históricas, inclusive quando a pergunta é colocada em torno do número de perfis que entram, saem ou concluem a jornada.
  * Confirme se uma alteração sinalizada é uma anomalia genuína usando uma verificação estatística determinística, em vez de depender apenas do sinalizador de anomalia bruta.
  * Execute diagnósticos limitados e somente leitura nos dados de execução da jornada para identificar uma causa raiz provável, identificando o que cada verificação procurou e encontrou junto com a recomendação.
  * Investigue alertas de anomalias que fazem referência a uma versão e um carimbo de data e hora específicos do jornada.

  Exemplos de prompts:
  * &quot;Por que as entradas da minha jornada de boas-vindas caíram ontem?&quot;
  * &quot;As saídas tiveram um pico na jornada de Abandono do carrinho esta semana?&quot;
  * &quot;Envios parecem baixos para a jornada Lembrete de Renovação hoje — o que aconteceu?&quot;
  * &quot;Por que houve uma queda repentina no número de perfis que entraram na minha jornada de agradecimento de aniversário de membros nos últimos 30 dias?&quot;
  * &quot;Menos perfis do que o normal estão concluindo minha jornada de Lembrete de Renovação este mês — por quê?&quot;
  * &quot;Um alerta de anomalia foi disparado para a jornada [ID da Versão da Jornada] em [carimbo de data/hora] — investigue.&quot;

* **Comparação de Versões do Jornada**

  * Compare duas versões do jornada no Chat do parceiro.
  * Revise uma comparação estruturada de nós adicionados, removidos, modificados e movidos com detalhes em nível de campo.
  * Identifique conexões alteradas, alterações de propriedade no nível da jornada e contagens acumuladas sem abrir o Journey Optimizer.

  >[!NOTE]
  >
  >No momento, a comparação no nível de atividade de ação para conteúdo de canal não é compatível. As alterações de conteúdo do canal são sinalizadas como **Não verificadas** até que esse recurso esteja disponível.

  Para obter mais detalhes sobre como gerenciar versões do jornada, consulte [versões do Jornada](publish-journey.md#journey-versions).

  Exemplos de prompts:
  * &quot;Compare as versões [Versão A] e [Versão B] da jornada [Nome da Jornada].&quot;
  * &quot;O que mudou entre essas duas versões da jornada [Nome da Jornada]?&quot;
  * &quot;Mostre-me os nós e as propriedades de jornada que foram alteradas entre as versões [Versão A] e [Versão B].&quot;

### Solicitação de práticas recomendadas

Para maximizar a eficácia do Jornada Analyze, siga estas práticas recomendadas:

* **Seja específico(a)**: use prompts claros e concisos para obter insights direcionados. Por exemplo, em vez de perguntar &quot;Quais são minhas jornadas?&quot;, especifique &quot;Listar todas as jornadas criadas no último mês&quot;.
* **Combinar insights**: integre insights dos recursos de Audience e Data Insights para obter uma visão holística do desempenho da jornada.
* **Refinamento iterativo**: use as análises de fallout e de sobreposição para refinar continuamente o design e o agendamento da jornada.

### Configurar práticas recomendadas

* **Defina objetivos claros**: antes de analisar as jornadas, estabeleça metas claras (por exemplo: melhorar a retenção, aumentar as conversões).
* **Monitore regularmente**: agende revisões regulares do desempenho da jornada para identificar tendências e anomalias.
* **Otimize a segmentação**: mantenha uma segmentação de público-alvo equilibrada para evitar fadiga e maximizar o engajamento.

## Simulação de jornada {#journey-simulation}

A habilidade Simulação de jornada leva a Simulação rápida orientada por IA à interface do chat, permitindo que os usuários validem a lógica de uma jornada conversacionalmente. Por meio do Colaborador, os usuários podem gerar dados de teste simulados, executar e gerenciar uma simulação e revisar os resultados.

### Principais casos de uso

1. **Gerar dados de teste simulados**

   * Gerar o mínimo de usuários simulados necessários para exercitar as ramificações da jornada.
   * Gere dados de evento para jornadas acionadas por evento, para que cada ramificação seja acionada.

1. **Executar e gerenciar simulações**

   * Iniciar uma execução de simulação.
   * Reinicializa uma execução de simulação.
   * Verifique o status de uma execução de simulação.
   * Listar os usuários simulados incluídos em uma execução.
   * Recuperar logs de execução.

1. **Revisar resultados da simulação**

   * Retorne resultados detalhados, incluindo a passagem passo a passo do caminho.
   * Retornar resultados da ramificação para a execução simulada.

### Limitações

No momento, esse recurso só oferece suporte ao fluxo de Simulação rápida e não substitui totalmente a experiência de simulação manual do Journey Optimizer.

Use a Simulação rápida para uma verificação rápida e automatizada da sanidade da lógica de uma jornada. Para obter controle granular sobre usuários e cenários simulados, use a [experiência de simulação manual no Journey Optimizer](simulate-journey-gs.md).

Como parte dessa experiência de Simulação rápida, os usuários não podem:

* Escolha um usuário simulado salvo existente para uma execução.
* Editar um usuário simulado antes de executar uma simulação novamente.
* Crie, navegue, atualize ou exclua usuários simulados persistentes por meio do chat.
* Direcione um caminho específico ou caso de teste personalizado.


{{$include /help/_includes/do-not-localize/start/ai-augmented-journeys-coworker-skills.md}}
