---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6e436424d0b7bd4f6172f4a4c00cc8c74c9570af
workflow-type: tm+mt
source-wordcount: '1938'
ht-degree: 69%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes.

Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais.  Uma seção dedicada de [Atualizações mais recentes](#updates-rn) destaca novos recursos e melhorias à medida que são implantados na produção, para que você sempre seja informado sobre todas as alterações em tempo real. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Atualizações mais recentes {#updates-rn}

Os novos recursos e aprimoramentos lançados nas últimas semanas estão listados abaixo, com a data de disponibilidade. Elas serão agrupadas com o conteúdo das próximas notas de versão no final do mês. Consulte também as [notas de versão mais recentes abaixo](#latest-rn).

### Novos recursos {#updates-features}

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
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p>Para mais informações, consulte a <a href="../personalization/functions/helpers.md#execution-metadata">documentação detalhada</a></p>
<p>Data de disponibilidade: 13 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>O agente de experimentação está aqui!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, o Agente de experimentação está disponível na Journey Optimizer. </p>
<p>O Agente de experimentação é uma ferramenta alimentada por IA que moderniza como você pode executar e gerenciar experimentos digitais em sites, emails, mensagens por push e aplicativos. Ele ajuda você a executar experimentos com mais eficiência, organizar metas de negócios e gerar insights acionáveis, destacando o que funcionou, o que não funcionou e onde experimentar em seguida.</p>
<p>Para mais informações, consulte a <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">documentação detalhada</a></p>
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
<p>Para mais informações, consulte a <a href="../email/pdf-attachments.md">documentação detalhada</a></p>
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

**Novos alertas de jornada**

Novos alertas pré-configurados estão disponíveis para o jornada: [Taxa de Descarte de Perfil Excedida](../reports/alerts.md#alert-discard-rate) (Taxa de descartes de perfil para perfis inseridos nos últimos 5 minutos excedeu o limite), [Taxa de Erro de Ação Personalizada Excedida](../reports/alerts.md#alert-custom-action-error-rate) (Taxa de erros de ação personalizada para chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite) e [Taxa de Erro de Perfil Excedida](../reports/alerts.md#alert-profile-error-rate) (Taxa de perfis com erro para perfis inseridos nos últimos 5 minutos excedeu o limite). É possível modificar os valores limite e assinar alertas individuais em nível de jornada em vez de alertas globais.

Data de disponibilidade: 14 de outubro de 2025

**Suporte a atributos personalizados para o endereço Mailto (cancelar inscrição)**

Com o Journey Optimizer, se você estiver gerenciando o consentimento fora do Adobe, é possível definir endpoints personalizados externos ao definir seu próprio link de cancelamento de inscrição com um clique e um endereço de email de cancelamento de inscrição personalizado na configuração de email. Quando os destinatários clicam no link para cancelar assinatura, o Journey Optimizer anexa alguns parâmetros padrão específicos do perfil ao evento de atualização de consentimento.

Para personalizar ainda mais os endpoints personalizados, agora é possível definir atributos personalizados que também serão anexados ao evento de consentimento. [Leia mais](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esse recurso já está disponível para a **[!UICONTROL URL para Cancelamento de Inscrição com Um Clique]** personalizada desde agosto de 25 e agora é lançado para a opção **[!UICONTROL Mailto (cancelar inscrição)]** em Disponibilidade Limitada. Entre em contato com o seu representante da Adobe para obter acesso.

Data de disponibilidade: 6 de outubro de 2025

## Notas de versão de setembro de 2025 {#latest-rn}

**Data de lançamento**: 23 a 24 de setembro de 2025

### Novos recursos {#sept-25-9-features}

<table>
<thead>
<tr>
<th><strong>Acelerador de experimentação do Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Acelerador de experimentação do Journey Optimizer é um produto de IA desenvolvido para elevar o nível das suas experiências. Criado para usuários do Adobe Journey Optimizer e do Adobe Target, ele unifica o gerenciamento de experiências, fornece oportunidades e insights alimentados por IA e introduz um novo agente de experimentação.</p>
<p>Você pode esperar por:</p>
<ul>
<li><strong>Inventário de experimentos unificado:</strong> visualize, filtre e gerencie rapidamente todos os experimentos do Adobe Journey Optimizer e do Adobe Target em um espaço de trabalho central.</li>
<li><strong>Insights e oportunidades de experimentos de IA:</strong> vá além das leituras estatísticas com insights e recomendações orientados por IA generativa. Cada experimento agora apresenta oportunidades acionáveis e completas com lógica de apoio para que as equipes possam decidir com mais confiança o que testar a seguir.</li>
<li><strong>Suporte a MAB (Multi-Armed Bandit) no Journey Optimizer:</strong> maximize o impacto enquanto reduz o tráfego desperdiçado com experimentos de Multi-Armed Bandit. Em vez de dividir públicos-alvo uniformemente, o MAB aloca automaticamente mais visitantes para as variações de melhor desempenho em tempo real, para que você possa entregar melhores experiências a mais clientes enquanto ainda aprende o que funciona.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>Para mais informações, consulte a <a href="../content-management/experiment-accelerator.md">documentação detalhada</a></p>
<p>Data de disponibilidade: 3 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>O Journey Agent chegou!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Desenvolvido pelo <a href="https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, o Journey Agent está disponível no Journey Optimizer. Ele permite analisar jornadas por meio de uma interface de linguagem natural. O agente detectará conflitos de público-alvo ou agendamento e suspensões de perfil em uma jornada para ajudar você a tomar medidas para resolvê-los. Em breve, você poderá criar jornadas com suporte agentivo.</p>
<p>Para mais informações, consulte a <a href="https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">documentação detalhada</a></p>
<p>Data de disponibilidade: 24 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo escuro no designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O designer de email do Journey Optimizer agora permite alternar para a exibição no modo escuro, onde você pode definir outras configurações personalizadas específicas que serão exibidas somente para destinatários que lerem seus emails no modo escuro.</p>
<p>Observe o seguinte:</p>
<ul>
<li>A renderização final no modo escuro pode variar e depende do cliente de email do destinatário.</li>
<li>Nem todos os clientes de email permitem o modo escuro. Além disso, alguns clientes de email aplicam seu próprio modo escuro padrão para todos os emails recebidos. Em ambos os casos, as configurações personalizadas definidas no designer de email não podem ser renderizadas.</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Para mais informações, consulte a <a href="../email/dark-mode.md">documentação detalhada</a></p>
 <p>Data de disponibilidade: 16 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Otimização do caminho da jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use o novo nó Otimizar para direcionar públicos-alvo específicos ou execute testes A/B para determinar o melhor caminho para atender aos KPIs focados em negócios.</p>
<p>Essa ferramenta permite testar, variar e personalizar as comunicações, o sequenciamento e o momento para melhor alcançar os clientes.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>Para mais informações, consulte a <a href="../building-journeys/optimize.md">documentação detalhada</a></p>
<p>Data de disponibilidade: 4 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Método de delegação personalizado para subdomínios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além da delegação completa e do método CNAME, há um novo método de configuração de subdomínio disponível: o método de delegação personalizado, que permite controlar e manter totalmente todos os aspectos do DNS necessários para entregar, renderizar e rastrear mensagens.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>Para mais informações, consulte a <a href="../configuration/delegate-custom-subdomain.md">documentação detalhada</a></p>
<p>Data de disponibilidade: 4 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Usar dados da Adobe Experience Platform para personalização e tomada de decisão</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lançado anteriormente em beta público, esse recurso agora está disponível para todos os ambientes. Nesta versão, os seguintes aprimoramentos foram introduzidos:</p>
<ul><li>Suporte para personalização de pesquisa de conjunto de dados em canais de entrada.</li>
<li>A função auxiliar "datasetLookup" agora pode ser usada em fragmentos de expressão. Por enquanto, esse recurso está disponível para um conjunto limitado de clientes. Para obter acesso, entre em contato com um representante da Adobe.</li>
<li>Uma opção na interface de gerenciamento de conjuntos de dados agora permite habilitar conjuntos de dados para personalização de pesquisa, sem precisar executar uma chamada de API.</li>
<li>Monitoramento aprimorado para monitorar o status de ingestão de dados e saber quando os conjuntos de dados estão prontos para pesquisa.</li>
<li>Diretrizes e medidas de proteção atualizadas para garantir desempenho e confiabilidade ideais.</li>
<li>Os conjuntos de dados da Adobe Experience Platform agora podem ser aproveitados nas regras de limite do serviço de decisão.</li></ul></p>
<p>Para mais informações, consulte a <a href="../data/lookup-aep-data.md">documentação detalhada</a></p>
<p>Data de disponibilidade: 1º de setembro de 2025</p>
</td>
</tr>


### Aprimoramentos {#sept-25-9-improvements}

* **Suporte a webhook para campanhas acionadas por API**\
  Campanhas acionadas por API agora oferecem suporte a webhooks. Configure um URL de webhook para receber atualizações de status em tempo real para cada mensagem, melhorando a observabilidade e permitindo o monitoramento e a automação contínuos. [Leia mais](../configuration/feedback-webhooks.md)

  Data de disponibilidade: 29 de setembro de 2025

* **Suporte a mTLS para Canal de SMS**
Ao configurar um provedor de SMS personalizado, agora há a opção de habilitar a autenticação TLS mútua (mTLS), que exige que o cliente e o servidor confirmem as identidades um do outro antes que uma conexão segura seja estabelecida. [Leia mais](../sms/sms-configuration-custom.md) - Data de disponibilidade: 23 de setembro de 2025

* **Esquemas baseados em modelo**\
  Os esquemas baseados em modelo agora podem ser usados pelo para oferecer suporte às suas necessidades de modelagem relacional em campanhas orquestradas. [Leia mais](../orchestrated/gs-schemas.md) - Data de disponibilidade: 23 de setembro de 2025

* **Suporte à pesquisa de conjunto de dados em jornadas**\
  A nova atividade em jornadas **Consulta de conjunto de dados** permite recuperar dados dinamicamente de conjuntos de dados de registros da Adobe Experience Platform durante o tempo de execução. Ao aproveitar esse recurso, é possível acessar dados que podem não estar no perfil ou no conteúdo do evento, garantindo que as interações com o cliente sejam relevantes e oportunas. [Leia mais](../building-journeys/dataset-lookup.md) - Data de disponibilidade: 23 de setembro de 2025

  Esta atividade está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.

* **Redirecionar suporte em ações personalizadas da jornada**\
  Redirecionamentos (302) agora são aceitos em Ações personalizadas da jornada. - Data de disponibilidade: 23 de setembro de 2025

* **Alertas de monitoramento de configuração de canais**: agora você pode se inscrever para receber alertas do sistema por email ou pela central de notificações do Journey Optimizer caso ocorra um erro de configuração de canais de email ao usar o tipo de delegação de subdomínio personalizado. [Leia mais](../reports/alerts.md#alert-channel-config-failure) - Data de disponibilidade: 23 de setembro de 2025

* **Solicitações para cancelar assinatura com um clique**: introduzimos melhorias que fortalecem ainda mais o tratamento de solicitações para cancelar assinatura com um clique configuradas no Adobe Managed, garantindo um processamento confiável e consistente. - Data de disponibilidade: 23 de setembro de 2025

* **Parâmetros de corpo JSON aninhados agora são aceitos na autenticação personalizada**\
  Ao configurar a autenticação personalizada para uma ação personalizada, objetos JSON aninhados (por exemplo, subobjetos dentro de `bodyParams`) agora são aceitos. [Leia mais](../datasource/external-data-sources.md#custom-authentication-mode) - Data de disponibilidade: 18 de setembro de 2025

* **Frequência de limitação de redefinição por hora**: agora é possível aplicar limite por hora para conjuntos de regras de canal. Anteriormente disponível em Disponibilidade limitada, esse recurso agora está disponível para todos os ambientes e permite que você escolha 1 hora (anteriormente 3 horas). [Leia mais](../conflict-prioritization/channel-capping.md) - Data de disponibilidade: 17 de setembro de 2025

* **Simulação de variações de conteúdo para todos os canais de entrada**\
  Anteriormente disponível apenas para os canais de email, SMS e notificação por push, a simulação de variações de conteúdo agora também se aplica a todos os canais de entrada. [Leia mais](../test-approve/simulate-sample-input.md) - Data de disponibilidade: 17 de setembro de 2025

* **Expressão para regras de limite do serviço de decisão**: agora é possível criar suas próprias expressões para definir o limite de uma regra de um item de decisão. [Leia mais](../experience-decisioning/items.md#capping) - Data de disponibilidade: 16 de setembro de 2025

* **Suporte a domínio dinâmico**: o Journey Optimizer agora oferece suporte à personalização completa e do URL base de domínios predefinidos aceitos pela Adobe. [Leia mais](../personalization/personalization-build-expressions.md#where) - Data de disponibilidade: 12 de setembro de 2025

  Esse recurso está em disponibilidade limitada para alguns clientes.

* **Webhooks** - Esta versão apresenta os seguintes aprimoramentos para Webhooks ao configurar um provedor de SMS personalizado:

   * Agora você pode definir a finalidade do webhook, de Entrada ou de Feedback, dependendo do tipo de dados que deseja capturar. [Leia mais](../sms/sms-configuration-custom.md#webhook) - Data de disponibilidade: 23 de setembro de 2025

   * A interface para configurar palavras-chave foi aprimorada para facilitar a configuração. [Leia mais](../sms/sms-configuration-custom.md#webhook) - Data de disponibilidade: 23 de setembro de 2025

* **SMS**

   * Ao configurar um provedor SMS personalizado, agora é possível definir uma palavra-chave **Padrão** usada quando um SMS recebido contém uma palavra-chave não reconhecida. Você também pode criar palavras-chave **Custom** para ações específicas. [Leia mais](../sms/sms-configuration-custom.md) - Data de disponibilidade: 23 de setembro de 2025

   * Agora você pode acessar respostas indefinidas de palavras-chave de entrada enviadas por uma mensagem SMS, incluindo erros de digitação, palavras ou frases que não estão explicitamente definidos na configuração. Eles são armazenados no conjunto de dados do **Evento de experiência de rastreamento de email do AJO**, em **InboundMessage**, por 13 meses. Disponível somente com Sinch, Infobip e provedor de SMS personalizado. - Data de disponibilidade: 23 de setembro de 2025

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025-->

<!--
### Coming soon {#sept-25-9-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

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


<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
