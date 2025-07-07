---
solution: Journey Optimizer
product: journey optimizer
title: Adicionar CSS personalizado ao conteúdo do email
description: Saiba como adicionar CSS personalizado ao seu conteúdo de email diretamente no Designer de email no Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, editor, resumo, email
exl-id: e4645bc7-fb99-4fcc-8d0e-bf8b9efc828e
source-git-commit: edf82b966588a792c660430ced2cfe72c6b88216
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 7%

---

# Adicionar CSS personalizado ao conteúdo do email {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Insira seu próprio CSS"
>abstract="Para maior flexibilidade e controle sobre a aparência do conteúdo, é possível adicionar CSS personalizado diretamente no Designer de email para aplicar estilos avançados e específicos."

Ao criar seus emails, você pode adicionar seu próprio CSS personalizado diretamente no [!DNL Journey Optimizer] [Designer de email](get-started-email-design.md). Esse recurso permite aplicar estilos avançados e específicos para obter mais flexibilidade e controle sobre a aparência do conteúdo.

## Definir CSS personalizado {#define-custom-css}

Para adicionar CSS personalizado ao seu conteúdo de email, siga as etapas abaixo.

1. Verifique se há conteúdo definido no Designer de email adicionando pelo menos um [componente](content-components.md).

1. Selecione **[!UICONTROL Corpo]**, na **[!UICONTROL Árvore de navegação]** à esquerda ou na parte superior do painel direito. A seção **[!UICONTROL Estilos CSS]** é exibida à direita.

   ![Selecione o botão Adicionar CSS personalizado](assets/email-body-css-styles.png){width="85%"}

   >[!NOTE]
   >
   >A seção **[!UICONTROL Estilos CSS]** só está disponível quando o conteúdo já está presente no editor.

1. Clique no botão **[!UICONTROL Adicionar CSS personalizado]**.

   >[!NOTE]
   >
   >O botão **[!UICONTROL Adicionar CSS personalizado]** só está disponível quando **[!UICONTROL Corpo]** é selecionado. No entanto, você pode aplicar estilos CSS personalizados a todos os componentes dentro do conteúdo.

1. Insira seu código CSS na área de texto dedicada que aparece. Verifique se o CSS personalizado é válido e segue a sintaxe apropriada. [Saiba mais](#use-valid-css)

   ![Inserir CSS personalizado na área de texto dedicada](assets/email-body-custom-css.png){width="65%"}

   >[!NOTE]
   >
   >Ao usar um [modelo com conteúdo bloqueado](../content-management/content-locking.md#use), não é possível adicionar CSS personalizado ao seu conteúdo. O rótulo do botão é alterado para **[!UICONTROL Exibir CSS personalizado]** e qualquer CSS personalizado já presente no conteúdo é somente leitura.

1. Salve seu CSS personalizado e verifique se o CSS personalizado foi aplicado corretamente ao conteúdo. Se esse não for o caso, verifique a seção [Solução de problemas](#troubleshooting).

   ![Selecione o botão Adicionar CSS personalizado](assets/email-body-custom-css-applied.png){width="85%"}

1. Se você remover todo o conteúdo, a seção desaparecerá e o CSS personalizado definido anteriormente não será mais aplicado.

1. Adicione conteúdo de volta ao editor para que a seção **[!UICONTROL Estilos CSS]** reapareça. O CSS personalizado é aplicado novamente.

## Assegure o uso de CSS válido {#use-valid-css}

Você pode inserir qualquer string CSS válida na área de texto **[!UICONTROL Adicionar CSS personalizado]**. O CSS adequadamente formatado é aplicado imediatamente ao conteúdo.

>[!CAUTION]
>
>Os usuários são responsáveis pela segurança de seus CSS personalizados. Certifique-se de que o CSS não introduza vulnerabilidades ou conflitos com o conteúdo existente.
>
>Evite usar CSS que possa quebrar involuntariamente o layout ou a funcionalidade do conteúdo.

+++ Exemplos de CSS

Abaixo estão exemplos de CSS válido.

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

+++

+++ Exemplos de CSS inválido

Se um CSS inválido for inserido, uma mensagem de erro será exibida, indicando que o CSS não pode ser salvo. Abaixo estão exemplos de CSS inválido.

O uso de `<style>` tags não é aceito:

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

Sintaxe inválida, como chaves ausentes, não é aceita:

```css
body {
  background: red;
```

+++

## Implementação técnica {#implementation}

Seu CSS personalizado é adicionado ao final da seção `<head>` como parte de uma marca `<style>` com o atributo `data-name="global-custom"`, como no exemplo abaixo. Isso garante que os estilos personalizados sejam aplicados globalmente ao conteúdo.

+++ Ver exemplo

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

+++

O CSS personalizado não é interpretado ou validado pelo painel **[!UICONTROL Configurações]** do Email Designer. Ela é totalmente independente e só pode ser modificada por meio da opção **[!UICONTROL Adicionar CSS personalizado]**.

### Grades de Proteção - Conteúdo importado

Se você quiser usar o CSS personalizado com o conteúdo importado para o Designer de email, considere o seguinte:

* Se você importar conteúdo externo do HTML, incluindo CSS, a menos que converta esse conteúdo, ele estará no **[!UICONTROL Modo de compatibilidade]**, onde a seção **[!UICONTROL Estilos CSS]** não está disponível. [Saiba mais sobre como importar conteúdo existente](existing-content.md)

* Se você estiver importando conteúdo criado com o Designer de email, incluindo CSS aplicado por meio da opção **[!UICONTROL Adicionar CSS personalizado]**, o CSS aplicado anteriormente ficará visível e poderá ser editado pela mesma opção.

<!--
* If importing content created with the Email Designer with CSS applied externally, the CSS code previously applied cannot be accessed within the **[!UICONTROL Add custom CSS]** pop-up window, but you can still override it with new custom CSS.-->

## Solução de problemas {#troubleshooting}

Se o CSS personalizado não for aplicado, considere as opções abaixo.

* Verifique se o CSS é válido e está livre de erros de sintaxe (como chaves ausentes, nomes de propriedades incorretos). [Saiba como](#use-valid-css)

* Verifique se o CSS está sendo adicionado à tag `<style>` com o atributo `data-name="global-custom"`.

* Verifique se a marca de estilo `global-custom` tem o atributo `data-disabled` definido como `true`. Se esse for o caso, o CSS personalizado não será aplicado.

+++ Por exemplo:

  ```html
  <style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>
  ```

+++

* Certifique-se de que seu CSS não seja substituído por outras regras CSS, incluindo qualquer [tema](apply-email-themes.md) aplicado ao seu conteúdo.

   * Use as ferramentas de desenvolvedor do navegador para inspecionar o conteúdo e verificar se o CSS está direcionando os seletores corretos.

   * Considere adicionar `!important` às suas declarações para garantir que elas tenham prioridade.

+++ Por exemplo:

     ```css
     .acr-Form {
       background: red !important;
     }
     ```

+++
