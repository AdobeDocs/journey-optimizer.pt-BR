---
solution: Journey Optimizer
product: journey optimizer
title: Simular a jornada
description: Saiba como simular sua jornada
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: teste, jornada, verificação, erro, solução de problemas
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: c2c8b1a64e79482fcc9340950209579cf74c50b3
workflow-type: tm+mt
source-wordcount: 1891
ht-degree: 0%

---

# Simular a jornada {#simulate-journey}

>[!IMPORTANT]
>
>Você precisa de pelo menos uma das seguintes permissões para acessar o recurso **[!UICONTROL Simulação]**: **Simular jornadas**, **Publicar jornadas** ou **Aprovar e Publicar jornadas**. [Saiba mais](../administration/permissions.md)
>
>Para usar a IA em **[!UICONTROL Simulação]** (**[!UICONTROL Simulação rápida]**, gerando usuários simulados com IA, **[!UICONTROL Gerar valores de evento]**), os usuários exigem a permissão **[!UICONTROL Gerar conteúdo]** do recurso **[!UICONTROL Assistente de IA]**.

Use a **[!UICONTROL Simulação]** para validar sua jornada com **usuários simulados** antes de publicar. Esta página o orienta durante a **[!UICONTROL Simulação rápida]** e a **[!UICONTROL Simulação manual]**, criando e enviando usuários simulados, acionando eventos unitários quando a jornada precisar deles e revisando o log de **[!UICONTROL Resultados]**.

Para obter uma visão geral por tipo de jornada, consulte [Introdução à simulação de Jornada](simulate-journey-gs.md).

## Tipos de simulação {#simulation-types}

Após a ativação, as jornadas em lote com entrada de público-alvo de leitura oferecem duas maneiras de executar uma simulação:

* A **[!UICONTROL Simulação rápida]** é executada de ponta a ponta com usuários gerados, valores de eventos gerados e configurações de teste padrão, habilitados pela Journey Agent. É uma maneira rápida de simular uma jornada completa com o mínimo de intervenção. A simulação rápida é iniciada assim que você seleciona essa opção.

* **[!UICONTROL A simulação manual]** permite executar uma simulação passo a passo, manualmente. Crie usuários simulados (manualmente ou com o Journey Agent), acione-os na jornada, defina cargas de evento (manualmente ou com o Journey Agent) e substitua esperas.

![Painel de configurações de simulação com as opções de Simulação rápida e Simulação manual ao lado da tela de jornada](assets/quick-simulation-1.png)

### Simulação rápida {#quick-simulation}

Em qualquer jornada em **[!UICONTROL Simulação]**, a **[!UICONTROL Simulação rápida]** executa a jornada com usuários gerados, valores de evento e configurações preenchidas previamente.

1. Selecione **[!UICONTROL Simulação rápida]**.

1. Revise os campos que o Adobe Journey Optimizer reuniu para a execução. Clique em **[!UICONTROL Atualizar valores]** para alterar configurações de teste e endereços de execução, ou continue sem alterações.

   Esta etapa só será exibida se a jornada usar Esperas ou Canais. Você pode ajustar todas as durações de espera e endereços de execução para usuários simulados, por exemplo, usar seu próprio email para que as mensagens da execução sejam enviadas para sua caixa de entrada.

   ![Caixa de diálogo Simulação Rápida na etapa Coletando informações com Atualizar valores e Continuar na próxima etapa](assets/quick-simulation-2.png)

1. Se você abriu **[!UICONTROL Atualizar valores]**, edite as configurações, por exemplo, o endereço usado para provas de mensagem e, em seguida, confirme para iniciar a simulação.

   ![Etapa de atualização rápida de valores de simulação com substituição de tempo de espera e campos de email e telefone de prova](assets/quick-simulation-3.png)

1. O Journey Agent gera um conjunto de usuários simulados a partir da definição da jornada.

   Para jornadas com um nó de email, SMS ou push, o agente solicita que você confirme o endereço de email, o número de telefone ou o token de push a serem usados. Os usuários simulados são gerados usando esses valores. Depois de concluído, clique em **[!UICONTROL Gerar]**.

1. Quando a execução for concluída, clique em **[!UICONTROL Exibir resultados]** para examinar caminhos, erros e ramificações descobertas. Ver [Exibir resultados](#viewing-results).

   ![Simulação Rápida concluída com todas as etapas bem-sucedidas e Exibir Resultados disponíveis](assets/quick-simulation-4.png)

A simulação rápida também é compatível com jornadas e jornadas acionadas por eventos que incluem atividades de eventos. Os valores de evento são definidos e acionados automaticamente para cada usuário simulado gerado. Depois que um usuário entra na jornada, cada evento é acionado assim que atinge o Wait correspondente.

### Simulação manual {#manual-simulation}

Escolha **[!UICONTROL Simulação manual]** quando precisar escolher cada usuário simulado, controlar ordem de envio, configurar cargas de evento e substituir as durações de **[!UICONTROL Espera]** para a execução.

Continue com [Criar e gerenciar usuários simulados](#test-users), [Acionar seus eventos](#firing-events) e [Exibir resultados](#viewing-results).

## Criar e gerenciar usuários simulados {#test-users}

>[!IMPORTANT]
>
>Você precisa de pelo menos uma das seguintes permissões para acessar o recurso **[!UICONTROL Simulação]**: **Simular jornadas**, **Publicar jornadas** ou **Aprovar e Publicar jornadas**. [Saiba mais](../administration/permissions.md)
>
>Para usar a IA em **[!UICONTROL Simulação]** (**[!UICONTROL Simulação rápida]**, gerando usuários simulados com IA, **[!UICONTROL Gerar valores de evento]**), os usuários exigem a permissão **[!UICONTROL Gerar conteúdo]** do recurso **[!UICONTROL Assistente de IA]**.

Os usuários simulados são entidades temporárias semelhantes a perfis definidas em **[!UICONTROL Configurações de simulação]**. Esta seção aborda como criá-los, salvá-los para reutilização, ajustá-los ou removê-los da lista e enviá-los para a jornada.

1. Comece preenchendo a lista **[!UICONTROL Usuários de teste]**:

   +++ Gerar usuários com IA

   O Adobe Journey Optimizer gera um conjunto de usuários simulados a partir da definição de jornada.

   Para jornadas com um nó de email, push ou SMS, a IA solicita que você confirme o endereço de email ou o número de telefone a ser usado. Os usuários simulados serão gerados usando esses valores definidos. Depois de concluído, clique em **[!UICONTROL Gerar]**.

   ![Gerar caixa de diálogo de usuários simulados com campos de email e telefone de execução e botão Gerar](assets/simulate-generate.png)

   +++

   +++ Procurar inventário

   Escolha **[!UICONTROL Procurar inventário]** para adicionar usuários simulados que você já salvou, por exemplo, usuários criados a partir de um formulário ou JSON ou usuários mantidos após a execução de uma geração de IA.

   ![Caixa de diálogo de inventário de Usuários Simulados com pesquisa, tabela de usuários e botão Selecionar](assets/simulate-inventory.png)

   +++

   +++ Criar a partir do formulário

   1. Insira um **[!UICONTROL Nome de exibição]**, **[!UICONTROL Namespace de identidade]** e **[!UICONTROL Descrição]** para identificar este usuário simulado.

      ![Criar formulário de Usuários Simulados com nome para exibição, namespace de identidade, descrição e atributos de esquema de União](assets/simulate-form.png)

   1. Em seguida, selecione os atributos do esquema Union que deseja preencher para este usuário.

   1. Clique em **[!UICONTROL Adicionar associação de público-alvo]** para simular associações de segmento.

   1. Na janela **[!UICONTROL Criar Usuários Simulados]**, clique em **[!UICONTROL Adicionar usuário simulado]** para definir vários usuários simulados em uma sessão.

      Você pode alterar a forma como os usuários são mostrados na lista, recolher todos os cartões na exibição empilhada ou abrir os metadados de atributo de um usuário.

      ![Criar rodapé de Usuários Simulados com Adicionar usuário simulado, Recolher tudo e controles de exibição de layout](assets/simulate-form-3.png)

   1. No menu de usuário Simulado, use **[!UICONTROL Duplicar]** para copiar um usuário, **[!UICONTROL Aplicar todos os atributos a outros usuários]** para copiar os atributos de um usuário para todos os outros usuários na sessão ou **[!UICONTROL Excluir]** para remover um usuário.

      ![Criar cartões de Usuários Simulados com Duplicar, Aplicar todos os atributos a outros usuários e Excluir em cada usuário](assets/simulate-form-2.png)

   1. Clique em **[!UICONTROL Salvar]** quando terminar de configurar os usuários nesta sessão.

   +++

   +++ Criar a partir de JSON

   Defina novos usuários simulados atualizando os campos correspondentes com os dados do usuário simulados.

   ![Criar editor JSON de Usuários Simulados com modelo de usuários e controle Formatar JSON](assets/simulate-json.png)

   +++

1. Os usuários simulados que você criou aparecem na lista **[!UICONTROL Usuários de teste]**. Para cada entrada, selecione uma das seguintes opções:

   * ![Ícone Editar](assets/do-not-localize/Smock_Edit_18_N.svg): atualizar os detalhes do usuário simulado.
   * ![Ícone Enviar](assets/do-not-localize/Smock_Send_18_N.svg): Executar a simulação somente para este usuário simulado.

     Essa opção não está disponível para jornadas que começam com um Evento, pois a entrada do usuário simulada é acionada pelo evento que está sendo enviado. [Saiba mais](#firing-events)

   * ![Ícone Limpar](assets/do-not-localize/Smock_Close_18_N.svg): Remova o usuário desta lista. O usuário simulado não é excluído e permanece disponível na seleção Usuários simulados.

   ![Testar lista de usuários com ações de edição, envio e remoção e caminho simulado realçado na tela](assets/simulate-4-2.png)

1. Para alterar a lista após sua seleção, clique em **[!UICONTROL Gerenciar usuários]** para adicionar mais usuários simulados, a partir do inventário ou criando novos. Para remover todos os usuários da lista de **[!UICONTROL Usuários de teste]** para esta execução, escolha **[!UICONTROL Limpar todos os usuários]**.

   ![Menu Gerenciar usuários aberto com opções de adição de usuários e Limpar todos os usuários](assets/simulate-manage.png)

1. Se sua jornada incluir uma atividade **[!UICONTROL Aguardar]**, abra a guia **[!UICONTROL Configurações de teste]** para ajustar quanto tempo a espera dura durante a simulação. Por exemplo, se a atividade ativa **[!UICONTROL Wait]** estiver configurada por vários dias, você poderá substituí-la por 10 segundos para que o usuário simulado passe somente esse tempo no nó antes de passar para a próxima atividade.

1. Clique em **[!UICONTROL Enviar tudo]** para enviar todos os usuários simulados da lista para a jornada ou clique em ![Ícone Enviar](assets/do-not-localize/Smock_Send_18_N.svg) em uma linha para enviar somente esse usuário. Uma mensagem de confirmação `Simulated users have entered the journey successfully.` é exibida quando os usuários simulados entram com êxito na jornada.

   ![Testar a guia de usuários depois que os usuários entrarem na jornada com a mensagem de sucesso e o caminho na tela](assets/simulate-5-2.png)

1. Se a jornada incluir eventos unitários, será necessário selecionar o evento a ser acionado. Consulte [Acionar seus eventos](#firing-events).

1. Acesse a guia **[!UICONTROL Resultados]** para abrir o log de execução e analisar como cada etapa foi executada. Para obter mais informações, consulte [Exibir resultados](#viewing-results).

1. Ao concluir o teste, abra o menu **[!UICONTROL Gerenciar simulação]**:

   * **[!UICONTROL Fechar simulação]** para sair da sessão de simulação atual.
   * **[!UICONTROL Redefinir simulação]** para limpar todos os dados da execução atual, usuários simulados selecionados, valores de eventos definidos e outras configurações de teste, para que você possa iniciar uma nova simulação do zero.

     ![Gerenciar menu de simulação aberto com Redefinir simulação e Fechar opções de simulação](assets/simulate-15.png)

Depois de validar a jornada em **[!UICONTROL Simulação]**, examine o log de **[!UICONTROL Resultados]**. Se ocorrerem erros, deixe **[!UICONTROL Simulação]**, aplique as alterações necessárias à jornada e execute **[!UICONTROL Simulação]** novamente até que a execução pareça correta. Em seguida, você pode publicar a jornada. Consulte [Publicar sua jornada](../building-journeys/publish-journey.md).

## Acionar os eventos {#firing-events}

Se a jornada incluir um ou mais eventos unitários, é possível acioná-los enquanto a Simulação estiver ativa. Para jornadas que não iniciam de um Evento, mas que contém um, essa seção não estará visível até que um usuário simulado entre na jornada.

1. Em **[!UICONTROL Selecionar tipo de evento]**, selecione o evento a ser acionado para esta simulação.

   ![Selecione a lista suspensa de tipo de evento aberta na seção Testar eventos das configurações de Simulação](assets/simulate-10-2.png)

1. Para aplicar a mesma alteração a todos os usuários da lista, use a opção **[!UICONTROL Gerenciar eventos]** para:

   * **[!UICONTROL Gerar valores de evento]** para permitir que o Journey Agent gere todas as cargas usando IA. Quando os valores são gerados, o usuário é marcado como **[!UICONTROL Pronto para enviar]**.
   * **[!UICONTROL Edite os dados do evento]** para alterar a carga de cada usuário simulado na lista.

   ![Menu Gerenciar eventos em Testar eventos com Gerar com IA e Editar todas as opções](assets/simulate-9-2.png)

1. Configure a carga do evento para cada usuário clicando no ![Editar evento](assets/do-not-localize/Smock_Edit_18_N.svg) ao lado de um usuário para:

   * **[!UICONTROL Gerar valores de evento]** para permitir que o Journey Agent gere a carga usando IA. Quando os valores são gerados, o usuário é marcado como **[!UICONTROL Pronto para enviar]**.
   * **[!UICONTROL Edite os dados do evento]** para alterar a carga apenas desse usuário simulado.

   ![Menu por usuário em Eventos de teste com opções Gerar valores de evento e Editar dados de evento](assets/simulate-8-2.png)

1. Em **[!UICONTROL Eventos de teste]**, selecione **[!UICONTROL Enviar todos]** para enviar este evento para todos os usuários simulados listados em **[!UICONTROL Usuários de teste]**, ou selecione ![Ícone Enviar](assets/do-not-localize/Smock_Send_18_N.svg) para que um único evento seja acionado somente para esse usuário.

   ![Seção de eventos de teste com Enviar todos e controles de envio por usuário para usuários marcados como Pronto](assets/simulate-11-2.png)

1. Depois que os eventos são acionados, a tela é atualizada para refletir a progressão de cada usuário.

1. Acesse a guia **[!UICONTROL Resultados]** para abrir o log de execução e analisar como cada etapa foi executada. Para obter mais informações, consulte [Exibir resultados](#viewing-results).

1. Ao concluir o teste, abra o menu **[!UICONTROL Gerenciar simulação]**:

   * **[!UICONTROL Fechar simulação]** para sair da sessão de simulação atual.
   * **[!UICONTROL Redefinir simulação]** para limpar todos os dados da execução atual, usuários simulados selecionados, valores de eventos definidos e outras configurações de teste, para que você possa iniciar uma nova simulação do zero.

     ![Gerenciar menu de simulação aberto com Redefinir simulação e Fechar opções de simulação](assets/simulate-15.png)

## Exibir resultados {#viewing-results}

A guia **[!UICONTROL Resultados]** permite exibir os resultados do teste. No menu suspenso **[!UICONTROL Usuário de teste]**, selecione o usuário simulado cuja execução você deseja inspecionar.

Selecione **[!UICONTROL Todos]** para ver os resultados agregados em cada usuário simulado na execução. Essa exibição ajuda a verificar a simulação completa rapidamente, incluindo atividades, resultados e erros, sem escolher um único usuário simulado primeiro.

![Guia Resultados com resumo da simulação, filtro de usuário de teste e cobertura de caminho na tela de jornada](assets/simulate-6-2.png)

Para cada atividade, o log pode mostrar se o usuário simulado entrou ou saiu da etapa e os erros que ocorreram durante a simulação.

Para atividades de **Aguardar**, o log inclui dois valores relacionados à duração:

* **Duração definida**: a duração especificada na atividade **Wait** para a jornada publicada e aplicada quando a jornada estiver ativa. O log registra se Simulation aplica uma substituição das configurações de teste, por exemplo, 10 segundos, em vez de depender exclusivamente do valor definido na jornada.
* **Duração real**: o tempo decorrido em que o usuário simulado permaneceu na atividade **Wait**. Este valor é definido na guia **[!UICONTROL Configurações de teste]**.

Quando aparecerem erros no log, deixe **Simulação**, aplique as alterações necessárias à jornada e execute **Simulação** novamente. Após a validação ser bem-sucedida, publique a jornada. Consulte [Publicar sua jornada](../building-journeys/publish-journey.md).
