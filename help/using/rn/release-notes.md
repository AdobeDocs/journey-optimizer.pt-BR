---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 913104934e78b61b91ea3fca21ee80372050a1fb
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 48%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais.  Uma seção dedicada de [Atualizações mais recentes](#updates-rn) destaca novos recursos e melhorias à medida que são implantados na produção, para que você sempre seja informado sobre todas as alterações em tempo real. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de versão de outubro de 2025 {#oct-25-10-rn}

**Data de lançamento**: quinta-feira, 22 de outubro de 2025

### Novos recursos {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Formulários personalizados de página de destino</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o [!DNL Journey Optimizer], agora é possível capturar atributos de perfil por meio das páginas de destino.</p>
<p>Crie, projete e gerencie formulários personalizados adaptados às suas necessidades com base em um conjunto de dados específico. Em seguida, é possível usar esses formulários em páginas de destino para adicionar os atributos de perfil de sua escolha ao conjunto de dados definido para cada formulário.</p>
<p>No momento, esse recurso está na disponibilidade limitada para clientes nos Estados Unidos e na Austrália. Entre em contato com o representante da Adobe para obter acesso.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../landing-pages/lp-forms.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sexta-feira, 23 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Período de Silêncio/Exclusões Baseadas no Tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Quiet hours permite definir exclusões com base no tempo para canais de email, SMS, push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade.</p>
<p>Você pode aplicar horas de silêncio por meio de conjuntos de regras, que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
<p>Atualmente, as regras de horário de silêncio estão disponíveis apenas para um conjunto de organizações (Disponibilidade limitada). Para ser adicionado à lista de espera, entre em contato com o representante da Adobe.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/quiet-hours.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 22 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Mensagens de alta taxa de transferência para campanhas de email acionadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo modo de mensagens transacionais de alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real em larga escala e aceita até 5.000 transações por segundo com maior disponibilidade. Esse modo também aceita mensagens transacionais sem fazer referência ou criar perfis de clientes, como check-out de convidado, confirmação de pedido, redefinições de senha, notificações de segurança e outros avisos operacionais/de serviço.</p>
<p>Esse recurso só está disponível para o canal de email, em organizações que compraram a oferta complementar de mensagens transacionais de alta taxa de transferência da Adobe. Entre em contato com seu representante da Adobe para obter mais informações.</p>
<p>Para obter mais informações, consulte a <a href="../campaigns/api-triggered-high-throughput.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 22 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regras de direcionamento reutilizáveis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para economizar tempo e esforço, o Journey Optimizer agora permite criar regras reutilizáveis em um menu de interface dedicada e aproveitá-las ao criar o direcionamento, como parte da Otimização de conteúdo em uma campanha ou jornada, na atividade Otimizar jornada.</p>
<p>As regras de direcionamento estão atualmente em Disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso. Observe que esse recurso só está disponível para organizações que compraram a oferta complementar do Decisioning. Ele será implantado progressivamente para todos os clientes.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/rules.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 22 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos alertas de Jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos alertas pré-configurados estão disponíveis para monitorar a execução do jornada:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Taxa de Descarte de Perfil Excedida</a>: Taxa de descartes de perfil para perfis inseridos nos últimos 5 minutos excedeu o limite</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Taxa de Erro de Ação Personalizada Excedida</a>: Taxa de erros de ação personalizada para chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Taxa de Erro de Perfil Excedida</a>: Taxa de perfis com erro em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite.</li></ul> <p>É possível modificar os valores limite e assinar alertas individuais em nível de jornada em vez de alertas globais.</p>
<p>Para obter mais informações, consulte a <a href="../reports/alerts.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 14 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Auxiliar de metadados de execução</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova função auxiliar "executionMetadata" está disponível no editor de personalização. Ele permite anexar informações contextuais a qualquer ação nativa e capturá-las em um conjunto de dados para exportação para sistemas externos.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Para obter mais informações, consulte a <a href="../personalization/functions/helpers.md#execution-metadata">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 13 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator com agente de experimentação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer Experimentation Accelerator agora inclui o Agente de experimentação, uma ferramenta conversacional alimentada por IA que permite a você interagir com seus experimentos, insights e oportunidades. Ele melhora a experiência do Journey Optimizer Experimentation Accelerator, ajudando você a executar experimentos com mais eficiência, descobrir o que funciona e descobrir onde otimizar a seguir.</p>
<p>Para obter mais informações, consulte a <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sábado, 10 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anexos de PDF para emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível anexar um arquivo PDF estático a uma mensagem de email enviada com o Journey Optimizer.</p>
<ul>
<li>É possível enviar até 6 mensagens com um anexo PDF por perfil em um ano.</li>
<li>O tamanho máximo para cada anexo é 5 MB.</li>
<li>Para qualquer tamanho ou volume adicional, é possível comprar o complemento Anexos em PDF. Para obter mais informações, entre em contato com um representante da Adobe.</li>
</ul>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para obter mais informações, consulte a <a href="../email/pdf-attachments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 30 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pública para recuperar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível para recuperar jornadas e seus objetos associados, como campanhas e superfícies.</p>
<p>Para mais informações, consulte a <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentação detalhada</a></p>
<p>Data de disponibilidade: 25 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Aprimoramentos {#updates-improvements}

<!--Availability date: October 22, 2025-->

**Campo de execução para o canal do WhatsApp**

Além de email e SMS, você pode saber como atualizar o campo de execução padrão para seus deliveries do WhatsApp no nível da sandbox. Também é possível substituir o campo de execução definido globalmente, alterando-o nos parâmetros avançados da atividade de jornada do WhatsApp ou na configuração do canal do WhatsApp. [Leia mais](../configuration/primary-email-addresses.md)

Data de disponibilidade: quinta-feira, 22 de outubro de 2025

**Suporte a atributos personalizados para endereço Mailto (cancelar assinatura)**

Com o Journey Optimizer, se você estiver gerenciando consentimento fora da Adobe, é possível configurar pontos de acesso externos personalizados por definir seu próprio link de cancelamento de assinatura com um clique e um endereço de email de cancelamento de assinatura personalizado na configuração de email. Quando os destinatários clicam no link para cancelar a assinatura, o Journey Optimizer anexa alguns parâmetros padrão específicos do perfil ao evento de atualização de consentimento.

Para customizar ainda mais os pontos de acesso personalizados, agora é possível definir atributos personalizados que também serão anexados ao evento de consentimento. [Leia mais](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esse recurso já está disponível para o **[!UICONTROL URL de cancelamento de assinatura com um clique]** personalizado desde agosto de 2025 e agora foi lançado para a opção **[!UICONTROL Mailto (cancelar assinatura)]** em disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Data de disponibilidade: 6 de outubro de 2025

### Em breve {#oct-25-10-soon}

Os recursos e aprimoramentos a seguir estão programados para serem lançados nos próximos dias. **As informações estão sujeitas a alterações**. Links, telas e documentação atualizados serão compartilhados assim que essas atualizações estiverem ativas na produção.

#### Novos recursos {#oct-25-10-soon-features}

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
<p>Anteriormente lançado na versão beta, esse recurso agora está disponível para várias organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<!--img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p-->
</td>
</tr>
</tbody>
</table>

#### Aprimoramentos {#oct-25-10-soon-improvements}

**Decisão em emails por meio de modelos de IA**

Agora você pode usar os modelos de IA para otimizar o melhor conteúdo do seu email por meio do uso do Decisioning. Por exemplo, esse recurso permite oferecer o melhor conteúdo com base em eventos personalizados, como compras, cliques de botão, adicionar ao carrinho etc.

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

-->
