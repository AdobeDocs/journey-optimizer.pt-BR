---
title: Introdução a experiências baseadas em código
description: Saiba mais sobre experiências baseadas em código no Journey Optimizer
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 60c74bcc5e33afa354a2380d3e6f490a4c2c3e6d
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 7%

---

# Introdução ao canal baseado em código {#get-sarted-code-based}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* **[Introdução ao canal baseado em código](get-started-code-based.md)**
* [Pré-requisitos baseados em código](code-based-prerequisites.md)
* [Amostras de implementação baseadas em código](code-based-implementation-samples.md)
* [Criar experiências baseadas em código](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>O canal de experiência baseado em código está disponível no momento como uma versão beta somente para usuários selecionados. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.

[!DNL Journey Optimizer] O permite personalizar e testar as experiências que você deseja entregar aos clientes em todos os seus pontos de contato, como aplicativos web, aplicativos móveis, aplicativos para desktop, consoles de vídeo, dispositivos conectados à TV, TVs inteligentes, quiosques, caixas eletrônicos, assistentes de voz, dispositivos da IoT etc.

Com o **experiência baseada em código** você pode definir experiências de entrada usando um editor não visual simples e intuitivo. Ele permite inserir e editar elementos específicos em locais individuais e mais granulares de seus aplicativos ou páginas da Web, independentemente do tipo de aplicativos que você possui, em vez de aplicar modificações a um conteúdo inteiro.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

Quando você [criar uma campanha](../campaigns/create-campaign.md#configure), selecione **Experiência baseada em código (Beta)** como sua ação e definir configurações básicas.

>[!NOTE]
>
>Se esta for a primeira vez que estiver criando uma experiência online, certifique-se de seguir os pré-requisitos descritos [nesta seção](code-based-prerequisites.md).

<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Cliente potencial" src="../assets/do-not-localize/privacy-audit.jpeg">
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
<a href="code-based-prerequisites.md"><strong>Pré-requisitos</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Pouco frequentes" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Criar uma experiência baseada em código</strong></a>
</div>
<p></td>
<td>
<a href="create-code-based.md#edit-code">
<img alt="Validação" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>Editar seu código</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## Quando usar canais baseados em código em comparação a outros canais {#code-based-vs-other-channels}

### Baseado em código em comparação a outros canais

Quando usar o canal baseado em código em vez do outro [!DNL Journey Optimizer] canais?

* Considere usar experiências baseadas em código a qualquer momento quando sua propriedade digital não for acessada por um navegador da Web ou um aplicativo móvel - casos em que você provavelmente pode usar melhor o [!DNL Journey Optimizer] [canal da web](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} canal.

* Você pode usar o canal baseado em código como uma alternativa para o [!DNL Journey Optimizer] canal da web se o site não puder ser carregado no [editor visual da web](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} que capacita a criação visual para o canal da web.

* Também é possível usar o canal baseado em código como uma alternativa para o [!DNL Journey Optimizer] Canais da Web ou no aplicativo caso você tenha uma implementação baseada em API, headless ou do lado do servidor.

### Canal baseado em código vs. canal da Web

Para executar casos de uso da Web, é possível usar o canal da Web ou a experiência baseada em código, mas, dependendo do contexto, um seria mais apropriado do que o outro. As principais diferenças estão listadas abaixo para que você possa tomar uma decisão informada sobre quando usar o.

**Web**
* Editar seu conteúdo usando o [editor visual](../web/author-web.md){target="_blank"}.
* Você precisa do [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* O canal da Web permite modificar tudo na página e tem uma lista predefinida de ações que podem ser usadas para fazer alterações. [Saiba mais](../web/author-web.md){target="_blank"}
* É fácil de configurar e começar a trabalhar rapidamente.
* É focado no profissional de marketing.

**Experiência baseada em código**
* Editar seu conteúdo usando o [Editor de expressão](create-code-based.md#edit-code).
* A experiência baseada em código requer trabalho de desenvolvimento anterior em sua implementação para garantir que suas superfícies possam interpretar e entregar o conteúdo publicado na borda pelo [!DNL Journey Optimizer] para estas superfícies. [Saiba mais](#surface-definition)
* Requer mais planejamento e pode alterar apenas as coisas que os desenvolvedores especificam. Portanto, é essencial identificar os componentes (banner inicial, imagem principal, barra de menu etc.) nas superfícies que precisam ser modificadas para personalização ou teste e trabalhe com sua equipe de desenvolvimento para criar a implementação necessária para lidar com essas alterações.
* Ela permite usar o conteúdo do código JSON.
* É focado no desenvolvedor-persona.

## Como funciona {#how-it-works}

>[!CAUTION]
>
>Este recurso é para a persona do desenvolvedor e/ou para usuários experientes. Ele pode ser usado por profissionais de marketing com algumas habilidades de escrita de código, desde que as implementações de superfície e a configuração inicial sejam tratadas pela sua equipe de desenvolvimento.

Para editar o conteúdo usando o [!DNL Journey Optimizer] recurso de experiência baseado em código, suas páginas ou aplicativos precisam ser instrumentados. Para fazer isso, você deve declarar antecipadamente os locais individuais específicos (chamados de &quot;[superfícies](#surface-definition)&quot;) onde deseja inserir ou substituir o conteúdo<!--HOW??-->.

>[!NOTE]
>
>Atualmente, o conteúdo associado a uma superfície só pode ser HTML ou JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

As principais etapas para implementar uma campanha baseada em código são as seguintes.

1. Definir um [superfície](#surface-definition), que é basicamente o local em que você deseja adicionar sua experiência baseada em código e criar uma campanha no [!DNL Journey Optimizer] usando essa superfície. [Saiba como](create-code-based.md#create-code-based-campaign)

1. Componha uma experiência especificando o conteúdo da superfície selecionada usando o [!DNL Journey Optimizer] Editor de expressão. [Saiba como](create-code-based.md#edit-code)

1. A equipe de implementação do aplicativo faz chamadas explícitas de API ou SDK para buscar conteúdo para as superfícies nomeadas, como &quot;Texto do banner&quot; ou &quot;Bandeja do Recommendations 1&quot;, ou pontos de decisão não relacionados à interface do usuário em um aplicativo, como &quot;parâmetros de algoritmo de pesquisa&quot;. Nesse caso, a equipe de implementação é responsável pela renderização ou outra forma de interpretar e agir sobre o conteúdo retornado.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## O que é uma superfície? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definir uma superfície de experiência baseada em código"
>abstract="Uma superfície baseada em código é qualquer entidade projetada para interação do usuário ou do sistema, que é exclusivamente identificada por um URI."

A **superfície de experiência baseada em código** é qualquer entidade projetada para interação do usuário ou do sistema<!--ask Robert to explain further-->, que é exclusivamente identificado por um **URI**.

Em outras palavras, uma superfície pode ser vista como um container em qualquer nível de hierarquia com uma entidade (ponto de contato) que existe.<!--good idea to illustrate how it can be seen, but to clarify-->

* Ele pode ser uma página da Web, um aplicativo para dispositivos móveis, um aplicativo de desktop, um local de conteúdo específico em uma entidade maior (por exemplo, um `div`) ou um padrão de exibição fora do padrão (por exemplo, um quiosque ou um banner de aplicativo de desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Ele também pode ser estendido para partes específicas de contêineres de conteúdo para fins de não exibição ou exibição abstrata (por exemplo, blobs JSON fornecidos aos serviços).

* Também pode ser uma superfície curinga que corresponde a várias definições de superfície do cliente (por exemplo, um local de imagem principal em cada página do site pode ser traduzido em um URI de superfície como: web://mydomain.com/*#hero_image).

Basicamente, um URI de superfície é composto por várias seções:
1. **Tipo**: web, mobileapp, serviço, quiosque, tvcd etc.
1. **Propriedade**: domínio ou conjunto de aplicativos
1. **Caminho**: atividade de página/aplicativo ± local na atividade de página/aplicativo <!--to clarify-->

A tabela abaixo lista alguns exemplos de definição de URI de superfície para vários dispositivos.

| Tipo | URI | Descrição |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | Representa um caminho e uma página individuais de um site. |
| Web | web://domain.com/path/page.html#element | Representa um elemento individual em uma página específica de um domínio específico. |
| Web | web://domain.com/*#element | Superfície curinga - representa um elemento individual em cada uma das páginas em um domínio específico. |
| Área de trabalho | desktop://com.vendor.bundle | Representa um aplicativo de área de trabalho específico. |
| Área de trabalho | desktop://com.vendor.bundle#element | Representa um elemento específico em um aplicativo, como um botão, menu, banner principal etc. |
| Aplicativo iOS | ios://com.vendor.bundle | Representa um aplicativo móvel específico para uma única plataforma, neste caso, um aplicativo iOS. |
| Aplicativo iOS | ios://com.vendor.bundle/activity | Representa uma atividade específica (exibição) em um aplicativo móvel. |
| Aplicativo iOS | ios://com.vendor.bundle/activity#element | Representa um elemento específico em uma atividade, como um botão ou outro elemento de exibição. |
| aplicativo Android | android://com.vendor.bundle | Representa um aplicativo móvel específico para uma única plataforma, neste caso, um aplicativo Android. |
| aplicativo tvOS | tvos://com.vendor.bundle | Representa um aplicativo tvOS específico. |
| Aplicativo de TV | tvcd://com.vendor.bundle | Representa um aplicativo de dispositivo específico conectado à TV ou Smart TV - ID do pacote. |
| Serviço de | service://servicename | Representa um processo do lado do servidor ou outra entidade manual. |
| Quiosque | kiosk://location/screen | Exemplo de possíveis tipos de superfície adicionais que podem ser adicionados facilmente. |
| ATM | atm://location/screen | Exemplo de possíveis tipos de superfície adicionais que podem ser adicionados facilmente. |