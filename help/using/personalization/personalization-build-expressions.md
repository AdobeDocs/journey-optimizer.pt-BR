---
solution: Journey Optimizer
product: journey optimizer
title: Sobre o editor de expressão
description: Saiba como trabalhar com o editor de expressão.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 9%

---

# Sobre o editor de expressão {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Sobre o editor de expressão"
>abstract="O editor de expressão permite selecionar, organizar, personalizar e validar todos os dados para criar uma personalização personalizada para o seu conteúdo."

O editor de expressão é a peça central da personalização no [!DNL Journey Optimizer]. Ela está disponível em todos os contextos onde é necessário definir personalização como emails, push e ofertas.

Na interface do editor de expressão, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

![](assets/perso_ee1.png)

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização.

![](assets/perso_ee3.png)

As fontes disponíveis são:

* **[!UICONTROL Atributos do perfil]** : lista todas as referências associadas ao esquema de perfil descrito em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.
* **[!UICONTROL Associações de segmento]** : lista todos os segmentos criados no serviço de Segmentação do Adobe Experience Platform. Mais informações sobre a segmentação disponíveis [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Decisões de oferta]** : lista todas as ofertas associadas a uma disposição específica. Selecione a disposição e insira as ofertas no seu conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../design/deliver-personalized-offers.md).
* **[!UICONTROL Atributos contextuais]** : quando uma atividade de ação de canal (Email, push, SMS) é usada em uma jornada, campos de jornada contextual ficam disponíveis por meio desse menu. Saiba mais [nesta seção](personalization-use-case.md).
* **[!UICONTROL Funções auxiliares]** : lista todas as funções auxiliares disponíveis para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto de personalização. Saiba mais [nesta seção](functions/functions.md).

Clique no botão + para adicionar um atributo ao editor.

>[!NOTE]
>
>O menu de elipse ao lado do ícone &quot;+&quot; permite obter mais detalhes para cada variável e adicionar os atributos usados com mais frequência ao [favoritos](personalization-favorites.md).

![](assets/attribute-details.png)

No exemplo a seguir, o editor de expressão permite selecionar os perfis que fazem aniversário hoje e concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)

Quando a expressão de personalização estiver pronta, será necessário validá-la pelo editor de expressão. Saiba mais [nesta seção](personalization-validation.md).
