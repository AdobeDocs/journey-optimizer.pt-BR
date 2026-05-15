---
solution: Journey Optimizer
product: journey optimizer
title: Envie uma mensagem aos assinantes
description: Saiba como criar uma jornada para enviar uma mensagem aos assinantes de uma lista
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: jornada, caso de uso, mensagem, assinantes, lista, ler
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sDhncesYlIjsj2zjB-QmjWqP--0KDyp-5x5-UGLSjRc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 355
ht-degree: 15%

---

# Enviar uma mensagem aos assinantes de uma lista {#send-a-message-to-the-subscribers-of-a-list}

O objetivo deste caso de uso é criar uma jornada para enviar uma mensagem aos assinantes de uma lista.

Neste exemplo, o grupo de campos **[!UICONTROL Detalhes sobre Consentimento e Preferência]** de [!DNL Adobe Experience Platform] é usado. Para localizar este grupo de campos, no menu **[!UICONTROL Gerenciamento de Dados]**, escolha **[!UICONTROL Esquemas]**. Na guia **[!UICONTROL Grupos de campos]**, digite o nome do grupo de campos no campo de pesquisa.

![Este grupo de campos inclui o elemento de assinaturas](assets/consent-and-preference-details-field-group.png)

Para configurar essa jornada, siga estas etapas:

1. Crie uma jornada que comece com uma atividade **[!UICONTROL Read]**. Saiba mais em [Criar a primeira jornada](journey-gs.md).
1. Adicione uma atividade de ação **[!UICONTROL Email]** à jornada. Saiba como [Trabalhar com ações de canal](journey-action.md).
1. Na seção **[!UICONTROL Parâmetros de email]** das configurações de atividade de **[!UICONTROL Email]**, substitua o endereço de email padrão (`PersonalEmail.adress`) pelo endereço de email dos assinantes da lista:

   1. Clique no ícone **[!UICONTROL Habilitar substituição de parâmetro]** à direita do campo **[!UICONTROL Endereço]** e clique no ícone **[!UICONTROL Editar]**.

      ![Fluxo de Jornada com Público-alvo de Leitura para direcionamento da lista de assinantes](assets/message-to-subscribers-uc-1.png)

   1. No editor de expressão, insira a expressão para recuperar os endereços de email dos assinantes. [Leia mais](expression/expressionadvanced.md).

      Este exemplo mostra uma expressão que inclui referências a campos de mapa:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      Neste exemplo, essas funções são usadas:

      | Função | Descrição | Exemplo |
      | --- | --- | --- |
      | `entry` | Refere-se a um elemento de mapa de acordo com o namespace selecionado | Consultar uma lista de assinaturas específica |
      | `firstEntryKey` | Recupera a primeira chave de entrada de um mapa | Recuperar o primeiro email dos assinantes |

      Neste exemplo, o nome da lista de assinaturas é `daily-email`. Os endereços de email são definidos como chaves no mapa `subscribers`, que está vinculado ao mapa da lista de assinaturas.

      Leia mais sobre [referências a campos](expression/field-references.md) em expressões.

      ![Configuração de email com conteúdo personalizado para assinantes](assets/message-to-subscribers-uc-2.png)

   1. Na caixa de diálogo **[!UICONTROL Adicionar uma expressão]**, clique em **[!UICONTROL Ok]**.

>[!CAUTION]
>
>A substituição de endereço de email deve ser usada somente para casos de uso específicos. Na maioria das vezes, não é necessário alterar o endereço de email, pois o valor definido como o endereço principal nos **[!UICONTROL Campos de execução]** é o que deve ser usado. [Saiba mais](../configuration/primary-email-addresses.md)
