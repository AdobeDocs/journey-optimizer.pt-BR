---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 87%

---

# Notas de versão {#release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

As notas de versão anteriores estão disponíveis [nesta página](release-notes-2022.md). Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.


## Melhorias em março de 2023 {#march-2023}

**Gerenciar tags em suas Jornadas**

Como um profissional da Journey Optimizer, agora você pode organizar seus objetos de negócios usando tags do. Tags são uma maneira rápida e fácil de classificar objetos para melhorar a pesquisa. No momento, esse recurso está na versão beta e só está disponível para Jornada. [Saiba mais](../building-journeys/tags.md)

**Tags de gestão de decisão renomeadas para Qualificadores de coleção**

Para evitar qualquer confusão em potencial com o recurso de lançamento recente de tags na Adobe Experience Platform, as tags do Gerenciamento de decisão foram renomeadas para &quot;Qualificadores de coleção&quot;.

Observe que, embora o termo &quot;tag&quot; não seja mais usado na interface do usuário do Gerenciamento de decisão, ele ainda é usado em serviços de back-end, como APIs e conjuntos de dados.

## Notas de versão de fevereiro de 2023 {#feb-2023}

### Novos recursos{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal no aplicativo (beta)</strong><br/></th>
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
<th><strong>Exportar conjuntos de dados do Journey Optimizer para destinos de armazenamento na nuvem (beta)</strong><br/></th>
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

* O campo **Período de espera de reentrada** foi adicionado às propriedades da jornada. Este campo possibilita definir o tempo de espera antes de permitir que um perfil entre novamente em jornadas unitárias (que começam com um evento ou uma qualificação de segmento). Isso impede que uma mesma jornada seja incorretamente acionada várias vezes no mesmo evento. Por padrão, o campo é definido como 5 minutos. [Saiba mais](../building-journeys/journey-gs.md#entrance)

* Foram realizadas melhorias nas **datas de início e término da jornada**. Se você não tiver especificado uma data de início, ela agora será adicionada automaticamente no momento da publicação. Para jornadas de **Segmento de leitura**, agora é possível adicionar uma data de término. Isso permite que os perfis saiam automaticamente quando a data for atingida. [Saiba mais](../building-journeys/journey-gs.md#dates)

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

<!--
* **Placements** - Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)
-->

* **Personalização de URL**: ao adicionar URLs como conteúdo às representações de suas ofertas, agora é possível personalizar esses URLs usando o editor de expressão. [Saiba mais](../offers/offer-library/add-representations.md)

* **Limite** - Agora você pode redefinir o contador de limite de oferta diariamente, semanalmente ou mensalmente. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

* **Limite** - Agora você pode escolher qual evento do Adobe Experience Platform deve ser observado para o limite de offer decisioning. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

## Versão de janeiro de 2023 {#jan-2023-release}

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

* Ao adicionar uma **Qualificação de segmento** ou um **Segmento de leitura** em uma jornada, o namespace agora é pré-preenchido, por padrão, com o último namespace usado. Consulte as seções [Qualificação de segmento](../building-journeys/segment-qualification-events.md#about-segment-qualification) e [Segmento de leitura](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

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
