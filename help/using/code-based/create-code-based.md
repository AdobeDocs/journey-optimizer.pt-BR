---
title: Criar experiências baseadas em código
description: Saiba como criar experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 9%

---

# Criar experiências baseadas em código {#create-code-based}

Atualmente, em [!DNL Journey Optimizer], você só pode criar experiências baseadas em código em **campanhas**.

As medidas de proteção e recomendações específicas para experiências baseadas em código são detalhadas [nesta página](code-based-prerequisites.md).

## Criar uma campanha baseada em código {#create-code-based-campaign}

Para começar a criar sua experiência baseada em código por meio de uma campanha, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Campanhas]** e clique em **[!UICONTROL Criar campanha]**. [Saiba mais](../campaigns/create-campaign.md)

1. Selecione o tipo de campanha que deseja executar

   * **Agendado - Marketing**: execute a campanha imediatamente ou em uma data especificada. As campanhas programadas são destinadas ao envio de mensagens de marketing. Eles são configurados e executados na interface do usuário do.

   * **Acionado por API - Marketing/Transacional**: execute a campanha usando uma chamada de API. As campanhas acionadas por API destinam-se ao envio de mensagens de marketing ou transacionais, ou seja, mensagens enviadas após uma ação executada por um indivíduo: redefinição de senha, compra de carrinho etc.

1. Conclua as etapas para criar uma campanha, como as propriedades da campanha, [público-alvo](../audience/about-audiences.md) e [agendamento](../campaigns/create-campaign.md#schedule). Para obter mais informações sobre como configurar uma campanha, consulte [esta página](../campaigns/get-started-with-campaigns.md).

1. Selecione a ação **[!UICONTROL Experiência baseada em código]**.

1. Selecione ou crie a configuração de experiência baseada em código. [Saiba mais](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. Edite o conteúdo conforme desejado usando o editor de personalização. [Saiba mais](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## Editar o conteúdo do código {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Usar o editor de personalização"
>abstract="Insira e edite o código que deseja entregar como parte desta ação de experiência baseada em código."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=pt-BR" text="Introdução ao editor de personalização"

1. Na tela de edição da campanha, selecione **[!UICONTROL Editar código]**.

   ![](assets/code-based-campaign-edit-code.png)

1. O [editor de personalização](../personalization/personalization-build-expressions.md) se abre. É uma interface de criação de experiência não visual que permite criar seu código.

1. Você pode alternar o modo de criação de HTML para JSON e vice-versa.

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >Alterar o modo de criação resultará na perda de todo o código atual, portanto, alterne os modos antes de iniciar a criação.

1. Insira o código conforme necessário. Você pode aproveitar o editor de personalização do [!DNL Journey Optimizer] com todos os seus recursos de personalização e criação. [Saiba mais](../personalization/personalization-build-expressions.md)

1. Você pode adicionar fragmentos de expressão HTML ou JSON, se necessário. [Saiba como](../personalization/use-expression-fragments.md)

   Também é possível salvar parte do conteúdo do código como fragmento. [Saiba como](../content-management/fragments.md#save-as-expression-fragment)

1. Em campanhas baseadas em código, é possível usar o recurso de decisão da experiência. Selecione o ícone **[!UICONTROL Decisões]** na barra esquerda e clique em **[!UICONTROL Criar decisão]**. [Saiba mais](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >No momento, a Escolha de experiências está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.


1. Clique em **[!UICONTROL Salvar e fechar]** para confirmar as alterações.

Agora, assim que o desenvolvedor fizer uma chamada de API ou SDK para buscar conteúdo para a superfície definida na configuração do canal, as alterações serão aplicadas à página da Web ou aplicativo.

## Testar a campanha baseada em código {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Visualize sua experiência baseada em código"
>abstract="Acesse uma simulação de como será a sua experiência baseada em código."

Para exibir uma pré-visualização de sua experiência baseada em código modificada, siga as etapas abaixo. Informações detalhadas sobre como selecionar perfis de teste e visualizar seu conteúdo estão disponíveis na [página Visualizar e testar seu conteúdo](../content-management/preview-test.md).

>[!CAUTION]
>
>Você deve ter perfis de teste disponíveis para simular quais ofertas serão entregues a eles. Saiba como [criar perfis de teste](../audience/creating-test-profiles.md).

1. Na tela do editor de personalização ou de edição de conteúdo, selecione **[!UICONTROL Simular conteúdo]**.

   ![](assets/code-based-campaign-simulate.png)

1. Clique em **[!UICONTROL Gerenciar perfis de teste]** para selecionar um ou mais perfis de teste.

1. Uma visualização da sua experiência modificada baseada em código é exibida.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## Ativar a campanha baseada em código {#activate-code-based-campaign}

Depois de definir sua campanha baseada em código e editar seu conteúdo conforme desejado usando o [editor baseado em código](#edit-code), você pode revisá-lo e ativá-lo. Siga as etapas abaixo.

>[!NOTE]
>
>Você também pode pré-visualizar o conteúdo da campanha antes de ativá-lo. [Saiba mais](#test-code-based-campaign)

1. Em sua campanha baseada em código, selecione **[!UICONTROL Revisar para ativar]**.

   ![](assets/code-based-campaign-review.png)

1. Verifique e edite, se necessário, o conteúdo, as propriedades, a configuração, o público-alvo e o agendamento.

1. Selecione **[!UICONTROL Ativar]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Depois de clicar em **[!UICONTROL Ativar]**, pode levar até 1 minuto para que as alterações nas campanhas baseadas em código sejam disponibilizadas em tempo real no seu local.

Sua campanha baseada em código pega o status do **[!UICONTROL Live]** e agora está visível para o público selecionado. Cada recipient da campanha pode visualizar as modificações.

>[!NOTE]
>
>Se você definiu um agendamento para sua campanha baseada em código, ele tem o status **[!UICONTROL Agendado]** até que a data e a hora de início sejam atingidas.
>
>Se você ativar uma campanha baseada em código que afeta os mesmos locais que outra campanha que já está ativa, todas as alterações serão aplicadas aos seus locais.

Saiba mais sobre como ativar campanhas em [esta seção](../campaigns/review-activate-campaign.md).

## Interromper uma campanha baseada em código {#stop-code-based-campaign}

Quando uma campanha baseada em código está ativa, você pode interrompê-la para impedir que seu público-alvo veja suas modificações. Siga as etapas abaixo.

1. Selecione uma campanha ao vivo da lista.

1. No menu superior, selecione **[!UICONTROL Parar campanha]**.

   ![](assets/code-based-campaign-stop.png)

1. As modificações adicionadas não estarão mais visíveis para o público-alvo definido.

>[!NOTE]
>
>Quando uma campanha baseada em código é interrompida, não é possível editá-la ou ativá-la novamente. Você só pode duplicá-la e ativar a campanha duplicada.

## Relatórios de campanha baseados em código

Você pode acessar relatórios de campanha baseados em código na tela de resumo da campanha.

Os relatórios globais exibem eventos que ocorreram pelo menos duas horas atrás e abrangem eventos durante um período selecionado. Em comparação, os Relatórios em tempo real focalizam eventos que ocorreram nas últimas 24 horas, com um intervalo mínimo de dois minutos a partir da ocorrência do evento.

### Relatório ao vivo baseado em código {#live-report-code-based}

No **[!UICONTROL Relatório ao vivo]** da sua campanha, a guia **[!UICONTROL Experiência baseada em código]** detalha as principais informações relativas aos seus aplicativos ou páginas da Web. [Saiba mais sobre o relatório ao vivo](../reports/campaign-live-report.md)

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de experiência baseado em código.

Os KPIs do **[!UICONTROL Desempenho da experiência baseada em código]** detalham as principais informações relativas ao engajamento de seus visitantes com suas experiências baseadas em código, como:

* **[!UICONTROL Impressões]**: número total de experiências entregues a todos os usuários.

* **[!UICONTROL Interações]**: número total de interações com seu aplicativo/página. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

O gráfico **[!UICONTROL Resumo da experiência baseado em código]** mostra a evolução das suas experiências (impressões, impressões exclusivas e interações) nas últimas 24 horas.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### Relatório global baseado em código {#global-report-code-based}

Um relatório global de campanha baseado em código pode ser acessado diretamente da sua campanha com o botão **[!UICONTROL Exibir relatório]**. [Saiba mais sobre o relatório global](../reports/campaign-global-report.md)

No seu **[!UICONTROL Relatório global]** do Campaign, a guia **[!UICONTROL Experiência baseada em código]** detalha as principais informações relativas aos seus aplicativos ou páginas da Web.

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++Saiba mais sobre as diferentes métricas e widgets disponíveis para o Relatório de experiência baseado em código.

Os KPIs de desempenho da experiência **[!UICONTROL baseada em código]** detalham as principais informações relativas ao engajamento dos visitantes com suas experiências, como:

* **[!UICONTROL Impressões exclusivas]**: número de usuários exclusivos a quem a experiência foi entregue.

* **[!UICONTROL Impressões]**: número total de experiências entregues a todos os usuários.

* **[!UICONTROL Interações]**: porcentagem de envolvimentos com seu aplicativo/página. Isso inclui qualquer ação realizada pelos usuários, como cliques ou quaisquer outras interações.

O gráfico **[!UICONTROL Resumo da experiência baseado em código]** mostra a evolução das suas experiências (impressões exclusivas, impressões e interações) para o período em questão.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
