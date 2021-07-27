---
title: Notas de versão
description: Notas de versão do Journey Optimizer
source-git-commit: 4d3352184aac7fe19096c21650982e29506f2bff
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 24%

---


# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do Journey Optimizer.
Você também pode consultar as [Atualizações de documentação mais recentes](documentation-updates.md).

## Versão de julho de 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Aproveitar relacionamentos de schema</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Experience Platform permite definir relações entre esquemas para usar um conjunto de dados como uma tabela de pesquisa para outro. O Journey Optimizer agora pode aproveitar os dados provenientes de um schema vinculado.</p>
<p>Esses campos estão disponíveis na configuração de evento unitário, nas condições de jornada, na personalização da mensagem e na personalização da ação personalizada.</p>
<p>Para obter mais informações, consulte a <a href="event/experience-event-schema.md#leverage_schema_relationships">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lista de permissões</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir uma lista segura para envio específica no nível da sandbox para evitar o envio de emails indesejados para seus recipients em um ambiente de teste, por exemplo.
</p>
<p>Para obter mais informações, consulte a <a href="allow-list.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

* A taxa de limitação geral de todos os segmentos de leitura executados simultaneamente na mesma sandbox é limitada a 17.000 mensagens por segundo. [Leia mais](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* O campo **Cache duration** foi removido do painel de configuração da fonte de dados. [Leia mais](datasource/about-data-sources.md)
* Para fontes de dados externas, uma regra de limitação de 15 chamadas por segundo agora é definida automaticamente. [Leia mais](configuration/external-systems.md#capping)
* Para jornadas ao vivo, a tela de propriedades da jornada agora exibe a data da publicação e o nome do usuário que publicou a jornada. [Leia mais](building-journeys/journey-gs.md#change-properties)
* Na tela jornada list , o filtro jornada type foi adicionado. [Leia mais](user-interface.md#section_lgm_hpz_pgb)
* O parâmetro [!UICONTROL Throttling rate] foi adicionado na atividade Read segment . [Leia mais](building-journeys/read-segment.md#configuring-segment-trigger-activity)
