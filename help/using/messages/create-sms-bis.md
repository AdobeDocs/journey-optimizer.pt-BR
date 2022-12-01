---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma mensagem de SMS.
description: Saiba como criar uma mensagem SMS no Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 7%

---

# Criar uma mensagem de SMS. {#create-sms-bis}

>[!NOTE]
>
>De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. Para fazer isso, os recipients do SMS podem responder com palavras-chave de aceitação e recusa.

## Criar uma mensagem SMS em uma jornada ou campanha

Para começar a personalizar a mensagem SMS, siga estas etapas:

>[!BEGINTABS]

>[!TAB Adicionar uma mensagem SMS a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de SMS da seção Ações da paleta.

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície da mensagem a ser usada.

   Para obter mais informações sobre como configurar uma jornada, consulte.

Agora você pode começar a projetar o conteúdo de sua mensagem SMS do **[!UICONTROL Editar conteúdo]** botão.

>[!TAB Adicionar uma mensagem SMS a uma campanha]

1. Crie uma nova campanha agendada ou acionada por API, selecione **[!UICONTROL SMS]** como sua ação e escolha o **[!UICONTROL Superfície do aplicativo]** para usar.

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

1. No **[!UICONTROL Rastreamento de ações]** , especifique se deseja rastrear cliques em links na mensagem SMS.

1. Clique no botão **[!UICONTROL Seleção do público-alvo]** para definir o público-alvo a ser direcionado a partir da lista de segmentos disponíveis do Adobe Experience Platform.

1. No **[!UICONTROL Namespace de identidade]** , escolha o namespace a ser usado para identificar os indivíduos do segmento selecionado.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha no .

1. No **[!UICONTROL Acionadores de ação]** escolha o **[!UICONTROL Frequência]** da sua mensagem SMS:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mês

Agora você pode começar a projetar o conteúdo de sua mensagem SMS do **[!UICONTROL Editar conteúdo]** botão.

>[!ENDTABS]

## Definir o conteúdo do SMS

1. Na tela de configuração da jornada ou campanha, clique no botão **[!UICONTROL Editar conteúdo]** para configurar o conteúdo do SMS.

1. Clique no botão **[!UICONTROL Mensagem]** para abrir o editor de expressão.

1. Use o editor de expressão para definir o conteúdo e adicionar conteúdo dinâmico. Você pode usar qualquer atributo, como o nome do perfil ou a cidade.

1. Clique em **[!UICONTROL Salvar]** e verifique a mensagem na visualização.

1. Quando a mensagem SMS estiver pronta, conclua a configuração de seu para enviá-la.

## Validar o SMS

>[!NOTE]
>
> Para melhorar o deliverability, você sempre deve usar os números de telefone nos formatos compatíveis com o provedor. Por exemplo, Twilio e Sinch suportam apenas números de telefone no formato E.164.

Após definir o conteúdo da mensagem, é possível usar perfis de teste para pré-visualizá-lo e testá-lo. Se você inseriu, é possível verificar como esse conteúdo é exibido na mensagem, usando dados de perfil de teste.

Para visualizar como sua mensagem SMS é exibida em dispositivos móveis, clique no botão **[!UICONTROL Simular conteúdo]** guia . Saiba mais sobre a simulação de conteúdo no.

Você também deve verificar os alertas na seção superior do editor.  Alguns deles são avisos simples, mas outros podem impedir que você use a mensagem. Saiba mais em.
