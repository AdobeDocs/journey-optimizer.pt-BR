---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a esquemas
description: Saiba como usar esquemas da Adobe Experience Platform no Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: esquemas, plataforma, dados, estrutura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 70f647cf4e95c1152a5c16395b88b11a6b72865c
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 18%

---

# Introdução a esquemas {#schemas-gs}

[!DNL Adobe Journey Optimizer] depende de **esquemas Adobe Experience Platform** para descrever a estrutura dos dados de forma consistente e reutilizável. Um esquema fornece uma definição abstrata de um objeto do mundo real (como uma pessoa) e descreve quais dados devem ser incluídos em cada instância desse objeto (como nome, aniversário etc.). Quando os dados são assimilados na Experience Platform, eles são sempre estruturados de acordo com um **esquema XDM**.

## Esquemas padrão e relacionais

Há dois tipos de esquemas no Adobe Experience Platform:

* **Esquemas padrão** são esquemas hierárquicos que usam classes e grupos de campos para capturar dados de registro ou de série temporal.

  Um schema padrão é composto de:

   * Uma **classe** (que define o comportamento dos dados: registro ou série temporal).
   * Um ou mais **grupos de campos** (que adicionam campos específicos ao esquema).

  No Journey Optimizer, os esquemas padrão são normalmente usados para representar **pessoas individuais e seus atributos**, capturar **interações de série temporal**, como cliques, compras ou logons, e potencializar o **Perfil de cliente em tempo real** para segmentação e personalização.

  ➡️ [Saiba como criar e configurar um esquema padrão neste vídeo](#video-schema) (vídeo)

* **Esquemas relacionais** são esquemas simples e não hierárquicos que não usam classes ou grupos de campos. Eles são usados para capturar dados de registro de entidades relacionais e são usados principalmente em [!DNL Journey Optimizer] **Campanhas orquestradas**.

  Exemplos de entidades relacionais incluem:
   * Reservas, contratos ou subscrições
   * Produtos ou catálogos
   * Lojas, locais ou parceiros

  Com esquemas relacionais, você pode enviar uma mensagem por entidade (por exemplo, por reserva ou por assinatura), criar segmentos com base em atributos de entidade (por exemplo, categoria de produto, localização da loja) e melhorar a capacidade de endereçamento, atingindo todos os contatos vinculados a uma entidade.

  Como os esquemas relacionais funcionam:

   1. **Criar esquemas manualmente ou importar via DDL**
   1. **Vincule esquemas** para definir relações entre entidades e pessoas (por exemplo, transações de fidelidade vinculadas a membros, recompensas vinculadas a marcas).
   1. **Assimilar dados** em seu conjunto de dados de fontes compatíveis.

  ➡️ [Saiba como gerenciar esquemas e conjuntos de dados relacionais](../orchestrated/gs-schemas.md)
➡️ [Introdução às campanhas orquestradas](../orchestrated/gs-schemas.md)

## Vídeo tutorial{#video-schema}

Saiba como criar um esquema padrão, adicionar grupos de campos, criar e configurar grupos de campos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Criar um esquema, um conjunto de dados e assimilar dados para adicionar perfis de teste no Journey Optimizer](../audience/creating-test-profiles.md)
>* [Visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}
>* [Práticas recomendadas para modelagem de dados](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=pt-BR){target="_blank"}
>* [Criar um esquema usando a API de registro de esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=pt-BR){target="_blank"}
>* [Definir uma relação entre dois esquemas usando o Editor de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=pt-BR){target="_blank"}
