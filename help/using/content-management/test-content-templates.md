---
solution: Journey Optimizer
product: journey optimizer
title: Testar modelos de conteúdo
description: Saiba como testar a renderização de alguns de seus modelos de conteúdo de email
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
TQID: https://experienceleague.adobe.com/CC56E9rV4TImjLBbm-fsq2a4JKLnEA4wJB2DVLgOAfM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 4%

---

# Testar modelos de conteúdo de email {#test-template}

Você pode testar a renderização de alguns de seus modelos de email, sejam eles criados do zero ou de um conteúdo existente. Para isso, siga as etapas abaixo.

1. Acesse a lista de modelos de conteúdo por meio do menu **[!UICONTROL Gerenciamento de Conteúdo]** > **[!UICONTROL Modelos de Conteúdo]** e selecione qualquer modelo de email.

1. Clique em **[!UICONTROL Editar conteúdo]** das **[!UICONTROL Propriedades do modelo]**.

1. Clique em **[!UICONTROL Simular Conteúdo]** e selecione um perfil de teste para verificar sua renderização. [Saiba mais](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

   >[!NOTE]
   >
   >O [!DNL Journey optimizer] também permite que você teste diferentes variantes de seus modelos de conteúdo visualizando-as e enviando provas usando dados de entrada de exemplo carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba como simular variações de conteúdo](../test-approve/simulate-sample-input.md)

1. Você pode enviar uma prova para testar seu conteúdo e aprová-lo por alguns usuários internos antes de usá-lo em uma jornada ou campanha.

   * Para fazer isso, clique no botão **[!UICONTROL Enviar prova]** e siga as etapas descritas em [esta seção](../content-management/proofs.md).

   * Antes de enviar a prova, você deve selecionar a [configuração de email](../configuration/channel-surfaces.md) que será usada para testar seu conteúdo.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Atualmente, o rastreamento não é compatível ao testar modelos de conteúdo de email, o que significa que o rastreamento de eventos, parâmetros UTM e links de página de aterrissagem não será eficaz nas provas que estão sendo enviadas de um modelo. Para testar o rastreamento, [use o modelo de conteúdo](../email/use-email-templates.md) em um email e envie uma prova usando perfis de teste, ou dados de entrada de amostra carregados de um arquivo CSV/JSON, ou adicionados manualmente. [Saiba como visualizar e testar seu conteúdo](../content-management/preview-test.md)
