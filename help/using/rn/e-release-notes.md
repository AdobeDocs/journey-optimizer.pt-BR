---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 132121b4dd9c20149e4a5b24e90ebffd4ebbdcbc
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 38%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de agosto de 2023 {#aug-rn-2023}

**Data de lançamento**: 23 a 24 de agosto de 2023

### Novos recursos{#aug-2023-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Enviar mensagens no aplicativo em suas jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode enviar mensagens personalizadas no aplicativo para os usuários do aplicativo em uma jornada. Use o Journey Optimizer para criar notificações e personalizar o layout, a exibição, o texto e os botões das mensagens para criar uma experiência perfeita.</p>
<img src="assets/in_app_journey_1.png"/>
<p>Para obter mais informações, consulte a <a href="../in-app/get-started-in-app.md">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Validar seus emails com seed lists</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar e gerenciar seed lists no Journey Optimizer. Uma lista de propagação consiste em endereços de email de teste para os quais você envia um email antes de enviá-lo para o público-alvo real. Use esse recurso para monitorar as cópias de email enviadas e garantir que todos os formatos de exibição, URLs, imagens e links estejam corretos.</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gerar texto e imagens com o assistente de Conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Depois de criar e personalizar sua mensagem, leve o conteúdo ao próximo nível com o assistente de Conteúdo. Agora você pode usar o assistente de Conteúdo para otimizar o impacto da sua mensagem, experimentando com diferentes títulos principais e imagens. Cada variante é gerenciada como um Tratamento exclusivo, para medir e comparar qual título gera efetivamente mais cliques.</p>
<p>No momento, esse recurso está disponível como um beta privado.</p>
<img src="assets/gen-ai-image-2.png"/>
<!--p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



### Melhorias {#aug-2023-improvements}

Esta versão vem com as melhorias listadas abaixo.

**APIs**

Uma nova API para criar e gerenciar Fragmentos de conteúdo agora está disponível. [Saiba mais](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**Canal de email**

* Uma nova opção está disponível nas configurações da superfície de email para incluir endereços de email suprimidos devido a reclamações de spam nos públicos-alvo de mensagens transacionais. Mesmo que marquem mensagens de marketing como spam, esses perfis poderão receber mensagens transacionais, como redefinição de senha ou declarações de conta. Essa opção está desabilitada por padrão.

**Jornadas**

* Agora é possível aproveitar as respostas de chamada da API em ações personalizadas e orquestrar sua jornada com base nessas respostas. No momento, esse recurso está disponível como um beta privado.
* Foi introduzido um novo tipo de alerta de sistema. Agora você pode ser notificado quando houver falha em uma ação personalizada.
* Ao duplicar uma jornada, agora é possível definir o nome da cópia da jornada.


**Correspondência direta**

* Suporte ao Azure Blob como destino de roteamento.
* Suporte `&` como separador personalizado.