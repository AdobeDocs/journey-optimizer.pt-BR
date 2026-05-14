---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Criar ofertas substitutas
description: Saiba como criar ofertas substitutas para exibir clientes que não estão qualificados para nenhuma oferta
badge: label="Legado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 9ba16ad9-a5e7-4ce7-8ed6-7707d37178c6
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Du6LWrtaD6lS54qfxT7K8YIRvft8gO8ZlZabCMJ84tk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 411
ht-degree: 22%

---

# Criar ofertas substitutas {#create-fallback-offers}

>[!TIP]
>
>O serviço de Decisão, o novo recurso de tomada de decisão do [!DNL Adobe Journey Optimizer], agora está disponível por meio da experiência baseada em código e dos canais de email. [Saiba mais](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_new_fallback"
>title="Oferta substitutas"
>abstract="Uma oferta substituta é a oferta padrão exibida quando um usuário final não é elegível para nenhuma oferta personalizada."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_fallback_offer_details "
>title="Detalhes da oferta substituta"
>abstract="Especifique o nome da oferta substituta. Você também pode associá-la a um ou mais qualificadores de coleção existentes, permitindo pesquisar e organizar a biblioteca de ofertas com mais facilidade."

A oferta substituta é enviada aos clientes se eles não estiverem qualificados para outras ofertas. As etapas para criar uma oferta substituta consistem na criação de uma ou várias representações, como ao criar uma oferta.

➡️ [Conheça este recurso no vídeo](#video)

A lista de ofertas substitutas está acessível no menu **[!UICONTROL Ofertas]**.

![](../assets/offers_list.png)

Para criar uma oferta substituta, siga estas etapas:

>[!NOTE]
>
>Observe que, diferentemente das ofertas personalizadas, as ofertas substitutas não têm regras de qualificação e parâmetros de restrição, pois são apresentadas aos clientes como últimos recursos sem condição.

1. Clique em **[!UICONTROL Criar oferta]** e selecione **[!UICONTROL Oferta substituta]**.

   ![](../assets/create_fallback.png)

1. Especifique o nome da oferta substituta. Você também pode associar um ou vários qualificadores de coleção existentes (anteriormente conhecidos como &quot;tags&quot;) a eles, permitindo pesquisar e organizar a Biblioteca de ofertas com mais facilidade.

   ![](../assets/fallback_details.png)

1. Para atribuir rótulos de uso de dados personalizados ou principais à oferta, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Controle de Acesso em Nível de Objeto)](../../administration/object-based-access.md)

1. Crie uma ou várias representações para a oferta substituta. Para fazer isso, arraste e solte disposições do painel esquerdo, como ao criar uma oferta personalizada. Consulte [Criar ofertas personalizadas](../offer-library/creating-personalized-offers.md).

   ![](../assets/fallback_content.png)

   >[!CAUTION]
   >
   >As ofertas substitutas devem conter todas as representações usadas em uma [decisão](../offer-activities/create-offer-activities.md). Por exemplo, se você tiver cinco ofertas em uma decisão e cada uma delas tiver uma representação diferente, cinco representações deverão ser incluídas na oferta substituta.

1. Depois que as representações da oferta substituta forem adicionadas, um resumo será exibido. Se tudo estiver configurado corretamente e sua oferta substituta estiver pronta para ser apresentada aos clientes, clique em **[!UICONTROL Concluir]** e selecione **[!UICONTROL Salvar e aprovar]**.

   Você também pode salvar a oferta substituta como rascunho para editá-la e aprová-la posteriormente.

   ![](../assets/fallback_review.png)

1. A oferta substituta é exibida na lista com o status **[!UICONTROL Ativo]** ou **[!UICONTROL Rascunho]**, dependendo se você a aprovou ou não na etapa anterior.

   Agora ele está pronto para ser entregue aos clientes. Você pode selecioná-la para exibir suas propriedades e editá-la. <!-- no suppression? -->

   ![](../assets/fallback_created.png)

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/341361?captions=por_br&quality=12)

