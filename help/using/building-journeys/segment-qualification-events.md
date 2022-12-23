---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de qualificação de segmento
description: Saiba mais sobre eventos de qualificação de segmento
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: dd65c4155320c818f97400548c0f9d4d6d4e2507
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 3%

---

# Eventos de qualificação de segmento {#segment-qualification}

## Sobre eventos de qualificação de segmento{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventos de qualificação de segmento"
>abstract="Essa atividade permite que sua jornada escute as entradas e saídas dos perfis nos segmentos do Adobe Experience Platform para fazer com que os indivíduos entrem ou avancem em uma jornada."

Essa atividade permite que sua jornada escute as entradas e saídas dos perfis nos segmentos do Adobe Experience Platform para fazer com que os indivíduos entrem ou avancem em uma jornada. Para obter mais informações sobre a criação de segmentos, consulte esta seção [seção](../segment/about-segments.md).

Digamos que você tenha um segmento de &quot;cliente prateado&quot;. Com essa atividade, você pode fazer com que todos os novos clientes de prata insiram uma jornada e enviem uma série de mensagens personalizadas.

Esse tipo de evento pode ser posicionado como a primeira etapa ou posterior na jornada.

>[!IMPORTANT]
>
>Lembre-se de que os segmentos do Adobe Experience Platform são calculados uma vez por dia (**lote** segmentos) ou em tempo real (**transmitido** segmentos, usando a opção Públicos de alta frequência do Adobe Experience Platform).
>
>Se o segmento selecionado for transmitido, os indivíduos pertencentes a esse segmento potencialmente entrarão na jornada em tempo real. Se o segmento for em lote, as pessoas recém-qualificadas para esse segmento potencialmente inserirão a jornada quando o cálculo de segmentos for executado no Adobe Experience Platform.
>
>Grupos de campos de evento de experiência não podem ser usados em jornadas que começam com um Segmento de Leitura, uma qualificação de Segmento ou uma atividade de evento comercial.


1. Expanda a **[!UICONTROL Eventos]** categoria e solte uma **[!UICONTROL Qualificação do segmento]** atividade na tela.

   ![](assets/segment5.png)

1. Adicione um **[!UICONTROL Rótulo]** à atividade . Esta etapa é opcional.

1. Clique no botão **[!UICONTROL Segmento]** e selecione os segmentos que deseja aproveitar.

   >[!NOTE]
   >
   >Observe que você pode personalizar as colunas exibidas na lista e classificá-las.

   ![](assets/segment6.png)

   Depois que o segmento é adicionado, a variável **[!UICONTROL Copiar]** permite copiar o nome e a ID:

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. No **[!UICONTROL Comportamento]** escolha se deseja acompanhar as entradas do segmento, as saídas ou ambos.

   >[!NOTE]
   >
   >Observe que **[!UICONTROL Enter]** e **[!UICONTROL Sair]** correspondem à **Realizado** e **Saída** status de participação do segmento da Adobe Experience Platform. Para obter mais informações sobre como avaliar um segmento, consulte [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

1. Selecione um namespace. Isso só será necessário se o evento for posicionado como a primeira etapa da jornada.

   >[!NOTE]
   >
   >Você só pode selecionar um namespace de identidade com base em pessoas. Se você tiver definido um namespace para uma tabela de pesquisa (por exemplo: Namespace do ProductID para uma Pesquisa de produto), ele não estará disponível no **Namespace** lista suspensa.

   ![](assets/segment7.png)

A carga contém as seguintes informações de contexto, que podem ser usadas em condições e ações:

* o comportamento (entrada, saída)
* o carimbo de data e hora da qualificação
* a id do segmento

Ao usar o editor de expressão em uma condição ou ação que siga um **[!UICONTROL Qualificação do segmento]** você tem acesso à atividade **[!UICONTROL Qualificação do segmento]** nó . Você pode escolher entre a variável **[!UICONTROL Hora da última qualificação]** e **[!UICONTROL status]** (entrar ou sair).

Consulte [Atividade de condição](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Uma nova jornada que inclui um evento de qualificação de segmento é operacional dez minutos após a publicação. Esse intervalo de tempo corresponde ao intervalo de atualização do cache do serviço dedicado. Portanto, é necessário aguardar dez minutos antes de usar essa jornada.

## Práticas recomendadas {#best-practices-segments}

O **[!UICONTROL Qualificação do segmento]** atividade permite a entrada imediata em jornadas de indivíduos que se qualificam ou se desqualificam de um segmento do Adobe Experience Platform.

A velocidade de recepção dessas informações é alta. As medições efetuadas mostram uma velocidade de 10 000 eventos recebidos por segundos. Como resultado, você deve entender como os picos de entrada podem ocorrer, como evitá-los e como preparar sua jornada para eles.

### Segmentos em lote{#batch-speed-segment-qualification}

Ao usar a qualificação de segmento para um segmento de lote, observe que um pico de entrada ocorrerá no momento do cálculo diário. O tamanho do pico dependerá do número de indivíduos que entram (ou saem) no segmento diariamente.

Além disso, se o segmento de lote for recém-criado e usado imediatamente em uma jornada, o primeiro lote de cálculo pode fazer com que um grande número de indivíduos insira a jornada.

### Segmentos canalizados{#streamed-speed-segment-qualification}

Ao usar a qualificação de segmento para segmentos dinamizados, há menos risco de obter grandes picos de entradas/saídas devido à avaliação contínua do segmento. Ainda assim, se a definição do segmento levar a que um grande volume de clientes se qualifique ao mesmo tempo, também pode haver um pico.

Para obter mais informações sobre a segmentação de streaming, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### Como evitar sobrecargas{#overloads-speed-segment-qualification}

Estas são algumas práticas recomendadas que ajudarão a evitar sobrecarga de sistemas aproveitados no jornada (fontes de dados, ações personalizadas, atividades de ação de canal).

Não use em **[!UICONTROL Qualificação do segmento]** , um segmento de lote imediatamente após sua criação. Ele evitará o primeiro pico de cálculo. Observe que haverá um aviso amarelo na tela de jornada se você estiver prestes a usar um segmento que nunca foi calculado.

![](assets/segment-error.png)

Coloque uma regra de limitação para fontes de dados e ações usadas em jornadas para evitar sobrecarregá-las. Saiba mais em [Documentação do Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target=&quot;_blank&quot;}. Observe que a regra de limitação não tem nenhuma tentativa. Se precisar tentar novamente, use um caminho alternativo na jornada marcando a caixa **[!UICONTROL Adicione um caminho alternativo em caso de tempo limite ou erro]** em condições ou ações.

Antes de usar o segmento em uma jornada de produção, sempre avalie primeiro o volume de indivíduos qualificados para esse segmento a cada dia. Para fazer isso, você pode verificar a variável **[!UICONTROL Segmentos]** abra o segmento e olhe para o menu **[!UICONTROL Perfis ao longo do tempo]** gráfico.

![](assets/segment-overload.png)
