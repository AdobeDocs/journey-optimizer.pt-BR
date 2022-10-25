---
title: Conjunto de dados de inserções
description: Esta seção lista todos os campos usados no conjunto de dados exportado para disposições
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 5%

---

# Conjunto de dados de inserções {#placements-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para disposições é atualizado.

![](../assets/dataset-placements.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A exibição hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [esta seção](../export-catalog/access-dataset.md).

Esta é a lista de todos os campos que podem ser usados no **[!UICONTROL Repositório de objetos de decisão - disposições]** conjunto de dados.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identificador {#identifier}

**Campo:** _id
**Título:** Identificador
**Descrição:** Um identificador exclusivo para o registro.
**Tipo:** sequência de caracteres

## _experiência {#experience}

**Campo:** _experiência
**Tipo:** objeto

### _experience > decisão

**Campo:** decisão
**Tipo:** objeto

#### _experience > decisioning > Identificador de canal da disposição

**Campo:** channelID
**Título:** Identificador de canal da disposição
**Descrição:** O canal no qual a proposta foi feita. O valor é um URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.
**Tipo:** sequência de caracteres

#### _experience > decisioning > Tipo de componente de conteúdo

**Campo:** componentType
**Título:** Tipo de componente de conteúdo
**Descrição:** Um conjunto enumerado de URIs em que cada valor mapeia para um tipo fornecido ao componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.
**Tipo:** sequência de caracteres

#### _experience > decisioning > contentTypes

**Campo:** contentTypes
**Tipo:** array

**_experience > decisioning > contentTypes > MIME Media Type**

**Título:** Tipo de mídia MIME
**Descrição:** Uma restrição para o tipo de mídia dos componentes esperados nessa disposição. Pode haver mais de um tipo de mídia possível para um componente, como um formato de imagem diferente.
**Tipo:** sequência de caracteres

#### _experience > decisioning > Descrição da disposição

**Campo:** descrição
**Título:** Descrição da disposição
**Descrição:** Ele é usado para transmitir intenções legíveis humanas sobre como o conteúdo dinâmico é usado na entrega geral de mensagens. Que um determinado espaço é um \&quot;Banner\&quot; em uma página da Web, geralmente é transmitido por meio da descrição e não por um método formal.
**Tipo:** sequência de caracteres

#### _experience > decisioning > Nome da disposição

**Campo:** name
**Título:** Nome da disposição
**Descrição:** Um nome atribuído para o posicionamento para referenciá-lo em interações humanas.
**Tipo:** sequência de caracteres

## _repo {#repo}

**Campo:** _repo
**Tipo:** objeto

### _repo > ETag de posicionamento

**Campo:** tag
**Título:** ETag de posicionamento
**Descrição:** A revisão de que o objeto da opção de decisão estava no momento em que o instantâneo foi tirado.
**Tipo:** sequência de caracteres
