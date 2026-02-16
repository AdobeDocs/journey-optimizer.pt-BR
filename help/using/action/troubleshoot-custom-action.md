---
solution: Journey Optimizer
product: journey optimizer
title: Solucionar problemas de ações personalizadas
description: Saiba como solucionar problemas de uma ação personalizada
feature: Journeys, Actions, Custom Actions, Monitoring
topic: Administration
role: Developer, Admin
level: Experienced
keywords: action, third-party, custom, jornada, API
exl-id: c0bb473a-82dc-4604-bd8a-020447ac0c93
source-git-commit: bae446ea38a0cb97487201f7dcf4df751578ad0a
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 1%

---

# Solucionar problemas de ações personalizadas {#troubleshoot-a-custom-action}

Você pode testar suas ações personalizadas enviando chamadas de API da seção de administração da interface do usuário do Journey Optimizer. Esse recurso ajuda você a solucionar problemas de ações personalizadas antes ou depois de usá-las em uma jornada.

Como administrador, use o recurso **[!UICONTROL Enviar solicitação de teste]** para validar as configurações de ação personalizadas fazendo chamadas de API reais diretamente do Adobe Journey Optimizer. Esse recurso garante que a estrutura de solicitação, os cabeçalhos, a autenticação e a carga sejam formatados corretamente antes de serem usados em uma jornada.

![](assets/send-test-request.png){width="70%" align="left"}

O uso desse recurso simplifica o processo de teste e validação, garantindo que as ações personalizadas funcionem corretamente nas jornadas ativas.

>[!NOTE]
>
>Se sua organização tiver o proxy IP (saída) habilitado, a chamada **[!UICONTROL Enviar solicitação de teste]** o ignorará. Para confirmar o roteamento de proxy, execute um teste ou uma jornada ativa. Saiba mais sobre o proxy IP (saída) e a habilitação em [Integrar a sistemas externos](../configuration/external-systems.md#faq).


## Pré-requisitos {#troubleshoot-custom-action-prereq}

Para usar o recurso **[!UICONTROL Enviar solicitação de teste]**, uma **ação personalizada** deve ser pré-configurada com uma URL, cabeçalhos e configurações de autenticação.

Para que os administradores usem esse recurso, são necessárias as seguintes permissões:

* Os usuários devem ter a permissão **[!DNL Manage journeys events, data sources and actions]**.
* Esta permissão está incluída na função *Administradores do Jornada*.
* A permissão **[!DNL View journeys events]** sozinha não é suficiente.

Saiba mais sobre permissões de jornada em [esta seção](../administration/high-low-permissions.md#journey-capability).

## Como usar o recurso Enviar solicitação de teste {#troubleshoot-custom-action-use}

Para testar uma ação personalizada, siga estas etapas:

1. Navegue até a tela de configuração **Ações** e selecione uma ação personalizada.
1. Clique no botão **[!UICONTROL Enviar solicitação de teste]**, na parte inferior da tela de configuração de ação.
   ![Botão Enviar solicitação de teste no painel Configuração de ação](assets/test-request.png){width="70%" align="left"}
1. Na janela pop-up, permitindo que você especifique parâmetros de solicitação:

   * Se o método de ação personalizada **for GET**, nenhuma carga será necessária.
   * Se o método de ação personalizado **for POST**, você deverá fornecer uma carga JSON.

     >[!NOTE]
     >
     >O Adobe Journey Optimizer levantará um erro se a estrutura desse JSON estiver incorreta, mas não o fará se houver uma incompatibilidade com um tipo de dados. Por exemplo, não haverá erro se um parâmetro inteiro for usado para o que deve ser uma string.

   * Se a autenticação estiver definida, você será solicitado a inserir detalhes de autenticação.

1. Clique em **Enviar** para executar a solicitação.
1. A resposta da API, incluindo cabeçalhos e códigos de status, será exibida na interface.

## Manuseio de autenticação {#troubleshoot-custom-action-auth}

Quando uma ação personalizada inclui autenticação, o Adobe Journey Optimizer exige que o usuário insira detalhes de autenticação para cada solicitação de teste:

* **Autenticação Básica**: o usuário deve fornecer a *senha*.
* **Autenticação da Chave de API:** o usuário deve inserir a chave de API *value*.
* **Autenticação Personalizada**: o usuário deve fornecer os parâmetros de autenticação na solicitação *bodyParam*. Duas seções foram adicionadas neste caso: **Solicitação de autenticação** e **Resposta de autenticação**.

## Principais benefícios {#troubleshoot-custom-action-benefits}

Como administrador do Journey Optimizer, você também pode usar ferramentas externas (por exemplo, Postman) para testar suas ações personalizadas. Os principais benefícios do recurso de solução de problemas no produto em comparação a um teste externo estão listados abaixo:

* A solicitação de teste é executada por **Jornada AJO**, significando:

   * A estrutura de solicitação exata (incluindo cabeçalhos específicos do Adobe Journey Optimizer) é usada.
   * O IP de origem e os cabeçalhos correspondem àqueles usados nas jornadas ativas.

* O recurso **[!UICONTROL Enviar solicitação de teste]** pode ser usado para solucionar problemas de **jornadas em tempo real**, pois a ação personalizada já foi implantada.

* Esse recurso de teste no produto elimina a necessidade de copiar manualmente os detalhes de configuração entre as ferramentas, reduzindo o risco de erros.

## Solução de problemas {#troubleshoot-custom-action-check}

Se a solicitação falhar, você pode verificar:

* As credenciais de autenticação inseridas no teste.
* O método de solicitação (GET vs. POST) e a carga útil correspondente.
* O endpoint da API e os cabeçalhos definidos na ação personalizada.
* Use os dados de resposta para identificar possíveis erros de configuração.

## Manipular eventos de descarte e tempos limite ociosos {#handling-discard-events-and-idle-timeouts}

Quando uma ação personalizada em uma jornada aciona um evento que deve iniciar uma **segunda jornada**, verifique se a segunda jornada está em um estado válido e se o evento é reconhecido. Se o evento não atender às condições de entrada da segunda jornada, o evento poderá ser **descartado** e aparecer em logs com códigos como `notSuitableInitialEvent`. Os tempos limite de ociosidade podem ocorrer se a segunda jornada não estiver pronta, resultando no descarte de eventos nos logs.

**Causas comuns:**

* **Qualificação de evento não atendida** - A segunda jornada usa um evento baseado em regras com uma condição de qualificação (por exemplo, um campo obrigatório não deve estar vazio, como `isNotEmpty` em um campo específico). Se a carga do evento não atender a essa condição (por exemplo, o campo está vazio ou ausente), o evento será **recebido, mas descartado**, e a segunda jornada não será acionada. Esse é o comportamento esperado; a documentação e os registros confirmam que, se a condição de qualificação não for atendida, o evento será descartado e a jornada não será acionada para esse perfil. Verifique se o conteúdo enviado pela ação personalizada inclui todos os campos e valores exigidos pela configuração do evento da segunda jornada. Saiba como [configurar eventos baseados em regras](../event/about-creating.md) e [solucionar problemas de recepção de eventos](../building-journeys/troubleshooting-execution.md#checking-if-people-enter-the-journey) na execução da jornada.

* **Segunda jornada não pronta** - Os tempos limite de ociosidade poderão ocorrer se a segunda jornada ainda não estiver ativa (por exemplo, não em modo de teste ou não ativa) ou se houver um intervalo de tempo entre o acionamento da ação personalizada e a segunda jornada pronta para receber. Verifique se a jornada de destino foi publicada ou está no modo de teste antes da ação personalizada ser acionada.

* **Diagnosticando eventos de descarte** - Se você vir eventos de descarte em logs, verifique os logs de jornada e os rastreamentos do Splunk para confirmar se o evento foi recebido, mas descartado devido à qualificação (a carga não atendia à regra) ou ao tempo. Verifique se a data de início e a configuração da segunda jornada estão corretas e se a jornada está dentro de sua janela de data ativa.

Para evitar o descarte de eventos ao encadear jornadas por meio de ações personalizadas, valide a carga do evento em relação à regra de evento da segunda jornada e confirme se a jornada de destino está ativa ou em teste e dentro de sua janela de data ativa.

## Recursos adicionais

Navegue pelas seções abaixo para saber mais sobre como configurar e usar suas ações personalizadas:

* [Introdução a ações personalizadas](../action/action.md) - Saiba o que é uma ação personalizada e como ela ajuda você a se conectar a sistemas de terceiros
* [Configurar ações personalizadas](../action/about-custom-action-configuration.md) - Saiba como criar e configurar uma ação personalizada
* [Usar ações personalizadas](../building-journeys/using-custom-actions.md) - Saiba como usar ações personalizadas em suas jornadas
* [Envio de coleções em parâmetros de ação personalizados](../building-journeys/collections.md) - Saiba como enviar uma coleção em parâmetros de ação personalizados que é preenchida dinamicamente no tempo de execução

