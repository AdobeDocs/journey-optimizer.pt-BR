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
TQID: https://experienceleague.adobe.com/YbH8cXjrh5E9v9twpwxB3ENb606W-1JAonJRxnorl9c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: b5cb2dff-e9ba-4e50-a3eb-6a50eef729b8id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: d08afb72-92f6-4856-88e3-11ec34313c2fid: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 89c7799f3d330a0fceb40d55ab3da69fb6c279d8
workflow-type: tm+mt
source-wordcount: 1242
ht-degree: 1%

---

# Adicionar fragmentos visuais a emails {#use-visual-fragments}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como inserir fragmentos visuais reutilizáveis em seus emails, personalizar os campos editáveis e interromper ou manter a herança com o fragmento original.

>[!ENDSHADEBOX]

Um fragmento é um componente reutilizável que pode ser referenciado em um ou mais emails em campanhas, jornadas ou modelos de conteúdo do Journey Optimizer. Essa funcionalidade permite a pré-criação de vários blocos de conteúdo personalizados que podem ser usados por usuários de marketing para reunir rapidamente o conteúdo de email em um processo de design aprimorado. [Saiba como criar e gerenciar fragmentos](../content-management/fragments.md).

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
   * Abra o fragmento em uma nova guia e edite-o, se necessário. [Saiba mais](../content-management/manage-fragments.md#edit-fragments)
   * Explorar referências. [Saiba mais](../content-management/fragments.md#visual-expression)

1. Se necessário, é possível quebrar a herança com o fragmento original. [Saiba mais](#break-inheritance)

   Depois de desbloqueado, você pode personalizar ainda mais o fragmento como qualquer outro componente e usar a guia **[!UICONTROL Estilos]**.

1. Adicione quantos fragmentos desejar e **[!UICONTROL Salve]** suas alterações.

## Gerenciar conteúdo condicional em fragmentos {#fragment-dynamic-content}

Ao trabalhar com fragmentos visuais que contêm conteúdo condicional, siga estas diretrizes. [Saiba mais sobre conteúdo dinâmico](../personalization/dynamic-content.md#emails)

>[!CAUTION]
>
>**Não há suporte para aninhamento de fragmentos com conteúdo condicional.** Não é possível colocar um fragmento com conteúdo condicional dentro de um fragmento desbloqueado que também tenha conteúdo condicional. Essa configuração não suportada pode causar:
>
>* Perda de mapeamentos de variante de conteúdo condicional
>* Avisos sobre o modo de compatibilidade no Email Designer
>* Renderização de email inconsistente

**Estruturar o email corretamente:** Ao usar vários fragmentos com conteúdo condicional, adicione cada fragmento diretamente no próprio bloco de estrutura no nível do email. Evite aninhar fragmentos com conteúdo condicional dentro de outros fragmentos desbloqueados que também contêm conteúdo condicional.

**Planeje com antecedência:** Antes de adicionar fragmentos ao seu email, identifique quais contêm conteúdo condicional e planeje seu layout de acordo. Isso ajuda a evitar problemas de configuração e garante uma estrutura limpa desde o início.

**Crie fragmentos reutilizáveis com cuidado:** Ao criar fragmentos que incluirão conteúdo condicional, considere como eles serão usados. Se um fragmento precisar ser aninhado dentro de outros fragmentos, evite adicionar conteúdo condicional aos fragmentos principal e secundário.

**Solução de problemas:** se você perder mapeamentos de variantes de conteúdo condicional ou avisos de modo de compatibilidade, siga as etapas abaixo.

* Verifique se há fragmentos aninhados com conteúdo condicional na estrutura de email
* Reestruturar movendo cada fragmento com conteúdo condicional para o seu próprio bloco de estrutura no nível do email
* Salve e verifique se as variantes de conteúdo condicional foram restauradas corretamente

## Usar variáveis implícitas {#implicit-variables-in-fragments}

As variáveis implícitas aprimoram a funcionalidade existente do fragmento para melhorar a eficiência na reutilização de conteúdo e nos casos de uso de script. Os fragmentos podem usar variáveis de entrada e criar variáveis de saída utilizáveis no conteúdo da campanha e da jornada.

Saiba como usar variáveis implícitas em [esta seção](../personalization/use-expression-fragments.md#implicit-variables).

## Personalizar campos editáveis {#customize-fields}

Se determinadas partes do fragmento selecionado tiverem se tornado editáveis, você poderá substituir o valor padrão depois de adicionar o fragmento ao conteúdo. [Saiba como tornar um fragmento personalizável](../content-management/customizable-fragments.md)

Para personalizar campos editáveis em um fragmento usado em um email, siga estas etapas.

1. Adicione um fragmento personalizável ao seu conteúdo de email e selecione-o para abrir o painel **[!UICONTROL Fragmento]** no lado direito.

1. Todos os campos editáveis no fragmento são exibidos na guia **[!UICONTROL Configurações]**, nas propriedades do fragmento.

   No exemplo abaixo, a fonte da imagem e o texto alternativo podem ser editados, bem como os campos &quot;Título&quot;/&quot;Subtítulo&quot; e o URL do botão &quot;Mais informações&quot;.

   ![](assets/fragment-editable-fields.png)

1. Passe o mouse sobre qualquer campo editável na tela central. O campo é destacado em verde e um ícone de lápis é exibido ao clicar no texto que ele contém.

   ![](assets/fragment-editable-field-selected.png){width="80%" align="center"}

1. Edite o texto do campo em linha diretamente na tela central do Designer de email.

   >[!NOTE]
   >
   >Para localizar facilmente os campos editáveis no seu conteúdo, você também pode selecioná-los no painel direito, mas só pode editar esses campos na tela central.

1. Para componentes de **[!UICONTROL Texto]**, **[!UICONTROL Botão]** e **[!UICONTROL Html]**, a barra de ferramentas do Designer de Email também dá acesso a opções de formatação de rich text — negrito, itálico, hiperlinks e muito mais.

   ![Opções de formatação de rich text na barra de ferramentas do Designer de email](assets/fragment-editable-fields-rich-text.png)

   >[!TIP]
   >
   >Os fragmentos criados antes da introdução do recurso de edição de rich text têm campos editáveis definidos como modo somente texto por padrão. Para habilitar opções completas de formatação, vá para o editor de fragmentos usando o botão **[!UICONTROL Abrir fragmento]**, clique em **[!UICONTROL Habilitar]** para desbloquear o modo rich-text e **[!UICONTROL Salvar]** o fragmento. [Saiba mais](../content-management/customizable-fragments.md#rich-text-visual)

   ![Aviso de compatibilidade no Email Designer](assets/email-custom-fragment-compatibility.png){width="50%" align="left" zoomable="yes"}

1. Você pode clicar em **[!UICONTROL Simular conteúdo]** para ver como o conteúdo editável e o estilo são renderizados. [Saiba mais sobre a visualização de conteúdo](../content-management/preview-test.md)

>[!CAUTION]
>
>Quando o **rótulo** e a **URL** de um componente de botão se tornam editáveis em um fragmento, os relatórios de rastreamento mostram a URL em vez do rótulo do botão. [Saiba mais sobre o rastreamento](message-tracking.md)

## Interromper herança {#break-inheritance}

Ao editar um fragmento visual, as alterações são sincronizadas. Eles são propagados automaticamente para todos os rascunhos ou jornadas/campanhas ativas e modelos de conteúdo que contêm esse fragmento.

Quando adicionados a um email ou modelo de conteúdo, os fragmentos são sincronizados por padrão. No entanto, é possível quebrar a herança do fragmento original. Nesse caso, o conteúdo do fragmento é copiado para o design atual e as alterações não são mais sincronizadas.

Para interromper a herança, siga as etapas abaixo:

1. Selecione o fragmento.

1. Clique no ícone de desbloqueio na barra de ferramentas contextual.

   ![](assets/fragment-break-inheritance.png)

1. Esse fragmento se torna um elemento independente que não está mais vinculado ao fragmento original. Edite-o como qualquer outro componente de conteúdo em seu conteúdo. [Saiba mais](content-components.md)

### Fragmentos bloqueados {#locked-fragments}

Se o fragmento tiver sido bloqueado pelo autor, o ícone de desbloqueio ficará esmaecido e não poderá ser usado para interromper a herança.

![](assets/fragment-locked.png)

Os fragmentos bloqueados permanecem sincronizados onde quer que apareçam, impedindo edições locais que poderiam quebrar os padrões da marca ou os requisitos de conformidade.

Saiba como bloquear um fragmento em [esta seção](../content-management/create-fragments.md#lock-visual-fragment).

>[!NOTE]
>
>O autor do fragmento pode alterar a configuração posteriormente para usos futuros redefinindo seu comportamento para **[!UICONTROL Permitir que a herança seja interrompida]** nas configurações do fragmento.

