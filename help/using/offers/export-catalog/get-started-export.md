---
title: Introdução à exportação de catálogo de ofertas
description: Saiba como exportar seu catálogo de ofertas como um conjunto de dados.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 14%

---

# Introdução à exportação de catálogo de ofertas {#export-catalog}

O Journey Optimizer permite exportar automaticamente seu catálogo de ofertas para o Adobe Experience Platform.

A exportação cria um conjunto de dados para cada objeto da Biblioteca de ofertas (consulte [Acessar conjuntos de dados exportados](../export-catalog/access-dataset.md)). O serviço inclui:

* Ofertas personalizadas
* Ofertas substitutas
* Disposições
* Decisões (anteriormente conhecidas como atividades de oferta)

Cada vez que um desses objetos é modificado na Biblioteca de ofertas, um novo trabalho de exportação é executado automaticamente para atualizar os conjuntos de dados.

>[!NOTE]
>
>Esse recurso não é habilitado por padrão. Se quiser usá-lo, entre em contato com o Adobe para ativá-lo para o catálogo. Após habilitá-los, os trabalhos de exportação serão automatizados e não exigirão nenhuma ação do seu lado.
