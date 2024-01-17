---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos-alvo da Adobe Experience Platform
description: Saiba como trabalhar com públicos-alvo da Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: cdcce470481393c821d1c5df95639602510a690a
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 43%

---

# Introdução aos públicos-alvo da Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Público-alvo"
>abstract="Ao aproveitar os dados do perfil do cliente em tempo real, a Adobe Experience Platform permite criar facilmente definições de segmento para criar públicos-alvo que capturam as preferências e os comportamentos exclusivos dos clientes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selecione o público-alvo da campanha"
>abstract="Esta lista exibe todos os públicos-alvo disponíveis na Adobe Experience Platform. Selecione o público-alvo a ser direcionado pela campanha. A mensagem configurada na campanha será enviada a todas as pessoas pertencentes ao público-alvo selecionado. [Saiba mais sobre públicos-alvo](../audience/about-audiences.md)"

Um público-alvo é um conjunto de pessoas que compartilham comportamentos e/ou características semelhantes. Saiba mais sobre públicos-alvo na [Documentação do Serviço de segmentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.

[!DNL Journey Optimizer] O permite criar públicos-alvo da Adobe Experience Platform diretamente da **[!UICONTROL Públicos-alvo]** e aproveite-as em suas jornadas ou campanhas.

Os públicos-alvo podem ser gerados usando métodos diferentes:

* **Definições de segmento**: crie uma nova definição de público-alvo usando o Serviço de segmentação da Adobe Experience Platform. [Saiba como criar definições de segmento](creating-a-segment-definition.md)
* **Importação de arquivo CSV**: importe um público usando um arquivo CSV. Saiba como importar públicos no Adobe Experience Platform [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.
* **Composição de público**: crie um fluxo de trabalho de composição para combinar públicos-alvo existentes do Adobe Experience Platform em uma tela visual e aproveitar várias atividades (dividir, excluir...) para criar novos públicos-alvo. [Introdução à composição de público-alvo](get-started-audience-orchestration.md)

## Públicos-alvo no [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Você pode selecionar em campanhas e jornadas qualquer público da Adobe Experience Platform gerado usando [definições de segmento](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>Por enquanto, os públicos-alvo resultantes da [composições de público](../audience/get-started-audience-orchestration.md) pode ser direcionado somente em campanhas. Esse recurso está disponível como um beta privado para jornada.
>
>O uso de públicos [carregado de um arquivo CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"} O em campanhas e jornadas está disponível no momento como um beta privado.
>
>Para obter mais informações, entre em contato com o seu representante da Adobe.

É possível aproveitar os públicos-alvo no **[!DNL Journey Optimizer]** de maneiras diferentes:

* Escolha um público para uma **campanha**, na qual a mensagem é enviada a todos os indivíduos que pertencem ao público-alvo selecionado. [Saiba como definir o público-alvo de uma campanha](../campaigns/create-campaign.md#define-the-audience-audience).

* Use uma atividade de orquestração **Ler público-alvo** em uma jornada para fazer com que todas as pessoas físicas no público entrem na jornada e recebam as mensagens incluídas na jornada.

  Digamos que você tenha um público-alvo de “cliente prata”. Com essa atividade, você pode fazer com que todos os clientes prata entrem em uma jornada e enviar-lhes uma série de mensagens personalizadas. [Saiba como configurar uma atividade Ler público-alvo](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Use a atividade de evento **Qualificação de público-alvo** em uma jornada para fazer com que as pessoas físicas entrem ou avancem na jornada com base nas entradas e saídas de público do Adobe Experience Platform.

  Por exemplo, é possível fazer com que todos os novos clientes prata entrem em uma jornada e enviar-lhes mensagens. Para obter mais informações sobre como usar essa atividade, consulte [Saiba como configurar uma atividade de qualificação de público-alvo](../building-journeys/audience-qualification-events.md).

* Use a atividade **Condição** em uma jornada para criar condições com base na associação de público-alvo. [Saiba como usar públicos-alvo em condições](../building-journeys/condition-activity.md#using-a-segment).

## Métodos de avaliação de público-alvo {#evaluation-method-in-journey-optimizer}

No Adobe Journey Optimizer, os públicos-alvo são gerados a partir das definições de segmento usando um dos três métodos de avaliação abaixo.

+++ Segmentação de transmissão

A lista de perfis do público-alvo é mantida atualizada em tempo real à medida que novos dados fluem para o sistema.

A segmentação por transmissão é um processo contínuo de seleção de dados que atualiza os públicos-alvo em resposta à atividade do usuário. Depois que uma definição de segmento é criada e o público-alvo resultante é salvo, a definição de segmento é aplicada aos dados recebidos no Journey Optimizer. Isso significa que as pessoas físicas são adicionadas ou removidas do público-alvo à medida que os dados do perfil são alterados, garantindo que o público-alvo seja sempre relevante. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"}

>[!NOTE]
>
>Use os eventos corretos como critérios de segmentação de transmissão. [Saiba mais](#streaming-segmentation-events-guardrails)

+++

+++ Segmentação em lote

A lista de perfis do público-alvo é avaliada a cada 24 horas.

A segmentação em lote é uma alternativa à segmentação por transmissão que processa todos os dados de perfil de uma só vez através das definições de segmento. Isso cria um instantâneo do público-alvo que pode ser salvo e exportado para uso. No entanto, diferentemente da segmentação por transmissão, a segmentação em lote não atualiza continuamente a lista de públicos-alvo em tempo real, e os novos dados que chegam após o processo em lote não serão refletidos no público-alvo até o próximo processo em lote. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ Segmentação de borda

A segmentação de borda é a capacidade de avaliar segmentos no Adobe Experience Platform instantaneamente [na borda](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=pt-BR){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

Se você souber qual método de avaliação deseja usar, selecione-o usando a lista suspensa. Você também pode clicar no ícone de navegação ícone da pasta com uma lupa para ver uma lista dos métodos de avaliação de definição de segmento disponíveis. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Depois de definir um público-alvo pela primeira vez, perfis serão adicionados ele quando se qualificarem.

O preenchimento retroativo de dados anteriores no público-alvo pode levar até 24 horas. Depois que o público-alvo é preenchido retroativamente, ele será mantido atualizado continuamente e está sempre pronto para o direcionamento.

### Uso do evento com segmentação por transmissão {#streaming-segmentation-events-guardrails}

A segmentação por transmissão é útil para personalização em tempo real com casos de uso de alto valor. No entanto, é importante [events](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"} para usar como critérios de segmentação.

Consequentemente, para um desempenho ideal de segmentação por transmissão, evite usar os seguintes eventos:

* **Mensagem aberta** Evento de Tipo de Interação

  Ao criar seu público-alvo, o uso de **Mensagem aberta** os eventos de interação se tornaram não confiáveis, pois não são indicadores reais da atividade do usuário e podem afetar negativamente o desempenho da segmentação. Saiba mais sobre o motivo disso [Publicação no blog do Adobe](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  Portanto, o Adobe recomenda não usar **Mensagem aberta** eventos de interação com segmentação por transmissão. Em vez disso, use sinais reais de atividade do usuário, como cliques, compras ou dados de beacon.

* **Mensagem enviada** Evento de Status de Feedback

  A variável **Mensagem enviada** o evento de feedback é usado com frequência para a verificação de frequência ou supressão antes do envio de um email. A Adobe recomenda evitá-lo, pois pressiona o desempenho e pode causar degradação do sistema.

  Portanto, para frequência ou lógica de supressão, use regras de negócios em vez de **Mensagem enviada** eventos de feedback. Observe que, em breve, limites de frequência diária para perfis individuais estarão disponíveis, complementando a cadência mensal existente para regras de negócios.

>[!NOTE]
>
>Você pode usar **Mensagem aberta** e **Mensagem enviada** eventos na segmentação em lote sem preocupações com o desempenho.
