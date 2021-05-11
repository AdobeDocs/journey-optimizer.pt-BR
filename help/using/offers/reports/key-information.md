---
title: Informações-chave sobre eventos do Gerenciamento de decisões
description: Saiba mais sobre as principais informações enviadas com cada evento de Gerenciamento de decisões.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 75%

---

# Informações-chave dos eventos do Gerenciamento de decisões {#events-key-information}

Cada evento enviado quando uma decisão é tomada contém quatro pontos de dados principais que podem ser aproveitados para fins de análise e relatórios.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: nome e ID da oferta substituta, se nenhuma oferta personalizada foi selecionada,
* **[!UICONTROL Placement]**: nome, ID e canal do posicionamento usado para entregar a oferta,
* **[!UICONTROL Selections]**: nome e ID da oferta selecionada para o perfil,
* **[!UICONTROL Activity]**: Nome e ID da decisão (anteriormente conhecida como atividade de oferta).

Além disso, você também pode aproveitar os campos **[!UICONTROL identityMap]** e **[!UICONTROL Timestamp]** para recuperar informações sobre o perfil e a hora em que a oferta foi entregue.

Para obter mais informações sobre todos os campos XDM enviados com cada decisão, consulte [esta seção](xdm-fields.md).
