---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão de 2025
description: Notas de versão de 2025 do Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 311dbb72079b91d3faa1c60c38a66a806d80da42
workflow-type: tm+mt
source-wordcount: '5119'
ht-degree: 100%

---

# Notas de versão de 2025 {#release-notes-2025}

Esta página lista todos os recursos e melhorias da versão de 2025 do [!DNL Journey Optimizer].

## Notas de versão de julho de 2025 {#25-7-rn}

**Data de lançamento**: 29 de julho de 2025

### Novos recursos {#features-25-7}

Os novos recursos incluídos nesta versão são detalhados abaixo.

#### Recursos

<table>
<thead>
<tr>
<th><strong>Marcas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, você pode criar e personalizar as suas próprias marcas para definir claramente a sua identidade visual e verbal nas comunicações. Com a pontuação de alinhamento à marca, você pode receber feedback em tempo real sobre o desempenho do seu conteúdo em termos de refletir o tom, o estilo e as diretrizes da sua marca, ajudando a manter a consistência da marca a cada mensagem enviada.</p>
<p>Anteriormente lançado na versão beta, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../content-management/brands.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar tomada de decisão no canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, você pode adicionar políticas de decisão a campanhas e jornadas por email. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
Para mais informações, consulte a <a href="../experience-decisioning/create-decision.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal LINE </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer expandiu seus recursos entre canais para incluir suporte para o canal LINE. Esse aprimoramento permite criar, editar e visualizar experiências LINE, garantindo interações mais personalizadas e envolventes. Com o LINE, você pode se conectar com mais clientes, enviar conteúdo relevante e melhorar seu engajamento.</p>
<p>Anteriormente disponível somente mediante solicitação, o canal LINE já está disponível para todos os usuários (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../../rp_landing_pages/line-landing-page.md">documentação detalhada</a>.</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Teste de simulação de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O teste de simulação da jornada é um modo de publicação especial no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais, sem entrar em contato com clientes reais ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganharem confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para mais informações, consulte a <a href="../building-journeys/journey-dry-run.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID complementar para jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar jornadas usando uma ID de perfil juntamente com outro identificador, como uma ID de pedido, ID de assinatura ou ID de prescrição, permitindo que o mesmo perfil esteja na mesma jornada várias vezes ao mesmo tempo. Isso possibilita cenários como o gerenciamento de vários pedidos ou assinaturas em paralelo, com cada instância seguindo seu próprio caminho pela jornada.</p>
<p>Anteriormente lançado com disponibilidade limitada, o uso de IDs complementares em jornadas já está disponível para todos os ambientes. Nesta versão com disponibilidade geral, o recurso agora permite jornadas de público-alvo de leitura.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Para mais informações, consulte a <a href="../building-journeys/supplemental-identifier.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

### Alertas no produto

Agora, você pode inscrever-se para receber **alertas por email e no produto** sobre lançamentos do produto Journey Optimizer.

Para inscrever-se:

* Acesse as **Preferências da Adobe Experience Cloud**
* Em **Notificações**, procure **Novas versões do Journey Optimizer**
* Habilitar notificações no aplicativo e por email

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Alteração nas condições da jornada {#ee-change@}

A partir de 8 de julho, em novas organizações de clientes, a criação de expressões usando eventos de experiência não será mais aceita no editor de expressão usado em condições de jornada. Como resultado, os eventos de experiência na [fonte de dados da Experience Platform](../datasource/adobe-experience-platform-data-source.md) não poderão ser usados para criar expressões. Abordagens alternativas e práticas recomendadas para criar expressões/lógica com eventos de experiência são apresentadas [aqui](../building-journeys/exp-event-lookup.md).

Não há alteração em como os dados do evento de contexto de jornada são acessados em jornadas unitárias. Nos editores de expressão e personalização, os usuários podem continuar a acessar os dados transmitidos com o evento de jornada inicial.

Saiba mais [nesta seção de Perguntas frequentes](../building-journeys/exp-event-lookup.md#faq-ee).

### Aprimoramentos {#25-7-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

* **Campanhas**

   * **Várias ações de entrada em campanhas**: para simplificar a orquestração de campanhas, agora é possível definir várias ações de entrada em uma mesma campanha. Esse recurso permite que você forneça várias experiências baseadas em código, mensagens no aplicativo, cartões de conteúdo ou ações da web para locais diferentes ao mesmo tempo, cada ação com um conteúdo específico.
     [Leia mais](../campaigns/campaign-action.md#multi-action)

   * **Reorganização do inventário de campanhas**: campanhas programadas e acionadas por API agora são divididas em guias separadas no inventário de campanhas para facilitar a navegação e o gerenciamento.

[Saiba mais](../campaigns/manage-campaigns.md)

* **Gerenciamento de dados**
   * **Atualização de conjuntos de dados do sistema de gestão de decisões**: as ofertas personalizadas e substitutas excluídas agora são marcadas como arquivadas nos conjuntos de dados “decision_object_repository_personalized_offers” e “decision_object_repository_fallback_offers”. Os registros existentes no conjunto de dados não são alterados.

[Saiba mais](../offers/export-catalog/access-dataset.md)

* **Jornadas**
   * **Aprimoramentos das ferramentas de sandbox da jornada**: ao copiar jornadas em várias sandboxes com os recursos de exportação e importação de pacotes, os seguintes recursos também estão disponíveis:
      * Selecionar um evento existente no destino
      * Copiar um evento independentemente de uma jornada
      * Detectar relações de grupos de campos/fontes de dados, vinculando-os no destino, se existirem, ou criando-os, se não existirem.

[Saiba mais](../configuration/copy-objects-to-sandbox.md)

* **Canal: no aplicativo**
   * **Pares de chave/valor no aplicativo**: com mensagens no aplicativo, é possível definir pares de chave e valor para incluir variáveis personalizadas no conteúdo da mensagem. Esses pares de valor e chave permitem transmitir dados adicionais com base na sua configuração e no caso de uso específicos. [Leia mais](../in-app/design-in-app.md)

* **Canal: cartão de conteúdo**

   * **Desqualificação de campanhas com base em regras**: ao editar regras de entrega adicionais, a opção “Regras de entrega” anterior foi substituída por três tipos de regra distintos para controlar melhor o cronograma e a visibilidade das mensagens:
      * Mostrar mensagem se: condições que determinam quando o cartão de conteúdo é mostrado.
      * Ignorar mensagem se: condições que ocultam temporariamente o cartão de conteúdo. Ele pode reaparecer se as condições de exibição forem satisfeitas novamente.
      * Desqualificar mensagem se: condições que impedem permanentemente que o cartão de conteúdo seja mostrado novamente.

[Saiba mais](../content-card/design-content-card.md)

* **Decisão**
   * **APIs das ferramentas de migração**: a equipe do Journey Optimizer está desenvolvendo APIs das ferramentas de migração para migrar entidades da gestão de decisões para a tomada de decisão. Essas ferramentas permitem uma migração fluida entre sandboxes com recursos de resolução de dependência e reversão. Se tiver interesse, entre em contato com o seu representante da Adobe.

* **Personalização**
   * Uma nova função de ajuda, “SHA256”, foi adicionada ao editor de personalização. Essa função é usada para calcular e retornar o hash sha256 de uma string.

[Saiba mais](../personalization/functions/string.md#sha256)


## Notas de versão de junho de 2025 {#25-6-rn}

**Data de lançamento**: 18 de junho de 2025

### Novos recursos {#25-06-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Conjuntos de dados da Adobe Experience Platform na decisão (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponíveis para personalização, os conjuntos de dados da Adobe Experience Platform agora podem ser aproveitados para a decisão. Isso permite estender a definição dos atributos de decisão para dados adicionais nos conjuntos de dados para atualizações em massa que mudam periodicamente, sem precisar atualizar manualmente os atributos um de cada vez. Por exemplo, disponibilidade, tempos de espera etc.</p>
<p>Esse recurso está atualmente disponível para todos os clientes como uma versão beta pública. Entre em contato com o representante da sua conta se desejar obter acesso.</p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/aep-data-exd.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 20 de junho de 2025</p>
</td>
</tr>
</tbody>
</table>

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
<p>Agora é possível definir campos editáveis específicos em modelos de conteúdo JSON ou HTML que habilitam usuários comuns a editar facilmente o conteúdo em uma exibição de formulário na criação do canal de experiência baseada em código, sem a necessidade de manipular qualquer código.<br />Mais do que isso, ao definir os modelos de conteúdo da experiência baseada em código, agora é possível inserir políticas de decisão no modelo, aumentando a capacidade de reutilização e a facilidade de uso.</p>
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
<p>Agora é possível incluir ofertas personalizadas em suas jornadas por meio de uma atividade dedicada de decisão de conteúdo na tela da jornada e usá-las em atividades da jornada, incluindo condições e ações personalizadas.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/content-decision.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Teste de simulação de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O teste de simulação da jornada é um modo de publicação especial no Adobe Journey Optimizer que permite aos profissionais de jornada o teste de uma jornada usando dados de produção reais, sem entrar em contato com clientes reais ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganharem confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.</p>
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
<p>Agora é possível pausar e retomar jornadas. Esse recurso oferece aos profissionais de jornada maior controle e flexibilidade ao permitir que as jornadas ativas sejam temporariamente suspensas sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.</p>
<p>É possível pausar e retomar apenas uma jornada ou executar operações de pausa e retomada em massa para um grupo de jornadas.</p>
<p>Além disso, é possível aplicar filtros globais a jornadas pausadas para excluir perfis com base em seus atributos.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será implantado globalmente em uma versão futura.</p>
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

   * **Janela de duração personalizada** para limitação: um novo campo **Todos** agora está disponível na tela de configuração de conjuntos de regras de canal, permitindo que você aplique regras de limitação de frequência em vários dias, semanas ou meses, dependendo da duração especificada.

   * **Frequência de limitação de redefinição por hora**: agora você pode aplicar a limitação por hora para conjuntos de regras de canal. Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Entre em contato com o atendimento ao cliente para habilitá-la.

   * **Duração diária**: anteriormente em disponibilidade limitada, o limite de frequência “Diário” nos conjuntos de regras do canal agora está disponível para todos os clientes.

  Para obter mais informações, consulte a [documentação detalhada](../conflict-prioritization/channel-capping.md).

* **Experiências baseadas em código**

   * A adição de uma política de decisão agora está disponível em modelos de conteúdo de experiência baseada em código, nos quais ela pode ser usada para aproveitar ofertas em campos de formulário editáveis. [Leia mais](../code-based/code-based-form-fields.md)

   * Na jornada de experiência baseada em código ou na tela de edição de campanha, agora você pode adicionar diretamente uma política de decisão sem abrir o editor de personalização. [Leia mais](../code-based/create-code-based.md#edit-code)

* **Suporte a CSS personalizado no Designer de email**

  O Journey Optimizer agora permite adicionar CSS personalizado ao conteúdo do email diretamente no Designer de email. [Leia mais](../email/custom-css.md)

* **Nova navegação com guias para campanhas**

  Um novo padrão de navegação permite acesso mais rápido à criação de conteúdo e oferece suporte à expansão de configurações em todas as campanhas. [Leia mais](../campaigns/create-campaign.md)

* **Decisão**

   * **Decisão e cópia da sandbox** (data de disponibilidade: 3 de junho de 2025): os objetos de decisão agora podem ser copiados entre sandboxes, simplificando os fluxos de trabalho de teste e implantação. [Leia mais](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **Compatibilidade de atributos de itens de decisão para regras de tomada de decisão** (data de disponibilidade: 4 de junho de 2025) * Agora, você pode utilizar os atributos de itens de decisão para criar regras de tomada de decisão. [Leia mais](../experience-decisioning/rules.md#create)

* **Atualização da API de execução de mensagem interativa** — Data de disponibilidade: 6 de junho de 2025

  A API de execução de mensagem interativa agora permite excluir o cronograma da execução de campanhas futuras. [Leia mais](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}


## Notas de versão de maio de 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Novos recursos {#25-05-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Exibição de calendário para inventários de campanha e jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há uma exibição de calendário disponível nas listas de jornadas e campanhas. Ela permite ver todas as ativações de jornadas e campanhas nas respectivas listas.</p>
<p>Essa alteração está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para solicitar acesso, use <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">este formulário</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obter mais informações, consulte estas seções: <a href="../building-journeys/journey-ui.md">Procurar e filtrar jornadas</a>, <a href="../campaigns/manage-campaigns.md">Acessar campanhas</a>.</p>
<p>Data de disponibilidade: 28 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração de fragmentos de conteúdo do Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a integração do Adobe Experience Manager e do Adobe Journey Optimizer, agora é possível usar com facilidade os fragmentos de conteúdo do Adobe Experience Manager no conteúdo do Journey Optimizer. Essa conexão perfeita facilita o acesso e o uso do conteúdo do AEM diretamente no Journey Optimizer.</p>
<p>Anteriormente disponível para um conjunto limitado de organizações (DL), esse recurso agora está disponível para o público geral com o seguinte aprimoramento: agora é possível definir espaços reservados e mapear valores de personalização na assinatura do fragmento usando o modo Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Para obter mais informações, consulte a <a href="../integrations/aem-fragments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do Dynamic Media com o Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os ativos do Dynamic Media agora estão diretamente disponíveis e acessíveis no Journey Optimizer. Essa integração permite:</p>
<ul>
<li>Gerenciar ativos centralmente com atualizações em tempo real.</li>
<li>Modificar instantaneamente suas configurações de ativos, como largura e altura.</li>
<li>Personalizar modelos do Dynamic Media atualizando o conteúdo e adicionando campos de personalização.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../integrations/aem-dynamic.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID complementar para jornadas acionadas por eventos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar jornadas usando uma ID de perfil juntamente com outro identificador, como uma ID de pedido, ID de assinatura ou ID de prescrição, permitindo que o mesmo perfil esteja na mesma jornada várias vezes ao mesmo tempo. Isso possibilita cenários como o gerenciamento de vários pedidos ou assinaturas em paralelo, com cada instância seguindo seu próprio caminho pela jornada.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/supplemental-identifier.md">documentação detalhada</a>.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simular variações de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de disponibilidade geral, o recurso agora inclui suporte para conteúdo multilíngue e experimentos de conteúdo, permitindo testar variações em diferentes idiomas e tratamentos. Além disso, agora ele é compatível com atributos contextuais (além dos atributos de perfil), permitindo testes de conteúdo ainda mais dinâmicos e específicos.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Para obter mais informações, consulte a <a href="../test-approve/simulate-sample-input.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronizar o cronograma de ler público-alvo com o trabalho de segmentação em lote</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar execuções diárias da jornada após a conclusão da segmentação em lote Essa opção agora está disponível em jornadas agendadas diariamente para todos os clientes. Ela permite definir uma janela de tempo de até 6 horas para aguardar os dados de público-alvo de trabalhos de segmentação em lote, garantindo que as jornadas sejam executadas com os dados mais atualizados ou sejam ignoradas, se não estiverem prontas. </p>
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-audience.md#schedule">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 20 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Provedor de SMS personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite configurar provedores de SMS adicionais além das opções padrão: Sinch, Infobip e Twilio. Com a configuração personalizada do provedor SMS, é possível integrar diretamente provedores de terceiros, aproveitar a personalização avançada de conteúdo para gerar mensagens dinâmicas e gerenciar preferências de consentimento (aceitação e recusa) para garantir a conformidade.</p>
<p>Para obter mais informações, consulte a <a href="../sms/sms-configuration-custom.md">documentação detalhada</a>.</p>
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Data de disponibilidade: 20 de maio de 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível aplicar temas pré-aprovados rapidamente para garantir a consistência da marca em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de forma independente, reduzindo a dependência de equipes de design.</p>
<p>No momento, esse recurso está na versão beta e disponível apenas para clientes beta. Para participar do programa beta, entre em contato com seu representante da Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 14 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisão - Novo construtor de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar fórmulas de classificação de decisão específicas por definir e combinar critérios a partir de uma interface nova e aprimorada. Em vez de contar apenas com uma prioridade de oferta estática, é possível definir fórmulas de classificação personalizadas que combinam pontuações do modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta e sinais contextuais por meio de uma interface guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/ranking/ranking-formulas.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 14 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#25-05-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.


* **Suporte a novos objetos de campanha para cópia da sandbox** — Data de disponibilidade: 15 de maio de 2025

  Ao copiar campanhas em várias sandboxes usando os recursos de exportação e importação de pacotes, as seguintes dependências agora também são copiadas: configurações de canal, variantes e configurações de experimento, políticas e itens de decisão. [Leia mais](../configuration/copy-objects-to-sandbox.md)

* **Pastas para páginas de destino** - Data de disponibilidade: 9 de maio de 2025

  Para gerenciar facilmente as páginas de destino, agora é possível usar pastas para organizá-las com mais eficiência em uma hierarquia estruturada. [Leia mais](../landing-pages/manage-lp.md)

* **Correspondência direta: suporte à chave SSH para conexões SFTP** - Data de disponibilidade: 5 de maio de 2025

  Na configuração de roteamento do arquivo de correspondência direta, além do SFTP existente com autenticação por senha, agora é possível exportar o arquivo de correspondência direta para um servidor SFTP com autenticação por chave SSH. [Leia mais](../direct-mail/direct-mail-configuration.md)

* **Ativação de pílulas para personalização** - Data de disponibilidade: 5 de maio de 2025

  Um novo botão “Pílulas” foi adicionado ao editor de personalização. Quando habilitado, os atributos contextuais e de perfil são exibidos como pílulas, melhorando a legibilidade do código. [Leia mais](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esse recurso será implantado gradualmente em todos os ambientes nos próximos 30 dias.

* **Suporte ao recurso “Redirecionar para URL” no canal da Web** — Data de disponibilidade: 20 de maio de 2025

  O canal da web do Journey Optimizer agora permite redirecionar visitantes para outro URL existente, em vez de criar uma nova variação no editor visual. Esse recurso pode ser usado para realizar experimentos comparando duas páginas completamente diferentes, em vez de apenas alterar alguns elementos em uma página. [Leia mais](../web/create-web.md#web-redirect-to-url)

* **Pastas para modelos e fragmentos** — Data de disponibilidade: 20 de maio de 2025

  As pastas permitem organizar objetos com mais facilidade e eficácia, usando uma hierarquia estruturada. Anteriormente disponíveis para apenas algumas organizações (disponibilidade limitada), as pastas agora estão disponíveis para todos os usuários (disponibilidade geral), permitindo o gerenciamento de modelos e fragmentos de conteúdo. Saiba mais nas seções [Modelos de conteúdo](../content-management/access-content-templates.md#folders) e [Fragmentos](../content-management/manage-fragments.md#folders).

* **Rastreamento de cliques em modelos de email** — Data de disponibilidade: 20 de maio de 2025

  O rastreamento de cliques em elementos `<area>` nos mapas de imagem de conteúdos de email agora é um recurso nativo do [!DNL Journey Optimizer]. Isso visa garantir que as áreas do mapa de imagem recebam o mesmo tratamento de rastreamento que os hiperlinks padrão, o que envolve a inclusão de códigos, dados e parâmetros de rastreamento. [Saiba mais sobre o rastreamento de mensagens](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Painel direito na lista de campanhas** — Data de disponibilidade: 20 de maio de 2025

  Agora, selecionar uma campanha na lista abre um painel que exibe seus detalhes.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## Notas da versão de abril de 2025 {#25-4-rn}

**Data de lançamento**: 29-30 de abril de 2025

### Novos recursos {#25-04-features}

Os novos recursos incluídos nesta versão estão listados abaixo.

<table>
<thead>
<tr>
<th><strong>Editor de personalização - Aprendizado prático</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há um playground de personalização disponível, onde é possível experimentar com expressões de personalização. Ele permite explorar modelos de amostra e conteúdos para ajudar a iniciar e experimentar suas próprias expressões de personalização.</p>
<p>Para obter mais informações, consulte a <a href="../personalization/personalize.md#playground">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 24 de abril de 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Canal LINE </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer expandiu seus recursos entre canais para incluir suporte para o canal LINE. Esse aprimoramento permite criar, editar e visualizar experiências LINE, garantindo interações mais personalizadas e envolventes. Com o LINE, você pode se conectar com mais clientes, enviar conteúdo relevante e melhorar seu engajamento.</p>
<p>O canal LINE é habilitado para clientes do Adobe Journey Optimizer mediante solicitação. Entre em contato com o Atendimento ao cliente da Adobe ou com o(a) representante da Adobe para ativar o recurso em sua organização.</p>
<p>Para obter mais informações, consulte a <a href="../../rp_landing_pages/line-landing-page.md">documentação detalhada</a>.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Métricas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As métricas de jornada agora estão disponíveis, permitindo medir o impacto de suas atividades nas métricas principais do seu negócio e fornecer insights mais claros sobre seu desempenho.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>Para obter mais informações, consulte a <a href="../building-journeys/success-metrics.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 9 de abril de 2025</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Integração do Adobe Express (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora se integra ao Adobe Express, permitindo conectar facilmente seus ativos criativos à orquestração de jornada. Essa integração simplifica o processo de criação e implantação de conteúdo personalizado em campanhas. </p>
<p>No momento, essa integração não está disponível para uso com o Healthcare Shield ou com o Privacy and Security Shield.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Para obter mais informações, consulte a <a href="../integrations/express.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Acionar execuções diárias de jornada após a conclusão da segmentação em lote (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para jornadas agendadas diariamente, uma nova opção permite definir uma janela de tempo de até 6 horas para aguardar os dados de público-alvo de trabalhos de segmentação em lote, garantindo que as jornadas sejam executadas com os dados mais atualizados ou sejam ignoradas, se não estiverem prontas. A opção “Acionar após a avaliação de público-alvo em lote” está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-audience.md#schedule">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Pontuação de alinhamento à marca (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O recurso de pontuação de alinhamento à marca oferece um feedback claro diretamente no Designer de email, ajudando a visualizar se o conteúdo está alinhado ao tom, estilo e diretrizes da marca. Esse recurso está disponível na versão beta.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/brands-score.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### Aprimoramentos {#25-04-improv}

**API de visualização de campanhas**

Há novas APIs disponíveis para visualizar campanhas, além dos recursos existentes de envio de provas. [Leia mais](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**Ferramentas de sandbox**

* **Ferramentas de sandbox para ações personalizadas**

  As ações personalizadas agora são incluídas na lista de objetos do Adobe Journey Optimizer que podem ser copiados usando as ferramentas de sandbox, simplificando o teste e a implantação. [Leia mais](../configuration/copy-objects-to-sandbox.md)

* **Ferramentas de sandbox para campanhas** - Data de disponibilidade: 3 de abril de 2025

  Agora é possível copiar campanhas em várias sandboxes usando recursos de exportação e importação de pacotes. As campanhas são copiadas junto com todos os itens relacionados ao perfil, público-alvo, esquema, mensagens em linha e objetos dependentes. Alguns itens não são copiados, como itens de decisão, rótulos de uso de dados e configurações de idioma. [Leia mais](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personalização**

* **Novo atributo contextual**

  A **ID de perfil da mensagem**, um novo atributo contextual, agora está disponível para seleção no editor de personalização. Este é um atributo orientado por mensagem que identifica exclusivamente as mensagens enviadas para cada perfil direcionado em uma entrega. É possível usar esse identificador exclusivo, por exemplo, como um parâmetro de rastreamento de URL para distinguir cada link aberto ou clicado pelos destinatários.

* **Atributos preenchidos no painel de atributos** - Data de disponibilidade: 2 de abril de 2025

  Por padrão, o painel de atributos no editor de personalização agora mostra apenas atributos preenchidos. Para exibir todos os atributos, use o botão de configurações para desativar a opção **[!UICONTROL Mostrar apenas atributos preenchidos]**. [Leia mais](../personalization/personalization-build-expressions.md)

**Canal de email**

* **Rastreamento personalizado de URL** - Data de disponibilidade: 30 de abril de 2025

  Para aumentar a flexibilidade e o controle sobre as configurações de email, agora é possível personalizar todos os parâmetros de rastreamento de URL de uma só vez na configuração do canal de email, em vez de fazer isso no Designer de email para cada link do conteúdo. [Leia mais](../email/surface-personalization.md#personalize-url-tracking)

* **Designer de email** - Data de disponibilidade: 1º de abril de 2025

  Para melhorar a acessibilidade no Journey Optimizer, agora há dois novos campos disponíveis no Designer de email, os quais correspondem ao elemento `<title>` e ao atributo `lang` no elemento `<html>` do conteúdo do email. Além dessas configurações, é possível definir o campo **[!UICONTROL Pré-cabeçalho]** na seção **[!UICONTROL Corpo]** do email. [Leia mais](../email/email-metadata.md)

**Manuais de casos de uso**

* **Criação e compartilhamento de manuais de estratégia (beta privado)** - Agora é possível criar, gerenciar e compartilhar seus próprios manuais de estratégia de casos de uso. No momento, esse recurso está disponível apenas para algumas organizações como um beta privado. Para obter acesso, entre em contato com o(a) representante da Adobe. [Leia mais](../start/playbooks.md)

**Navegação**

* **Gerenciamento de conteúdo** - Data de disponibilidade: 2 de abril de 2025

  Para gerenciar facilmente seus modelos e fragmentos de conteúdo, agora é possível usar pastas para organizá-los de forma mais eficaz em uma hierarquia estruturada. Saiba mais nas seções [Modelos de conteúdo](../content-management/access-content-templates.md#folders) e [Fragmentos](../content-management/manage-fragments.md#folders).

  >[!AVAILABILITY]
  >
  >Esta melhoria está disponível apenas para um conjunto de organizações (disponibilidade limitada).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## Notas de versão de março de 2025 {#25-3-rn}

### Novos recursos {#25-03-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integração com o Dynamic Media (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os ativos do Dynamic Media agora estão diretamente disponíveis e acessíveis no Journey Optimizer. Essa integração permite:
<ul>
<li>Gerenciar ativos centralmente com atualizações em tempo real</li>
<li>Modificar instantaneamente suas configurações de ativos, como largura e altura</li>
<li>Personalizar modelos do Dynamic Media atualizando o conteúdo e adicionando campos de personalização</li>
</ul>
<p>
<p>Esta integração está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../integrations/aem-dynamic.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integração com o Adobe GenStudio (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para aprimorar a eficiência do marketing e manter a consistência da marca, agora é possível integrar perfeitamente as experiências do GenStudio para marketing de desempenho com o Journey Optimizer. Isso permite que você aproveite a criação de conteúdo com inteligência artificial do GenStudio juntamente com os recursos avançados de orquestração do Journey Optimizer.<p>
<p>O uso da integração do GenStudio no Journey Optimizer está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield (disponibilidade limitada).</p>
<p>Para obter mais informações, consulte a <a href="../integrations/genstudio.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avaliação de público-alvo flexível (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponível para apenas algumas organizações (disponibilidade limitada), a avaliação de público-alvo flexível agora está disponível para todos os usuários (disponibilidade geral). Esse recurso permite executar um trabalho de segmentação sob demanda para públicos-alvo selecionados, garantindo que você sempre tenha os dados de público-alvo mais atualizados antes de direcioná-los para jornadas e campanhas do Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obter mais informações, consulte a <a href="../audience/creating-a-segment-definition.md#flexible">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Aprimoramentos {#25-03-improv}

**Editor de personalização** (data de disponibilidade: 12 de março)

O editor de personalização do Journey Optimizer foi atualizado com novos recursos:
* **Design do editor de código atualizado**: uma interface mais simples e moderna para melhorar a usabilidade e o foco.
* **Pesquisar e substituir**: adição da funcionalidade para localizar e substituir rapidamente o conteúdo no editor.
* **Desfazer e refazer**: permite reverter ou reaplicar facilmente as alterações.
* **Tamanho de fonte personalizável**: permite ajustar o tamanho da fonte do editor para facilitar a leitura.
* **Validação JSON em linha**: fornece validação do lado do cliente em tempo real para conteúdo JSON, a fim de acelerar a detecção de erros.
* **Preenchimento automático para atributos de perfil e contexto**: oferece sugestões inteligentes para simplificar a criação de conteúdo.
* **Realce de sintaxe aprimorado**: melhora a legibilidade por tornar a estrutura do código mais visualmente distinta.

![Vídeo mostrando o novo recurso no editor de personalização](assets/do-not-localize/personalization-editor.gif)

Para obter mais informações, consulte a [documentação detalhada](../personalization/personalization-build-expressions.md).

**Aprovações**

Ao definir as condições para uma política de aprovação, agora há a opção de filtrar por tag e/ou categoria de objeto.

Para obter mais informações, consulte a [documentação detalhada](../test-approve/approval-policies.md).

**Configuração**

* Agora é possível atribuir tags unificadas da Adobe Experience Platform às configurações de canais. Isso permite classificá-las facilmente e melhorar a pesquisa e a navegação em todas as listas. [Saiba mais](../configuration/channel-surfaces.md#channel-config-tags)

* Ao configurar ou editar um subdomínio de email no Journey Optimizer, agora você pode optar por gerenciar o registro DMARC associado por conta própria, se disponível no domínio principal. [Saiba mais](../configuration/dmarc-record.md#set-up-dmarc)

**Regras de negócios**

Agora você pode usar o limite de frequência diário em jornadas e campanhas com segmentação em lote. Para garantir a precisão das regras diárias de limite de frequência, escolha o namespace de prioridade mais alta ao criar uma campanha ou jornada. Saiba mais sobre a prioridade de namespace no [Guia do serviço de identidade da Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Como lembrete, o limite de frequência diária em conjuntos de regras está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.

Para obter mais informações sobre regras de negócios, consulte a [documentação detalhada](../conflict-prioritization/rule-sets.md).

**Modelos de conteúdo**

Os modelos de conteúdo do tipo HTML agora estão obsoletos. Observe que ainda é possível usar os modelos de conteúdo HTML anteriores criados no [!DNL Journey Optimizer]. [Saiba mais sobre modelos de conteúdo](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## Notas da versão de fevereiro de 2025 {#25-02-rn}

**Data de lançamento**: 18 a 19 de fevereiro de 2025


### Novos recursos {#25-02-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Criar e gerenciar regras de negócios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar regras de negócios usando conjuntos de regras. Os conjuntos de regras são grupos de regras que ajudam a limitar as mensagens enviadas em campanhas e ações de jornada entre canais, além de controlar as entradas de perfis nas jornadas.<p>
<p><ul><li>Crie conjuntos de regras de canal para restringir o número de mensagens enviadas por um ou vários canais. Utilize-os em campanhas ou ações de jornada para aplicar as regras definidas no conjunto de regras. O conjunto de regras de canal permite aplicar regras de limite com base nos tipos de comunicação. Por exemplo, defina um conjunto de regras para limitar “mensagens promocionais” e outro para “boletins informativos”. Aplique o conjunto de regras apropriado em sua ação de campanha ou jornada, dependendo do tipo de comunicação que você está enviando.</li>
<li> Crie conjuntos de regras de jornada para controlar entradas de perfil nas jornadas. Limite a frequência com que um perfil pode entrar em uma jornada em um determinado período ou o número de jornadas nas quais um perfil pode ser inscrito simultaneamente. Aplique-as no nível da jornada para garantir um gerenciamento de entradas adequado.</li></ul></p>
<p>Anteriormente disponíveis para um conjunto de organizações (disponibilidade limitada), as regras de negócios agora estão disponíveis para todos os usuários (disponibilidade geral). As regras de negócios do domínio de jornada continuam disponíveis somente para um conjunto limitado de organizações (disponibilidade limitada).</p>
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/rule-sets.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerar páginas de destino com o Assistente de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a ajuda do Assistente de IA, agora é possível criar um conteúdo atrativo para suas páginas de destino, incluindo designs de página inteira, texto personalizado e visuais customizados.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Para obter mais informações, consulte a <a href="../content-management/generative-lp.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marcas com o Assistente de IA (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível configurar suas próprias marcas para definir a identidade visual e verbal da sua marca. </p>
<p>Esse recurso foi lançado como um beta privado para um conjunto limitado de clientes. Ele será disponibilizado progressivamente a todos os clientes em versões futuras.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/brands.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Solucionar problemas de ações personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível validar uma configuração de ação personalizada fazendo chamadas de API reais diretamente do Adobe Journey Optimizer. Esse novo recurso ajuda você a solucionar problemas de ações personalizadas antes ou depois de usá-las em uma jornada. </p>
<p>Para obter mais informações, consulte a <a href="../action/troubleshoot-custom-action.md">documentação detalhada</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avaliação flexível de público-alvo (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A avaliação flexível de público-alvo permite executar um trabalho de segmentação por demanda para públicos-alvo selecionados, garantindo que você sempre tenha os dados do público-alvo mais atualizados antes de direcioná-los em jornadas e campanhas do Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obter mais informações, consulte a <a href="../audience/creating-a-segment-definition.md#flexible">documentação detalhada</a>.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Data de disponibilidade: 28 de janeiro de 2025</p>
</tr>
</tbody>
</table>
</table>


### Aprimoramentos {#25-02-improvements}

As melhorias abaixo estão incluídas na atualização de fevereiro.

* **Tempo de vida do conjunto de dados**: a partir deste mês, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer para novas sandboxes e organizações da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada nas sandboxes de clientes existentes em uma próxima fase.

  Saiba mais sobre esta atualização nas [Perguntas frequentes dedicadas](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Correspondência direta**: um novo tipo de servidor, Zona de destino de dados, agora é compatível com o roteamento de arquivos na configuração do canal de correspondência direta. [Leia mais](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS**: agora é possível gerenciar a entrega de mensagens SMS de pontos de acesso multirregionais substituindo os URLs de entrega, feedback, entrada e retorno de chamada. Para oferecer suporte a isso, um novo campo Substituir URL foi adicionado à configuração Credenciais da API. Essa alteração está disponível somente com o provedor Sinch. [Leia mais](../sms/sms-configuration-sinch.md)

* **Personalização** (Data de disponibilidade: 29 de janeiro de 2025): há novas funções auxiliares de data/hora disponíveis para uso no editor de personalização. [Leia mais](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuração de email**: se você estiver gerenciando o consentimento fora da Adobe, agora será possível definir um endereço de email personalizado para cancelar a inscrição e um URL personalizado para cancelar a inscrição com um clique como parte das configurações do canal de email. [Leia mais](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisão** (Data de disponibilidade: 28 de janeiro de 2025): o serviço de decisão agora oferece suporte a tipos de dados de objeto ao editar o esquema do catálogo de itens. [Leia mais](../experience-decisioning/catalogs.md)
