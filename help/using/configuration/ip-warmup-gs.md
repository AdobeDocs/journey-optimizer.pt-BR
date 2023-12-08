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
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 9d48213d8367fdc6c0fae62b73d1706bc4983d9d
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 91%

---

# Introdução aos planos de aquecimento de IP {#ip-warmup-gs}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* **[Introdução ao aquecimento de IP](ip-warmup-gs.md)**
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* [Criar um plano de aquecimento de IP](ip-warmup-plan.md)
* [Executar o plano de aquecimento de IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>O recurso de aquecimento de IP está disponível no momento como um beta somente para usuários(as) selecionados. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

Com o [!DNL Journey Optimizer], é possível executar facilmente fluxos de trabalho de aquecimento de IP diretamente da interface, de forma padronizada e eficiente, seguindo as práticas recomendadas para uma capacidade de entrega ideal.

➡️ [Saiba como criar e executar um plano de aquecimento de IP neste vídeo](#video)

>[!CAUTION]
>
>Esse recurso se aplica somente ao canal de email.

Quando os emails são enviados usando uma nova plataforma, os provedores de serviços de Internet (ISPs) suspeitam de endereços IP que não são reconhecidos. Se grandes volumes de emails forem enviados repentinamente, os ISPs freqüentemente os marcam como spam.

Para evitar a marcação como spam, é possível aumentar progressivamente o volume enviado usando o recurso plano de aquecimento de IP. Essa nova opção no menu **[!UICONTROL Administração]** permite fazer isso de forma mais fácil e consolidada, em vez de criar jornadas diárias complexas.

>[!NOTE]
>
>Saiba mais sobre como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=pt-BR).

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

## Vídeo explicativo {#video}

Saiba como criar e executar um plano de aquecimento de IP.

>[!VIDEO](https://video.tv.adobe.com/v/3425965/?quality=12&learn=on)
