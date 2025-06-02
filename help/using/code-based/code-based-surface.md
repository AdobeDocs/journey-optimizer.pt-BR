---
title: Superfície baseada em código
description: Saiba o que é uma superfície de experiência baseada em código
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 07ec74fb-7fbc-48c6-a8fc-f58f24a60723
source-git-commit: d3f15c09194a50b95107fb84d680606a468f8644
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 50%

---

# Superfícies de experiência baseada em código {#code-based-surface}

## O que é uma superfície? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Adicionar o URI de superfície para seu componente"
>abstract="Se sua implementação não for para Web, iOS ou Android, ou se você precisar direcionar URIs específicos, insira um URI de superfície, que é um identificador exclusivo que direciona para a entidade onde você deseja fornecer sua experiência. Certifique-se de inserir um URI de superfície que corresponda ao usado em sua própria implementação."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Criar uma configuração de experiência baseada em código para outras plataformas"

Uma experiência baseada em código **superfície** é qualquer entidade projetada para interação do usuário ou do sistema, exclusivamente identificada por um [URI](#surface-uri). A superfície é especificada na [implementação do aplicativo](code-based-prerequisites.md#implementation-prerequisites) e deve corresponder à superfície referenciada na [configuração de canal de experiência baseada em código](code-based-configuration.md).

Uma superfície pode ser vista como um container em qualquer nível de hierarquia com uma entidade (ponto de contato) que existe.

* Ela pode ser uma página da Web, um aplicativo móvel, um aplicativo de desktop, um local de conteúdo específico em uma entidade maior (por exemplo, um `div`) ou um modelo de exibição fora do padrão (por exemplo, um quiosque ou um banner de aplicativo de desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Ela também pode se estender para partes específicas de containers de conteúdo para fins de não exibição ou exibição abstrata (por exemplo, blobs JSON fornecidos aos serviços).

* Também pode ser uma superfície curinga que corresponde a várias definições de superfície do cliente (por exemplo, um local de image hero em cada página do site pode ser traduzido em um URI de superfície como: web://mydomain.com/*#hero_image).

>[!NOTE]
>
>Quando você tem várias ações de experiência baseadas em código sendo executadas na mesma superfície, a **[!UICONTROL Pontuação de prioridade]** da campanha ou da jornada determina o que é entregue ao usuário final se ele se qualificar para mais de uma ação. [Saiba mais sobre pontuações de prioridade](../conflict-prioritization/priority-scores.md)

## Identificador de superfície {#surface-uri}

Um **URI de superfície** serve como um identificador preciso direcionado a elementos ou componentes distintos da interface do usuário em um aplicativo. Basicamente, um URI de superfície é composto de várias seções:

1. **Tipo**: web, aplicativo móvel, ATM, quiosque, TVCD, serviço etc.
1. **Propriedade**: URL da página ou pacote de aplicativos
1. **Container**: local na atividade da página/aplicativo

A tabela abaixo lista alguns exemplos de definição de URI de superfície para vários dispositivos.

**Web e dispositivos móveis**

| Tipo | URI | Descrição |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | Representa um elemento individual em uma página específica de um domínio específico, onde um elemento pode ser um rótulo, como nos seguintes exemplos: hero_banner, top_nav, menu, rodapé etc. |
| Aplicativo para iOS | `mobileapp://com.vendor.bundle/activity#element` | Representa um elemento específico em uma atividade do aplicativo nativo, como um botão ou outro elemento de exibição. |
| Aplicativo para Android | `mobileapp://com.vendor.bundle/#element` | Representa um elemento específico em um aplicativo nativo. |

**Outros tipos de dispositivo**

| Tipo | URI | Descrição |
| --------- | ----------- | ------- | 
| Desktop | `desktop://com.vendor.bundle/#element` | Representa um elemento específico em um aplicativo, como um botão, menu, banner hero, etc. |
| Aplicativo de TV | `tvcd://com.vendor.bundle/#element` | Representa um elemento específico de uma Smart TV ou um aplicativo em um dispositivo conectado a uma TV: ID do pacote. |
| Serviço | `service://servicename/#element` | Representa um processo do lado do servidor ou outra entidade manual. |
| Quiosque | `kiosk://location/screen#element` | Exemplo de possíveis tipos de superfície adicionais que podem ser adicionados facilmente. |
| ATM | `atm://location/screen#element` | Exemplo de possíveis tipos de superfície adicionais que podem ser adicionados facilmente. |

**Superfícies curingas**

| Tipo | URI | Descrição |
| --------- | ----------- | ------- | 
| Web com curinga | `wildcard:web://domain.com/*#element` | Superfície curinga: representa um elemento individual em cada uma das páginas em um domínio específico. |
| Web com curinga | `wildcard:web://*domain.com/*#element` | Superfície curinga: representa um elemento individual em cada uma das páginas em todos os domínios que terminam em “domain.com”. |

## Composição do URI {#uri-composition}

No [!DNL Journey Optimizer], o canal de experiência baseado em código oferece suporte a dois tipos de implementações de clientes:

* Com base no [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} para seus sites ou no [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} para seus aplicativos móveis;
* Lado do servidor ou híbrido usando [APIs do AEP Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=pt-BR){target="_blank"}.

>[!NOTE]
>
>Saiba mais sobre os pré-requisitos de implementação em [esta seção](code-based-prerequisites.md#implementation-prerequisites).

Usando experiências baseadas em código, você pode modificar o conteúdo em locais granulares <!--(such as a specific location on a page, or inside a mobile native app)--> que são identificados exclusivamente por [!DNL Journey Optimizer] usando [URIs de superfície](#surface-uri).

Esses URIs de superfície são compostos e manipulados dependendo do método de implementação:

* **SDK da Web/Móvel**: o desenvolvedor da Web/móvel precisa definir esses locais granulares como cadeias de caracteres simples, pois o SDK da Web/Móvel é capaz de compor automaticamente o URI da superfície com base na URL/ID do aplicativo atual e na cadeia de caracteres do local.

* **APIs do Edge Network**: o desenvolvedor do aplicativo/página deve definir URIs de superfície completos que incluam o caminho completo e o local onde o conteúdo será consumido, pois os URIs completos são necessários neste tipo de implementação.

É por isso que, ao criar uma [configuração de canal de experiência baseada em código](code-based-configuration.md), você tem duas maneiras de especificar a superfície de acordo com a plataforma selecionada:

* Para as plataformas **[!UICONTROL Web]**, **[!UICONTROL iOS]** e **[!UICONTROL Android]**, é necessário inserir a **URL/ID do aplicativo** e um **local ou caminho** para compor a superfície. Saiba mais sobre como configurar experiências baseadas em código para plataformas [web](code-based-configuration.md#web) e [móveis](code-based-configuration.md#mobile)

* Se a plataforma for **[!UICONTROL Outro]**, você precisará inserir o **URI da superfície** completo, como nos exemplos [acima](#surface-uri). Saiba mais sobre como configurar experiências baseadas em código para [outras](code-based-configuration.md#other) plataformas
