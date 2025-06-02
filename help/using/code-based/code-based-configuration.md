---
title: Configuração baseada em código
description: Criar configuração baseada em código
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: d3f15c09194a50b95107fb84d680606a468f8644
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 22%

---

# Configurar a experiência baseada em código {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Definir uma configuração de experiência baseada em código"
>abstract="Uma configuração baseada em código define o caminho e o local dentro do aplicativo, exclusivamente identificados por um URI na implementação do aplicativo, onde o conteúdo será entregue e consumido."

Antes de [criar sua experiência](create-code-based.md), é necessário criar uma configuração de experiência baseada em código na qual você define onde o conteúdo será entregue e consumido dentro do seu aplicativo.

Uma configuração de experiência baseada em código deve fazer referência à superfície, que é basicamente o local em que você deseja renderizar as alterações. De acordo com a plataforma selecionada, você precisa inserir um local/caminho ou o URI de superfície completo. [Saiba mais](code-based-surface.md)

>[!NOTE]
>
>Quando você tem várias ações de experiência baseadas em código usando a mesma configuração de canal (e, portanto, executando na mesma superfície), a **[!UICONTROL Pontuação de prioridade]** da campanha ou da jornada determina o que é entregue ao usuário final se ele se qualificar para mais de uma ação. [Saiba mais sobre pontuações de prioridade](../conflict-prioritization/priority-scores.md)

## Criar uma configuração de experiência baseada em código {#create-code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Indique o local específico dentro da página ou aplicativo"
>abstract="Este campo especifica o destino exato na página ou no aplicativo que você deseja que usuários acessem. Pode ser uma seção específica dentro de uma página da web ou uma página no interior da estrutura de navegação do aplicativo."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="Definir um URL para criação e visualização de conteúdo"
>abstract="Este campo garante que as páginas geradas ou encontradas pela regra tenham um URL designado, o que é essencial para criar e visualizar conteúdo com eficiência."

Para criar uma configuração de canal de experiência baseada em código, siga estas etapas:

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/code_config_1.png)

1. Insira um nome e uma descrição (opcional) para a configuração.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar os caracteres de sublinhado `_`, ponto `.` e hífen `-`.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md)

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

1. Selecione o canal de **experiência baseada em código**.

   ![](assets/code_config_2.png)

1. Selecione a plataforma para a qual a experiência de base de código será aplicada:

   * [Web](#web)
   * [iOS e/ou Android](#mobile)
   * [Outras](#other)

   >[!NOTE]
   >
   >Você pode selecionar várias plataformas. Ao escolher várias plataformas, o conteúdo é entregue a todas as páginas ou aplicativos selecionados.

1. Escolha o formato esperado pelo aplicativo para este local específico. Isso será usado ao criar a experiência baseada em código em campanhas e jornadas.

   ![](assets/code_config_4.png)

1. Clique em **[!UICONTROL Enviar]** para salvar suas alterações.

Agora você pode selecionar essa configuração ao [criar uma experiência baseada em código](create-code-based.md) em suas campanhas e jornadas.

>[!NOTE]
>
>A equipe de implementação do aplicativo é responsável por fazer chamadas explícitas à API ou ao SDK para buscar conteúdo para as superfícies definidas na configuração de experiência baseada em código selecionada. Saiba mais sobre as diferentes implementações de clientes em [esta seção](code-based-implementation-samples.md).

### Plataformas da Web {#web}

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="Definir um URL para criação e visualização de conteúdo"
>abstract="Este campo garante que as páginas geradas ou encontradas pela regra tenham um URL designado, o que é essencial para criar e visualizar conteúdo com eficiência."

Para definir as configurações de experiência baseada em código para plataformas da Web, siga as etapas abaixo.

1. Selecione uma das seguintes opções:

   * **[!UICONTROL Página única]** - Se quiser aplicar as alterações a uma única página exclusivamente, insira uma **[!UICONTROL URL da página]**.

     ![](assets/code_config_single_page.png)

   * **[!UICONTROL Regra de correspondência de páginas]** - Para direcionar várias URLs correspondentes à mesma regra, crie uma ou mais regras. [Saiba mais](../web/web-configuration.md#web-page-matching-rule)

     <!--This could be used to apply changes universally across a website, such as updating a hero banner across all pages or adding a top image to display on every product page.-->

     Por exemplo, se você deseja editar elementos que são exibidos em todas as páginas de produtos femininas do seu site Luma, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Começa com]** > `luma` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `women`.

     ![](assets/code_config_matching_rules.png)

1. O seguinte se aplica ao URL de visualização:

   * Se um único URL de página for inserido, esse URL será usado para a pré-visualização, sem a necessidade de inserir outro URL.
   * Se uma [regra de correspondência de páginas](../web/web-configuration.md#web-page-matching-rule) for selecionada, você deverá inserir uma **[!UICONTROL URL de criação e visualização padrão]** que será usada para visualizar a experiência em um navegador. [Saiba mais](test-code-based.md#preview-on-device)

     ![](assets/code_config_matching_rules_preview.png)

1. O campo **[!UICONTROL Local na página]** especifica o destino exato dentro da página que você deseja que os usuários acessem. Pode ser uma seção específica em uma página na estrutura de navegação do site, como &quot;banner principal&quot; ou &quot;painel do produto&quot;.

   >[!CAUTION]
   >
   >A cadeia de caracteres ou o caminho inserido neste campo deve corresponder ao declarado na implementação do aplicativo ou da página. Isso garante que o conteúdo seja entregue no local desejado dentro do aplicativo ou página especificada. [Saiba mais](code-based-surface.md#uri-composition)

   ![](assets/code_config_location_on_page.png)

### Plataformas para dispositivos móveis (iOS e Android) {#mobile}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="Forneça a ID do aplicativo"
>abstract="Forneça a ID do aplicativo para uma identificação e configuração precisas no ambiente operacional do aplicativo, garantindo integração e funcionalidade perfeitas."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="Inserir o URL para visualizar o conteúdo"
>abstract="Esse campo é essencial para habilitar a simulação e a visualização do conteúdo diretamente no dispositivo do aplicativo."

Para definir as configurações de experiência baseada em código para plataformas móveis, siga as etapas abaixo.

1. Insira sua **[!UICONTROL ID do aplicativo]**. Isso permite a identificação e a configuração precisas no ambiente operacional do aplicativo e garante integração e funcionalidade perfeitas.

1. Forneça o **[!UICONTROL Local ou caminho dentro do aplicativo]**. Este campo especifica o destino exato no aplicativo que você deseja que os usuários acessem. Pode ser uma seção ou página específica na profundidade da estrutura de navegação do aplicativo, como &quot;banner principal&quot; ou &quot;painel do produto&quot;.

   ![](assets/code_config_3.png)

1. Preencha o campo **[!UICONTROL Visualizar URL]** para habilitar visualizações no dispositivo. Esse URL informa ao serviço de visualização o URL específico a ser usado ao acionar a visualização no dispositivo. [Saiba mais](test-code-based.md#preview-on-device)

   O URL de visualização é um deep link configurado pelo desenvolvedor do aplicativo. Isso garante que todos os URLs correspondentes ao esquema de deep link sejam abertos no aplicativo, em vez de em um navegador móvel da Web. Entre em contato com o desenvolvedor do aplicativo para obter o esquema de deep link configurado para ele.

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

### Outras plataformas {#other}

Para definir as configurações de experiência baseadas em código para outras plataformas (como consoles de vídeo, dispositivos conectados à TV, TVs inteligentes, quiosques, ATMs, assistentes de voz, dispositivos de IoT etc.), siga as etapas abaixo.

1. Selecione **[!UICONTROL Outros]** como a plataforma se sua implementação não for para Web, iOS ou Android, ou se você precisar direcionar URIs específicos.

1. Insira o **[!UICONTROL URI da superfície]**. Um URI de superfície é um identificador exclusivo que corresponde à entidade em que você deseja fornecer sua experiência. [Saiba mais](code-based-surface.md#surface-uri)

   ![](assets/code_config_5.png)

   >[!CAUTION]
   >
   >Insira um URI de superfície que corresponda ao usado em sua própria implementação. Caso contrário, as alterações não poderão ser entregues. [Saiba mais](code-based-surface.md#uri-composition)

1. **[!UICONTROL Adicione outro URI de superfície]**, se necessário. Você pode adicionar até 10 URIs.

   >[!NOTE]
   >
   >Ao adicionar vários URIs, o conteúdo é entregue a todos os componentes listados.
