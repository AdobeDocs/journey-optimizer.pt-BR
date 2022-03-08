---
title: Criar uma página de aterrissagem
description: Saiba como configurar e publicar uma landing page no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 4%

---

# Criar e publicar landing pages {#create-lp}

>[!CAUTION]
>
>O uso de landing pages está disponível no momento somente para usuários selecionados. Se quiser aproveitar esse recurso, entre em contato com o executivo da sua conta Adobe.

## Acessar landing pages {#access-landing-pages}

Para acessar a lista de landing pages, selecione **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** no menu esquerdo.

![](assets/lp_access-list.png)

O **[!UICONTROL Landing Pages]** exibe todos os itens criados. Você pode filtrá-los com base em seu status ou data de modificação.

![](assets/lp_access-list-filter.png)

## Criar uma página de aterrissagem {#create-landing-page}

As etapas para criar uma landing page são as seguintes.

1. Na lista de landing page, clique em **[!UICONTROL Create landing page]**.

   ![](assets/lp_create-lp.png)

1. Adicione um título. Você pode adicionar uma descrição, se necessário.

   ![](assets/lp_create-lp-details.png)

1. Selecione uma predefinição.

   ![](assets/lp_create-lp-presets.png)

   >[!NOTE]
   >
   >Para definir predefinições de landing page, entre em contato com o representante da conta do Adobe ou com o [Equipe de suporte ao Atendimento ao cliente do Adobe](https://helpx.adobe.com/br/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

1. Clique em **[!UICONTROL Create]**.

1. A página primária e suas propriedades são exibidas. Saiba como definir as configurações da página primária [here](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Clique no ícone + para adicionar uma subpágina. Saiba como definir as configurações de subpágina [here](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Depois de configurar e projetar o [página primária](#configure-primary-page)e o [subpáginas](#configure-subpages) se houver, você poderá [teste](#test-landing-page) e [publicar](#publish-landing-page) sua landing page.

## Configurar a página primária {#configure-primary-page}

A página primária é a página que é imediatamente exibida aos usuários depois que eles clicam no link de sua página inicial, como de um email ou de um site.

Para definir as configurações da página primária, siga as etapas abaixo.

1. Você pode alterar o nome da página, que é **[!UICONTROL Primary page]** por padrão.

1. Edite o conteúdo da sua página usando o designer de conteúdo. Saiba como definir o conteúdo da página de aterrissagem [here](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Defina o URL da página de aterrissagem. A primeira parte do URL requer que a delegação de domínio seja executada. Ela é pré-preenchida e não pode ser editada por meio da interface do usuário do . Para configurá-lo, entre em contato com seu representante de conta do Adobe ou com o [Equipe de suporte ao Atendimento ao cliente do Adobe](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

   >[!CAUTION]
   >
   >O URL da página de aterrissagem deve ser exclusivo.

   ![](assets/lp_access-url.png)

1. Você pode definir uma data de expiração para sua página. Nesse caso, você deve selecionar uma ação ao expirar a página:

   * **[!UICONTROL Redirect URL]**: Insira o URL da página para a qual os usuários serão redirecionados quando a página expirar.
   * **[!UICONTROL Custom page]**: [Configurar uma subpágina](#configure-subpages) e selecione-o na lista suspensa que é exibida.
   * **[!UICONTROL Browser error]**: Digite o texto do erro que será exibido em vez da página.

   ![](assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. Se você selecionou uma ou mais listas de assinaturas ao [criação da página primária](design-lp.md), são exibidos na variável **[!UICONTROL Subscription list]** seção.

   ![](assets/lp_subscription-list.png)

1. Na página de aterrissagem, é possível diretamente [criar uma jornada](../building-journeys/journey-gs.md#jo-build) que enviará uma mensagem de confirmação para os usuários quando enviarem o formulário. Saiba como criar uma jornada desse tipo no final [caso de uso](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Clique em **[!UICONTROL Create journey]** para ser redirecionado para o **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** lista.

## Configurar subpáginas {#configure-subpages}

É possível adicionar até 2 subpáginas. Por exemplo, você pode criar uma página de &#39;agradecimento&#39; que será exibida depois que os usuários enviarem o formulário e você pode definir uma página de erro que será chamada se ocorrer um problema com a landing page.

Para definir as configurações de subpágina, siga as etapas abaixo.

1. Você pode alterar o nome da página, que é **[!UICONTROL Subpage 1]** por padrão.

1. Edite o conteúdo da sua página usando o designer de conteúdo. Saiba como definir o conteúdo da página de aterrissagem [here](design-lp.md).

1. Defina o URL da página de aterrissagem. A primeira parte do URL requer que a delegação de domínio seja executada. Ela é pré-preenchida e não pode ser editada por meio da interface do usuário do . Para configurá-lo, entre em contato com seu representante de conta do Adobe ou com o [Equipe de suporte ao Atendimento ao cliente do Adobe](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}.

   >[!CAUTION]
   >
   >O URL da página de aterrissagem deve ser exclusivo.

![](assets/lp_subpage-settings.png)

## Testar a landing page {#test-landing-page}

Depois que as configurações e o conteúdo da landing page forem definidos, você poderá usar perfis de teste para visualizá-los. Se você inseriu [conteúdo personalizado](../personalization/personalize.md), você poderá verificar como esse conteúdo é exibido na landing page, aproveitando os dados do perfil de teste.

>[!CAUTION]
>
>Você precisa ter perfis de teste disponíveis para pré-visualizar suas mensagens e enviar provas. Saiba como [criar perfis de teste](../building-journeys/creating-test-profiles.md).

1. Na interface da landing page, clique no link **[!UICONTROL Preview & test]** para acessar a seleção de perfil de teste.

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >O **[!UICONTROL Preview]** também é acessível no designer de conteúdo.

1. No **[!UICONTROL Preview & test]** selecione um ou mais perfis de teste.

   ![](assets/lp_test-profiles.png)

   As etapas para selecionar perfis de teste são as mesmas que ao testar uma mensagem. Eles são detalhados [nesta seção](../messages/preview.md#select-test-profiles).

1. Selecione o **[!UICONTROL Preview]** e clique em **[!UICONTROL Open preview]** para testar sua landing page.

   ![](assets/lp_open-preview.png)

1. A visualização da landing page é aberta em uma nova guia. Os elementos personalizados são substituídos pelos dados de perfil de teste selecionados.

   ![](assets/lp_preview.png)

1. Selecione outros perfis de teste para visualizar a renderização de cada variante da landing page.

## Verificar alertas {#check-alerts}

Ao criar a landing page, os alertas avisam quando você precisa tomar ações importantes antes de publicar.

Os alertas são exibidos na parte superior direita da tela, conforme mostrado abaixo:

![](assets/lp_alerts.png)

>[!NOTE]
>
>Se você não vir este botão, nenhum alerta foi detectado.

Dois tipos de alertas podem acontecer:

* **Avisos** consulte recomendações e práticas recomendadas. <!--For example, a message will display if -->

* **Erros** impedir a publicação da mensagem, desde que não sejam resolvidas. Por exemplo, você receberá um aviso se o URL da página primária estiver ausente.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> Você precisa resolver tudo **erro** alertas antes da publicação.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you need to resolve all **error** alerts.
-->

## Publicar a landing page {#publish-landing-page}

Quando a landing page estiver pronta, você poderá publicá-la para disponibilizá-la para uso em uma mensagem.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Antes de publicar, verifique e resolva os alertas. [Saiba mais](#check-alerts)

Depois que a landing page é publicada, ela é adicionada à lista de landing page com a variável **[!UICONTROL Published]** status.

Agora ele está ativo e pronto para ser usado em um [!DNL Journey Optimizer] [message](../messages/create-message.md) que será enviado por meio de um [jornada](../building-journeys/journey.md).

>[!NOTE]
>
>Você pode monitorar os impactos de sua landing page por meio de relatórios específicos. [Saiba mais](lp-report.md)

