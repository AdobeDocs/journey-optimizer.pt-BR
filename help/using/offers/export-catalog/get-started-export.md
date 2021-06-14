---
title: Introdução à exportação do catálogo de ofertas
description: Saiba como exportar seu catálogo de ofertas como um conjunto de dados.
feature: Ofertas
topic: Integrações
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 15%

---

# Introdução à exportação do catálogo de ofertas {#export-catalog}

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
