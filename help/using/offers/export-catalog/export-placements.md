---
title: Conjunto de dados Disposições
description: Esta seção lista todos os campos usados no conjunto de dados exportado para disposições.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# Conjunto de dados de disposições {#placements-dataset}

Cada vez que uma oferta é modificada, o conjunto de dados gerado automaticamente para disposições é atualizado.

![](../../assets/dataset-placements.png)

O lote bem-sucedido mais recente no conjunto de dados é exibido à direita. A exibição hierárquica do esquema do conjunto de dados é exibida no painel esquerdo.

>[!NOTE]
>
>Saiba como acessar os conjuntos de dados exportados para cada objeto da Biblioteca de ofertas em [this section](../export-catalog/access-dataset.md).

Uma disposição descreve um local ou local em uma mensagem personalizada. É usado para definir restrições técnicas para o conteúdo fornecido pela decisão de personalização. A disposição também representa uma solicitação para produzir certos tipos de métricas quando um evento de experiência é produzido onde essa disposição está envolvida. Por exemplo, a disposição facilita uma imagem clicável personalizada dentro de um email mostrado para um usuário final. A disposição pode, por exemplo, solicitar da experiência montada que o clique em sua imagem seja relatado em um evento de experiência com uma métrica https://ns.adobe.com/xdm/data/metrics/web/linkclicks e uma referência a essa disposição.

Esta é a lista de todos os campos que podem ser usados no conjunto de dados **[!UICONTROL Decision Object Repository - Placements]**.

## Identificador

Um identificador exclusivo para o registro.

Tipo: sequência de caracteres

## _experiência

### decisão

#### Identificador de canal da disposição

O canal no qual a proposta foi feita. O valor é um URI de canal válido. Consulte https://ns.adobe.com/xdm/channels/channel.

Tipo: sequência de caracteres

#### Tipo de componente de conteúdo

Um conjunto enumerado de URIs em que cada valor mapeia para um tipo fornecido ao componente de conteúdo. Alguns consumidores das representações de conteúdo esperam que o valor @type seja uma referência ao schema que descreve propriedades adicionais do componente de conteúdo.

Tipo: sequência de caracteres

#### Tipo de mídia MIME

Uma restrição para o tipo de mídia dos componentes esperados nessa disposição. Pode haver mais de um tipo de mídia possível para um componente, como um formato de imagem diferente.

Tipo: sequência de caracteres

#### Descrição da disposição

Ele é usado para transmitir intenções legíveis humanas sobre como o conteúdo dinâmico é usado na entrega geral de mensagens. Que um determinado espaço é um \&quot;Banner\&quot; em uma página da Web, geralmente é transmitido por meio da descrição e não por um método formal.

Tipo: sequência de caracteres

#### Nome da disposição

Um nome atribuído para o posicionamento para referenciá-lo em interações humanas.

Tipo: sequência de caracteres

## _repo

### ETag de posicionamento

A revisão de que o objeto da opção de decisão estava no momento em que o instantâneo foi tirado.

Tipo: sequência de caracteres
