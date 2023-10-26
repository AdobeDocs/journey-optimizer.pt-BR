---
solution: Journey Optimizer
product: journey optimizer
title: Criar um MMS
description: Saiba como criar um MMS no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 9%

---

# Criar uma mensagem MMS {#create-mms}

## Pré-requisitos{#sms-prerequisites}

Antes de criar sua mensagem SMS, primeiro é necessário configurar o fornecedor de SMS com o Journey Optimizer. Siga estas etapas:

* Antes de enviar SMS, você deve integrar as configurações do provedor com o Journey Optimizer.

+++ Saiba como criar uma nova credencial de API do MMS do Sinch.

   1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione o **[!UICONTROL Credenciais da API]** menu. Clique em **[!UICONTROL Criar novas credenciais de API]** botão.

      ![](assets/sms_6.png)

   1. Configurar suas credenciais da API de SMS:

   * Para **[!DNL Sinch MMS]**:

      * **[!UICONTROL Nome]**: escolha um nome para a credencial da API.

      * **[!UICONTROL ID do projeto]**, **[!UICONTROL ID do aplicativo]** e **[!UICONTROL Token de API]**: no menu da API de conversa, você pode encontrar suas credenciais no menu Aplicativo.  [Saiba mais](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html)

     ![](assets/mms_provider.png)

   1. Clique em **[!UICONTROL Enviar]** quando você concluiu a configuração das credenciais da API.

  Depois de criar e configurar a credencial de API, agora é necessário criar uma superfície de canal (ou seja, predefinição de mensagem) para mensagens SMS.

+++

* Depois de concluído, você precisará criar uma superfície de SMS. Essas etapas devem ser executadas por um administrador do sistema do Adobe Journey Optimizer.

+++ Saiba como criar sua superfície de canal.

   1. No painel esquerdo, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** e selecione **[!UICONTROL Marcas]** > **[!UICONTROL Superfícies de canal]**. Clique em **[!UICONTROL Criar superfície de canal]** botão.

      ![](assets/preset-create.png)

   1. Insira um nome e uma descrição (opcional) para a superfície e selecione o canal SMS.

      ![](assets/sms-create-surface.png)

      >[!NOTE]
      >
      > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

   1. Defina o **Configurações de SMS**.

      ![](assets/sms-surface-settings.png)

      Comece selecionando o **[!UICONTROL Tipo de SMS]** que serão enviados com a superfície: **[!UICONTROL Transacional]** ou **[!UICONTROL Marketing]**.

      * Escolher **Marketing** para SMS promocional: essas mensagens exigem o consentimento do usuário.
      * Escolher **Transacional** para mensagens não comerciais, como confirmação de pedidos, notificações de redefinição de senha ou informações de entrega, por exemplo.

      Ao criar uma mensagem SMS, você deve escolher uma superfície de canal válida que corresponda à categoria selecionada para a mensagem.

      >[!CAUTION]
      >
      >**Transacional** Mensagens SMS podem ser enviadas a perfis que cancelaram a assinatura de comunicações de marketing. Essas mensagens só podem ser enviadas em contextos específicos.

   1. Selecione o **[!UICONTROL Configuração de SMS]** para associar à superfície.

      Para obter mais informações sobre como configurar o seu ambiente para enviar mensagens SMS, consulte [nesta seção](#create-api).

   1. Insira o **[!UICONTROL Número do remetente]** &#x200B;que você deseja usar para suas comunicações.

   1. Selecione o **[!UICONTROL Campo de execução do SMS]** para selecionar o **[!UICONTROL Atributo de perfil]** associados aos números de telefone dos perfis.

   1. Se quiser usar a função de redução de URL em suas mensagens SMS, selecione um item na lista suspensa **[!UICONTROL Subdomínio]** lista.

      >[!NOTE]
      >
      >Para selecionar um subdomínio, verifique se você configurou anteriormente pelo menos um subdomínio SMS. [Saiba como](sms-subdomains.md)

   1. Insira o **[!UICONTROL Número de recusa]** que você deseja usar para esta superfície. Quando os perfis optam por não participar desse número, você ainda pode enviar mensagens de outros números com os quais possa estar usando para enviar mensagens SMS [!DNL Journey Optimizer].

      >[!NOTE]
      >
      >Entrada [!DNL Journey Optimizer], o cancelamento de SMS não é mais gerenciado no nível do canal. Agora é específico de um número.

   1. Após configurar todos os parâmetros, clique em **[!UICONTROL Enviar]** para confirmar. Você também pode salvar a superfície de canal como rascunho e retomar sua configuração posteriormente.

      ![](assets/sms-submit-surface.png)

   1. Depois que a superfície de canal é criada, ela é exibida na lista com o **[!UICONTROL Processando]** status.

      >[!NOTE]
      >
      >Se as verificações não forem bem-sucedidas, saiba mais sobre os possíveis motivos de falha no [nesta seção](#monitor-channel-surfaces).

   1. Depois que as verificações forem bem-sucedidas, a superfície de canal obterá a variável **[!UICONTROL Ativo]** status. Ele está pronto para ser usado para enviar mensagens.

      ![](assets/preset-active.png)


## Criar uma mensagem de SMS. {#create-sms-journey-campaign}

Navegue pelas guias abaixo para saber como adicionar uma mensagem SMS em uma campanha ou jornada.

>[!BEGINTABS]

>[!TAB Adicionar uma mensagem SMS a uma Jornada]

1. Abra a jornada e arraste e solte uma atividade de SMS da **Ações** seção da paleta.

   ![](assets/sms_create_1.png)

1. Forneça informações básicas sobre a mensagem (rótulo, descrição, categoria) e escolha a superfície de mensagem a ser usada.

   ![](assets/sms_create_2.png)

   Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md)

   A variável **[!UICONTROL Superficial]** é pré-preenchido, por padrão, com a última superfície usada para esse canal pelo usuário.

Agora é possível começar a projetar o conteúdo da sua mensagem SMS usando o **[!UICONTROL Editar conteúdo]** botão. [Definir o conteúdo do SMS](#sms-content)

>[!TAB Adicionar uma mensagem SMS a uma campanha]

1. Crie uma nova campanha programada ou acionada por API, selecione **[!UICONTROL SMS]** como sua ação e escolha a opção **[!UICONTROL Superfície do aplicativo]** para usar. [Saiba mais sobre a configuração de SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Clique em **[!UICONTROL Criar]**.

1. No **[!UICONTROL Propriedades]** edite o da sua campanha **[!UICONTROL Título]** e **[!UICONTROL Descrição]**.

   ![](assets/sms_create_4.png)

1. Clique em **[!UICONTROL Selecionar público]** botão para definir o público-alvo a ser direcionado na lista de públicos-alvo disponíveis do Adobe Experience Platform. [Saiba mais](../audience/about-audiences.md).

1. No **[!UICONTROL Namespace de identidade]** escolha o namespace a ser usado para identificar os indivíduos do público-alvo selecionado. [Saiba mais](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Clique em **[!UICONTROL Criar experimento]** para começar a configurar seu experimento de conteúdo e criar tratamentos para medir seu desempenho e identificar a melhor opção para seu público-alvo. [Saiba mais](../campaigns/content-experiment.md)

1. No **[!UICONTROL Rastreamento de ações]** especifique se deseja rastrear cliques nos links da mensagem SMS.

1. As campanhas são projetadas para serem executadas em uma data específica ou em uma frequência recorrente. Saiba como configurar o **[!UICONTROL Agendar]** da sua campanha no [nesta seção](../campaigns/create-campaign.md#schedule).

1. No **[!UICONTROL Acionadores de ação]** selecione o **[!UICONTROL Frequência]** de sua mensagem SMS:

   * Uma vez
   * Diariamente
   * Semanalmente
   * Mês

Agora é possível começar a projetar o conteúdo da sua mensagem SMS usando o **[!UICONTROL Editar conteúdo]** botão. [Projetar o conteúdo de SMS](#sms-content)

>[!ENDTABS]

## Definir o conteúdo MMS{#mms-content}

1. Na tela de configuração do jornada ou da campanha, clique no link **[!UICONTROL Editar conteúdo]** botão para configurar o conteúdo do SMS.

1. Clique em **[!UICONTROL Mensagem]** para abrir o editor de expressão.

   ![](assets/sms-content.png)

1. Use o editor de expressão para definir o conteúdo e adicionar conteúdo dinâmico. Você pode usar qualquer atributo, como o nome do perfil ou a cidade. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md) no Editor de expressão.

1. Ative a opção MMS para adicionar mídia ao conteúdo de SMS.

   >[!NOTE]
   >
   > A opção MMS só está disponível com Sinch. É necessário criar uma credencial de API específica para criar o MMS. [Saiba mais](sms-configuration.md#create-new-api)

   ![](assets/sms_create_6.png)

1. Adicionar um **[!UICONTROL Título]** à sua mídia.

1. Insira o URL da mídia na caixa **[!UICONTROL Mídia]** campo.

   ![](assets/sms_create_7.png)

1. Clique em **[!UICONTROL Salvar]** e verifique sua mensagem na visualização. Você pode usar **[!UICONTROL Simular conteúdo]** para visualizar seus URLs encurtados ou conteúdo personalizado.

Agora você pode testar e enviar sua mensagem SMS para o público-alvo. [Saiba mais](send-sms.md)
Depois de enviado, você pode medir o impacto do SMS nos relatórios do Campaign ou do Jornada. Para obter mais informações sobre relatórios, consulte [esta seção](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. Para fazer isso, os destinatários de SMS podem responder com palavras-chave de aceitação e recusa. [Saiba como gerenciar a recusa](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Tópicos relacionados**

* [Pré-visualizar, testar e enviar sua mensagem SMS](send-sms.md)
* [Configurar canal de SMS](sms-configuration.md)
* [Relatório de SMS](../reports/journey-global-report.md#sms-global)