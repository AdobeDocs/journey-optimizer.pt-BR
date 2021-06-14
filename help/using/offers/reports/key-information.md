---
title: Informações-chave sobre eventos do Gerenciamento de decisão
description: Saiba mais sobre as principais informações enviadas com cada evento de Gerenciamento de decisões.
feature: Ofertas
topic: Integrações
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 91%

---

# Informações-chave sobre eventos do Gerenciamento de decisão {#events-key-information}

Cada evento enviado quando uma decisão é tomada contém quatro pontos de dados principais que podem ser aproveitados para fins de análise e relatórios.

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: nome e ID da oferta substituta, se nenhuma oferta personalizada foi selecionada,
* **[!UICONTROL Placement]**: nome, ID e canal do posicionamento usado para entregar a oferta,
* **[!UICONTROL Selections]**: nome e ID da oferta selecionada para o perfil,
* **[!UICONTROL Activity]**: Nome e ID da decisão (anteriormente conhecida como atividade de oferta).

Além disso, você também pode aproveitar os campos **[!UICONTROL identityMap]** e **[!UICONTROL Timestamp]** para recuperar informações sobre o perfil e a hora em que a oferta foi entregue.

Para obter mais informações sobre todos os campos XDM enviados com cada decisão, consulte [esta seção](xdm-fields.md).
