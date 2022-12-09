---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão 2022
description: Notas de versão do Journey Otimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '3479'
ht-degree: 0%

---

# Notas de versão 2022 {#release-notes-2022}

Esta página lista todos os recursos e melhorias para [!DNL Journey Optimizer] lançado em 2022.


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
<p>Para obter mais informações, consulte <a href="../personalization/get-started-dynamic-content.md">documentação detalhada</a>.
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
<p>Além das campanhas programadas existentes, agora é possível criar campanhas acionadas por API no Journey Otimizer e invocá-las de um sistema externo usando APIs.</p>
<p>Isso permite cobrir várias necessidades operacionais e de mensagens transacionais, como redefinições de senha, token OTP, entre outras.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Para obter mais informações, consulte <a href="../campaigns/api-triggered-campaigns.md">documentação detalhada</a>.
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
<p>Para obter mais informações, consulte <a href="../administration/object-based-access.md">documentação detalhada</a>.
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
<p>Com sua estrutura de governança DULE (Label Usage Labeling and Enforcement), o Journey Otimizer agora pode aproveitar as políticas de governança da Adobe Experience Platform para impedir que campos confidenciais sejam exportados para sistemas de terceiros por meio de ações personalizadas. Se o sistema identificar um campo restrito nos parâmetros de ação personalizados, um erro será exibido, impedindo que você publique a jornada.</p>
<p>O uso de DULE (Label Usage Labeling and Enforcement) está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte <a href="../action/action-privacy.md">documentação detalhada</a>.
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
<p>A Adobe Experience Platform permite que você adote e aplique facilmente políticas de marketing para respeitar as preferências de consentimento dos clientes. As políticas de consentimento são definidas na Adobe Experience Platform. No Journey Otimizer, você pode aplicar essas políticas de consentimento às suas ações personalizadas. Por exemplo, você pode definir políticas de consentimento para excluir clientes que não consentiram em receber email, push ou comunicação por SMS.
<p>Atualmente, a Aplicação de consentimento automatizada está disponível apenas para organizações que compraram a oferta complementar do Healthcare Shield.</p>
<p>Para obter mais informações, consulte <a href="../action/consent.md">documentação detalhada</a>.
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
<p>O Journey Otimizer oferece suporte à definição de funções de usuário e políticas de acesso para gerenciar permissões para recursos e objetos. Através de <strong>Permissões da Adobe Experience Cloud</strong>, é possível criar e gerenciar funções, bem como atribuir as permissões de recurso desejadas para essas funções. As permissões também permitem gerenciar rótulos, sandboxes e usuários associados a uma função específica.</p>
<p> O uso de Permissões está atualmente restrito a clientes selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte <a href="../administration/attribute-based-access.md">documentação detalhada</a>.
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
<p>Como usuário do Journey Otimizer, agora você pode acessar alertas do sistema por meio da interface do usuário para ser notificado quando as jornadas não funcionarem conforme o esperado. Você pode exibir os alertas disponíveis e assinar eles. O primeiro alerta disponível nesta versão avisa se uma atividade Ler segmento não processou nenhum perfil durante o período de tempo definido. Mais informações serão disponibilizadas agora que esse workflow está desbloqueado.</p>
<p>Para obter mais informações, consulte <a href="../reports/alerts.md">documentação detalhada</a>.
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

* O **Conjunto de dados da entidade** O agora está disponível como um conjunto de dados pronto para uso no Adobe Journey Otimizer. Esse conjunto de dados de pesquisa inclui metadados para enriquecer as informações dos conjuntos de dados de rastreamento e feedback. Isso ajudará você a melhorar seus relatórios e consultas com dados mais compreensíveis. [Saiba mais](../data/datasets-query-examples.md#entity-dataset)
* Uma nova garantia foi adicionada a jornadas unitárias (começando por um evento ou uma qualificação de segmento) para impedir que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil agora será temporariamente bloqueada por padrão por 5 minutos. [Saiba mais](../start/guardrails.md#events-g)

**Administração**

* Ao ativar ou desativar a lista de permissões, um novo aviso agora é exibido para detalhar os impactos de cada ação. [Saiba mais](../configuration/allow-list.md#enable-allow-list)
* A interface do usuário para criar superfícies de canal, criar pools de IP, gerenciar a lista de supressão e a lista de permissões e configurar o canal SMS foi atualizada.
* Agora, ao criar a superfície do primeiro canal para um determinado subdomínio, o tempo de processamento levará de 10 minutos a 10 dias e apenas 3 horas para superfícies subsequentes usando esse subdomínio. [Saiba mais](../configuration/channel-surfaces.md#create-channel-surface)
* A interface do usuário para criar predefinições de página de aterrissagem e subdomínios de página de aterrissagem foi atualizada. [Saiba mais](../landing-pages/lp-subdomains.md)

**Controlos de auditoria**

* Com o Journey Otimizer, você pode identificar ações executadas pelos usuários no sistema em vários serviços e recursos, como campanhas, jornadas, mensagens, landing pages etc. Os recursos de log de auditoria agora incluem alterações em várias outras ações e são registrados automaticamente conforme a atividade ocorre. Saiba mais [nesta página](../privacy/audit-logs.md).

**Suporte para arquivamento**

* O novo **Conjunto de dados da entidade** inclui um campo Template que permite exportar o formato e a estrutura das mensagens enviadas em todos os canais para fins de arquivamento. [Saiba mais](../configuration/archiving-support.md)

**Landing pages**

* Agora é possível usar dados contextuais provenientes de outra página dentro da mesma landing page. Por exemplo, se você vincular uma caixa de seleção a uma lista de assinaturas na página inicial principal, poderá usar essa lista de assinaturas na subpágina &quot;obrigado&quot;. [Saiba mais](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Outras alterações{#sept-2022-other}

* O modo Journey Burst foi substituído pelo modo de delivery Campaign Rapid. [Saiba mais](../campaigns/create-campaign.md#rapid-delivery)
* Para melhorar o desempenho, os grupos de campos de evento Experiência não podem mais ser usados em jornadas que começam com um segmento Lido, uma qualificação de Segmento ou uma atividade de evento comercial. Essa alteração se aplica somente a novas jornadas. Os existentes manterão o comportamento atual. [Saiba mais](../start/guardrails.md#expression-editor)
* A limitação de 1 hora para jornadas de segmento de leitura agendadas foi removida. Essas jornadas agora podem ser executadas sem atraso.




## Versão de agosto de 2022 {#aug-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Criar e gerenciar campanhas no Journey Otimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use as campanhas do Journey Otimizer para fornecer conteúdo único a um segmento específico usando vários canais. Ao usar jornadas, as ações são projetadas para serem executadas em sequência. Com campanhas, as ações são executadas simultaneamente, imediatamente ou com base em um agendamento especificado. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Saiba como criar uma campanha no <a href="../campaigns/get-started-with-campaigns.md">documentação detalhada</a> e <a href="https://video.tv.adobe.com/v/346680">vídeo de recurso</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Enviar SMS para seus usuários (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar, personalizar e enviar SMS no Journey Otimizer, por meio de uma integração com o <b>Sininho</b> ou <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Saiba como criar e enviar um SMS neste <a href="../sms/create-sms.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Melhorias

**Relatório**

* A tabela e o gráfico de políticas de consentimento agora estão disponíveis nos relatórios globais da jornada. Esses widgets permitem rastrear os perfis excluídos das políticas em suas ações personalizadas. [Saiba mais](../reports/journey-global-report.md#journey-global)

   Para ter acesso aos widgets mais recentes, observe que será necessário redefinir os diferentes painéis de relatórios. Para obter mais informações sobre personalização de painel, consulte [documentação detalhada](../reports/global-report.md).

**Administração**

* Agora é possível atualizar o número de telefone principal a ser usado para o canal SMS. [Saiba mais](../configuration/primary-email-addresses.md)


## Versão de julho de 2022 {#july-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Novo fluxo de mensagens em linha</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Otimizer fornece um novo fluxo para a criação de mensagens em jornadas. As mensagens em linha salvarão os usuários tempo significativo e simplificarão o processo do fluxo de trabalho para criar e entregar um email, uma notificação por push ou um SMS no Journey Otimizer. Ao remover mensagens como uma etapa separada e, em vez disso, torná-las editáveis em linha como parte de uma ação na Tela de jornada, os usuários precisarão clicar em menos botões e navegar por menos telas para projetar e editar seu conteúdo.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Controle de acesso baseado em atributos (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível identificar campos de esquema com rótulos que definem escopos organizacionais ou de uso de dados. Os administradores podem usar a interface Permissões para definir políticas de acesso que cubram campos de esquema XDM e gerenciar melhor o acesso dado aos usuários ou grupos de usuários (usuários internos, externos ou de terceiros), e gerenciar o acesso a tipos específicos de dados (ou seja, dados pessoais confidenciais/SPD).</p>
<p>O uso do controle de acesso baseado em atributos está atualmente restrito aos usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte <a href="../administration/attribute-based-access.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trabalhos de decisão em lote</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode executar tarefas de decisão em lote a partir da interface do usuário, de modo que não precise que um desenvolvedor execute tarefas de api em lote e possa reduzir o tempo necessário para o marketing. Essa nova interface permite criar tarefas e gerenciar trabalhos atuais/anteriores.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Para obter mais informações, consulte <a href="../offers/batch-delivery.md">documentação detalhada.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Use automaticamente a oferta com melhor desempenho em suas decisões (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar sistemas de modelos de otimização personalizados no gerenciamento de decisões. Esse novo tipo de modelo permite otimizar e personalizar ofertas com base em segmentos e oferecer desempenho.</p>
<p>O uso de modelos de AI de otimização personalizada está atualmente restrito a usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obter mais informações, consulte <a href="../offers/ranking/personalized-optimization-model.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* **Encerrar uma jornada** - Na tela da jornada, a variável **End** foi removida da paleta. Tags finais agora são adicionadas por padrão no final de cada caminho e não podem ser removidas. Essa melhoria permite melhor fornecer informações sobre onde um cliente abandonou a jornada, sem nenhuma ação necessária do profissional de jornada. Consulte a [documentação](../building-journeys/end-journey.md) e [vídeo de recurso](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* O **Fuso horário do perfil** agora está desmarcada por padrão nas propriedades da jornada. [Saiba mais](../building-journeys/timezone-management.md#timezone-from-profiles)

**Mensagens**

* As predefinições de mensagem agora são **superfícies dos canais**. [Saiba mais](../configuration/channel-surfaces.md)

**Administração**

* **Edição de registro PTR** - Agora, ao atualizar um registro PTR, o tempo de processamento levará apenas 3 horas. [Saiba mais](../configuration/ptr-records.md#processing)

* **Interface de usuário da lista permitida** - Agora você pode usar a interface do usuário do Journey Otimizer para adicionar novos endereços de email ou domínios à lista permitida. [Saiba mais](../configuration/allow-list.md)

* **Atualização lógica de lista permitida** - Agora a lógica da lista permitida se aplica assim que o recurso é ativado, mesmo que a lista esteja vazia. [Saiba mais](../configuration/allow-list.md#logic)

* **Parâmetros de rastreamento de URL** - Agora você pode usar o Editor de expressão para configurar parâmetros de rastreamento de URL em suas superfícies de email (ou seja, predefinições). [Saiba mais](../email/email-settings.md#url-tracking)

**Gestão de decisões**

* **Tamanho do público-alvo** - Um novo componente de estimativa de tamanho de público-alvo agora é exibido na interface do usuário ao criar uma regra de decisão, ao selecionar um segmento ou uma regra para definir uma qualificação de oferta ou ao adicionar um segmento ou uma regra a um escopo de decisão.


## Versão de junho de 2022 {#june-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Enviar SMS para seus usuários (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar, personalizar e enviar SMS no Journey Otimizer, por meio de uma integração com o <b>Sininho</b> ou <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>No momento, o canal SMS está disponível apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com seu representante da Adobe.</p>
<p>Saiba como criar e enviar um SMS neste <a href="../sms/create-sms.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Encontre imagens mais impactantes mais rapidamente com a integração com o Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O plug-in de integração do Adobe Stock e do Adobe Journey Otimizer Email Designer fornece aos clientes uma maneira fácil de navegar, licenciar e salvar imagens para uso na criação de mensagens. </br> O novo <b>Localizar fotos semelhantes do Stock</b> também permite localizar fotos de Estoque que corresponderão ao conteúdo, cor e composição de suas imagens. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Para obter mais informações, consulte <a href="../email/stock.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar Cco de email em todos os seus emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o recurso Email Cco (cópia cega de carbono) para armazenar emails enviados pelo Adobe Journey Otimizer. Ative essa opção nas predefinições de email para que cada email enviado seja copiado para o CCO.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Para obter mais informações, consulte <a href="../configuration/archiving-support.md#bcc-email">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copiar objetos entre sandboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível recriar as experiências de uma sandbox do Journey Otimizer para outra, por exemplo, de uma sandbox de não produção para uma sandbox de produção. Esse novo recurso copia uma jornada inteira, incluindo quaisquer objetos dos quais a jornada depende para ser executada corretamente, de um ambiente a outro. Além de Jornadas, também é possível copiar outros componentes, como Ofertas, Mensagens, Esquemas, Conjuntos de dados, Fontes de dados, Eventos e Ações.</p>
<p>Para obter mais informações, consulte <a href="../building-journeys/copy-to-sandbox.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>




### Melhorias

**Gestão de decisões**

* **Suporte a arquivos HTML e JSON** - Agora é possível arrastar e soltar arquivos HTML e JSON externos da biblioteca do Adobe Experience Cloud Asset no conteúdo de representação da oferta. [Saiba mais](../offers/offer-library/add-representations.md#html-json)


**Email**

* **Salvar como modelo** - Agora você pode salvar um conteúdo de email como modelo e reutilizá-lo ao criar outras mensagens. [Saiba mais](../email/email-templates.md)


**Administração**

* **Visualizar parâmetros de URL de rastreamento** - Ao configurar uma predefinição de mensagem, se você definir parâmetros de rastreamento de URL, uma visualização dinâmica do URL de rastreamento resultante será exibida. [Saiba mais](../email/email-settings.md#url-tracking)

* **Edição de predefinição de mensagem** - Agora, ao atualizar uma predefinição de mensagem, o tempo de processamento só pode levar até 3 horas. [Saiba mais](../configuration/channel-surfaces.md#edit-channel-surface)

* **Edição de pool de IPs** - Agora, ao atualizar um pool IP, o tempo de processamento só pode demorar até 3 horas. [Saiba mais](../configuration/ip-pools.md#edit-ip-pool)




## Versão de maio de 2022 {#may-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Regras de frequência de mensagem</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir regras de negócios entre canais que excluirão automaticamente perfis excessivamente solicitados de mensagens e ações.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Para obter mais informações, consulte <a href="../configuration/frequency-rules.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerenciamento de decisões - Modelo de otimização automática de classificação AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar sistemas de modelo treinados no Gerenciamento de decisões. Esse novo recurso classifica as ofertas para exibição em um determinado perfil.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>Para obter mais informações, consulte <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Logs de auditoria do Journey Otimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode monitorar ações executadas por usuários nos recursos do Adobe Journey Otimizer.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Para obter mais informações, consulte <a href="../privacy/audit-logs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Personalização**

* **Nova função auxiliar para ocultação de caracteres** - O `mask` A função auxiliar permite substituir uma parte de uma string por caracteres &quot;X&quot;. [Saiba mais](../personalization/functions/string.md#mask)

**Landing pages**

* **Landing pages sem um formulário** - Agora é possível criar e publicar uma landing page que não contenha um formulário e não exija nenhuma ação dos visitantes.
* **Templates de landing page** - Agora é possível salvar uma landing page como template e reutilizá-la ao criar outras landing pages. [Saiba mais](../landing-pages/lp-templates.md)
* **Voltar à página principal** - Agora é possível adicionar um link para a página primária a partir de qualquer subpágina na mesma página de aterrissagem.
* **Suporte a JavaScript personalizado** - Agora é possível adicionar JavaScript personalizado ao conteúdo da página de aterrissagem para executar estilos avançados ou adicionar comportamentos personalizados às páginas de aterrissagem.    [Saiba mais](../landing-pages/lp-custom-js.md)

**Jornadas**

* **Ler segmento** - As jornadas de segmento de leitura única agora são movidas para o status Finished 30 dias após a execução da jornada. Para segmentos de Leitura agendados, é de 30 dias após a execução da última ocorrência. [Saiba mais](../building-journeys/read-segment.md)
* **Editor de expressão** - O [limite](../building-journeys/functions/functionlimit.md) foi adicionada para permitir que você limite o número de itens de uma lista. O [sort](../building-journeys/functions/functionsort.md) agora permite classificar um objeto de lista. O suporte a listObject também foi adicionado ao [disctinct](../building-journeys/functions/functiondistinct.md) e [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) funções.

**Administração**

* **Atualização do painel de uso da licença** - O painel de uso da licença disponível na [!DNL Adobe Journey Optimizer] a interface do usuário agora reflete o valor preciso da variável **Licenciado** Riqueza média do perfil. Você verá uma queda nessa representação de métrica, o que significa que o limite de licença agora é relatado corretamente. [Saiba mais](../segment/license-usage.md)


## Versão de abril de 2022 {#april-2022-release}

### Melhorias

**Landing pages**

* **Nova opção para caixas de seleção de aceitação/rejeição** - Agora é possível inserir uma única caixa de seleção para aceitação/recusa nas landing pages de assinatura. Os usuários precisam marcar a caixa para consentir (aceitar) e desmarcá-la para remover seu consentimento (recusar). [Saiba mais](../landing-pages/design-lp.md#define-lp-specific-content)

* **Preenchimento prévio de campos de landing pages** - Agora é possível dar aos usuários a capacidade de preencher previamente os campos de landing page com informações de perfil. [Saiba mais](../landing-pages/create-lp.md#configure-primary-page)

**Gestão de decisões**

* **API de decisão no Edge** - A API do Edge Decisioning pode fornecer e renderizar ofertas personalizadas que são gerenciadas no gerenciamento de decisões. É possível criar suas ofertas e outros objetos relacionados usando a interface do usuário (UI) ou as APIs do gerenciamento de decisão. [Saiba mais](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administração**

* **Duração do envio de PTR** - A duração para a edição de PTR entrar em vigor agora é de algumas horas. [Saiba mais](../configuration/ptr-records.md#processing)

**Design de email**

* **20 novos modelos de email** agora estão disponíveis para criar seu conteúdo de email no Journey Otimizer.

**Interface do usuário**

* **Ajuda contextual na interface do usuário do Journey Otimizer** - Links de ajuda contextual foram adicionados a várias páginas no Journey Otimizer. Quando disponível, clique no ícone &quot;i&quot; para exibir uma descrição rápida da funcionalidade atual e acessar artigos relacionados.

**Integração com o Adobe Campaign Standard**

Como cliente do Adobe Campaign Standard, agora você pode enviar emails, notificações por push e SMS usando o Journey Otimizer. Use as novas ações integradas para aproveitar os recursos de Mensagens transacionais do Campaign Standard no Journey Otimizer.  [Saiba mais](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Versão de março de 2022 {#march-2022-release}

### Melhorias

**Jornadas**

* Para evitar campos desnecessários no schema de perfil unificado, o schema do Evento de etapa de jornada não é mais habilitado para perfis por padrão. Se necessário, você pode ativá-lo. [Saiba mais](../reports/sharing-overview.md)
* Os novos eventos de etapa relacionados a trabalhos de exportação agora são enviados pelo Journey Otimizer para a Adobe Experience Platform. Exemplos de consultas foram adicionados à documentação. [Saiba mais](../reports/query-examples.md)

**Gestão de decisões**

* Agora é possível especificar se o limite de oferta é aplicado a todos os usuários ou a um perfil específico, bem como a todas as disposições ou por disposição. [Saiba mais](../offers/offer-library/add-constraints.md#capping)
* A API de decisão em lote permite que as organizações usem a funcionalidade de gerenciamento de decisões para todos os perfis em um determinado segmento em uma chamada. O conteúdo da oferta para cada perfil no segmento é colocado em um conjunto de dados AEP, onde está disponível para fluxos de trabalho em lote personalizados. [Saiba mais](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administração**

* Agora é possível ativar/desativar o link de cancelamento de subscrição no/do cabeçalho do email no nível predefinido da mensagem e definir um URL de cancelamento de subscrição personalizado no nível da mensagem. [Saiba mais](../configuration/channel-surfaces.md#list-unsubscribe)
* A lista permitida agora poderá ser ativada e desativada por meio da variável [!DNL Journey Optimizer] interface em sandboxes de produção e não produção. [Saiba mais](../configuration/allow-list.md#enable-allow-list)

**Personalização**

* Agora você pode salvar mais de 40 expressões de personalização na biblioteca. [Saiba mais](../personalization/personalization-library.md)

## Versão de fevereiro de 2022 {#feb-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Páginas de aterrissagem de assinatura</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar e criar páginas de aterrissagem no Journey Otimizer e direcionar seus usuários para formulários online, onde eles podem aceitar ou recusar receber suas comunicações ou assinar um serviço específico, como um boletim informativo.</p>
<p>Para obter mais informações, consulte <a href="../landing-pages/create-lp.md">documentação detalhada</a> e relacionadas <a href="../landing-pages/lp-use-cases.md">caso de uso de exemplo</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nova biblioteca de expressão de personalização</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Otimizer agora fornece uma biblioteca onde você pode acessar expressões de personalização predefinidas. Essas expressões são configuradas por usuários administradores.</p>
<p>Para obter mais informações, consulte <a href="../personalization/personalization-library.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Transmita informações para rastrear suas mensagens com parâmetros de rastreamento do UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No conteúdo da mensagem do Journey Otimizer, é possível adicionar parâmetros de UTM aos links: eles podem fornecer dados adicionais sobre esse link e ajudar a identificar onde e por que uma pessoa clicou em seu link.</p>
<p>Para obter mais informações, consulte <a href="../configuration/channel-surfaces.md#configure-email-settings">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Para otimizar o desempenho, todas as jornadas no modo de teste que não foram acionadas por uma semana agora serão retornadas ao status Rascunho . [Leia mais](../building-journeys/testing-the-journey.md#important_notes)
* A integração entre o Journey Otimizer e o Adobe Campaign Classic foi otimizada para melhorar o desempenho. A configuração padrão de limitação foi alterada para 4000 chamadas / 5 minutos.    [Leia mais](../action/acc-action.md#important-notes)

**Relatório**

* Os deliveries agora podem ser filtrados dependendo de seu status:
   * Na lista Message Execution , agora é possível excluir provas da lista de deliveries.
   * Nos seus relatórios Live/Global, você pode optar por excluir eventos de teste.

* Agora você pode acessar os relatórios em Enviar dados de Otimização de Tempo: o número de pessoas que eram mensagens imediatamente e o número de pessoas que receberam mensagens com otimização por 1 hora, otimização por 2 horas etc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestão de decisões**

* As classificações e a classificação de AI agora são agrupadas em uma única guia.

## Versão de janeiro de 2022 {#january-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Jornadas - Otimize seu aumento de IP com as condições de limite de perfil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ao configurar um <strong>Condição</strong> em uma jornada, agora você pode definir um limite de perfil. Esse novo tipo de condição permite definir um número máximo de perfis para um caminho de jornada. Quando esse limite é atingido, os perfis de entrada assumem um caminho alternativo. Isso permite aumentar o volume de seus deliveries (aumento do IP). Por exemplo, você pode querer aumentar seus deliveries em um domínio dividindo a execução: envie 1000 mensagens no dia 1, 2000 no dia 2, etc.</p>
<p>Para obter mais informações, consulte <a href="../building-journeys/condition-activity.md#profile_cap">documentação detalhada</a> e relacionadas <a href="../building-journeys/ramp-up-deliveries-uc.md">caso de uso de exemplo</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Jornadas - Melhorias na leitura do segmento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O <strong>Leitura incremental</strong> foi adicionada a opção recorrente <strong>Ler segmento</strong> atividades. Essa opção permite direcionar somente os indivíduos que entraram no segmento desde a última execução da jornada. A primeira execução sempre direciona todos os membros do segmento.</p>
<p>Para obter mais informações, consulte <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Os eventos de etapa do Journey Otimizer agora podem ser vinculados a outros conjuntos de dados em [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). O **profileID** , no schema incorporado Journey Step Event, agora é definido como um campo de identidade. [Saiba mais](../reports/sharing-overview.md#integration-cja)

**Gestão de decisões**

* Ao atualizar uma oferta, oferta de fallback, coleção de ofertas ou decisão de oferta que é mencionada direta ou indiretamente em uma mensagem publicada, as atualizações agora são refletidas automaticamente na mensagem correspondente, sem a necessidade de republicá-la. [Saiba mais](../offers/offers-e2e.md#insert-decision-in-email)

* Ao simular quais ofertas serão entregues para um determinado perfil de teste, agora é possível modificar as configurações padrão da simulação e exibir o código correspondente às suas simulações que podem ser usadas para fins de solução de problemas. [Saiba mais](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administração**

* Agora, os administradores podem editar registros PTR com um subdomínio CNAME configurado. [Saiba mais](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalização**

* **Adicionar a favoritos** - Para ajudar a melhorar a eficiência ao trabalhar com personalização, introduzimos o conceito de salvar favoritos. Adicionar atributos diferentes ao menu de favoritos fornece acesso rápido aos itens usados com mais frequência. [Saiba mais](../personalization/personalize.md#fav)
