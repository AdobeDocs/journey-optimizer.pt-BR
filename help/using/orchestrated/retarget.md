---
solution: Journey Optimizer
product: journey optimizer
title: Iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer
description: Saiba como iniciar e monitorar campanhas orquestradas com o Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# Criação de consultas de redirecionamento {#retarget}

+++ Sumário

| Bem-vindo às campanhas orquestradas | Lançar a primeira campanha orquestrada | Consultar o banco de dados | Atividades de campanhas orquestradas |
|---|---|---|---|
| [Introdução a campanhas orquestradas](gs-orchestrated-campaigns.md)<br/><br/>[Etapas de configuração](configuration-steps.md)<br/><br/>[Acesse e gerencie campanhas orquestradas](access-manage-orchestrated-campaigns.md)<br/><br/>[Etapas principais para criar uma campanha orquestrada](gs-campaign-creation.md) | [Criar e agendar a campanha](create-orchestrated-campaign.md)<br/><br/>[Orquestrar atividades](orchestrate-activities.md)<br/><br/>[Iniciar e monitorar a campanha](start-monitor-campaigns.md)<br/><br/>[Relatórios](reporting-campaigns.md) | [Trabalhar com o construtor de regras](orchestrated-rule-builder.md)<br/><br/>[Criar a primeira consulta](build-query.md)<br/><br/>[Editar expressões](edit-expressions.md)<br/><br/><b>[Redirecionamento](retarget.md)</b> | [Introdução às atividades](activities/about-activities.md)<br/><br/>Atividades:<br/>[And-join](activities/and-join.md) - [Criar público](activities/build-audience.md) - [Alterar dimensão](activities/change-dimension.md) - [Atividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Desduplicação](activities/deduplication.md) - [Enriquecimento](activities/enrichment.md) - [Bifurcação](activities/fork.md) - [Reconciliação](activities/reconciliation.md) - [Salvar público](activities/save-audience.md) - [Divisão](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Documentação em andamento

>[!ENDSHADEBOX]

O redirecionamento permite acompanhar os recipients com base em como eles responderam a uma campanha orquestrada anterior. Por exemplo, você pode enviar um segundo email para perfis que receberam, mas não clicaram no primeiro.

A campanha orquestrada fornece duas fontes de dados principais para isso:

- **Feedback de Mensagem**: captura eventos relacionados à entrega, por exemplo, mensagem enviada, aberta, rejeitada, etc.

- **Acompanhamento de email**: captura as ações do usuário, por exemplo, cliques e aberturas.

## Criar uma regra de redirecionamento baseada em comentários

A Regra de Redirecionamento Baseada em Comentários permite redirecionar destinatários com base em eventos de entrega de mensagens capturados no conjunto de dados **Comentários de Mensagens**. Esses eventos incluem resultados como mensagens que estão sendo enviadas, abertas, rejeitadas ou marcadas como spam.

Usando esses dados, você pode definir regras para identificar os recipients que receberam uma mensagem anterior, mas não se envolveram com ela, permitindo a comunicação de acompanhamento com base em status de delivery específicos.

1. Crie uma nova **Campanha orquestrada**.

2. Adicione uma atividade **Criar Público** e defina o targeting dimension como **Recipient (caas)**.

3. No **Construtor de Regras**, clique em **Adicionar Condição** e selecione **Comentários sobre a Mensagem** no Seletor de Atributos. Clique em **Confirmar**.

4. Adicione uma condição para **Status de Feedback** e defina o valor como **Mensagem Enviada**.

5. Para direcionar uma campanha orquestrada específica:

   - Adicione outra condição, pesquise por `entity` e navegue até:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Selecione **Nome da campanha orquestrada** e especifique o nome da campanha.

6. Para direcionar uma mensagem ou atividade específica dentro dessa campanha orquestrada:

   - Adicione outra condição, pesquise por `entity` e navegue até:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Selecione **Nome da Ação de Campanha Orquestrada** e especifique o nome da ação de campanha.

     Nomes de ações podem ser encontrados clicando no ![ícone de Informações](assets/do-not-localize/info-icon.svg) ao lado de uma atividade na tela.

   >[!TIP]
   >
   >Em vez de usar nomes, você também pode filtrar pela **ID da campanha** (UUID), que pode ser encontrada nas propriedades da campanha.

## Criar uma regra de redirecionamento baseada em rastreamento

A regra de redirecionamento baseada em rastreamento segmenta os destinatários com base em suas interações com uma mensagem, usando dados do conjunto de dados **Acompanhamento de email**. Ele captura as ações do usuário, como aberturas de email e cliques em links.

Para redirecionar destinatários com base nas interações de mensagem (por exemplo, abrir ou clicar), use a entidade **Acompanhamento de email** da seguinte maneira:

1. Crie uma nova **Campanha orquestrada** e adicione uma atividade **Criar público** com **Destinatário (caas)** como dimensão de direcionamento para se concentrar nos destinatários anteriores da campanha orquestrada.

1. Adicione uma nova condição para o **Acompanhamento de emails**. Clique em **Confirmar** para criar uma condição &quot;O Acompanhamento de Email Existe, como&quot;.

1. Nessa condição, adicione uma condição e procure pelo atributo **Tipo de Interação**.

1. Nas opções de condição personalizadas, use **Incluído em** como operador e selecione um ou mais valores dependendo do seu caso de uso. Por exemplo:
   - **Mensagem Aberta**
   - **Link de Mensagem Clicado**

1. Para associar os dados de rastreamento a uma campanha específica:

   - Adicione uma condição no bloco de rastreamento de email.

   - Navegue até `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Adicione condições para o **Nome da Campanha Orquestrada** e, se necessário, o **Nome da Ação da Campanha Orquestrada**.

     Nomes de ações podem ser encontrados clicando no ![ícone de Informações](assets/do-not-localize/info-icon.svg) ao lado de uma atividade na tela.

   >[!TIP]
   >
   >Em vez de usar nomes, você também pode filtrar pela **ID da campanha** (UUID), que pode ser encontrada nas propriedades da campanha.
