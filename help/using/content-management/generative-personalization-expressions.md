---
solution: Journey Optimizer
product: journey optimizer
title: Assistente de IA para expressões de personalização
description: Saiba como usar o Assistente de IA no Journey Optimizer para gerar expressões de personalização a partir da linguagem natural no Editor do Personalization e como o controle Adicionar expressão funciona no Designer de email.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
feature_v2: []
subfeature_v2: id: d6e0d39b-5df3-4c72-8263-fd834397ee97id: c41e8697-e629-4c38-96b3-564faaa17acf
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 1113
ht-degree: 2%

---

# Assistente de IA para expressões de personalização{#generative-personalization-expressions}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba como usar o Assistente de IA no Adobe Journey Optimizer para gerar, corrigir e explicar expressões de personalização de linguagem natural no Editor do Personalization e no Designer de email.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Antes de começar a usar esse recurso, leia as [Medidas de Proteção e Limitações](gs-generative.md#generative-guardrails) relacionadas.
></br>
>
>Você deve concordar com um [contrato de usuário](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html?lang=pt-BR) antes de usar o Assistente de IA no Journey Optimizer. Para obter mais informações, entre em contato com o(a) representante da Adobe.

## Visão geral {#where-available}

O [!UICONTROL Assistente de IA] ajuda você a gerar uma nova personalização a partir de linguagem simples, explicar o que as expressões existentes fazem e corrigir problemas no código selecionado, de modo que você gaste menos tempo na descoberta de sintaxe e de campos manuais. Você também pode iterar em uma seleção ou solicitar outras alterações na conversa. Ela está disponível de duas maneiras:

* **[!UICONTROL Editor do Personalization]** — onde quer que o editor esteja disponível entre canais (linha de assunto, corpo e outros campos que o abrem). Esse é o caminho geral para a personalização assistida por IA. Para saber onde e como abrir o editor, consulte [Adicionar personalização](../personalization/personalization-build-expressions.md#where).
* **Barra de ferramentas do Designer de email** — ao criar emails no Designer de email, selecione um componente e use **[!UICONTROL Adicionar expressão]** na barra de ferramentas contextual para abrir o assistente em uma caixa de ferramentas sem abrir primeiro o editor completo. Esse ponto de entrada não está disponível fora da criação de email. Consulte [Gerar a partir do Designer de email](#generate-email-designer).

Para obter mais detalhes sobre a configuração e os idiomas do Assistente de IA, consulte [Introdução ao Assistente de IA](gs-generative.md). Para conceitos de personalização, consulte [Introdução à personalização](../personalization/personalize.md). Para ideias de prompt, consulte [Práticas recomendadas de prompt da IA](ai-assistant-prompting-guide.md).

Dependendo do contexto da campanha ou da jornada, o assistente pode trabalhar com dados e construir o [!UICONTROL Personalization Editor] que já está exposto, por exemplo, atributos de perfil, associação de segmento, funções auxiliares e fontes de personalização relacionadas.

>[!NOTE]
>
>O assistente mantém o contexto de seus prompts apenas enquanto o [!UICONTROL Assistente do AI] permanece aberto nessa sessão. Fechar o assistente ou o editor limpa a conversa; na próxima vez que você abrir o assistente, iniciará uma nova conversa.

## Gerar expressões de personalização {#generate}

Essas etapas abordam a geração de expressões de personalização do zero. Para trabalhar com o código já existente no editor, consulte [Editar, corrigir ou explicar o código existente](#edit-existing).

1. Em sua mensagem ou conteúdo, abra o **[!UICONTROL Editor de Personalization]**.

1. Coloque o cursor no editor onde deseja que o código de personalização gerado seja inserido e clique no botão **[!UICONTROL Assistente de IA]**.

   ![](assets/ai-perso-access.png)

1. No campo de texto, descreva a expressão de personalização desejada em linguagem simples, por exemplo, quais atributos de perfil, segmentos ou lógica são necessários, depois clique em **[!UICONTROL Gerar]**.

   Você também pode usar prompts prontos para uso da seção **[!UICONTROL Prompts Rápidos]**, como saudação personalizada, geração de código promocional e muito mais.

   ![](assets/ai-perso-generate.png)

   >[!NOTE]
   >
   >Qualquer prompt ou pergunta não relacionada retorna um erro fora do escopo. Ajuste seu prompt e faça uma pergunta relevante sobre a personalização necessária.

1. Você pode continuar discutindo com o assistente em uma conversa de vários turnos: ela mantém o contexto de seus prompts para que você possa refinar a mesma expressão passo a passo. Para recomeçar, clique no botão **[!UICONTROL Nova sessão]**.

   ![](assets/ai-perso-question.png)

1. Depois de gerar uma expressão, clique em **[!UICONTROL Mostrar visualizações para perfis de amostra]** para ver como a expressão é avaliada em relação ao perfil de amostra sintético **one** e para exibir a carga associada como JSON. A visualização é uma verificação pontual **única** para que você possa ter certeza de que seu código foi resolvido conforme esperado — ela **não** simula vários destinatários, dados variados ou cobertura completa. Os dados de amostra não são salvos ou armazenados em sua organização.

   Se precisar ajustar a amostra (por exemplo, enfatizar atributos diferentes), descreva o que precisa na discussão com o assistente e inclua a palavra-chave **preview** no prompt.

   ![](assets/ai-perso-preview-button.png)

   +++Visualizar exemplo

   ![](assets/ai-perso-preview.png)

   >[!NOTE]
   >
   >Não espere várias linhas de visualização ou cenários exaustivos aqui. O controle está intencionalmente limitado a **um** amostra de avaliação para uma verificação rápida de código, não cobertura parcial em muitos perfis. Solicitar um conjunto de visualizações não realisticamente grande pode fazer com que a solicitação falhe.

   +++

   >[!NOTE]
   >
   >Esse controle é para uma verificação rápida do seu código de personalização no editor, não para uma pré-visualização completa da mensagem do seu conteúdo. Para validação completa da experiência, use o fluxo de simulação normal. [Saiba como visualizar e testar seu conteúdo](../content-management/preview-test.md)

1. Para implementar a saída em sua expressão de personalização, clique em **[!UICONTROL Aplicar]**. A saída do assistente é inserida no local do cursor no editor de personalização. Para substituir o código que já está lá, selecione-o primeiro no editor e use o **[!UICONTROL Editar com o AI Assistant]** (consulte [Editar, corrigir ou explicar o código existente](#edit-existing)).

   Você também pode copiar a saída e colá-la onde for necessário usando o ícone ![Copiar](../orchestrated/assets/do-not-localize/activity-copy.svg).

## Editar, corrigir ou explicar o código existente {#edit-existing}

Você pode selecionar uma expressão de personalização existente e usar o AI Assistant para corrigir problemas de personalização, explicar o que o código faz ou solicitar outras alterações.

1. Selecione o código de personalização existente no editor.

1. Clique com o botão direito do mouse na seleção e escolha **[!UICONTROL Editar com o Assistente de IA]** para que o assistente use sua seleção como contexto.

   ![](assets/ai-perso-right-click.png)

1. O **[!UICONTROL Assistente de IA]** é aberto. Em **[!UICONTROL Comandos Rápidos]**, clique em **[!UICONTROL Explicar]** ou **[!UICONTROL Corrigir]** ou use o campo de texto para solicitar outras alterações e iniciar uma conversa.

   ![](assets/ai-perso-edit.png)

1. Ao usar a **[!UICONTROL Correção]**, clique em **[!UICONTROL Mostrar detalhes da correção]** na discussão para mostrar uma explicação da correção e uma linha por linha antes e depois da visualização.

   ![](assets/ai-perso-fix.png)

1. Como ocorre ao gerar uma expressão de personalização, clique em **[!UICONTROL Aplicar]** para implementar a saída do assistente. Ele substitui o código selecionado no editor de personalização. Por exemplo, se você solicitou uma explicação do código, a aplicação adicionará comentários na expressão que descrevem o que ele faz.

## Gerar na barra de ferramentas do Email Designer {#generate-email-designer}

>[!NOTE]
>
>Esta seção se aplica somente quando você edita o conteúdo do **email** no Designer de email. Para outros canais, use o **[!UICONTROL Personalization Editor]**.

No Designer de Email, você pode usar o [!UICONTROL Assistente de IA para expressões de personalização] da barra de ferramentas contextual sem abrir o [!UICONTROL Editor do Personalization] completo primeiro.

1. No Designer de email, selecione o componente que deseja personalizar e clique no local onde deseja inserir a expressão.

1. Na barra de ferramentas contextual, clique em **[!UICONTROL Adicionar expressão]**.

   ![](assets/ai-perso-add-expression.png)

1. Uma caixa de ferramentas é aberta, onde você pode solicitar a personalização do Assistente de IA. Digite o que você precisa em linguagem simples. O assistente sugere campos de perfil e outros atributos que correspondam ao seu prompt, para que você possa criar a expressão mais rapidamente.

1. O assistente gera a expressão.

   ![](assets/ai-perso-add-expression-insert.png)

   Você pode:

   * Valide a saída da expressão com um valor de exemplo - use a guia **[!UICONTROL Preview]**.
   * Gerar outra sugestão pelo mesmo prompt - usar **[!UICONTROL Regenerar]**.
   * Limpar a discussão e começar novamente - usar **[!UICONTROL Redefinir]**.
   * Refine a expressão no editor completo - clique no ícone ![Editar](assets/do-not-localize/Smock_Edit_18_N.svg "Editar") para abrir o **[!UICONTROL Editor do Personalization]**.

1. Quando estiver satisfeito com o resultado, clique em **[!UICONTROL Inserir]** para adicionar a expressão ao seu conteúdo.
