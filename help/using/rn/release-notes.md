---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3343f4f525db4b8bc5b5f6e12f9c6f5f0290b034
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 32%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de versão de maio de 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Novos recursos {#25-05-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Exibição de calendário para estoque de Campanha e Jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma visualização de calendário agora está disponível nas listas de jornadas e campanhas. Ele permite visualizar todas as jornadas e ativações de campanhas nas respectivas listas.</p>
<p>No momento, essa alteração está disponível apenas para algumas organizações (disponibilidade limitada). Para solicitar acesso, use <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">este formulário</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obter mais informações, consulte estas seções: <a href="../building-journeys/journey-ui.md">Procurar e filtrar suas jornadas</a>, <a href="../campaigns/modify-stop-campaign.md">Acessar campanhas</a>.</p>
<p>Data de disponibilidade: quinta-feira, 28 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do fragmento de conteúdo do Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a integração do Adobe Experience Manager e do Adobe Journey Optimizer, agora é possível usar Fragmentos de conteúdo do Adobe Experience Manager sem esforço no conteúdo do Journey Optimizer. Essa conexão perfeita facilita o acesso e o uso do conteúdo do AEM diretamente no Journey Optimizer.</p>
<p>Anteriormente disponível para um conjunto limitado de organizações (DL), esse recurso agora está disponível para o público geral com o seguinte aprimoramento: agora é possível definir espaços reservados e mapear valores de personalização na assinatura do fragmento usando o modo Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Para obter mais informações, consulte a <a href="../integrations/aem-fragments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sábado, 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração com o Adobe Experience Manager Dynamic Media</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os ativos do Dynamic Media agora estão diretamente disponíveis e acessíveis no Journey Optimizer. Essa integração permite:</p>
<ul>
<li>Gerencie centralmente ativos com atualizações em tempo real.</li>
<li>Modifique as configurações de ativos, como largura e altura, instantaneamente.</li>
<li>Personalize modelos do Dynamic Media atualizando o conteúdo e adicionando campos de personalização.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../integrations/aem-dynamic.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sábado, 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID complementar para jornadas acionadas por eventos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar jornadas usando uma ID de perfil juntamente com outro identificador, como uma ID de pedido, ID de assinatura ou ID de receita, permitindo que o mesmo perfil esteja na mesma jornada várias vezes de uma vez. Isso permite cenários como gerenciar vários pedidos ou assinaturas em paralelo, com cada instância seguindo seu próprio caminho pela jornada.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/supplemental-identifier.md">documentação detalhada</a>.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Data de disponibilidade: sábado, 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simular variações de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de Disponibilidade Geral, o recurso agora inclui suporte para conteúdo multilíngue e experimentos de conteúdo, permitindo que você teste variações em diferentes idiomas e tratamentos. Além disso, agora ele é compatível com atributos contextuais (além dos atributos de perfil), permitindo testes de conteúdo ainda mais dinâmicos e específicos.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Para obter mais informações, consulte a <a href="../test-approve/simulate-sample-input.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: sábado, 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronizar a programação de público-alvo de leitura com o trabalho de segmentação em lote</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar execuções diárias de jornada após a conclusão da segmentação em lote. Essa opção agora está disponível em jornadas programadas diariamente para todos os clientes. Ele permite definir um período de até 6 horas para aguardar os dados do público-alvo de trabalhos de segmentação em lote, garantindo que as jornadas sejam executadas com os dados mais atualizados ou ignoradas, se não estiverem prontas.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-audience.md#schedule">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 20 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Provedor de SMS personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite configurar provedores de SMS adicionais além das opções padrão: Sinch, Infobip e Twilio. Com a configuração personalizada do provedor SMS, você pode integrar diretamente provedores de terceiros, aproveitar a personalização avançada de carga para mensagens dinâmicas e gerenciar preferências de consentimento (aceitação/recusa) para garantir a conformidade.</p>
<p>Para obter mais informações, consulte a <a href="../sms/sms-configuration-custom.md">documentação detalhada</a>.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Data de disponibilidade: quarta-feira, 20 de maio de 2025</p>
</td>
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
<p>Agora é possível aplicar rapidamente temas pré-aprovados para garantir a consistência da marca em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de maneira independente, reduzindo a dependência de equipes de design.</p>
<p>No momento, esse recurso está na versão beta, disponível apenas para clientes beta. Para participar do programa beta, entre em contato com seu representante da Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 14 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisão - Novo construtor de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar fórmulas de classificação específicas no serviço de decisão por definir e combinar critérios na nova interface aprimorada. Em vez de depender apenas de uma prioridade de oferta estática, você pode definir fórmulas de classificação personalizadas que combinam pontuações do modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta e sinais contextuais por meio de uma interface guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/exd-ranking-formulas.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quinta-feira, 14 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Conflict & prioritization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, managing the volume and timing of campaigns and journeys is essential to avoid overwhelming customers with too many interactions. Journey Optimizer now offers several tools for conflict management and prioritization - previously available only to limited-access (LA) organizations - that are now generally available (GA).</p>
<p>Previously released in Limited Availability, this capability is now available to all environments. With this General Availability release, the following enhancements have been introduced:</p>
<ul>
<li>Expanded Support: Conflict management tools now support both Unitary Journeys and Audience Qualification Journeys, in addition to Read audience journeys.</li>
<li>Improved Troubleshooting: Two new step event fields are now available in the Query Service, enabling you to analyze why a profile was rejected from a journey or campaign.</li>
<li>Enhanced Reporting: Reports now indicate which specific rule excluded a profile from a journey or campaign, providing greater transparency and actionable insights.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>For more information, refer to the <a href="../conflict-prioritization/gs-conflict-prioritization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<!--table>
<thead>
<tr>
<th><strong>Scale your Experimentation winner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Scale the Winner enables you to automatically or manually roll out the winning variation of an experiment to your full audience. This feature ensures that, once a top performer is identified, you can maximize its reach and effectiveness without constant manual oversight.</p>
</td>
</tr>
</tbody>
</table-->


### Melhorias {#25-05-improv}

As melhorias incluídas nesta versão estão listadas abaixo.


* **Suporte a novos objetos de campanha para cópia da sandbox** - Data de disponibilidade: 15 de maio de 2025

  Ao copiar campanhas em várias sandboxes usando os recursos de exportação e importação de pacotes, as seguintes dependências também são copiadas: configurações de canal, variantes e configurações de experimento, políticas de decisão e itens. [Leia mais](../configuration/copy-objects-to-sandbox.md)

  <!--* **Decisioning** - Availability date: May 16, 2025

    Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows. [Read more](../configuration/copy-objects-to-sandbox.md#decisioning)-->

* **Pastas para páginas de aterrissagem** - Data de disponibilidade: 9 de maio de 2025

  Para gerenciar facilmente as landing pages, agora é possível usar pastas para organizá-las com mais eficiência em uma hierarquia estruturada. [Leia mais](../landing-pages/manage-lp.md)

* **Correspondência direta: Suporte à chave SSH para conexões SFTP** - Data de disponibilidade: 5 de maio de 2025

  Na configuração de roteamento de arquivo de correspondência direta, além do SFTP existente com tipo de autenticação de senha, agora é possível exportar seu arquivo de correspondência direta para um servidor SFTP com autenticação de chave SSH. [Leia mais](../direct-mail/direct-mail-configuration.md)

* **Ativação de pílulas para personalização** - Data de disponibilidade: 5 de maio de 2025

  Um novo botão “Pílulas” foi adicionado ao editor de personalização. Quando habilitado, os atributos contextuais e de perfil são exibidos como pílulas, melhorando a legibilidade do código. [Leia mais](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esse recurso será implantado gradualmente em todos os ambientes nos próximos 30 dias.

* Suporte a &#39;Redirecionar para URL&#39; do **no canal da Web** - Data de disponibilidade: 20 de maio de 2025

  O canal da Web do Journey Optimizer agora permite redirecionar os visitantes para outro URL existente, em vez de criar uma nova variação no editor visual. Esse recurso pode ser usado para executar experimentos comparando duas páginas completamente diferentes, em vez de apenas alterar alguns elementos em uma página. [Leia mais](../web/create-web.md#web-redirect-to-url)

* **Pastas para modelos e fragmentos** - Data de disponibilidade: 20 de maio de 2025

  As pastas permitem organizar os objetos de forma mais fácil e eficaz em uma hierarquia estruturada. Anteriormente disponíveis para apenas algumas organizações (disponibilidade limitada), as pastas agora estão disponíveis para todos os usuários (disponibilidade geral), permitindo o gerenciamento de modelos e fragmentos de conteúdo. Leia mais nas seções [Modelos de conteúdo](../content-management/access-content-templates.md#folders) e [Fragmentos](../content-management/manage-fragments.md#folders).

* **Rastreamento de cliques em modelos de email** - Data de disponibilidade: 20 de maio de 2025

  O rastreamento de cliques nos elementos `<area>` nos mapas de imagem no conteúdo de email agora tem suporte nativo no [!DNL Journey Optimizer]. Isso garante que as áreas do mapa de imagem recebam os mesmos dados de rastreamento de encapsulamento, dados de rastreamento e parâmetros anexados que os hiperlinks padrão. [Saiba mais sobre o rastreamento de mensagens](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Painel direito na lista de campanhas** - Data de disponibilidade: 20 de maio de 2025

  Na lista de campanhas, selecionar uma campanha agora abre um painel que exibe seus detalhes.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.

* **Decision item attribute support for decisioning rules**
  
  You can now leverage decision item attributes to create decisioning rules.

* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

