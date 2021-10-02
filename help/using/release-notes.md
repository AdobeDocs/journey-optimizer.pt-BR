---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7c02f27f0160aea2c2f55c7dc5a8e7c3de3ac159
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 18%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Você também pode consultar as [Atualizações de documentação mais recentes](documentation-updates.md).



## Versão de setembro de 2021 {#september-2021-release}

### Novos recursos

<table>
<thead>
<tr>

<th><strong>Relatórios - Melhor insight para o público-alvo</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Novas métricas estão disponíveis nos relatórios: Targeted e Excluded para mensagens de email e push são visíveis nos relatórios online e global. </br> Para ter acesso às métricas mais recentes, observe que será necessário redefinir os diferentes painéis de relatórios para cada canal e tipo de relatório. Para obter mais informações sobre personalização de painel, consulte a <a href="reports/live-report.md">documentação detalhada.</a></p>
<p>Uma nova coluna na lista de execução de mensagens exibe o número de perfis direcionados para cada execução de mensagem. </p>
<p>Para obter mais informações, consulte a <a href="message-monitoring.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Transmita listas de dados dinamicamente usando ações personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível enviar coleções ou uma lista de dados nos parâmetros de ação personalizados que serão preenchidos dinamicamente no tempo de execução. Há suporte para dois tipos de coleções: coleções simples e coleções de objetos. As ações personalizadas criadas anteriormente continuarão funcionando. </p>
<p>Para obter mais informações sobre coleções, consulte a <a href="building-journeys/collections.md">documentação detalhada</a>. </p>
<p>As funções de filtro e interseção foram adicionadas à lista de funções disponíveis no editor de expressão avançado. Isso oferece mais possibilidades para filtragem e comparação de coleção.</p>
<p>Consulte a documentação nas funções <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">filter</a> e <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionintersect.html">intersett</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decision Management - Personalize your offers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize content added to your offers' representations using the expression editor.</p>
<p>For more information, refer to the <a href="offers/offer-library/creating-personalized-offers.md#content">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Melhorias

**Jornadas**

* Os esquemas e conjuntos de dados gerados pelo sistema que foram criados durante o provisionamento para eventos da etapa agora estão no modo somente leitura, protegendo contra qualquer modificação inadvertida em esquemas críticos. [Saiba mais](reports/sharing-overview.md)
* Rotule a atividade **Wait** com um rótulo que será exibido na tela. O rótulo também é usado em registros de relatórios e modos de teste para identificar claramente o que você está fazendo. [Saiba mais](building-journeys/about-journey-activities.md#best-practices)
* Encontre seus eventos e ações mais rapidamente filtrando elementos nas categorias **Events** e **Action** usando pesquisa. As atividades de orquestração não são mais filtradas. [Saiba mais](building-journeys/using-the-journey-designer.md)
* Ao definir uma condição de ID de evento em um evento com base em regras ou de negócios, o operador &quot;contém&quot; agora fica disponível para tipos de sequências de caracteres de campos. [Saiba mais](event/about-creating.md)

**Configuração de email**

* Quando um pool IP tiver sido associado a uma predefinição de mensagem, você poderá editá-lo, sendo a atualização assíncrona. Você também pode verificar cada status de atualização do pool de IP. [Saiba mais](configuration/ip-pools.md#edit-ip-pool)

## Versão de agosto de 2021 {#august-2021-release}

### Novos recursos

<table>
<thead>
<tr>

<th><strong>Enviar mensagens na melhor hora - Otimização do tempo de envio</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envie seu push ou email automaticamente na melhor hora para cada cliente que interagir com o Adobe Journey Optimizer. A Otimização de tempo de envio, viabilizada pelos serviços de IA do Adobe, prevê o melhor momento para enviar um email ou mensagem de push para maximizar o engajamento com base nas taxas de abertura e cliques do histórico prontas para uso.</p>
<p>No momento, esse recurso está na versão beta e só está disponível para clientes beta. Para participar do programa beta, entre em contato com o Atendimento ao cliente do Adobe.</p>
<p>Para obter mais informações, consulte a <a href="building-journeys/journeys-message.md#send-time-optimization">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Alavancar relacionamentos de schema em eventos de negócios - Gerenciamento de tabela de pesquisa</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aproveitar os relacionamentos entre schemas ao configurar um evento comercial. Isso vem além da capacidade de aproveitar campos de tabelas vinculadas ao configurar um evento unitário, ao usar condições em uma jornada, na personalização da mensagem e na personalização da ação personalizada.</p>
<p>Para obter mais informações, consulte a <a href="event/experience-event-schema.md#leverage_schema_relationships">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>URLs personalizados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os URLs personalizados levam os recipients para páginas específicas de um site ou para um microsite personalizado, dependendo dos atributos do perfil. No Adobe Journey Optimizer, agora é possível adicionar personalização a URLs no conteúdo da mensagem. A personalização do URL pode ser aplicada ao texto e às imagens, e usar os dados do perfil ou dados contextuais.</p>
<p>Para obter mais informações, consulte a <a href="personalization/personalization-syntax.md#perso-urls">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Certifique-se de que seus emails cheguem aos seus usuários - Tentativa de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir o período de nova tentativa por predefinição para garantir que as tentativas não sejam mais executadas quando não forem mais necessárias. Por exemplo, você pode definir o período de nova tentativa como 24 horas para uma mensagem transacional de redefinição de senha contendo um link válido por apenas um dia. Observe que as configurações de repetição se aplicam somente ao canal de email.</p>
<p>Para obter mais informações, consulte a <a href="configuration/retries.md#retry-duration">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Definir endereços a serem excluídos do envio - Lista de supressão</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A adição de endereços de email e domínios à lista de supressão agora está disponível na interface do usuário, um por um, ou no modo em massa por meio de um upload de arquivo CSV.</p>
<p>Para obter mais informações, consulte a <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Melhorias

**Jornadas**

* **Cabeçalhos dinâmicos**  - Agora é possível transmitir dados dinâmicos em parâmetros do cabeçalho HTTP. Esses parâmetros podem ser usados pelos sistemas de integração que recebem as chamadas HTTP da ação de jornada, por exemplo, carimbo de data e hora ou ID de rastreamento. [Saiba mais](action/about-custom-action-configuration.md#url-configuration)
* **Caminhos de URL dinâmicos**  - agora você pode configurar caminhos de URL dinâmicos para ações personalizadas. [Saiba mais](action/about-custom-action-configuration.md#url-configuration)
* A taxa de limitação geral para segmentos de leitura foi alterada de 17.000 para 20.000 mensagens por segundo. [Saiba mais](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interface do usuário**

* **Pesquisa**  - Em cada página, agora é possível pesquisar objetos comerciais e artigos de ajuda diretamente do campo Pesquisa do Experience Cloud unificado. [Saiba mais](user-interface.md#unified-search)
* **Recentes**  - A exibição de elementos recentes da página inicial do Adobe Journey Optimizer agora é estendida para objetos comerciais adicionais. Com esta atualização, os atalhos para o seu acesso recente incluem Mensagens, Jornadas, Segmentos, Esquemas, Conjuntos de dados, Fontes de dados, Eventos, Ações, Fontes e Destinos. [Saiba mais](action/about-custom-action-configuration.md#passing-collection)

**Design de conteúdo**

* **Plano de fundo**  - As imagens de plano de fundo agora são suportadas na visualização ao vivo. [Saiba mais](preview.md)
* **Link de rejeição com um clique**  - É possível inserir um novo tipo de link no seu conteúdo de email: o  **Opt-** outlink permite que os usuários cancelem a assinatura de receberem suas comunicações com apenas um clique, sem serem redirecionados para uma landing page para confirmar a recusa. [Saiba mais](message-tracking.md#one-click-opt-out-link)

**Personalização**

* **Editor de expressão**  - agora é possível adicionar facilmente um valor de fallback ao definir a personalização: quando o campo de personalização estiver vazio para um perfil, o valor de fallback será exibido. [Saiba mais](personalization/functions/helpers.md)

**Configuração de email**

* **Lista de permissões**  - A lista de permissões agora pode ser ativada e desativada em uma sandbox de não produção por meio de uma chamada de API. [Saiba mais](allow-list.md#enable-allow-list)
* **Navegação**  - A lista de supressão, que estava acessível no menu  **Administração > Canais > Configuração de email >** Geral, foi movida para o novo submenu  **Supressão** listsubmenu, que reúne todos os recursos relacionados para facilitar o acesso. [Saiba mais](configuration/manage-suppression-list.md#access-suppression-list)

**Gerenciamento de decisão**

* A maneira de adicionar e configurar representações ao criar uma oferta foi atualizada para melhorar a experiência do usuário. Especificamente, a biblioteca de Ativos agora é exibida somente quando você define o conteúdo do tipo imagem para uma representação. [Saiba mais](offers/offer-library/creating-personalized-offers.md#representations)

### Correções

* Correção de um problema de acessibilidade na navegação da guia de mensagem.
* Correção de um problema de localização nos rótulos do designer de email.
* Correção de um problema ao selecionar mais de um nó em uma jornada e clicar em &quot;Excluir&quot; no painel de propriedades.
* Correção de um problema que impedia a adição de um novo cabeçalho a uma ação usada em uma jornada.
* Agora você pode descobrir o motivo pelo qual uma criação de predefinição de mensagem falhou por meio de um aviso mais explícito na interface do usuário.


## Versão de julho de 2021 {#july-2021-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Usar metadados em suas mensagens - Gerenciamento de tabela de pesquisa</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Enriqueça suas experiências com dados de referência carregados no Journey Optimizer. Os exemplos incluem pesquisar metadados em uma ID de reserva em um evento de experiência ou encontrar informações do produto de uma sku em um evento de experiência para uso na tela. </p>
<p>Agora você pode aproveitar os relacionamentos entre esquemas para usar um conjunto de dados como uma tabela de pesquisa para outro. Em seguida, você pode aproveitar todos os campos das tabelas vinculadas ao configurar um evento unitário, ao usar condições em uma jornada, na personalização da mensagem e na personalização da ação personalizada.</p>
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
* Correção de um problema no Designer de email ao carregar um arquivo HTML em que a folha de estilos interna com a propriedade `background-image` não era compatível.
