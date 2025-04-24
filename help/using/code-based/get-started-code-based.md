---
title: Introdução a experiências baseadas em código
description: Saiba mais sobre experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: ht
source-wordcount: '789'
ht-degree: 100%

---

# Introdução ao canal baseado em código {#get-sarted-code-based}

O [!DNL Journey Optimizer] permite personalizar e testar as experiências que você deseja entregar aos clientes em todos os seus pontos de contato, como aplicativos Web, aplicativos móveis, aplicativos de desktop, consoles de vídeo, dispositivos conectados à TV, smart TVs, quiosques, ATMs, assistentes de voz, dispositivos IoT, etc.

Com o recurso **experiência baseada em código**, é possível definir experiências de entrada usando um editor não visual simples e intuitivo. Isso permite inserir e editar elementos específicos em locais individuais e mais granulares de aplicativos ou páginas da Web, independentemente do tipo de aplicativos que você possui, ao invés de aplicar modificações a um conteúdo inteiro.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Recomendações específicas para experiências baseadas em código são detalhadas [nesta página](code-based-prerequisites.md).


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
<a href="code-based-configuration.md">
<img alt="Validação" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Configuração de canais baseada em código</strong></a>
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
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ [Esta seção](../experience-decisioning/experience-decisioning-uc.md) apresenta um caso de uso completo que mostra como usar experimentos de conteúdo para comparar decisões com o canal de experiência baseado em código.

## Quando usar canais baseados em código em vez de outros canais {#code-based-vs-other-channels}

### Baseado em código vs. outros canais

Quando usar o canal baseado em código em vez de outros canais do [!DNL Journey Optimizer]?

* Você pode considerar o uso de experiências baseadas em código a qualquer momento quando sua propriedade digital não for acessada por um navegador Web ou por um aplicativo móvel, casos em que provavelmente será melhor usar o [canal Web](../web/get-started-web.md){target="_blank"} do [!DNL Journey Optimizer] ou o canal de [mensagens no aplicativo](../in-app/get-started-in-app.md){target="_blank"} do [!DNL Journey Optimizer].

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* É possível usar o canal baseado em código como uma alternativa aos canais da Web ou no aplicativo do [!DNL Journey Optimizer], caso tenha uma implementação baseada em API, headless ou do lado do servidor.

* Também é possível usar o canal baseado em código em aplicativos móveis nativos como uma alternativa ao canal no aplicativo se quiser modificar o conteúdo dentro do aplicativo nativo em vez de mostrar modais, pop-ups ou sobreposições.

### Baseado em código vs. canal da Web {#code-based-vs-web}

Para executar casos de uso da Web, é possível usar o canal da web ou a experiência baseada em código, mas, dependendo do contexto, um seria mais apropriado do que o outro. As principais diferenças estão listadas abaixo, para que você possa tomar uma decisão informada sobre o que usar e quando.

**Web**

* Edite o conteúdo usando o editor visual do [designer da web](../web/web-visual-editor.md){target="_blank"} ou o [editor não visual](../web/web-non-visual-editor.md) da web.
* É necessário ter o [SDK da Web da Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}, uma implementação do lado do cliente.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* O canal da Web permite modificar tudo na página e tem uma lista predefinida de ações que podem ser usadas para fazer alterações. [Saiba mais](../web/web-visual-editor.md){target="_blank"}
* É fácil de configurar e começar a usar.
* É focado na persona do profissional de marketing.

**Experiência baseada em código**

* Editar o conteúdo usando o [Editor de personalização](create-code-based.md#edit-code).
* É necessário ter o [SDK da Web da Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} - implementação do lado do cliente ou da [API do Servidor Edge Network da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=pt-BR){target="_blank"} - implementação do lado do servidor.
* A experiência baseada em código requer trabalho de desenvolvimento anterior em sua implementação para garantir que os aplicativos possam interpretar e entregar o conteúdo publicado na borda pelo [!DNL Journey Optimizer] para estes locais. [Saiba mais](code-based-surface.md)
* Ela requer mais planejamento e pode alterar apenas as coisas que os desenvolvedores especificam. Portanto, é essencial identificar os componentes (banner inicial, imagem hero, barra de menu, etc.) nos aplicativos que precisam ser modificados para personalização ou teste e trabalhar com a equipe de desenvolvimento na criação da implementação necessária para lidar com essas alterações.
* Ela permite usar o conteúdo de código JSON.
* É focada na persona do desenvolvedor

## Como funciona {#how-it-works}

>[!CAUTION]
>
>Este recurso é para a persona do desenvolvedor e/ou para usuários(as) experientes. Ele pode ser usado por profissionais de marketing que possuem algum nível de experiência em geração de código, desde que as configurações de canal e a instalação inicial sejam feitas pela sua equipe de desenvolvimento.

Para editar o conteúdo usando o recurso da experiência baseada em código do [!DNL Journey Optimizer], suas páginas ou aplicativos precisam ser instrumentados. Para fazer isso, você precisa declarar antecipadamente os locais individuais específicos (chamados de “[superfícies](code-based-surface.md)”) onde deseja inserir ou substituir o conteúdo.

>[!NOTE]
>
>Atualmente, o conteúdo associado a uma configuração deve estar apenas em HTML ou JSON.

Estas são as principais etapas para criar e entregar uma experiência baseada em código.

1. Certifique-se de seguir os pré-requisitos específicos do canal. [Saiba mais](code-based-prerequisites.md)

1. Defina uma [superfície](code-based-surface.md#surface-definition) na implementação do aplicativo, que é basicamente o local em que você deseja adicionar a experiência.

1. Crie uma configuração de canal baseado em código que faça referência a esse local. [Saiba como](code-based-configuration.md#create-code-based-configuration)

1. Crie uma jornada ou campanha no [!DNL Journey Optimizer] usando esta configuração. [Saiba como](create-code-based.md#create-code-based-campaign)

1. Componha uma experiência especificando o conteúdo da configuração selecionada usando o editor de personalização do [!DNL Journey Optimizer]. [Saiba como](create-code-based.md#edit-code)

1. Teste a experiência baseada em código. [Saiba como](test-code-based.md)

1. Publique-a. [Saiba como](publish-code-based.md)

1. Quando a jornada ou campanha de experiência baseada em código estiver ativa, a implementação do aplicativo ou da página que solicita conteúdo para a superfície deverá estar em vigor para que o conteúdo seja recuperado e exibido.

   >[!INFO]
   >
   >Com o objetivo de certificar-se disso, a equipe de implementação do aplicativo faz chamadas explícitas de API ou SDK para buscar conteúdo para a superfície definida na configuração baseada em código, como “Texto do banner” ou “Bandeja de recomendações 1”, ou pontos de decisão não relacionados à interface em um aplicativo, como “parâmetros de algoritmo de pesquisa”. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Saiba mais](code-based-implementation-samples.md)

