---
solution: Journey Optimizer
product: journey optimizer
title: Sobre o editor de personalização
description: Saiba como trabalhar com o editor de personalização.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, sobre, iniciar
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 19d33bf2d455aaca3fd0e961bebe5dd1d1f5b32c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 14%

---

# Introdução ao editor de personalização {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Sobre o editor de personalização"
>abstract="O editor de personalização permite selecionar, organizar, personalizar e validar todos os dados para criar um conteúdo personalizado."

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Preenchimento automático"
>abstract="Ativar essa opção permite que o sistema preencha automaticamente o código e faça sugestões enquanto você estiver digitando a expressão. Essa opção está disponível somente para formatos HTML e Texto."

O editor de personalização é a peça central da personalização em [!DNL Journey Optimizer]. Ele está disponível em todos os contextos em que você precisa definir a personalização, como emails, push e ofertas.

Na interface do editor de personalização, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para seu conteúdo.

![](assets/perso_ee1.png)

## Fontes de personalização disponíveis {#sources}

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização. As fontes disponíveis são:

* **[!UICONTROL Atributos do perfil]**: lista todas as referências associadas ao esquema de perfil descrito na [documentação do Modelo de Dados (XDM) do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.
* **[!UICONTROL Públicos-alvo]** : lista todos os públicos-alvo criados no serviço de Segmentação do Adobe Experience Platform. Mais informações sobre segmentação disponíveis [aqui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=pt-BR){target="_blank"}.
* **[!UICONTROL Decisões de oferta]** : lista todas as ofertas associadas a uma disposição específica. Selecione o posicionamento e insira as ofertas no conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Atributos contextuais]**: quando uma atividade de ação de canal (email, push, SMS) é usada em uma jornada ou campanha, os atributos contextuais relacionados a eventos e propriedades ficam disponíveis para personalização. Um exemplo de personalização que utiliza atributos contextuais é apresentado em [esta seção](personalization-use-case.md).
* **[!UICONTROL Funções auxiliares]** : lista todas as funções auxiliares disponíveis para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e as manipula no contexto da personalização. Saiba mais [nesta seção](functions/functions.md).

## Adicionar atributos de personalização {#add}

Clique no botão + para adicionar um atributo à expressão de personalização.

O menu de reticências ao lado do ícone &quot;+&quot; permite obter mais detalhes para cada variável e adicionar os atributos usados com mais frequência aos favoritos. [Saiba como adicionar atributos aos favoritos](personalization-favorites.md)

>[!NOTE]
>
>Se você estiver direcionando um público-alvo com atributos de enriquecimento gerados usando um fluxo de trabalho de composição, poderá aproveitar esses atributos de enriquecimento para personalizar sua mensagem. [Saiba como usar atributos de enriquecimento de públicos-alvo](../audience/about-audiences.md#enrichment)

Além disso, você pode definir um texto de fallback padrão que será exibido se um atributo de perfil do tipo string estiver vazio. Para fazer isso, clique no botão de reticências ao lado do atributo e selecione **[!UICONTROL Inserir com texto alternativo]**. Escreva o texto que deve ser exibido por padrão se o valor do atributo estiver vazio para um perfil e clique em **[!UICONTROL Adicionar]**.

![](assets/attribute-details.png)

No exemplo a seguir, o editor de personalização permite selecionar os perfis que fazem aniversário hoje e, em seguida, concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)

Quando a expressão de personalização estiver pronta, será necessário validá-la pelo editor de personalização. Saiba mais [nesta seção](personalization-validation.md).
