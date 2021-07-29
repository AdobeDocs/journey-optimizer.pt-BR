---
title: Notas de versão
description: Notas de versão do Journey Optimizer
source-git-commit: c9fa07efd03e84bf38fb1d67fabba4b6066c4179
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 16%

---


# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Você também pode consultar as [Atualizações de documentação mais recentes](documentation-updates.md).

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
<p>O Adobe Experience Platform permite definir relações entre esquemas para usar um conjunto de dados como uma tabela de pesquisa para outro. O [!DNL Journey Optimizer] agora pode aproveitar os dados provenientes de um schema vinculado.</p>
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
<p>Agora é possível definir uma lista específica de segurança de envio no nível da sandbox, para ter um ambiente seguro para fins de teste. Em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para seus clientes. Esse recurso é habilitado por meio das APIs de supressão.</p>
<p>Para obter mais informações, consulte a <a href="allow-list.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* A taxa de limitação geral de todos os segmentos de leitura executados simultaneamente na mesma sandbox é limitada a 17.000 mensagens por segundo. [Leia mais](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* O campo **Cache duration** foi removido do painel de configuração da fonte de dados. [Leia mais](datasource/about-data-sources.md)
* Para fontes de dados externas, uma regra de limitação de 15 chamadas por segundo agora é definida automaticamente. [Leia mais](configuration/external-systems.md#capping)
* Para jornadas ao vivo, a tela de propriedades da jornada agora exibe a data da publicação e o nome do usuário que publicou a jornada. [Leia mais](building-journeys/journey-gs.md#change-properties)
* Na tela jornada list , o filtro jornada type foi adicionado. [Leia mais](user-interface.md#section_lgm_hpz_pgb)
* O parâmetro **[!UICONTROL Throttling rate]** foi adicionado na atividade Read segment . [Leia mais](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Visualizar e testar mensagens**
* A identidade e o namespace agora estão visíveis na tela **[!UICONTROL Preview]**. [Leia mais](preview.md#preview-your-messages)
* O número de emails de teste para provas agora está restrito a 10.
* Os caracteres permitidos para o **Prefixo da linha de assunto** em provas agora são limitados. [Leia mais](preview.md#send-proofs)

**Editor de expressão de personalização**
* A lista suspensa de ajuda foi renomeada e reordenada.

### Correções

* Correção de um problema que gerava mensagens duplicadas sendo entregues para delivery de email em lote.
* Agora os eventos são gerados adequadamente quando o envio de email não é executado depois que o período de nova tentativa termina.
* Correção de um problema em que as informações de IP estavam ausentes na tela Registros PTR .
* A localização no painel de ofertas no Editor de expressão agora está implementada.
* Corrigido o espaçamento incorreto em pop-ups de informações.
