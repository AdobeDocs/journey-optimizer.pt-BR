---
title: Criar ofertas personalizadas
description: Saiba como criar, configurar e gerenciar suas ofertas
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 11596bfbe5f98e362224384d51ba32d61275bc1d
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 3%

---

# Criar ofertas personalizadas {#create-personalized-offers}

Antes de criar uma oferta, verifique se você criou:

* A **placement** em que a oferta será exibida. Consulte [Criar disposições](../offer-library/creating-placements.md)
* Se quiser adicionar uma condição de qualificação: a **regra de decisão** que definirá a condição sob a qual a oferta será apresentada. Consulte [Criar regras de decisão](../offer-library/creating-decision-rules.md).
* Um ou vários **tags** que você pode querer associar à oferta. Consulte [Criar tags](../offer-library/creating-tags.md).

➡️ [Descubra este recurso no vídeo](#video)

A lista de ofertas personalizadas pode ser acessada na variável **[!UICONTROL Ofertas]** menu.

![](../assets/offers_list.png)

## Criar uma oferta {#create-offer}

>[!CONTEXTUALHELP]
>id="od_offer_attributes"
>title="Sobre atributos de oferta"
>abstract="Com atributos de oferta, é possível associar pares de valores chave à oferta para fins de análise e geração de relatórios."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_attributes"
>title="Atributos da oferta"
>abstract="Com atributos de oferta, é possível associar pares de valores chave à oferta para fins de análise e geração de relatórios."

Para criar um **oferta** siga estas etapas:

1. Clique em **[!UICONTROL Criar oferta]**, em seguida selecione **[!UICONTROL Oferta personalizada]**.

   ![](../assets/create_offer.png)

1. Especifique o nome da oferta, bem como sua data e hora de início e término. Fora dessas datas, a oferta não será selecionada pelo mecanismo do Decisioning.

   ![](../assets/offer_details.png)

   >[!CAUTION]
   >
   >A atualização das datas de início/término pode afetar o limite. [Saiba mais](add-constraints.md#capping-change-date)

1. Também é possível associar uma ou várias **[!UICONTROL tags]** à oferta, permitindo pesquisar e organizar a Biblioteca de ofertas com mais facilidade. [Saiba mais](creating-tags.md).

1. O **[!UICONTROL Atributos da oferta]** Essa seção permite associar pares de valores chave à oferta para fins de relatório e análise.

1. Para atribuir rótulos de uso de dados personalizados ou principais à oferta, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o Controle de Acesso no Nível do Objeto (OLAC)](../../administration/object-based-access.md)

   ![](../assets/offer_manage-access.png)

1. Adicione representações para definir onde a oferta será exibida na mensagem. [Saiba mais](add-representations.md)

   ![](../assets/channel-placement.png)

1. Adicione restrições para definir as condições da oferta a ser exibida. [Saiba mais](add-constraints.md)

   >[!NOTE]
   >
   >Ao selecionar segmentos ou regras de decisão, é possível ver informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar os dados.
   >
   >Observe que as estimativas de perfil não estão disponíveis quando os parâmetros da regra incluem dados que não estão no perfil, como dados de contexto. Por exemplo, uma regra de elegibilidade que requer que o tempo atual seja ≥80 graus.

   ![](../assets/offer-constraints-example.png)

1. Revise e salve a oferta. [Saiba mais](#review)

## Revisar a oferta {#review}

Depois que as regras e restrições de qualificação tiverem sido definidas, um resumo das propriedades da oferta será exibido.

1. Verifique se tudo está configurado corretamente.

1. Você pode exibir informações sobre os perfis qualificados estimados. Clique em **[!UICONTROL Atualizar]** para atualizar os dados.

   ![](../assets/offer-summary-estimate.png)

1. Quando sua oferta estiver pronta para ser apresentada aos usuários, clique em **[!UICONTROL Concluir]**.

1. Selecionar **[!UICONTROL Salvar e aprovar]**.

   ![](../assets/offer_review.png)

   Também é possível salvar a oferta como rascunho, para editá-la e aprová-la posteriormente.

A oferta é exibida na lista com a variável **[!UICONTROL Aprovado]** ou **[!UICONTROL Rascunho]** , dependendo de você ter aprovado ou não na etapa anterior.

Agora ele está pronto para ser entregue aos usuários.

![](../assets/offer_created.png)

## Gerenciar ofertas {#offer-list}

Na lista de ofertas, é possível selecionar a oferta para exibir suas propriedades. Você também pode editá-la, alterar seu status (**Rascunho**, **Aprovado**, **Arquivado**), duplique a oferta ou exclua-a.

![](../assets/offer_created.png)

Selecione o **[!UICONTROL Editar]** botão para voltar para o modo de edição da oferta, onde você pode modificar o [detalhes](#create-offer), [representações](#representations), bem como editar o [regras e restrições de qualificação](#eligibility).

Selecione uma oferta aprovada e clique em **[!UICONTROL Desfazer aprovar]** para definir o status da oferta novamente como **[!UICONTROL Rascunho]**.

Para definir novamente o status como **[!UICONTROL Aprovado]**, selecione o botão correspondente que é exibido.

![](../assets/offer_approve.png)

O **[!UICONTROL Mais ações]** ativa as ações descritas abaixo.

![](../assets/offer_more-actions.png)

* **[!UICONTROL Duplicar]**: cria uma oferta com as mesmas propriedades, representações, regras de elegibilidade e restrições. Por padrão, a nova oferta tem a variável **[!UICONTROL Rascunho]** status.
* **[!UICONTROL Excluir]**: remove a oferta da lista.

   >[!CAUTION]
   >
   >A oferta e seu conteúdo não estarão mais acessíveis. Esta ação não pode ser desfeita.
   >
   >Se a oferta for usada em uma coleção ou decisão, ela não poderá ser excluída. Você deve remover a oferta de qualquer objeto primeiro.

* **[!UICONTROL Arquivar]**: define o status da oferta como **[!UICONTROL Arquivado]**. A oferta ainda está disponível na lista, mas não é possível definir seu status novamente como **[!UICONTROL Rascunho]** ou **[!UICONTROL Aprovado]**. Você só pode duplicá-la ou excluí-la.

Também é possível excluir ou alterar o status de várias ofertas ao mesmo tempo, marcando as caixas de seleção correspondentes.

![](../assets/offer_multiple-selection.png)

Se quiser alterar o status de várias ofertas com status diferentes, somente os status relevantes serão alterados.

![](../assets/offer_change-status.png)

Depois que uma oferta for criada, clique no nome na lista.

![](../assets/offer_click-name.png)

Isso permite acessar informações detalhadas dessa oferta. Selecione o **[!UICONTROL Log de alterações]** guia para [monitorar todas as alterações](../get-started/user-interface.md#monitoring-changes) que foram feitas à oferta.

![](../assets/offer_information.png)

## Tutorial em vídeo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
