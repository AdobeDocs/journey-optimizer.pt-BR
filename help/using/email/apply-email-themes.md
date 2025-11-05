---
solution: Journey Optimizer
product: journey optimizer
title: Experiência aprimorada de criação de email
description: Saiba como simplificar a criação de emails com temas e módulos reutilizáveis, garantindo a consistência do design e a eficiência em suas campanhas.
badge: label="Disponibilidade limitada" type="Informative"
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: Temas de email, Módulos, Reutilização, Consistência de marca, Design de email, CSS personalizado, Otimização móvel
exl-id: e81d9634-bbff-44d0-8cd7-e86f85075c06
source-git-commit: 4d12c36391c2546788d49cca6e2468a29fc1e74f
workflow-type: tm+mt
source-wordcount: '1567'
ht-degree: 3%

---

# Aplicar temas ao conteúdo do email {#apply-email-themes}

>[!CONTEXTUALHELP]
>id="ajo_use_theme"
>title="Aplicar um tema ao email"
>abstract="Selecione um tema para o email para aplicar rapidamente um estilo específico que se ajuste à sua marca e design."

>[!AVAILABILITY]
>
>Esse recurso está com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Com temas, os usuários não técnicos têm a capacidade de criar conteúdo reutilizável que se adapta a uma marca e idioma de design específicos, adicionando estilo personalizado sobre os modelos padrão<!-- to achieve brand specific results-->.

Esse recurso permite que os profissionais de marketing aproveitem emails visualmente atraentes e consistentes com a marca de forma mais rápida e com menos esforço, ao mesmo tempo em que fornece opções avançadas de personalização para necessidades de design exclusivas.

## Medidas de proteção e limitações {#themes-guardrails}

* Ao criar um email do zero, você pode optar por começar a criar o conteúdo usando um tema para aplicar rapidamente um estilo específico que se ajuste à sua marca e design.

  Se você escolher o modo Estilo manual, não será possível aplicar temas, a menos que redefina seu email.

* [Fragmentos](../content-management/fragments.md) não são compatíveis entre os modos Usar Temas e Estilo Manual.

   * Para usar um [fragmento](../content-management/fragments.md) em um conteúdo com tema, este fragmento deve ter sido criado por si mesmo, usando temas. [Saiba mais](#leverage-themes-fragment)

   * Ao usar um fragmento em um conteúdo de email, aplique um tema definido para esse fragmento. Deixar de fazer isso pode causar problemas de exibição, especialmente no Outlook 2021 e em versões anteriores. [Saiba mais](#leverage-themes-fragment)

* Se estiver usando um conteúdo criado no HTML, você estará no [modo de compatibilidade](existing-content.md) e não poderá aplicar temas diretamente a esse conteúdo.

   * Para aplicar temas, primeiro salve o conteúdo importado [como um novo modelo](../content-management/create-content-templates.md#save-as-template) e, em seguida, converta este modelo em um conteúdo compatível com temas. Em seguida, você pode usar esse template para criar o conteúdo de email. Saiba como converter um modelo criado com estilo manual [nesta seção](#theme-convertor).

   * Você também pode converter o conteúdo importado do HTML. [Saiba mais](existing-content.md)

  <!--To fully leverage all the capabilities of the Email Designer, including themes, you must either create a new content in Use Themes mode, or convert your imported HTML content. [Learn more](existing-content.md)-->

<!--If you apply a theme to a content using a [fragment](../content-management/fragments.md) created with Manual Styling mode, the rendering may not be optimal.-->

## Criar um tema {#create-and-edit-themes}

Para definir um tema que você pode aproveitar em seu conteúdo de email futuro, siga as etapas abaixo.

1. Para começar, crie um novo [modelo de conteúdo](../content-management/create-content-templates.md).

1. Selecione a opção **[!UICONTROL Criar ou editar temas]**.

   ![](assets/theme-create.png)

1. Selecione um tema do Adobe. Neste exemplo, selecione o **[!UICONTROL Tema padrão]** e clique em **[!UICONTROL Criar]**.

   ![](assets/theme-select.png)

1. Você também pode selecionar um modelo personalizado na guia **[!UICONTROL Meus temas]** e clicar em **[!UICONTROL Editar]** para atualizá-lo.

   ![](assets/theme-edit.png)

1. Na guia **[!UICONTROL Configurações gerais]**, comece a definir seu tema dando a ele um nome específico que corresponda à sua marca. Você pode ajustar a largura padrão do visor para seus emails e também exportar o tema atual para [compartilhá-lo em sandboxes](../configuration/copy-objects-to-sandbox.md).

   <!--![](assets/theme-general-settings.png)-->

1. Use o painel à direita para navegar pelas diferentes guias e atualizar as configurações de design.

   ![](assets/theme-right-pane.png)

1. Na guia **[!UICONTROL Cores]**:

   * Use o botão **[!UICONTROL Editar]** para configurar uma **[!UICONTROL paleta de cores]** com cores padrão para sua marca. Selecione uma **[!UICONTROL Predefinição]** para criar rapidamente um esquema de cores ou ajustar cada cor do seu tema individualmente. Você também pode usar uma combinação de ambos.

     ![](assets/theme-colors.gif)

   * Clique em **[!UICONTROL Adicionar variante]** para criar várias variantes de cores, como o modo claro e escuro, em que cada variante do tema tem sua própria paleta de cores e controles de nuance.

     ![](assets/theme-colors-variant.png)

   * Para cada variante, clique no ícone **[!UICONTROL Editar]** para editar qualquer elemento individual. É possível usar a paleta padrão criada ou qualquer cor personalizada.

     ![](assets/theme-colors-edit-variant.gif)

1. Nas **[!UICONTROL Configurações de texto]**, é possível definir a fonte global que deseja usar para todo o tema. Para um controle mais granular, também é possível editar cada texto de cabeçalho e parágrafo para ajustar a fonte, o tamanho, o estilo e assim por diante.

   ![](assets/theme-text.png)

1. Na guia **[!UICONTROL Espaçamento]**, selecione um elemento individual na lista para espaçá-lo corretamente entre os diferentes componentes.

   <!--![](assets/theme-spacing.png)-->

1. Usando as outras guias à direita, você pode gerenciar separadamente cada elemento de botão, divisor, formatação de imagem adicional e espaçamento do layout de grade para esse tema.

   ![](assets/theme-buttons.png)

1. Clique em **[!UICONTROL Salvar]** para armazenar este tema para uso futuro. Agora ele é exibido na guia **[!UICONTROL Meus temas]**.

<!--A little strange upon hitting Save, because once the theme is created, you need to hit Close to go back to Design your template screen, then click Cancel if you don't want to proceed with template creation.-->

## Aplicar temas a um conteúdo de email {#apply-themes-email}

Para aplicar temas de estilo padrão ou personalizados a um modelo de conteúdo ou a um email, siga as etapas abaixo.

1. Em [!DNL Journey Optimizer], [adicione uma ação de email](create-email.md) a uma jornada ou campanha, ou crie um email [modelo de conteúdo](../content-management/create-content-templates.md#create-template-from-scratch) e [edite o corpo do email](get-started-email-design.md#key-steps).

1. Você pode selecionar uma das seguintes ações:

   * Selecione um [modelo de email](use-email-templates.md) interno para abrir o Designer de email. Um tema padrão específico para cada modelo é aplicado automaticamente.

   * Crie um [novo conteúdo do zero](content-from-scratch.md) e selecione **[!UICONTROL Usar Temas]** para começar com um tema de estilo predefinido.

     ![](assets/theme-from-scratch.png)

     >[!CAUTION]
     >
     >Se você escolher o modo Estilo manual, não será possível aplicar temas, a menos que redefina o design.
     >
     >Para usar um [fragmento](../content-management/fragments.md) em um conteúdo com tema, este fragmento deve ter sido criado por si mesmo, usando temas. [Saiba mais](#leverage-themes-fragment)

1. No Designer de Email, clique no botão **[!UICONTROL Temas]** no painel direito. O tema padrão ou o tema do modelo é exibido. Você pode alternar entre as duas variantes de cor para esse tema.

   ![](assets/theme-default-hero.png)

1. Clique na seta ao lado do tema usado no momento. A lista de temas personalizados e do Adobe disponíveis é exibida.

   ![](assets/theme-hero-change.png)

1. Clique em **[!UICONTROL Meus temas]** e selecione um tema criado.

   ![](assets/theme-select-custom.png)

1. Clique fora da lista suspensa. O tema personalizado recém-selecionado aplica automaticamente seus estilos a todos os componentes de email. É possível alternar entre as variantes de cor, se houver.

1. Quando um tema for selecionado em um modelo de conteúdo, você poderá clicar no botão **[!UICONTROL Editar tema]** para atualizá-lo. [Saiba mais](#create-and-edit-themes)

   ![](assets/theme-edit-in-template.png){width="40%"}

   >[!NOTE]
   >
   >Esta opção não está disponível ao usar temas em conteúdos de email.

1. Se você aproveitar um tema usando várias variantes de cores, poderá escolher uma variante específica para um determinado componente de estrutura. Isso permite definir uma variante de cor para todo o conteúdo e usar uma variante diferente para apenas uma estrutura específica.

   >[!NOTE]
   >
   >Não é possível executar esta ação em componentes de conteúdo.

   Para fazer isso, selecione um componente de estrutura, clique na **[!UICONTROL opção Usar variante de tema específica]** da guia **[!UICONTROL Estilos]** à direita e aplique a variante desejada a essa estrutura.

   ![](assets/theme-structure-variant.png)

   Neste exemplo, a primeira variante de cor do tema atual é aplicada a todo o conteúdo do email, mas a terceira variante de cor é aplicada à estrutura selecionada. É possível ver que as cores do fundo do corpo e do visor para essa estrutura específica são diferentes do restante do conteúdo.

Você pode alternar temas a qualquer momento. O conteúdo do email permanece inalterado, mas os estilos são atualizados para refletir o novo tema.

### Desbloquear estilos {#unlocking-styles}

Quando um componente é selecionado, é possível desbloquear seu estilo usando o ícone dedicado na guia **[!UICONTROL Estilos]**.

![](assets/theme-unlock-style.png){width="90%"}

O tema selecionado ainda é aplicado a esse componente, mas você pode substituir seus elementos de estilo. Se você alterar temas, o novo tema será aplicado somente aos elementos de estilo que não foram substituídos.<!--can you revert this action?-->

Por exemplo, se você desbloquear um componente de texto, poderá alterar <!--the font size from 11 to 14 and -->a cor da fonte de preto para vermelho:

![](assets/theme-unlock-style-ex-white.png){width="80%" align="center" zoomable="yes"}

Se você alterar temas, <!--the font size is still 14 and -->a cor da fonte ainda será vermelha para esse componente, mas a cor do plano de fundo desse componente será alterada com o novo tema:

![](assets/theme-unlock-style-ex-colored.png){width="80%"}

## Aproveitar temas em um fragmento {#leverage-themes-fragment}

Para aproveitar um fragmento em um modelo ou email com [temas aplicados](#apply-themes-email), este fragmento deve ter sido criado por conta própria usando temas. Caso contrário, você não poderá usar esse fragmento no conteúdo temático.

Para criar um fragmento compatível com temas, siga as etapas abaixo.

1. No [!DNL Journey Optimizer], crie um fragmento visual e clique em **[!UICONTROL Criar]** para criar o conteúdo do fragmento. [Saiba como](../content-management/create-fragments.md)

1. Selecione **[!UICONTROL Usar Temas]** para começar com um tema de estilo predefinido.

   ![](assets/fragment-use-themes.png){width="100%"}

   >[!CAUTION]
   >
   >Se você escolher o modo Estilo manual, não será possível aplicar temas, a menos que redefina o design do fragmento.

1. Uma vez no Designer de email, você pode começar a criar o fragmento.

1. Clique no botão **[!UICONTROL Temas]** no painel direito. O tema padrão é exibido. Você pode alternar entre as diferentes variantes de cor para esse tema.

   ![](assets/fragment-default-theme.png){width="100%" align="center" zoomable="yes"}

1. É possível selecionar outros temas para visualizar o conteúdo do fragmento. Para fazer isso, selecione a seta ao lado do tema padrão e clique em **[!UICONTROL Selecionar temas]**.

   ![](assets/fragment-select-themes.png){width="40%"}

1. Você pode navegar entre as guias **[!UICONTROL Temas do Adobe]** e **[!UICONTROL Meus temas]** e selecionar até cinco temas compatíveis (de ambas as guias) para o fragmento.

   ![](assets/fragment-select-compatible-themes.png){width=70%}

   >[!CAUTION]
   >
   >Ao usar o fragmento em um conteúdo de email, [aplique um tema](#apply-themes-email) definido para esse fragmento. Deixar de fazer isso pode causar problemas de exibição, especialmente no Outlook 2021 e em versões anteriores.

1. Clique em **[!UICONTROL Fechar]**.

1. Selecione novamente a seta ao lado do **[!UICONTROL Tema padrão]**. Agora é possível alternar entre os diferentes temas selecionados para visualizar cada renderização de estilo.

   ![](assets/fragment-selected-themes.png){width=90%}

1. Clique em **[!UICONTROL Selecionar temas]** novamente para adicionar mais temas ou alterar sua seleção.

## Tornar um modelo compatível com temas {#theme-convertor}

[!DNL Journey Optimizer] permite converter um modelo que foi criado usando o estilo manual em um conteúdo compatível com tema. Isso pode ser particularmente útil se você criou modelos de conteúdo antes de os temas serem introduzidos no [!DNL Journey Optimizer], ou se você estiver importando conteúdo externo.

1. Abra um [modelo de conteúdo](../content-management/create-content-templates.md) do email e edite o conteúdo usando o Designer de Email.

1. Selecione o ícone **[!UICONTROL Temas]** no painel direito e clique no botão **[!UICONTROL Gerar tema do conteúdo]**.

   ![](assets/generate-theme.png){width=100%}

1. A janela **[!UICONTROL Criar um tema]** é aberta. O [!DNL Journey Optimizer] detecta automaticamente os elementos de estilo e os consolida em um novo tema.

   ![](assets/generate-theme-create-window.png){width=90%}

1. Forneça um nome para o tema.

1. Faça seus próprios ajustes, conforme necessário, da mesma forma que faz ao criar um tema do zero, como adicionar uma variante de cor, editar fontes etc. [Saiba como](#create-and-edit-themes)

   ![](assets/generate-theme-colors.png){width=90%}

1. Clique em **[!UICONTROL Salvar]** para armazenar este novo tema para reutilização. Agora é possível aplicar esse tema ao seu conteúdo, como qualquer outro tema. [Saiba como](#leverage-themes-fragment)