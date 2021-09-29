---
title: Personalizar conteúdo no Journey Optimizer
description: Introdução à personalização
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: c68aa48c7762b6d2d96a7c921025104247ceffa3
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 15%

---

# Introdução à personalização{#add-personalization}

Descubra os recursos de personalização [!DNL Adobe Journey Optimizer] para adaptar suas mensagens a cada recipient específico, aproveitando os dados e as informações que você tem sobre ele. Pode ser seu primeiro nome, seus interesses, onde ele vive, o que ele comprou e muito mais.

➡️ [Saiba como personalizar uma mensagem nestes vídeos](#video-perso)

[!DNL Journey Optimizer] O usa uma sintaxe de personalização  **** simples com base em Handlebars que permite criar expressões com conteúdo delimitado por chaves duplas **{}}**. É possível adicionar várias expressões no mesmo conteúdo ou campo sem restrições. Saiba mais em [Sintaxe de personalização](personalization-syntax.md).

A personalização é baseada nos dados de perfil gerenciados pelo esquema do **Perfil individual XDM** definido na Adobe Experience Platform. Saiba mais na documentação do [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.

>[!CAUTION]
>O schema **Perfil individual XDM** é o único schema que você pode usar para personalizar o conteúdo em [!DNL Journey Optimizer].

**Exemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Ao processar a mensagem (email e push), o Journey Optimizer substitui a expressão pelos dados contidos no banco de dados da Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` torna-se &quot;Olá, John Doe&quot;.


## contextos de personalização{#personalization-areas}

O conteúdo e a exibição de mensagens entregues por [!DNL Journey Optimizer] podem ser personalizados de várias maneiras diferentes.

Em cada campo com o ícone do editor, é possível abrir o editor de personalização (também conhecido como Editor de expressão) e definir a personalização.

![](assets/perso_icon.png)

### Personalize seus emails

Ao criar um email, você pode adicionar personalização no campo **Email subject** da mensagem.

![](assets/perso_subject.png)

No Designer de email, é possível personalizar o conteúdo:

* Na **mensagem**: clique dentro de um bloco de texto, clique no ícone **Personalizar** na barra de ferramentas contextual e selecione **Inserir personalização** campo. Para obter mais informações sobre a interface do Designer de email, consulte esta [seção](../design-emails.md).

   ![](assets/perso_insert.png)

* Para um **link**: selecione algum texto ou imagem dentro de um bloco de texto, clique no ícone **Insert link** na barra de ferramentas contextual. Na janela , é possível adicionar um bloco de personalização clicando no ícone **Add personalization**.

   ![](assets/perso_link.png)

Em ambos os casos, você acessa o editor de personalização.

![](assets/perso_ee.png)

### Personalize suas notificações por push

Você também pode personalizar suas **Notificações por push** nos seguintes campos:

* **Title**
* **Corpo**
* **Som personalizado**
* **Etiquetas**
* **Dados personalizados**

![](assets/perso_push.png)

Saiba mais sobre a configuração de notificação por push em [this section](../push-gs.md).

### Personalize suas ofertas {#personalize-offers}

Também é possível acessar o editor de personalização ao adicionar conteúdo do tipo texto às representações das ofertas.

Saiba mais sobre como gerenciar conteúdo com o Gerenciamento de decisões em [esta seção](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Usar o editor de expressão {#use-expression-editor}

O editor de expressão é a parte central da personalização em [!DNL Journey Optimizer].

Ela está disponível em todos os contextos onde é necessário definir personalização como emails, push e ofertas.

Na interface do editor de expressão, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

![](assets/perso_ee1.png)

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização. As fontes disponíveis são:

* **Perfil** : lista todas as referências associadas ao esquema de perfil descrito na documentação do  [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **Associação**  de segmento: lista todos os segmentos criados no serviço de Segmentação da Adobe Experience Platform. Mais informações sobre a segmentação disponíveis [aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **Ofertas** : lista todas as ofertas associadas a uma disposição específica. Selecione a disposição e insira as ofertas no seu conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../deliver-personalized-offers.md).
* **Contexto** : quando a atividade  **** Messageactivity é usada em uma jornada, os campos de jornada contextual ficam disponíveis nesse menu. Saiba mais [nesta seção](personalization-use-case.md).
* **Funções**  de ajuda: lista todas as funções auxiliares disponíveis para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto de personalização. Saiba mais [nesta seção](functions/functions.md).

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
