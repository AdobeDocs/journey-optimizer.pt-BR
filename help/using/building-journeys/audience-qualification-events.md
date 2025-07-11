---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de qualificação de público-alvo
description: Saiba como usar e configurar eventos de qualificação de público-alvo
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: qualificação, eventos, público-alvo, jornada, plataforma
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 7%

---

# Eventos de qualificação de público-alvo {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventos de qualificação de público-alvo"
>abstract="Essa atividade permite que sua jornada acompanhe as entradas e saídas de perfis nos públicos-alvo da Adobe Experience Platform para fazer com que as pessoas entrem ou avancem em uma jornada."

## Sobre eventos de qualificação de público-alvo{#about-segment-qualification}

Essa atividade permite que sua jornada acompanhe as entradas e saídas dos perfis nos públicos da Adobe Experience Platform para que os indivíduos entrem ou avancem em uma jornada. Para saber mais sobre a criação de públicos-alvo, consulte esta [seção](../audience/about-audiences.md).

Digamos que você tenha um público-alvo de “cliente prata”. Com essa atividade, você pode fazer com que todos os novos clientes Silver insiram uma jornada e enviem a eles uma série de mensagens personalizadas.

Esse tipo de evento pode ser posicionado como a primeira etapa ou posteriormente na jornada.

➡️ [Conheça este recurso no vídeo](#video)


>[!CAUTION]
>
>Antes de começar a configurar uma qualificação de Público-alvo, [leia as Medidas de Proteção e as Limitações](#audience-qualification-guardrails).


## Configurar a atividade {#configure-segment-qualification}

Para configurar a atividade **[!UICONTROL Qualificação de público-alvo]**, siga estas etapas:

1. Expanda a categoria **[!UICONTROL Eventos]** e solte uma atividade **[!UICONTROL Qualificação de público-alvo]** na tela.

   ![](assets/segment5.png)

1. Adicione um **[!UICONTROL Rótulo]** à atividade. Esta etapa é opcional.

1. Clique no campo **[!UICONTROL Público-alvo]** e selecione os públicos-alvo que deseja aproveitar.

   >[!NOTE]
   >
   >Você pode personalizar as colunas exibidas na lista e classificá-las.

   ![](assets/segment6.png)

   Depois que o público-alvo é adicionado, o botão **[!UICONTROL Copiar]** permite copiar seu nome e ID:

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. No campo **[!UICONTROL Comportamento]**, escolha se você deseja escutar entradas de público-alvo, saídas ou ambas.

   >[!NOTE]
   >
   >**[!UICONTROL Enter]** e **[!UICONTROL Exit]** correspondem aos status de participação de público **Realized** e **Exited** da Adobe Experience Platform. Para obter mais informações sobre como avaliar um público, consulte a [documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=pt-BR#interpret-segment-results){target="_blank"}.

1. Selecione um namespace. Isso só será necessário se o evento for posicionado como a primeira etapa da jornada. Por padrão, o campo é pré-preenchido com o último namespace usado.

   >[!NOTE]
   >
   >Você só pode selecionar um namespace de identidade com base em pessoas. Se você tiver definido um namespace para uma tabela de pesquisa (por exemplo: namespace ProductID para uma pesquisa de Produto), ele não estará disponível na lista suspensa **Namespace**.

   ![](assets/segment7.png)

A carga contém as seguintes informações de contexto, que podem ser usadas em condições e ações:

* o comportamento (entrada, saída)
* o carimbo de data e hora da qualificação
* a id do público-alvo

Ao usar o editor de expressão em uma condição ou ação que segue uma atividade de **[!UICONTROL Qualificação de público-alvo]**, você tem acesso ao nó **[!UICONTROL Qualificação de público-alvo]**. Você pode escolher entre o **[!UICONTROL Último horário de qualificação]** e o **[!UICONTROL status]** (entre ou saia).

Consulte [Atividade de condição](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Uma nova jornada que inclui um evento de **Qualificação de público-alvo** se torna operacional dez minutos após a sua publicação. Esse intervalo corresponde ao intervalo de atualização do cache do serviço dedicado. Portanto, é necessário aguardar dez minutos antes de usar essa jornada.

## Práticas recomendadas {#best-practices-segments}

A atividade **[!UICONTROL Qualificação de público-alvo]** permite a entrada imediata em jornadas de indivíduos que estão sendo qualificados ou desqualificados de um público do Adobe Experience Platform.

A velocidade de recepção dessas informações é alta. As medidas mostram uma velocidade de 10.000 eventos recebidos por segundo. Como resultado, certifique-se de entender como os picos de entrada podem acontecer, como evitá-los e como preparar sua jornada para eles.

### Públicos em lote {#batch-speed-segment-qualification}

Ao usar a Qualificação de público-alvo para um público-alvo em lote, observe que um pico de entrada ocorre no momento do cálculo diário. O tamanho do pico depende do número de indivíduos entrando (ou saindo) do público diariamente.

Além disso, se o público-alvo do lote for recém-criado e usado imediatamente em uma jornada, o primeiro lote de cálculo pode fazer com que um número muito grande de indivíduos entre na jornada.

### Públicos transmitidos {#streamed-speed-segment-qualification}

Ao usar a qualificação de público-alvo para públicos-alvo transmitidos, há menos risco de grandes picos de entradas/saídas devido à avaliação contínua do público-alvo. No entanto, se a definição de público-alvo levar a um grande volume de clientes se qualificando simultaneamente, ainda poderá ocorrer um pico.

Evite usar eventos abertos e enviados com segmentação por transmissão. Em vez disso, use sinais reais de atividade do usuário, como cliques, compras ou dados de beacon. Para frequência ou lógica de supressão, use regras de negócios em vez de enviar eventos. [Saiba mais](../audience/about-audiences.md#open-and-send-event-guardrails)

Para obter mais informações sobre a segmentação por transmissão, consulte a [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

### Como evitar sobrecargas {#overloads-speed-segment-qualification}

Estas são algumas das práticas recomendadas para evitar sobrecarga de sistemas aproveitados no jornada (fontes de dados, ações personalizadas, atividades de ação de canal):

* Não use um público em lote imediatamente após sua criação em uma atividade **[!UICONTROL Qualificação de público-alvo]**. Isso evita o primeiro pico de cálculo. Um aviso amarelo será exibido na tela de jornada se você estiver prestes a usar um público que nunca foi calculado.

  ![](assets/segment-error.png)

* Coloque uma regra de limitação para fontes de dados e ações usadas em jornadas para evitar sobrecarga. Saiba mais em [documentação do Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=pt-BR){target="_blank"}. Observe que a regra de limitação não tem repetição. Se você precisar tentar novamente, use um caminho alternativo na jornada marcando a caixa **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]** em condições ou ações.

* Antes de usar o público em uma jornada de produção, avalie o volume de indivíduos qualificados para esse público diariamente. Para fazer isso, verifique o menu **[!UICONTROL Público-alvo]**, abra o público-alvo e examine o gráfico **[!UICONTROL Perfis ao longo do tempo]**.

  ![](assets/segment-overload.png)

## Medidas de proteção e limitações {#audience-qualification-guardrails}

Siga as medidas de proteção e recomendações abaixo para criar jornadas de qualificação de público-alvo. Consulte também [Práticas recomendadas de qualificação de público-alvo](#best-practices-segments).


* As jornadas de qualificação de público-alvo são projetadas principalmente para funcionar com públicos de transmissão. Essa combinação garante uma melhor experiência em tempo real. É altamente recomendável usar **streaming audiences** na atividade de qualificação de público-alvo.

  No entanto, se você quiser usar atributos baseados em assimilação em lote no público-alvo de transmissão ou um público em lote para uma jornada de qualificação de público-alvo, considere o período para avaliação/ativação de público-alvo. Um público-alvo ou público-alvo de transmissão em lote que usa atributos assimilados em lote fica pronto para uso na atividade **Qualificação de público-alvo** aproximadamente **2 horas** após a conclusão do trabalho de segmentação. Esse trabalho é executado uma vez por dia, no horário definido pelo administrador da organização da Adobe.

* Os públicos do Adobe Experience Platform são calculados uma vez por dia (**batch** públicos-alvo) ou em tempo real (para **públicos-alvo transmitidos**, usando a opção Públicos-alvo de alta frequência do Adobe Experience Platform).

   * Se o público-alvo selecionado for transmitido, os indivíduos que pertencem a esse público-alvo potencialmente entram na jornada em tempo real.
   * Se o público-alvo for em lote, as pessoas recém-qualificadas para esse público-alvo potencialmente inserirão a jornada quando o cálculo do público-alvo for executado no Adobe Experience Platform.

  Como prática recomendada, use a transmissão de públicos-alvo em uma atividade **Qualificação de público-alvo**. Para casos de uso em lote, use uma atividade **[Ler público](read-audience.md)**.

  >[!NOTE]
  >
  >Devido à natureza em lote de públicos-alvo criados usando fluxos de trabalho de composição e uploads personalizados, esses públicos-alvo não podem ser direcionados em uma atividade de &quot;Qualificação de público-alvo&quot;. Somente públicos-alvo criados usando definições de segmento podem ser aproveitados nessa atividade.


* Grupos de campos de evento de experiência não podem ser usados em jornadas que comecem com uma atividade **Ler público**, **Qualificação de público** ou **Evento comercial**.

* Ao usar uma atividade **Qualificação de público-alvo** em uma jornada, essa atividade pode levar até 10 minutos para ficar ativa e ouvir os perfis que entram ou saem do público-alvo.


>[!CAUTION]
>
>[As medidas de proteção para dados e segmentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=pt-BR){target="_blank"} também se aplicam ao Adobe Journey Optimizer.



## Vídeo tutorial {#video}

Entenda os casos de uso aplicáveis às jornadas de qualificação de público-alvo neste vídeo. Saiba como criar uma jornada com Qualificação de público-alvo e quais práticas recomendadas devem ser aplicadas.

>[!VIDEO](https://video.tv.adobe.com/v/3446209?quality=12&captions=por_br)
