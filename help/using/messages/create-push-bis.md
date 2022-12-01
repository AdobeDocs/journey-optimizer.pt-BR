---
solution: Journey Optimizer
product: journey optimizer
title: Configurar uma notificação por push
description: Saiba como criar uma notificação por push no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 2%

---

# Criar uma notificação por push {#create-push-notification-bis}

## Criar a notificação por push em uma jornada ou campanha {#create}

Para criar uma notificação por push, siga as etapas abaixo:

>[!BEGINTABS]

>[!TAB Adicionar um push a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de Push da seção Ações da paleta.

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.

   Para obter mais informações sobre como configurar uma jornada, consulte

1. Na tela de configuração da jornada, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo de push.

1. Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo.

1. Quando o push estiver pronto, conclua a configuração do para enviá-lo.

   Para rastrear o comportamento dos recipients por meio de aberturas e/ou interações de push, verifique se as opções dedicadas na seção de rastreamento estão habilitadas na .

>[!TAB Adicionar um push a uma campanha]

1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL Notificação por push]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar.

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform.

1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha no .

1. No **[!UICONTROL Acionadores de ação]** escolha o **[!UICONTROL Frequência]** da sua notificação por push:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mensalmente

1. Na tela de configuração da campanha, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo de push.

1. Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo.

1. Quando o push estiver pronto, conclua a configuração do para enviá-lo.

   Para rastrear o comportamento dos recipients por meio de aberturas e/ou interações de push, verifique se as opções dedicadas na seção de rastreamento estão ativadas no ).

>[!ENDTABS]

## Modo de entrega rápida {#rapid-delivery}

O modo de entrega rápida, anteriormente conhecido como modo Burst no jornada, é um [!DNL Journey Optimizer] que permite o envio muito rápido de mensagens de push em grandes volumes por meio de campanhas.

A entrega rápida é usada quando o atraso na entrega de mensagens é essencial para os negócios, quando você deseja enviar um alerta por push urgente em telefones celulares, por exemplo, uma notícia de última hora para os usuários que instalaram seu aplicativo de canal de notícias.

Para obter mais informações sobre desempenho ao usar o modo Rapid delivery, consulte.

### Pré-requisitos {#prerequisites}

As mensagens de delivery rápidas vêm com os seguintes requisitos:

* A entrega rápida está disponível para **[!UICONTROL Programado]** somente campanhas e não está disponível para campanhas acionadas por API,
* Nenhuma personalização é permitida na mensagem de push,
* O público-alvo deve conter menos de 30 M perfis,
* Você pode executar até 5 campanhas simultaneamente usando o modo Rapid delivery .

### Ativar modo de entrega rápida

1. Criar uma campanha de notificação por push e ativar **[!UICONTROL Entrega rápida]** opção.

1. Configure o conteúdo da mensagem e selecione o público-alvo a ser direcionado.

   >[!IMPORTANT]
   >
   >Certifique-se de que o conteúdo da mensagem não inclua nenhuma personalização e que o público-alvo contenha menos de 30M perfis.

1. Revise e ative sua campanha como de costume. Observe que, no modo de teste, as mensagens não são enviadas por meio do modo Rapid delivery .