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
source-git-commit: 31e25c511d8873e54c7b92e65511108a77f84941
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 44%

---

# Introdução às mensagens do WhatsApp {#get-started-whatsapp}

Agora você pode enviar mensagens do WhatsApp diretamente pelo Journey Optimizer por meio da [API da nuvem](https://developers.facebook.com/docs/whatsapp/cloud-api/) do Meta. Este recurso permite a integração perfeita do WhatsApp em jornadas e campanhas, melhorando a comunicação e o engajamento com os recipients.

* Em uma **Jornada**. Crie uma jornada, adicione uma atividade do **WhatsApp**, defina as configurações básicas e navegue até o painel direito **[!UICONTROL Ações: WhatsApp]** para criar o conteúdo da mensagem do WhatsApp. Saiba como criar uma jornada [nesta página](../building-journeys/journey-gs.md).

* Em uma **Campanha**. Crie uma campanha, selecione **WhatsApp** como ação, defina configurações básicas e edite o conteúdo da mensagem para definir a mensagem do WhatsApp a ser enviada. Saiba como criar uma campanha [nesta página](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Pré-requisitos {#prereq}

Integrar o WhatsApp com o Journey Optimizer requer o seguinte:

* Conta do Meta Business Manager
* [Conta Comercial do WhatsApp com nome de remetente e número de telefone verificados](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Token de autorização do usuário com permissões apropriadas](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modelos da Meta aprovados](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

É necessário também concordar com o seguinte antes de continuar com a integração:

* [Regras de conteúdo do WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformidade com as políticas da Meta](https://www.whatsapp.com/legal)
* [Limites de conversa de 24 horas](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limitações {#limitations}

As seguintes limitações se aplicam ao canal do WhatsApp:

* O canal do WhatsApp no Adobe Journey Optimizer está preparado para a HIPAA, mas os fornecedores terceirizados não estão cobertos pela BAA da Adobe. Os clientes são responsáveis por sua própria conformidade e validação do fornecedor.

* Observe que mensagens de resposta automatizadas ou predefinidas ainda não são compatíveis.

* A partir de abril de 2025, a entrega de todas as mensagens de modelo de marketing para usuários do WhatsApp que têm um número de telefone dos Estados Unidos (um número composto por um código de discagem +1 e um código de área dos EUA) foi temporariamente suspensa. [Saiba mais na Metadocumentação](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* A funcionalidade de integração nativa não permite a integração com um provedor de serviços de negócios (BSP) de terceiros.

## Vídeo tutorial {#video}

O vídeo abaixo mostra como integrar o WhatsApp como um canal nativo no Adobe Journey Optimizer para fornecer mensagens seguras, em tempo real e personalizadas em escala.

+++ Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3470249?learn=on&captions=por_br)

+++

