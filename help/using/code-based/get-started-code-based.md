---
title: Introdução a experiências baseadas em código
description: Saiba mais sobre experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 83c8417d4aee278eba33e4adf6ccd033bcc6be1a
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 83%

---

# Introdução ao canal baseado em código {#get-sarted-code-based}

O [!DNL Journey Optimizer] permite personalizar e testar as experiências que você deseja entregar aos clientes em todos os seus pontos de contato, como aplicativos Web, aplicativos móveis, aplicativos de desktop, consoles de vídeo, dispositivos conectados à TV, smart TVs, quiosques, ATMs, assistentes de voz, dispositivos IoT, etc.

Com o recurso **experiência baseada em código**, é possível definir experiências de entrada usando um editor não visual simples e intuitivo. Isso permite inserir e editar elementos específicos em locais individuais e mais granulares de aplicativos ou páginas da Web, independentemente do tipo de aplicativos que você possui, ao invés de aplicar modificações a um conteúdo inteiro.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>As medidas de proteção e recomendações específicas para experiências baseadas em código são detalhadas [nesta página](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Lead" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>Como funciona</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Validação" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>Medidas de proteção e pré-requisitos</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Pouco frequente" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Criar uma experiência baseada em código</strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="Validação" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Amostras de implementação</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Quando usar canais baseados em código em vez de outros canais {#code-based-vs-other-channels}

### Baseado em código vs. outros canais

Quando usar o canal baseado em código em vez de outros canais do [!DNL Journey Optimizer]?

* Você pode considerar o uso de experiências baseadas em código a qualquer momento quando sua propriedade digital não for acessada por um navegador Web ou por um aplicativo móvel, casos em que provavelmente será melhor usar o [canal Web](../web/get-started-web.md){target="_blank"} do [!DNL Journey Optimizer] ou o canal de [mensagens no aplicativo](../in-app/get-started-in-app.md){target="_blank"} do [!DNL Journey Optimizer].

* Você pode usar o canal baseado em código como uma alternativa ao canal da Web do [!DNL Journey Optimizer] se o site não puder ser carregado no editor visual do [Designer da Web](../web/edit-web-content.md#work-with-web-designer){target="_blank"} ou se você não puder usar a [extensão do navegador](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} que permite a criação visual para o canal da Web.

* Também é possível usar o canal baseado em código como uma alternativa aos canais da Web ou no aplicativo do [!DNL Journey Optimizer], caso tenha uma implementação baseada em API, headless ou do lado do servidor.

### Baseado em código vs. canal da Web {#code-based-vs-web}

Para executar casos de uso da Web, é possível usar o canal da web ou a experiência baseada em código, mas, dependendo do contexto, um seria mais apropriado do que o outro. As principais diferenças estão listadas abaixo para que você possa tomar uma decisão informada sobre quando usar cada um.

**Web**

* Editar o conteúdo usando o editor visual do [Designer da Web](../web/edit-web-content.md#work-with-web-designer){target="_blank"}.
* Você precisa que a implementação do [SDK da Web da Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} e a extensão [Auxiliar de edição visual da Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} estejam instaladas no navegador da Web. [Saiba mais](../web/web-prerequisites.md){target="_blank"}
* O canal da Web permite modificar tudo na página e tem uma lista predefinida de ações que podem ser usadas para fazer alterações. [Saiba mais](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* É fácil de configurar e começar a usar.
* É focado na persona do profissional de marketing.

**Experiência baseada em código**

* Editar o conteúdo usando o [Editor de personalização](create-code-based.md#edit-code).
* A experiência baseada em código requer trabalho de desenvolvimento anterior em sua implementação para garantir que os aplicativos possam interpretar e entregar o conteúdo publicado na borda pelo [!DNL Journey Optimizer] para estes locais. [Saiba mais](code-based-configuration.md#surface-definition)
* Ela requer mais planejamento e pode alterar apenas as coisas que os desenvolvedores especificam. Portanto, é essencial identificar os componentes (banner inicial, Hero image, barra de menu, etc.) nos aplicativos que precisam ser modificados para personalização ou teste e trabalhar com a equipe de desenvolvimento na construção da implementação necessária para lidar com essas alterações.
* Ela permite usar o conteúdo de código JSON.
* É focada na persona do desenvolvedor

## Como funciona {#how-it-works}

>[!CAUTION]
>
>Este recurso é para a persona do desenvolvedor e/ou para usuários(as) experientes. Ele pode ser usado por profissionais de marketing com algumas habilidades de escrita de código, desde que as configurações de canal e a configuração inicial sejam tratadas pela sua equipe de desenvolvimento.

Para editar o conteúdo usando o recurso da experiência baseado em código do [!DNL Journey Optimizer], suas páginas ou aplicativos precisam ser instrumentados. Para fazer isso, você deve declarar antecipadamente os locais individuais específicos (chamados &quot;[superfícies](code-based-configuration.md#surface-definition)&quot;) onde deseja inserir ou substituir o conteúdo.

>[!NOTE]
>
>Atualmente, o conteúdo associado a uma configuração só pode ser HTML ou JSON.

As principais etapas para implementar uma campanha baseada em código são as seguintes.

1. Defina uma [superfície](code-based-configuration.md#surface-definition) na implementação do aplicativo, que é basicamente o local em que você deseja adicionar a experiência baseada em código, e crie uma configuração de canal de experiência baseada em código que faça referência a esse local. [Saiba como](code-based-configuration.md#create-code-based-configuration)

1. Crie uma jornada ou campanha em [!DNL Journey Optimizer] usando esta configuração. [Saiba como](create-code-based.md#create-code-based-campaign)

1. Componha uma experiência especificando o conteúdo da configuração selecionada usando o editor de personalização do [!DNL Journey Optimizer]. [Saiba como](create-code-based.md#edit-code)

1. A equipe de implementação do aplicativo faz chamadas explícitas de API ou SDK para buscar conteúdo para as superfícies nomeadas, como “Texto do banner” ou “Bandeja de recomendações 1”, ou pontos de decisão não relacionados à interface em um aplicativo, como “parâmetros de algoritmo de pesquisa”. Nesse caso, a equipe de implementação é responsável pela renderização ou outra forma de interpretar e agir sobre o conteúdo retornado. [Saiba mais](code-based-implementation-samples.md)
