---
solution: Journey Optimizer
product: journey optimizer
title: Executar operações de ciclo de vida de dados
description: Saiba como executar operações de ciclo de vida de dados
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 100%

---

# Executar operações de ciclo de vida de dados {#data-hygiene}

>[!AVAILABILITY]
>
>Os recursos de ciclo de vida dos dados estão disponíveis atualmente apenas para organizações que adquiriram as ofertas complementares **Healthcare Shield** e **Privacy and Security Shield**.

À medida que os dados são assimilados continuamente na Adobe Experience Platform, é fundamental garantir que eles sejam usados conforme planejado, atualizados quando necessário e excluídos de acordo com as políticas organizacionais.

Essas tarefas podem ser realizadas usando o menu **[!UICONTROL Ciclo de vida de dados]**, que permite configurar e agendar operações de ciclo de vida de dados, garantindo que seus registros sejam mantidos adequadamente.

![](assets/data-hygiene.png)


## Recomendações {#data-hygiene-recommendations}

Ao executar operações de higiene de dados (como excluir identidades ou conjuntos de dados), esteja ciente de que os eventos de entrega históricos associados às identidades excluídas não aparecerão mais nos relatórios padrão ou nas consultas do datalake. Isso pode resultar em discrepâncias entre o número de emails relatados como **Entregues** e o número de emails **Recebidos** nas caixas de entrada dos destinatários, especialmente em jornadas mais antigas.

Antes de realizar exclusões em grande escala, valide e exporte quaisquer dados de entrega ou relatório necessários. Se a reconciliação for necessária após a higiene de dados, entre em contato com o suporte da Adobe para acessar logs arquivados ou usar consultas do conjunto de dados do evento de feedback de mensagem para dados recentes.

## Saiba mais {#data-hygiene-learn-more}

Para obter mais informações sobre o Privacy Service e como executar operações de ciclo de vida de dados, consulte a documentação da Adobe Experience Platform:

* [Visão geral do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=pt-BR)
* [Ciclo de vida de dados na Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=pt-BR)
