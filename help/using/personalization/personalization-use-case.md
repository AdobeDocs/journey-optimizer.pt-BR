---
solution: Journey Optimizer
product: journey optimizer
title: 'Caso de uso do Personalization: &dois pontos; notificação de status do pedido'
description: Saiba como personalizar uma mensagem com informações de perfil, decisão de oferta e contexto.
feature: Personalization, Use Cases
topic: Personalization
role: Developer
level: Intermediate
keywords: expressão, editor, caso de uso, personalização
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
TQID: https://experienceleague.adobe.com/TzGxWPRUHz4Hf-Acni4-LjNTpAYTjZBBt-GMxlNXQHM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1086
ht-degree: 1%

---

# Caso de uso do Personalization: notificação de status do pedido {#personalization-use-case}

>[!BEGINSHADEBOX]

**Nesta página:** siga um caso de uso de status de pedido que combine dados de perfil, decisão de oferta e jornada contextual para personalizar uma notificação por push no Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Nesse caso de uso, você verá como usar vários tipos de personalização em uma única mensagem de notificação por push. Serão usados três tipos de personalização:

* **Perfil**: personalização da mensagem com base em um campo de perfil
* **Decisão de oferta**: personalização baseada em variáveis de gestão de decisões
* **Contexto**: personalização baseada em dados contextuais da jornada

O objetivo deste exemplo é encaminhar um evento para [!DNL Journey Optimizer] toda vez que um pedido de cliente for atualizado. Em seguida, uma notificação por push é enviada ao cliente com informações sobre o pedido e uma oferta personalizada.

Para esse caso de uso, os seguintes pré-requisitos são necessários:

* configurar um evento de pedido incluindo o número do pedido, o status e o nome do item. Consulte esta [seção](../event/about-events.md).
* crie uma decisão, consulte esta [seção](../offers/offer-activities/create-offer-activities.md).

➡️ [Descubra um caso de uso semelhante no vídeo](#video)

## Etapa 1 - Criar a jornada {#create-journey}

1. Clique no menu **[!UICONTROL Jornadas]** e crie uma nova jornada.

   ![](assets/perso-uc4.png)

1. Adicione o evento de entrada e uma atividade de ação **Push**.

   ![](assets/perso-uc5.png)

1. Configurar e projetar a mensagem de notificação por push. Consulte esta [seção](../push/create-push.md).

## Etapa 2 - Adicionar personalização ao perfil {#add-perso}

1. Na atividade **Push**, clique em **Editar conteúdo**.

1. Clique no campo **Título**.

   ![](assets/perso-uc2.png)

1. Insira o assunto e adicione personalização do perfil. Use a barra de pesquisa para localizar o campo de nome do perfil. No texto do assunto, coloque o cursor onde deseja inserir o campo de personalização e clique no ícone **+**. Clique em **Salvar**.

   ![](assets/perso-uc3.png)

## Etapa 3 - Adicionar personalização em dados contextuais {#add-perso-contextual-data}

1. Na atividade **Push**, clique em **Editar conteúdo** e no campo **Título**.

   ![](assets/perso-uc9.png)

1. Selecione o menu **Atributos contextuais**. Os atributos contextuais só estarão disponíveis se uma jornada tiver passado dados contextuais para a mensagem. Clique em **Journey Orchestration**. As seguintes informações contextuais são exibidas:

   * **Eventos**: esta categoria reagrupa todos os campos dos eventos colocados antes da atividade de ação de canal na jornada.
   * **Propriedades da Jornada**: os campos técnicos relacionados à jornada para um determinado perfil, por exemplo, a ID da jornada ou os erros específicos encontrados. Saiba mais em [documentação do Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Expanda o item **Eventos** e procure o campo de número do pedido relacionado ao seu evento. Você também pode usar a caixa de pesquisa. Clique no ícone **+** para inserir o campo de personalização no texto do assunto. Clique em **Salvar**.

   ![](assets/perso-uc11.png)

1. Agora clique no campo **Corpo**.

   ![](assets/perso-uc12.png)

1. Digite a mensagem e insira, no menu **[!UICONTROL Atributos contextuais]**, o nome do item do pedido e o andamento do pedido.

   ![](assets/perso-uc13.png)

1. No menu esquerdo, selecione **Offer Decisions** para inserir uma variável de decisão. Selecione o posicionamento e clique no ícone **+** ao lado da decisão de adicioná-lo ao corpo.

   ![](assets/perso-uc14.png)

1. Clique em validar para verificar se não há erros e clique em **Salvar**.

   ![](assets/perso-uc15.png)

## Etapa 4 — testar e publicar a jornada {#test-publish}

1. Clique no botão **Testar** e em **Acionar um evento**.

   ![](assets/perso-uc17.png)

1. Insira os diferentes valores para passar no teste. O modo de teste funciona somente com perfis de teste. O identificador de perfil precisa corresponder a um perfil de teste. Clique em **Enviar**.

   ![](assets/perso-uc18.png)

   A notificação por push é enviada e exibida no celular do perfil de teste.

   ![](assets/perso-uc19.png)

1. Verifique se não há erros e publique a jornada.

## Vídeo tutorial {#video}

O vídeo abaixo mostra um caso de uso semelhante que utiliza dados contextuais de uma jornada para personalizar um email.

>[!VIDEO](https://video.tv.adobe.com/v/3425027?quality=12)

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página aborda um caso de uso de notificação por push do status do pedido que combina três tipos de personalização — campo de perfil, decisão de oferta e dados de jornada contextuais — em uma única mensagem.

**Intenções**

* Criar uma jornada com um evento de pedido e uma atividade de ação de push
* Adicionar personalização baseada em perfil (nome do cliente) ao título de push
* Adicionar personalização de dados contextuais (número do pedido, nome do item, andamento do pedido) do evento de jornada
* Adicionar personalização da decisão de oferta ao corpo do push
* Testar a jornada no modo de teste e publicar

>[!TAB Glossário]

* **Personalização do perfil**: Personalization com base em um campo de perfil, como nome, acessado por meio de `profile.*` atributos. *(específico do produto)*
* **Offer decision**: Personalization com base em variáveis de gestão de decisões; inserido no menu Offer Decisions, no editor de personalização. *(específico do produto)*
* **Personalização contextual**: Personalization com base nos dados da jornada — campos de evento (por exemplo, número do pedido, nome do item, andamento do pedido) e propriedades da jornada (por exemplo, ID da jornada, erros). Disponível somente quando uma jornada tiver passado dados contextuais para a mensagem. *(específico do produto)*
* **Propriedades da Jornada**: campos técnicos relacionados à jornada de um determinado perfil, como ID da jornada ou erros encontrados, acessíveis em Atributos contextuais > Journey Orchestration. *(específico do produto)*

>[!TAB Terminologia]

* **Nome canônico:** personalização contextual — variantes: personalização baseada em contexto, personalização de contexto de jornada
* **Sinônimos:** &quot;Journey Orchestration&quot; (rótulo da interface do usuário no menu Atributos contextuais) = fonte de dados de jornada contextual
* **Não confunda:** Personalização de perfil (valores de campo de perfil estáticos, sempre disponíveis) ≠ Personalização contextual (dados de eventos e propriedades de jornada, disponíveis somente após o contexto de jornada ter sido passado para a mensagem) ≠ Personalização da decisão de oferta (variáveis de gestão de decisão)

>[!TAB Medidas de proteção e limitações]

* Os atributos contextuais estão disponíveis no editor de personalização somente se uma jornada tiver passado dados contextuais para a mensagem.
* O modo de teste funciona somente com perfis de teste; o identificador de perfil inserido na configuração do evento deve corresponder a um perfil de teste existente.

>[!TAB Perguntas frequentes]

**P: Quais são os três tipos de personalização combinados neste caso de uso?**

Personalização de perfil (nome do cliente de `profile.*`), personalização de dados contextuais (número do pedido, nome do item e progresso do pedido do evento de jornada) e personalização de decisões de oferta (uma oferta de gestão de decisões inserida no corpo).

**P: De onde vêm os atributos contextuais no editor de personalização?**

Os atributos contextuais vêm de eventos colocados antes da atividade de ação de canal na jornada e das propriedades técnicas da jornada. Eles aparecem no editor de personalização em Atributos contextuais > Journey Orchestration > Eventos (campos de evento) ou Propriedades da Jornada (metadados da jornada).

**P: Quais são os pré-requisitos para este caso de uso?**

Um evento de pedido deve ser configurado com campos de número do pedido, status e nome do item, e uma decisão deve existir na gestão de decisões.

**P: Como faço para testar a notificação por push neste caso de uso?**

Clique no botão Testar na jornada, em seguida, clique em &quot;Acionar um evento&quot; e insira os valores do evento na janela Configuração do evento. O modo de teste funciona somente com perfis de teste; o identificador do perfil deve corresponder a um perfil de teste existente.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: ae5284c7 -->
