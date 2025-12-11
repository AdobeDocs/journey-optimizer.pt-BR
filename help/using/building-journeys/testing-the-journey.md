---
solution: Journey Optimizer
product: journey optimizer
title: Teste a jornada
description: Saiba como testar sua jornada
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: teste, jornada, verificação, erro, solução de problemas
exl-id: 9937d9b5-df5e-4686-83ac-573c4eba983a
version: Journey Orchestration
source-git-commit: 578950270213177b4d4cc67bad8ae627e440ff44
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 7%

---

# Teste a jornada{#testing_the_journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_test"
>title="Teste a jornada"
>abstract="Use perfis de teste para testar a jornada antes de publicá-la. Isso permite analisar como as pessoas fluem na jornada e solucionam problemas antes da publicação."

Depois de criar a jornada, você pode testá-la antes de publicar. O Journey Optimizer oferece o &quot;Modo de teste&quot; como uma maneira de exibir perfis de teste conforme eles se movem ao longo da jornada, detectando possíveis erros antes da ativação. A execução de testes rápidos permite verificar se as jornadas funcionam corretamente para que você possa publicá-las com confiança.

Somente perfis de teste podem inserir uma jornada no modo de teste. Você pode criar novos perfis de teste ou transformar perfis existentes em perfis de teste. Saiba mais sobre perfis de teste em [esta seção](../audience/creating-test-profiles.md).

>[!NOTE]
>
>Antes de testar a jornada, você deve resolver todos os erros, se houver. Saiba como verificar erros antes de testar em [esta seção](../building-journeys/troubleshooting.md). Se os perfis de teste não progredirem no modo de teste, consulte [solução de problemas de transições do modo de teste](troubleshooting-execution.md#troubleshooting-test-transitions).

## Observações importantes {#important_notes}

### Limitações gerais

* **Perfis de teste somente** - Somente indivíduos sinalizados como &quot;perfis de teste&quot; no Serviço de Perfil do Cliente em Tempo Real podem inserir uma jornada no modo de teste. [Saiba como criar perfis de teste](../audience/creating-test-profiles.md).
* **Requisito de namespace** - O modo de teste está disponível somente para jornadas de rascunho que usam um namespace. O modo de teste precisa verificar se uma pessoa que entra na jornada é um perfil de teste ou não e, portanto, deve ser capaz de acessar o Adobe Experience Platform.
* **Limite de perfil** - Um máximo de 100 perfis de teste podem inserir uma jornada durante uma única sessão de teste.
* **Acionamento de evento** - Os eventos só podem ser acionados na interface. Eventos não podem ser disparados de sistemas externos usando uma API.
* **Públicos-alvo de carregamento personalizados** - o modo de teste de Jornada não oferece suporte ao enriquecimento de atributo de [público-alvo de carregamento personalizado](../audience/custom-upload.md).

### Comportamento durante e após o teste

* **Desabilitando o modo de teste** - Quando você desabilita o modo de teste, todos os perfis que estão ou foram inseridos na jornada são removidos e os relatórios são limpos.
* **Flexibilidade de reativação** - Você pode habilitar e desabilitar o modo de teste quantas vezes forem necessárias.
* **Desativação automática** - as Jornadas que permanecem inativas no modo de teste por **durante uma semana** revertem automaticamente para o status Rascunho para otimizar o desempenho e evitar o uso de recursos obsoletos.
* **Edição e publicação** - Enquanto o modo de teste estiver ativo, você não poderá modificar a jornada. No entanto, você pode publicar a jornada diretamente. Não é necessário desativar o modo de teste antes de.

### Execução

* **Comportamento de divisão** - Quando a jornada atinge uma divisão, a ramificação superior é sempre selecionada. Reordene as ramificações se desejar que um caminho diferente seja testado.
* **Tempo de evento** - Se a jornada incluir*vários eventos, acione cada evento em sequências. Enviar um evento muito cedo (antes da conclusão do primeiro nó de espera) ou muito tarde (após o tempo limite configurado) descartará o evento e enviará o perfil para um caminho de tempo limite. Sempre confirmar se as referências aos campos de carga útil do evento permanecem válidas, enviando a carga útil dentro da janela definida
* **Janela de data ativa** - Verifique se a janela de [datas/hora de início e término](journey-properties.md#dates) configurada pela jornada inclui a hora atual ao iniciar o modo de teste. Caso contrário, os eventos de teste acionados serão descartados silenciosamente. Saiba mais sobre como solucionar esse problema [nesta página](troubleshooting-execution.md#troubleshooting-test-transitions).
* **Eventos de reação** - Para eventos de reação com tempo limite, o tempo de espera mínimo e padrão é de 40 segundos.
* **Conjuntos de dados de teste** - Os eventos acionados no modo de teste são armazenados em conjuntos de dados dedicados rotulados da seguinte maneira: `JOtestmode - <schema of your event>`

<!--
* Fields from related entities are hidden from the test mode.
-->

## Ativar o modo de teste

Para usar o modo de teste, siga estas etapas:

1. Para ativar o modo de teste, clique no botão **[!UICONTROL Modo de teste]**, localizado no canto superior direito.

   ![Botão de modo de teste na interface do jornada](assets/journeytest1.png)

1. Se a jornada tiver pelo menos uma atividade **Wait**, defina o parâmetro **[!UICONTROL Wait time]** para definir o tempo que cada atividade de espera e tempo limite de evento durarão no modo de teste. O tempo padrão é de 10 segundos para esperas e tempos limite de evento. Isso garantirá que você obtenha os resultados do teste rapidamente.

   ![Configuração de parâmetro de tempo de espera no modo de teste](assets/journeytest_wait.png)

   >[!NOTE]
   >
   >Quando um evento de reação com um tempo limite é usado em uma jornada, o valor padrão e mínimo do tempo de espera é de 40 segundos. Consulte [esta seção](../building-journeys/reaction-events.md).

1. Use o botão **[!UICONTROL Acionar um evento]** para configurar e enviar eventos para a jornada.

   ![Acionar um botão de evento no modo de teste](assets/journeyuctest1.png)

1. Configure os diferentes campos esperados. No campo **Identificador de Perfil**, insira o valor do campo usado para identificar o perfil de teste. Pode ser o endereço de email, por exemplo. Envie eventos relacionados a perfis de teste. Consulte [esta seção](#firing_events).

   ![Campos de configuração de evento com entrada de Identificador de Perfil](assets/journeyuctest1-bis.png)

1. Depois que os eventos forem recebidos, clique no botão **[!UICONTROL Mostrar log]** para exibir o resultado do teste e verificá-los. Consulte [esta seção](#viewing_logs).

   ![Exibir botão de log para exibir os resultados do teste](assets/journeyuctest2.png)

1. Se houver algum erro, desative o modo de teste, modifique sua jornada e teste novamente. Depois que os testes forem concluídos, você poderá publicar sua jornada. Consulte [esta página](../building-journeys/publish-journey.md).

## Acionar os eventos {#firing_events}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_configuration"
>title="Configurar o modo de teste"
>abstract="Se a jornada contiver vários eventos, use a lista suspensa para selecionar um evento. Em seguida, para cada evento, configure os campos transmitidos e a execução do envio do evento."

Use o botão **[!UICONTROL Acionar um evento]** para configurar um evento que fará com que uma pessoa entre na jornada.


### Pré-requisitos {#trigger-events-prerequisites}

Como pré-requisito, você deve saber quais perfis são sinalizados como perfis de teste no Adobe Experience Platform. Na verdade, o modo de teste permite apenas esses perfis na jornada.

O evento deve conter uma ID. A ID esperada depende da configuração do evento. Pode ser uma ECID ou um endereço de email, por exemplo. O valor dessa chave precisa ser adicionado no campo **Identificador de Perfil**.

Se a jornada não conseguir habilitar o modo de teste com erro `ERR_MODEL_RULES_16`, verifique se o evento usado inclui um [namespace de identidade](../audience/get-started-identity.md) ao usar uma ação de canal.

O namespace de identidade é usado para identificar exclusivamente os perfis de teste. Por exemplo, se o email for usado para identificar os perfis de teste, o namespace de identidade **Email** deverá ser selecionado. Se o identificador exclusivo for o número de telefone, o namespace de identidade **Telefone** deverá ser selecionado.

>[!NOTE]
>
>* Quando você aciona um evento no modo de teste, um evento real é gerado, o que significa que ele também atingirá outras jornadas que ouvem esse evento.
>
>* Verifique se cada evento no modo de teste é acionado na ordem correta e dentro da janela de espera configurada. Por exemplo, se houver uma espera de 60 segundos, o segundo evento deverá ser acionado somente após essa espera de 60 segundos ter decorrido e antes que o tempo limite expire.
>

### Configuração de eventos {#trigger-events-configuration}

Se a jornada contiver vários eventos, use a lista suspensa para selecionar um evento. Em seguida, para cada evento, configure os campos transmitidos e a execução do envio do evento. A interface ajuda você a passar as informações corretas na carga do evento e garantir que o tipo de informação esteja correto. O modo de teste salva os últimos parâmetros usados em uma sessão de teste para uso posterior.

![Interface de configuração de evento com campos e lista suspensa para seleção de evento](assets/journeytest4.png)

A interface permite transmitir parâmetros de evento simples. Se você quiser passar coleções ou outros objetos avançados no evento, selecione **[!UICONTROL Visualização de código]** para ver todo o código da carga e modificá-lo. Por exemplo, você pode copiar e colar informações de evento preparadas por um usuário técnico.

![Visualização de código da carga do evento no formato JSON para configuração avançada](assets/journeytest5.png)

Um usuário técnico também pode usar essa interface para compor cargas de evento e acionar eventos sem precisar usar uma ferramenta de terceiros.

Ao clicar no botão **[!UICONTROL Enviar]**, o teste é iniciado. A progressão do indivíduo na jornada é representada por um fluxo visual. O caminho torna-se progressivamente verde à medida que o indivíduo se move pela jornada. Se ocorrer um erro, um símbolo de aviso será exibido na etapa correspondente. Você pode colocar o cursor nele para exibir mais informações sobre o erro e acessar detalhes completos (quando disponíveis).

![Fluxo visual de teste de Jornada mostrando o progresso do perfil e quaisquer erros](assets/journeytest6.png)

Quando você seleciona um perfil de teste diferente na tela de configuração do evento e executa o teste novamente, o fluxo visual é limpo e mostra o caminho do novo indivíduo.

Ao abrir uma jornada no teste, o caminho exibido corresponde ao último teste executado.

## Modo de teste para jornadas baseadas em regras {#test-rule-based}

O modo de teste também está disponível para jornadas que usam um evento com base em regras. Para obter mais informações sobre eventos baseados em regras, consulte [esta página](../event/about-events.md).

Ao acionar um evento, a tela **Configuração de evento** permite que você defina os parâmetros de evento que serão aprovados no teste. Você pode visualizar a condição da ID de evento clicando no ícone de dica de ferramenta no canto superior direito. Uma dica de ferramenta também está disponível ao lado de cada campo que faz parte da avaliação da regra.

![Tela de configuração de evento com dicas de ferramentas de avaliação de regra](assets/jo-event8.png)

## Modo de teste para eventos comerciais {#test-business}

Ao usar um [evento comercial](../event/about-events.md), use o modo de teste para acionar uma única entrada de perfil de teste na jornada, simular o evento e passar a ID de perfil correta. Você precisa passar os parâmetros de evento e o identificador do perfil de teste que inserirá a jornada em teste. No modo de teste, não há modo de &quot;Visualização de código&quot; disponível para jornadas com base em eventos comerciais.

Observe que, quando você aciona um evento de negócios pela primeira vez, não é possível alterar a definição do evento de negócios na mesma sessão de teste. Você só pode fazer com que a mesma pessoa ou uma pessoa diferente insira a jornada que passa o mesmo ou outro identificador. Se quiser alterar os parâmetros do evento comercial, você deverá interromper e iniciar novamente o modo de teste.

## Exibir logs {#viewing_logs}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_logs"
>title="Logs do modo de teste"
>abstract="O botão **Mostrar log** exibe os resultados do teste no formato JSON. Esses resultados exibem o número de pessoas dentro da jornada e seu status."

O botão **[!UICONTROL Mostrar log]** permite exibir os resultados do teste. Esta página exibe as informações atuais da jornada em formato JSON. Um botão permite copiar nós inteiros. É necessário atualizar manualmente a página para atualizar os resultados do teste da jornada.

![Logs de teste exibindo resultados de execução de jornada no formato JSON](assets/journeytest3.png)


>[!NOTE]
>
>Nos logs de teste, em caso de erro ao chamar um sistema de terceiros (fonte de dados ou ação), o código de erro e a resposta do erro são exibidos.

O número de indivíduos (tecnicamente chamados de instâncias) atualmente dentro da jornada é exibido. Estas são informações úteis exibidas para cada indivíduo:

* _Id_: a ID interna do indivíduo na jornada. Ele pode ser usado para fins de depuração.
* _currentstep_: a etapa em que o indivíduo está na jornada. Recomendamos adicionar rótulos às suas atividades para identificá-las mais facilmente.
* _currentstep_ > fase: o status da jornada do indivíduo (em execução, concluída, com erro ou expirada). Consulte mais informações abaixo.
* _currentstep_ > _extraInfo_: descrição do erro e outras informações contextuais.
* _currentstep_ > _fetchErrors_: informações sobre erros de busca de dados ocorridos durante esta etapa.
* _externalKeys_: o valor da fórmula de chave definida no evento.
* _enrichedData_: os dados que a jornada jornada recuperou se ela usa fontes de dados.
* _transitionHistory_: a lista de etapas seguidas pelo indivíduo. Para eventos, a carga é exibida.
* _actionExecutionErrors_ : informações sobre os erros ocorridos.

Estes são os diferentes status da jornada de um indivíduo:

* _Em execução_: o indivíduo está atualmente na jornada.
* _Concluído_: o indivíduo está no final da jornada.
* _Erro_: o indivíduo foi interrompido na jornada devido a um erro.
* _Tempo limite_: o indivíduo parou na jornada devido a uma etapa que demorou muito.

Quando um evento é acionado usando o modo de teste, um conjunto de dados é gerado automaticamente com o nome da origem.

O modo de teste cria automaticamente um Evento de experiência e o envia para a Adobe Experience Platform. O nome da origem deste evento de experiência é &quot;Eventos de teste da Journey Orchestration&quot;.

