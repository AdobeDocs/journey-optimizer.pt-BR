---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a esquemas
description: Saiba como usar esquemas da Adobe Experience Platform no Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: esquemas, plataforma, dados, estrutura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 609
ht-degree: 78%

---

# Introdução a esquemas {#schemas-gs}

>[!BEGINSHADEBOX]

**Nesta página:** entenda como os esquemas padrão e relacionais da Adobe Experience Platform definem a estrutura dos dados para que você possa modelar perfis, eventos comportamentais e entidades relacionais para personalização e campanhas orquestradas no Adobe Journey Optimizer.

>[!ENDSHADEBOX]

O [!DNL Adobe Journey Optimizer] usa **esquemas da Adobe Experience Platform** para descrever a estrutura dos dados de forma consistente e reutilizável. Um esquema fornece uma definição abstrata de um objeto do mundo real (como uma pessoa) e descreve quais dados devem ser incluídos em cada instância desse objeto (como nome, data de aniversário e assim por diante). Quando os dados são assimilados na Experience Platform, eles são sempre estruturados de acordo com um **esquema XDM**.

## Esquemas padrão e relacionais

Há dois tipos de esquemas na Adobe Experience Platform:

* **Esquemas padrão** são esquemas hierárquicos que usam classes e grupos de campos para capturar dados de registros ou séries temporais.

  Um esquema padrão é composto de:

   * Uma **classe** (que define o comportamento dos dados: registro ou série temporal).
   * Um ou mais **grupos de campos** (que adicionam campos específicos ao esquema).

  No Journey Optimizer, os esquemas padrão são normalmente usados para representar **pessoas individuais e seus atributos**, capturar **interações de série temporal**, como cliques, compras ou logons, e potencializar o **perfil do cliente em tempo real** para segmentação e personalização.

  ➡️ [Aprenda como criar e configurar um esquema padrão neste vídeo](#video-schema) (vídeo)

* **Esquemas relacionais** são esquemas simples e sem hierarquia que não usam classes ou grupos de campos. Eles são usados para capturar dados de registro de entidades relacionais e servem principalmente para **campanhas orquestradas** do [!DNL Journey Optimizer].

  Exemplos de entidades relacionais incluem:
   * Reservas, contratos ou assinaturas
   * Produtos ou catálogos
   * Lojas, locais ou parceiros

  Com esquemas relacionais, você pode enviar uma mensagem por entidade (por exemplo, por reserva ou por assinatura), criar segmentos com base em atributos de entidade (por exemplo, categoria de produto, localização da loja) e melhorar a capacidade de endereçamento, alcançando todos os contatos vinculados a uma entidade.

  Como os esquemas relacionais funcionam:

   1. **Criar esquemas manualmente ou importar via DDL**
   1. **Vincule esquemas** para definir relações entre entidades e pessoas (por exemplo, transações de fidelidade vinculadas a membros, recompensas vinculadas a marcas).
   1. **Assimile dados** em seu conjunto de dados de fontes compatíveis.

  ➡️ [Aprenda a gerenciar esquemas relacionais e conjuntos de dados](../orchestrated/gs-schemas.md)
➡️ [Introdução às campanhas orquestradas](../orchestrated/gs-schemas.md)

>[!IMPORTANT]
>
>Ativar um esquema para o Perfil de cliente em tempo real é uma decisão permanente: uma vez ativado, o esquema não pode ser desativado ou excluído. Os conjuntos de dados criados nesse esquema podem ser desativados ou excluídos separadamente, mas isso remove os registros do perfil associado e pode afetar os workflows de segmentação e ativação. Antes de habilitar, finalize a configuração de identidade e a seleção de grupo de campos. Para obter orientações detalhadas, consulte [Planejamento de habilitação de perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"} e [Gerenciamento de esquemas habilitados para perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"} na documentação do Adobe Experience Platform.

## Vídeo tutorial{#video-schema}

Saiba como criar um esquema padrão, adicionar grupos de campos, criar e configurar grupos de campos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Introdução à gestão de dados no Journey Optimizer](gs-data.md)
>* [Criar um esquema, um conjunto de dados e assimilar dados para adicionar perfis de teste no Journey Optimizer](../audience/creating-test-profiles.md)
>* [Visão geral do sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=pt-BR){target="_blank"}
>* [Práticas recomendadas para modelagem de dados](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=pt-BR){target="_blank"}
>* [Planejamento de habilitação do perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}
>* [Gerenciamento de esquemas habilitados para perfil](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}
>* [Criar um esquema usando a API de registro de esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=pt-BR){target="_blank"}
>* [Definir uma relação entre dois esquemas usando o Editor de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=pt-BR){target="_blank"}
