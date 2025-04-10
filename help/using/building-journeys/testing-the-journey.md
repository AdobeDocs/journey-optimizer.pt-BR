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
source-git-commit: 1ee75284f3c5f0c7870e8bd8779d4daf9879aa40
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 8%

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
>Antes de testar a jornada, você deve resolver todos os erros, se houver. Saiba como verificar erros antes de testar em [esta seção](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

Para usar o modo de teste, siga estas etapas:

1. Para ativar o modo de teste, clique no botão **[!UICONTROL Modo de teste]**, localizado no canto superior direito.

   ![](assets/journeytest1.png)

1. Se a jornada tiver pelo menos uma atividade **Wait**, defina o parâmetro **[!UICONTROL Wait time]** para definir o tempo que cada atividade de espera e tempo limite de evento durarão no modo de teste. O tempo padrão é de 10 segundos para esperas e tempos limite de evento. Isso garantirá que você obtenha os resultados do teste rapidamente.

   ![](assets/journeytest_wait.png)

   >[!NOTE]
   >
   >Quando um evento de reação com um tempo limite é usado em uma jornada, o valor padrão e mínimo do tempo de espera é de 40 segundos. Consulte [esta seção](../building-journeys/reaction-events.md).

1. Use o botão **[!UICONTROL Acionar um evento]** para configurar e enviar eventos para a jornada.

   ![](assets/journeyuctest1.png)

1. Configure os diferentes campos esperados. No campo **Identificador de Perfil**, insira o valor do campo usado para identificar o perfil de teste. Pode ser o endereço de email, por exemplo. Envie eventos relacionados a perfis de teste. Consulte [esta seção](#firing_events).

   ![](assets/journeyuctest1-bis.png)

1. Depois que os eventos forem recebidos, clique no botão **[!UICONTROL Mostrar log]** para exibir o resultado do teste e verificá-los. Consulte [esta seção](#viewing_logs).

   ![](assets/journeyuctest2.png)

1. Se houver algum erro, desative o modo de teste, modifique sua jornada e teste novamente. Depois que os testes forem concluídos, você poderá publicar sua jornada. Consulte [esta página](../building-journeys/publishing-the-journey.md).

## Observações importantes {#important_notes}

* No modo de teste, você só pode acionar eventos usando a interface. Eventos não podem ser disparados de sistemas externos usando uma API.
* Somente indivíduos sinalizados como &quot;perfis de teste&quot; no Serviço de perfil do cliente em tempo real têm permissão para entrar na jornada testada. Consulte esta [seção](../audience/creating-test-profiles.md).
* O modo de teste só está disponível em jornadas de rascunho que usam um namespace. O modo de teste precisa verificar se uma pessoa que entra na jornada é um perfil de teste ou não e, portanto, deve ser capaz de acessar o Adobe Experience Platform.
* O número máximo de perfis de teste que podem inserir uma jornada durante uma sessão de teste é 100.
* Quando você desativa o modo de teste, ele esvazia as jornadas de todas as pessoas que entraram anteriormente ou que estão atualmente nele. Também apaga os relatórios.
* Você pode ativar/desativar o modo de teste quantas vezes forem necessárias.
* Não é possível modificar a jornada quando o modo de teste está ativado. Quando estiver no modo de teste, você poderá publicar a jornada diretamente; não é necessário desativar o modo de teste antes de.
* Ao atingir uma divisão, a ramificação superior é sempre escolhida. É possível reorganizar a posição das ramificações de divisão se quiser que o teste escolha um caminho diferente.
* Para otimizar o desempenho e evitar o uso de recursos obsoletos, todas as jornadas no modo de teste que não forem acionadas por uma semana retornarão para o status **Rascunho**.
* Os eventos acionados pelo modo de teste são armazenados em conjuntos de dados dedicados. Esses conjuntos de dados são rotulados da seguinte maneira: `JOtestmode - <schema of your event>`
* Ao testar jornadas que incluem vários eventos, você deve acionar cada evento em sequência. Enviar um evento muito cedo (antes da conclusão do primeiro nó de espera) ou muito tarde (após o tempo limite configurado) descartará o evento e enviará o perfil a um caminho de tempo limite. Sempre confirmar se as referências aos campos de carga útil do evento permanecem válidas, enviando a carga útil dentro da janela definida


<!--
* Fields from related entities are hidden from the test mode.
-->

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

### Configuração do evento {#trigger-events-configuration}

Se a jornada contiver vários eventos, use a lista suspensa para selecionar um evento. Em seguida, para cada evento, configure os campos transmitidos e a execução do envio do evento. A interface ajuda você a passar as informações corretas na carga do evento e garantir que o tipo de informação esteja correto. O modo de teste salva os últimos parâmetros usados em uma sessão de teste para uso posterior.

![](assets/journeytest4.png)

A interface permite transmitir parâmetros de evento simples. Se você quiser passar coleções ou outros objetos avançados no evento, clique em **[!UICONTROL Exibição de Código]** para ver todo o código da carga e modificá-lo. Por exemplo, você pode copiar e colar informações de evento preparadas por um usuário técnico.

![](assets/journeytest5.png)

Um usuário técnico também pode usar essa interface para compor cargas de evento e acionar eventos sem precisar usar uma ferramenta de terceiros.

Ao clicar no botão **[!UICONTROL Enviar]**, o teste é iniciado. A progressão do indivíduo na jornada é representada por um fluxo visual. O caminho torna-se progressivamente verde à medida que o indivíduo se move pela jornada. Se ocorrer um erro, um símbolo de aviso será exibido na etapa correspondente. Você pode colocar o cursor nele para exibir mais informações sobre o erro e acessar detalhes completos (quando disponíveis).

![](assets/journeytest6.png)

Quando você seleciona um perfil de teste diferente na tela de configuração do evento e executa o teste novamente, o fluxo visual é limpo e mostra o caminho do novo indivíduo.

Ao abrir uma jornada no teste, o caminho exibido corresponde ao último teste executado.

## Modo de teste para jornadas baseadas em regras {#test-rule-based}

O modo de teste também está disponível para jornadas que usam um evento com base em regras. Para obter mais informações sobre eventos baseados em regras, consulte [esta página](../event/about-events.md).

Ao acionar um evento, a tela **Configuração de evento** permite que você defina os parâmetros de evento que serão aprovados no teste. Você pode visualizar a condição da ID de evento clicando no ícone de dica de ferramenta no canto superior direito. Uma dica de ferramenta também está disponível ao lado de cada campo que faz parte da avaliação da regra.

![](assets/jo-event8.png)

## Modo de teste para eventos comerciais {#test-business}

Ao usar um [evento comercial](../event/about-events.md), use o modo de teste para acionar uma única entrada de perfil de teste na jornada, simular o evento e passar a ID de perfil correta. Você precisa passar os parâmetros de evento e o identificador do perfil de teste que inserirá a jornada em teste. No modo de teste, não há modo de &quot;Visualização de código&quot; disponível para jornadas com base em eventos comerciais.

Observe que, quando você aciona um evento de negócios pela primeira vez, não é possível alterar a definição do evento de negócios na mesma sessão de teste. Você só pode fazer com que a mesma pessoa ou uma pessoa diferente insira a jornada que passa o mesmo ou outro identificador. Se quiser alterar os parâmetros do evento comercial, você deverá interromper e iniciar novamente o modo de teste.

## Exibir logs {#viewing_logs}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_logs"
>title="Logs do modo de teste"
>abstract="O botão **Mostrar log** exibe os resultados do teste no formato JSON. Esses resultados exibem o número de pessoas dentro da jornada e seu status."

O botão **[!UICONTROL Mostrar log]** permite exibir os resultados do teste. Esta página exibe as informações atuais da jornada em formato JSON. Um botão permite copiar nós inteiros. É necessário atualizar manualmente a página para atualizar os resultados do teste da jornada.

![](assets/journeytest3.png)


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

