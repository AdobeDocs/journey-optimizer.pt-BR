---
title: Introdução aos conjuntos de dados
description: Saiba como usar conjuntos de dados do Adobe Experience Platform no Adobe Journey Optimizer
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 11%

---

# Introdução aos conjuntos de dados {#datasets-gs}

Todos os dados assimilados no Adobe Experience Platform são mantidos no Data Lake como conjuntos de dados. Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas).

## Acessar conjuntos de dados{#access-datasets}

O **Conjuntos de dados** espaço de trabalho em [!DNL Adobe Journey Optimizer] a interface do usuário permite explorar dados e criar conjuntos de dados.

Selecionar **Conjuntos de dados** na navegação à esquerda para abrir o painel Conjuntos de dados .

![](assets/datasets-home.png)

Adicionar dados ao Adobe Experience Platform é a base para a criação de um Perfil. Você poderá aproveitar os perfis no [!DNL Adobe Journey Optimizer]. Primeiro, defina esquemas, use ferramentas de ETL para preparar e padronizar seus dados e, em seguida, crie conjuntos de dados com base em seus esquemas.

Selecione o **Procurar** para exibir a lista de todos os conjuntos de dados disponíveis para sua organização. Os detalhes são exibidos para cada conjunto de dados listado, incluindo seu nome, o esquema ao qual o conjunto de dados adere e o status da execução de assimilação mais recente.

Por padrão, somente os conjuntos de dados assimilados são exibidos. Se quiser ver os conjuntos de dados gerados pelo sistema, habilite o **Mostrar conjuntos de dados do sistema** alterne do filtro.

![](assets/ajo-system-datasets.png)

Selecione o nome de um conjunto de dados para acessar a tela de atividade do Conjunto de dados e ver os detalhes do conjunto de dados selecionado. A guia activity inclui um gráfico que visualiza a taxa de mensagens que estão sendo consumidas, bem como uma lista de lotes bem-sucedidos e com falha.

## Criar conjuntos de dados{#create-datasets}

Para criar um novo conjunto de dados, comece selecionando **Criar conjunto de dados** no painel Conjuntos de dados .

É possível:

* Criar conjunto de dados a partir do esquema. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Crie um conjunto de dados a partir do arquivo CSV. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=pt-BR){target=&quot;_blank&quot;}


Assista a este vídeo para saber como criar um conjunto de dados, mapeá-lo para um esquema, adicionar dados a ele e confirmar que os dados foram assimilados.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


Saiba como criar um esquema, um conjunto de dados e assimilar dados para adicionar perfis de teste no Adobe Journey Optimizer em [esta amostra completa](../segment/creating-test-profiles.md)

Saiba mais sobre a criação de conjunto de dados em [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

Saiba como usar a interface do usuário de conjuntos de dados no [Documentação de visão geral da Ingestão de dados](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=pt-BR){target=&quot;_blank&quot;}.


**Consulte também**

* [Criar um esquema, um conjunto de dados e assimilar dados para adicionar perfis de teste no Journey Optimizer](../segment/creating-test-profiles.md)
* [Visão geral da assimilação de streaming](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=pt-BR){target=&quot;_blank&quot;}
* [Assimilar dados no Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
