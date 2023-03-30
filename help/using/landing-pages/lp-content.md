---
solution: Journey Optimizer
product: journey optimizer
title: Definir o conteúdo específico da página de aterrissagem
description: Saiba como criar conteúdo específico de página de aterrissagem no Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: inicial, página de aterrissagem, criação, página, formulário, componente
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: abf0a3f87baf9aa822e2f4aa5a90777359767541
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Definir o conteúdo específico da página de aterrissagem {#lp-content}

>[!CONTEXTUALHELP]
>id="ac_lp_components"
>title="Usar componentes de conteúdo"
>abstract="Os componentes do conteúdo são espaços reservados vazios para o conteúdo que você pode usar para criar o layout de uma página de aterrissagem. Para definir um conteúdo específico que permitirá aos usuários selecionar e enviar suas opções, use o componente de formulário."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/content-components.html#add-content-components" text="Adicionar componentes de conteúdo"

Para criar o conteúdo da página de aterrissagem, você pode usar os mesmos componentes de um email. [Saiba mais](../email/content-components.md#add-content-components)

Para projetar conteúdo específico que permitirá aos usuários selecionar e enviar suas opções, [usar o componente de formulário](#use-form-component) e defina [estilos específicos da página de aterrissagem](#lp-form-styles).

>[!NOTE]
>
>Você também pode criar uma página de aterrissagem de cliques sem uma **[!UICONTROL Formulário]** componente. Nesse caso, a landing page será exibida para os usuários, mas eles não precisarão enviar nenhum formulário. Isso pode ser útil se você quiser apenas mostrar uma landing page sem exigir qualquer ação dos recipients, como aceitar ou rejeitar, ou se desejar fornecer informações que não exigem entrada do usuário.

Usando o designer de conteúdo da página de aterrissagem, também é possível aproveitar os dados contextuais provenientes da página primária em uma subpágina. [Saiba mais](#use-primary-page-context)

## Usar o componente de formulário {#use-form-component}

>[!CONTEXTUALHELP]
>id="ac_lp_formfield"
>title="Definir os campos do componente de formulário"
>abstract="Defina como os recipients serão vistos e envie suas opções da landing page."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/lp-content.html#lp-form-styles" text="Definir estilos de formulário de landing page"

>[!CONTEXTUALHELP]
>id="ac_lp_submission"
>title="O que acontece ao clicar no botão"
>abstract="Defina o que acontecerá após os usuários enviarem o formulário de landing page."

Para definir um conteúdo específico que permitirá que os usuários selecionem e enviem suas opções a partir da página de aterrissagem, use o **[!UICONTROL Formulário]** componente. Para isso, siga as etapas abaixo.

1. Arraste e solte a página de aterrissagem específica **[!UICONTROL Formulário]** componente da paleta esquerda para o espaço de trabalho principal.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >O **[!UICONTROL Formulário]** só pode ser usado uma vez na mesma página.

1. Selecione-o. O **[!UICONTROL Conteúdo do formulário]** é exibida na paleta direita para permitir a edição dos diferentes campos do formulário.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Alterne para **[!UICONTROL Estilo do formulário]** a qualquer momento para editar os estilos do conteúdo do componente de formulário. [Saiba mais](#define-lp-styles)

1. No **[!UICONTROL Caixa de seleção 1]** , você pode editar o rótulo correspondente a essa caixa de seleção.

1. Defina se essa caixa de seleção deve ser de opt in ou out de usuários: eles concordam em receber comunicações ou pedem para não mais ser contatados?

   ![](assets/lp_designer-form-update.png)

   Selecione entre as três opções abaixo:

   * **[!UICONTROL Aceitar se estiver marcado]**: os usuários precisam marcar a caixa para consentir (aceitar).
   * **[!UICONTROL Rejeitar se marcado]**: os usuários precisam marcar a caixa para remover seu consentimento (opt out).
   * **[!UICONTROL Aceitar se marcado, recusar se desmarcado]**: essa opção permite inserir uma única caixa de seleção para participação/não participação. Os usuários precisam marcar a caixa para consentir (aceitar) e desmarcá-la para remover seu consentimento (recusar).

1. Escolha o que será atualizado entre as três opções a seguir:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Lista de assinaturas]**: Você deve selecionar a lista de subscrição que será atualizada se o perfil marcar essa caixa de seleção. Saiba mais sobre [listas de assinaturas](subscription-list.md).

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Canal (email)]**: A aceitação ou recusa se aplica a todo o canal. Por exemplo, se um perfil que recusa tiver dois endereços de email, ambos os endereços serão excluídos de todas as suas comunicações.

   * **[!UICONTROL Identidade de email]**: A aceitação ou recusa se aplica somente ao endereço de email usado para acessar a landing page. Por exemplo, se um perfil tiver dois endereços de email, somente aquele usado para aceitar receberá comunicações da sua marca.

1. Clique em **[!UICONTROL Adicionar campo]** > **[!UICONTROL Caixa de seleção]** para adicionar outra caixa de seleção. Repita as etapas acima para definir suas propriedades.

   ![](assets/lp_designer-form-checkbox-2.png)

1. Você também pode adicionar uma **[!UICONTROL Campo de texto]**.

   ![](assets/lp_designer-form-add-text-field.png)

   * Insira o **[!UICONTROL Rótulo]** que será exibido na parte superior do campo no formulário.

   * Insira um **[!UICONTROL Espaço reservado]** texto. Ele será exibido dentro do campo antes que o usuário preencha o campo .

   * Verifique a **[!UICONTROL Torne o campo de formulário obrigatório]** , se necessário. Nesse caso, a landing page só poderá ser enviada se o usuário tiver preenchido esse campo. Se um campo obrigatório não for preenchido, uma mensagem de erro será exibida quando o usuário enviar a página.

   ![](assets/lp_designer-form-text-field.png)

1. Depois de adicionar todas as caixas de seleção e/ou campos de texto desejados, clique em **[!UICONTROL Chamada à ação]** para expandir a seção correspondente. Ela permite definir o comportamento do botão na variável **[!UICONTROL Formulário]** componente.

   ![](assets/lp_designer-form-call-to-action.png)

1. Defina o que acontecerá ao clicar no botão :

   * **[!UICONTROL Redirecionar URL]**: Insira o URL da página para a qual os usuários serão redirecionados.
   * **[!UICONTROL Texto de confirmação]**: Digite o texto de confirmação que será exibido.
   * **[!UICONTROL Vincular a uma subpágina]**: Configure um [subpágina](create-lp.md#configure-subpages) e selecione-o na lista suspensa que é exibida.

   ![](assets/lp_designer-form-confirmation-action.png)

1. Defina o que acontecerá ao clicar no botão em caso de erro:

   * **[!UICONTROL Redirecionar URL]**: Insira o URL da página para a qual os usuários serão redirecionados.
   * **[!UICONTROL Texto de erro]**: Digite o texto do erro que será exibido. Você pode visualizar o texto de erro ao definir a variável [estilos de formulário](#define-lp-styles).

   * **[!UICONTROL Vincular a uma subpágina]**: Configure um [subpágina](create-lp.md#configure-subpages) e selecione-o na lista suspensa que é exibida.

   ![](assets/lp_designer-form-error.png)

1. Se desejar fazer atualizações adicionais ao enviar o formulário, selecione **[!UICONTROL Aceitar]** ou **[!UICONTROL Recusar]** e defina se deseja atualizar uma lista de subscrição, o canal ou apenas o endereço de email usado.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Salve o conteúdo e clique na seta ao lado do nome da página para retornar ao [propriedades da página de aterrissagem](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

## Definir estilos de formulário de landing page {#lp-form-styles}

1. Para modificar os estilos do conteúdo do componente de formulário, alterne a qualquer momento para a função **[!UICONTROL Estilo do formulário]** guia .

   ![](assets/lp_designer-form-style.png)

1. Expanda o **[!UICONTROL Caixas de seleção]** para definir a aparência das caixas de seleção e do texto correspondente. Por exemplo, você pode ajustar a família ou o tamanho da fonte e a cor da borda da caixa de seleção.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. Expanda o **[!UICONTROL Botões]** para modificar a aparência do botão no formulário componente. Por exemplo, você pode adicionar uma borda, editar a cor do rótulo ao passar o mouse ou ajustar o alinhamento do botão.

   ![](assets/lp_designer-form-style-buttons.png)

   Você pode visualizar algumas de suas configurações, como a cor do rótulo do botão ao passar o mouse **[!UICONTROL Visualizar]** botão. Saiba mais sobre como testar landing pages [here](create-lp.md#test-landing-page).

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. Expanda o **[!UICONTROL Layout do formulário]** seção para editar as configurações de layout, como cor do plano de fundo, preenchimento ou margem.

   ![](assets/lp_designer-form-style-layout.png)

1. Expanda o **[!UICONTROL Erro de formulário]** para ajustar a exibição da mensagem de erro que é exibida caso ocorra um problema. Marque a opção correspondente para visualizar o texto do erro no formulário.

   ![](assets/lp_designer-form-error-preview.png)

## Usar contexto da página primária {#use-primary-page-context}

Você pode usar dados contextuais provenientes de outra página dentro da mesma landing page.

Por exemplo, se você vincular uma caixa de seleção <!-- or the submission of the page--> para [lista de assinaturas](subscription-list.md) na página de aterrissagem primária, você pode usar essa lista de subscrição na subpágina &quot;thank you&quot;.

Digamos que você vincule duas caixas de seleção na página principal a duas listas de assinatura diferentes. Se um usuário assinar um desses itens, você deseja exibir uma mensagem específica ao enviar o formulário, dependendo da caixa de seleção selecionada.

Para isso, siga as etapas abaixo:

1. Na página primária, vincule cada caixa de seleção do **[!UICONTROL Formulário]** para a lista de subscrição relevante. [Saiba mais](#use-form-component).

   ![](assets/lp_designer-form-luma-newsletter.png)

1. Na subpágina, coloque o ponteiro do mouse onde deseja inserir o texto e selecione **[!UICONTROL Adicionar personalização]** na barra de ferramentas contextual.

   ![](assets/lp_designer-form-subpage-perso.png)

1. No **[!UICONTROL Editar personalização]** janela , selecione **[!UICONTROL Atributos contextuais]** > **[!UICONTROL Páginas de aterrissagem]** > **[!UICONTROL Contexto da página primária]** > **[!UICONTROL Assinatura]**.

1. Todas as listas de assinaturas selecionadas na página principal são listadas. Selecione os itens relevantes usando o ícone + .

   ![](assets/lp_designer-form-add-subscription.png)

1. Adicione as condições relevantes usando as funções auxiliares do Editor de expressão. [Saiba mais](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >Se houver um caractere especial, como um hífen na expressão, você deverá escapar do texto incluindo o hífen.

1. Salve as alterações.

![](assets/lp_designer-form-preview-checked-box.png)

Agora, quando os usuários selecionam uma das caixas de seleção, a mensagem correspondente à caixa de seleção selecionada é exibida ao enviar o formulário.

![](assets/lp_designer-form-thankyou-preview.png)

>[!NOTE]
>
>Se um usuário marcar as duas caixas de seleção, ambos os textos serão exibidos.

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [Expression editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->