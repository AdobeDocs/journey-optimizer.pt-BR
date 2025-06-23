---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão antecipadas
description: 'Notas de versão antecipadas do Journey Optimizer '
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 20f5dc6eab5695b485f4569ad098922a130d4b56
workflow-type: ht
source-wordcount: '1022'
ht-degree: 100%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.


## Notas de versão antecipadas de junho de 2025 {#25-6-rn}


**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados na data de lançamento.

**Data de lançamento**: 18 de junho de 2025


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
<p>As mensagens do Rich Communication Services (RCS) agora são aceitas no Journey Optimizer, o que permite os seguintes recursos de mensagens aprimorados sujeitos ao suporte do provedor e da operadora:</p>
<ul>
<li>Suporte a remetentes com marca e verificados: envie mensagens usando perfis de negócios verificados com elementos de marca (logotipo, nome do remetente, etc.).</li>
<li>Insights de entregas de mensagens: receba relatórios de entrega detalhados, incluindo atualizações de status de mensagem (por exemplo, enviado, entregue, lido).</li>
<li>Rastreamento de link: incorpore e rastreie URLs em mensagens RCS para análise de engajamento.</li>
<li>Fallback para SMS: retorno automático para SMS quando o dispositivo do perfil não dá suporte a RCS ou está temporariamente inacessível via RCS.</li>
<li>Composição básica de mensagem: envie mensagens RCS baseadas em texto com mídia opcional e elementos avançados, dependendo do suporte do provedor.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Campos de formulário no conteúdo de experiência baseado em código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir campos editáveis específicos em modelos de conteúdo JSON ou HTML que habilitam usuários comuns a editar facilmente o conteúdo em uma exibição de formulário na criação do canal de experiência baseada em código, sem a necessidade de manipular qualquer código.<br />Mais do que isso, ao definir os modelos de conteúdo de experiência baseada em código, agora é possível inserir políticas de decisão no modelo, aprimorando a capacidade de reutilização e a facilidade de uso.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Método de delegação personalizado para subdomínios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além da delegação completa e do método CNAME, há um novo método de configuração de subdomínio disponível: o método de delegação personalizado, que permite controlar e manter totalmente todos os aspectos do DNS necessários para entregar, renderizar e rastrear mensagens.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Atividade de decisão de conteúdo em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível incluir ofertas personalizadas em suas jornadas por meio de uma atividade dedicada de Decisão de conteúdo na tela da jornada e usá-las em atividades da jornada, incluindo condições e ações personalizadas.</p>
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



<table>
<thead>
<tr>
<th><strong>Execução de prática de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A execução de prática de jornada é um modo especial de publicação no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais sem entrar em contato com clientes do mundo real ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganharem confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la.</p>
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.</p>
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
<p>Agora é possível pausar e retomar jornadas. Esse recurso oferece aos profissionais de jornada maior controle e flexibilidade ao permitir que as jornadas ativas sejam temporariamente suspensas sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.</p>
<p>É possível pausar e retomar apenas uma jornada ou executar operações de pausa e retomada em massa para um grupo de jornadas.</p>
<p>Além disso, é possível aplicar filtros globais a jornadas pausadas para excluir perfis com base em seus atributos.</p>
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.</p>
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

   * **Janela de duração personalizada** para limites: um novo campo **Contagem de repetições** agora está disponível na tela de configuração de conjuntos de regras de canal, permitindo aplicar regras de limitação de frequência por vários dias, semanas ou meses, dependendo da duração especificada.

   * **Duração por hora**: agora é possível aplicar limites por hora para conjuntos de regras de canal.

* **Experiências baseadas em código**

   * A adição de uma política de decisão agora está disponível em modelos de conteúdo de experiência baseada em código.

   * Na tela de edição da jornada ou campanha da experiência baseada em código, agora é possível adicionar uma política de decisão diretamente, sem abrir o editor de personalização.

* **Suporte a CSS personalizado no Designer de email**

  O Journey Optimizer agora permite adicionar CSS personalizado ao conteúdo do email diretamente no Designer de email.

* **Nova navegação com guias para campanhas**

  Um novo padrão de navegação permite um acesso mais rápido à criação de conteúdo e oferece suporte à expansão adicional das configurações em campanhas.

* **Decisão**: data de disponibilidade: 3 de junho de 2025

  Os objetos de decisão agora podem ser copiados entre sandboxes, simplificando os fluxos de trabalho de teste e implantação. [Leia mais](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Suporte a atributos de item de decisão para regras de decisão** — Data de disponibilidade: 4 de junho de 2025

  Agora é possível usar atributos de item de decisão para criar regras de decisão. [Leia mais](../experience-decisioning/rules.md#create)

* **Atualização da API de execução de mensagem interativa** — Data de disponibilidade: 6 de junho de 2025

  A API de execução de mensagem interativa agora permite excluir a programação da execução de campanhas futuras. [Leia mais](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}