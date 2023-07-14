---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2e3335372dca8c344773eaf365e8f90589ecfd7e
workflow-type: tm+mt
source-wordcount: '2591'
ht-degree: 93%

---

# Notas de versão {#release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

As notas de versão anteriores estão disponíveis [nesta página](release-notes-2022.md). Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.


## Atualizações de julho de 2023


<table>
<thead>
<tr>
<th><strong>Composição de público</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar workflows de composição para combinar públicos-alvo existentes do Adobe Experience Platform em uma tela visual e aproveitar várias atividades (dividir, enriquecer...) para criar novos públicos-alvo. Os públicos-alvo recém-criados são salvos no Adobe Experience Platform junto com os públicos-alvo existentes e podem ser aproveitados nas campanhas do Journey Optimizer para direcionar os clientes.</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>Para obter mais informações, consulte a <a href="../audience/get-started-audience-orchestration.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


## Notas de versão de junho de 2023 {#june-rn-2023}

<table>
<thead>
<tr>
<th><strong>Campanhas acionadas por API para casos de uso de marketing</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível usar APIs para acionar campanhas de marketing no Adobe Journey Optimizer a partir de um sistema externo.</p>
<p>Até essa versão, o recurso de campanhas acionadas por API cobria várias necessidades de mensagens operacionais e transacionais, como redefinições de senha ou token OTP, mas não podia ser usado para criar campanhas de marketing. Os canais disponíveis para campanhas acionadas por API são: email, SMS e mensagens por push.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Para obter mais informações, consulte a <a href="../campaigns/api-triggered-campaigns.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<!--
### Improvements {#june-2023-improvements}


**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.

**Journeys**

You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

<!--
## June 2023 early release notes {#june-rn-2023}

Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Audiences**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    


**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.     

* A new type of system alert has been introduced. You can now get notified when a custom action fails.
-->

## Notas de versão de maio de 2023 {#may-rn-2023}

### Novos recursos{#may-2023-features}



<table>
<thead>
<tr>
<th><strong>Experimentação de conteúdo em campanhas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora oferece suporte a experimentos em campanhas. Experimentos são ensaios aleatórios, o que, no contexto de testes online, significa que você expõe alguns usuários selecionados aleatoriamente a uma determinada variação de uma mensagem e outro conjunto de usuários selecionados aleatoriamente a outra variação ou tratamento. Após a exposição, é possível medir as métricas de resultado em que está interessado, como abertura de emails, assinaturas ou compras.</p>
<img src="assets/do-not-localize/experiment.gif"/>
<p>Para obter mais informações, consulte a <a href="../campaigns/content-experiment.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Objective reporting and performance measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the Objectives tab of your campaign reports.</p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../reports/campaign-global-report.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->


<table>
<thead>
<tr>
<th><strong>Criar e usar fragmentos no conteúdo de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar, usar e gerenciar fragmentos para produzir rapidamente emails e modelos de conteúdo. Um fragmento é um componente reutilizável pré-construído que pode ser referenciado em vários emails em campanhas e jornadas do Journey Optimizer para um processo de design aprimorado e acelerado.</p>
<img src="assets/do-not-localize/fragments.gif"/>
<p>Para obter mais informações, consulte a <a href="../email/fragments.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Usar tags em suas campanhas (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível atribuir tags unificadas da Adobe Experience Platform às campanhas. Isso permite classificá-las facilmente e melhorar a pesquisa na lista de campanhas. Observe que o recurso de Tags unificadas está atualmente na versão beta.</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Para obter mais informações, consulte a <a href="../start/search-filter-categorize.md#tags">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Modelo de classificação de IA de otimização personalizada (Disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os modelos de classificação de IA de otimização personalizada agora estão disponíveis na Gestão de decisões. Esse novo tipo de modelo permite otimizar e personalizar ofertas com base nos públicos e no desempenho da oferta.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Para obter mais informações, consulte a <a href="../offers/ranking/personalized-optimization-model.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>



### Melhorias {#may-2023-improvements}

**Públicos-alvo**

* Em preparação para a disponibilidade geral do recurso Portal de público-alvo, a Adobe Experience Platform está atualizando o uso de “públicos-alvo” e “segmentos” no sistema e na documentação.

   * Público-alvo: um conjunto de pessoas, contas, famílias ou outras entidades que compartilham características e comportamentos comuns.
   * Definição de segmento: na Adobe Experience Platform, as regras usadas para descrever as principais características ou comportamentos de um público-alvo. Esse termo era anteriormente conhecido apenas como “segmento”.

  Como resultado, na na interface do Adobe Journey Optimizer e da Adobe Experience Platform, “Segmentos” será substituído por “Públicos-alvo” para refletir esse novo caminho de criação e gerenciamento de público-alvo.

  As traduções do termo “público-alvo” ao se referir a um grupo de perfis direcionados para receber uma mensagem foram harmonizadas em todos os produtos de Experiência digital para alguns idiomas:

   * Alemão: Zielgruppe
   * Português (Brasil): público-alvo
   * Espanhol: público destinatario

<!--* Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.-->

**Canal SMS**

* O Infobip foi adicionado como provedor de fornecedores ao configurar suas superfícies de canal de SMS. [Leia mais](../sms/sms-configuration.md)
* Twillio - A configuração de credencial da API agora inclui a capacidade de adicionar SID de serviço de mensagens para integração perfeita com sua conta do Twillio. [Leia mais](../sms/sms-configuration.md)

**Canal no aplicativo**

* Adição de novas regras de acionador de mensagem para o serviço do Adobe Places. [Leia mais](../in-app/inapp-configuration.md)
* Adição de novos recursos da Adobe Experience Platform Assurance para capturar eventos de dispositivos e adicionar como regras de acionador.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

**Campanhas**

* Agora é possível duplicar uma campanha a partir da tela de inventário usando o menu de ação de reticências. [Leia mais](../campaigns/modify-stop-campaign.md#duplicate)
* Agora é possível excluir modificações de rascunho em uma campanha ativa.
* As etapas para ativar uma campanha agora foram simplificadas. [Leia mais](../campaigns/modify-stop-campaign.md)

**Gestão de decisões**

* Agora é possível editar o limite de frequência se a oferta tiver o status **[!UICONTROL Rascunho]** e nunca tiver sido publicada antes com o limite de frequência habilitado. [Leia mais](../offers/offer-library/add-constraints.md#frequency-capping)

**Personalização**

* Agora é possível selecionar e inserir referências de ativos diretamente do Editor de personalização ao trabalhar em conteúdo de HTML.

### Correções{#may-2023-fixes}

* Mensagens no aplicativo - correção de um problema no qual o agendamento da campanha entrava em conflito com as configurações de frequência da mensagem.


## Notas da versão de abril de 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Novos recursos{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal web (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer está expandindo seus recursos entre canais adicionando compatibilidade com o canal web. Agora é possível criar, alterar e visualizar experiências da Web como em qualquer outro canal, por meio de uma interface visual inteligente e intuitiva, a fim de personalizar a experiência dos usuários finais. Observe que, atualmente, o Journey Optimizer só permite a criação de experiências da Web em campanhas.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Para obter mais informações, consulte a <a href="../web/get-started-web.md">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Fluxo de trabalho de início rápido de integração para dispositivos móveis (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O novo fluxo de trabalho de início rápido de integração para dispositivos móveis está disponível. Use esse novo recurso do produto para configurar rapidamente o SDK móvel para começar a coletar e validar dados de eventos móveis e enviar notificações por push para dispositivos móveis com o Adobe Journey Optimizer. Esse recurso é acessível por meio da página inicial da Coleção de dados, na forma de um beta público.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Para obter mais informações, consulte a <a href="../push/mobile-onboarding-wf.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novo painel da jornada (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> O painel da jornada agora está dividido em duas guias:</p>
<ul><li>Use a guia <strong>Visão geral</strong> para acessar um novo painel que exibe as métricas principais relacionadas às suas jornadas.</li>
<li>Use a guia <strong>Procurar</strong> para acessar a lista de todas as jornadas.</li></ul>
<p>Esse recurso pode ser acessado em todas as jornadas como um beta público.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-gs.md#journey-access">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#april-2023-improvements}

**Jornadas**

* A tela da jornada agora exibe a ID da atividade nas atividades de mensagem e tags finais. Isso melhora os relatórios e o redirecionamento.
* O layout do painel de configuração, que aparece em ações, fontes de dados, eventos e jornadas, foi aprimorado.
* Novo insight para um número de nós em telas com proteções para ajudar no crescimento: mantenha as jornadas fáceis de ler, controle a qualidade e solucione problemas com um número máximo de 50 nós por jornada. [Leia mais](../start/guardrails.md#journeys-guardrails-journeys)
* Ao adicionar uma ação de [email](../email/create-email.md), [SMS](../sms/create-sms.md) ou [push](../push/create-push.md) em uma jornada, a superfície agora é pré-preenchida, por padrão, com a última superfície usada para esse canal na jornada atual.
* Agora é possível definir parâmetros de consulta estáticos ou dinâmicos em suas ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#url-configuration)

**Relatórios**

* Agora é possível exportar os relatórios do Journey Optimizer como um arquivo PDF. [Saiba mais](../reports/global-report.md#export-reports)

**Designer de conteúdo**

* O Designer de conteúdo do Adobe Journey Optimizer foi atualizado e o acesso aos estilos e componentes de design foi simplificado. Esta nova versão propõe uma melhor experiência do usuário e vem com um desempenho aprimorado, compatibilidade parcial com o modo escuro e suporte aos novos padrões de acessibilidade.



## Notas da versão de março de 2023 {#mar-2023}

### Novos recursos{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal no aplicativo (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode enviar mensagens personalizadas no aplicativo para os usuários do aplicativo em uma campanha. Use o Journey Optimizer para criar notificações e personalizar o layout, a exibição, o texto e os botões das mensagens para criar uma experiência perfeita.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obter mais informações, consulte a <a href="../in-app/get-started-in-app.md">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rastreamento de cliques de SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o rastreamento de cliques de SMS, você pode monitorar o desempenho de seus URLs encurtados, identificar quem os clicou e usar esses dados para redirecionar esses clientes com campanhas subsequentes.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Para obter mais informações, consulte a <a href="../sms/create-sms.md#sms-content">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar tags em suas jornadas (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como um profissional do Journey Optimizer, agora você pode organizar seus objetos de negócios usando tags. As tags são uma maneira rápida e fácil de classificar objetos para melhorar a pesquisa. No momento, esse recurso está na versão beta e só está disponível para jornadas.</p>
<p>Para obter mais informações, consulte a <a href="../start/search-filter-categorize.md#tags">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#mar-2023-improvements}

**Jornadas**

* A nova **API de limitação** permite definir um limite para o número de eventos enviados por segundo, evitando picos de tráfego grandes demais em sistemas externos ou APIs. Quando o limite definido é atingido, todas as chamadas de API subsequentes são enfileiradas e processadas o mais rápido possível, na ordem em que forem recebidas. Observe que esse recurso suporta apenas uma configuração de limitação em todas as suas sandboxes. [Saiba mais](../configuration/external-systems.md)
* A tela da jornada foi aperfeiçoada para oferecer uma experiência do usuário mais simples e polida. No final de cada caminho na tela, os espaços reservados vazios foram removidos. Agora é possível adicionar suas atividades simplesmente arrastando-as para o final de um caminho.
* Na tela da jornada, o rótulo da tag **Fim** não é mais definida automaticamente com o nome da atividade anterior. Os usuários podem adicionar manualmente um rótulo personalizado, se necessário.
* O tempo limite padrão e a duração de erro nas propriedades da jornada foram alterados de 5 para 30 segundos. [Saiba mais](../configuration/external-systems.md#timeout)
* A taxa de limitação padrão em atividades de leitura de público foi alterada de 20.000 para 5.000 mensagens por segundo. [Saiba mais](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Uma medida de proteção foi adicionada ao modo de teste para ouvir apenas os eventos enviados através da interface. Os eventos enviados por uma ferramenta externa não são considerados. [Saiba mais](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Gestão de decisões**

* Para evitar qualquer possível confusão com o lançamento recente do recurso de tags na Adobe Experience Platform, as tags da gestão de decisões agora são chamadas de “Qualificadores de coleção”.

  Observe que, embora o termo “tag” não seja mais usado na interface da gestão de decisões, ele ainda é usado nos serviços de back-end, como APIs e conjuntos de dados.

* Agora é possível redefinir o contador de limite de oferta por dia, por semana ou por mês. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

* Você também pode escolher qual evento da Adobe Experience Platform deve ser observado para o limite de definição de ofertas. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

* Parâmetros complementares foram adicionados à tela de criação de posicionamentos. Eles permitem controlar se uma oferta pode ser duplicada em vários posicionamentos e especificar se o conteúdo e os metadados da oferta devem ser incluídos na resposta da API. [Saiba mais](../offers/offer-library/creating-placements.md)

**Personalização**

* Agora é possível incluir texto de fallback padrão para atributos de perfil baseados em sequência de caracteres no Editor de expressão. Esses valores serão exibidos se os atributos selecionados não retornarem nenhum resultado. [Saiba mais](../personalization/personalization-build-expressions.md#add)

**Relatórios**

* A funcionalidade do widget de relatórios foi aprimorada com a capacidade de personalizar a forma como os usuários visualizam seus dados. Com esse aprimoramento, os usuários agora podem escolher entre várias opções de visualização, incluindo gráficos, tabelas e gráficos de rosca.

  Para ter acesso aos widgets mais recentes, observe que será necessário redefinir os diferentes painéis de relatórios. Para obter mais informações sobre a personalização de painéis, consulte a [documentação detalhada](../reports/global-report.md#modify-dashboard).

## Notas da versão de fevereiro de 2023 {#feb-2023}

### Novos recursos{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal no aplicativo (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode enviar mensagens personalizadas no aplicativo para os usuários do aplicativo em uma campanha. Use o Journey Optimizer para criar notificações e personalizar o layout, a exibição, o texto e os botões das mensagens para criar uma experiência perfeita.</p>
<p><strong>Aviso</strong>: no momento, esse recurso está na versão beta e só está disponível para clientes beta. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Para obter mais informações, consulte a <a href="../in-app/get-started-in-app.md"> documentação detalhada </a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportar conjuntos de dados do Journey Optimizer para destinos de armazenamento na nuvem (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível estabelecer uma conexão ativa com locais de armazenamento na nuvem para exportar o conteúdo de seus conjuntos de dados. Os destinos disponíveis são: Amazon S3 Cloud Storage, Azure Blob, Azure Data Lake Gen 2, Data Landing Zone, Google Cloud Storage e SFTP.</p>
<p><strong>Aviso</strong>: esse recurso está atualmente na versão beta e está disponível para todos os usuários do Adobe Journey Optimizer. Entre em contato com seu representante da Adobe para obter acesso aos destinos, caso ainda não o tenha.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Para obter mais informações, consulte a <a href="../data/export-datasets.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Melhorias {#feb-2023-improvements}

**Jornadas**

* O campo **Período de espera de reentrada** foi adicionado às propriedades da jornada. Esse campo permite definir o tempo de espera antes de permitir que um perfil entre na jornada novamente em jornadas unitárias (começando com um evento ou uma qualificação de público-alvo). Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos. [Saiba mais](../building-journeys/journey-gs.md#entrance)

* Foram realizadas melhorias nas **datas de início e término da jornada**. Se você não tiver especificado uma data de início, ela agora será adicionada automaticamente no momento da publicação. Para **Ler público** jornadas, agora é possível adicionar uma data de término. Isso permite que os perfis saiam automaticamente quando a data for atingida. [Saiba mais](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Administração**

* **Lista de permissões**: agora é possível baixar a lista de permissões como um arquivo .csv. [Saiba mais](../configuration/allow-list.md#download-allowed-list)

* **Superfície de email**: uma verificação adicional foi incluída nas configurações da superfície de email. Se o registro MX do subdomínio usado no endereço **Responder para (email)** ou no **endereço de email Cco** não estiver configurado corretamente, a superfície de email não poderá mais ser criada. Você precisa configurá-lo ou usar outro. [Saiba mais](../email/email-settings.md#reply-to-email)

* **Superfície de email**: na seção **Parâmetros de rastreamento de URL** das configurações da superfície de email, o limite para cada campo de **Valor** foi atualizado de 255 caracteres para 5 KB, a fim de oferecer compatibilidade com o rastreamento do Adobe Analytics. [Saiba mais](../email/email-settings.md#url-tracking)

**Gestão de decisões**

* **Posicionamentos** - Parâmetros complementares foram adicionados à tela de criação de posicionamentos. Eles permitem controlar se uma oferta pode ser duplicada em vários posicionamentos e especificar se o conteúdo e os metadados da oferta devem ser incluídos na resposta da API. [Saiba mais](../offers/offer-library/creating-placements.md)

* **Personalização de URL**: ao adicionar URLs como conteúdo às representações de suas ofertas, agora é possível personalizar esses URLs usando o editor de expressão. [Saiba mais](../offers/offer-library/add-representations.md)

## Notas da versão de janeiro de 2023{#jan-2023-release}

### Novos recursos{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Higiene de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Adobe Experience Platform fornece um conjunto de recursos de higiene de dados que permitem gerenciar seus dados armazenados por meio de exclusões programáticas de conjuntos de dados e registros do consumidor. Esse recurso está disponível agora para o Adobe Journey Optimizer. </p>
<p>Você pode gerenciar seus armazenamentos de dados para garantir que as informações sejam usadas conforme esperado, atualizadas quando dados incorretos precisarem de correção e excluídas quando as políticas organizacionais considerarem necessário.</p>
<p><strong>Atenção</strong> - Atualmente, os recursos de Higiene de dados estão disponíveis apenas para as organizações que compraram as ofertas complementares do <strong>Healthcare Shield</strong> e do <strong>Privacy and Security Shield</strong>.</p><p>Para obter mais informações, consulte a <a href="../privacy/data-hygiene.md">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modelos de conteúdo de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar modelos de conteúdo independentes que possam ser aproveitados em jornadas e campanhas para reutilização rápida.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Saiba como criar, editar e usar modelos de conteúdo <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=pt-BR">neste vídeo</a>. Para obter mais informações, consulte a <a href="../email/content-templates.md">documentação detalhada</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#jan-2023-improvements}

**Jornadas**

* Ao adicionar uma **Qualificação de público** ou **Ler público** em uma jornada, o namespace agora é pré-preenchido, por padrão, com o último namespace usado. Consulte a [Qualificação de público](../building-journeys/audience-qualification-events.md#about-segment-qualification) e [Ler público](../building-journeys/read-audience.md#configuring-segment-trigger-activity) seções.

* Um novo botão está disponível na barra de ferramentas da tela de jornada, que permite baixar uma captura de tela da sua jornada.

**Designer de email**

* Agora você pode exportar o conteúdo de email do menu **Exportar HTML**. Os arquivos exportados são disponibilizados em um arquivo compactado (.zip).

**Administração**

* Uma nova subseção fornece recomendações sobre a criação de um endereço **Responder para (email)** e sobre como garantir uma gestão adequada das respostas. [Saiba mais](../email/email-settings.md#reply-to-email)

* Ao criar ou editar **pools de IPs**, os registros PTR associados agora são exibidos na lista de IP e ao passar o cursor do mouse sobre os endereços IP selecionados. [Saiba mais](../configuration/ip-pools.md#create-ip-pool)

* Depois que um pool de IP é selecionado em uma superfície de canal, as informações do registro PTR agora são visíveis ao passar o cursor do mouse sobre os endereços IP. [Saiba mais](../email/email-settings.md#subdomains-and-ip-pools)

* A interface de edição de [registros PTR](../configuration/ptr-records.md#edit-ptr-record) e [campos de execução](../configuration/primary-email-addresses.md) foi atualizada.

* A interface de criação e edição de subdomínios foi aprimorada. [Saiba mais](../configuration/delegate-subdomain.md)

* A tela de **Uploads recentes** da lista de supressão foi atualizada. [Saiba mais](../configuration/manage-suppression-list.md#recent-uploads)

**Campanhas**

* Uma solicitação cURL de exemplo que permite a execução de campanhas acionadas por API agora é gerada automaticamente e disponibilizada na tela da campanha. [Saiba mais](../campaigns/api-triggered-campaigns.md)


**Personalização**

* Novas funções de ajuda estão disponíveis: formatCurrency, charCodeAt, stringToDate, toString, formatNumber e toHexString. Além disso, a função toDateTimeOnly agora aceita os tipos de campos string, data, longo e int. [Saiba mais](../personalization/functions/functions.md)
