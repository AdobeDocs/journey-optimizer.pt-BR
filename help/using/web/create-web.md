---
title: Criação de experiências da web
description: Saiba como criar uma página da Web e editar seu conteúdo no Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '1543'
ht-degree: 18%

---

# Criação de experiências da web {#create-web}

O [!DNL Journey Optimizer] permite personalizar a experiência da Web fornecida aos clientes por meio de jornadas ou campanhas de entrada.

## Definir uma experiência da web por meio de uma jornada ou campanha {#create-web-experience}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definir uma configuração da web"
>abstract="Uma configuração da web pode corresponder a um URL de página única ou várias páginas, permitindo que você faça modificações no conteúdo em uma ou várias páginas da web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Criar uma regra de correspondência de páginas"
>abstract="Uma regra de correspondência de páginas permite direcionar vários URLs que correspondem à mesma regra, por exemplo, se você deseja aplicar as alterações em um banner hero no site inteiro ou adicionar uma imagem superior que é exibida em todas as páginas de produtos de um site."

Para começar a criar sua experiência da Web por meio de uma campanha ou jornada, siga as etapas abaixo.

>[!NOTE]
>
>Se esta for a primeira vez que estiver criando uma experiência online, certifique-se de seguir os pré-requisitos descritos [nesta seção](web-prerequisites.md).

>[!BEGINTABS]

>[!TAB Adicionar uma experiência da Web a uma jornada]

Para adicionar uma atividade **Web** a uma jornada, siga estas etapas:

1. [Criar uma jornada](../building-journeys/journey-gs.md).

1. Inicie sua jornada com uma atividade [Evento](../building-journeys/general-events.md) ou [Ler público](../building-journeys/read-audience.md).

1. Arraste e solte uma atividade **[!UICONTROL Web]** da seção **[!UICONTROL Actions]** da paleta.

   ![](assets/web-activity-journey.png)

   >[!NOTE]
   >
   >Como **Web** é uma atividade de experiência de entrada, ela vem com uma atividade **Wait** de 3 dias. [Saiba mais](../building-journeys/wait-activity.md#auto-wait-node)

1. Insira um **[!UICONTROL Rótulo]** e uma **[!UICONTROL Descrição]** para a mensagem.

1. Selecione ou crie a [configuração da Web](web-configuration.md) a ser usada.

   ![](assets/web-activity-configuration.png)

1. Selecione o botão **[!UICONTROL Editar conteúdo]** e edite o conteúdo conforme desejado. [Saiba mais](#edit-web-content)

1. Se necessário, conclua o fluxo de jornada arrastando e soltando ações ou eventos adicionais. [Saiba mais](../building-journeys/about-journey-activities.md)

1. Quando a experiência da Web estiver pronta, finalize a configuração e publique sua jornada para ativá-la. [Saiba mais](../building-journeys/publishing-the-journey.md)

Para obter mais informações sobre como configurar uma jornada, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Criação de uma campanha da web]

Para começar a criar sua experiência da Web por meio de uma campanha, siga as etapas abaixo.

1. Crie uma campanha. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione o tipo de campanha que deseja executar

   * **Agendado - Marketing**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas são destinadas ao envio de mensagens de marketing. Eles são configurados e executados na interface do usuário do.

   * **Acionado por API - Marketing/Transacional**: execute a campanha usando uma chamada de API. As campanhas acionadas por API destinam-se ao envio de mensagens de marketing ou transacionais, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc. [Saiba como acionar uma campanha usando APIs](../campaigns/api-triggered-campaigns.md)

1. Conclua as etapas para criar uma campanha da Web, como as propriedades da campanha, [público](../audience/about-audiences.md) e [agendamento](../campaigns/create-campaign.md#schedule).

1. Selecione a ação **[!UICONTROL Web]**.

1. Selecione ou crie a configuração da Web. [Saiba mais sobre a configuração da Web](web-configuration.md)

   ![](assets/web-campaign-steps.png)

1. Clique no botão **[!UICONTROL Editar conteúdo]** para editar seu conteúdo conforme desejado. [Saiba mais](#edit-web-content)

   <!--![](assets/web-campaign-edit-content.png)-->

Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

➡️ [Saiba como criar uma campanha da Web neste vídeo](#video)

>[!ENDTABS]

## Editar conteúdo da Web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Confirmar o URL para editar"
>abstract="Confirme o URL da página da web específica a ser usada para editar o conteúdo que será aplicado na configuração da web definida acima. A página da Web deve ser implementada usando o SDK da Web da Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Inserir o URL para editar"
>abstract="Insira o URL de uma página da Web específica a ser usada para editar o conteúdo que será aplicado a todas as páginas que correspondem à regra. A página da Web deve ser implementada usando o SDK da Web da Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR" text="Saiba mais"

Depois de [adicionar uma ação da Web](#create-web-experience) a uma jornada ou campanha, você poderá editar o conteúdo do site usando:

* o [web designer](web-visual-editor.md), para criar sua experiência usando um editor visual;
* ou o [editor não visual](web-non-visual-editor.md).

Para começar a criar sua experiência na Web, siga as etapas abaixo.

1. Na guia **[!UICONTROL Ação]** da campanha ou da atividade **[!UICONTROL Web]** da jornada, selecione **[!UICONTROL Editar conteúdo]**.

   ![](assets/web-campaign-edit-content.png)

1. A tela de edição é exibida. É possível:

   * Clique no botão **[!UICONTROL Editar página da Web]** para começar a criar seu conteúdo usando o designer da Web para obter uma experiência visual. [Saiba mais](web-visual-editor.md)

     ![](assets/web-campaign-edit-web-page.png)

   * Desmarque a opção **[!UICONTROL Editor visual]** para usar o modo de edição não visual e clique em **[!UICONTROL Adicionar uma modificação]** para começar a editar seu conteúdo da Web sem carregar o editor visual. [Saiba mais](web-non-visual-editor.md)

     ![](assets/web-campaign-add-modification.png)

## Testar a experiência da web {#test-web-experience}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Visualizar a experiência da Web"
>abstract="Acesse uma simulação de como sua experiência da Web será."

Depois de [criar sua experiência da Web](web-visual-editor.md) usando o designer da Web, você poderá usar perfis de teste para visualizar suas páginas da Web modificadas. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** da tela de conteúdo de edição de jornada ou campanha e, em seguida, adicione um perfil de teste para verificar sua página da Web usando os dados do perfil de teste.

![](assets/web-designer-preview.png)

Você também pode abri-lo no navegador padrão ou copiar o URL de teste para colá-lo em qualquer navegador. Isso permite compartilhar o link com a equipe e as partes interessadas, que poderão visualizar a nova experiência da Web em qualquer navegador antes que a campanha entre em vigor.

>[!NOTE]
>
>Ao copiar a URL de teste, o conteúdo exibido é aquele personalizado para o perfil de teste usado quando a simulação de conteúdo foi gerada em [!DNL Journey Optimizer].

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

## Redirecionar para URL {#web-redirect-to-url}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_redirect"
>title="Redirecionar para outro URL"
>abstract="Insira um URL existente para o qual você deseja redirecionar visitantes da página."

Ao criar uma experiência da Web, você pode redirecionar os visitantes para outro URL existente, em vez de criar uma nova variação no web designer.

Usando essa capacidade, você pode executar um [Experimento de conteúdo](../content-management/content-experiment.md) comparando duas experiências diferentes, em vez de apenas alterar alguns elementos em uma página.

Por exemplo, crie uma campanha da Web com dois tratamentos:

* Em **Tratamento A**, crie uma experiência da Web usando o designer da Web para metade da população direcionada.

* Em **Treatment B**, selecione a opção **[!UICONTROL Redirecionar para URL]** para a outra metade da população direcionada. Insira a URL de uma página com um design alternativo que você criou fora do [!DNL Journey Optimizer].

  ![](assets/web-campaign-redirect-to-url.png)

  >[!NOTE]
  >
  >A visualização do site não é mais exibida e o botão de alternância **[!UICONTROL Editor visual]** está desabilitado.

Assim que a campanha da Web for ativada, você poderá acompanhar o desempenho da experiência da Web criada no [!DNL Journey Optimizer] para os visitantes da sua página contra aqueles que foram redirecionados para a página de aterrissagem externa. Saiba como usar o [relatório de campanha de experimentação](../reports/campaign-global-report-cja-experimentation.md)

## Disponibilize sua experiência online {#web-experience-live}

>[!IMPORTANT]
>
> Se a campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para ativar as experiências da Web. [Saiba mais](../test-approve/gs-approval.md)

Depois de definir sua experiência online e editar o conteúdo conforme desejado, você pode ativar a jornada ou campanha para tornar as alterações visíveis para o público.

Você também pode visualizar seu conteúdo de experiência online antes de ativá-lo. [Saiba mais](#test-web-experience)

>[!NOTE]
>
>Se você ativar uma jornada/campanha da Web que afeta as mesmas páginas que outra jornada ou campanha que já está ativa, todas as alterações serão aplicadas às suas páginas da Web.
>
>Se várias jornadas ou campanhas atualizarem os mesmos elementos do site, a jornada/campanha de prioridade mais alta terá prioridade.

### Publicar uma jornada da Web {#activate-web-journey}

Para ativar sua experiência online a partir de uma jornada, siga as etapas abaixo.

1. Verifique se a jornada é válida e se não há erros. [Saiba mais](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. Na jornada, selecione a opção **[!UICONTROL Publicar]**, localizada no menu suspenso no canto superior direito.

   ![](assets/web-journey-publish.png)

   >[!NOTE]
   >
   >Saiba mais sobre a publicação de jornadas em [esta seção](../building-journeys/publishing-the-journey.md).

Sua jornada da Web está no status **[!UICONTROL Live]** e agora é somente leitura. Cada destinatário da jornada pode ver as modificações adicionadas ao site.

>[!NOTE]
>
>Após clicar em **[!UICONTROL Publicar]**, pode levar até 15 minutos para que as alterações fiquem disponíveis online no seu site.

### Ativar uma campanha da Web {#activate-web-campaign}

Depois de definir as configurações da campanha da Web e editar o conteúdo conforme desejado, você pode revisar e ativar a campanha da Web. Siga as etapas abaixo.

1. Em sua campanha da Web, selecione **[!UICONTROL Revisar para ativar]**.

1. Verifique e edite, se necessário, o conteúdo, as propriedades, a configuração, o público-alvo e o agendamento.

1. Selecione **[!UICONTROL Ativar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Saiba mais sobre como ativar campanhas em [esta seção](../campaigns/review-activate-campaign.md).

Sua campanha da Web recebe o status de **[!UICONTROL Ativo]** e agora está visível para o público selecionado. Cada recipient da campanha pode ver as modificações adicionadas ao site.

>[!NOTE]
>
>Depois de clicar em **[!UICONTROL Ativar]**, pode levar até 15 minutos para que as alterações nas campanhas da Web fiquem disponíveis ao vivo no site.
>
>Se você definiu um agendamento para sua campanha da Web, ele tem o status **[!UICONTROL Agendado]** até que a data e a hora de início sejam atingidas.

Assim que a experiência estiver ativa, você poderá monitorar as jornadas e campanhas da Web. [Saiba mais](monitor-web-experiences.md)

## Parar uma jornada ou campanha da Web {#stop-web-experience}

Quando uma jornada ou campanha da Web está ativa, você pode interrompê-la para impedir que seu público veja as modificações. Siga as etapas abaixo.

1. Selecione uma jornada ou campanha ao vivo na respectiva lista.

1. Execute a ação relevante de acordo com seu caso:

   * No menu superior da campanha, selecione **[!UICONTROL Parar campanha]**.

     ![](assets/web-campaign-stop.png)

   * No menu superior de jornada, clique no botão **[!UICONTROL Mais]** e selecione **[!UICONTROL Parar]**.

     ![](assets/web-journey-stop.png)

1. As modificações adicionadas não estarão mais visíveis para o público-alvo definido.

>[!NOTE]
>
>Quando uma jornada da Web ou campanha é interrompida, não é possível editá-la ou ativá-la novamente. Você só pode duplicá-la e ativar a jornada/campanha duplicada.

## Vídeo tutorial{#video}

O vídeo abaixo mostra como criar uma campanha da Web, configurar suas propriedades, revisá-la e publicá-la.

>[!VIDEO](https://video.tv.adobe.com/v/3449986/?quality=12&learn=on&captions=por_br)