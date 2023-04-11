---
solution: Journey Optimizer
product: journey optimizer
title: Trabalhar com modelos de AEM
description: Saiba como criar modelos no AEM e exportá-los para o Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
source-git-commit: 7a044f7c048ba797e7b857212f6d6b0cf2644b5d
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# Trabalhar com modelos do Adobe Experience Manager {#aem-templates}

>[!AVAILABILITY]
>
>A integração com o Adobe Experience Manager está disponível no momento como um beta somente para usuários selecionados.
> Como usuário beta, use [este formulário](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} para compartilhar comentários.

Com o Adobe Journey Optimizer, você pode criar mensagens personalizadas por meio de sites do Adobe Experience Manager. Comece criando seus modelos usando fontes de conteúdo Adobe Experience Manager e envie-os para o Adobe Journey Optimizer. Depois de compartilhados, esses modelos podem ser acessados no designer de email do Adobe Journey Optimizer, simplificando o processo de criação e envio de mensagens para o público-alvo desejado.

## Pré-requisitos {#prerequisites}

Antes de começar a usar esse recurso, verifique se você está alinhado com os seguintes requisitos:

* **Configurações de Experience Manager**

   Esse recurso está disponível com [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

   Como parte do programa beta, a configuração Cloud Service é executada pelo Adobe no Adobe Experience Manager para se conectar ao Adobe Journey Optimizer.

* **Permissões**

   Para criar, editar e excluir modelos de conteúdo no Adobe Journey Optimizer, você deve ter a variável **[!DNL Manage Library Items]** permissão incluída no **[!DNL Content Library Manager]** perfil do produto. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)

## Medidas de proteção e limitações{#aem-templates-limitations}

Para otimizar ainda mais o uso do Adobe Experience Manager com o Adobe Journey Optimizer, é importante estar ciente das seguintes medidas de proteção e limitações adicionais:

* A sintaxe Journey Optimizer adequada é necessária para que a personalização no template Experience Manager seja efetiva. [Saiba mais](../personalization/personalization-syntax.md)

* A exportação de modelo em massa não é suportada no momento, os modelos devem ser exportados individualmente.

* A sincronização entre o Experience Manager e o Journey Optimizer não está disponível no momento. Se forem feitas alterações em um template Experience Manager após o envio para o Journey Optimizer, o usuário precisará reexportar o template e reenviá-lo para o Journey Optimizer.

## Enviar um modelo para o Journey Optimizer{#aem-templates-send}

Para exportar um template Adobe Experience Manager para o Adobe Journey Optimizer, siga as etapas abaixo:

1. Na página inicial do Adobe Experience Manager, selecione o **[!UICONTROL Marketing de saída]**.

   ![](assets/aem-outbound-menu.png)

1. Na biblioteca de conteúdo, é possível usar modelos configurados anteriormente ou criar um do zero. [Saiba mais](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. Ao incorporar a sintaxe de personalização do Journey Optimizer ao seu modelo, você pode aprimorar seus recursos de personalização. [Saiba mais](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. Selecione o modelo que deseja exportar para o Journey Optimizer e clique em **[!UICONTROL Enviar para]** no menu avançado.

   ![](assets/aem-advanced-menu.png)

1. Insira o **[!UICONTROL Nome]** do template Content e selecione o target **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. Depois de clicar no botão **[!UICONTROL Enviar]** , o processo de exportação será iniciado. Quando a exportação for concluída, você verá a seguinte mensagem na interface do usuário: &quot;Modelo &quot;XX&quot; enviado com êxito para AJO&quot;.

O modelo é adicionado aos modelos de conteúdo do Adobe Journey Optimizer da sandbox selecionada.

## Usar e personalizar um template do Adobe Experience Manager{#aem-templates-perso}

Quando o template Experience Manager estiver disponível no Journey Optimizer como um template de conteúdo, você poderá identificar e incorporar o conteúdo necessário para o email, incluindo a personalização.

1. No Journey Optimizer, na **[!UICONTROL Modelo de conteúdo]** , acesse o template importado.

   ![](assets/aem_ajo_1.png)

1. Ao clicar no botão **[!UICONTROL Alerta]** , você pode verificar rapidamente se alguma configuração importante está ausente. Isso ajudará a garantir que suas mensagens estejam configuradas corretamente e evitará possíveis erros ou problemas.

   ![](assets/aem_ajo_2.png)

1. No **[!UICONTROL Propriedades do template]** clique no botão **[!UICONTROL Gerenciar acesso]** para atribuir rótulos de uso de dados personalizados ou principais ao modelo. [Saiba mais sobre o Controle de Acesso no Nível do Objeto (OLAC)](../administration/object-based-access.md)

1. Para personalizar ainda mais seu modelo de Experience Manager e adicionar personalização personalizada ao seu conteúdo, clique em **[!UICONTROL Editar conteúdo]**. Isso permitirá fazer alterações facilmente e adaptar o modelo às suas necessidades específicas. [Saiba mais](get-started-email-design.md)

   >[!NOTE]
   >
   > Se quiser editar e personalizar seu template, você só poderá usar o modo de compatibilidade.

1. Quando o template de conteúdo estiver pronto, [testar e validar](content-templates.md#test-template).

1. Depois que o conteúdo tiver sido definido, você poderá usá-lo ao criar um novo email navegando na variável **[!UICONTROL Modelos salvos]** coleção. Em seguida, selecione **[!UICONTROL Usar este modelo]**.

   ![](assets/aem_ajo_3.png)

1. Agora é possível editar e personalizar o conteúdo. Para obter mais informações sobre como criar o conteúdo de email, consulte esta seção [página](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. Se você tiver adicionado conteúdo personalizado ao seu modelo de Experience Manager, clique em **[!UICONTROL Simular conteúdo]** para visualizar como ele aparecerá na mensagem usando perfis de teste.

[Saiba mais sobre perfis de visualização e teste](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. Ao visualizar a pré-visualização da mensagem, qualquer elemento personalizado é automaticamente substituído pelos dados correspondentes do perfil de teste selecionado.

   Se necessário, perfis de teste adicionais podem ser adicionados por meio da variável **[!UICONTROL Gerenciar perfis de teste]** botão.

   ![](assets/aem_ajo_7.png)

Quando o email estiver pronto, conclua a configuração do [jornada](../building-journeys/journey-gs.md) ou [campanha](../campaigns/create-campaign.md)e ativá-la para enviar a mensagem.
