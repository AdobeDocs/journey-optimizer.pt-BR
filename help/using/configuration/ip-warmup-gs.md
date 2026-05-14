---
solution: Journey Optimizer
product: journey optimizer
title: Introdução aos planos de aquecimento de IP
description: Saiba como implementar um plano de aquecimento de IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, capacidade de entrega
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
TQID: https://experienceleague.adobe.com/xjJKrCXUmQY5sZu2w-B09agQh-tb4qkSXM0Vh2-TDnc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 459
ht-degree: 38%

---

# Introdução aos planos de aquecimento de IP {#ip-warmup-gs}

Com o [!DNL Journey Optimizer], você pode executar facilmente fluxos de trabalho de aquecimento de IP diretamente da interface do usuário, de forma padronizada e eficiente, seguindo as práticas recomendadas para a entrega ideal. Quando os emails são enviados usando uma nova plataforma, os provedores de serviços de Internet (ISPs) suspeitam de endereços IP que não são reconhecidos. Se grandes volumes de emails forem enviados repentinamente, os ISPs freqüentemente os marcam como spam.

Para evitar a marcação como spam, é possível aumentar progressivamente o volume enviado usando o recurso plano de aquecimento de IP. Esta nova opção no menu **[!UICONTROL Administração]** permite que você automatize o gerenciamento de volumes e simplifique o processo de aquecimento sem exigir configurações complexas do jornada.

>[!NOTE]
>
>Antes de implementar seu plano de aquecimento de IP, conheça os fundamentos de capacidade de entrega, a criação de reputação e as práticas recomendadas neste [guia de capacidade de entrega de aquecimento de IP](ip-warmup-deliverability-guide.md).

➡️ [Saiba como criar e executar um plano de aquecimento de IP neste vídeo](#video)

>[!AVAILABILITY]
>
>Esse recurso só pode ser habilitado em sandboxes do tipo produção.

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

As principais etapas para implementar um plano de aquecimento de IP são as seguintes:

1. Primeiro, é necessário criar uma ou mais campanhas com a opção aquecimento de IP habilitada. [Saiba mais](ip-warmup-campaign.md)

1. Crie um plano de aquecimento de IP no [!DNL Journey Optimizer] e faça upload da planilha do Excel preparada com a ajuda do consultor(a) de capacidade de entrega. [Saiba mais](ip-warmup-plan.md)

1. Selecione uma campanha para cada fase do plano e ative as execuções correspondentes. [Saiba mais](ip-warmup-execution.md)

## Vídeo tutorial {#video}

Saiba como criar e executar um plano de aquecimento de IP.

>[!VIDEO](https://video.tv.adobe.com/v/3453845/?captions=por_br&learn=on)

>[!NOTE]
>
>Saiba mais sobre como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=pt-BR).

## Recursos adicionais {#additional-resources}

Explore estas publicações úteis do blog para obter orientação mais detalhada sobre o aquecimento de IP:

* [Guia de capacidade de entrega do Adobe Journey Optimizer: da reputação zero à experiência da caixa de entrada](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=pt) - Guia abrangente que aborda fundamentos de reputação, calendários de aquecimento, monitoramento e práticas recomendadas de solução de problemas.

* [Noções básicas sobre como configurar o aquecimento de IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949?profile.language=pt) - Saiba mais sobre os fundamentos da configuração de planos de aquecimento de IP e práticas recomendadas para uma implementação bem-sucedida.

* [Recursos avançados em planos de aquecimento de IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958?profile.language=pt) - Descubra recursos avançados e controles granulares para otimizar sua estratégia de aquecimento de IP.

* [Solução de problemas de aquecimento de IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952?profile.language=pt) - Encontre soluções para problemas comuns, como atrasos de público-alvo e saiba mais sobre os mecanismos de repetição inteligente.
