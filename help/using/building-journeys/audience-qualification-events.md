---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de qualificação de público-alvo
description: Saiba mais sobre eventos de qualificação de público-alvo
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: qualificação, eventos, público-alvo, jornada, plataforma
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 7%

---

# Eventos de qualificação de público-alvo {#segment-qualification}

## Sobre eventos de qualificação de público-alvo{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventos de qualificação de público-alvo"
>abstract="Essa atividade permite que sua jornada acompanhe as entradas e saídas de perfis nos públicos-alvo da Adobe Experience Platform para fazer com que as pessoas entrem ou avancem em uma jornada."

Essa atividade permite que sua jornada acompanhe as entradas e saídas de perfis nos públicos-alvo da Adobe Experience Platform para fazer com que as pessoas entrem ou avancem em uma jornada. Para obter mais informações sobre criação de público, consulte esta [seção](../audience/about-audiences.md).

Digamos que você tenha um público-alvo de &quot;cliente prata&quot;. Com essa atividade, você pode fazer com que todos os novos clientes Silver insiram uma jornada e enviem a eles uma série de mensagens personalizadas.

Esse tipo de evento pode ser posicionado como a primeira etapa ou posteriormente na jornada.

>[!IMPORTANT]
>
>Lembre-se de que os públicos-alvo da Adobe Experience Platform são calculados uma vez por dia (**lote** públicos) ou em tempo real (**transmitido** públicos-alvo, usando a opção Públicos-alvo de alta frequência do Adobe Experience Platform).
>
>Se o público-alvo selecionado for transmitido, os indivíduos que pertencem a esse público-alvo potencialmente entrarão na jornada em tempo real. Se o público-alvo for em lote, as pessoas recém-qualificadas para esse público-alvo potencialmente inserirão a jornada quando o cálculo do público for executado no Adobe Experience Platform.
>
>Grupos de campos de evento de experiência não podem ser usados em jornadas que começam com uma atividade Ler público, uma qualificação de Público ou um evento comercial.


1. Expanda o **[!UICONTROL Eventos]** categoria e solte um **[!UICONTROL Qualificação do público-alvo]** atividade na tela.

   ![](assets/segment5.png)

1. Adicionar um **[!UICONTROL Rótulo]** à atividade. Esta etapa é opcional.

1. Clique em **[!UICONTROL Público]** e selecione os públicos que deseja aproveitar.

   >[!NOTE]
   >
   >Observe que é possível personalizar as colunas exibidas na lista e classificá-las.

   ![](assets/segment6.png)

   Depois que o público-alvo é adicionado, a variável **[!UICONTROL Copiar]** permite copiar o nome e a ID:

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. No **[!UICONTROL Comportamento]** escolha se deseja ouvir entradas de público-alvo, saídas ou ambas.

   >[!NOTE]
   >
   >Observe que **[!UICONTROL Enter]** e **[!UICONTROL Sair]** correspondem à variável **Realizado** e **Sair** status de participação de público do Adobe Experience Platform. Para obter mais informações sobre como avaliar um público-alvo, consulte a [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Selecione um namespace. Isso só será necessário se o evento for posicionado como a primeira etapa da jornada. Por padrão, o campo é pré-preenchido com o último namespace usado.

   >[!NOTE]
   >
   >Você só pode selecionar um namespace de identidade com base em pessoas. Se você tiver definido um namespace para uma tabela de pesquisa (por exemplo: Namespace de ProductID para uma pesquisa de Produto), ele não estará disponível na **Namespace** lista suspensa.

   ![](assets/segment7.png)

A carga contém as seguintes informações de contexto, que podem ser usadas em condições e ações:

* o comportamento (entrada, saída)
* o carimbo de data e hora da qualificação
* a id do público-alvo

Ao usar o editor de expressão em uma condição ou ação que segue um **[!UICONTROL Qualificação do público-alvo]** atividade, você terá acesso à **[!UICONTROL AudienceQualification]** nó. Você pode escolher entre as opções **[!UICONTROL Hora da última qualificação]** e a variável **[!UICONTROL status]** (entre ou saia).

Consulte [Atividade de condição](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Uma nova jornada que inclui um evento de qualificação de público-alvo está operacional dez minutos após a sua publicação. Esse intervalo corresponde ao intervalo de atualização do cache do serviço dedicado. Portanto, é necessário aguardar dez minutos antes de usar essa jornada.

## Práticas recomendadas {#best-practices-segments}

A variável **[!UICONTROL Qualificação do público-alvo]** A atividade permite a entrada imediata em jornadas de indivíduos que estão sendo qualificados ou desqualificados de um público da Adobe Experience Platform.

A velocidade de recepção dessas informações é alta. As medições efetuadas mostram uma velocidade de 10 000 eventos recebidos por segundos. Como resultado, você deve entender como os picos de entrada podem acontecer, como evitá-los e como preparar sua jornada para eles.

### Públicos em lote{#batch-speed-segment-qualification}

Ao usar a qualificação de público-alvo para um público-alvo em lote, observe que um pico de entrada ocorrerá no momento do cálculo diário. O tamanho do pico dependerá do número de indivíduos entrando (ou saindo) do público diariamente.

Além disso, se o público-alvo do lote for recém-criado e usado imediatamente em uma jornada, o primeiro lote de cálculo pode fazer com que um número muito grande de indivíduos entre na jornada.

### Públicos transmitidos{#streamed-speed-segment-qualification}

Ao usar a qualificação de público para públicos transmitidos, há menos risco de obter grandes picos de entradas/saídas devido à avaliação contínua do público. Ainda assim, se a definição de público-alvo levar a fazer com que um grande volume de clientes se qualifiquem ao mesmo tempo, também poderá haver um pico.

Para obter mais informações sobre a segmentação por transmissão, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### Como evitar sobrecargas{#overloads-speed-segment-qualification}

Estas são algumas das práticas recomendadas que ajudarão a evitar sobrecarga dos sistemas aproveitados no jornada (fontes de dados, ações personalizadas, atividades de ação de canal).

Não use, em uma **[!UICONTROL Qualificação do público-alvo]** atividade, um público-alvo em lote imediatamente após a sua criação. Evitará o primeiro pico de cálculo. Observe que haverá um aviso amarelo na tela de jornada se você estiver prestes a usar um público que nunca foi calculado.

![](assets/segment-error.png)

Coloque uma regra de limitação para fontes de dados e ações usadas em jornadas para evitar sobrecarga. Saiba mais em [Documentação do Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. Observe que a regra de limitação não tem repetição. Se precisar tentar novamente, use um caminho alternativo na jornada marcando a caixa **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]** em condições ou ações.

Antes de usar o público em uma jornada de produção, sempre avalie primeiro o volume de indivíduos qualificados para esse público todos os dias. Para fazer isso, você pode verificar o **[!UICONTROL Público]** , abra o público-alvo e observe o **[!UICONTROL Perfis ao longo do tempo]** gráfico.

![](assets/segment-overload.png)
