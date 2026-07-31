---
solution: Journey Optimizer
product: journey optimizer
title: Habilidades do Journey Optimizer no CX Co-worker
description: Descubra as habilidades do Adobe Journey Optimizer disponíveis no CX Co-worker, com orientações detalhadas e prompts de amostra.
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 2
source-git-commit: 7f60cb8e5c7fe9140ee0689d53e12aba7ade3a3b
workflow-type: tm+mt
source-wordcount: '2969'
ht-degree: 7%

---


# Habilidades do Journey Optimizer no CX Co-worker {#ajo-coworker-skills}

>[!BEGINSHADEBOX]

**Nesta página:** Descubra as habilidades do Adobe Journey Optimizer disponíveis no CX Co-worker — desde a criação e análise de jornadas até a geração de conteúdo de canal — com orientação detalhada, prompts de exemplo e práticas recomendadas para cada habilidade.

>[!ENDSHADEBOX]

## Visão geral {#overview}

O CX Co-worker traz recursos alimentados por IA para a Adobe Journey Optimizer. O [CX Coworker](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-coworker/content/home){target="_blank"} é a experiência de conversação da Adobe que se integra aos seus aplicativos de negócios para ajudá-lo a trabalhar com mais eficiência.

Com suas habilidades alimentadas por IA, o CX Co-worker permite que os usuários do Journey Optimizer criem, analisem e otimizem jornadas de marketing usando uma interface de linguagem natural. Com as Habilidades da Jornada, os profissionais podem criar jornadas rapidamente, detectar e resolver conflitos de agendamento ou público-alvo, analisar o desempenho e os pontos de queda e identificar jornadas de melhor desempenho a serem replicadas para campanhas futuras. Ele capacita os profissionais a tomar decisões orientadas por dados, melhorar o envolvimento do cliente e simplificar a orquestração de jornadas.

O CX Co-worker oferece várias habilidades para gerenciar Jornadas e desafios de fidelidade:

**habilidades focadas na Jornada:**

* **Criação de Jornada**: criar e configurar jornadas de marketing por meio de prompts de linguagem natural
* **Criação de Conteúdo de Canal**: gere, edite e gerencie conteúdo específico de canal (email, push, SMS) para jornada usando a geração de conteúdo habilitado por IA
* **Analisar Jornada**: analise jornadas, detecte problemas, descubra insights e otimize o desempenho da jornada

**Habilidades com foco em fidelidade:**

* **Gerenciamento de Desafio de Fidelidade**: crie e gerencie desafios de fidelidade usando prompts de linguagem natural

<!--
feedback from Ivan: Need to remove Simulate skill from docs until Nico confirms the release timeline.

In addition, **Journey Simulation** is a Journey Optimizer feature that includes [Journey Simulate](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs), an in-product agentic skill, non conversational, with three capabilities: 

* Generating simulated users
* Generating event values
* Quick simulation
-->

## Habilidades de jornada {#journey-skills}

### Criar jornada {#journey-create}

A Criação de jornadas permite que os usuários do Journey Optimizer criem e configurem jornadas de marketing usando uma interface de linguagem natural. Com a Criação de Jornadas, os profissionais podem criar jornadas rapidamente descrevendo seus requisitos em prompts de conversação. A habilidade orienta os usuários sobre as diferentes opções para criar uma jornada, permitindo que os profissionais de marketing se concentrem na estratégia em vez de na configuração técnica.

>[!AVAILABILITY]
>
>Você precisa das seguintes permissões para usar totalmente os recursos Criar do Jornada:
>
>**Gerenciar Jornadas**: essa permissão permite que você crie novas jornadas diretamente no CX Co-worker.
>
>**Exibir eventos de Jornada, fontes de dados e ações**: essa permissão garante que o CX Co-worker possa realizar pesquisas por meio de eventos de Jornada e ações personalizadas.
>
>**Exibir segmentos**: essa permissão garante que o CX Co-worker possa procurar segmentos de público-alvo ao criar uma Jornada.
>
>**Gerenciar segmentos**: essa permissão permite que você crie novos públicos diretamente no CX Co-worker.

#### Principais casos de uso

O Jornada Create oferece recursos que podem ser aproveitados para acelerar a execução de marketing:

1. **Criação de jornada acionada por evento**

   * Crie jornadas que são ativadas com base em eventos específicos do cliente.
   * Projetar respostas automatizadas para ações do cliente em tempo real.
   * Crie fluxos de comunicação personalizados com base no comportamento do cliente.

   **jornada de visita à loja:**
   &quot;Crie uma jornada que começa quando um usuário entra no local da loja. Envie uma notificação por push para dar as boas-vindas aos usuários do armazenamento. Aguarde 2 dias e verifique se o usuário tem um endereço de email válido. Se o usuário tiver um endereço de email válido, envie uma pesquisa por email para perguntar sobre a experiência da loja. Se o usuário não tiver um endereço de email válido, envie uma notificação por push para solicitar o registro.&quot;

   **jornada pós-compra:**
   &quot;Crie uma jornada que começa quando um cliente faz uma compra online. Envie uma notificação por push para agradecer a compra. Em seguida, verifique se eles são membros do programa de fidelidade. Se o usuário for um membro do programa de fidelidade, envie uma segunda notificação por push com um código de desconto de 10%. Se o usuário não for um membro do programa de fidelidade, envie um push convidando-o a se inscrever no programa de fidelidade. Aguarde 2 dias e envie um push de acompanhamento com uma pesquisa sobre a experiência de compra deles.&quot;

   **Promoção baseada em eventos:**
   &quot;Criar uma jornada acionada quando a pontuação do jogo atingir 50. Envie uma mensagem SMS aos membros do programa de fidelidade dizendo que estão qualificados para receber uma fatia gratuita de pizza do patrocinador do parceiro.&quot;

1. **Criação de jornada direcionada ao público-alvo**

   * Crie jornadas direcionadas a segmentos específicos do público-alvo.
   * Projete sequências de comunicação em várias etapas com tempo estratégico.

   **Campanha sazonal:**
   &quot;Eu quero criar uma jornada direcionada a um público de visitantes do dia. Quero enviar um email alertando esse público-alvo para minha próxima venda de fim de ano que inclui uma variedade de recursos básicos para caminhadas. Aguarde 3 dias após o envio do primeiro e-mail e envie um segundo e-mail que tenha um cupom de 15% com frete grátis. Aguarde 1 semana e envie uma 3ª mensagem de email para mostrar nosso novo saco de dormir e coleção de tendas. Programe a jornada para iniciar em 20/12.&quot;

   **Apreciação de fidelidade:**
   &quot;Crie uma jornada de apreciação de fidelidade para proprietários de SUVs, incluindo uma notificação por push de agradecimento com uma oferta gratuita de lavagem de carro e um lembrete de notificação por push de acompanhamento se a primeira notificação não tiver interação em até 1 dia.&quot;

1. **Criação de jornada acionada por evento comercial**

   * Crie jornadas que são ativadas com base em um evento comercial específico e direcionem um público especificado (por exemplo, produto de volta ao estoque ou alteração de pontuação do jogo)
   * Acione mensagens oportunas e sensíveis ao contexto quando as condições dos negócios mudarem.

1. **Criação de jornada de qualificação de público-alvo**

   * Crie jornadas que são ativadas quando os perfis entram ou saem de uma definição de segmento de público-alvo.
   * Automatize as mensagens de entrada e saída para oferecer suporte às metas de integração, retenção e retomada.

1. **Fluxos de jornada condicionais**

   * Crie ramificações de decisão com base nos atributos do cliente.
   * Criar caminhos divididos que se adaptam às preferências do cliente.

1. **Criar jornada a partir da imagem**

   * Faça upload de uma imagem de referência no colaborador e peça para criar uma jornada usando a imagem como referência
   * A habilidade de criação de jornada extrairá um prompt editável da imagem de referência

Com essa habilidade, os requisitos de idioma natural são traduzidos em configurações de jornada estruturadas.

#### Competências dentro do âmbito

Os seguintes recursos são compatíveis com a Criação de Jornada:

* **Criação de jornada de linguagem natural**: permite que os usuários descrevam o fluxo de jornada em linguagem de conversação.
* **jornadas baseadas em eventos e em público-alvo**: oferece suporte aos tipos de jornada baseados em acionadores e agendados, bem como à qualificação de eventos comerciais e públicos-alvo.
* **Lógica condicional**: lida com divisões de decisão e ramificações com base nos atributos do cliente.
* **Mensagens multicanais**: oferece suporte a notificações por push, email e canais SMS.
* **Agendamento de Jornada**: configura datas de início e tempo para jornadas agendadas.

#### Habilidades fora do escopo

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

#### Solicitação de práticas recomendadas

Para maximizar a eficácia da Criação de Jornadas, siga estas práticas recomendadas:

1. **Seja específico**: forneça detalhes claros sobre suas metas do jornada, público-alvo e ações desejadas. Inclua informações sobre canais, tempo e condições.
1. **Especificar Tempo**: indique claramente os períodos de espera entre as ações e quando a jornada deve começar.
1. **Definir condições**: ao usar a lógica condicional, explique os critérios para cada caminho de ramificação.
1. **Incluir Canais**: especifique quais canais de comunicação você deseja usar (push, email, SMS).
1. **Agendamento de menção**: para jornadas agendadas, forneça a data e a hora de início desejadas.
1. **Ações personalizadas**: se você estiver usando ações personalizadas em seu fluxo de trabalho, será necessário especificar que você está usando uma ação personalizada, juntamente com o nome exato da ação personalizada. Exemplo:
Quando um usuário entrar no meu local de armazenamento, envie uma mensagem de boas-vindas usando a ação personalizada ExternalPush. Aguarde 2 dias e envie uma mensagem de acompanhamento usando a ação personalizada ExternalEmail com uma pesquisa em sua visita.
1. **Validar expressões**: verifique e valide todas as expressões criadas pelas Habilidades do Jornada para garantir que os campos e valores corretos sejam usados.

#### Configurar práticas recomendadas

* **Definir objetivos claros**: antes de criar jornadas, estabeleça metas claras (melhorar a retenção, gerar conversões, aumentar o engajamento).
* **Preparar públicos-alvo**: verifique se os públicos-alvo já foram criados e segmentados corretamente.
* **Conteúdo da Mensagem do Plano**: Defina sua estratégia de mensagens antes da criação da jornada.
* **Considere a Experiência do Cliente**: crie fluxos de jornada que respeitem as preferências do cliente e evitem a comunicação excessiva.

### Criação de conteúdo do canal {#channel-content-create}

<!--Ivan : Need to speak with Amar on new options for content generation as this skill has changed. -->

>[!AVAILABILITY]
>
>Este recurso está disponível para todos os clientes com Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

A Criação de conteúdo de canal permite que os usuários do Journey Optimizer gerem, editem e gerenciem conteúdo específico de canal para jornada usando a geração de conteúdo habilitada por IA.

#### Principais casos de uso

1. **Geração de conteúdo específico do canal**: gere conteúdo para email, notificações por push, SMS e outros canais usando prompts de linguagem natural.

   &quot;Gerar conteúdo de email para minha jornada de boas-vindas. Crie um email de boas-vindas para novos clientes com um tom amigável e inclua uma oferta de desconto de 10%.&quot;

   &quot;Gerar uma notificação por push para minha jornada de visita à loja. Crie uma mensagem de boas-vindas que incentive os clientes a fazer o check-in e receber uma oferta especial.&quot;

   &quot;Gerar conteúdo de SMS para minha jornada acionada por evento. Crie uma mensagem curta notificando os clientes sobre uma venda rápida com um call-to-action.&quot;

1. **Criação de conteúdo baseado em modelo**: procure e selecione entre os modelos disponíveis com recursos de visualização.

   &quot;Mostre-me os modelos de email disponíveis para a minha jornada de campanha sazonal.&quot;

   &quot;Selecione um modelo para meu email com um design moderno e limpo.&quot;

1. **Gerenciamento de conteúdo multicanal**: gere e gerencie conteúdo para vários canais no mesmo fluxo de trabalho de jornada.

1. **Edição de conteúdo em contexto**: abra o conteúdo gerado no Designer de Conteúdo para edição e refinamento.

   &quot;Abra o conteúdo do email no Designer de Conteúdo para que eu possa personalizar o design.&quot;

1. **Refinamento e iteração de conteúdo**: gere novamente o conteúdo com tons ou estilos diferentes usando a ação Regenerar.

   &quot;Gere novamente o conteúdo da notificação por push com um tom mais casual.&quot;

   &quot;Atualize o conteúdo do email para incluir um código promocional.&quot;

1. **Integração com a tela do Jornada**: selecione jornadas no inventário e exiba canais associados.

#### Competências dentro do âmbito

Os seguintes recursos são compatíveis com a Criação de conteúdo de canal:

* **Geração de conteúdo habilitada por IA**: gere conteúdo para email, push, SMS e outros canais usando prompts de linguagem natural.
* **Gerenciamento de modelos**: procure e selecione entre os modelos disponíveis com recursos de visualização.
* **Edição no contexto**: abra o conteúdo gerado no Designer de Conteúdo para edição e refinamento.
* **Regeneração de conteúdo**: gere novamente o conteúdo com diferentes tons, estilos ou mensagens usando a ação Regenerar.
* **Suporte a vários canais**: gere e gerencie conteúdo para vários canais no mesmo fluxo de trabalho do jornada.
* **Acesso ao inventário da Jornada**: selecione jornadas no inventário e exiba canais associados.

#### Habilidades fora do escopo

As seguintes funcionalidades não são compatíveis no momento:

* **Verificações de alinhamento da marca e qualidade do conteúdo**
* **Insira nós de conteúdo diretamente na tela de jornada**
* **Importação de modelo**

#### Solicitação de práticas recomendadas

1. **Seja específico**: forneça detalhes claros sobre o tipo de conteúdo, o tom, o público-alvo e as principais mensagens.
1. **Especificar Canal**: indique claramente para qual canal você está criando conteúdo (email, push, SMS).
1. **Definir Tom**: especifique o tom desejado (amigável, formal, casual, urgente).
1. **Iterar e Refinar**: use a ação de regeneração para refinar o conteúdo até que ele atenda aos seus requisitos.

### Jornada análise {#journey-analyze}

As Habilidades de Jornada permitirão que os usuários do Journey Optimizer analisem e otimizem jornadas usando uma interface de linguagem natural. Com as Habilidades da Jornada, os profissionais podem identificar e resolver rapidamente conflitos de agendamento e/ou público-alvo, detectar pontos de abandono de usuários em uma jornada e fornecer insights ou recomendações. Ele capacita os profissionais a tomar decisões orientadas por dados, melhorar o envolvimento do cliente e simplificar a orquestração de jornadas.

>[!AVAILABILITY]
>
>As habilidades de Jornada estão disponíveis para todos os clientes que têm acesso ao CX Co-worker. No entanto, você precisará das seguintes permissões para usar totalmente os recursos do Jornada Skills:
>
>**Exibir Jornadas**: essa permissão permite exibir insights sobre a jornada diretamente no CX Co-worker.
>
>**Gerenciar Jornadas**: essa permissão permite que você crie novas jornadas diretamente no CX Co-worker.
>
>**Exibir segmentos**: essa permissão permite que você visualize insights sobre os públicos diretamente no CX Co-worker.
>
>**Gerenciar segmentos**: essa permissão permite que você crie novos públicos diretamente no CX Co-worker.

#### Principais casos de uso

O Jornada Analyze oferece uma variedade de funcionalidades que podem ser aproveitadas para otimizar esforços de marketing:

1. **Análise de fallout da jornada**

   * Identifique onde e por que os clientes desistem durante uma jornada.
   * Detecte padrões no comportamento do cliente que levam ao desengajamento.
   * Use insights para refinar o design da jornada e melhorar a retenção.

   Exemplos de prompts:
   * &quot;Quero analisar o fallout por nó para a Campanha do jornada de 4 de julho.&quot;
   * &quot;Execute uma análise de fallout para a Campanha do jornada de 4 de julho.&quot;
   * &quot;O que é perda de perfil ao longo da Campanha de 4 de julho do jornada?&quot;
   * &quot;Mostrar onde os usuários estão saindo na Campanha do jornada de 4 de julho.&quot;

1. **Análise de sobreposição de público-alvo da jornada**

   * Analise a sobreposição de público-alvo em diversas jornadas.
   * Evite a fadiga de público-alvo causada pelo excesso de direcionamento.
   * Otimize a segmentação para garantir um engajamento equilibrado.

   Exemplos de prompts:
   * &quot;Quais públicos-alvo são usados em mais de X jornadas?&quot;
   * &quot;Liste todas as jornadas usando o [nome do público-alvo].&quot;
   * &quot;Mostrar conflitos de sobreposição de público-alvo para a jornada [Nome da Jornada].&quot;
   * &quot;Mostrar públicos sobrepostos para a jornada [Nome da Jornada] e outras jornadas.&quot;

1. **Análise de sobreposição de cronograma da jornada**

   * Detecte conflitos de data entre jornadas programadas que direcionam o mesmo público-alvo.
   * Evite o excesso de comunicação e melhore a eficiência do agendamento.
   * Maximize o impacto no público-alvo garantindo que as jornadas ocorram nos momentos ideais.

   Exemplos de prompts:
   * &quot;Há algum conflito de agendamento para a jornada [Nome da Jornada]?&quot;
   * &quot;Verifique se há conflitos de agendamento envolvendo o [Nome da Jornada] da jornada.&quot;
   * &quot;Destaque as sobreposições de agendamento entre a jornada [Nome da Jornada] e jornadas ativas.&quot;
   * &quot;A jornada [Nome da Jornada] está em conflito com alguma outra jornada?&quot;

1. **Insights operacionais**

   * Insights do Jornada com base em prompts - Surja insights operacionais sobre o jornada, ou seja, &quot;mostrar todas as jornadas ativas para mim&quot;.

   Exemplos de prompts:
   * &quot;Quando o [Nome da Jornada] foi publicado?&quot;
   * &quot;Quando o [Nome da Jornada] foi interrompido?&quot;
   * &quot;Listar todas as jornadas atualmente no modo de teste&quot;
   * &quot;Quantas jornadas ao vivo eu tenho?&quot;
   * &quot;Forneça uma lista de todas as jornadas recorrentes agendadas e seus tempos de execução esperados.&quot;

1. **Análise de Erro de Ação Personalizada de Jornada**

   * Identifique quando as ações personalizadas estão falhando ou quando as taxas de erro aumentam em uma jornada.
   * Diagnosticar as causas raiz antes que as falhas ocorram em uma interrupção mais ampla da jornada.
   * Use etapas de correção específicas para restaurar rapidamente a confiabilidade da ação personalizada.

   Exemplos de prompts:
   * &quot;Por que as ações personalizadas estão falhando na jornada [Nome da Jornada]?&quot;
   * &quot;Qual é a taxa de erro da ação personalizada [Nome da Ação Personalizada] na jornada [Nome da Jornada]?&quot;
   * &quot;Mostrar a causa raiz das falhas de ação personalizada na jornada [Nome da Jornada].&quot;
   * &quot;Há algum erro de ação personalizada afetando a jornada [Nome da Jornada] neste momento?&quot;

#### Competências dentro do âmbito

Os seguintes recursos são compatíveis com o Jornada Analyze:

* **Consultas reativas**: permite que usuários façam perguntas específicas sobre o desempenho da jornada, a utilização do público-alvo e conflitos de agendamento.
* **Integração com outras habilidades**: colabora com os recursos de Audience e Data Insights para uma análise mais profunda.
* **Estrutura de resposta**: raciocínio (explique a lógica), resumo da análise (destaque os pontos principais), detalhes do problema (descreva o problema) e recomendação (proponha as próximas etapas).
* **Análise de erro de ação personalizada**: detectar e diagnosticar falhas de ação personalizada e picos de erro em uma jornada.

#### Habilidades fora do escopo

As seguintes funcionalidades não são compatíveis no momento:

* **Criação automatizada de jornadas**
* **Detecção de anomalias em tempo real**
* **Sobreposição de canais**
* **Análise de entrada da jornada**
* **Análise de problemas técnicos**
* **Análise de fadiga**

#### Solicitação de práticas recomendadas

Para maximizar a eficácia do Jornada Analyze, siga estas práticas recomendadas:

1. **Seja específico(a)**: use prompts claros e concisos para obter insights direcionados. Por exemplo, em vez de perguntar &quot;Quais são minhas jornadas?&quot;, especifique &quot;Listar todas as jornadas criadas no último mês&quot;.
1. **Combinar insights**: integre insights dos recursos de Audience e Data Insights para obter uma visão holística do desempenho da jornada.
1. **Refinamento iterativo**: use as análises de fallout e de sobreposição para refinar continuamente o design e o agendamento da jornada.

#### Configurar práticas recomendadas

* **Defina objetivos claros**: antes de analisar as jornadas, estabeleça metas claras (por exemplo: melhorar a retenção, aumentar as conversões).
* **Monitore regularmente**: agende revisões regulares do desempenho da jornada para identificar tendências e anomalias.
* **Otimize a segmentação**: mantenha uma segmentação de público-alvo equilibrada para evitar fadiga e maximizar o engajamento.

## Habilidades de fidelidade {#loyalty-skills}

### Gerenciamento de desafios de fidelidade {#loyalty-challenge-management}

>[!AVAILABILITY]
>
>As habilidades de fidelidade estão disponíveis no CX Co-worker para organizações qualificadas. Os clientes com uma licença do programa de fidelidade podem acessar essas habilidades de fidelidade, mesmo que não tenham uma licença adicional do CX Co-worker.

O gerenciamento de desafios de fidelidade permite que os usuários do Journey Optimizer criem e gerenciem desafios de fidelidade no CX Co-worker usando prompts de linguagem natural. Para obter uma documentação abrangente sobre como criar, configurar e gerenciar desafios de fidelidade, incluindo instruções detalhadas de configuração, consulte o [Guia de Desafios de Fidelidade](../loyalty-challenges/get-started.md).

#### Principais casos de uso

1. **Desafio de integração de várias etapas**

   &quot;Crie um desafio chamado &quot;Início Rápido da Nova Conta&quot; para clientes recém-inscritos que exija que eles concluam essas etapas em ordem: abra uma conta corrente, financie-a com pelo menos US$ 500 e baixe o aplicativo móvel. Quando todos os passos estiverem feitos, recompense-os com 5.000 pontos de bônus. Execute-o de 1º de setembro a 31 de outubro, fuso horário do Leste.&quot;

1. **Desafio de limite de atividade cumulativo**

   &quot;Crie um desafio chamado &quot;Spend &amp; Earn Summer&quot; para titulares de cartões, onde os membros ganham um crédito de US$ 50 em demonstrativo quando gastam US$ 1.500 em seu cartão de crédito durante o terceiro trimestre. Comece em 1º de julho, fuso horário do Leste dos EUA.&quot;

1. **Desafio de sequência de frequência**

   &quot;Crie um desafio chamado &quot;Frequent Flyer Sprint&quot; para membros de nível elite que exigem 3 voos por mês por dois meses consecutivos. Conclusão de recompensa com uma extensão de status de nível e 10.000 milhas bônus. Comece no primeiro dia do próximo mês, fuso horário do Pacífico.&quot;

1. **Desafio de ação única qualificada**

   &quot;Configure um desafio chamado &quot;Go Paperless&quot; que premia assinantes pós-pagos com 500 pontos de bônus depois de se inscreverem em pagamento automático e mudarem para cobrança sem papel dentro de 30 dias. Comece no primeiro dia do mês que vem, fuso horário central.&quot;

1. **Desafio da meta de participação/consumo**

   &quot;Crie um desafio chamado &quot;Explorer Badge&quot; para membros que exige que eles concluam cinco atividades em pelo menos três categorias diferentes durante o mês de agosto. Recompense-os com 1.000 pontos e um selo &quot;Explorer&quot; na conclusão. Início em 1º de agosto, Fuso horário das montanhas dos EUA.&quot;

1. **Desafio de ação diário**

   &quot;Ajude-me a criar um desafio para os amantes do matcha que exige que eles entrem na loja todos os dias nesta semana e comprem uma bebida de matcha. A recompensa será de 200 pontos a mais se completarem o desafio. Chame de &quot;Louco sobre Matcha&quot;, use o SKU matcha-001, comece segunda-feira da próxima semana, fuso horário do Leste.&quot;

#### Competências dentro do âmbito

Os seguintes recursos são compatíveis com o Loyalty Challenge Management:

* **Criação de desafio**: criar configuração de desafio a partir da linguagem natural (público-alvo, critérios de ação, tempo, recompensa, nomenclatura).
* **Atualizações de desafio**: modifique os detalhes do desafio por meio de prompts iterativos.
* **Publicação de desafio**: publique configurações de desafio com suporte diretamente da conversa.
* **Visibilidade de contexto de desafio**: recuperar e revisar informações de desafio ao iterar.

#### Habilidades fora do escopo

As seguintes funcionalidades não são compatíveis no momento:

* Exclusão por desafio
* Insights de fidelidade e habilidades de recomendações
* Automação completa de criação de conteúdo para mensagens de desafio em todos os casos

#### Solicitação de práticas recomendadas

1. **Nomeie-o**: forneça ao desafio um título claro e memorável entre aspas.
1. **Especificar o público-alvo**: quem qualifica (por exemplo, todos os membros, um nível, um segmento, novos inscritos, titulares de cartões, assinantes).
1. **Defina a ação e a quantidade**: o que os membros devem fazer e a frequência, o limite ou a sequência que conta como conclusão.
1. **Definir a janela de tempo**: uma data inicial (e uma data final, se for de duração fixa) mais o fuso horário.
1. **Declarar a recompensa**: pontos, milhas, créditos de demonstrativo, extensões de status, vouchers ou vantagens concedidas na conclusão.
1. **Referenciar o evento de qualificação**: aponte para a SKU, o produto, a ação da conta ou o evento de envolvimento específico que o desafio rastreia.


<!--
Feedback from Ivan: Journey simulate is not ready as a skill

## Journey Simulate: Use Cases, Agentic Skills and User Guide

## Overview

>[!BEGINSHADEBOX]

Journey Simulation is available to all Journey Optimizer customers. Journey Simulate, the in-product agentic skill within Journey Simulation, is available to customers that are a part of the Agent Orchestrator Explorer program and requires at least one of the following permissions:

* **Simulate journeys**: Run simulation workflows from the journey canvas.

* **Publish journeys**: Publish journeys, including flows that use simulation before go-live.

* **Approve and Publish journeys**: Approve and publish journeys when your organization uses approval workflows.

To use AI in **[!UICONTROL Simulation]** (**[!UICONTROL Quick simulation]**, generating simulated users with AI, **[!UICONTROL Generate event values]**), users require **[!UICONTROL Generate Content]** permission from the **[!UICONTROL AI Assistant]** capability. 

[Learn more about permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/administration/permissions).

>[!ENDSHADEBOX]

Journey Simulation is a Journey Optimizer feature that enables Journey Optimizer users to safely test and validate marketing journeys before activation. Within Journey Simulation, Journey Simulate is an in-product agentic skill, not a conversational one, that automates and assists the testing process directly from the journey canvas.

Journey Simulate includes three capabilities:

* Generating simulated users
* Generating event values
* Quick simulation. 

Together, they bridge the gap between journey creation and activation, building confidence in journey logic and reducing the risk of post-launch errors.

## Use cases

### Key use cases for Journey Simulate

Journey Simulate offers three capabilities that can be leveraged to reduce testing time and improve journey quality before go-live:

**Generating simulated users**

* Generate simulated users automatically based on journey paths and required attributes.
* Create simulated users that cover all branches and conditions in a journey, including execution addresses (email, push, SMS).
* Update simulated user attributes on demand to refine test scenarios.
* Ensure all journey branches are covered by assigning the right simulated user to each path.

**Generating event values**

* Generate values for events used in a journey to drive test execution through specific paths.
* Define event attribute values that trigger the desired conditions and branches during simulation.

**Quick simulation**

* Start journey simulation and trigger test executions for all simulated users needed to test all paths of a journey, in a single interaction.
* Visualize how simulated users flow through a journey, step by step, including branching paths and conditional logic.
* Identify which simulated user flows through which path, and why, with detailed node-by-node traversal.
* Review simulation reporting at the end of a run in the Journey Optimizer UI to validate outcomes before activation.

## In scope skills and limitations

### **In scope**

The following capabilities are supported by the Journey Simulation feature:

* **Simulated user management**: View, edit, and update simulated user attributes, including execution addresses and personalization data.
* **Simulation control**: Start and stop journey simulation directly through the Journey Simulation in-product experience.
* **Test execution**: Trigger test executions for one or multiple simulated users.
* **Journey flow visualization**: View step-by-step traversal of simulated users through journey nodes, including branching, splits, and user status.
* **Simulation reporting**: View reporting at the end of a simulation run in the Journey Optimizer UI.
* **Multi-user testing**: Run and visualize tests for multiple simulated users simultaneously, covering all journey branches.

In addition to this, the following capabilities are supported by the Journey Simulate skill:

* **Simulated user generation**: Create simulated users based on journey paths, existing test profiles, or specified attributes.
* **Event value generation**: Generate and assign event attribute values to drive test execution through specific journey paths.
* **Quick simulation**: Run a full end-to-end simulation with minimal intervention. The skill automatically generates simulated users, event values, and pre-filled test settings, then executes the journey and surfaces results for review.

### **Limitations**

Simulation may not support every activity, channel, or integration that Test mode or a live journey supports, and behavior may change as the capability matures.

➡️ Learn more about [Simulation limitations](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs#limitations) in the Journey Optimizer documentation.

-->
