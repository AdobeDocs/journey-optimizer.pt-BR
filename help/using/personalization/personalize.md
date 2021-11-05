---
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 7be83409f7a594747963c5b125f3bf96c0b4f8b6
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 15%

---

# Introdução à personalização{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] recursos de personalização para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre eles. Pode ser seu primeiro nome, interesses, onde vivem, o que compraram e muito mais.

➡️ [Saiba como personalizar uma mensagem nesses vídeos](#video-perso)

[!DNL Journey Optimizer] usa uma **inline** sintaxe de personalização simples com base em Handlebars, que permite criar expressões com conteúdo delimitado por chaves duplas **{{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Saiba mais em [Sintaxe de personalização](personalization-syntax.md).

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Saiba mais em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

>[!CAUTION]
>O **Perfil individual XDM** schema é o único schema que pode ser usado para personalizar o conteúdo em [!DNL Journey Optimizer].

**Exemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados da Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` torna-se &quot;Olá, John Doe&quot;.


## contextos de personalização{#personalization-areas}

O conteúdo e a exibição das mensagens entregues por [!DNL Journey Optimizer] O pode ser personalizado de várias maneiras diferentes.

Em cada campo com o ícone do editor, é possível abrir o editor de personalização (também conhecido como Editor de expressão) e definir a personalização.

![](assets/perso_icon.png)

### Personalize seus emails

Ao criar um email, você pode adicionar personalização ao **[!UICONTROL Subject line]** campo da mensagem.

![](assets/perso_subject.png)

No Designer de email, é possível personalizar o conteúdo:

* No **message**: clique dentro de um bloco de texto, clique no botão **Personalizar** ícone na barra de ferramentas contextual e selecione **Inserir personalização** campo. Para obter mais informações sobre a interface do Designer de email, consulte esta seção [seção](../design-emails.md).

   ![](assets/perso_insert.png)

* Para um **link**: selecione algum texto ou imagem dentro de um bloco de texto, clique no botão **Inserir link** na barra de ferramentas contextual. Na janela , é possível adicionar um bloco de personalização clicando no botão **Adicionar personalização** ícone .

   ![](assets/perso_link.png)

Em ambos os casos, você acessa o editor de personalização.

![](assets/perso_ee.png)

### Personalize suas notificações por push

Você também pode personalizar seu **Notificações por push** nos seguintes campos:

* **Title**
* **Corpo**
* **Som personalizado**
* **Etiquetas**
* **Dados personalizados**

![](assets/perso_push.png)

Saiba mais sobre a configuração de notificação por push em [esta seção](../push-gs.md).

### Personalize suas ofertas {#personalize-offers}

Também é possível acessar o editor de personalização ao adicionar conteúdo do tipo texto às representações das ofertas.

Saiba mais sobre como gerenciar conteúdo com o Gerenciamento de decisões no [esta seção](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Usar o editor de expressão {#use-expression-editor}

O editor de expressão é a peça central da personalização no [!DNL Journey Optimizer].

Ela está disponível em todos os contextos onde é necessário definir personalização como emails, push e ofertas.

Na interface do editor de expressão, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

![](assets/perso_ee1.png)

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização.

![](assets/perso_ee3.png)

As fontes disponíveis são:

* **[!UICONTROL Profile attributes]** : lista todas as referências associadas ao esquema de perfil descrito em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : lista todos os segmentos criados no serviço de Segmentação da Adobe Experience Platform. Mais informações sobre a segmentação disponíveis [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : lista todas as ofertas associadas a uma disposição específica. Selecione a disposição e insira as ofertas no seu conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : quando a variável **Mensagem** é usada em uma jornada, campos de jornada contextual estão disponíveis por meio desse menu. Saiba mais [nesta seção](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : lista todas as funções auxiliares disponíveis para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto de personalização. Saiba mais [nesta seção](functions/functions.md).

Na seleção, a referência é adicionada no editor.

>[!NOTE]
>
>O ícone de informações ao lado do ícone &quot;+&quot; abre uma dica de ferramenta que fornece mais detalhes para cada variável.

No exemplo a seguir, o editor de expressão permite selecionar os perfis que fazem aniversário hoje e concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)

## Vídeos tutoriais{#video-perso}

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Saiba como usar informações de evento contextual de uma jornada para personalizar uma mensagem.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
