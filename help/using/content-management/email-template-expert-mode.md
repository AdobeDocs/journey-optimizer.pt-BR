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
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 2240a4bf85d3f5f41a12d128afdc15431dbab75b
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 7%

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

Ao usar o editor avançado do HTML, as seguintes medidas de proteção protegem a compatibilidade do conteúdo e definem expectativas.

* O editor avançado do HTML **não valida** seu código. Ele não verifica erros de sintaxe ou layouts com falha. Revise seu conteúdo cuidadosamente antes de salvar.

* Atualizações futuras do sistema podem substituir as alterações feitas na marcação padrão. **As alterações não podem persistir**.

* A equipe de suporte [!DNL Adobe] do **não pode solucionar ou resolver** problemas causados por código personalizado e alterações manuais. Mantenha um backup do seu conteúdo caso precise reverter.

* Não é possível simular conteúdo na visualização avançada do HTML. Alterne para o modo de exibição de Área de Trabalho para visualizar seu conteúdo.

* Para garantir a compatibilidade do conteúdo, **não é possível salvar** no modo de exibição avançado do HTML. Volte para a exibição da área de trabalho quando estiver pronto para salvar suas alterações.

>[!WARNING]
>
>O editor avançado do HTML no modelo de conteúdo não é o mesmo que **[!UICONTROL Codificar o seu próprio]** modo no Designer de email. No modo [!UICONTROL Codifique o seu próprio], você não pode voltar para o editor visual. Depois de escolher esse caminho, você permanecerá na edição somente de código. O editor avançado do HTML, por outro lado, permite alternar entre a visualização do HTML e a visualização da Área de trabalho (visual) a qualquer momento. [Saiba mais sobre o editor de código](../email/code-content.md)

## Alternar para a visualização avançada do HTML {#switch-to-html-view}

Para abrir o editor avançado do HTML e editar a fonte do modelo, siga estas etapas.

1. Abra ou crie um [modelo de email](../content-management/create-content-templates.md) e abra o [Designer de email](../email/get-started-email-design.md) para editar o conteúdo.

1. Clique no botão **[!UICONTROL HTML]** no canto superior direito da tela.

   ![Local do botão HTML na barra de ferramentas Email Designer](assets/email-template-expert-mode-button.png)

1. Na primeira vez que você abre o editor avançado do HTML, uma mensagem de aviso é exibida. Revise-o com atenção e clique em **[!UICONTROL OK]** para continuar. [Saiba mais](#guardrails)

   ![Caixa de diálogo de aviso ao abrir o editor avançado do HTML pela primeira vez](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >Este aviso aparece somente na primeira vez que você abre o editor avançado do HTML e redefine a cada mês.

1. O editor avançado do HTML é exibido.

   ![Interface avançada do editor do HTML mostrando o código-fonte do modelo de email](assets/email-template-expert-mode.png)

1. Adicione as alterações desejadas ao conteúdo do email.

   >[!WARNING]
   >
   >Insira o código HTML e CSS correto, pois não há um processo de validação de sintaxe e o [!DNL Adobe] não fornece suporte. [Saiba mais](#guardrails)

1. A simulação e o salvamento de conteúdo não estão disponíveis na visualização avançada do HTML por motivos de compatibilidade. Volte para a exibição da área de trabalho para visualizar seu conteúdo e salvar suas alterações.

   ![Retorne ao modo de exibição de Área de Trabalho para salvar suas alterações](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >As edições são preservadas ao alternar entre exibições.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}-->

## Tópicos relacionados

* [Desenvolva seu próprio conteúdo de email](../email/code-content.md)
* [Criar modelos de conteúdo](create-content-templates.md)
* [Introdução ao Designer de email](../email/get-started-email-design.md)

