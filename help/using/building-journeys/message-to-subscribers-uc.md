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
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 924
ht-degree: 5%

---

# Enviar uma mensagem aos assinantes de uma lista {#send-a-message-to-the-subscribers-of-a-list}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como criar uma jornada que envia uma mensagem aos assinantes de uma lista usando o grupo de campos Detalhes sobre Consentimento e Preferência.

>[!ENDSHADEBOX]

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página mostra como criar uma jornada que envia um email para os assinantes de uma lista substituindo o parâmetro de endereço de email padrão por uma expressão que lê os endereços dos assinantes de um campo de mapa de consentimento.

**Intenções:**

* Criar uma jornada direcionada a assinantes de uma lista específica usando uma atividade Ler público
* Substituir o endereço de email padrão em uma atividade de ação Email usando o editor de expressão
* Use as funções `entry` e `firstEntryKey` para recuperar endereços de email de assinantes em um mapa de consentimento
* Faça referência ao grupo de campos Detalhes sobre Consentimento e Preferência para acessar os dados da lista de assinaturas

**Glossário:**

* **Substituição de endereço de email (substituição de parâmetro)**: uma configuração de atividade de email de jornada que substitui o endereço de email de perfil padrão por uma expressão personalizada, usada para casos especiais, como direcionamento de lista de assinaturas. *(específico do produto)*
* **Grupo de campos de Detalhes sobre Consentimento e Preferência**: um grupo de campos de esquema do Adobe Experience Platform que contém dados de assinatura e consentimento, incluindo o mapa `subscriptions` usado para armazenar endereços de email de assinantes. *(específico do produto)*
* **`entry`função**: uma função de expressão que faz referência a um elemento de mapa por sua chave de namespace — usada aqui para fazer referência a uma lista de assinaturas específica (por exemplo, `daily-email`). *(específico do produto)*
* **`firstEntryKey`função**: uma função de expressão que recupera a primeira chave de um mapa — usada aqui para recuperar o primeiro endereço de email do mapa de assinantes de uma lista de assinaturas. *(específico do produto)*

**Medidas de Proteção:**

* A substituição de endereço de email deve ser usada somente para casos de uso específicos, como direcionamento de lista de assinaturas; na maioria dos casos, o endereço principal definido nos Campos de execução deve ser usado
* O grupo de campos Detalhes do consentimento e da preferência deve estar presente no esquema para que este caso de uso funcione
* O nome da lista de assinaturas usado na expressão (por exemplo, `daily-email`) deve corresponder exatamente ao nome configurado nos dados

**Terminologia:**

* Nome canônico: Substituição de endereço de email — Acrônimo: none — variantes: substituição de parâmetro, substituição de parâmetro de email
* Sinônimos: &quot;lista de assinaturas&quot; = &quot;lista de assinantes&quot;
* Não confunda: &quot;email address override&quot; ≠ &quot;primary email address&quot; — O endereço de email principal é o endereço padrão usado em todas as jornadas; a substituição é uma expressão por atividade usada apenas para casos especiais, como envio de lista de assinaturas

**Perguntas frequentes:**

* **P: Como faço para enviar um email aos assinantes de uma lista de assinaturas em vez de endereços de email de perfil?** — Habilite a substituição de parâmetro no campo Endereço da atividade Email e insira uma expressão usando as funções `entry` e `firstEntryKey` para recuperar endereços do mapa de assinantes da lista de assinaturas de destino.
* **P: Qual grupo de campos é necessário para este caso de uso?** — O grupo de campos Detalhes sobre Consentimento e Preferência da Adobe Experience Platform, que contém a estrutura de mapa `subscriptions` usada para armazenar endereços de email de assinantes.
* **P: Devo sempre usar a substituição de endereço de email ao direcionar assinantes?** — Não; a substituição de endereço de email é somente para casos de uso específicos. Na maioria das jornadas, o endereço principal definido nos Campos de execução deve ser usado.
* **P: O que a função `firstEntryKey` faz neste contexto?** — Ele recupera a primeira chave de endereço de email do mapa `subscribers` associado a uma lista de assinaturas específica, permitindo que a jornada direcione a assinantes individuais.

+++
