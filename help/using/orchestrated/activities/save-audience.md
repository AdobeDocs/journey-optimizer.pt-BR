---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Save audience
description: Saiba como usar a atividade Salvar público-alvo em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 3%

---

# Salvar público-alvo {#save-audience}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Acessar e gerenciar campanhas orquestradas](access-manage-orchestrated-campaigns.md) | [Etapas principais para a criação de campanha orquestrada](gs-campaign-creation.md)<br/><br/>[Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/><b>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)</b><br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/>[Redirecionamento](retarget.md) | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

A atividade **[!UICONTROL Salvar público-alvo]** é uma atividade **[!UICONTROL de Direcionamento]** que permite atualizar um público-alvo existente ou criar um novo público a partir da população gerada anteriormente na campanha orquestrada. Após criado, esses públicos são adicionados à lista de públicos-alvo do aplicativo e podem ser acessados no menu **[!UICONTROL Públicos-alvo]**.

Essa atividade é particularmente útil para preservar segmentos de público calculados na mesma campanha orquestrada, disponibilizando-os para reutilização em campanhas futuras. Normalmente está conectado a outras atividades de direcionamento, como **[!UICONTROL Criar público-alvo]** ou **[!UICONTROL Combinar]**, para capturar e salvar a população resultante.

## Configurar a atividade Save audience {#save-audience-configuration}

Siga estas etapas para configurar a atividade **Salvar público-alvo**:

1. Adicione uma atividade **Save audience** à sua campanha orquestrada.

1. No menu suspenso **Modo**, selecione a ação que deseja executar:

   * **Criar ou atualizar um público existente**: definir um **Rótulo de público-alvo**. Se o público-alvo já existir, ele será atualizado; caso contrário, um novo público-alvo será criado.

   * **Atualizar um público-alvo** existente: escolha o **Público-alvo** que deseja atualizar na lista de públicos-alvo existentes.

1. Selecione o **Modo de atualização** que se aplica aos públicos existentes:

   * **Substituir conteúdo do público-alvo por novos dados**: todo o conteúdo do público-alvo é substituído e os dados antigos são perdidos. Somente os dados da transição de entrada da atividade **Salvar público-alvo** são retidos. Essa opção apaga o tipo de público-alvo e o targeting dimension do público-alvo atualizado.

   * **Concluir público-alvo com novos dados**: o conteúdo antigo do público-alvo é retido e os dados da transição de entrada da atividade **Salvar público-alvo** são adicionados a ele.

1. Marque a opção **Generate an outbound transition** se desejar adicionar uma transição após a atividade **Save audience**.

O conteúdo do público-alvo salvo ficará disponível na exibição detalhada do público-alvo, que pode ser acessada no menu **Públicos-alvo**. As colunas disponíveis nesta exibição correspondem às da transição de entrada da atividade **Salvar público-alvo** da campanha orquestrada.

## Exemplo {#save-audience-example}

O exemplo a seguir ilustra uma simples atualização de público-alvo do direcionamento. Um programador executa a campanha orquestrada uma vez por mês. Um query recupera todos os perfis que fizeram assinatura nos diferentes aplicativos disponíveis. A atividade **Salvar público-alvo** atualiza o público-alvo removendo os perfis que cancelaram a assinatura do serviço desde a última execução orquestrada da campanha e adicionando perfis que fizeram assinatura recentemente.
