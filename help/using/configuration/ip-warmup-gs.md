---
solution: Journey Optimizer
product: journey optimizer
title: Introdução aos planos de aquecimento de IP
description: Saiba como implementar um plano de aquecimento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
source-git-commit: 53be033ff0474cbafff71ed36194c18627234fd4
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 27%

---

# Introdução aos planos de aquecimento de IP {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* **[Introdução ao aquecimento de IP](ip-warmup-gs.md)**
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* [Criar um plano de aquecimento de IP](ip-warmup-plan.md)
* [Executar o plano de aquecimento de IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>O recurso de aquecimento de IP está disponível no momento como um beta apenas para usuários selecionados. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

Com [!DNL Journey Optimizer]No entanto, é possível executar facilmente workflows de aquecimento de IP diretamente da interface do usuário, de forma padronizada e eficiente, seguindo as práticas recomendadas para a entrega ideal.

>[!CAUTION]
>
>Esse recurso se aplica somente ao canal de email.

Quando os emails são enviados usando uma nova plataforma, os provedores de serviços de Internet (ISPs) suspeitam de endereços IP que não são reconhecidos. Se grandes volumes de emails forem enviados repentinamente, os ISPs freqüentemente os marcam como spam.

Para evitar ser marcado como spam, você pode aumentar progressivamente o volume enviado usando o recurso de plano de aquecimento de IP. Uma nova opção no **[!UICONTROL Administração]** permite que você faça isso com mais tranquilidade em vez de criar jornadas diárias complexas. Isso deve garantir o desenvolvimento suave da fase de inicialização e permitir que você reduza a taxa geral de endereços inválidos.

>[!NOTE]
>
>Saiba mais sobre como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

As principais etapas para implementar um plano de aquecimento de IP são as seguintes:

1. Primeiro, é necessário criar uma ou mais campanhas com a opção de aquecimento de IP ativada. [Saiba mais](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. Crie um plano de aquecimento de IP e faça upload do seu plano. [Saiba mais](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. Selecione uma campanha para cada fase do plano e ative as execuções correspondentes. [Saiba mais](ip-warmup-running.md)
