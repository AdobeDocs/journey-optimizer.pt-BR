---
solution: Journey Optimizer
product: journey optimizer
title: Personalizar configurações da superfície de email
description: Saiba como definir valores personalizados para suas configurações no nível de superfície de canal de email
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: configurações, email, configuração, subdomínio
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 56c2708408d15286f008c9f2c16581ce0f0a1c4e
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 13%

---

# Personalizar configurações da superfície de email {#surface-personalization}

Para obter mais flexibilidade e controle sobre as configurações de email, [!DNL Journey Optimizer] permite definir valores personalizados para subdomínios e cabeçalhos<!--and URL tracking parameters--> ao criar superfícies de email.

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível como um beta apenas para usuários selecionados. <!--To join the beta program, contact Adobe Customer Care.-->

## Adicionar subdomínios dinâmicos  {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalização indisponível"
>abstract="Esta superfície foi criada sem nenhum atributo de personalização. Consulte a documentação para saber quais são as etapas a serem seguidas, se a personalização for necessária."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Habilitar subdomínios dinâmicos"
>abstract="Ao criar uma superfície de email, você pode configurar subdomínios dinâmicos com base nas condições definidas por meio do editor de expressão. Você pode adicionar até 50 subdomínios dinâmicos."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Alguns subdomínios podem estar indisponíveis"
>abstract="Certos subdomínios não estão disponíveis para seleção no momento devido ao registro do loop de feedback pendente. Esse processo pode demorar até 10 dias úteis. Após a conclusão, você pode escolher entre todos os subdomínios disponíveis."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Introdução à delegação de subdomínio"

Ao criar uma superfície de email, você pode configurar subdomínios dinâmicos com base em condições específicas.

Por exemplo, se você tiver restrições legais para enviar mensagens de um endereço de email dedicado por país, poderá usar subdomínios dinâmicos. Isso permite criar uma única superfície com vários subdomínios de envio correspondentes a diferentes países, em vez de criar várias superfícies para cada país. Em seguida, você pode direcionar clientes com base em vários países consolidados em uma única campanha.

Para definir subdomínios dinâmicos em uma superfície de canal de email, siga as etapas abaixo.

1. Antes de criar uma superfície, configure os subdomínios que deseja usar para enviar emails de acordo com seu caso de uso. [Saiba como](../configuration/about-subdomain-delegation.md)

   Por exemplo, digamos que você queira usar subdomínios diferentes para países diferentes: configure um subdomínio específico para os EUA, um específico para o Reino Unido etc.

1. Crie uma superfície de canal. [Saiba como](../configuration/channel-surfaces.md)

1. Selecione o **[!UICONTROL E-mail]** canal.

1. No **Subdomínio** habilite a opção **[!UICONTROL Subdomínio dinâmico]** opção.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Selecione o ícone Editar ao lado do primeiro **[!UICONTROL Condição]** campo.

1. A variável [Editor de expressão](../personalization/personalization-build-expressions.md) é aberto. Neste exemplo, defina uma condição como `Country` igual a `US`.

   ![](assets/surface-email-edit-condition.png)

1. Selecione o subdomínio que deseja associar a essa condição. [Saiba mais sobre subdomínios](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Determinados subdomínios não estão disponíveis para seleção no momento devido a [loop de comentários](../reports/deliverability.md#feedback-loops) registro. Esse processo pode demorar até 10 dias úteis. Após a conclusão, você pode escolher entre todos os subdomínios disponíveis. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Todos os recipients baseados nos EUA receberão mensagens usando o subdomínio selecionado para esse país, o que significa que todos os URLs envolvidos (como mirror page, URL de rastreamento ou link de cancelamento de inscrição) serão preenchidos com base nesse subdomínio.

1. Defina outros subdomínios dinâmicos conforme desejado. Você pode adicionar até 50 itens.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Definir todos os outros [configurações de email](email-settings.md) e [enviar](../configuration/channel-surfaces.md#create-channel-surface) sua superfície.

Depois de adicionar um ou mais subdomínios dinâmicos a uma superfície, os seguintes itens serão preenchidos com base no subdomínio dinâmico resolvido para essa superfície:

* Todos os URLs (URL de recurso, URL de mirror page e URL de rastreamento)

* A variável [cancelar inscrição do URL](email-settings.md#list-unsubscribe)

* A variável **Do email** e **Email de erro** sufixos

>[!NOTE]
>
>Se você configurar subdomínios dinâmicos e desativar o **[!UICONTROL Subdomínio dinâmico]** todos os valores dinâmicos são removidos. Selecione um subdomínio e envie a superfície para que as alterações entrem em vigor.

## Personalizar o cabeçalho {#personalize-header}

Você também pode usar a personalização para todos os parâmetros de cabeçalho definidos em uma superfície.

Por exemplo, se você tiver várias marcas, poderá criar uma única superfície e usar valores personalizados para seus cabeçalhos de email. Isso permite garantir que todos os emails enviados de suas diferentes marcas sejam endereçados a cada um de seus clientes com o endereço correto **De** nomes e emails. Da mesma forma, quando seus destinatários atingem o **Responder** no software cliente de email, você deseja que o **Responder para** os nomes e e-mails correspondem à marca correta para o usuário correto.

Para usar variáveis personalizadas para seus parâmetros de cabeçalho de superfície, siga as etapas abaixo.

>[!NOTE]
>
>Você pode personalizar tudo **[!UICONTROL Parâmetros de cabeçalho]** campos, exceto o **[!UICONTROL Prefixo de email de erro]** campo.


1. Defina os parâmetros do cabeçalho como faria normalmente. [Saiba como](email-settings.md#email-header)

1. Para cada campo, selecione o ícone Editar.

   ![](assets/surface-email-personalize-header.png)

1. A variável [Editor de expressão](../personalization/personalization-build-expressions.md) é aberto. Defina sua condição como desejado e salve as alterações.

   Por exemplo, defina uma condição para que cada recipient receba um email do representante de sua própria marca.

   >[!NOTE]
   >
   >Você só pode selecionar **[!UICONTROL Atributos do perfil]** e **[!UICONTROL Funções auxiliares]**.

1. Repita as etapas acima para cada parâmetro ao qual deseja adicionar personalização.

>[!NOTE]
>
>Se você tiver adicionado um ou mais subdomínios dinâmicos à superfície, a variável **Do email** e **Email de erro** os sufixos serão preenchidos com base na variável [subdomínio dinâmico](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Exibir detalhes da superfície {#view-surface-details}

Ao usar uma superfície com configurações personalizadas em uma campanha ou superfície, você pode exibir os detalhes da superfície diretamente na campanha ou superfície. Siga as etapas abaixo.

1. Criar um email [campaign](../campaigns/create-campaign.md) ou [jornada](../building-journeys/journey-gs.md).

1. Selecione o **[!UICONTROL Editar conteúdo]** botão.

1. Clique em **[!UICONTROL Exibir detalhes da superfície]** botão.

   ![](assets/campaign-view-surface-details.png)

1. A variável **[!UICONTROL Configurações de entrega]** é exibida. Você pode exibir todas as configurações da superfície, incluindo os subdomínios dinâmicos e os parâmetros de cabeçalho personalizados.

   >[!NOTE]
   >
   >Todas as informações nesta tela são somente leitura.

1. Selecionar **[!UICONTROL Expandir]** para exibir os detalhes dos subdomínios dinâmicos.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
