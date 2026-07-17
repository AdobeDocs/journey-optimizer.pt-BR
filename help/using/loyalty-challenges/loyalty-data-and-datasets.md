---
solution: Journey Optimizer
product: journey optimizer
title: Dados e conjuntos de dados de fidelidade
description: Saiba quais dados de perfil e conjuntos de dados da Adobe Experience Platform os desafios de fidelidade exigem e como o TTL (time-to-live, tempo de vida útil) do conjunto de dados afeta a retenção.
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 619
ht-degree: 8%

---

# Dados e conjuntos de dados de fidelidade {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**Sumário**

[Introdução aos desafios de fidelidade](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Criar e gerenciar desafios**

* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* [Criar desafios](create-challenges.md)
* [Criar tarefas](create-tasks.md)
* [Monitorar o desempenho de desafio de fidelidade](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configurar desafios de fidelidade](loyalty-admin.md)
* [Guia de definição de recompensa](reward-definition-guide.md)
* [Guia do Transformador de eventos](event-transformer-guide.md)
* **Dados e conjuntos de dados de fidelidade** ◀︎ **Você está aqui**
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../rn/releases.md).

## Visão geral {#overview}

Os desafios de fidelidade dependem da Adobe Experience Platform para identidade, atributos de perfil, eventos de experiência e públicos. Use esta página para saber quais dados devem ser preparados, quais conjuntos de dados estão envolvidos e como o **TTL (time-to-live)** afeta a retenção antes de criar desafios ou usar as APIs de desafios de fidelidade.

Entre em contato com o administrador do Adobe para obter a configuração do programa do Journey Optimizer ou configure o preenchimento de premiação e o mapeamento de eventos no menu **[!UICONTROL Admin. de fidelidade]**. [Saiba como configurar desafios de fidelidade](loyalty-admin.md). Para obter pontos de extremidade e autenticação REST, consulte a [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}.

## Conectores de fidelidade por meio de origens {#loyalty-connectors-sources}

Se os seus dados de fidelidade forem gerenciados em uma plataforma externa de recompensas, você poderá assimilar esses dados na Adobe Experience Platform usando os conectores das **Fontes** e, em seguida, usá-los nos Desafios de Fidelidade.

Os conectores de fidelidade e recompensa listados na documentação da Journey Optimizer incluem:

* **Talon.One**
* **Capilar**
* **Kobie**

Para integração de conectores e configuração completa, consulte [Introdução a conectores de fontes](../start/get-started-sources.md) e o [catálogo de fontes do Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=pt-BR#sources-catalog){target="_blank"}.

## Dados do Adobe Experience Platform {#aep-data}

### Atributos do perfil {#profile-attributes}

Desafie públicos, personalização e relatórios que usam perfis na classe **[!DNL XDM Individual Profile]**. Alinhe a identidade [namespace](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces){target="_blank"} que você usa para Desafios de Fidelidade com a forma como os membros são identificados nos dados do seu perfil e com o namespace selecionado em **[!UICONTROL Configurações globais]** no menu **[!UICONTROL Administrador de fidelidade]**.

Para atributos de fidelidade padrão no perfil (pontos, camada, programa, status e campos relacionados), use o grupo de campos de esquema **[Detalhes de Fidelidade](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}** do Experience Platform. Esse grupo de campos define o objeto `loyalty` e suas propriedades (por exemplo, `points`, `tier`, `program` e `status`).

➡️ [Grupo de campos de esquema de Detalhes de Fidelidade](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### Eventos de experiência {#experience-events}

As tarefas **[!UICONTROL Comprar]**, **[!UICONTROL Gastar]** e **[!UICONTROL Evento personalizado]** dependem dos eventos de experiência assimilados na Adobe Experience Platform. Para tarefas de **[!UICONTROL Evento personalizado]**, as definições de evento correspondentes (caminho do identificador, ID do esquema XDM opcional, esquema e transformador) devem ser configuradas no menu **[!UICONTROL Admin. de fidelidade]** para que os profissionais de marketing possam inserir valores de evento personalizados no construtor de tarefas. [Saiba como configurar definições de evento](loyalty-admin.md#event-definitions)

Certifique-se de que as cargas do evento usem o mesmo namespace de identidade da configuração de Desafios de fidelidade para que o progresso possa ser atribuído ao perfil correto.

### Públicos-alvo e relatórios {#audiences-reporting}

Os profissionais de marketing selecionam [públicos-alvo](../audience/about-audiences.md) da Platform ao configurar a qualificação para o desafio. Os painéis de relatórios de fidelidade usam o Adobe Customer Journey Analytics. [Saiba como monitorar o desempenho do desafio de fidelidade](loyalty-reporting.md)

## Tempo de vida (TTL) do conjunto de dados {#dataset-ttl}

Os desafios de fidelidade armazenam dados operacionais e de relatórios em conjuntos de dados do Adobe Experience Platform (incluindo conjuntos de dados relacionados a eventos e personalização criados para o seu programa). O conjunto de dados **tempo de vida (TTL)** controla por quanto tempo os dados ficam retidos no data lake e, quando aplicável, no repositório de perfis.

O Journey Optimizer aplica medidas de proteção TTL a muitos conjuntos de dados gerados pelo sistema. Os conjuntos de dados relacionados à fidelidade seguem o mesmo modelo de retenção da Platform para sua sandbox.

➡️ [Medidas de proteção de TTL (Time-to-live) de conjuntos de dados no Journey Optimizer](../data/datasets-ttl.md)

>[!NOTE]
>
>A configuração de fidelidade no nível da organização pode incluir configurações de arquivamento e retenção (por exemplo, duração do arquivamento) gerenciadas pelo serviço de metadados de fidelidade. Entre em contato com o administrador do Adobe se precisar ajustar a retenção para o ambiente beta privado.
