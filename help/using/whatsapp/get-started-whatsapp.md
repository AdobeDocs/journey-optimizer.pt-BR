---
solution: Journey Optimizer
product: journey optimizer
title: Introdução às mensagens do WhatsApp
description: Saiba como criar e enviar mensagens do WhatsApp no Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 01105f4dc3f6b52598c634373988570cf6916406
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 87%

---

# Introdução às mensagens do WhatsApp {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**Nesta página:** Entenda como o canal do WhatsApp funciona no Journey Optimizer, juntamente com seus pré-requisitos e limitações, para que você possa decidir como adicionar o WhatsApp às suas jornadas e campanhas.

>[!ENDSHADEBOX]

Agora é possível enviar mensagens do WhatsApp diretamente pelo Journey Optimizer por meio da [API de nuvem](https://developers.facebook.com/docs/whatsapp/cloud-api/) da Meta. Este recurso permite a integração perfeita do WhatsApp em jornadas e campanhas, melhorando a comunicação e o engajamento com destinatários.

* Em uma **jornada**. Crie uma jornada, adicione uma atividade do **WhatsApp**, defina as configurações básicas e navegue até o painel direito **[!UICONTROL Ações: WhatsApp]** para criar o conteúdo da mensagem do WhatsApp. Saiba como criar uma jornada [nesta página](../building-journeys/journey-gs.md).

* Em uma **Campanha**. Crie uma campanha, selecione **WhatsApp** como ação, defina configurações básicas e edite o conteúdo da mensagem para definir a mensagem do WhatsApp a ser enviada. Saiba como criar [uma campanha de ação](../campaigns/campaign-action.md#action-campaign-action) | [uma campanha acionada por API](../campaigns/api-triggered-campaigns.md) | [uma campanha orquestrada](../orchestrated/create-orchestrated-campaign.md#create)

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Pré-requisitos {#prereq}

Integrar o WhatsApp com o Journey Optimizer requer o seguinte:

* Conta do Meta Business Manager
* [Conta comercial do WhatsApp com nome do remetente e número de telefone verificados](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Token de autorização do usuário com permissões apropriadas](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modelos aprovados do Meta](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

É necessário também concordar com o seguinte antes de continuar com a integração:

* [Regras de conteúdo do WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformidade com as políticas da Meta](https://www.whatsapp.com/legal)
* [Limites de conversa de 24 horas](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limitações {#limitations}

Os seguintes limites se aplicam ao canal do WhatsApp:

* O canal do WhatsApp no Adobe Journey Optimizer é pronto para HIPAA, mas os fornecedores terceirizados não estão incluídos na cobertura do BAA da Adobe. Os clientes são responsáveis por sua própria conformidade e validação do fornecedor.

* Observe que mensagens de resposta automatizadas ou predefinidas ainda não são permitidas.

* A partir de abril de 2025, a entrega de todas as mensagens de modelo de marketing para usuários do WhatsApp que têm um número de telefone dos Estados Unidos (um número composto pelo código de país +1 e um código de área dos EUA) foi temporariamente suspensa. [Saiba mais na documentação da Meta](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* A funcionalidade de integração nativa não permite a integração com um provedor de serviços comerciais (BSP) terceirizado.

## Vídeo tutorial {#video}

O vídeo abaixo mostra como integrar o WhatsApp como um canal nativo ao Adobe Journey Optimizer para fornecer mensagens seguras, em tempo real e personalizadas em grande escala.

+++ Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## Recursos adicionais de aprendizado

Explore mais tutoriais em vídeo sobre mensagens e configuração do WhatsApp.

➡️ [Tutoriais do canal do WhatsApp](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

