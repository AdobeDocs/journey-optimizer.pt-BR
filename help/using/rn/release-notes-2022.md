---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão de 2022
description: Notas de versão do Journey Optimizer 2022
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: b2446c6a243d6d95b6f695b9c7007e62c51d8fa3
workflow-type: ht
source-wordcount: '3598'
ht-degree: 100%

---

# Notas de versão de 2022 {#release-notes-2022}

Esta página lista todos os recursos e as melhorias do [!DNL Journey Optimizer] lançado em 2022.



## Versão de outubro de 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Melhorias {#oct-2022-improvements}

**Jornadas**

* A opção de **Forçar a reentrada na recorrência** foi adicionada em parâmetros de programação de público-alvo de leitura recorrentes. Essa opção permite fazer com que todos os perfis ainda presentes na jornada saiam automaticamente na próxima execução. Quando a opção estiver desativada, os perfis devem concluir a jornada antes de entrar novamente em outra ocorrência. [Saiba mais](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**Administração**

* Uma mensagem foi adicionada à interface para avisar que as configurações de subdomínio, subdomínio de página de destino, registro PTR e pool de IP são comuns a todas as sandboxes e, portanto, qualquer modificação em uma dessas configurações também afetará as sandboxes de produção.
* As etapas para fazer upload da lista de supressão como um arquivo CSV da interface foram modificadas. [Saiba mais](../configuration/manage-suppression-list.md#download-suppression-list)

**Campanhas**

* Agora é possível arquivar campanhas concluídas e interrompidas. [Saiba mais](../campaigns/modify-stop-campaign.md#archive)


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
<p>Regras condicionais são criadas com um construtor visual de regras no Editor de expressão, onde você pode armazená-las para reutilização em suas jornadas e campanhas.</p>
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
<p>Como usuário do Journey Optimizer, agora você pode acessar alertas do sistema por meio da interface para ser notificado quando a jornada não funcionar conforme o esperado. Você pode visualizar os alertas disponíveis e assiná-los. O primeiro alerta disponível nesta versão avisa se uma atividade do público-alvo de leitura não houver processado nenhum perfil durante o intervalo de tempo definido. Mais informações serão disponibilizadas agora que esse fluxo de trabalho está desbloqueado.</p>
<!--p>For more information, refer to the <a href="../reports/alerts.md">detailed documentation</a>.</p-->
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
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Melhorias{#sept-2022-improvements}

**Jornadas**

* O **Conjunto de dados da entidade** agora está disponível como um conjunto de dados pronto para uso no Adobe Journey Optimizer. Esse conjunto de dados de pesquisa inclui metadados para enriquecer as informações dos conjuntos de dados de rastreamento e feedback. Isso ajudará você a melhorar seus relatórios e consultas com dados mais compreensíveis. [Saiba mais](../data/datasets-query-examples.md#entity-dataset)
* Uma nova medida de proteção foi adicionada às jornadas unitárias (que começam com um evento ou uma qualificação de público-alvo) para impedir que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada no perfil agora será temporariamente bloqueada por 5 minutos. [Saiba mais](../start/guardrails.md#events-g)

**Administração**

* Ao ativar ou desativar a lista de permissões, um novo aviso agora é exibido para detalhar os impactos de cada ação. [Saiba mais](../configuration/allow-list.md#enable-allow-list)
* A interface que permite criar configurações de canal e pools de IP, gerenciar a lista de supressão e a lista de permissões e configurar o canal de SMS foi atualizada.
* Agora, ao criar a primeira configuração de canal para um determinado subdomínio, o tempo de processamento será de 10 minutos a 10 dias e até três horas para superfícies subsequentes que usam esse subdomínio. [Saiba mais](../configuration/channel-surfaces.md#create-channel-surface)
* A interface de criação de predefinições de página de destino e subdomínios de página de destino foi atualizada. [Saiba mais](../landing-pages/lp-subdomains.md)

**Controles de auditoria**

* Com o Journey Optimizer, você pode identificar as ações executadas pelos usuários no sistema em vários serviços e recursos, como campanhas, jornadas, mensagens, páginas de destino etc. Os recursos de log de auditoria agora incluem alterações em várias outras ações e são registrados automaticamente conforme a atividade ocorre. Saiba mais [nesta página](../privacy/audit-logs.md).

**Suporte para arquivamento**

* O novo **Conjunto de dados da entidade** inclui um campo modelo que permite exportar o formato e a estrutura de anúncio das mensagens enviadas em todos os canais para fins de arquivamento. [Saiba mais](../configuration/archiving-support.md)

**Páginas de destino**

* Agora é possível usar dados contextuais provenientes de outra página dentro da mesma página de destino. Por exemplo, se você vincular uma caixa de seleção a uma lista de assinaturas na página de destino principal, poderá usar essa lista de assinaturas na subpágina de agradecimento. [Saiba mais](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Outras alterações{#sept-2022-other}

* O modo de disparo de jornada foi substituído pelo modo de entrega rápida de campanha. [Saiba mais](../push/create-push.md#rapid-delivery)
* Para melhorar o desempenho, os grupos de campos de evento de experiência não podem mais ser usados em jornadas que comecem com atividades de público-alvo de leitura, qualificação de público-alvo ou evento comercial. Essa alteração se aplica somente a novas jornadas. As existentes manterão o comportamento atual. [Saiba mais](../start/guardrails.md#expression-editor)
* A limitação de 1 hora para jornadas de público-alvo de leitura programadas foi removida. Essas jornadas agora podem ser executadas sem atraso.




## Versão de agosto de 2022 {#aug-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Criar e gerenciar campanhas no Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use as campanhas do Journey Optimizer para fornecer conteúdo uma única vez a um público-alvo específico usando vários canais. Ao usar jornadas, as ações são projetadas para serem executadas em sequência. Com campanhas, as ações são executadas simultaneamente, imediatamente ou com base em um cronograma especificado. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Saiba como criar uma campanha na <a href="../campaigns/get-started-with-campaigns.md">documentação detalhada</a> e no <a href="https://video.tv.adobe.com/v/3414156?captions=por_br">vídeo do recurso</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Enviar SMS para os usuários (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar, personalizar e enviar SMS no Journey Optimizer por meio de uma integração com o <b>Sinch</b> ou <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Saiba como criar e enviar um SMS nesta <a href="../sms/create-sms.md">documentação detalhada</a>.</p>
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
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Melhorias

**Relatórios**

* A tabela e o gráfico de políticas de consentimento agora estão disponíveis nos relatórios globais da jornada. Esses widgets permitem rastrear os perfis excluídos das políticas em suas ações personalizadas. [Saiba mais](../reports/journey-global-report-cja.md#journey-global)

  Para ter acesso aos widgets mais recentes, observe que será necessário redefinir os diferentes painéis de relatórios. Para obter mais informações sobre a personalização de painéis, consulte a [documentação detalhada](../reports/report-gs-cja.md).

**Administração**

* Agora é possível atualizar o número de telefone principal a ser usado para o canal SMS. [Saiba mais](../configuration/primary-email-addresses.md)


## Versão de julho de 2022 {#july-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Novo fluxo de mensagens incorporadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer oferece um novo fluxo para a criação de mensagens em jornadas. As mensagens incorporadas economizarão tempo significativo dos usuários e simplificarão o processo do fluxo de trabalho para criar e entregar um email, uma notificação por push ou um SMS no Journey Optimizer. Ao remover a criação das mensagens como uma etapa separada e, em vez disso, incorporar sua edição como parte de uma ação na tela de jornada, os usuários poderão clicar em menos botões e navegar em menos telas para criar e editar seus conteúdos.</p>
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
<p>Agora é possível identificar campos de esquema com rótulos que definem escopos organizacionais ou de uso de dados. Os administradores podem usar a interface de permissões para definir políticas de acesso que cubram campos de esquema XDM e gerenciar melhor o acesso fornecido aos usuários ou grupos de usuários (usuários internos, externos ou de terceiros), além de gerenciar o acesso a tipos específicos de dados (ou seja, dados pessoais confidenciais/SPD).</p>
<p>O uso do controle de acesso baseado em atributos está atualmente restrito aos usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<p>Para obter mais informações, consulte a <a href="../administration/attribute-based-access.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Processos de decisão em lote</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode executar processos de decisão em lote a partir da interface, de modo que não seja necessário que um desenvolvedor execute processos de API em lote e possa reduzir o tempo necessário para o marketing. Essa nova interface permite criar processos e gerenciar processos atuais/anteriores.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/batch-delivery.md">documentação detalhada.</p>
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
<p>Agora você pode usar sistemas de modelo de otimização personalizados na gestão de decisões. Esse novo tipo de modelo permite otimizar e personalizar ofertas com base nos públicos-alvo e no desempenho da oferta.</p>
<p>O uso de modelos de AI de otimização personalizada está atualmente restrito a usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/ranking/personalized-optimization-model.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* **Encerramento de uma jornada** - Na tela da jornada, a atividade **Fim** foi removida da paleta. As tags finais agora são adicionadas por padrão no final de cada caminho e não podem ser removidas. Essa melhoria permite obter relatórios melhores sobre onde um cliente saiu da jornada, sem nenhuma ação necessária por parte do profissional de jornada. Consulte a [documentação](../building-journeys/end-journey.md) e o [vídeo em destaque](https://video.tv.adobe.com/v/345376){target="_blank"}.


* A opção de **Fuso horário do perfil** agora está desmarcada por padrão nas propriedades da jornada. [Saiba mais](../building-journeys/timezone-management.md#timezone-from-profiles)

**Mensagens**

* As predefinições de mensagem agora são as **configurações de canal**. [Saiba mais](../configuration/channel-surfaces.md)

**Administração**

* **Edição de registro PTR** — Agora, ao atualizar um registro PTR, o tempo de processamento será de até 3 horas. [Saiba mais](../configuration/ptr-records.md#processing)

* **Interface de lista de permissões** — Agora é possível usar a interface do Journey Optimizer para adicionar novos domínios ou endereços de email à lista de permissões. [Saiba mais](../configuration/allow-list.md)

* **Atualização lógica da lista de permissões** — Agora a lógica da lista de permissões se aplica assim que o recurso é ativado, mesmo que a lista esteja vazia. [Saiba mais](../configuration/allow-list.md#logic)

* **Parâmetros de rastreamento de URL** — agora você pode usar o Editor de expressão para configurar parâmetros de rastreamento de URL em suas superfícies de email (ou seja, predefinições). [Saiba mais](../email/email-settings.md#url-tracking)

**Gestão de decisões**

* **Tamanho do público-alvo** - Um novo componente de estimativa de tamanho de público-alvo agora é exibido na interface ao criar uma regra de decisão, ao selecionar um público-alvo ou uma regra para definir uma elegibilidade de oferta ou ao adicionar um público-alvo ou uma regra a um escopo de decisão.


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
<p>Agora você pode criar, personalizar e enviar SMS no Journey Optimizer por meio de uma integração com o <b>Sinch</b> ou <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>No momento, o canal SMS está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o seu representante da Adobe.</p>
<p>Saiba como criar e enviar um SMS nesta <a href="../sms/create-sms.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Encontre imagens impactantes mais rapidamente com a integração do Adobe Stock</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O plug-in de integração do Designer de email do Adobe Stock e Adobe Journey Optimizer fornece aos clientes uma maneira fácil de navegar, licenciar e salvar imagens para uso na criação de mensagens. </br> A nova opção <b>Localizar fotos semelhantes do Stock</b> também permite localizar fotos do Stock que correspondam ao conteúdo, cor e composição de suas imagens. </p>
<p>Para obter mais informações, consulte a <a href="../integrations/stock.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar Email Cco em todos os seus emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o recurso Email Cco (com cópia oculta) para armazenar emails enviados pelo Adobe Journey Optimizer. Ative essa opção nas predefinições de email para que cada email enviado seja copiado de forma oculta para o endereço do Cco.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/archiving-support.md#bcc-email">documentação detalhada</a>.</p>
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
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on audiences and offer performance.</p>
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
<p>Agora é possível transferir as experiências de uma sandbox do Journey Optimizer para outra, por exemplo, criando uma sandbox de produção a partir de uma sandbox de não produção. Esse novo recurso copia uma jornada inteira de um ambiente para outro, incluindo todos os objetos dos quais ela depende para ser executada corretamente. Além das Jornadas, também é possível copiar outros componentes, como Ofertas, Mensagens, Esquemas, Conjuntos de dados, Fontes de dados, Eventos e Ações.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/copy-to-sandbox.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>




### Melhorias

**Gestão de decisões**

* **Compatibilidade com arquivos HTML e JSON** - agora, é possível arrastar e soltar arquivos HTML e JSON externos da biblioteca de ativos da Adobe Experience Cloud para o conteúdo de representação da oferta. [Saiba mais](../offers/offer-library/add-representations.md#html-json)


**Email**

* **Salvar como modelo** - agora, você pode salvar um conteúdo de email como modelo e reutilizá-lo ao criar outras mensagens. [Saiba mais](../content-management/content-templates.md#save-as-template)


**Administração**

* **Visualizar parâmetros de URL de rastreamento** - ao configurar uma predefinição de mensagem, se você definir parâmetros de rastreamento de URL, uma visualização dinâmica do URL de rastreamento resultante será exibida. [Saiba mais](../email/email-settings.md#url-tracking)

* **Edição de predefinição de mensagem** - Agora, ao atualizar uma predefinição de mensagem, o tempo de processamento pode levar até 3 horas. [Saiba mais](../configuration/channel-surfaces.md#edit-channel-surface)

* **Edição de pool de IPs** - Agora, ao atualizar um pool de IPs, o tempo de processamento pode levar até 3 horas. [Saiba mais](../configuration/ip-pools.md#edit-ip-pool)




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
<p>Para obter mais informações, consulte a <a href="../configuration/rule-sets.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestão de decisões - Modelo de otimização automática de classificação de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar sistemas de modelo treinados na Gestão de decisões. Esse novo recurso classifica as ofertas para exibição em um determinado perfil.</p>
<p>Para obter mais informações, consulte a <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentação detalhada</a>.</p>
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
<th><strong>Logs de auditoria do Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível monitorar ações executadas por usuários nos recursos do Adobe Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../privacy/audit-logs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Personalização**

* **Nova função auxiliar para ocultação de caracteres** - A função auxiliar do `mask` permite substituir uma parte de uma string por caracteres “X”. [Saiba mais](../personalization/functions/string.md#mask)

**Páginas de destino**

* **Páginas de destino sem um formulário** - Agora é possível criar e publicar uma página de destino que não contenha um formulário e não exija nenhuma ação dos visitantes.
* **Modelos de página de destino** - Agora é possível salvar uma página de destino como modelo e reutilizá-la na criação de outras páginas de destino. [Saiba mais](../landing-pages/lp-templates.md)
* **Voltar à página principal** - Agora é possível adicionar um link para a página principal de qualquer subpágina da mesma página de destino.
* **Suporte a JavaScript personalizado** - Agora é possível adicionar JavaScript personalizado ao conteúdo da página de destino para executar estilos avançados ou adicionar comportamentos personalizados às páginas de destino.    [Saiba mais](../landing-pages/lp-custom-js.md)

**Jornadas**

* **Público-alvo de leitura** - Jornadas de público-alvo de leitura únicas agora são atualizadas para o status “Concluído” 30 dias após a execução da jornada. Para públicos-alvo de leitura agendados, isso acontece 30 dias após a execução da última ocorrência. [Saiba mais](../building-journeys/read-audience.md)
* **Editor de expressão** - A função [limite](../building-journeys/functions/functionlimit.md) foi adicionada para limitar o número de itens de uma lista. A função [classificar](../building-journeys/functions/functionsort.md) agora permite classificar um objeto de lista. O suporte a listObject também foi adicionado às funções [disctinct](../building-journeys/functions/functiondistinct.md) e [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md).

**Administração**

* **Atualização do painel de uso da licença** - o painel de uso da licença, disponível na interface do [!DNL Adobe Journey Optimizer], agora reflete o valor preciso para a riqueza do perfil da média **Licenciada**. Você verá uma queda nessa representação de métrica, o que significa que o limite de licença agora é relatado corretamente. [Saiba mais](../audience/license-usage.md)


## Versão de abril de 2022 {#april-2022-release}

### Melhorias

**Páginas de destino**

* **Nova opção de caixas de seleção para aceitar/recusar** - Agora é possível inserir uma única caixa de seleção para aceitar/recusar nas páginas de destino de assinatura. Os usuários precisam marcar a caixa para consentir (aceitar) e desmarcá-la para remover seu consentimento (recusar). [Saiba mais](../landing-pages/design-lp.md#define-lp-specific-content)

* **Preenchimento prévio de campos de páginas de destino** - Agora é possível conceder aos usuários a capacidade de preencher previamente os campos da página de destino com informações de perfil. [Saiba mais](../landing-pages/create-lp.md#configure-primary-page)

**Gestão de decisões**

* **API de decisão do Edge** — A API de decisão do Edge pode fornecer e renderizar ofertas personalizadas que são gerenciadas na gestão de decisões. É possível criar suas ofertas e outros objetos relacionados usando a interface ou as APIs da gestão de decisões. [Saiba mais](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administração**

* **Duração do envio de PTR** - A duração da edição de PTR agora é de algumas horas. [Saiba mais](../configuration/ptr-records.md#processing)

**Design de email**

* **20 novos modelos de email** agora estão disponíveis para criar seu conteúdo de email no Journey Optimizer.

**Interface do usuário**

* **Ajuda contextual na interface do Journey Optimizer** - Foram adicionados links de ajuda contextual a várias páginas do Journey Optimizer. Quando disponível, clique no ícone “i” para exibir uma descrição rápida da funcionalidade atual e acessar artigos relacionados.

**Integração com o Adobe Campaign Standard**

Como cliente do Adobe Campaign Standard, agora você pode enviar emails, notificações por push e SMS usando o Journey Optimizer. Use as novas ações integradas para utilizar os recursos de mensagens transacionais do Campaign Standard no Journey Optimizer.  [Saiba mais](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Versão de março de 2022 {#march-2022-release}

### Melhorias

**Jornadas**

* Para evitar campos desnecessários no esquema de perfil unificado, o esquema de eventos de etapas da jornada não é mais habilitado para perfis por padrão. Se necessário, você pode ativá-lo. [Saiba mais](../reports/sharing-overview.md)
* Os novos eventos de etapa relacionados aos processos de exportação agora são enviados pelo Journey Optimizer para a Adobe Experience Platform. Exemplos de consultas foram adicionados à documentação. [Saiba mais](../reports/query-examples.md)

**Gestão de decisões**

* Agora é possível especificar se o limite de oferta é aplicado a todos os usuários ou a um perfil específico, bem como a todos os posicionamentos ou por posicionamento. [Saiba mais](../offers/offer-library/add-constraints.md#capping)
* A API de decisão em lote permite que as organizações usem a funcionalidade de gestão de decisões para todos os perfis em um determinado público-alvo, através de uma única chamada. O conteúdo da oferta de cada perfil no público-alvo é colocado em um conjunto de dados da AEP, onde estará disponível para fluxos de trabalho em lote personalizados. [Saiba mais](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administração**

* Agora é possível habilitar ou desabilitar o link de cancelamento de inscrição no/do cabeçalho do email no nível da predefinição da mensagem e definir um URL de cancelamento de inscrição personalizado no nível da mensagem. [Saiba mais](../configuration/channel-surfaces.md#list-unsubscribe)
* A lista de permissões agora poderá ser habilitada ou desabilitada por meio da interface do [!DNL Journey Optimizer] em sandboxes de produção e não produção. [Saiba mais](../configuration/allow-list.md#enable-allow-list)

**Personalização**

* Agora, você pode salvar mais de 40 expressões de personalização na biblioteca. [Saiba mais](../personalization/use-expression-fragments.md)

## Versão de fevereiro de 2022 {#feb-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Páginas de destino de subscrição</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar e projetar páginas de destino no Journey Optimizer e direcionar seus usuários para formulários online, onde eles podem aceitar ou recusar receber suas comunicações ou assinar um serviço específico, como um boletim informativo.</p>
<p>Para obter mais informações, consulte a <a href="../landing-pages/create-lp.md">documentação detalhada</a> e o <a href="../landing-pages/lp-use-cases.md">caso de uso de exemplo</a> relacionado.</p>
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
<p>Agora, o Journey Optimizer fornece uma biblioteca onde você pode acessar expressões de personalização predefinidas. Essas expressões são configuradas por usuários administradores.</p>
<p>Para obter mais informações, consulte a <a href="../personalization/use-expression-fragments.md">documentação detalhada</a>.</p>
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
<th><strong>Transmita informações para rastrear suas mensagens com parâmetros de rastreamento UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No conteúdo da mensagem do Journey Optimizer, agora é possível adicionar parâmetros UTM aos links: eles podem fornecer dados adicionais sobre esse link e ajudar a identificar onde e por que uma pessoa clicou em seu link.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/channel-surfaces.md#configure-email-settings">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Para otimizar o desempenho, todas as jornadas no modo de testes que não forem acionadas por uma semana agora serão alternadas de volta para o status Rascunho . [Leia mais](../building-journeys/testing-the-journey.md#important_notes)
* A integração entre o Journey Optimizer e o Adobe Campaign v7/v8 foi otimizada para melhorar o desempenho. A configuração padrão de limite foi alterada para 4.000 chamadas / 5 minutos. [Leia mais](../action/acc-action.md#important-notes)

**Relatórios**

* As entregas agora podem ser filtradas dependendo de seu status:
   * Na lista Execução de mensagem , agora é possível excluir provas da lista de entregas.
   * Nos seus relatórios Live/Global, você pode optar por excluir eventos de teste.

* Agora você pode acessar os relatórios em Enviar dados de Otimização de Tempo: o número de pessoas que receberam mensagens imediatamente e o número de pessoas que receberam mensagens com otimização de 1 hora, otimização de 2 horas etc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestão de decisões**

* As classificações e a classificação de AI agora estão agrupadas em uma única guia.

## Versão de janeiro de 2022 {#january-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Jornadas - otimize seu incremento de IP com condições de limite de perfis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ao configurar uma atividade de <strong>Condição</strong> em uma jornada, agora é possível definir um limite de perfis. Esse novo tipo de condição permite definir um número máximo de perfis para um caminho de jornada. Quando esse limite é atingido, os perfis que entram pegam um caminho alternativo. Isso permite incrementar o volume das suas entregas (incremento de IP). Por exemplo, você pode querer incrementar suas entregas em um domínio dividindo a execução: enviar 1000 mensagens no dia 1, 2000 no dia 2, etc.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/condition-activity.md#profile_cap">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Jornadas - melhorias no público-alvo de leitura</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A opção <strong>Leitura incremental</strong> foi adicionada às atividades recorrentes de <strong>Público-alvo de leitura</strong>. Essa opção permite direcionar somente às pessoas físicas que entraram no público-alvo desde a última execução da jornada. A primeira execução sempre direciona a todos os membros do público-alvo.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Os eventos de etapa do Journey Optimizer agora podem ser vinculados a outros conjuntos de dados no [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR). O campo **profileID**, no esquema integrado Evento de Etapas da Jornada, agora está definido como um campo de identidade. [Saiba mais](../reports/sharing-overview.md#integration-cja)

**Gestão de decisões**

* Ao atualizar uma oferta, oferta substituta, coleção de ofertas ou decisão de oferta que é mencionada direta ou indiretamente em uma mensagem publicada, as atualizações agora são refletidas automaticamente na mensagem correspondente, sem a necessidade de publicá-la novamente. [Saiba mais](../offers/offers-e2e.md#insert-decision-in-email)

* Ao simular quais ofertas serão entregues para um determinado perfil de teste, agora é possível modificar as configurações padrão da simulação e exibir o código correspondente às simulações que podem ser usadas para fins de solução de problemas. [Saiba mais](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administração**

* Agora, os administradores podem editar registros PTR com um subdomínio CNAME configurado. [Saiba mais](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalização**

* **Adicionar aos favoritos** - Para ajudar a melhorar a eficiência ao trabalhar com personalização, introduzimos o conceito de salvar favoritos. Adicionar atributos diferentes ao menu de favoritos fornece acesso rápido aos itens usados com mais frequência. [Saiba mais](../personalization/personalize.md#fav)
