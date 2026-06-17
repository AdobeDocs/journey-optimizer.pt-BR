---
title: Introdução a experiências baseadas em código
description: Saiba mais sobre experiências baseadas em código no Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
TQID: https://experienceleague.adobe.com/ZOCKgdEGK0G3GOhNbwxSXVOQo0We6-QdjzItFtZ5T3E
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f88eedcc-cf3e-46b8-9e94-0293589325f3
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ffb7556c4fef469982c3216fa0fcab2efaec862d
workflow-type: tm+mt
source-wordcount: 986
ht-degree: 96%

---

# Introdução ao canal baseado em código {#get-started-code-based}

>[!BEGINSHADEBOX]

**Nesta página:** Descubra como o canal baseado em código permite que você forneça conteúdo personalizado a locais granulares em seus aplicativos e páginas da Web e quando usá-lo em vez de outros canais.

>[!ENDSHADEBOX]

O [!DNL Journey Optimizer] permite personalizar e testar as experiências que você deseja entregar aos clientes em todos os seus pontos de contato, como aplicativos Web, aplicativos móveis, aplicativos de desktop, consoles de vídeo, dispositivos conectados à TV, smart TVs, quiosques, ATMs, assistentes de voz, dispositivos IoT, etc.

Com o recurso **experiência baseada em código**, é possível definir experiências de entrada usando um editor não visual simples e intuitivo. Isso permite inserir e editar elementos específicos em locais individuais e mais granulares de aplicativos ou páginas da Web, independentemente do tipo de aplicativos que você possui, ao invés de aplicar modificações a um conteúdo inteiro.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Recomendações específicas para experiências baseadas em código são detalhadas [nesta página](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ Um caso de uso de ponta a ponta, que mostra como utilizar experimentos de conteúdo para comparar decisões com o canal de experiência baseado em código, é apresentado [nesta seção](../experience-decisioning/experience-decisioning-uc.md).

## Quando usar canais baseados em código em vez de outros canais {#code-based-vs-other-channels}

### Baseado em código vs. outros canais

Quando usar o canal baseado em código em vez de outros canais do [!DNL Journey Optimizer]?

* Você pode considerar o uso de experiências baseadas em código a qualquer momento quando sua propriedade digital não for acessada por um navegador Web ou por um aplicativo móvel, casos em que provavelmente será melhor usar o [canal Web](../web/get-started-web.md){target="_blank"} do [!DNL Journey Optimizer] ou o canal de [mensagens no aplicativo](../../rp_landing_pages/in-app-landing-page.md){target="_blank"} do [!DNL Journey Optimizer].

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* É possível usar o canal baseado em código como uma alternativa aos canais da Web ou no aplicativo do [!DNL Journey Optimizer], caso tenha uma implementação baseada em API, headless ou do lado do servidor.

* Também é possível usar o canal baseado em código em aplicativos móveis nativos como uma alternativa ao canal no aplicativo se quiser modificar o conteúdo dentro do aplicativo nativo em vez de mostrar modais, pop-ups ou sobreposições.

### Baseado em código vs. canal da Web {#code-based-vs-web}

Para executar casos de uso da Web, é possível usar o canal da web ou a experiência baseada em código, mas, dependendo do contexto, um seria mais apropriado do que o outro. As principais diferenças estão listadas abaixo, para que você possa tomar uma decisão informada sobre o que usar e quando.

**Web**

* Edite o conteúdo usando o editor visual do [designer da web](../web/web-visual-editor.md){target="_blank"} ou o [editor não visual](../web/web-non-visual-editor.md) da web.
* É necessário ter o [SDK da web da Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}, uma implementação do lado do cliente.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* O canal da Web permite modificar tudo na página e tem uma lista predefinida de ações que podem ser usadas para fazer alterações. [Saiba mais](../web/web-visual-editor.md){target="_blank"}
* É fácil de configurar e começar a usar.
* É focado na persona do profissional de marketing.

**Experiência baseada em código**

* Editar o conteúdo usando o [Editor de personalização](create-code-based.md#edit-code).
* É necessário ter o [SDK da web da Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"}, implementação do lado do cliente, ou a [API do servidor da Edge Network da AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=pt-BR){target="_blank"}, implementação do lado do servidor.
* A experiência baseada em código requer trabalho de desenvolvimento anterior em sua implementação para garantir que os aplicativos possam interpretar e entregar o conteúdo publicado na borda pelo [!DNL Journey Optimizer] para estes locais. [Saiba mais](code-based-surface.md)
* Ela requer mais planejamento e pode alterar apenas as coisas que os desenvolvedores especificam. Portanto, é essencial identificar os componentes (banner da página inicial, imagem hero, barra de menu etc.) nos aplicativos que precisam ser modificados para personalização ou teste e trabalhar com a equipe de desenvolvimento na criação da implementação necessária para lidar com essas alterações.
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

1. Crie uma jornada ou campanha no [!DNL Journey Optimizer] usando esta configuração. [Saiba como](create-code-based.md#create-code-based-experience)

1. Componha uma experiência especificando o conteúdo da configuração selecionada usando o editor de personalização do [!DNL Journey Optimizer]. [Saiba como](create-code-based.md#edit-code)

1. Teste a experiência baseada em código. [Saiba como](test-code-based.md)

1. Publique-a. [Saiba como](publish-code-based.md)

1. Quando a jornada ou campanha de experiência baseada em código estiver ativa, a implementação do aplicativo ou da página que solicita conteúdo para a superfície deverá estar em vigor para que o conteúdo seja recuperado e exibido.

   >[!INFO]
   >
   >Com o objetivo de certificar-se disso, a equipe de implementação do aplicativo faz chamadas explícitas de API ou SDK para buscar conteúdo para a superfície definida na configuração baseada em código, como “Texto do banner” ou “Bandeja de recomendações 1”, ou pontos de decisão não relacionados à interface em um aplicativo, como “parâmetros de algoritmo de pesquisa”. <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [Saiba mais](code-based-implementation-samples.md)

## Recursos adicionais

* **[Criar experiências baseadas em código](create-code-based.md)**: saiba como criar e configurar campanhas e jornadas baseadas em código para implementações personalizadas.
* **[Configurar canal baseado em código](code-based-configuration.md)**: defina configurações de experiência baseada em código com configurações apropriadas de superfície e implementação.
* **[Pré-requisitos com base em código](code-based-prerequisites.md)**: entenda os requisitos técnicos e os recursos de desenvolvedor necessários para a implementação.
* **[Testar experiências baseadas em código](test-code-based.md)**: saiba como visualizar e testar experiências baseadas em código antes de publicar.
* **[Amostras de implementação](code-based-implementation-samples.md)**: explore exemplos de código e padrões de implementação para vários casos de uso.
* **[Tutoriais de experiências baseadas em código](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/create-a-code-based-experience-campaign){target="_blank"}**: explore tutoriais em vídeo passo a passo sobre recursos baseados em código e práticas recomendadas.

