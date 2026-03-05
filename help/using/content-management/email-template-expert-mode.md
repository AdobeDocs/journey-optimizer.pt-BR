---
solution: Journey Optimizer
product: journey optimizer
title: Editar modelos de email com o editor avançado do HTML
description: Use o Expert Mode para exibir e editar a origem de conteúdo de email do HTML no editor do WYSIWYG, com controle de sinalizador de recursos, medidas de proteção e validação de salvamento.
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
source-git-commit: 74102069afa519898149de33f890568950571f26
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 5%

---

# Editar modelos de email com o editor avançado do HTML {#email-template-expert-mode}

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

O **editor avançado de HTML** é um modo especialista que permite exibir e editar o código fonte bruto de modelos de conteúdo de email diretamente da interface do Designer de email [!DNL Journey Optimizer].

Esse recurso permite inserir expressões avançadas, como condições, diretamente na origem. Ao voltar para a visualização visual (desktop), o conteúdo é renderizado novamente para que você possa verificar sua aparência e continuar editando em ambas as visualizações.

>[!NOTE]
>
>Esse recurso só está disponível em modelos de conteúdo e para o canal de email.

## Medidas de proteção {#guardrails}

Ao usar o editor avançado do HTML, as seguintes medidas de proteção estão em vigor para proteger a compatibilidade do conteúdo e definir expectativas.

* Atualmente, não há **nenhum processo de validação** no editor avançado do HTML. Erros de sintaxe e layouts quebrados não são verificados. Certifique-se de revisar seu conteúdo cuidadosamente antes de salvar.

* Atualizações futuras do sistema podem reverter alterações feitas na marcação padrão. Esteja ciente de que **suas alterações podem ser substituídas**.

* Problemas causados por código personalizado e alterações manuais **não podem ser solucionados** ou resolvidos pela equipe de suporte do [!DNL Adobe]. Caso precise reverter para uma versão anterior, certifique-se de ter um backup do conteúdo.

* Para garantir a compatibilidade do conteúdo, **não é possível salvar** na exibição avançada do HTML. Quando estiver pronto para salvar as alterações, você deverá voltar para a exibição da Área de Trabalho.

>[!WARNING]
>
>O editor avançado do HTML no modelo de conteúdo não é o mesmo que **[!UICONTROL Codificar o seu próprio]** modo no Designer de email. No modo [!UICONTROL Codifique o seu próprio], você não pode voltar para o editor visual. Depois de escolher esse caminho, você permanecerá na edição somente de código. O editor avançado do HTML, por outro lado, permite alternar entre a visualização do HTML e a visualização da Área de trabalho (visual) a qualquer momento. [Saiba mais sobre o editor de código](../email/code-content.md)

## Alternar para a visualização avançada do HTML {#switch-to-desktop-view}

1. Abra ou crie um [modelo de email](../content-management/create-content-templates.md) e abra o [Designer de email](../email/get-started-email-design.md) para editar o conteúdo.

1. Clique no botão **[!UICONTROL HTML]** no canto superior direito da tela.

   ![](assets/email-template-expert-mode-button.png)

1. Na primeira vez que você abre o editor avançado do HTML, uma mensagem de aviso é exibida. Revise-o com atenção e clique em **[!UICONTROL OK]** para continuar. [Saiba mais](#guardrails)

   >[!NOTE]
   >
   >Este aviso aparece somente na primeira vez que você abre o editor avançado do HTML e redefine a cada mês.

   ![](assets/email-template-expert-mode-warning.png)

1. O editor avançado do HTML é exibido.

   ![](assets/email-template-expert-mode.png)

1. Adicione as alterações desejadas ao conteúdo do email.

   >[!WARNING]
   >
   >Insira o código HTML e CSS correto, pois não há um processo de validação de sintaxe e o [!DNL Adobe] não fornece suporte. [Saiba mais](#guardrails)

1. Salvar não está disponível na visualização avançada do HTML. Volte para o modo de exibição de desktop para salvar as alterações.

   &lt;![](assets/email-template-expert-mode-save.png)

   >[!NOTE]
   >
   >O conteúdo só pode ser salvo na exibição de desktop por motivos de compatibilidade de conteúdo. As edições são preservadas ao alternar entre exibições.
