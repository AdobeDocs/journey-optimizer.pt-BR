---
title: Monitorar suas campanhas da Web
description: Saiba como monitorar suas experiências da Web no Journey Optimizer
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
TQID: https://experienceleague.adobe.com/CEjKwnKx1ixUKA-mO7FfWGXaW9FyO-I-ZYyYm0scs88
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c618a0dc-1818-4c6d-9916-0d92e6796f24
  - id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: a5a700893cc89b29f5fbc214cf3e73f6069144c2
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 3%

---

# Monitorar suas campanhas da Web {#monitor-web-experiences}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como monitorar suas experiências da Web ao vivo no Adobe Journey Optimizer verificando os relatórios da Web e configurando o rastreamento de cliques em elementos específicos da página.

>[!ENDSHADEBOX]

## Verifique os relatórios da Web {#check-web-reports}

Assim que sua experiência online estiver online, você poderá verificar a guia **[!UICONTROL Web]** do [relatório de Jornada](../reports/journey-global-report-cja-web.md) e do [relatório de Campanha](../reports/campaign-global-report-cja-web.md) para comparar elementos, como o número de impressões, a taxa de cliques e o número de compromissos, com sua página da Web.

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

Para melhorar ainda mais o monitoramento da experiência online, você também pode rastrear os cliques em qualquer elemento específico do site. Isso permite exibir o número de cliques nesse elemento nos relatórios da Web. [Saiba como](#use-click-tracing)

## Usar o rastreamento de cliques {#use-click-tracking}

O web designer permite selecionar qualquer elemento do site e rastrear os cliques nesse elemento.

Essas informações podem ser úteis para melhorar a experiência dos usuários do site. Por exemplo, se os [relatórios da Web](../reports/campaign-global-report-cja-web.md) mostrarem que muitos usuários clicam em um elemento que não é realmente clicável, talvez você queira adicionar um link a esse elemento.

1. Selecione um elemento na página e escolha **[!UICONTROL Clique em rastrear elemento]** no menu contextual.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Qualquer item, clicável ou não, pode ser selecionado.

1. A ação rastreada correspondente é exibida automaticamente no painel **[!UICONTROL Clique em rastrear]**, à esquerda.

   ![](assets/web-designer-click-track-pane.png)

1. Adicione um rótulo significativo para gerenciar todos os elementos rastreados e encontrá-los facilmente nos relatórios. O campo **[!UICONTROL Seletor de CSS]** mostra informações para localizar o elemento selecionado.

1. Repita as etapas acima para selecionar quantos outros elementos forem necessários para o rastreamento de cliques. As ações correspondentes são todas listadas no painel esquerdo.

   ![](assets/web-designer-click-tracking-actions.png)

1. Para remover o rastreamento de cliques em um elemento, selecione o ícone excluir correspondente.

Assim que a campanha estiver online, você poderá verificar o número de cliques para cada elemento no [relatório online](../reports/campaign-live-report.md#web-tab) e no [relatório do Customer Journey Analytics](../reports/campaign-global-report-cja-web.md) da Web de campanhas.
