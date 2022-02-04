---
title: Sobre o Editor de expressão
description: Saiba como trabalhar com o Editor de expressão.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 8%

---

# Sobre o Editor de expressão {#build-personalization-expressions}

O editor de expressão é a peça central da personalização no [!DNL Journey Optimizer]. Ela está disponível em todos os contextos onde é necessário definir personalização como emails, push e ofertas.

Na interface do editor de expressão, você selecionará, organizará, personalizará e validará todos os dados para criar uma personalização personalizada para o seu conteúdo.

![](assets/perso_ee1.png)

A parte esquerda da tela exibe um seletor de domínio que permite selecionar a fonte para personalização.

![](assets/perso_ee3.png)

As fontes disponíveis são:

* **[!UICONTROL Profile attributes]** : lista todas as referências associadas ao esquema de perfil descrito em [Documentação do Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : lista todos os segmentos criados no serviço de Segmentação da Adobe Experience Platform. Mais informações sobre a segmentação disponíveis [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : lista todas as ofertas associadas a uma disposição específica. Selecione a disposição e insira as ofertas no seu conteúdo. Para obter uma documentação completa sobre como gerenciar ofertas, consulte [esta seção](../messages/deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : quando a variável **Mensagem** é usada em uma jornada, campos de jornada contextual estão disponíveis por meio desse menu. Saiba mais [nesta seção](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : lista todas as funções auxiliares disponíveis para executar operações em dados, como cálculos, formatação de dados ou conversões, condições e manipulá-las no contexto de personalização. Saiba mais [nesta seção](functions/functions.md).

Na seleção, a referência é adicionada no editor.

>[!NOTE]
>
>O ícone de informações ao lado do ícone &quot;+&quot; abre uma dica de ferramenta que fornece mais detalhes para cada variável.
>
>Você pode adicionar os atributos usados com mais frequência aos favoritos. Saiba mais [nesta seção](personalization-favorites.md).

No exemplo a seguir, o editor de expressão permite selecionar os perfis que fazem aniversário hoje e concluir a personalização inserindo uma oferta específica correspondente a este dia.

![](assets/perso_ee2.png)

Quando a expressão de personalização estiver pronta, será necessário validá-la pelo Editor de expressão. Saiba mais [nesta seção](personalization-validation.md).
