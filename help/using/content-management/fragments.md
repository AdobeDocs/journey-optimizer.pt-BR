---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a fragmentos
description: Saiba como trabalhar com fragmentos de conteúdo para reutilizar conteúdo em campanhas e jornadas do Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
TQID: https://experienceleague.adobe.com/2XVXr3MjYnD-7o0C2ARXQ8j3sJOFfJfvjfCEZdkV50I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 06565328f42ff79943f774df55d8e41118b40815
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 19%

---

# Introdução a fragmentos {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Definir seus próprios fragmentos"
>abstract="Crie e gerencie fragmentos independentes para tornar o conteúdo reutilizável em várias jornadas e campanhas."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Criar fragmentos"

Um fragmento é um componente reutilizável que pode ser referenciado em um ou mais emails em [!DNL Journey Optimizer] campanhas e jornadas. Essa funcionalidade permite pré-criar vários blocos de conteúdo personalizados que podem ser usados por usuários de marketing para reunir rapidamente o conteúdo de email em um processo de design aprimorado.

>[!NOTE]
>
>Os **[!UICONTROL Fragmentos]** descritos nesta página são componentes de **conteúdo** reutilizáveis. Eles são diferentes de:
>
>* **[Fragmentos de Jornada](../building-journeys/journey-fragments.md)** — conjuntos reutilizáveis de nós de jornada inseridos em jornadas.
>* **[Fragmentos de conteúdo do AEM](../integrations/aem-fragments.md)** — conteúdo criado no Adobe Experience Manager e usado em [!DNL Journey Optimizer].

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Saiba como gerenciar, criar e usar fragmentos nestes vídeos](#video-fragments)

Para aproveitar ao máximo os fragmentos:

* **Criar seus próprios fragmentos**: crie fragmentos visuais ou de expressão, do zero ou salvando o conteúdo como fragmento. [Saiba como criar um fragmento](create-fragments.md). Além disso, você pode aproveitar a **API REST de conteúdo** do Journey Optimizer para gerenciar fragmentos de conteúdo. Para obter mais informações, consulte a [documentação das APIs do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}.
* **Reutilizar os fragmentos:** Use-os quantas vezes forem necessárias no conteúdo. Consulte [Adicionar fragmentos visuais](../email/use-visual-fragments.md) e [Aproveitar fragmentos de expressão](../personalization/use-expression-fragments.md)

## Antes de começar {#fragment-prerequisites}

Para criar, editar, arquivar e publicar fragmentos, você precisa das permissões de **[!DNL Manage library items]** e **[Publicar fragmento]** inclusas no perfil do produto **[!DNL Content Library Manager]**. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

Nesta versão, as seguintes limitações se aplicam:

* **Fragmentos visuais** estão disponíveis somente para o canal de email.
* **Fragmentos de expressão** não estão disponíveis para o canal no aplicativo.

Mais medidas de proteção aplicáveis aos fragmentos estão disponíveis em [esta seção](../start/guardrails.md#fragments-guardrails).

## Fragmentos visuais e de expressão {#visual-expression}

Dois tipos de fragmentos estão disponíveis:

* **Fragmentos visuais** são blocos visuais predefinidos que você pode reutilizar em várias entregas de email usando o [Designer de email](../email/get-started-email-design.md) ou em [modelos de conteúdo](../email/use-email-templates.md).
* **Fragmentos de expressão** são expressões predefinidas disponíveis em uma entrada dedicada no [editor de personalização](../personalization/personalization-build-expressions.md).

Todos os fragmentos criados podem ser acessados no menu esquerdo **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**. [Saiba como gerenciar fragmentos](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## Vídeo tutorial {#video-fragments}

Saiba como gerenciar, criar e usar **fragmentos visuais** no [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Saiba como gerenciar, criar e usar **fragmentos de expressão** em [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
