---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 38%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**. Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.


## Notas de pré-lançamento de agosto de 2025 {#25-7-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**. Links, telas e a documentação atualizada são publicados na data de lançamento.

Consulte também [Notas de pré-lançamento do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: quarta-feira, 19 de agosto de 2025


### Novos recursos {#Aug-25-8-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Pausar e retomar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível pausar e retomar jornadas. Esse recurso oferece aos profissionais de jornada maior controle e flexibilidade ao permitir que as jornadas ativas sejam temporariamente suspensas sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.</p>
<p>É possível pausar e retomar apenas uma jornada ou executar operações de pausa e retomada em massa para um grupo de jornadas.</p>
<p>Além disso, é possível aplicar filtros globais a jornadas pausadas para excluir perfis com base em seus atributos.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Anteriormente disponível para um conjunto limitado de clientes (disponibilidade limitada), esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-pause.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Exibição de calendário</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há uma exibição de calendário disponível nas listas de jornadas e campanhas. Ela permite ver todas as ativações de jornadas e campanhas nas respectivas listas.</p>
<p>Anteriormente disponível em Disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de Disponibilidade Geral, o recurso inclui:</p>
<ul>
<li>Melhorias de design para a navegação em datas</li>
<li>A capacidade de ver campanhas de rascunho se você tiver definido uma data de início e término</li>
<li>Uma nova configuração para ocultar e mostrar os itens do calendário em execução por muito tempo</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-ui.md#journeys-calendar">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modo escuro no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer Email Designer agora oferece a capacidade de alternar para a exibição no modo escuro, onde você pode definir ainda configurações personalizadas específicas que serão exibidas somente para destinatários que leem seus emails no modo escuro.</p>
<p>Observe o seguinte:</p>
<ul>
<li>A renderização final do modo escuro pode variar e depende do cliente de email do recipient.</li>
<li>Nem todos os clientes de email oferecem suporte ao modo escuro personalizado. Além disso, alguns clientes de email aplicam apenas seu próprio modo escuro padrão para todos os emails recebidos. Em ambos os casos, as configurações personalizadas definidas no Designer de email não podem ser renderizadas.</li>
</ul>
<P>No momento, esse recurso está na versão beta e disponível apenas para clientes beta. Para participar do programa beta, entre em contato com seu representante da Adobe.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../email/dark-mode.md">documentação detalhada</a>. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Otimização em campanhas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora capacita você com as ferramentas para fornecer conteúdo personalizado e otimizado para o público de suas campanhas, permitindo que você execute experimentos de conteúdo, crie direcionamentos com base em regras e use combinações avançadas de ambos para maximizar a eficiência de suas campanhas.</p>
<p>Com a Otimização, você pode:</p>
<ul>
<li>Teste várias variações de conteúdo para identificar as mensagens mais eficazes.</li>
<li>Forneça conteúdo personalizado com base em atributos do usuário e dados contextuais.</li>
<li>Combine direcionamento e experimentação para estratégias de campanha avançadas.</li>
<li>Filtrar usuários que não correspondem aos critérios da variante.</li>
<li>Garantir mecanismos de fallback para manter o engajamento do usuário.</li>
</ul>
<P>Quando a campanha estiver ativa, os perfis serão avaliados em relação aos critérios definidos e, com base nos critérios de correspondência, eles serão entregues com a experiência ou o conteúdo apropriado da campanha.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#Aug-25-8-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.