---
solution: Journey Optimizer
product: journey optimizer
title: Criar uma página de destino
description: Saiba como configurar e publicar uma landing page no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: aterrissagem, página de aterrissagem, criação, publicação
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 0db7f514a2604ad09fbd9863a51d3c86d69eac41
workflow-type: tm+mt
source-wordcount: '1518'
ht-degree: 23%

---

# Criar e publicar landing pages {#create-lp}

Para direcionar seus clientes para uma página da Web definida que você deseja exibir quando clicarem em um link específico, crie uma página de aterrissagem no [!DNL Journey Optimizer], configure a página principal e quaisquer subpáginas, teste-a e publique-a.

As principais etapas para criar landing pages são as seguintes:

![](assets/lp-creation-process.png)

## Criar uma página de destino {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="Definir e configurar a página de destino"
>abstract="Para criar uma página de destino, você precisa selecionar uma predefinição, configurar a página principal e as subpáginas e, por fim, testar a página antes de publicá-la."

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="Atribuir rótulos à página de destino"
>abstract="Para proteger ativos digitais confidenciais, você pode definir autorizações para gerenciar o acesso aos dados da página de destino usando rótulos."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html?lang=pt-BR" text="Controle de acesso no nível do objeto"


Para criar uma landing page, selecione uma predefinição, configure a página principal e as subpáginas e teste a página antes de publicá-la. Essas etapas são detalhadas abaixo:


1. Navegue até **[!UICONTROL Gestão de Conteúdo]** > **[!UICONTROL Landing pages]** no menu esquerdo.

1. Na lista de páginas de aterrissagem, clique em **[!UICONTROL Criar página de aterrissagem]**.

   ![](assets/lp_create-lp.png)

1. Adicione um título. Você pode adicionar uma descrição, se necessário.

   ![](assets/lp_create-lp-details.png)

1. Para atribuir rótulos de uso de dados personalizados ou principais à página de aterrissagem, selecione **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md)

1. Selecione ou crie tags do Adobe Experience Platform a partir do campo **[!UICONTROL Tags]** para categorizar sua página de aterrissagem para pesquisa aprimorada. [Saiba mais](../start/search-filter-categorize.md#tags)

1. Selecione uma predefinição. Saiba como criar predefinições de página de aterrissagem em [esta seção](../landing-pages/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. Clique em **[!UICONTROL Criar]**.

1. A página principal e suas propriedades são exibidas. Saiba como definir as configurações de página primária [aqui](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Clique no ícone + para adicionar uma subpágina. Saiba como definir as configurações de subpágina [aqui](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Depois de configurar e criar a [página principal](#configure-primary-page) e as [subpáginas](#configure-subpages), se houver, você pode [testar](#test-landing-page) e [publicar](#publish-landing-page) sua página de aterrissagem.

>[!CAUTION]
>
>Você não pode acessar sua landing page simplesmente copiando e colando o URL definido em um navegador da Web, mesmo que publicado. Em vez disso, você pode testá-lo usando a função de visualização, como descrito em [esta seção](#test-landing-page).

## Configurar a página principal {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="Definir as configurações da página principal"
>abstract="A página principal é exibida imediatamente depois que os usuários clicam no link da landing page que consta em um email ou site."
<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="Design the landing page content"-->

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="Definir o URL da página de destino"
>abstract="Nesta seção, defina um URL de página de destino exclusivo. A primeira parte do URL requer a configuração prévia de um subdomínio de página de destino como parte da predefinição selecionada."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-subdomains" text="Configurar subdomínios de página de destino"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets#lp-create-preset" text="Criar predefinições de página de destino"

A página principal é a página imediatamente exibida aos usuários depois que eles clicam no link para a página de aterrissagem, como a partir de um email ou site.

Para definir as configurações de página principal, siga as etapas abaixo.

1. Você pode alterar o nome da página, que é **[!UICONTROL Página principal]** por padrão.

1. Edite o conteúdo da página usando o designer de conteúdo. Saiba como definir o conteúdo da página de aterrissagem [aqui](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Defina o URL da sua landing page. A primeira parte da URL exige que você tenha configurado previamente um subdomínio de página de aterrissagem como parte da [predefinição](../landing-pages/lp-presets.md#lp-create-preset) selecionada. [Saiba mais](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >O URL da landing page deve ser exclusivo.
   >
   >Você não pode acessar sua landing page simplesmente copiando esse URL em um navegador da Web, mesmo que publicado. Em vez disso, você pode testá-lo usando a função de visualização, como descrito em [esta seção](#test-landing-page).

   ![](assets/lp_access-url.png)

1. Se desejar que a página de aterrissagem pré-carregue os dados de formulário que já estão disponíveis, selecione os **[!UICONTROL Preencher campos de formulário previamente com informações de perfil]**.

   ![](assets/lp_prefill-form-fields.png)

   Quando essa opção estiver ativada, se um perfil já tiver aceitado/recusado ou já tiver sido adicionado a uma lista de assinaturas, suas opções serão refletidas na exibição da landing page.

   Por exemplo, se um perfil tiver optado por receber comunicações sobre eventos futuros, a caixa de seleção correspondente já estará marcada na próxima vez que a landing page for exibida para esse perfil.

   ![](assets/lp_prefill-form-ex.png)

1. É possível definir uma data de expiração para a página. Nesse caso, você deve selecionar uma ação ao expirar a página:

   * **[!UICONTROL URL de redirecionamento]**: digite a URL da página para a qual os usuários serão redirecionados quando a página expirar.
   * **[!UICONTROL Página personalizada]**: [Configure uma subpágina](#configure-subpages) e selecione-a na lista suspensa exibida.
   * **[!UICONTROL Erro do navegador]**: digite o texto do erro que será exibido em vez da página.

   ![](assets/lp_expiry-date.png)

<!--1. In the **[!UICONTROL Additional data]** section, define one or more keys and their corresponding parameter values. You will be able to leverage these keys in the content of your primary page and subpages using the [personalization editor](../personalization/personalization-build-expressions.md). Learn more in [this section](lp-content.md#use-form-component#use-additional-data).

    ![](assets/lp_create-lp-additional-data.png)-->

1. Se você selecionou uma ou mais listas de assinaturas ao [criar a página primária](design-lp.md), elas serão exibidas na seção **[!UICONTROL Lista de assinaturas]**.

   ![](assets/lp_subscription-list.png)

1. Na página de aterrissagem, você pode [criar diretamente uma jornada](../building-journeys/journey-gs.md#jo-build) que enviará uma mensagem de confirmação aos usuários quando eles enviarem o formulário. Saiba como criar uma jornada no final deste [caso de uso](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Clique em **[!UICONTROL Criar jornada]** para ser redirecionado para a lista **[!UICONTROL Gerenciamento de Jornadas]** > **[!UICONTROL Jornadas]**.

## Configurar subpáginas {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="Definir as configurações de subpágina"
>abstract="Você pode adicionar até 2 subpáginas. Por exemplo, você pode criar uma página de “agradecimento” que será exibida depois que as pessoas enviarem o formulário e você pode definir uma página de erro que será chamada se ocorrer um problema com a página de destino."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/content-management/landing-pages/landing-pages-design/design-lp" text="Criar o conteúdo da página de destino"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="Definir o URL da página de destino"
>abstract="Nesta seção, defina um URL de página de destino exclusivo. A primeira parte do URL requer a configuração prévia de um subdomínio de página de destino como parte da predefinição selecionada."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-subdomains.html?lang=pt-BR" text="Configurar subdomínios de página de destino"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets.html?lang=pt-BR#lp-create-preset" text="Criar predefinições de página de destino"

Você pode adicionar até 2 subpáginas. Por exemplo, você pode criar uma página de “agradecimento” que será exibida depois que as pessoas enviarem o formulário e você pode definir uma página de erro que será chamada se ocorrer um problema com a página de destino.

Para definir as configurações de subpágina, siga as etapas abaixo.

1. Você pode alterar o nome da página, que é **[!UICONTROL Subpágina 1]** por padrão.

1. Edite o conteúdo da página usando o designer de conteúdo. Saiba como definir o conteúdo da página de aterrissagem [aqui](design-lp.md).

   >[!NOTE]
   >
   >É possível inserir um link para a página principal de qualquer subpágina da mesma página de destino. Por exemplo, para redirecionar os usuários que cometeram um erro e desejam assinar novamente, é possível adicionar um link da subpágina de confirmação para a página principal da assinatura. Saiba como inserir links em [esta seção](../email/message-tracking.md#insert-links).

1. Defina o URL da sua landing page. A primeira parte do URL exige a configuração prévia de um subdomínio de página de destino. [Saiba mais](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >O URL da landing page deve ser exclusivo.
   >
   >Você não pode acessar sua subpágina simplesmente copiando e colando esse URL em um navegador da Web, mesmo se publicado. Em vez disso, você pode testá-lo usando a função de visualização, como descrito em [esta seção](#test-landing-page).

![](assets/lp_subpage-settings.png)

## Testar a landing page {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ac_preview_lp_profiles"
>title="Visualizar e testar a página de destino"
>abstract="Depois de definir as configurações e o conteúdo da página de destino, você pode usar perfis de teste para visualizar."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles.html?lang=pt-BR" text="Selecionar perfis de teste"

Depois que as configurações e o conteúdo da landing page forem definidos, você poderá usar perfis de teste para pré-visualizá-la. Se você inseriu [conteúdo personalizado](../personalization/personalize.md), será possível verificar como esse conteúdo é exibido na página de aterrissagem, usando os dados do perfil de teste.

>[!CAUTION]
>
>Para testar páginas de aterrissagem, você deve ter a permissão **[!UICONTROL Publicar Mensagens]**.
>
>Você deve ter perfis de teste disponíveis para poder visualizar suas mensagens e enviar provas. Saiba como [criar perfis de teste](../audience/creating-test-profiles.md).

1. Na interface da página de aterrissagem, clique no botão **[!UICONTROL Simular conteúdo]** para acessar a seleção de perfil de teste.

   ![](assets/lp_simulate-button.png)

   >[!NOTE]
   >
   >O botão **[!UICONTROL Simular conteúdo]** também pode ser acessado no designer de conteúdo.

1. Na tela **[!UICONTROL Simular]**, selecione um ou mais perfis de teste.

   ![](assets/lp_test-profiles.png)

   As etapas para selecionar perfis de teste são as mesmas que ao testar uma mensagem. Eles estão detalhados na seção [Gestão de Conteúdo](../content-management/test-profiles.md).

1. Selecione **[!UICONTROL Abrir visualização]** para testar a página de aterrissagem.

   ![](assets/lp_open-preview.png)

1. A visualização da landing page é aberta em uma nova guia. Os elementos personalizados são substituídos pelos dados do perfil de teste selecionado.

   <!--![](assets/lp_preview.png)-->

1. Selecione outros perfis de teste para visualizar a renderização de cada variante da página de aterrissagem.

## Verificar alertas {#check-alerts}

Ao criar uma landing page, os alertas avisam quando você deve realizar ações importantes antes de publicar.

Os alertas são exibidos na parte superior direita da tela, conforme mostrado abaixo:

![](assets/lp_alerts.png)

>[!NOTE]
>
>Se você não vir esse botão, nenhum alerta foi detectado.

Dois tipos de alertas podem ocorrer:

* **Os avisos** referem-se às recomendações e práticas recomendadas. <!--For example, a message will display if -->

* **Erros** impedem a publicação da página de aterrissagem, desde que não sejam resolvidos. Por exemplo, você receberá um aviso se o URL da página principal estiver ausente.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> Você deve resolver todos os alertas de **erro** antes da publicação.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

-->

## Publicar a página de destino {#publish-landing-page}

>[!CAUTION]
>
>Para publicar páginas de aterrissagem, os usuários devem ter a permissão **[!UICONTROL Publicar Mensagens]**.


Quando a landing page estiver pronta, você poderá publicá-la para disponibilizá-la para uso em uma mensagem.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Antes de publicar, verifique e resolva os alertas. [Saiba mais](#check-alerts)

Assim que a página de aterrissagem for publicada, ela será adicionada à lista de páginas de aterrissagem com o status **[!UICONTROL Publicado]**.

Agora ele está ativo e pronto para ser usado em uma mensagem [!DNL Journey Optimizer] que será enviada por meio de uma [jornada](../building-journeys/journey.md).

>[!NOTE]
>
>Você não pode acessar sua página de aterrissagem simplesmente copiando e colando em um navegador a URL definida ao [criar a página](#create-landing-page), mesmo se publicada. Em vez disso, você pode testá-lo usando a função de visualização, como descrito em [esta seção](#test-landing-page).

Você pode monitorar os impactos da landing page por meio de relatórios específicos. [Saiba mais](../reports/lp-report-live.md)
