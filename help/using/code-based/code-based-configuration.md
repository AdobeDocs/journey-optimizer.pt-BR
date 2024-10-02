---
title: Configuração baseada em código
description: Criar configuração baseada em código
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 50%

---

# Configurar a experiência baseada em código {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="ID do aplicativo"
>abstract="Forneça a ID do aplicativo para obter precisão no processo de identificação e configuração dentro do ambiente operacional do aplicativo, garantindo integração e funcionalidade perfeitas."

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Localização na página"
>abstract="A localização ou caminho dentro do campo do aplicativo especifica o destino exato dentro do aplicativo que você deseja que os usuários acessem. Pode ser uma seção ou página específica na profundidade da estrutura de navegação do aplicativo."

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="URI de superfície"
>abstract="Um URI de superfície serve como um identificador preciso que direciona para elementos ou componentes distintos da interface de um aplicativo."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="URL padrão de criação e visualização"
>abstract="Este campo garante que as páginas geradas ou encontradas pela regra tenham um URL designado, o que é essencial para criar e visualizar conteúdo com eficiência."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="URL padrão de criação e visualização"
>abstract="Este campo garante que as páginas geradas ou encontradas pela regra tenham um URL designado, o que é essencial para criar e visualizar conteúdo com eficiência."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="Visualizar URL"
>abstract="Esse campo é essencial para habilitar a simulação e a visualização do conteúdo diretamente no dispositivo do aplicativo."

## Criar uma configuração de canais {#reatte-code-based-configuration}

Para criar uma configuração de canal, siga estas etapas:

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/code_config_1.png)

1. Insira um nome e uma descrição (opcional) para a configuração.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

1. Selecione o canal de **experiência baseada em código**.

   ![](assets/code_config_2.png)

1. Selecione a plataforma para a qual a experiência de base de código será aplicada.

1. Para a Web:

   * Especifique uma **[!UICONTROL URL da página]** para aplicar as alterações a uma única página exclusivamente.

   * Ou crie uma **[!UICONTROL Regra de correspondência de páginas]** para direcionar várias URLs que correspondam à regra especificada. Por exemplo, isso pode ser usado para aplicar alterações universalmente em um site, como atualizar um banner principal em todas as páginas ou adicionar uma imagem superior para exibir em cada página de produto. [Saiba mais](../web/web-configuration.md)

1. Para iOS e Android:

   * Insira sua **[!UICONTROL ID do aplicativo]** e seu **[!UICONTROL Local ou caminho dentro do aplicativo]**.

     ![](assets/code_config_3.png){width="500"}

1. Selecione Outros como a plataforma se sua implementação não for para Web, iOS ou Android, ou se precisar direcionar URIs específicos. Ao escolher várias plataformas ou adicionar vários URIs, o conteúdo será entregue a todas as páginas ou aplicativos selecionados.

   * Insira o **[!UICONTROL URI da superfície]**.

   >[!CAUTION]
   >
   >Verifique se o URI de superfície usado em sua campanha baseada em código corresponde ao usado em sua própria implementação. Caso contrário, as alterações não serão aplicadas.

1. Preencha o campo **[!UICONTROL Visualizar URL]** para habilitar visualizações no dispositivo. Esse URL informa ao serviço de visualização o URL específico a ser usado ao acionar uma visualização.

   * Para a Web:

      * Se um único URL de página for inserido, esse URL será usado para a pré-visualização.
      * Se uma regra de correspondência de páginas for selecionada, você deverá inserir um URL de visualização padrão que será usado para visualizar a experiência no navegador.

   * Para plataformas móveis (iOS/Android):

      * O URL de visualização é um deep link configurado pelo desenvolvedor do aplicativo. Isso garante que todos os URLs correspondentes ao esquema de deeplink sejam abertos no aplicativo, em vez de em um navegador móvel da Web. Entre em contato com o desenvolvedor do aplicativo para obter o esquema de deep link configurado para ele.

+++  Os seguintes recursos podem ajudá-lo a configurar deep links para a implementação do seu aplicativo

      * Para o Android:

         * [Criar deep links para o contexto de aplicativos](https://developer.android.com/training/app-links/deep-linking?hl=pt-br)

      * Para o iOS:

         * [Definição de um esquema de URL personalizado para seu aplicativo](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

         * [Suporte a links universais no seu aplicativo](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >Se você encontrar problemas ao visualizar a experiência, consulte [esta documentação](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link).

1. Escolha o formato esperado pelo aplicativo nesse local específico. Isso será usado ao criar a experiência baseada em código em campanhas e jornadas.

1. Envie suas alterações.

Agora é possível selecionar sua configuração ao criar sua experiência baseada em código.


## O que é uma superfície? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definir uma configuração de experiência baseada em código"
>abstract="Uma configuração baseada em código define o caminho e o local dentro do aplicativo, exclusivamente identificados por um URI na implementação do aplicativo, onde o conteúdo será entregue e consumido."

Uma **superfície de experiência baseada em código** é qualquer entidade projetada para interação do usuário ou do sistema, que é exclusivamente identificada por um URI. A superfície é especificada na implementação do aplicativo e deve corresponder à composta na configuração do canal de experiência baseado em código.

Ao criar uma configuração de canal de experiência baseada em código - para plataformas da Web, iOS e Android, é necessário inserir um caminho e um local para compor a superfície, enquanto se a plataforma for Outro, será necessário inserir o URI completo, como nos exemplos abaixo.

Em outras palavras, uma superfície pode ser vista como um container em qualquer nível de hierarquia com uma entidade (ponto de contato) que existe.<!--good idea to illustrate how it can be seen, but to clarify-->

* Ela pode ser uma página da Web, um aplicativo móvel, um aplicativo de desktop, um local de conteúdo específico em uma entidade maior (por exemplo, um `div`) ou um modelo de exibição fora do padrão (por exemplo, um quiosque ou um banner de aplicativo de desktop).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Ela também pode se estender para partes específicas de containers de conteúdo para fins de não exibição ou exibição abstrata (por exemplo, blobs JSON fornecidos aos serviços).

* Também pode ser uma superfície curinga que corresponde a várias definições de superfície do cliente (por exemplo, um local de Hero image em cada página do site pode ser traduzido em um URI de superfície como: web://mydomain.com/*#hero_image).

Basicamente, um URI de superfície é composto por várias seções:
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
