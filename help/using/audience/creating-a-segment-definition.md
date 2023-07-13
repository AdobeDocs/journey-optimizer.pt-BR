---
solution: Journey Optimizer
product: journey optimizer
title: Criar definições de segmento
description: Saiba como criar públicos-alvo por meio de definições de segmento
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 5%

---

# Criar definições de segmento {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="Criar uma regra"
>abstract="O método de criação Criar regra permite criar uma nova definição de público-alvo usando o Serviço de público-alvo da Adobe Experience Platform."

Neste exemplo, criaremos um público-alvo para direcionar todos os clientes que moram em Atlanta, São Francisco ou Seattle e nasceram após 1980. Todos esses clientes devem ter aberto o aplicativo Luma nos últimos 7 dias e feito uma compra em 2 horas após a abertura do aplicativo.

➡️ [Saiba como criar públicos-alvo neste vídeo](#video-segment)

1. Acesse o **[!UICONTROL Públicos-alvo]** e clique no botão **[!UICONTROL Criar público]** botão.

   ![](assets/create-segment.png)

   A tela de definição de segmento permite configurar todos os campos necessários para definir seu público-alvo. Saiba como configurar públicos-alvo no [Documentação do Serviço de segmentação](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. No **[!UICONTROL Propriedades do público]** forneça um nome e uma descrição (opcional) para o público-alvo.

   ![](assets/segment-properties.png)

1. Arraste e solte os campos desejados do painel esquerdo no espaço de trabalho central e configure-os de acordo com suas necessidades.

   >[!NOTE]
   >
   >Observe que os campos disponíveis no painel esquerdo variam dependendo de como a variável **Perfil individual XDM** e **XDM ExperienceEvent** esquemas foram configurados para sua organização.  Saiba mais na [Documentação do Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.

   ![](assets/drag-fields.png)

   Neste exemplo, precisamos confiar em **Atributos** e **Eventos** campos para criar o público-alvo:

   * **Atributos**: perfis que vivem em Atlanta, São Francisco ou Seattle nascidos após 1980

     ![](assets/add-attributes.png)

   * **Eventos**: perfis que abriram o aplicativo Luma nos últimos 7 dias e fizeram uma compra em 2 horas após a abertura do aplicativo.

     ![](assets/add-events.png)

1. À medida que você adiciona e configura novos campos no espaço de trabalho, a variável **[!UICONTROL Propriedades do público]** O painel é atualizado automaticamente com informações sobre os perfis estimados pertencentes ao público-alvo.

   ![](assets/segment-estimate.png)

1. Quando o público estiver pronto, clique em **[!UICONTROL Salvar]**. Ele é exibido na lista de públicos da Adobe Experience Platform. Observe que uma barra de pesquisa está disponível para ajudá-lo a pesquisar um público específico na lista.

O público-alvo agora pode ser usado em suas jornadas. Para obter mais informações, consulte [esta seção](../audience/about-audiences.md).

## Vídeo explicativo{#video-segment}

Saiba como criar públicos.

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
