---
title: Criar emails no Journey Optimizer
description: Saiba como criar o conteúdo de seus emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '1505'
ht-degree: 1%

---

# Projetar o conteúdo de email na interface do usuário {#create-email-content}

Depois de [criou a mensagem](create-message.md), você pode começar a criar o conteúdo do email.

➡️ [Descubra este recurso no vídeo](#video)

1. Na mensagem recém-criada, selecione **[!UICONTROL Email designer]** no **[!UICONTROL Body]** seção.

   ![](assets/import-html_1.png)

1. Na página inicial do Designer de email, escolha como deseja criar o email com as seguintes opções:

   * Selecionar **[!UICONTROL Design from scratch]** para usar os recursos do designer de email para criar seu conteúdo de email. [Saiba mais](#design-scratch)

   * Selecionar **[!UICONTROL Start from template]** para criar seu email a partir de uma lista interna de templates. Observe que não é possível criar outros templates.

   * Selecionar **[!UICONTROL Code your own]** para inserir ou colar o código bruto do HTML. [Saiba mais](existing-content.md#import-raw-html-code).

   * Selecionar **[!UICONTROL Import HTML]** para importar um arquivo HTML ou uma pasta .zip. [Saiba mais](existing-content.md#import-html-content-from-file).

   ![](assets/email_designer_25.png)

## Design do zero {#design-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="Sobre componentes da estrutura"
>abstract="Os componentes da estrutura definem o layout do email."

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="Definição de colunas de email"
>abstract="O Designer de email permite definir facilmente o layout do email definindo a estrutura da coluna."

O Designer de email permite que você defina facilmente a estrutura do seu email. Ao adicionar e mover elementos estruturais com ações simples de arrastar e soltar, você pode projetar a forma do seu email em segundos.

Para começar a criar seu conteúdo de email com o designer de email, siga as etapas abaixo:

1. Depois de selecionar o **[!UICONTROL Design from scratch]** , comece a projetar o conteúdo de email arrastando e soltando **[!UICONTROL Structure components]** para definir o layout do email.

   >[!NOTE]
   >
   >Observe que a pilha de colunas não é compatível com todos os programas de email. Quando não houver suporte, as colunas não serão empilhadas.
   >
   >Depois de colocado no email, não é possível mover nem remover seus componentes, a menos que já exista um componente de conteúdo ou um fragmento inserido dentro dele.

   ![](assets/email_designer_2.png)

1. Adicionar quantos **[!UICONTROL Structure components]** conforme necessário.

   Selecione o **[!UICONTROL n:n column]** para definir o número de colunas de sua escolha (entre 3 e 10). Você também pode definir a largura de cada coluna, movendo as setas na parte inferior de cada coluna.

   >[!NOTE]
   >
   >Cada tamanho de coluna não pode estar abaixo de 10% da largura total do componente de estrutura. Não é possível remover uma coluna que não esteja vazia.

1. No **[!UICONTROL Content components]** , é possível adicionar quantos **[!UICONTROL Content components]** conforme necessário no componente de estrutura. [Saiba mais sobre componentes de conteúdo](content-components.md).

   ![](assets/email_designer_3.png)

1. Cada componente pode ser personalizado ainda mais com a variável **[!UICONTROL Component settings]** seção. Por exemplo, você pode alterar o estilo do texto, o preenchimento ou a margem do componente. [Saiba mais sobre alinhamento e preenchimento](#adjusting-vertical-alignment-and-padding).

   ![](assets/email_designer_4.png)

1. No **[!UICONTROL Assets picker]**, é possível adicionar diretamente ativos armazenados no **[!UICONTROL Assets library]** ao seu email. [Saiba mais sobre o gerenciamento de ativos](assets-essentials.md).

   Clique duas vezes na pasta que continha seus ativos e arraste e solte o ativo que deseja adicionar ao seu email.

   ![](assets/email_designer_5.png)

1. Adicione campos de personalização para personalizar o conteúdo dos dados de perfis. [Saiba mais sobre a personalização de conteúdo](../personalization/personalize.md).

   ![](assets/email_designer_6.png)

1. No **[!UICONTROL Links]** no painel esquerdo, verifique a lista de todos os URLs do seu conteúdo que serão rastreados. Você pode modificar as **[!UICONTROL Tracking Type]**, **[!UICONTROL Label]** e **[!UICONTROL Tags]** se necessário.

   ![](assets/email_designer_7.png)

   >[!NOTE]
   >
   >Saiba mais sobre links e rastreamento de mensagens em [esta página](message-tracking.md).

1. Se necessário, você pode alternar para o editor de código para personalizar ainda mais seu email clicando em **[!UICONTROL Switch to code editor]** no menu avançado. Para obter mais informações sobre o editor de códigos, consulte [esta página](existing-content.md#import-raw-html-code).

   >[!NOTE]
   >
   >Não será possível usar o designer visual para esse email após alternar para o editor de código.

   ![](assets/email_designer_26.png)

1. Clique em **[!UICONTROL Show preview]** para verificar a renderização de email. Você pode escolher a área de trabalho ou exibição móvel.

   Para obter mais informações sobre como visualizar seu email, consulte [esta página](preview.md).

   ![](assets/email_designer_8.png)

1. Quando o email estiver pronto, clique em **[!UICONTROL Save & Close]**.

Seu conteúdo de email agora pode ser usado em uma mensagem. [Saiba como enviar uma mensagem](publish-manage-message.md).

## Criar a versão de texto de um email {#generate-text-version}

É recomendável criar uma versão de texto do corpo do email, que é usada quando o conteúdo do HTML não pode ser exibido.

Por padrão, o Designer de email cria um **[!UICONTROL Plain text]** versão do email, incluindo campos de personalização. Esta versão é gerada e sincronizada automaticamente com a versão HTML do seu conteúdo.

Se preferir usar um conteúdo diferente para a versão de texto sem formatação, siga as etapas abaixo:

1. Em seu email, selecione o **[!UICONTROL Plain text]** guia .

   ![](assets/text_version_3.png)

1. Use o **[!UICONTROL Sync with HTML]** alternar para desativar a sincronização.

   ![](assets/text_version_1.png)

1. Clique na marca de seleção para confirmar sua escolha.

   ![](assets/text_version_2.png)

1. Em seguida, você pode editar a versão de texto simples, conforme desejado.

>[!CAUTION]
>
>* Alterações feitas em **[!UICONTROL Plain text]** não são refletidas na exibição HTML.
>
>* Se você reativar o **[!UICONTROL Sync with HTML]** após atualizar o conteúdo de texto sem formatação, as alterações serão perdidas e substituídas pelo conteúdo de texto gerado pela versão HTML.


## Adicionar um precabeçalho {#preheader}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Adição de um precabeçalho"
>abstract="Um precabeçalho é um texto resumido curto que segue a linha de assunto ao visualizar um email do seu cliente de email. Em muitos casos, ele fornece um breve resumo do email e, normalmente, tem uma frase de duração."

Um precabeçalho é um texto resumido curto que segue a linha de assunto ao visualizar um email do seu cliente de email. Em muitos casos, ele fornece um breve resumo do email e, normalmente, tem uma frase de duração.

>[!NOTE]
>
>Os pré-cabeçalhos não são suportados por todos os clientes de email. Quando não é suportado, o precabeçalho não é exibido.

Para definir o pré-cabeçalho de email, siga as etapas abaixo:

1. No Designer de email, adicione um **[!UICONTROL Structure components]** para começar a criar seu email.

   ![](assets/preheader_1.png)

1. No **[!UICONTROL Body settings]** painel direito, clique em **Editar** ao lado do **[!UICONTROL Preheader]** para adicionar conteúdo.

   ![](assets/preheader_2.png)

1. Adicione o pré-cabeçalho. Você pode personalizá-la ainda mais clicando no botão **[!UICONTROL Add personalization]** ícone .

   ![](assets/preheader_3.png)

1. No **[!UICONTROL Edit Personalization]** , é possível adicionar **[!UICONTROL Content block]**, **[!UICONTROL Dynamic content]** ou **[!UICONTROL Personalization fields]**.

1. Clique em **[!UICONTROL Validate]** para verificar a sintaxe de personalização.

   ![](assets/preheader_4.png)

1. Clique em **[!UICONTROL Save]**.

O pré-cabeçalho agora está configurado para o email.

## Configurações de plano de fundo {#about-backgrounds}

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="Configurações de plano de fundo"
>abstract="Você pode personalizar a cor do plano de fundo ou a imagem do plano de fundo para o seu conteúdo. Observe que a imagem de fundo não é suportada por todos os clientes de email."

Quando se trata de definir planos de fundo com o Email Designer, o Adobe recomenda o seguinte:

1. Aplique uma cor de fundo ao corpo do email, se exigido pelo design.
1. Na maioria dos casos, defina as cores do plano de fundo no nível da coluna.
1. Tente não usar as cores de fundo em componentes de imagem ou texto, pois elas são difíceis de gerenciar.

Abaixo estão as configurações de fundo disponíveis que você pode usar.

* Defina um **[!UICONTROL Background color]** para todo o email. Selecione as configurações de corpo na árvore de navegação acessível na paleta esquerda.

* Defina a mesma cor de plano de fundo para todos os componentes da estrutura selecionando **[!UICONTROL Viewport background color]**. Essa opção permite selecionar uma configuração diferente da cor do plano de fundo.

* Defina uma cor de plano de fundo diferente para cada componente de estrutura. Selecione uma estrutura na árvore de navegação acessível na paleta esquerda para aplicar uma cor de plano de fundo específica somente a essa estrutura.

   Certifique-se de não definir uma cor de plano de fundo da janela de visualização, pois ela pode ocultar as cores de plano de fundo da estrutura.

* Defina um **[!UICONTROL Background image]** para o conteúdo de um componente de estrutura.

   >[!NOTE]
   >
   >Alguns programas de email não suportam imagens de fundo. Quando não houver suporte, a cor de plano de fundo da linha será usada. Certifique-se de selecionar uma cor de plano de fundo de fallback apropriada caso a imagem não possa ser exibida.

* Defina uma cor de plano de fundo no nível da coluna.

   >[!NOTE]
   >
   >Esse é o caso de uso mais comum. O Adobe recomenda configurar as cores de fundo no nível da coluna, pois isso permite mais flexibilidade ao editar todo o conteúdo de email.

   Você também pode definir uma imagem de plano de fundo no nível da coluna, mas isso raramente é usado.

## Ajustar o alinhamento vertical e o preenchimento {#adjusting-vertical-alignment-and-padding}

Neste exemplo, ajustaremos o preenchimento e o alinhamento vertical dentro de um componente de estrutura composto de três colunas.

1. Selecione o componente de estrutura diretamente no email ou usando o **[!UICONTROL Navigation tree]** disponível no menu à esquerda.

   ![](assets/alignment_1.png)

1. Na barra de ferramentas, clique em **[!UICONTROL Select a column]** e escolha aquele que deseja editar. Também é possível selecioná-lo na árvore de estrutura.

   Os parâmetros editáveis para essa coluna são exibidos no **[!UICONTROL Column settings]** menu.

   ![](assets/alignment_2.png)

1. Em **[!UICONTROL Vertical alignment]**, selecione **[!UICONTROL Bottom]**.

   O componente de conteúdo é movido para a parte inferior da coluna.

   ![](assets/alignment_3.png)

1. Em **[!UICONTROL Padding]**, defina o preenchimento superior dentro da coluna. Clique no ícone de bloqueio para interromper a sincronização com o preenchimento inferior.

   Defina o preenchimento à esquerda e à direita para essa coluna.

   ![](assets/alignment_4.png)

1. Continue de forma semelhante para ajustar o alinhamento e o preenchimento das outras colunas.

1. Salve as alterações.

## Definir um estilo para links {#about-styling-links}

É possível sublinhar um link e selecionar sua cor e seu destino no Designer de email.

1. Em um texto **[!UICONTROL Content component]** onde um link é inserido, selecione seu link.

1. No **[!UICONTROL Component settings]** menu, verifique **[!UICONTROL Underline link]** para sublinhar o texto do rótulo de seu link.

   ![](assets/link_1.png)

1. Escolha como seu público será redirecionado com o **[!UICONTROL Target]** lista suspensa:

   * **[!UICONTROL None]**: abre o link no mesmo quadro em que foi clicado (padrão).
   * **[!UICONTROL Blank]**: abre o link em uma nova janela ou guia.
   * **[!UICONTROL Self]**: abre o link no mesmo quadro em que foi clicado.
   * **[!UICONTROL Parent]**: abre o link no quadro principal.
   * **[!UICONTROL Top]**: abre o link no corpo completo da janela.

   ![](assets/link_2.png)

1. Para alterar a cor do link, clique em **[!UICONTROL Link color]**.

   ![](assets/link_3.png)

1. Escolha a cor que você precisa.

1. Salve as alterações.

## Adicionar atributos de estilo em linha {#adding-inline-styling-attributes}

Na interface do Designer de email, ao selecionar um elemento e exibir suas configurações no painel lateral, é possível personalizar os atributos em linha e o valor desse elemento específico.

1. Selecione um elemento no seu conteúdo.
1. No painel lateral, procure a variável **[!UICONTROL Styles Inline]** configurações.

1. Modifique os valores dos atributos existentes ou adicione novos usando o **+** botão. Você pode adicionar qualquer atributo e valor compatível com CSS.

O estilo é aplicado ao elemento selecionado. Se os elementos filho não tiverem atributos de estilo específicos definidos, o estilo do elemento pai será herdado.

## Vídeo tutorial {#video}

Saiba como criar conteúdo de email com o editor de mensagens.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)
