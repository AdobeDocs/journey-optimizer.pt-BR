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
workflow-type: ht
source-wordcount: '591'
ht-degree: 100%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.


## Notas de pré-lançamento de agosto de 2025 {#25-7-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 19 de agosto de 2025


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
<p>Anteriormente disponível para um conjunto limitado de clientes (disponibilidade limitada), este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-pause.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Visualização de calendário</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há uma exibição de calendário disponível nas listas de jornadas e campanhas. Ela permite ver todas as ativações de jornadas e campanhas nas respectivas listas.</p>
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes. Nesta versão com disponibilidade geral, o recurso inclui:</p>
<ul>
<li>Melhorias de design para a navegação pelas datas</li>
<li>A possibilidade de ver rascunhos de campanha, se você tiver definido as datas inicial e final</li>
<li>Uma nova configuração para ocultar e mostrar os itens do calendário em execução por muito tempo</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>Para mais informações, consulte a <a href="../building-journeys/journey-ui.md#journeys-calendar">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modo escuro no designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O designer de email do Journey Optimizer agora permite alternar para a exibição no modo escuro, onde você pode definir outras configurações personalizadas específicas que serão exibidas somente para destinatários que lerem seus emails no modo escuro.</p>
<p>Observe o seguinte:</p>
<ul>
<li>A renderização final no modo escuro pode variar e depende do cliente de email do destinatário.</li>
<li>Nem todos os clientes de email permitem o modo escuro. Além disso, alguns clientes de email aplicam seu próprio modo escuro padrão para todos os emails recebidos. Em ambos os casos, as configurações personalizadas definidas no designer de email não podem ser renderizadas.</li>
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
<p>O Journey Optimizer agora fornece as ferramentas necessárias para oferecer conteúdo personalizado e otimizado para o público-alvo das suas campanhas, permitindo que você execute experimentos de conteúdo, crie direcionamentos com base em regras e use combinações avançadas de ambos para maximizar a eficiência das suas campanhas.</p>
<p>Com a otimização, você pode:</p>
<ul>
<li>Testar múltiplas variações de conteúdo para identificar as mensagens mais eficazes.</li>
<li>Fornecer conteúdo personalizado com base nos atributos dos usuários e dados contextuais.</li>
<li>Combinar direcionamento e experimentação para estratégias de campanha avançadas.</li>
<li>Filtrar usuários que não correspondem aos critérios da variante.</li>
<li>Garantir mecanismos de fallback para manter o engajamento dos usuários.</li>
</ul>
<P>Quando a campanha estiver ativa, os perfis serão avaliados em relação aos critérios definidos e, com base nos critérios de correspondência, serão entregues com a experiência ou o conteúdo apropriado da campanha.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#Aug-25-8-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.