---
solution: Journey Optimizer
product: journey optimizer
title: Sobre o editor de expressão
description: Saiba como trabalhar com o editor de expressão.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor, sobre, iniciar
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 15b3b783f0a679e207a104d6333e96c92a02efb1
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 6%

---

# Introdução ao Editor de expressão {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Sobre o editor de expressão"
>abstract="O editor de expressão permite selecionar, organizar, personalizar e validar todos os dados para criar uma personalização personalizada para o seu conteúdo."

O editor de expressão é a peça central da personalização no [!DNL Journey Optimizer]. Ela está disponível em todos os contextos onde é necessário definir personalização como emails, push e ofertas.

Na interface do editor de expressão, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

![](assets/perso_ee1.png)

## Fontes de personalização disponíveis {#sources}

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização. As fontes disponíveis são:

* **[!UICONTROL Atributos do perfil]** : lista todas as referências associadas ao esquema de perfil descrito em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}.
* **[!UICONTROL Associações de segmento]** : lista todos os segmentos criados no serviço de Segmentação do Adobe Experience Platform. Mais informações sobre a segmentação disponíveis [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL Decisões de oferta]** : lista todas as ofertas associadas a uma disposição específica. Selecione a disposição e insira as ofertas no seu conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../email/add-offers-email.md).
* **[!UICONTROL Atributos contextuais]** : quando uma atividade de ação de canal (Email, push, SMS) é usada em uma jornada, campos de jornada contextual ficam disponíveis por meio desse menu. Saiba mais [nesta seção](personalization-use-case.md).
* **[!UICONTROL Funções auxiliares]** : lista todas as funções auxiliares disponíveis para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto de personalização. Saiba mais [nesta seção](functions/functions.md).

## Adicionar atributos de personalização {#add}

Clique no botão + para adicionar um atributo à expressão de personalização.

O menu de reticências ao lado do ícone &quot;+&quot; permite obter mais detalhes para cada variável e adicionar os atributos usados com mais frequência aos favoritos. [Saiba como adicionar atributos a favoritos](personalization-favorites.md)

Além disso, é possível definir o texto de fallback padrão que será exibido se um atributo de perfil do tipo string estiver vazio. Para fazer isso, clique no botão de reticências ao lado do atributo e selecione **[!UICONTROL Inserir com texto de fallback]**. Escreva o texto que deve ser exibido por padrão se o valor do atributo estiver vazio para um perfil e clique em **[!UICONTROL Adicionar]**.

![](assets/attribute-details.png)

No exemplo a seguir, o editor de expressão permite selecionar os perfis que fazem aniversário hoje e concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)

Quando a expressão de personalização estiver pronta, será necessário validá-la pelo editor de expressão. Saiba mais [nesta seção](personalization-validation.md).
