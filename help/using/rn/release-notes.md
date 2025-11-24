---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 585abb9929499ae18a2e4fcaeb5f9f158b01698d
workflow-type: tm+mt
source-wordcount: '1498'
ht-degree: 98%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções também de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais.  Uma seção dedicada de [Atualizações mais recentes](#latest-updates) destaca novos recursos e melhorias à medida que são implantados na produção para informar sobre todas as alterações em tempo real. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Atualizações mais recentes {#latest-updates}

Os novos recursos e aprimoramentos lançados nas últimas semanas estão listados abaixo, com a data de disponibilidade. Eles serão agrupados com o conteúdo das próximas notas de versão no final do mês. Consulte também as [notas de versão mais recentes abaixo](#latest-rn).

### Novos recursos {#features}

<thead>
<tr>
<th><strong>Nova API para recuperar Campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível, permitindo recuperar e inspecionar programaticamente dados relacionados à campanha, como detalhes, versões e configurações.</p>
<p>Para obter mais informações, consulte a <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">documentação detalhada</a>.</p>
<p>Data de disponibilidade: terça-feira, 24 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos alertas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Três novos alertas de jornada agora estão disponíveis para ajudar a monitorar e rastrear os eventos de ciclo de vida da jornada e o desempenho da ação personalizada:</p>
<ul>
<li><strong>Jornada publicada</strong>: receba notificações quando uma jornada for publicada por um profissional na tela de jornada.</li>
<li><strong>Jornada concluída</strong>: receba alertas quando uma jornada for concluída, com definições específicas baseadas no tipo de jornada (Público-alvo de leitura ou acionada por evento).</li>
<li><strong>Limite de ação personalizada acionado</strong>: receba uma notificação quando o limite for ativado em um ponto de acesso de ação personalizada.</li>
</ul>
<p>É possível se inscrever nesses alertas no nível da organização ou para jornadas específicas.</p>
<p>Para obter mais informações, consulte a <a href="../reports/alerts.md#journey-alerts">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 5 de novembro de 2025</p>
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
<p>Lançado anteriormente na versão beta, esse recurso agora está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o representante da Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 5 de novembro de 2025</p>
</td>
</tr>
</tbody>
</table>

## Notas da versão de outubro de 2025 {#latest-rn}

### Novos recursos {#oct-25-10-features}


<table>
<thead>
<tr>
<th><strong>Conversor de imagem para HTML</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O conversor de imagem para HTML é um recurso viabilizado por IA que converte designs de imagem estática em modelos de conteúdo de email HTML totalmente personalizáveis e modulares. Essa ferramenta sem código permite que os profissionais de marketing transformem designs visuais em modelos de email responsivos e editáveis sem a necessidade de conhecimento técnico especializado, o que é perfeito para a migração de plataforma, a criação rápida de modelos e a criação de bibliotecas de modelos reutilizáveis.</p>
<p><img src="../email/assets/email_designer_converted_img.png"/></p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.</p>
<p>Para obter mais informações, consulte a <a href="../email/image-to-html.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 30 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Monitoramento e relatórios de ação personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esse recurso oferece melhor visibilidade da integridade e do desempenho do ponto de acesso de ação personalizada. Um novo painel de monitoramento de ação personalizada e campos correspondentes no conjunto de dados de eventos de etapa da jornada ajudarão a monitorar chamadas bem-sucedidas, erros, taxa de transferência, tempo de resposta e tempo de espera na fila dos pontos de acesso de ação personalizada. Agora você pode entender rapidamente quando, onde e por que uma situação anômala está ocorrendo em uma ação personalizada.</p>
<p>No momento, esse recurso está em disponibilidade limitada para clientes.</p>
<p>Para obter mais informações, consulte a <a href="../action/reporting.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 28 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

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
<p>Data de disponibilidade: 23 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Período de silêncio/ Exclusões com base no tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Período de silêncio permite definir exclusões com base no tempo para canais de email, SMS, Push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando a respeitar as preferências do cliente e os requisitos de conformidade.</p>
<p>É possível aplicar o período de silêncio por meio de conjuntos de regras que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso.</p>
<p>Atualmente, as regras de horário de silêncio estão disponíveis apenas para um conjunto de organizações (Disponibilidade limitada).  Eles estarão progressivamente disponíveis para todos os clientes em versões futuras.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/quiet-hours.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

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
<th><strong>Mensagens com alta taxa de transferência para campanhas de email acionadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo modo de mensagens transacionais com alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real de grande escala e aceita até 5.000 transações por segundo com maior disponibilidade. Esse modo também é compatível com mensagens transacionais sem referência ou criação de perfis de clientes, como check-out de convidado, confirmação de pedido, redefinições de senha, notificações de segurança e outras notificações operacionais/de serviço.</p>
<p>Esse recurso está disponível somente para o canal de email e para organizações que adquiriram a oferta complementar de mensagens transacionais com alta taxa de transferência da Adobe. Entre em contato com o representante da Adobe para obter mais informações.</p>
<p>Para obter mais informações, consulte a <a href="../campaigns/api-triggered-high-throughput.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de outubro de 2025</p>
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
<p>Para economizar tempo e esforço, o Journey Optimizer agora permite criar regras reutilizáveis em um menu de interface dedicado e aproveitá-las ao realizar o direcionamento, como parte da Otimização de conteúdo em uma campanha ou jornada ou na atividade Otimizar jornada.</p>
<p>As regras de direcionamento estão atualmente em Disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso. Observe que esse recurso só está disponível para organizações que adquiriram a oferta complementar da Tomada de decisões. Ele será implantado progressivamente para todos os clientes.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/rules.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos alertas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos alertas pré-configurados estão disponíveis para monitorar a execução da jornada:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Taxa de descarte de perfil excedida</a>: a proporção de descartes de perfil em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite.</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Taxa de erros de ação personalizada excedida</a>: a proporção de erros de ação personalizada em relação às chamadas HTTP bem-sucedidas nos últimos cinco minutos excedeu o limite</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Taxa de erro de perfil excedida</a>: a proporção de perfis com erro em relação aos perfis inseridos nos últimos cinco minutos excedeu o limite.</li></ul> <p>É possível modificar os valores limite e assinar alertas individuais em nível de jornada em vez de alertas globais.</p>
<p>Para obter mais informações, consulte a <a href="../reports/alerts.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 14 de outubro de 2025</p>
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
<p>Uma nova função auxiliar "executionMetadata" está disponível no editor de personalização. Ela permite anexar informações contextuais a qualquer ação nativa e capturá-las em um conjunto de dados para exportação a sistemas externos.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Para obter mais informações, consulte a <a href="../personalization/functions/helpers.md#execution-metadata">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 13 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator com o Experimentation Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer Experimentation Accelerator agora inclui o Experimentation Agent, uma ferramenta conversacional viabilizada por IA que permite interagir com experimentos, insights e oportunidades. Ele melhora a experiência do Journey Optimizer Experimentation Accelerator, ajudando na realização de experimentos com mais eficiência, em saber o que funciona e na descoberta de onde otimizar a seguir.</p>
<p>Para obter mais informações, consulte a <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=pt-BR" target="_blank">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 10 de outubro de 2025</p>
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



### Aprimoramentos {#updates-improvements}

**Campo de execução para o canal do WhatsApp**

Além de email e SMS, é possível atualizar o campo de execução padrão para as entregas do WhatsApp no nível da sandbox. Também é possível substituir o campo de execução definido globalmente, alterando-o nos parâmetros avançados da atividade de jornada do WhatsApp ou na configuração do canal do WhatsApp. [Leia mais](../configuration/primary-email-addresses.md)

Data de disponibilidade: 22 de outubro de 2025

**Suporte a atributos personalizados para endereço Mailto (cancelar assinatura)**

Com o Journey Optimizer, se você estiver gerenciando consentimento fora da Adobe, é possível configurar pontos de acesso externos personalizados por definir seu próprio link de cancelamento de assinatura com um clique e um endereço de email de cancelamento de assinatura personalizado na configuração de email. Quando os destinatários clicam no link para cancelar a assinatura, o Journey Optimizer anexa alguns parâmetros padrão específicos do perfil ao evento de atualização de consentimento.

Para customizar ainda mais os pontos de acesso personalizados, agora é possível definir atributos personalizados que também serão anexados ao evento de consentimento. [Leia mais](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esse recurso já está disponível para o **[!UICONTROL URL de cancelamento de assinatura com um clique]** personalizado desde agosto de 2025 e agora foi lançado para a opção **[!UICONTROL Mailto (cancelar assinatura)]** em disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Data de disponibilidade: 6 de outubro de 2025

<!--
### Coming soon {#oct-25-10-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

#### New capabilities {#oct-25-10-soon-features}

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved themes to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p>
</td>
</tr>
</tbody>
</table>

#### Improvements {#oct-25-10-soon-improvements}

**Decisioning in emails through AI models**

You can now use AI models to optimize the best content in your email through the use of Decisioning. For example, this capability allows you to offer the best content based on custom events such as Purchases, Button Clicks, Add to Cart, etc.
-->

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
