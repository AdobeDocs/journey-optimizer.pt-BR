---
solution: Journey Optimizer
product: journey optimizer
title: Introdução do Journey Optimizer ao engenheiro de dados
description: Como engenheiro de dados, saiba mais sobre como trabalhar com o Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 52%

---

# Introdução ao engenheiro de dados {#data-engineer}

Como um **Engenheiro de Dados do Adobe Journey Optimizer**, você prepara e mantém dados de perfil do cliente para potencializar as experiências orquestradas por [!DNL Journey Optimizer], modela dados de clientes e negócios em esquemas e configura conectores de origem para assimilar dados. Você pode começar a trabalhar com o [!DNL Adobe Journey Optimizer] assim que o [Administrador do sistema](administrator.md) conceder acesso e preparar seu ambiente.

>[!NOTE]
>
>Saiba mais sobre **assimilação de dados** na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=pt-BR){target="_blank"}.

## Etapas essenciais de configuração de dados

Siga estas etapas para configurar a base de dados do Journey Optimizer:

1. **Criar namespaces de identidade**. Na Adobe [!DNL Journey Optimizer], as **Identidades** vinculam consumidores em dispositivos e canais, e o resultado é um gráfico de identidade. O gráfico de identidade vinculado é usado para personalizar experiências com base em interações em todos os pontos de contato comerciais. Saiba mais sobre identidades e namespaces de identidade [nesta página](../../audience/get-started-identity.md).

   Além disso, configure **identificadores complementares** para permitir que o mesmo perfil insira várias instâncias do jornada com base em identificadores secundários, como IDs de pedido ou IDs de reserva. Saiba mais sobre [identificadores complementares](../../building-journeys/supplemental-identifier.md).

1. **Crie esquemas** e habilite-os para perfis. Um esquema é um conjunto de regras que representam e validam a estrutura e o formato dos dados. Em um nível alto, os esquemas fornecem uma definição abstrata de um objeto do mundo real (como uma pessoa) e descrevem quais dados devem ser incluídos em cada instância desse objeto (como nome, sobrenome, aniversário e assim por diante).

   * Para jornadas e campanhas padrão: use [esquemas XDM](../../data/get-started-schemas.md)
   * Para campanhas orquestradas: crie [esquemas relacionais](../../orchestrated/gs-schemas.md) para habilitar a segmentação de várias entidades

1. **Crie conjuntos de dados** e habilite-os para perfis. Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). Os conjuntos de dados também contêm metadados que descrevem vários aspectos dos dados armazenados. Depois que um conjunto de dados é criado, é possível mapeá-lo para um esquema existente e adicionar dados a ele. Saiba mais sobre conjuntos de dados [nesta página](../../data/get-started-datasets.md).

   Para cenários avançados, prepare **conjuntos de dados para pesquisas em tempo de execução** para enriquecer a execução da jornada com dados em tempo real de conjuntos de dados de registro. Saiba mais sobre [pesquisa de conjunto de dados](../../building-journeys/dataset-lookup.md).

1. **Configurar conectores de origem**. O Adobe Journey Optimizer permite que os dados sejam assimilados de fontes externas e fornece a capacidade de estruturar, rotular e aprimorar os dados recebidos com os serviços da Platform. Você pode assimilar dados de várias fontes, como aplicativos Adobe, armazenamentos baseados em nuvem, bancos de dados e muitas outras. Saiba mais sobre conectores de origem [nesta página](../get-started-sources.md).

1. **Criar perfis de teste**. Os perfis de teste são necessários ao usar o [modo de teste](../../building-journeys/testing-the-journey.md) em uma jornada, e para [visualizar e testar suas mensagens](../../content-management/preview-test.md) antes de enviar. As etapas para criar perfis de teste são detalhadas [nesta página](../../audience/creating-test-profiles.md).

1. **Configurar atributos computados** (opcional). Crie atributos derivados dos dados do perfil para simplificar a segmentação e a personalização. Os atributos computados calculam automaticamente métricas complexas como &quot;total de compras nos últimos 90 dias&quot; ou &quot;valor médio de pedido&quot;. Saiba mais sobre [atributos computados](../../audience/computed-attributes.md).

Além disso, para enviar mensagens no jornada, você deve configurar as **[!UICONTROL Fontes de Dados]**, os **[!UICONTROL Eventos]** e as **[!UICONTROL Ações]**. Saiba mais [nesta seção](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* A configuração da **fonte de dados** permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. Saiba mais sobre Fontes de dados [nesta seção](../../datasource/about-data-sources.md).

* Os **Eventos** permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, à pessoa que flui para a jornada. Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de transmissão para eventos autenticados e não autenticados (como eventos do Adobe Mobile SDK). Saiba mais sobre eventos [nesta seção](../../event/about-events.md).

* O [!DNL Journey Optimizer] vem com recursos de mensagem integrados: você pode criar suas mensagens em uma jornada e projetar o conteúdo. Se você estiver usando um sistema de terceiros para enviar mensagens, por exemplo, Adobe Campaign, crie uma **ação personalizada**. Saiba mais sobre ações [nesta seção](../../action/action.md).

## Monitorar e analisar dados de jornada

Depois que as jornadas estiverem em execução, você poderá consultar os eventos de etapa da jornada no Data Lake para monitorar o desempenho, solucionar problemas e analisar o comportamento do cliente. Usar consultas SQL para analisar:

* Padrões de entrada e saída de perfil
* Taxas de erro e motivos para descarte
* Ler desempenho do trabalho de exportação de público
* Métricas de desempenho de ação personalizada
* Jornada estados de instância e gargalos

Explore exemplos de consulta [prontos para uso para análise de jornada](../../reports/query-examples.md) para começar a análise de dados e solução de problemas.

## Permanecer atualizado

Acompanhe os recursos e as melhorias mais recentes do Journey Optimizer:

* **[Notas de versão](../../rn/release-notes.md)**: revise novos recursos, melhorias e correções lançados a cada mês
* **[Atualizações da documentação](../../rn/documentation-updates.md)**: controle alterações recentes na documentação, incluindo novas páginas e conteúdo atualizado
* **Notificações do Produto**: Habilite as notificações no seu [perfil do Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} para receber alertas sobre:
   * Novas versões e recursos do produto
   * Janelas de manutenção e atualizações do sistema
   * Anúncios e alterações importantes

  Para habilitar notificações, clique no ícone de perfil na parte superior direita do Adobe Experience Cloud, vá para **Preferências > Notificações** e configure suas preferências de notificação do Journey Optimizer.
