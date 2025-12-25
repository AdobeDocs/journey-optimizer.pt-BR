---
solution: Journey Optimizer
product: Journey Optimizer
title: Testar e aprovar
description: Testar e aprovar
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# Testar e aprovar{#section-overview}

A garantia de qualidade é essencial para fornecer experiências excepcionais para o cliente. O Adobe Journey Optimizer fornece recursos abrangentes de teste e aprovação para ajudar você a validar o conteúdo, verificar a lógica de jornada e garantir que as campanhas atendam aos padrões de qualidade antes de atingir seu público-alvo. Desde a pré-visualização de mensagens personalizadas com perfis de teste até a simulação de fluxos de jornada complexos, essas ferramentas permitem identificar e resolver problemas antecipadamente, reduzir riscos e manter a integridade da marca. Independentemente de você estar testando a renderização de email em dispositivos, validando jornadas de várias etapas ou estabelecendo fluxos de trabalho de aprovação formal, esta seção orienta você pelas práticas recomendadas e pelos processos passo a passo para criar confiança em suas campanhas e jornadas. Ao implementar testes completos e aprovações estruturadas, você minimizará erros, melhorará a capacidade de entrega e criará experiências perfeitas que repercutem com seus clientes.

## Por que o teste e a aprovação são importantes

Os processos de teste e aprovação servem como quality gates (portais de qualidade) essenciais que protegem a reputação da sua marca e garantem o sucesso da campanha. É por isso que eles são importantes:

* **Detectar erros antes que eles cheguem aos clientes** - Identifique links com falha, personalização incorreta, problemas de renderização e falhas lógicas em um ambiente controlado em que as correções são rápidas e sem riscos.

* **Melhore a capacidade de entrega** - Teste pontuações de spam, valide a autenticação de email e verifique a renderização entre clientes de email para maximizar as taxas de posicionamento e de engajamento da caixa de entrada.

* **Garanta a consistência da marca** - Visualize o conteúdo com diferentes perfis de teste para verificar se a personalização é exibida corretamente para vários segmentos de clientes e mantém os padrões da marca.

* **Validar jornadas complexas** - Simular fluxos de jornada de várias etapas para confirmar se os acionadores são acionados corretamente, se as condições são avaliadas corretamente e se os clientes recebem as mensagens certas na hora certa.

* **Estabelecer responsabilidade** - Implementar fluxos de trabalho de aprovação formais que exigem a aprovação das partes interessadas, criando uma propriedade clara e reduzindo lançamentos de campanhas não autorizadas ou prematuras.

* **Economize tempo e recursos** - Detecte problemas no início do ciclo de desenvolvimento quando as correções são mais baratas e rápidas, evitando correções dispendiosas pós-lançamento ou escalonamentos do atendimento ao cliente.

## Práticas recomendadas de teste

Para maximizar a eficácia de seus esforços de teste, siga estas práticas recomendadas:

1. **Testar antes e com frequência** - Não espere até que uma campanha seja totalmente criada. Teste o conteúdo, a personalização e a lógica de forma incremental à medida que você desenvolve.

1. **Use perfis de teste realistas** - [Crie perfis de teste](../using/audience/creating-test-profiles.md) que representem com precisão os segmentos de público-alvo, incluindo casos de borda e diferentes cenários de personalização.

1. **Testar em dispositivos e clientes** - Verifique a [renderização de email](../using/content-management/rendering.md) em clientes de email populares (Gmail, Outlook, Apple Mail) e dispositivos (desktop, celular, tablet) para garantir uma exibição consistente.

1. **Valide a personalização completamente** - Teste com vários [perfis de teste](../using/content-management/test-profiles.md) que tenham valores de atributo diferentes para confirmar se os tokens de personalização são renderizados corretamente e os valores de fallback funcionam.

1. **Simular caminhos de jornada** - Para jornadas complexas com várias ramificações, use o [modo de teste](../using/building-journeys/testing-the-journey.md) para testar diferentes condições de entrada e atributos de perfil para validar todos os caminhos possíveis.

1. **Verificar indicadores de capacidade de entrega** - Revisar [pontuações de spam](../using/content-management/spam-report.md), status de autenticação e métricas de integridade de email antes de envios grandes.

1. **Documentar resultados do teste** - Mantenha registros dos resultados do teste, problemas encontrados e resoluções para melhorar futuros processos de teste e compartilhar aprendizados com a sua equipe.

1. **Envolva as partes interessadas antecipadamente** - Compartilhe visualizações e resultados de teste com as partes interessadas antes da [aprovação formal](../using/test-approve/gs-approval.md) para coletar comentários e alinhar as expectativas.

## Fluxo de trabalho de teste recomendado

Siga esta abordagem sistemática para garantir testes completos e aprovações tranquilas:

### &#x200B;1. Desenvolvimento e visualização de conteúdo

Comece criando seu conteúdo e usando os recursos de visualização para verificar o design e a personalização iniciais:

* Crie seu [email](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [notificação por push](../using/push/create-push.md) ou outro conteúdo de canal
* Use o recurso **[Simular conteúdo](../using/content-management/preview-test.md)** para visualizar com perfis de teste
* Verificar [tokens de personalização](../using/personalization/personalization-syntax.md), conteúdo dinâmico e valores de fallback
* Verificar [renderização](../using/content-management/rendering.md) em telas de tamanhos diferentes e clientes de email

### &#x200B;2. Validação técnica

Validar aspectos técnicos que afetam a capacidade de entrega e a funcionalidade:

* Execute [verificações de pontuação de spam](../using/content-management/spam-report.md) para identificar possíveis problemas de entrega
* Testar links para garantir que não estejam quebrados e rastreiem corretamente
* Validar a configuração da [autenticação de email](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC)
* Revise a renderização do HTML e verifique se há problemas de compatibilidade de CSS
* Testar [design responsivo](../using/email/content-from-scratch.md) em dispositivos móveis e desktop

### &#x200B;3. Teste de Jornada

No jornada, valide a lógica de orquestração:

* Ative o **[Modo de teste](../using/building-journeys/testing-the-journey.md)** para simular a progressão do perfil através da jornada
* Teste diferentes [condições de entrada](../using/building-journeys/entry-management.md) e qualificações de público
* Verificar se as [atividades de espera](../using/building-journeys/wait-activity.md), [condições](../using/building-journeys/condition-activity.md) e a lógica de ramificação funcionam corretamente
* Use **[Dry run](../using/building-journeys/journey-dry-run.md)** para jornadas complexas para analisar caminhos de execução sem enviar mensagens
* Verifique se os [eventos](../using/event/about-events.md) são acionados corretamente e se as [ações personalizadas](../using/action/about-custom-action-configuration.md) são executadas conforme esperado

### &#x200B;4. Apresentação da aprovação

Quando o teste for concluído e os problemas forem resolvidos:

* Enviar a campanha ou a jornada para aprovação de acordo com a [política de aprovação](../using/test-approve/approval-policies.md) da sua organização
* Incluir resultados e documentação de teste com a [solicitação de aprovação](../using/test-approve/request-approval.md)
* Resolva qualquer comentário ou solicitação de mudança de [aprovadores](../using/test-approve/review-approve-request.md)
* Faça as revisões necessárias e teste novamente se as alterações forem significativas

### &#x200B;5. Verificação de pré-lançamento

Antes de ativar sua campanha ou jornada:

* Executar uma revisão final de todas as configurações, públicos e [agendamentos](../using/building-journeys/journey-properties.md)
* Verificar se todas as aprovações estão implementadas e documentadas
* Confirme se os horários de envio e os [fusos horários](../using/building-journeys/timezone-management.md) estão corretos
* Habilitar [monitoramento e alertas](../using/reports/alerts.md) para acompanhar o desempenho após a inicialização

### &#x200B;6. Monitorar e iterar

Após o lançamento, continue o monitoramento para detectar problemas antecipadamente:

* Configurar [alertas do sistema](../using/reports/alerts.md) para erros de jornada, altas taxas de rejeição ou baixo engajamento
* Revise os [relatórios ao vivo](../using/building-journeys/report-journey.md) para acompanhar o desempenho em relação às expectativas
* Esteja preparado para [pausar ou modificar](../using/building-journeys/journey-pause.md) jornadas se surgirem problemas críticos
* Documentar as lições aprendidas para melhorar os futuros processos de teste

## Testes em ação: casos de uso

Veja como os conceitos de teste se aplicam a cenários do mundo real:

* **[Enviar mensagens multicanais](../using/building-journeys/journeys-uc.md)** - Este caso de uso demonstra como testar uma jornada que combina Ler Público, eventos de reação e mensagens de email/push. Saiba como validar todo o fluxo do direcionamento de público-alvo para a entrega de mensagens e veja as etapas de teste e publicação em ação.

* **[Enviar uma mensagem aos assinantes](../using/building-journeys/message-to-subscribers-uc.md)** - Descubra como testar jornadas que direcionam listas de assinaturas com endereçamento de email dinâmico. Este exemplo mostra como validar expressões de personalização e garantir que as mensagens cheguem aos assinantes corretos.

* **[Enviar mensagens associadas ao tempo](../using/building-journeys/weekday-email-uc.md)** - Entenda como testar jornadas com condições baseadas no tempo para garantir que as mensagens sejam enviadas em dias específicos. Veja como validar atividades de espera e a lógica de programação.

* **[Veja mais casos de uso do jornada](../using/building-journeys/jo-use-cases.md)** - Acesse uma coleção abrangente de exemplos práticos que abrangem eventos de experiência, mensagens multicanais e integrações externas de sistema.

## Testar e aprovar o conteúdo

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=pt-BR)

Visualizar, testar e validar o conteúdo

Saiba como visualizar, testar e validar um conteúdo personalizado por meio de perfis de teste, testes de renderização de email, avaliações de pontuação de spam e muito mais.

[Explore a prévia e teste do conteúdo](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=pt-BR)

Fluxos de trabalho de aprovação para jornadas e campanhas

Entenda como configurar, gerenciar e executar processos de aprovação para garantir o controle de qualidade de jornadas e campanhas.

[Saiba mais sobre fluxos de trabalho de aprovação](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

Teste a jornada

Valide a jornada antes de publicá-la testando-a com perfis específicos para garantir que eventos, condições e ações funcionem conforme esperado.

[Teste a jornada](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

Execução de teste de jornada

Realize uma execução de teste para simular e validar o caminho de execução da jornada, identificando possíveis problemas antes da ativação.

[Saiba mais sobre a execução de teste da jornada](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

Monitoramento e solução de problemas

Acesse recursos abrangentes de solução de problemas, alertas do sistema e códigos de erro para resolver problemas de execução e desempenho de jornadas.

[Exibir monitoramento e solução de problemas](troubleshoot-journey-landing-page.md)
:::

::::

## Recursos adicionais

### Guias essenciais de teste e validação

* [Relatório ao vivo na sua Jornada](../using/building-journeys/report-journey.md) - Monitore métricas de jornada em tempo real para acompanhar o desempenho e identificar problemas durante a execução. Acesse detalhamentos detalhados da progressão do perfil, acionadores de eventos e taxas de conclusão de ações.

* [Criação de Perfis de Teste](../using/audience/creating-test-profiles.md) - Crie e gerencie perfis de teste para simular cenários de clientes reais e validar a personalização. Saiba como sinalizar perfis para teste, definir valores de atributo e organizar segmentos de perfil de teste.

* [Relatório de spam por email](../using/content-management/spam-report.md) - Verifique a pontuação de spam por email antes de enviar para melhorar a capacidade de entrega e o posicionamento da caixa de entrada. Entenda como os filtros de spam avaliam seu conteúdo e obtêm recomendações de melhoria.

* [Perguntas frequentes sobre o Jornada](../using/building-journeys/journey-faq.md) - Encontre respostas para perguntas comuns sobre a criação, o teste, a execução e a solução de problemas do jornada. Referência rápida para resolver problemas frequentes e entender o comportamento da jornada.

### Tópicos relacionados

* [Gerenciamento de conteúdo](content-management-landing-page.md) - Saiba como projetar, visualizar e gerenciar conteúdo usando modelos, fragmentos e o Email Designer. Práticas recomendadas de criação de conteúdo principal para uma identidade visual consistente.

* [Reporting &amp; Analytics](reporting-landing-page.md) - Analise o desempenho da campanha e do jornada com relatórios, painéis e métricas abrangentes. Tome decisões orientadas por dados para otimizar as experiências do cliente.

* [Configuração de Jornada](configure-journeys-landing-page.md) - Configure fontes de dados, eventos e ações personalizadas para habilitar a orquestração de jornada sofisticada. Estabeleça as bases técnicas para a criação de jornadas.

* [Gerenciamento de campanhas](../using/campaigns/get-started-with-campaigns.md) - Explore diferentes tipos de campanhas e saiba como criar, agendar e otimizar campanhas em lote e em tempo real para obter o máximo impacto.
