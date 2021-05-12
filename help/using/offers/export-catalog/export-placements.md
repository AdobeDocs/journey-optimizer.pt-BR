---
title: Conjunto de dados Disposições
description: Esta seção lista todos os campos usados no conjunto de dados exportado para disposições.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 4%

---

# Conjunto de dados de disposições {#placements-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para disposições é atualizado.

![](../../assets/dataset-placements.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A exibição hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [this section](../export-catalog/access-dataset.md).

Esta é a lista de todos os campos que podem ser usados no conjunto de dados **[!UICONTROL Decision Object Repository - Placements]**.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identificador

**Campo:** _id 
**Título:** Identificador 
**Descrição:** Um identificador exclusivo para o registro.
**Tipo:** sequência de caracteres

## _experiência

**Campo:** _experience 
**Type:** object

### decisão

**Campo:** 
**Tipo de decisão:** objeto

#### Identificador de canal da disposição

**Campo:** channelID 
**Título:** Identificador de canal da disposição 
**Descrição:** o canal no qual a proposta foi feita. O valor é um URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.
**Tipo:** sequência de caracteres

#### Tipo de componente de conteúdo

**Campo:** componenteTipo 
**Título:** Tipo de componente de conteúdo 
**Descrição:** um conjunto enumerado de URIs em que cada valor mapeia para um tipo fornecido para o componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.
**Tipo:** sequência de caracteres

#### contentTypes

**Campo:** contentTypes 
**Type:** array

* **Tipo de mídia MIME**

   **Título:** Tipo de mídia MIME
   **Descrição:** Uma restrição para o tipo de mídia dos componentes esperados nessa disposição. Pode haver mais de um tipo de mídia possível para um componente, como um formato de imagem diferente.
   **Tipo:** sequência de caracteres

#### Descrição da disposição

**Campo:** descrição 
**Título:** disposição Descrição 
**Descrição:** É usado para transmitir intenções legíveis humanas sobre como o conteúdo dinâmico é usado no delivery geral de mensagens. Que um determinado espaço é um \&quot;Banner\&quot; em uma página da Web, geralmente é transmitido por meio da descrição e não por um método formal.
**Tipo:** sequência de caracteres

#### Nome da disposição

**Campo:** nome 
**Título:** Nome da disposição 
**Descrição:** um nome atribuído para a disposição que se refere a ela em interações humanas.
**Tipo:** sequência de caracteres

## _repo

**Campo:** _repo 
**Type:** object

### ETag de posicionamento

**Campo:** 
**Título da tag:** Inserção ETag 
**Descrição:** A revisão de que o objeto de opção de decisão estava no momento em que o instantâneo foi tirado.
**Tipo:** sequência de caracteres
