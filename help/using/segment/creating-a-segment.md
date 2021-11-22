---
title: Criar um segmento
description: Saiba como criar segmentos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 5%

---

# Construir segmentos {#build-segments}

Neste exemplo, criaremos um segmento para direcionar todos os clientes que moram em Atlanta, São Francisco ou Seattle e nascem depois de 1980. Todos esses clientes devem ter aberto o aplicativo Luma nos últimos 7 dias, e então fizeram uma compra dentro de 2 horas após abrir o aplicativo.

1. Acesse o **[!UICONTROL Segments]** , em seguida, clique no botão **[!UICONTROL Create segment]** botão.

   ![](../assets/create-segment.png)

   A tela de definição de segmento permite configurar todos os campos necessários para definir seu segmento. Saiba como configurar segmentos no [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}.

   ![](../assets/segment-builder.png)

1. No **[!UICONTROL Segment properties]** , forneça um nome e uma descrição (opcional) para o segmento.

   ![](../assets/segment-properties.png)

1. Arraste e solte os campos desejados do painel esquerdo para o espaço de trabalho central e configure-os de acordo com suas necessidades.

   >[!NOTE]
   >
   >Observe que os campos disponíveis no painel esquerdo variam dependendo de como a variável **Perfil individual XDM** e **ExperiênciaEvento XDM** os esquemas foram configurados para sua organização.  Saiba mais na [Documentação do Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

   ![](../assets/drag-fields.png)

   Neste exemplo, precisamos confiar em **Atributos** e **Eventos** campos para criar o segmento:

   * **Atributos**: perfis que vivem em Atlanta, São Francisco ou Seattle, nascidos após 1980

      ![](../assets/add-attributes.png)

   * **Eventos**: perfis que abriram o aplicativo Luma nos últimos 7 dias, então fizeram uma compra dentro de 2 horas após abrir o aplicativo.

      ![](../assets/add-events.png)

1. À medida que você adiciona e configura novos campos no espaço de trabalho, a variável **[!UICONTROL Segment Properties]** O painel é atualizado automaticamente com informações sobre os perfis estimados pertencentes ao segmento.

   ![](../assets/segment-estimate.png)

1. Quando o segmento estiver pronto, clique em **[!UICONTROL Save]**. É exibido na lista de segmentos do Adobe Experience Platform. Observe que uma barra de pesquisa está disponível para ajudá-lo a pesquisar um segmento específico na lista.

O segmento agora pode ser usado em suas jornadas. Para obter mais informações, consulte [esta seção](../segment/about-segments.md).

## Tutorial em vídeo{#create-segment-video}

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
