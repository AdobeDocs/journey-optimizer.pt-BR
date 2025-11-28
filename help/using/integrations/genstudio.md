---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com o GenStudio for Performance Marketing no Journey Optimizer
description: Saiba como trabalhar com o GenStudio for Performance Marketing no Journey Optimizer
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
badge: label="Disponibilidade limitada" type="Informative"
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: 784f1fbfbf2cfa73666bdc943fc30028c9dc913c
workflow-type: tm+mt
source-wordcount: '1254'
ht-degree: 9%

---

# Trabalhar com o GenStudio for Performance Marketing {#ajo-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Usar um modelo criado com o GenStudio"
>abstract="Graças à integração perfeita com o Adobe GenStudio for Performance Marketing, você pode importar facilmente um modelo do GenStudio aprimorado com a tecnologia de IA da Adobe."

## Introdução ao GenStudio {#gs-genstudio}

O [Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/pt-br/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"} é um aplicativo generativo de IA que permite que as equipes de marketing criem seus próprios anúncios e emails para impulsionar campanhas de marketing personalizadas e impactantes que seguem os padrões da sua marca e estão em conformidade com as políticas da sua empresa. Ao utilizar a tecnologia de IA do Adobe, ele fornece um conjunto abrangente de ferramentas que simplificam as complexidades da criação e do gerenciamento de conteúdo para que os criadores possam se concentrar na inovação.

>[!AVAILABILITY]
>
>* A integração do GenStudio no [!DNL Adobe Journey Optimizer] não está disponível para uso com as ofertas complementares do **Healthcare Shield** ou **Privacy and Security Shield**.
>
>* Esse recurso está disponível somente para o canal de email.

Para aprimorar a eficiência do marketing e manter a consistência da marca, você pode integrar perfeitamente as experiências do [!DNL **GenStudio for Performance Marketing**] com o [!DNL **Adobe Journey Optimizer**]. Isso permite aproveitar a criação de conteúdo habilitado por IA do [!DNL GenStudio] junto com os recursos avançados de orquestração do [!DNL Journey Optimizer].

![Importar um conteúdo do GenStudio para o Adobe Journey Optimizer](../rn/assets/do-not-localize/genstudio.gif)

>[!INFO]
>
>Para ir além, confira esta [visão geral](https://business.adobe.com/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"} e uma [demonstração](https://business.adobe.com/products/genstudio-for-performance-marketing.html#demo){target="_blank"} de [!DNL Adobe GenStudio for Performance Marketing].

➡️ [Conheça este recurso no vídeo](#video)

## Pré-requisitos {#genstudio-prerequisites}

Para usar a integração do [!DNL GenStudio for Performance Marketing] com o [!DNL Journey Optimizer], verifique se os seguintes requisitos foram atendidos:

* Sua organização deve ter uma licença ativa para [!DNL GenStudio for Performance Marketing].

* [!DNL GenStudio for Performance Marketing] e [!DNL Adobe Journey Optimizer] devem pertencer à mesma organização IMS.

* Os usuários devem ter pelo menos a função **Colaborador** ou superior em [!DNL GenStudio for Performance Marketing] para utilizar os recursos de integração. [Saiba mais sobre as funções de usuário no GenStudio](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/user-roles){target="_blank"}

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](../content-management/gs-generative.md#generative-guardrails) for AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## Aproveitar os recursos do GenStudio no Journey Optimizer {#use-genstudio}

A integração do [!DNL GenStudio for Performance Marketing] e do [!DNL Journey Optimizer] permite que os profissionais de marketing da sua empresa trabalhem melhor em conjunto para simplificar processos.

Por exemplo, um profissional de marketing técnico, que usa o [!DNL Journey Optimizer] para desenvolver e automatizar campanhas de email, pode colaborar com um profissional de marketing de desempenho que cria conteúdo usando o [!DNL GenStudio].

Com essa integração, ambos podem trabalhar em conjunto para integrar facilmente o conteúdo sob a marca do [!DNL GenStudio] ao [!DNL Journey Optimizer], fornecendo emails envolventes direcionados a segmentos específicos de clientes e impulsionando as vendas.

### Principais recursos {#genstudio-capabilities}

Essa integração libera recursos avançados para sua organização de marketing:

* **Geração de conteúdo habilitada por IA**: aproveite a IA gerativa da Adobe para criar com eficiência várias variações de email na marca, com sugestões de cópia inteligentes e elementos de design.

* **Integração perfeita do fluxo de trabalho**: exporte modelos de email do Journey Optimizer para o GenStudio, crie variações com prompts de IA e importe-os de volta para o Journey Optimizer em um processo simplificado.

* **Gerenciamento centralizado de ativos**: acesse o ContentHub da GenStudio, desenvolvido pela Adobe Experience Manager Assets, para organizar, armazenar e recuperar todos os ativos digitais em um local centralizado.

* **Experimentação de conteúdo**: importe várias variações de email do GenStudio para o Journey Optimizer e aproveite os recursos de experimentação para testar e identificar o conteúdo com melhor desempenho.

* **Insights orientados por desempenho**: acompanhe o desempenho da campanha com análises alimentadas por IA para entender quais elementos criativos refletem em seu público-alvo e otimizar campanhas futuras.

### Casos de uso comuns {#genstudio-use-cases}

A integração entre [!DNL GenStudio for Performance Marketing] e [!DNL
O Journey Optimizer] oferece suporte a vários cenários de marketing:

* **Campanhas de lançamento de produtos**: gere rapidamente várias variantes de email para anúncios de produtos, teste-as com diferentes segmentos de público-alvo e dimensione a versão vencedora em toda a sua base de clientes.

* **Promoções de feriados e sazonais**: produza conteúdo de campanha sensível ao tempo em escala usando modelos do GenStudio, garantindo a consistência da marca e, ao mesmo tempo, cumprindo prazos apertados.

* **Teste A/B em escala**: crie várias variações de conteúdo no GenStudio e teste-as sistematicamente no Journey Optimizer para melhorar continuamente o desempenho do email.

* **Personalização de vários segmentos**: gere conteúdo personalizado para diferentes personalidades de clientes no GenStudio e implante cada variação em seu segmento correspondente no Journey Optimizer para relevância máxima.

## Usar a integração do GenStudio {#how-to-use}

O fluxo de trabalho de integração consiste em duas etapas principais: exportar um modelo do Journey Optimizer para o GenStudio e importar experiências do GenStudio de volta para o Journey Optimizer.

### Exportar um modelo do HTML do Journey Optimizer para o GenStudio {#export-from-ajo-to-genstudio}

Comece exportando um modelo do HTML [!DNL Journey Optimizer], incluindo as diretrizes da sua marca, para [!DNL GenStudio for Performance Marketing]. Siga as etapas abaixo.

1. No [!DNL Journey Optimizer], acesse o conteúdo do seu email em uma jornada ou campanha. [Saiba como](../email/get-started-email-design.md#key-steps)

1. No Designer Email, selecione **[!UICONTROL Exportar HTML]** no botão **[!UICONTROL Mais]**.

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Carregar este modelo exportado do HTML em [!DNL GenStudio for Performance Marketing]. <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Saiba como carregar um modelo do HTML no [!DNL GenStudio] na seção dedicada do [Guia do Usuário do Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}.

1. No GenStudio, use esse template para criar várias variações de email com prompts de IA e salvá-las.

   >[!NOTE]
   >
   >Saiba como criar experiências de email na [seção](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"} dedicada do GenStudio.

### Aproveitar as experiências do GenStudio no Journey Optimizer {#leverage-genstudio-experiences}

Depois de criar variações de email no GenStudio, importe-as de volta para o [!DNL Journey Optimizer] para usar em suas campanhas. Siga as etapas abaixo.

1. Em [!DNL Journey Optimizer], [adicione um email](../email/create-email.md) a uma campanha.

1. Na tela de configuração da campanha, acesse a [tela Editar conteúdo](../email/create-email.md#define-email-content) e clique em **[!UICONTROL Editar corpo do email]** para abrir o Email Designer. [Saiba como](../email/get-started-email-design.md#key-steps)

1. Na página inicial do Designer de Email, selecione **[!UICONTROL Importar HTML]** e clique no botão **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Navegue pelas experiências do GenStudio para começar a criar o conteúdo. Você pode filtrar as experiências em vários critérios, como produtos, personas, marcas ou até mesmo cores.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Selecione uma experiência e clique em **[!UICONTROL Usar]**.

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Selecione a pasta na qual deseja importar a experiência do GenStudio.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. O conteúdo selecionado é exibido no Designer de email.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >As experiências do GenStudio [criadas a partir de um [!DNL Journey Optimizer] modelo](#export-from-ajo-to-genstudio) são importadas diretamente para o Designer de email com recursos de edição completos. As experiências do GenStudio criadas sem um modelo [!DNL Journey Optimizer] são importadas para o [modo de compatibilidade](../email/existing-content.md), que pode ter funcionalidade de edição limitada.

1. Use as [ferramentas de edição de conteúdo de email](../email/content-from-scratch.md) e os [campos de personalização](../personalization/personalize.md) para editar seu email conforme necessário. Salve o conteúdo.

1. Volte para a página de resumo da campanha e clique em **[!UICONTROL Criar experimento]** para usar a experimentação. [Saiba como criar um experimento de conteúdo](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Crie vários tratamentos e repita as etapas acima para importar e aproveitar rapidamente as outras variações de experiência de email que você criou no [!DNL GenStudio].

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Salve as alterações e [ative](../campaigns/review-activate-campaign.md) a campanha.

1. Após executar o experimento, acompanhe o desempenho dos tratamentos da campanha com o [relatório da campanha de experimentação](../reports/campaign-global-report-cja-experimentation.md). Você pode então interpretar os resultados de seu experimento. [Saiba como](../content-management/get-started-experiment.md#interpret-results)

## Perguntas frequentes {#genstudio-faq}

Encontre respostas para perguntas comuns sobre a integração do [!DNL GenStudio for Performance Marketing] com o [!DNL Journey Optimizer].

+++Posso usar a integração do GenStudio para canais diferentes do email?

Atualmente, a integração do [!DNL GenStudio for Performance Marketing] está disponível somente para o canal de email. O suporte para canais adicionais poderá ser adicionado em versões futuras.
+++

+++A integração do GenStudio está disponível para todos os clientes da Journey Optimizer?

No momento, a integração não está disponível para organizações que usam as ofertas complementares do **Healthcare Shield** ou **Privacy and Security Shield**.
+++

+++Posso editar o conteúdo do GenStudio após importá-lo para o Journey Optimizer?

Sim, após importar as experiências do GenStudio para o [!DNL Journey Optimizer], você pode usar as [ferramentas de edição de conteúdo](../email/content-from-scratch.md) do Designer de email e adicionar [campos de personalização](../personalization/personalize.md) para personalizar ainda mais seu conteúdo de email.
+++

+++O que acontece com as experiências do GenStudio criadas sem um modelo do Journey Optimizer?

As experiências do GenStudio criadas a partir de um modelo [!DNL Journey Optimizer] são importadas diretamente para o Designer de email. As experiências do GenStudio criadas sem um modelo [!DNL Journey Optimizer] são importadas para o [modo de compatibilidade](../email/existing-content.md).
+++

+++Posso testar várias variações de email do GenStudio no Journey Optimizer?

Sim, você pode criar vários tratamentos de conteúdo importando diferentes variações de email do GenStudio e usar o recurso [experimentação de conteúdo](../content-management/content-experiment.md) do Journey Optimizer para testar qual variação tem melhor desempenho com seu público-alvo.
+++

+++Como o GenStudio garante a consistência da marca?

O GenStudio usa verificações de marca habilitadas por IA para garantir que todo o conteúdo gerado siga os padrões e as diretrizes da sua marca. Ao fazer upload de modelos que incluem os elementos da marca, o GenStudio aplica esses padrões a todas as variações de conteúdo criadas na plataforma.
+++

+++Posso colaborar com outros membros da equipe nas experiências do GenStudio?

Sim, o GenStudio foi projetado para colaboração. Vários membros da equipe com as permissões apropriadas podem trabalhar juntos na criação e refinamento de experiências de email antes de importá-las para o [!DNL Journey Optimizer].
+++

## Vídeo tutorial {#video}

Descubra como exportar um modelo de email do Journey Optimizer para o GenStudio para marketing de desempenho, criando emails compatíveis com a marca por meio do modelo no GenStudio e importando-os perfeitamente de volta para o Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3456038/?quality=12)