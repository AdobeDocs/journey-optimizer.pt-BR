---
solution: Journey Optimizer
product: journey optimizer
title: Criar emails
description: Saiba como criar seus emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: email, design, estoque, ativos
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: 3a9b11b1a4d2159261586394f1595e52c8b749e7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 12%

---

# Introdução ao design de email {#get-started-content-design}

É possível importar um conteúdo existente no [!DNL Journey Optimizer] ou utilize os recursos de design de conteúdo:

* Use [!DNL Journey Optimizer] **recursos de design de email** para criar ou importar emails responsivos. [Saiba mais](content-from-scratch.md)

* Aproveitar o **Adobe Experience Manager Assets Essentials** para enriquecer seus emails e criar e gerenciar seu próprio banco de dados de ativos. [Saiba mais](assets-essentials.md)

* Encontrar **fotos do Adobe Stock** para criar seu conteúdo e melhorar o design de emails. [Saiba mais](stock.md)

* Melhore a experiência dos clientes criando mensagens personalizadas e dinâmicas com base em seus atributos de perfil. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md).

➡️ [Descubra este recurso no vídeo](#video)

## Práticas recomendadas de design de email {#best-practices}

Ao enviar emails, é importante considerar que os recipients podem encaminhá-los, o que pode às vezes causar problemas com a renderização do email. Isso é particularmente verdadeiro ao usar classes CSS que podem não ser compatíveis com o provedor de email usado para encaminhamento, por exemplo, se estiver usando a classe CSS &quot;is-desktop-hidden&quot; para ocultar uma imagem em dispositivos móveis.

Para minimizar esses problemas de renderização, recomendamos manter sua estrutura de design de email o mais simples possível. Tente usar um único design que funcione bem para desktops e dispositivos móveis e evite usar classes CSS complexas ou outros elementos de design que possam não ser totalmente compatíveis com todos os clientes de email. Ao seguir essas práticas recomendadas, você pode ajudar a garantir que seus emails sejam renderizados corretamente de forma consistente, independentemente de como sejam visualizados ou encaminhados pelos recipients.

## Etapas principais para criar conteúdo de email {#key-steps}

Depois de [adição de um email](create-email.md) para uma jornada ou campanha, você pode começar a criar o conteúdo do seu email.

1. Na tela de configuração da jornada ou campanha, acesse o **[!UICONTROL Editar conteúdo]** para acessar o Designer de email. [Saiba mais](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. Na página inicial do Designer de email, escolha como deseja criar o email com as seguintes opções:

   * **Crie seu email do zero** por meio da interface do designer de email e aproveite imagens de [Adobe Experience Manager Assets Essentials](assets-essentials.md). Saiba como criar o conteúdo de email no [esta seção](content-from-scratch.md).

   * **Código ou cole HTML bruto** diretamente no designer de email. Saiba como codificar seu próprio conteúdo no [esta seção](code-content.md).

      >[!NOTE]
      >
      >Em uma campanha, você também pode selecionar a variável **[!UICONTROL Editor de códigos]** do botão **[!UICONTROL Editar conteúdo]** tela. [Saiba mais](create-email.md#define-email-content)

   * **Importar conteúdo HTML existente** de um arquivo ou uma pasta .zip. Saiba como importar conteúdo de email no [esta seção](existing-content.md).

   * **Selecionar um conteúdo existente** em uma lista de modelos incorporados ou personalizados. Saiba como trabalhar com modelos de email [esta seção](email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Depois que o conteúdo do email tiver sido definido e personalizado, você poderá exportar o conteúdo para validação ou para uso posterior. Clique em **[!UICONTROL Exportar HTML]** para salvar em seu computador um arquivo zip que incluirá o HTML e os ativos.

   ![](assets/email_designer_export.png)

## Vídeo tutorial {#video}

Saiba como criar conteúdo de email com o editor de mensagens.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)