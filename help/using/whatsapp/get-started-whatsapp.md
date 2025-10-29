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
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: ht
source-wordcount: '320'
ht-degree: 100%

---

# Introdução às mensagens do WhatsApp {#get-started-whatsapp}

Agora é possível enviar mensagens do WhatsApp diretamente pelo Journey Optimizer por meio da [API de nuvem](https://developers.facebook.com/docs/whatsapp/cloud-api/) da Meta. Este recurso permite a integração perfeita do WhatsApp em jornadas e campanhas, melhorando a comunicação e o engajamento com destinatários.

* Em uma **Jornada**. Crie uma jornada, adicione uma atividade do **WhatsApp**, defina as configurações básicas e navegue até o painel direito **[!UICONTROL Ações: WhatsApp]** para criar o conteúdo da mensagem do WhatsApp. Saiba como criar uma jornada [nesta página](../building-journeys/journey-gs.md).

* Em uma **Campanha**. Crie uma campanha, selecione **WhatsApp** como ação, defina configurações básicas e edite o conteúdo da mensagem para definir a mensagem do WhatsApp a ser enviada. Saiba como criar uma campanha [nesta página](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Pré-requisitos {#prereq}

Integrar o WhatsApp com o Journey Optimizer requer o seguinte:

* Conta do Meta Business Manager
* [Conta comercial do WhatsApp com nome de remetente e número de telefone verificados](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Token de autorização do usuário com permissões apropriadas](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modelos da Meta aprovados](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

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

>[!VIDEO](https://video.tv.adobe.com/v/3470249?captions=por_br&learn=on)

+++

