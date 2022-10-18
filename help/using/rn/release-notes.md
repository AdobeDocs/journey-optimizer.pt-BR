---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 15dc5e2854358f7f200a54a3f06fa6e98f146efe
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 90%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target=&quot;_blank&quot;}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [Informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.


## Outubro de 2022 {#oct-2022-release}

### Melhorias{#oct-2022-improvements}

**Jornadas**

* O **Forçar a reentrada na recorrência** foi adicionada em parâmetros de programação de segmentos de leitura recorrentes. Essa opção permite que todos os perfis ainda presentes na jornada o saiam automaticamente na próxima execução. Quando a opção estiver desativada, os perfis devem concluir a jornada antes que possam entrar novamente em outra ocorrência. [Saiba mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

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
<p>Isso permite cobrir várias necessidades de mensagens operacionais e transacionais, como redefinições de senha, token OTP, entre outras.</p>
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
<p> O uso do controle de acesso baseado em atributos está atualmente restrito a usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
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
<p>Com sua estrutura de governança DULE (Aplicação e rotulagem de uso de dados), o Journey Optimizer agora pode aproveitar as políticas de governança da Adobe Experience Platform para impedir que campos confidenciais sejam exportados para sistemas de terceiros por meio de ações personalizadas. Se o sistema identificar um campo restrito nos parâmetros de ação personalizados, um erro será exibido, impedindo que você publique a jornada.</p>
<p>O uso de DULE está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../action/action-privacy.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aplicação automática de consentimento (políticas de consentimento)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Adobe Experience Platform permite adotar e aplicar facilmente políticas de marketing para respeitar as preferências de consentimento dos clientes. As políticas de consentimento são definidas na Adobe Experience Platform. No Journey Optimizer, você pode aplicar essas políticas de consentimento às ações personalizadas. Por exemplo, você pode definir políticas de consentimento para excluir clientes que não consentiram em receber comunicações por email, push ou SMS.
<p>Atualmente, a Aplicação automática de consentimento está disponível apenas para organizações que compraram a oferta complementar do Healthcare Shield.</p>
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
<p>O Journey Optimizer permite definir funções de usuário e políticas de acesso para gerenciar permissões de recursos e objetos. Através das <strong>permissões da Adobe Experience Cloud</strong>, é possível criar e gerenciar funções, bem como atribuir as permissões de recurso desejadas para essas funções. As permissões também permitem gerenciar rótulos, sandboxes e usuários associados a uma função específica.</p>
<p> O uso das permissões está atualmente restrito a usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
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
<p>Como usuário do Journey Optimizer, agora você pode acessar alertas do sistema por meio da interface para ser notificado quando a jornada não funcionar conforme o esperado. Você pode visualizar os alertas disponíveis e assiná-los. O primeiro alerta disponível nesta versão avisa se uma atividade Ler segmento não houver processado nenhum perfil durante o intervalo de tempo definido. Mais informações serão disponibilizadas agora que esse fluxo de trabalho está desbloqueado.</p>
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

* O **Conjunto de dados da entidade** agora está disponível como um conjunto de dados pronto para uso no Adobe Journey Optimizer. Esse conjunto de dados de pesquisa inclui metadados para enriquecer as informações dos conjuntos de dados de rastreamento e feedback. Isso ajudará você a melhorar seus relatórios e consultas com dados mais compreensíveis. [Saiba mais](../start/datasets-query-examples.md#entity-dataset)
* Uma nova garantia foi adicionada às jornadas unitárias (que começam com um evento ou uma qualificação de segmento) para impedir que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada no perfil agora será temporariamente bloqueada por 5 minutos. [Saiba mais](../start/guardrails.md#events-g)

**Administração**

* Ao ativar ou desativar a lista de permissões, um novo aviso agora é exibido para detalhar os impactos de cada ação. [Saiba mais](../configuration/allow-list.md#enable-allow-list)
* A interface que permite criar superfícies de canal e pools de IP, gerenciar a lista de supressão e a lista de permissões e configurar o canal de SMS foi atualizada.
* Agora, ao criar a primeira superfície de canal para um determinado subdomínio, o tempo de processamento será de 10 minutos a 10 dias; porém, para superfícies subsequentes que usam esse subdomínio, esse tempo será reduzido para no máximo 3 horas. [Saiba mais](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* A interface de criação de predefinições de página de destino e subdomínios de página de destino foi atualizada. [Saiba mais](../configuration/lp-subdomains.md)

**Controles de auditoria**

* Com o Journey Optimizer, você pode identificar as ações executadas pelos usuários no sistema em vários serviços e recursos, como campanhas, jornadas, mensagens, páginas de destino etc. Os recursos de log de auditoria agora incluem alterações em várias outras ações e são registrados automaticamente conforme a atividade ocorre. Saiba mais [nesta página](../privacy/audit-logs.md).

**Suporte para arquivamento**

* O novo **Conjunto de dados da entidade** inclui um campo modelo que permite exportar o formato e a estrutura de anúncio das mensagens enviadas em todos os canais para fins de arquivamento. [Saiba mais](../configuration/archiving-support.md)

**Páginas de destino**

* Agora é possível usar dados contextuais provenientes de outra página dentro da mesma página de destino. Por exemplo, se você vincular uma caixa de seleção a uma lista de assinaturas na página de destino principal, poderá usar essa lista de assinaturas na subpágina de agradecimento. [Saiba mais](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Outras alterações{#sept-2022-other}

* O modo de disparo de jornada foi substituído pelo modo de entrega rápida de campanha. [Saiba mais](../campaigns/create-campaign.md#rapid-delivery)
* Para melhorar o desempenho, os grupos de campos de evento de experiência não podem mais ser usados em jornadas que começam com um segmento de leitura, uma qualificação de segmento ou uma atividade de evento comercial. Essa alteração se aplica somente a novas jornadas. As existentes manterão o comportamento atual. [Saiba mais](../start/guardrails.md#expression-editor)
* A limitação de 1 hora para jornadas de segmento de leitura programadas foi removida. Essas jornadas agora podem ser executadas sem atraso.

