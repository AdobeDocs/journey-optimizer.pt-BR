---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos visuais
description: Saiba como usar fragmentos visuais ao criar emails em campanhas e jornadas do Journey Optimizer
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 2%

---

# Adicionar fragmentos visuais aos emails {#use-visual-fragments}

Um fragmento é um componente reutilizável que pode ser referenciado em um ou mais emails em campanhas, jornadas ou modelos de conteúdo do Journey Optimizer. Essa funcionalidade permite pré-criar vários blocos de conteúdo personalizados que podem ser usados por usuários de marketing para reunir rapidamente o conteúdo de email em um processo de design aprimorado. [Saiba como criar e gerenciar fragmentos](../content-management/fragments.md).

➡️ [Saiba como gerenciar, criar e usar fragmentos neste vídeo](../content-management/fragments.md#video-fragments)

## Usar um fragmento {#use-fragment}

Para usar um fragmento em um email, siga as etapas abaixo.

>[!NOTE]
>
>Você pode adicionar até 30 fragmentos em um determinado delivery. Os fragmentos só podem ser aninhados até um nível.


1. Abra qualquer conteúdo de email ou modelo usando a [Designer de email](get-started-email-design.md).

1. Selecione o ícone **[!UICONTROL Fragmentos]** no painel esquerdo.

   ![](assets/fragments-in-designer.png)

1. A lista de todos os fragmentos visuais criados na sandbox atual é exibida. Eles são classificados por data de criação: os fragmentos visuais adicionados recentemente são mostrados primeiro na lista. É possível:

   * Procure um fragmento específico começando digitando seu rótulo.
   * Classifique os fragmentos em ordem crescente ou decrescente.
   * Altere a forma como os fragmentos são exibidos (cartões ou exibição em lista).
   * Atualize a lista.

   >[!NOTE]
   >
   >Se alguns fragmentos foram modificados ou adicionados enquanto você está editando o conteúdo, a lista será atualizada com as alterações mais recentes.

1. Arraste e solte qualquer fragmento da lista na área em que deseja inseri-lo.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >Você pode adicionar qualquer fragmento do **Rascunho** ou do **Live** ao seu conteúdo. No entanto, você não poderá ativar sua jornada ou campanha se um fragmento com o status Rascunho estiver sendo usado nele. Na publicação do jornada ou da campanha, os fragmentos de rascunho mostrarão um erro e você precisará aprová-los para poder publicar.

1. Como qualquer outro componente, é possível mover o fragmento no conteúdo.

1. Selecione o fragmento para exibir o painel correspondente à direita. Nesse local, você pode excluir o fragmento do seu conteúdo ou duplicá-lo. Também é possível executar essas ações diretamente no menu contextual exibido na parte superior do fragmento.

   ![](assets/fragment-right-pane.png)

1. Na guia **[!UICONTROL Configurações]**, é possível:

   * Escolha os dispositivos nos quais deseja que o fragmento seja exibido.
   * Abra o fragmento em uma nova guia para editá-lo, se necessário. [Saiba mais](../content-management/fragments.md#edit-fragments)
   * Explorar referências. [Saiba mais](../content-management/fragments.md#explore-references)

1. Você pode personalizar ainda mais o fragmento usando a guia **[!UICONTROL Estilos]**.

1. Se necessário, é possível quebrar a herança com o fragmento original. [Saiba mais](#break-inheritance)

1. Adicione quantos fragmentos desejar e **[!UICONTROL Salve]** suas alterações.

## Usar variáveis implícitas {#implicit-variables-in-fragments}

As variáveis implícitas aprimoram a funcionalidade existente do fragmento para melhorar a eficiência na reutilização de conteúdo e nos casos de uso de script. Os fragmentos podem usar variáveis de entrada e criar variáveis de saída utilizáveis no conteúdo da campanha e da jornada.

Saiba como usar variáveis implícitas em [esta seção](../personalization/use-expression-fragments.md#implicit-variables).

## Personalizar campos editáveis {#customize-fields}

Se determinadas partes do fragmento selecionado tiverem se tornado editáveis, você poderá substituir o valor padrão depois de adicionar o fragmento ao conteúdo. [Saiba como tornar seus fragmentos personalizáveis](../content-management/customizable-fragments.md)

Para personalizar campos editáveis em um fragmento, siga estas etapas:

1. Adicione o fragmento ao conteúdo e selecione-o para abrir o painel de propriedades no lado direito.

1. Todos os campos editáveis no fragmento são exibidos na guia **Configurações**, na seção **Fragmento**.

   Campos editáveis são realçados em verde no painel de visualização quando selecionados no painel direito, facilitando a identificação do local no conteúdo.

   No exemplo abaixo, a imagem **origem** e o **texto alternativo** podem ser editados, bem como o botão &quot;Clique aqui&quot; **URL**.

   ![](assets/fragment-editable.png)

## Interromper herança {#break-inheritance}

Ao editar um fragmento visual, as alterações são sincronizadas. Eles são propagados automaticamente para todos os rascunhos ou jornadas/campanhas ativas e modelos de conteúdo que contêm esse fragmento.

Quando adicionados a um email ou modelo de conteúdo, os fragmentos são sincronizados por padrão. No entanto, é possível quebrar a herança do fragmento original. Nesse caso, o conteúdo do fragmento é copiado para o design atual e as alterações não são mais sincronizadas.

Para interromper a herança, siga as etapas abaixo:

1. Selecione o fragmento.

1. Clique no ícone de desbloqueio na barra de ferramentas contextual.

   ![](assets/fragment-break-inheritance.png)

1. Esse fragmento se torna um elemento independente que não está mais vinculado ao fragmento original. Edite-o como qualquer outro componente de conteúdo em seu conteúdo. [Saiba mais](content-components.md)
