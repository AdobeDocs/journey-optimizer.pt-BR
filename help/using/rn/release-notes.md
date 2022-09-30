---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 18%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target=&quot;_blank&quot;}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [Informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Versão de setembro de 2022{#sept-2022-release}

### Novos recursos{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Conteúdo dinâmico e novo construtor de regras condicionais</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar conteúdo dinâmico para adaptar o conteúdo de suas mensagens com base em regras condicionais.</p> 
<p>Regras condicionais são criadas usando um construtor de regras visuais no Editor de expressão, onde você pode armazená-las para reutilização adicional em suas jornadas e campanhas.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Para obter mais informações, consulte a <a href="../personalization/get-started-dynamic-content.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campanhas acionadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além das campanhas programadas existentes, agora é possível criar campanhas acionadas por API no Journey Optimizer e chamá-las de um sistema externo usando APIs.</p>
<p>Isso permite cobrir várias necessidades operacionais e de mensagens transacionais, como redefinições de senha, token OTP, entre outras.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Para obter mais informações, consulte a <a href="../campaigns/api-triggered-campaigns.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Controle de acesso a dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Por meio do controle de acesso baseado em atributos, os administradores podem controlar o acesso a objetos específicos com base em determinados atributos. Esses atributos podem ser metadados adicionados a um objeto, como rótulos. A partir desta versão, os administradores também poderão definir funções de usuário que tenham acesso somente a campos e/ou objetos específicos e dados que correspondam a esses campos e/ou objetos.</p>
<p> O uso do controle de acesso baseado em atributos está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Para obter mais informações, consulte a <a href="../administration/object-based-access.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Governança e privacidade de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com sua estrutura de governança DULE (Label Usage Labeling and Enforcement), a Journey Optimizer agora pode aproveitar as políticas de governança da Adobe Experience Platform para impedir que campos confidenciais sejam exportados para sistemas de terceiros por meio de ações personalizadas. Se o sistema identificar um campo restrito nos parâmetros de ação personalizados, um erro será exibido, impedindo que você publique a jornada.</p>
<p>O uso de DULE (Label Usage Labeling and Enforcement) está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../action/action-privacy.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aplicação automática do consentimento (políticas de consentimento)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Experience Platform permite que você adote e aplique facilmente políticas de marketing para respeitar as preferências de consentimento dos clientes. As políticas de consentimento são definidas no Adobe Experience Platform. No Journey Optimizer, você pode aplicar essas políticas de consentimento às ações personalizadas. Por exemplo, você pode definir políticas de consentimento para excluir clientes que não consentiram em receber email, push ou comunicação por SMS.
<p>Atualmente, a Aplicação de consentimento automatizada está disponível apenas para organizações que compraram a oferta complementar do Healthcare Shield.</p>
<p>Para obter mais informações, consulte a <a href="../action/consent.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerenciamento de permissões</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Journey Optimizer oferece suporte à definição de funções de usuário e políticas de acesso para gerenciar permissões para recursos e objetos. Através de <strong>Permissões do Adobe Experience Cloud</strong>, é possível criar e gerenciar funções, bem como atribuir as permissões de recurso desejadas para essas funções. As permissões também permitem gerenciar rótulos, sandboxes e usuários associados a uma função específica.</p>
<p> O uso de Permissões está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../administration/attribute-based-access.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertas e monitoramento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como usuário do Journey Optimizer, agora você pode acessar alertas do sistema por meio da interface do usuário para ser notificado quando o jornada não funcionar conforme o esperado. Você pode exibir os alertas disponíveis e assinar eles. O primeiro alerta disponível nesta versão avisa se uma atividade Ler segmento não processou nenhum perfil durante o período de tempo definido. Mais informações serão disponibilizadas agora que esse workflow está desbloqueado.</p>
<p>Para obter mais informações, consulte a <a href="../reports/alerts.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Melhorias{#sept-2022-improvements}

**Jornadas**

* O **Conjunto de dados da entidade** O agora está disponível como um conjunto de dados pronto para uso no Adobe Journey Optimizer. Esse conjunto de dados de pesquisa inclui metadados para enriquecer as informações dos conjuntos de dados de rastreamento e feedback. Isso ajudará você a melhorar seus relatórios e consultas com dados mais compreensíveis. [Saiba mais](../start/datasets-query-examples.md#entity-dataset)
* Uma nova garantia foi adicionada às jornadas unitárias (começando com um evento ou uma qualificação de segmento) para impedir que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil agora será temporariamente bloqueada por padrão por 5 minutos. [Saiba mais](../start/guardrails.md#events-g)

**Administração**

* Ao ativar ou desativar a lista de permissões, um novo aviso agora é exibido para detalhar os impactos de cada ação. [Saiba mais](../configuration/allow-list.md#enable-allow-list)
* A interface do usuário para criar superfícies de canal, criar pools de IP, gerenciar a lista de supressão e a lista de permissões e configurar o canal SMS foi atualizada.
* Agora, ao criar a superfície do primeiro canal para um determinado subdomínio, o tempo de processamento levará de 10 minutos a 10 dias e apenas 3 horas para superfícies subsequentes usando esse subdomínio. [Saiba mais](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* A interface do usuário para criar predefinições de página de aterrissagem e subdomínios de página de aterrissagem foi atualizada. [Saiba mais](../configuration/lp-subdomains.md)

**Controlos de auditoria**

* Com o Journey Optimizer, você pode identificar ações executadas pelos usuários no sistema em vários serviços e recursos, como campanhas, jornadas, mensagens, landing pages etc. Os recursos de log de auditoria agora incluem alterações em várias outras ações e são registrados automaticamente conforme a atividade ocorre. Saiba mais [nesta página](../privacy/audit-logs.md).

**Suporte para arquivamento**

* O novo **Conjunto de dados da entidade** inclui um campo Template que permite exportar o formato e a estrutura das mensagens enviadas em todos os canais para fins de arquivamento. [Saiba mais](../configuration/archiving-support.md)

**Páginas de destino**

* Agora é possível usar dados contextuais provenientes de outra página dentro da mesma landing page. Por exemplo, se você vincular uma caixa de seleção a uma lista de assinaturas na página inicial principal, poderá usar essa lista de assinaturas na subpágina &quot;obrigado&quot;. [Saiba mais](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Outras alterações{#sept-2022-other}

* O Modo de Burst do Jornada foi substituído pelo modo de delivery Campaign Rapid. [Saiba mais](../campaigns/create-campaign.md#rapid-delivery)
* Para melhorar o desempenho, os grupos de campos de evento da Experiência não podem mais ser usados em jornadas que começam com um segmento Lido, uma qualificação de Segmento ou uma atividade de evento comercial. Essa alteração se aplica somente a novas jornadas. Os existentes manterão o comportamento atual. [Saiba mais](../start/guardrails.md#expression-editor)
* A limitação de 1 hora para jornadas de segmento de leitura programadas foi removida. Essas jornadas agora podem ser executadas sem atraso.

