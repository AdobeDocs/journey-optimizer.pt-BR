---
title: Usar públicos-alvo de upload personalizados para a tomada de decisão
description: Saiba como aproveitar Públicos de upload personalizados para decisões.
badge: label="Herdados" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: bd950410-691b-49d8-8851-8c6c448c00fd
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 2%

---

# Usar públicos-alvo de upload personalizados para a tomada de decisão {#custom-upload-decisioning}

Com o Journey Optimizer, você pode aproveitar os dados de públicos-alvo criados usando o upload personalizado (arquivo CSV) na Adobe Experience Platform para oferecer suporte aos fluxos de trabalho da Gestão de decisões. Isso é particularmente útil quando os dados não são necessários no perfil, mas ainda são essenciais para fins de decisão.

Os dados de públicos-alvo de upload personalizados podem ser aproveitados na Gestão de decisões para:

1. Critérios de elegibilidade em ofertas e decisões.
2. Personalização de conteúdo em representações de oferta.

Para obter mais informações sobre públicos-alvo de upload personalizado, consulte as seções:
* [Introdução a públicos e Journey Optimizer](../audience/about-audiences.md)
* [Importando uma audiência no Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## Leitura obrigatória {#must-read}

* Esta funcionalidade é suportada somente no **Gerenciamento de decisões**, não na Decisão (anteriormente conhecida como &quot;Experience Decisioning&quot;).
* Ele está disponível exclusivamente por meio de **solicitações de API de Decisão (Hub)** e não é suportado pela **API de Decisão da Edge** ou pela **decisão em lote**.
 

## Usar um público-alvo de upload personalizado como critério de qualificação {#eligibilty}

Você pode usar um público-alvo de upload personalizado como critério de qualificação no nível de oferta ou de decisão. Depois de adicionados, esses critérios podem excluir ofertas ou coleções de ofertas da qualificação. Estes são os vários locais onde você pode aproveitar os públicos-alvo de upload personalizado para refinar as ofertas e a qualificação para decisões:

* Crie uma regra de decisão usando um Público-alvo de upload personalizado:

   1. Ao criar uma regra, acesse a guia **Públicos-alvo** e procure seu público-alvo em CSV na lista. Arraste e solte o público-alvo na tela de regra.
   1. Use a guia **Atributos** e navegue até esquemas de enriquecimento vinculados ao público-alvo selecionado para acessar todos os dados do arquivo CSV e usá-los na regra. Isso permite usar um campo do arquivo CSV para refinar sua regra. [Saiba como criar uma regra de decisão](../offers/offer-library/creating-decision-rules.md)
   1. Salve a regra. Depois que a regra é criada, ela pode ser usada no nível da oferta e no nível da decisão para refinar sua qualificação.

  ![](assets/csv-rule.png)

* Use Públicos-alvo de upload personalizado como restrição de oferta. [Saiba como adicionar restrições a uma oferta](../offers/offer-library/add-constraints.md)

  Ao criar uma oferta, na etapa **Adicionar restrições**, é possível:

   * Usar o público-alvo de upload personalizado para definir a qualificação da oferta,
   * Aplique uma regra aproveitando o público-alvo de upload personalizado.

  ![](assets/csv-offer.png)

* Use Públicos-alvo de upload personalizados no nível de decisão.

  Ao configurar uma decisão, na etapa **Adicionar escopo de decisão**, você pode usar Upload de públicos personalizados como critério de avaliação para uma coleção de ofertas. [Saiba como definir o escopo da decisão](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![](assets/csv-decision.png)

## Usar um público-alvo de upload personalizado para personalizar representações de ofertas

Os públicos de upload personalizados também podem ser usados para personalizar o conteúdo das representações de oferta referenciando dados do arquivo CSV. [Saiba como adicionar representações a uma oferta](../offers/offer-library/add-representations.md)

Para poder aproveitar os atributos de público-alvo de um upload personalizado para personalização, primeiro é necessário adicionar o público-alvo personalizado como uma restrição. Para fazer isso, ao criar uma oferta, na etapa **Adicionar restrições**, adicione o público-alvo como restrições ou selecione uma regra aproveitando o público-alvo de upload personalizado.

![](assets/csv-offer.png)

Depois que o público-alvo é adicionado como uma restrição, você pode usar seus atributos para personalizar o conteúdo de representação. Para fazer isso, acesse a guia **Atributos de perfil** e procure o público-alvo de upload personalizado. Selecione os atributos relevantes do público-alvo para personalizar o conteúdo da oferta.

![](assets/csv-perso.png)
