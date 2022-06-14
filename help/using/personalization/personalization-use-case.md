---
title: Caso de uso de personalização &dois pontos; notificação de status do pedido
description: Saiba como personalizar uma mensagem com informações de perfil, decisão de oferta e contexto.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 0ca491315e214e3c12bec11a93da1a2b98b493b6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Caso de uso de personalização: notificação de status do pedido {#personalization-use-case}

Nesse caso de uso, você verá como usar vários tipos de personalização em uma única mensagem de notificação por push. Serão usados três tipos de personalização:

* **Perfil**: personalização de mensagem com base em um campo de perfil
* **Decisão da oferta**: personalização com base em variáveis de offer decisioning
* **Contexto**: personalização com base em dados contextuais da jornada

O objetivo deste exemplo é impulsionar um evento para [!DNL Journey Optimizer] sempre que um pedido de cliente é atualizado. Em seguida, uma notificação por push é enviada ao cliente com informações sobre o pedido e uma oferta personalizada.

Para esse caso de uso, os seguintes pré-requisitos são necessários:

* crie e crie uma mensagem de notificação por push, sem publicá-la. Consulte esta [seção](../messages/get-started-content.md).
* configure um evento de pedido incluindo o número do pedido, o status e o nome do item. Consulte esta [seção](../event/about-events.md).
* criar uma decisão, consulte esta [seção](../offers/offer-activities/create-offer-activities.md).

## Etapa 1 - Adicionar personalização ao perfil {#add-perso}

1. Clique no botão **[!UICONTROL Message]** e selecione a mensagem.

   ![](assets/perso-uc.png)

1. Clique no botão **Título** campo.

   ![](assets/perso-uc2.png)

1. Digite o assunto e adicione a personalização do perfil. Use a barra de pesquisa para localizar o campo de nome do perfil. No texto do assunto, coloque o cursor onde deseja inserir o campo de personalização e clique no link **+** ícone . Clique em **Salvar**.

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >Deixe a mensagem em rascunho. Não o publique ainda.

## Etapa 2 - Criar a jornada {#create-journey}

1. Clique no botão **[!UICONTROL Journeys]** e crie uma nova jornada.

   ![](assets/perso-uc4.png)

1. Adicione seu evento de entrada, um **Mensagem** e um **End** atividade .

   ![](assets/perso-uc5.png)

1. No **Mensagem** selecione a mensagem criada anteriormente. Clique em **Ok**.

   ![](assets/perso-uc6.png)

   Uma mensagem é exibida para informá-lo que os dados do evento de entrada e as propriedades da jornada foram passados para a mensagem.

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >A mensagem é exibida com um ícone de aviso. Isso ocorre porque a mensagem ainda não foi publicada.

## Etapa 3 - Adicionar personalização aos dados contextuais {#add-perso-contextual-data}

1. No **Mensagem** , clique no botão **Abrir a mensagem** ícone . A mensagem é aberta em uma nova guia.

   ![](assets/perso-uc8.png)

1. Clique no botão **Título** campo.

   ![](assets/perso-uc9.png)

1. Selecione o **Atributos contextuais** menu. Atributos contextuais só estarão disponíveis se uma jornada tiver passado dados contextuais para a mensagem. Clique em **Journey Orchestration**. As seguintes informações contextuais são exibidas:

   * **Eventos**: esta categoria agrupa todos os campos do(s) evento(s) colocado(s) antes da variável **Mensagem** na jornada.
   * **Propriedades da Jornada**: os campos técnicos relacionados à jornada de um determinado perfil, por exemplo, a ID da jornada ou os erros específicos encontrados. Saiba mais em [Documentação do Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Expanda o **Eventos** e procure o campo número do pedido relacionado ao seu evento. Também é possível usar a caixa de pesquisa. Clique no botão **+** ícone para inserir o campo de personalização no texto do assunto. Clique em **Salvar**.

   ![](assets/perso-uc11.png)

1. Em seguida, clique no botão **Corpo** campo.

   ![](assets/perso-uc12.png)

1. Digite a mensagem e insira, no **[!UICONTROL Contextual attributes]** , o nome do item da ordem e o andamento da ordem.

   ![](assets/perso-uc13.png)

1. No menu esquerdo, selecione **Decisões de oferta** para inserir uma variável de offer decisioning. Selecione a disposição e clique no botão **+** ícone ao lado da decisão de adicioná-lo ao corpo.

   ![](assets/perso-uc14.png)

1. Clique em validar para garantir que não haja erros e clique em **Salvar**.

   ![](assets/perso-uc15.png)

1. Agora, publique a mensagem.

   ![](assets/perso-uc16.png)

## Etapa 4 - Testar e publicar a jornada {#test-publish}

1. Abra a jornada novamente. Se a jornada já estiver aberta, atualize a página. Agora que a mensagem foi publicada, você pode ver que não há erro na jornada. Clique no botão **Teste** e, em seguida, clique em **Acionar um evento**.

   ![](assets/perso-uc17.png)

1. Insira os diferentes valores a serem aprovados no teste. O modo de teste só funciona com perfis de teste. O identificador de perfil precisa corresponder a um perfil de teste. Clique em **Enviar**.

   ![](assets/perso-uc18.png)

   A notificação por push é enviada e exibida no celular do perfil de teste.

   ![](assets/perso-uc19.png)

1. Verifique se não há erro e publique a jornada.
