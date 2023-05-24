---
title: Criar ofertas personalizadas
description: Saiba como criar, configurar e gerenciar suas ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 13%

---

# Criar ofertas personalizadas {#create-personalized-offers}

Antes de criar uma oferta, verifique se você criou:

* A **inserção** na qual a oferta será exibida. Consulte [Criar posicionamentos](../offer-library/creating-placements.md)
* Se quiser adicionar uma condição de qualificação: uma **regra de decisão** que definirá a condição sob a qual a oferta será apresentada. Consulte [Criar regras de decisão](../offer-library/creating-decision-rules.md).
* Um ou vários **qualificadores de coleção** (anteriormente conhecido como &quot;tags&quot;) que você pode desejar associar à oferta. Consulte [Criar qualificadores de coleção](../offer-library/creating-tags.md).

➡️ [Descubra este recurso no vídeo](#video)

A lista de ofertas personalizadas pode ser acessada na **[!UICONTROL Ofertas]** menu.

![](../assets/offers_list.png)

## Criar uma oferta {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Sobre atributos de oferta"
>abstract="Com atributos de oferta, é possível associar pares de valores chave à oferta para fins de análise e geração de relatórios."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="Atributos de oferta"
>abstract="Com atributos de oferta, é possível associar pares de valores chave à oferta para fins de análise e geração de relatórios."

Para criar uma **oferta**, siga estas etapas:

1. Clique em **[!UICONTROL Criar oferta]** e selecione **[!UICONTROL Oferta personalizada]**.

   ![](../assets/create_offer.png)

1. Especifique o nome da oferta, bem como a data e a hora de início e término. Fora dessas datas, a oferta não será selecionada pelo mecanismo de decisão.

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >A atualização das datas de início/término pode afetar o limite. [Saiba mais](add-constraints.md#capping-change-date)

1. Você também pode associar um ou vários existentes **[!UICONTROL qualificadores de coleção]** à oferta, permitindo pesquisar e organizar a Biblioteca de ofertas com mais facilidade. [Saiba mais](creating-tags.md).

1. A variável **[!UICONTROL Atributos da oferta]** permite associar pares de valor-chave à oferta para fins de relatório e análise.

1. Para atribuir rótulos de uso de dados personalizados ou principais à oferta, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Object Level Access Control)](../../administration/object-based-access.md)

   ![](../assets/offer_manage-access.png)

1. Adicione representações para definir onde a oferta será exibida na mensagem. [Saiba mais](add-representations.md)

   ![](../assets/channel-placement.png)

1. Adicione restrições para definir as condições para que a oferta seja exibida. [Saiba mais](add-constraints.md)

   >[!NOTE]
   >
   >Ao selecionar segmentos ou regras de decisão, é possível ver informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar dados.
   >
   >Observe que as estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que exige que o tempo atual seja ≥ 80 graus.

   ![](../assets/offer-constraints-example.png)

1. Revise e salve a oferta. [Saiba mais](#review)

## Revisar a oferta {#review}

Depois que as regras de elegibilidade e as restrições forem definidas, um resumo das propriedades da oferta será exibido.

1. Verifique se tudo está configurado corretamente.

1. Você pode exibir informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar dados.

   ![](../assets/offer-summary-estimate.png)

1. Quando sua oferta estiver pronta para ser apresentada aos usuários, clique em **[!UICONTROL Concluir]**.

1. Selecionar **[!UICONTROL Salvar e aprovar]**.

   ![](../assets/offer_review.png)

   Também é possível salvar a oferta como rascunho para editá-la e aprová-la posteriormente.

A oferta é exibida na lista com a variável **[!UICONTROL Aprovado]** ou **[!UICONTROL Rascunho]** Status, dependendo se você o aprovou ou não na etapa anterior.

Agora ele está pronto para ser entregue aos usuários.

![](../assets/offer_created.png)

## Gerenciar ofertas {#offer-list}

Na lista de ofertas, você pode selecionar a oferta para exibir suas propriedades. Você também pode editá-la, alterar seu status (**Rascunho**, **Aprovado**, **Arquivado**), duplique a oferta ou exclua.

![](../assets/offer_created.png)

Selecione o **[!UICONTROL Editar]** botão para voltar para o modo de edição de oferta, no qual você pode modificar a [detalhes](#create-offer), [representações](#representations), bem como editar as [regras e restrições de elegibilidade](#eligibility).

Selecione uma oferta aprovada e clique em **[!UICONTROL Desfazer aprovação]** para retornar o status da oferta para **[!UICONTROL Rascunho]**.

Para definir novamente o status como **[!UICONTROL Aprovado]**, selecione o botão correspondente que agora é exibido.

![](../assets/offer_approve.png)

A variável **[!UICONTROL Mais ações]** permite as ações descritas abaixo.

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplicar]**: cria uma oferta com as mesmas propriedades, representações, regras de elegibilidade e restrições. Por padrão, a nova oferta tem a variável **[!UICONTROL Rascunho]** status.
* **[!UICONTROL Excluir]**: remove a oferta da lista.

   >[!CAUTION]
   >
   >A oferta e seu conteúdo não estarão mais acessíveis. Esta ação não pode ser desfeita.
   >
   >Se a oferta for usada em uma coleção ou em uma decisão, ela não poderá ser excluída. Você deve remover a oferta de qualquer objeto primeiro.

* **[!UICONTROL Arquivar]**: define o status da oferta como **[!UICONTROL Arquivado]**. A oferta ainda está disponível na lista, mas você não pode definir seu status novamente como **[!UICONTROL Rascunho]** ou **[!UICONTROL Aprovado]**. Você só pode duplicá-la ou excluí-la.

Também é possível excluir ou alterar o status de várias ofertas ao mesmo tempo marcando as caixas de seleção correspondentes.

![](../assets/offer_multiple-selection.png)

Se quiser alterar o status de várias ofertas com status diferentes, somente os status relevantes serão alterados.

![](../assets/offer_change-status.png)

Depois que uma oferta é criada, você pode clicar no nome na lista.

![](../assets/offer_click-name.png)

Isso permite que você acesse informações detalhadas dessa oferta. Selecione o **[!UICONTROL Log de alterações]** guia para [monitorar todas as alterações](../get-started/user-interface.md#monitoring-changes) que foram feitas na oferta.

![](../assets/offer_information.png)

## Tutorial em vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
