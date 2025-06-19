---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5e7aad25fa08994f6cbce9adfce4a3dc94fe3e47
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 44%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/latest){target="_blank"}.


## Notas de versão de junho de 2025 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Data de lançamento**: quinta-feira, 18 de junho de 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Novos recursos {#25-06-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.


<table>
<thead>
<tr>
<th><strong>Mensagens RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O envio de mensagens por RCS (Serviços de Comunicação Avançada) agora é suportado no Journey Optimizer, habilitando os seguintes recursos de envio de mensagens aprimorados sujeitos ao suporte do provedor e da operadora:</p>
<ul>
<li>Suporte a remetente marcado e verificado: envie mensagens usando perfis comerciais verificados com elementos de marca (logotipo, nome do remetente etc.).</li>
<li>Insights de delivery de mensagens: receba relatórios de delivery detalhados, incluindo atualizações de status de mensagem (por exemplo, enviado, entregue, lido).</li>
<li>Rastreamento de link: incorpore e rastreie URLs em mensagens do RCS para análise de engajamento.</li>
<li>Fallback para SMS: fallback automático para SMS quando o dispositivo do perfil não dá suporte a RCS ou está temporariamente inacessível via RCS.</li>
<li>Composição básica de mensagem: envia mensagens RCS baseadas em texto com mídia opcional e elementos avançados, dependendo do suporte do provedor.</li>
</ul>
<p>Para obter mais informações, consulte a <a href="../sms/sms-configuration.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campos de formulário no conteúdo de experiência baseado em código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir campos editáveis específicos em modelos de conteúdo JSON ou HTML que permitem que usuários não técnicos editem facilmente o conteúdo em uma exibição de formulário na criação do canal de experiência baseado em código, sem a necessidade de manipular qualquer código.<br />Mais do que isso, ao definir os modelos de conteúdo de experiência baseados em código, agora é possível inserir políticas de decisão no modelo, aumentando a reutilização e a facilidade de uso.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Para obter mais informações, consulte a <a href="../code-based/code-based-form-fields.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Atividade de decisão de conteúdo em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível incluir ofertas personalizadas em suas jornadas por meio de uma atividade dedicada de Decisão de conteúdo na tela de jornada e usá-las em atividades de jornada, incluindo condições e ações personalizadas.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/content-decision.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Execução de prática de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Jornada Dry run é um modo de publicação de jornada especial no Adobe Journey Optimizer que permite que os profissionais de jornada testem uma jornada usando dados de produção reais sem entrar em contato com clientes reais ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganhar confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la ao vivo.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-dry-run.md">documentação detalhada</a>.</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Pausar e retomar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode pausar e retomar suas jornadas. Esse recurso oferece aos profissionais de jornadas maior controle e flexibilidade, permitindo que as jornadas ativas sejam temporariamente suspensas sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.</p>
<p>Você pode pausar e retomar apenas uma jornada ou executar operações de pausa e retomada em massa para um grupo de jornadas.</p>
<p>Além disso, é possível aplicar filtros globais a jornadas pausadas para excluir perfis com base em seus atributos.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-pause.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dimensionar o experimento vencedor</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A opção Dimensionar o experimento vencedor permite implantar de forma automática ou manual a variação vencedora de um experimento em todo o seu público-alvo. Esse recurso garante que, após identificar o melhor desempenho, seja possível maximizar seu alcance e eficácia sem necessidade de supervisão manual constante.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-experiment.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 2 de junho de 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflito e priorização</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No Journey Optimizer, gerenciar o volume e o momento de início das campanhas e jornadas é essencial para não sobrecarregar clientes com muitas interações. O Journey Optimizer agora oferece várias ferramentas para o gerenciamento de conflitos e a priorização, antes disponíveis apenas para um número limitado de organizações (disponibilidade limitada), mas que agora estão em disponibilidade geral.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Esta versão de disponibilidade geral também inclui os seguintes aprimoramentos:</p>
<ul>
<li>Suporte estendido: as ferramentas de gerenciamento de conflitos agora oferecem suporte às jornadas unitárias, jornadas de qualificação de público-alvo e jornadas de público-alvo de leitura.</li>
<li>Solução de problemas aprimorada: agora há dois novos campos de evento de etapa disponíveis no serviço de consulta, permitindo analisar por que um perfil foi rejeitado de uma jornada ou campanha.</li>
<li>Relatórios aprimorados: os relatórios agora indicam qual regra específica excluiu um perfil de uma jornada ou campanha, fornecendo maior transparência e insights acionáveis.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de junho de 2025</p>
</td>
</tr>
</tbody>
</table>


### Aprimoramentos {#25-06-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

* **Conjuntos de regras de canal**

   * **Janela de duração personalizada** para limitação - Um novo campo **A cada** agora está disponível na tela de configuração de conjuntos de regras de canal, permitindo que você aplique regras de limitação de frequência em vários dias, semanas ou meses, dependendo da duração especificada.

   * **Frequência de limite de redefinição por hora** - Agora é possível aplicar limite de hora em hora para conjuntos de regras de canal. Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Entre em contato com o atendimento ao cliente para ativá-lo.

   * **Duração diária** - Anteriormente disponível em Disponibilidade limitada, o limite de frequência &quot;Diário&quot; nos conjuntos de regras do canal agora está disponível para todos os clientes.

  Para obter mais informações, consulte a [documentação detalhada](../conflict-prioritization/channel-capping.md).

* **Experiências baseadas em código**

   * A adição de uma política de decisão agora está disponível em modelos de conteúdo de experiência baseados em código, nos quais ela pode ser usada para aproveitar ofertas em campos de formulário editáveis. [Leia mais](../code-based/code-based-form-fields.md)

   * Na tela de jornada de experiência ou edição de campanha baseada em código, agora é possível adicionar uma política de decisão diretamente, sem abrir o editor de personalização. [Leia mais](../code-based/create-code-based.md#edit-code)

* **Suporte a CSS personalizado no Designer de email**

  O Journey Optimizer agora permite adicionar CSS personalizado ao seu conteúdo de email diretamente no Designer de email. [Leia mais](../email/custom-css.md)

* **Nova navegação com guias para campanhas**

  Um novo padrão de navegação permite um acesso mais rápido à criação de conteúdo e oferece suporte à expansão adicional das configurações em campanhas. [Leia mais](../campaigns/create-campaign.md)

* **Decisão**: data de disponibilidade: 3 de junho de 2025

  Os objetos de decisão agora podem ser copiados entre sandboxes, simplificando os fluxos de trabalho de teste e implantação. [Leia mais](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Suporte a atributos de item de decisão para regras de decisão** — Data de disponibilidade: 4 de junho de 2025

  Agora é possível usar atributos de item de decisão para criar regras de decisão. [Leia mais](../experience-decisioning/rules.md#create)

* **Atualização da API de execução de mensagem interativa** — Data de disponibilidade: 6 de junho de 2025

  A API de execução de mensagem interativa agora permite excluir a programação da execução de campanhas futuras. [Leia mais](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
