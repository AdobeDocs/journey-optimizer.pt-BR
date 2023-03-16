---
title: Adicionar restrições a uma oferta
description: Saiba como definir as condições para uma oferta ser exibida
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 47145e980c37f67b6981ffd9cc4300d29e179f45
workflow-type: tm+mt
source-wordcount: '2323'
ht-degree: 16%

---

# Adicionar restrições a uma oferta {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Sobre restrições de oferta"
>abstract="Com as restrições, é possível especificar como a oferta será priorizada e apresentada ao usuário em comparação a outras ofertas."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="Sobre restrições de oferta"
>abstract="Com as restrições, é possível especificar como a oferta será priorizada e apresentada ao usuário em comparação a outras ofertas."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Sobre a prioridade da oferta"
>abstract="Nesse campo, é possível especificar as configurações de prioridade da oferta. A prioridade é um número usado para classificar as ofertas que atendem a todas as restrições, como elegibilidade, datas e limite."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="Definir prioridade"
>abstract="A prioridade ajuda a definir a prioridade da oferta em comparação às outras caso o usuário se qualifique para mais de uma oferta. Quanto maior for a prioridade de uma oferta, maior será sua prioridade em comparação a outras ofertas."

As restrições permitem definir as condições em que uma oferta será exibida.

1. Configure o **[!UICONTROL Elegibilidade da oferta]**. [Saiba mais](#eligibility)

   ![](../assets/offer-eligibility.png)

1. Defina as **[!UICONTROL Prioridade]** da oferta em comparação a outras se o usuário se qualificar para mais de uma oferta. Quanto maior for a prioridade de uma oferta, maior será sua prioridade em comparação a outras ofertas.

   ![](../assets/offer-priority.png)

1. Especifique os **[!UICONTROL Limitação]**, o que significa o número de vezes que a oferta será apresentada. [Saiba mais](#capping)

   ![](../assets/offer-capping.png)

1. Clique em **[!UICONTROL Próximo]** para confirmar todas as restrições definidas.

Por exemplo, se você definir as seguintes restrições:

![](../assets/offer-constraints-example.png)

* A oferta será considerada somente para usuários que correspondam à regra de decisão &quot;Clientes de fidelidade Gold&quot;.
* A prioridade da oferta é definida como &quot;50&quot;, o que significa que a oferta será apresentada antes de ofertas com prioridade entre 1 e 49 e depois das com prioridade de pelo menos 51.
* A oferta será apresentada apenas uma vez por mês por usuário em todas as disposições.

## Elegibilidade {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="Definir elegibilidade"
>abstract="Por padrão, qualquer perfil será elegível para receber a oferta, mas você pode usar segmentos ou regras de decisão para restringir a oferta a perfis específicos."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Sobre a elegibilidade da oferta"
>abstract="Nesta seção, é possível usar regras de decisão para determinar quais usuários estão qualificados a receber a oferta."
>additional-url="https://video.tv.adobe.com/v/329373" text="Assistir ao vídeo de demonstração"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="Estimativa total do perfil"
>abstract="Ao selecionar segmentos ou regras de decisão, é possível ver informações sobre os perfis qualificados estimados."

O **[!UICONTROL Elegibilidade da oferta]** permite restringir a oferta a perfis específicos que você define usando segmentos ou regras de decisão.

>[!NOTE]
>
>Saiba mais sobre como usar **segmentos** versus **regras de decisão** em [esta seção](#segments-vs-decision-rules).

* Por padrão, a variável **[!UICONTROL Todos os visitantes]** estiver selecionada, o que significa que qualquer perfil será qualificado para receber a oferta.

   ![](../assets/offer-eligibility-default.png)

* Também é possível limitar a apresentação da oferta aos membros de um ou vários [Segmentos Adobe Experience Platform](../../segment/about-segments.md).

   Para fazer isso, ative o **[!UICONTROL Visitantes que se enquadram em um ou vários segmentos]** , em seguida, adicione um ou vários segmentos do painel esquerdo e combine-os usando a **[!UICONTROL E]** / **[!UICONTROL Ou]** operadores lógicos.

   ![](../assets/offer-eligibility-segment.png)

* Se você quiser associar um [regra de decisão](../offer-library/creating-decision-rules.md) para a oferta, selecione **[!UICONTROL Por regra de decisão definida]**, em seguida, arraste a regra desejada do painel esquerdo para o **[!UICONTROL Regra de decisão]** área.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >No momento, as ofertas baseadas em eventos não são compatíveis com o [!DNL Journey Optimizer]. Se você criar uma regra de decisão com base em um [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, você não poderá aproveitá-lo em uma oferta.

Ao selecionar segmentos ou regras de decisão, é possível ver informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar os dados.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>As estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que requer que o tempo atual seja ≥80 graus.

### Uso de segmentos versus regras de decisão {#segments-vs-decision-rules}

Para aplicar uma restrição, é possível restringir a seleção de ofertas aos membros de um ou vários **Segmentos Adobe Experience Platform** ou você pode usar um **regra de decisão**, ambas as soluções correspondentes a diferentes usos.

Basicamente, a saída de um segmento é uma lista de perfis, enquanto uma regra de decisão é uma função executada sob demanda em relação a um único perfil durante o processo de decisão. A diferença entre esses dois usos é detalhada abaixo.

* **Segmentos**

   Por um lado, segmentos são um grupo de perfis do Adobe Experience Platform que correspondem a uma determinada lógica com base em atributos de perfil e eventos de experiência. No entanto, o Gerenciamento de ofertas não recalcula o segmento, que pode não estar atualizado ao apresentar a oferta.

   Saiba mais sobre segmentos em [esta seção](../../segment/about-segments.md).

* **Regras de decisão**

   Por outro lado, uma regra de decisão se baseia nos dados disponíveis no Adobe Experience Platform e determina para quem uma oferta pode ser exibida. Uma vez selecionada em uma oferta ou decisão para uma determinada disposição, a regra é executada toda vez que uma decisão é tomada, o que garante que cada perfil obtenha a mais recente e a melhor oferta.

   Saiba mais sobre as regras de decisão em [esta seção](creating-decision-rules.md).

## Limitação {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Sobre o limite de oferta"
>abstract="Nesse campo, é possível especificar quantas vezes a oferta pode ser apresentada."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Usar limite"
>abstract="Para evitar o excesso de solicitações aos seus clientes, use o limite para definir o número máximo de vezes que uma oferta pode ser apresentada."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html#capping-change-date" text="Alterar datas pode afetar o limite"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="Definir a frequência limite"
>abstract="Você pode optar por redefinir o contador de limite de oferta diariamente, semanalmente ou mensalmente. Observe que, depois de salvar sua oferta, você não poderá alterar a frequência selecionada."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="Impressão"
>abstract="O uso de impressões como eventos de limite está disponível somente para canais de entrada."

O limite é usado como uma restrição para definir o número máximo de vezes que uma oferta pode ser apresentada.

Limitar o número de vezes que os usuários obtêm ofertas específicas permite evitar o excesso de solicitações dos clientes e, portanto, otimizar cada ponto de contato com a melhor oferta.

Para definir a limitação, siga as etapas principais abaixo.

1. Certifique-se de que o **[!UICONTROL Incluir limitação]** botão alternar está selecionado. A limitação é incluída por padrão.

   >[!CAUTION]
   >
   >Não é possível ativar ou desativar o limite de frequência para ofertas criadas anteriormente. Para fazer isso, você precisa duplicar a oferta ou criar uma nova.

1. Definir qual **[!UICONTROL Evento de limitação]** será considerado para aumentar o contador. [Saiba mais](#capping-event)

1. Defina o número de vezes que a oferta pode ser apresentada. [Saiba mais](#capping-count)

1. Escolha se deseja que o limite seja aplicado a todos os usuários ou somente a um perfil. [Saiba mais](#capping-type)

1. Defina as **[!UICONTROL Frequência]** para definir a frequência de redefinição da contagem de limite. [Saiba mais](#frequency-capping)

1. Se você tiver definido vários [representações](add-representations.md) para sua oferta, especifique se deseja aplicar o limite **[!UICONTROL Em todas as disposições]** ou **[!UICONTROL Para cada disposição]**. [Saiba mais](#placements)

1. Depois de salvo e aprovada, se a oferta tiver sido apresentada, o número de vezes que você especificou neste campo de acordo com os critérios e o período definido, a entrega será interrompida.

O número de vezes que uma oferta é proposta é calculado no momento da preparação do email. Por exemplo, se você preparar um email com várias ofertas, esses números serão contados em relação ao limite máximo, independentemente de o email ser enviado ou não.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>O limite de contadores será redefinido quando a oferta expirar ou 2 anos após a data de início da oferta, o que ocorrer primeiro. Saiba como definir a data de uma oferta em [esta seção](creating-personalized-offers.md#create-offer).

### Evento de limitação {#capping-event}

O **[!UICONTROL Evento de limitação]** permite definir qual **[!UICONTROL Evento de limitação]** será tido em conta para aumentar o contador:

![](../assets/offer-capping-event.png)

* **[!UICONTROL Evento de decisão]** (valor padrão): Número máximo de vezes que uma oferta pode ser apresentada.
* **[!UICONTROL Impressão]**: Número máximo de vezes que a oferta pode ser exibida para um usuário.

   >[!NOTE]
   >
   >O uso de impressões como eventos de limitação está disponível para **canais de entrada** somente.

* **[!UICONTROL Cliques]**: Número máximo de vezes que a oferta pode ser clicada por um usuário.
* **[!UICONTROL Evento personalizado]**: Você pode definir um evento personalizado que será usado para limitar o número de ofertas enviadas. Por exemplo, é possível limitar o número de resgates até que sejam iguais a 10000, ou até que um determinado perfil tenha resgatado 1 vez. Para fazer isso, use [Adobe Experience Platform XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"} esquemas para criar uma regra de evento personalizada.

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

   No exemplo abaixo, você deseja limitar o número de finalizações.

   1. Selecionar **[!UICONTROL Evento personalizado]** na lista e use o **[!UICONTROL Adicionar evento personalizado]** botão.

      ![](../assets/offer-capping-custom-event-add.png)

   1. Use o **[!UICONTROL Criar regras de evento personalizadas]** para selecionar o evento relevante. Você pode escolher qualquer ação do usuário que deseja limitar as ofertas.

      Escolha **[!UICONTROL Comércio]** > **[!UICONTROL Check-outs]** > **[!UICONTROL Valor]** e selecione **[!UICONTROL existe]** na lista suspensa.

      ![](../assets/offer-capping-custom-event.png)

   1. Depois que a regra é criada, ela é exibida na variável **[!UICONTROL Consulta de evento personalizado]** campo.

      ![](../assets/offer-capping-custom-event-query.png)
   >[!CAUTION]
   >
   >Para todos os eventos de limitação, exceto o evento de decisão, o feedback do gerenciamento de decisões pode não ser coletado automaticamente, portanto, verifique se os dados estão chegando. [Saiba mais sobre a coleta de dados](../data-collection/data-collection.md)

### Limite da contagem {#capping-count}

O **[!UICONTROL Limite da contagem]** permite especificar o número de vezes que a oferta pode ser apresentada.

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>O número deve ser um número inteiro maior que 0.

Por exemplo, você definiu um evento de limite personalizado, como o número de finalizações é levado em conta. Se você inserir 10 no **[!UICONTROL Limite da contagem]** , nenhuma outra oferta será enviada após 10 finalizações.

### Tipo de limitação {#capping-type}

Você também pode especificar se deseja que o limite seja aplicado em todos os usuários ou em um perfil específico:

![](../assets/offer-capping-total.png)

* Selecionar **[!UICONTROL Total]** para definir quantas vezes uma oferta pode ser proposta em todo o público-alvo combinado, ou seja, em todos os usuários.

   Por exemplo, se você for um varejista de eletrônica com um &quot;negócio de porta de TV&quot;, você deseja que a oferta seja retornada apenas 200 vezes em todos os perfis.

* Selecionar **[!UICONTROL Por perfil]** para definir quantas vezes uma oferta pode ser proposta ao mesmo usuário.

   Por exemplo, se você for um banco com uma oferta de &quot;Cartão de crédito Platinum&quot;, não deseja que essa oferta seja exibida mais de 5 vezes por perfil. Na verdade, você acredita que, se o usuário tiver visto a oferta 5 vezes e não tiver agido, ele terá uma chance maior de agir na próxima melhor oferta.

### Limite de frequência {#frequency-capping}

O **[!UICONTROL Frequência]** permite definir a frequência de redefinição da contagem de limite. Para fazer isso, defina o período de tempo para a contagem (diária, semanal ou mensal) e insira o número de dias/semanas/meses de sua escolha.

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>A redefinição acontece às 12h UTC, no dia definido ou no primeiro dia da semana/mês, quando aplicável. O dia de início da semana é domingo. Qualquer duração escolhida não pode exceder 2 anos (ou seja, o número correspondente de meses, semanas ou dias).

Por exemplo, se desejar que a contagem de limite seja redefinida a cada 2 semanas, selecione **[!UICONTROL Semanalmente]** do **[!UICONTROL Repetir]** lista suspensa e tipo **2** no outro campo. A redefinição ocorrerá em todos os outros domingos às 12h UTC.

>[!CAUTION]
>
>Depois de salvar a oferta, você não poderá alterar o período (mensal, semanal ou diário) selecionado para a frequência.

### Limitação e disposições {#placements}

Se você tiver definido vários [representações](add-representations.md) para sua oferta, especifique se deseja aplicar o limite **[!UICONTROL Em todas as disposições]** ou **[!UICONTROL Para cada disposição]**.

![](../assets/offer-capping-placement.png)

* **[!UICONTROL Em todas as disposições]**: as contagens de limitação totalizarão todas as decisões nas disposições associadas à oferta.

   Por exemplo, se uma oferta tiver uma **Email** posicionamento e uma **Web** posicionamento e você define o limite em **2 por perfil em todas as disposições**, cada perfil pode receber a oferta até 2 vezes no total, independentemente da combinação de disposições.

* **[!UICONTROL Para cada disposição]**: as contagens de limitação aplicam as contagens de decisão para cada disposição separadamente.

   Por exemplo, se uma oferta tiver uma **Email** posicionamento e uma **Web** posicionamento e você define o limite em **2 por perfil para cada inserção**, cada perfil poderá receber até 2 vezes a oferta para o posicionamento do email e 2 vezes mais para a disposição da Web.

### Impacto da alteração de datas no limite {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="Alterar datas pode afetar o limite"
>abstract="Se o limite for aplicado a essa oferta, ele poderá ser afetado quando você alterar a data inicial ou final."

Você deve continuar com cuidado ao alterar a data de uma oferta, pois isso pode ter impacto no limite se as seguintes condições forem atendidas:

* A oferta é [aprovado](#review).
* [Limitação](#capping) já está aplicada à oferta.
* A limitação é definida por perfil.

>[!NOTE]
>
>Saiba como definir a data de uma oferta em [esta seção](creating-personalized-offers.md#create-offer).

A limitação por perfil armazena as contagens de limitação em cada perfil. Quando você altera a data de início e de término de uma oferta aprovada, a contagem de limites para alguns perfis pode ser afetada de acordo com os diferentes cenários descritos abaixo.

![](../assets/offer-capping-change-date.png)

Estes são os cenários possíveis quando **alteração de uma data de início de oferta**:

| Cenário:<br>Se... | O que acontece:<br>então.. | Possível impacto na contagem de limites |
|--- |--- |--- |
| ... a data de início da oferta é atualizada antes do início da data de início da oferta original, | ... a contagem máxima começará na nova data inicial. | Não |
| ... a nova data de início for anterior à data de término atual, | ... o limite continuará com uma nova data inicial e a contagem de limite anterior para cada perfil continuará. | Não |
| ... a nova data de início for posterior à data de término atual, | ... o limite atual expirará e a nova contagem de limites será iniciada novamente a partir de 0 para todos os perfis na nova data inicial. | Sim |

Estes são os cenários possíveis quando **extensão de uma data final de oferta**:

| Cenário:<br>Se... | O que acontece:<br>então.. | Possível impacto na contagem de limites |
|--- |--- |--- |
| ... uma solicitação de decisão ocorre antes da data de término da oferta original, | ... a contagem de limite será atualizada e a contagem de limite anterior para cada perfil continuará. | Não |
| ... nenhum pedido de decisão ocorrer antes da data de término original, | ... a contagem máxima será redefinida na data final original de cada perfil. A nova contagem de limite será reiniciada a partir de 0 para qualquer nova solicitação de decisão que ocorrerá após a data final original. | Sim |

**Exemplo**

Digamos que você tenha uma oferta com uma data inicial original definida como **Janeiro, 1**, que expira em **Janeiro, 31**.

1. Os perfis X, Y e Z são apresentados na oferta.
1. Ligado **Janeiro, 10**, a data de término da oferta é alterada para **15 de fevereiro**.
1. **De 11 de janeiro a 31 de janeiro**, somente o perfil Z é apresentado na oferta.

   * Porque uma solicitação de decisão ocorreu antes da data de término original **para o perfil Z**, a data de término da oferta pode ser estendida para **15 de fevereiro**.
   * No entanto, como nenhuma atividade ocorreu antes da data de término original para **perfis X e Y**, seus contadores expirarão e suas contagens de limite serão redefinidas para 0 em **Janeiro, 31**.

![](../assets/offer-capping-change-date-ex.png)
