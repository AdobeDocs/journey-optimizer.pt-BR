---
title: Notas de versão de 2022
description: Notas de versão do Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: 5aae2f685969460329f241720b0faf9c681fa668
workflow-type: tm+mt
source-wordcount: '2337'
ht-degree: 95%

---

# Notas de versão de 2022 {#release-notes-2022}

Esta página lista todos os recursos e as melhorias do [!DNL Journey Optimizer] lançado em 2022.


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
<p>Para obter mais informações, consulte a <a href="../messages/get-started-content.md">documentação detalhada</a>.</p>
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
<p>Agora você pode usar sistemas de modelo de otimização personalizados na gestão de decisões. Esse novo tipo de modelo permite otimizar e personalizar ofertas com base em segmentos e oferecer desempenho.</p>
<p>O uso de modelos de AI de otimização personalizada está atualmente restrito a usuários selecionados e será implantado em todos os ambientes em uma versão futura.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/ranking/personalized-optimization-model.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* **Encerramento de uma jornada** - Na tela da jornada, a variável **End** foi removida da paleta. Tags finais agora são adicionadas por padrão no final de cada caminho e não podem ser removidas. Essa melhoria permite melhores relatórios sobre onde um cliente saiu da jornada, sem nenhuma ação necessária do profissional de jornada. Consulte a [documentação](../building-journeys/journey-end.md) e [vídeo de recurso](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* O **Fuso horário do perfil** agora está desmarcada por padrão nas propriedades do jornada. [Saiba mais](../building-journeys/timezone-management.md#timezone-from-profiles)

**Mensagens**

* As predefinições de mensagem agora são **superfícies de canais**. [Saiba mais](../configuration/channel-surfaces.md)

**Administração**

* **Edição de registro PTR** — Agora, ao atualizar um registro PTR, o tempo de processamento será de até 3 horas. [Saiba mais](../configuration/ptr-records.md#processing)

* **Interface de lista de permissões** — Agora é possível usar a interface do Journey Optimizer para adicionar novos domínios ou endereços de email à lista de permissões. [Saiba mais](../configuration/allow-list.md)

* **Atualização lógica da lista de permissões** — Agora a lógica da lista de permissões se aplica assim que o recurso é ativado, mesmo que a lista esteja vazia. [Saiba mais](../configuration/allow-list.md#logic)

* **Parâmetros de rastreamento de URL** - Agora você pode usar o Editor de expressão para configurar parâmetros de rastreamento de URL em suas superfícies de email (ou seja, predefinições). [Saiba mais](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Tamanho do público-alvo** — Um novo componente de estimativa de tamanho de público-alvo agora é exibido na interface ao criar uma regra de decisão, ao selecionar um segmento ou uma regra para definir uma qualificação de oferta ou ao adicionar um segmento ou uma regra a um escopo de decisão.


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
<p>Saiba como criar e enviar um SMS nesta <a href="../messages/create-sms.md">documentação detalhada</a>.</p>
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
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Para obter mais informações, consulte a <a href="../design/stock.md">documentação detalhada</a>.</p>
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
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Para obter mais informações, consulte a <a href="../configuration/bcc-email.md">documentação detalhada</a>.</p>
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

* **Salvar como modelo** - agora, você pode salvar um conteúdo de email como modelo e reutilizá-lo ao criar outras mensagens. [Saiba mais](../design/email-templates.md)


**Administração**

* **Visualizar parâmetros de URL de rastreamento** - ao configurar uma predefinição de mensagem, se você definir parâmetros de rastreamento de URL, uma visualização dinâmica do URL de rastreamento resultante será exibida. [Saiba mais](../configuration/email-settings.md#url-tracking)

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
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Para obter mais informações, consulte a <a href="../configuration/frequency-rules.md">documentação detalhada</a>.</p>
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
<!--img src="assets/do-not-localize/optimization.gif"/-->
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
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Para obter mais informações, consulte a <a href="../privacy/audit-logs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Personalização**

* **Nova função auxiliar para ocultação de caracteres** - A função auxiliar do `mask` permite substituir uma parte de uma string por caracteres “X”. [Saiba mais](../personalization/functions/string.md#mask)

**Páginas de aterrissagem**

* **Páginas de aterrissagem sem um formulário** - Agora é possível criar e publicar uma página de aterrissagem que não contenha um formulário e não exija nenhuma ação dos visitantes.
* **Modelos de página de aterrissagem** - Agora é possível salvar uma página de aterrissagem como modelo e reutilizá-la na criação de outras páginas de aterrissagem. [Saiba mais](../landing-pages/lp-templates.md)
* **Voltar à página principal** - Agora é possível adicionar um link para a página principal de qualquer subpágina da mesma página de aterrissagem.
* **Suporte a JavaScript personalizado** - Agora é possível adicionar JavaScript personalizado ao conteúdo da página de aterrissagem para executar estilos avançados ou adicionar comportamentos personalizados às páginas de aterrissagem.	[Saiba mais](../landing-pages/lp-custom-js.md)

**Jornadas**

* **Segmento de leitura** - Jornadas de segmento de leitura única agora são atualizadas para o status “Concluído” 30 dias após a execução da jornada. Para segmentos de leitura agendados, isso acontece 30 dias após a execução da última ocorrência. [Saiba mais](../building-journeys/read-segment.md)
* **Editor de expressão** - A função [limite](../building-journeys/functions/functionlimit.md) foi adicionada para limitar o número de itens de uma lista. A função [classificar](../building-journeys/functions/functionsort.md) agora permite classificar um objeto de lista. O suporte a listObject também foi adicionado às funções [disctinct](../building-journeys/functions/functiondistinct.md) e [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md).

**Administração**

* **Atualização do painel de uso da licença** - o painel de uso da licença, disponível na interface do [!DNL Adobe Journey Optimizer], agora reflete o valor preciso para a riqueza do perfil da média **Licenciada**. Você verá uma queda nessa representação de métrica, o que significa que o limite de licença agora é relatado corretamente. [Saiba mais](../segment/license-usage.md)


## Versão de abril de 2022 {#april-2022-release}

### Melhorias

**Páginas de aterrissagem**

* **Nova opção de caixas de seleção para aceitar/recusar** - Agora é possível inserir uma única caixa de seleção para aceitar/recusar nas páginas de aterrissagem de assinatura. Os usuários precisam marcar a caixa para consentir (aceitar) e desmarcá-la para remover seu consentimento (recusar). [Saiba mais](../landing-pages/design-lp.md#define-lp-specific-content)

* **Preenchimento prévio de campos de páginas de aterrissagem** - Agora é possível conceder aos usuários a capacidade de preencher previamente os campos da página de aterrissagem com informações de perfil. [Saiba mais](../landing-pages/create-lp.md#configure-primary-page)

**Gerenciamento de decisão**

* **API de decisão no Edge** - A API de decisão do Edge pode fornecer e renderizar ofertas personalizadas que são gerenciadas no Offer Decisioning. É possível criar suas ofertas e outros objetos relacionados usando a interface ou as APIs do Offer Decisioning. [Saiba mais](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

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
* Os novos eventos de etapa relacionados aos trabalhos de exportação agora são enviados pelo Journey Optimizer para a Adobe Experience Platform. Exemplos de consultas foram adicionados à documentação. [Saiba mais](../reports/query-examples.md)

**Gerenciamento de decisão**

* Agora é possível especificar se o limite de oferta é aplicado a todos os usuários ou a um perfil específico, bem como a todos os posicionamentos ou por posicionamento. [Saiba mais](../offers/offer-library/add-constraints.md#capping)
* A API de decisão em lote permite que as organizações usem a funcionalidade do Offer Decisioning para todos os perfis em um determinado segmento em uma única chamada. O conteúdo da oferta de cada perfil no segmento é colocado em um conjunto de dados da AEP, onde ele estará disponível para fluxos de trabalho em lote personalizados. [Saiba mais](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administração**

* Agora é possível ativar/desativar o link de cancelamento de inscrição no/do cabeçalho do email no nível da predefinição da mensagem e definir um URL de cancelamento de inscrição personalizado no nível da mensagem. [Saiba mais](../configuration/channel-surfaces.md#list-unsubscribe)
* A lista de permissões agora poderá ser ativada e desativada por meio da interface do [!DNL Journey Optimizer] em sandboxes de produção e não produção. [Saiba mais](../configuration/allow-list.md#enable-allow-list)

**Personalização**

* Agora, você pode salvar mais de 40 expressões de personalização na biblioteca. [Saiba mais](../personalization/personalization-library.md)

## Versão de fevereiro de 2022 {#feb-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Páginas de aterrissagem de subscrição</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar e projetar páginas de aterrissagem no Journey Optimizer e direcionar seus usuários para formulários online, onde eles podem aceitar ou recusar receber suas comunicações ou assinar um serviço específico, como um boletim informativo.</p>
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
<p>Para obter mais informações, consulte a <a href="../personalization/personalization-library.md">documentação detalhada</a>.</p>
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
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
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
<p>Para obter mais informações, consulte a <a href="../configuration/channel-surfaces.md#configure-email-settings">documentação detalhada</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Para otimizar o desempenho, todas as jornadas no modo de testes que não forem acionadas por uma semana agora serão alternadas de volta para o status Rascunho . [Leia mais](../building-journeys/testing-the-journey.md#important_notes)
* A integração entre o Journey Optimizer e o Adobe Campaign Classic foi otimizada para melhorar o desempenho. A configuração padrão de limitação foi alterada para 4.000 chamadas / 5 minutos.	[Leia mais](../action/acc-action.md#important-notes)

**Relatórios**

* Os deliveries agora podem ser filtrados dependendo de seu status:
   * Na lista Message Execution , agora é possível excluir provas da lista de deliveries.
   * Nos seus relatórios Live/Global, você pode optar por excluir eventos de teste.

* Agora você pode acessar os relatórios em Enviar dados de Otimização de Tempo: o número de pessoas que receberam mensagens imediatamente e o número de pessoas que receberam mensagens com otimização de 1 hora, otimização de 2 horas etc.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

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
<p>Para obter mais informações, consulte a <a href="../building-journeys/condition-activity.md#profile_cap">documentação detalhada</a> e o <a href="../building-journeys/ramp-up-deliveries-uc.md">caso de uso de exemplo</a> relacionado.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Jornadas - melhorias no segmento de leitura</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A opção <strong>Leitura incremental</strong> foi adicionada às atividades recorrentes de <strong>Ler segmento</strong>. Essa opção permite direcionar somente aos indivíduos que entraram no segmento desde a última execução da jornada. A primeira execução sempre direciona a todos os membros do segmento.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Os eventos de etapa do Journey Optimizer agora podem ser vinculados a outros conjuntos de dados no [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR). O campo **profileID**, no esquema incorporado Journey Step Event, agora está definido como um campo de identidade. [Saiba mais](../reports/sharing-overview.md#integration-cja)

**offer decisioning**

* Ao atualizar uma oferta, oferta substituta, coleção de ofertas ou decisão de oferta que é mencionada direta ou indiretamente em uma mensagem publicada, as atualizações agora são refletidas automaticamente na mensagem correspondente, sem a necessidade de publicá-la novamente. [Saiba mais](../offers/offers-e2e.md#insert-decision-in-email)

* Ao simular quais ofertas serão entregues para um determinado perfil de teste, agora é possível modificar as configurações padrão da simulação e exibir o código correspondente às simulações que podem ser usadas para fins de solução de problemas. [Saiba mais](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administração**

* Agora, os administradores podem editar registros PTR com um subdomínio CNAME configurado. [Saiba mais](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalização**

* **Adicionar aos favoritos** - para ajudar a melhorar a eficiência ao trabalhar com personalização, introduzimos o conceito de salvar favoritos. Adicionar atributos diferentes ao menu de favoritos fornece acesso rápido aos itens usados com mais frequência. [Saiba mais](../personalization/personalize.md#fav)
