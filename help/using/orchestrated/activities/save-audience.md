---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Salvar público-alvo
description: Saiba como usar a atividade Salvar público-alvo em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 0abe441a413b748b46379871f3b70842715921a3
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 45%

---

# Salvar público-alvo {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Salvar atividade do público"
>abstract="A atividade **Salvar público-alvo** é uma atividade de **Direcionamento** que permite atualizar um público-alvo já existente ou criar um novo a partir da população gerada anteriormente na campanha orquestrada. Após criados, esses públicos-alvo são adicionados à lista de públicos-alvo do aplicativo e podem ser acessados pelo menu **Públicos-alvo**."


+++ Índice 

| Bem-vindo(a) às campanhas orquestradas | Lançar a sua primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](../gs-orchestrated-campaigns.md)<br/><br/>Criar e gerenciar Esquemas e Conjuntos de Dados relacionais:</br> <ul><li>[Introdução a Esquemas e Conjuntos de Dados](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carregamento de arquivo](../file-upload-schema.md)</li><li>[Assimilar dados](../ingest-data.md)</li></ul>[Acessar e gerenciar campanhas orquestradas](../access-manage-orchestrated-campaigns.md) | [Etapas principais para criar uma campanha orquestrada](../gs-campaign-creation.md)<br/><br/>[Criar e programar a campanha](../create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](../orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](../start-monitor-campaigns.md)<br/><br/>[Geração de relatórios](../reporting-campaigns.md) | [Trabalhar com o construtor de regras](../orchestrated-rule-builder.md)<br/><br/>[Criar a sua primeira consulta](../build-query.md)<br/><br/>[Editar expressões](../edit-expressions.md)<br/><br/>[Redirecionamento](../retarget.md) | [Introdução às atividades](about-activities.md)<br/><br/>Atividades:<br/>[Associação](and-join.md) - [Criar público-alvo](build-audience.md) - [Mudar dimensão](change-dimension.md) - [Atividades de canal](channels.md) - [Combinar](combine.md) - [Desduplicação](deduplication.md) - [Enriquecimento](enrichment.md) - [Bifurcação](fork.md) - [Reconciliação](reconciliation.md) - <b>[Salvar público-alvo](save-audience.md)</b> - [Divisão](split.md) - [Aguardar](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

O conteúdo desta página não é final e pode estar sujeito a alterações.

>[!ENDSHADEBOX]

A atividade **[!UICONTROL Salvar público-alvo]** é uma atividade de **[!UICONTROL Direcionamento]** usada para criar um novo público-alvo ou atualizar um já existente com base na população gerada anteriormente na campanha orquestrada. Depois de salvo, o público é adicionado à lista de públicos-alvo do aplicativo e torna-se acessível pelo menu **[!UICONTROL Públicos-alvo]**.

Normalmente, é usado para capturar segmentos de público-alvo criados no mesmo fluxo de trabalho de campanha, disponibilizando-os para reutilização em campanhas futuras. Normalmente, ela está conectada a outras atividades de direcionamento, como **[!UICONTROL Criar público-alvo]** ou **[!UICONTROL Combinar]**, para salvar a população direcionada final.

## Configurar a atividade Salvar público-alvo {#save-audience-configuration}

Siga estas etapas para configurar a atividade **[!UICONTROL Salvar público-alvo]**:

1. Adicione uma atividade **[!UICONTROL Salvar público-alvo]** à sua campanha orquestrada.

1. Insira um **[!UICONTROL Rótulo do público-alvo]** que identificará o público-alvo salvo.

1. Escolha um **[!UICONTROL Campo de mapeamento de perfil&#x200B;]** na Targeting dimension do Campaign.

   ➡️ [Siga as etapas detalhadas nesta página para criar sua dimensão de Direcionamento de Campanha](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Clique em **[!UICONTROL Adicionar mapeamentos de público-alvo]** se desejar associar o público-alvo salvo a campos de identidade adicionais.

   ![](../assets/save-audience-2.png)

1. Para finalizar a configuração, salve e publique a campanha orquestrada. Isso gerará e armazenará o seu público-alvo.

O conteúdo do público-alvo salvo ficará disponível na exibição detalhada do público-alvo, que pode ser acessada no menu **[!UICONTROL Públicos-alvo]** ou pode ser selecionado ao direcionar um público-alvo, por exemplo, com uma atividade **[!UICONTROL Ler público-alvo]**.

![](../assets/save-audience-4.png)


## Exemplo {#save-audience-example}

O exemplo a seguir demonstra como criar um público-alvo simples com o direcionamento. Um query identifica todos os recipients que reservaram uma viagem nos últimos 30 dias filtrando essa população na campanha orquestrada. Ao escolher **Recipients - CRMID** como a **Targeting dimension**, o público-alvo será direcionado a cada evento de reserva individual, em vez de somente ao destinatário como um todo. A atividade **[!UICONTROL Salvar público-alvo]** capta esses perfis para criar um público-alvo reutilizável de compradores recentes.

![](../assets/save-audience-3.png)
