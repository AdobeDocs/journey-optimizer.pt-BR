---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d69b04be97951a5a57228ea839cb9b9c274a92c2
workflow-type: tm+mt
source-wordcount: '1817'
ht-degree: 68%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Atualizações de setembro de 2025 {#sep-updates}

<table>
<thead>
<tr>
<th><strong>Usar dados do Adobe Experience Platform para personalização e decisão - Disponibilidade limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente lançado em beta público, esse recurso agora está disponível para todos os ambientes com Disponibilidade limitada. Nesta versão, os seguintes aprimoramentos foram introduzidos:</p>
<ul><li>Suporte para personalização de pesquisa de conjunto de dados em canais de entrada.</li>
<li>A função auxiliar "datasetLookup" agora pode ser usada em fragmentos de expressão.</li>
<li>Uma opção na interface de gerenciamento do conjunto de dados agora permite habilitar conjuntos de dados baseados em registro para personalização de pesquisa, sem precisar executar uma chamada de API.</li>
<li>Monitoramento aprimorado para rastrear o status de assimilação de dados e saber quando os conjuntos de dados estão prontos para pesquisa.</li>
<li>Diretrizes e medidas de proteção atualizadas para garantir desempenho e confiabilidade ideais.</li></ul></p>
<p>Para mais informações, consulte a <a href="../data/lookup-aep-data.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

## Notas de versão de agosto de 2025 {#25-8-rn}

**Data de lançamento**: 19 de agosto de 2025

### Novos recursos {#Aug-25-8-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Pausar e retomar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível pausar e retomar jornadas. Esse recurso oferece aos profissionais de jornada maior controle e flexibilidade ao permitir que as jornadas ativas sejam temporariamente suspensas sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.</p>
<p>É possível pausar e retomar apenas uma jornada ou executar operações de pausa e retomada em massa para um grupo de jornadas.</p>
<p>Além disso, é possível aplicar filtros globais a jornadas pausadas para excluir perfis com base em seus atributos.</p>
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para mais informações, consulte a <a href="../building-journeys/journey-pause.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Visualização de calendário</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há uma exibição de calendário disponível nas listas de jornadas e campanhas. Ela permite ver todas as ativações de jornadas e campanhas nas respectivas listas.</p>
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes. Nesta versão com disponibilidade geral, o recurso inclui:</p>
<ul>
<li>Melhorias de design para a navegação pelas datas,</li>
<li>A possibilidade de ver rascunhos de campanha, se tiver definido as datas inicial e final,</li>
<li>Uma nova configuração para ocultar e exibir os itens do calendário em execução por muito tempo.</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>Para mais informações, consulte a <a href="../building-journeys/journey-ui.md#calendar">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new Optimize node to target specific audiences or run A/B tests to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to test and vary, and customize communications, sequencing, and timing to best reach your customers.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/optimize.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Atividade de ação em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer é compatível com uma nova Atividade de ação genérica que permite configurar ações únicas e grupos de ação de entrada multiação, possibilitando uma configuração de ação simplificada na tela da jornada. Em especial, este novo recurso permite:</p>
<ul>
<li>Uma configuração de ação nativa simplificada na tela da jornada.</li>
<li>A capacidade de criar grupos de ação de entrada de várias ações.</li>
<li>A capacidade de adicionar otimização a qualquer ação de canal integrada.</li>
<li>A capacidade de adicionar opções de experimentação e multilíngues a qualquer ação.</li>
</ul>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Para mais informações, consulte a <a href="../building-journeys/journey-action.md">documentação detalhada</a></p>
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
<li>Para qualquer tamanho ou volume adicional, é possível adquirir um complemento de pacote de anexos. Para obter mais informações, entre em contato com o representante da Adobe.</li>
</ul>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para mais informações, consulte a <a href="../email/pdf-attachments.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

<!--
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
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Otimização em campanhas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora capacita você com as ferramentas para fornecer conteúdo personalizado e otimizado para seu público-alvo, permitindo que você execute experimentos de conteúdo, crie direcionamento baseado em regras e use combinações avançadas de ambos para maximizar a eficiência de suas campanhas e jornadas.</p>
<p>Com a otimização, você pode:</p>
<ul>
<li>Testar múltiplas variações de conteúdo para identificar as mensagens mais eficazes.</li>
<li>Fornecer conteúdo personalizado com base nos atributos dos usuários e dados contextuais.</li>
<li>Combine direcionamento e experimentação para estratégias avançadas.</li>
<li>Filtrar usuários que não correspondem aos critérios da variante.</li>
<li>Garantir mecanismos de fallback para manter o engajamento dos usuários.</li>
</ul>
<P>Quando a jornada ou campanha estiver ativa, os perfis serão avaliados em relação aos critérios definidos e, com base nos critérios de correspondência, serão entregues com a experiência ou o conteúdo apropriado.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Lançado anteriormente em 8 de agosto somente em campanhas do, essa capacidade agora também está disponível no jornada a partir de 22 de agosto.</p>
<p>Para mais informações, consulte a <a href="../campaigns/campaigns-message-optimization.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#Aug-25-8-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

* **Administração**

   * **Alertas de monitoramento de configuração de canal** - Agora você pode assinar para receber alertas do sistema por email ou na central de notificações da Journey Optimizer, caso <!--a channel configuration failure happens or if -->um registro DNS esteja ausente. [Leia mais](../reports/alerts.md#alert-dns-record-missing)

* **Assistente de IA**

   * **Geração de conteúdo em vários idiomas** - O conteúdo agora pode ser gerado em francês, espanhol, alemão, italiano, japonês, sueco, holandês e norueguês. [Leia mais](../content-management/generative-uc.md#languages)

     Data de disponibilidade: 25 de agosto


* **Campanhas**

   * **Controle de taxa em campanhas de saída** - Agora é possível habilitar o controle de taxa para campanhas de saída (email, SMS, notificações por push), permitindo que você evite a sobrecarga em sistemas downstream, como páginas de aterrissagem ou plataformas de atendimento ao cliente. [Leia mais](../campaigns/campaign-schedule.md#rate-control)

   * **Agendamento de campanha de ação**: os agendadores de campanha diários, semanais e mensais foram atualizados para fornecer controle mais detalhado sobre agendamentos recorrentes:

      * **Recorrência semanal**: agora é possível optar por repetir a campanha toda semana ou a cada duas semanas e selecionar o(s) dia(s) da semana em que ela deve ser executada.

      * **Recorrência mensal**: agora é possível optar por repetir a campanha todos os meses ou a cada dois meses e selecionar o dia do mês em que ela deve ser executada.

      * **Agendas diárias, semanais ou mensais**: é possível especificar se a agenda recorrente deve parar em uma data específica ou após um determinado número de ocorrências.

   * **Campanhas de ação transacional agendadas** - As campanhas de ação transacional agendadas agora estão disponíveis para enviar comunicações transacionais em lote e baseadas em público-alvo por canais de email, SMS e push.

* **Canal - Cartões de conteúdo**

   * **Modelos de layout de cartão de conteúdo** - O canal de cartão de conteúdo agora fornece layouts de mensagem OOTB que simplificarão sua experiência de criação. Esta versão inclui modelos de layout de Imagem pequena, Imagem grande e Somente imagem. [Leia mais](../content-card/design-content-card.md)

* **Canal - Push**

   * **Data de expiração da notificação por push** - Agora é possível especificar uma data de expiração para cada notificação por push, o que impede que mensagens sensíveis ao tempo (como promoções de Black Friday) sejam enviadas após uma determinada data, evitando assim a entrega de uma experiência ruim aos clientes.

* **Canal - SMS**

   * **Recusa difusa**: quando habilitada, a opção **Recusa difusa** detecta mensagens de entrada que se assemelham às palavras-chave de recusa definidas (por exemplo, &quot;CANCILAR&quot;) e envia automaticamente uma resposta de confirmação para verificar a intenção de cancelamento de assinatura do usuário. Se o usuário confirmar por meio do prompt definido, a subscrição será cancelada. [Leia mais](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >**Não participação difusa** só está disponível com Sinch e Infobip.

   * **Verificar Conexão de SMS** - Agora é possível testar e verificar facilmente suas credenciais de API de SMS no Adobe Journey Optimizer, enviando uma mensagem de exemplo para um dispositivo designado. [Leia mais](../sms/sms-configuration-sinch.md)

* **Configuração**

  &lt;!—* **Suporte a domínio dinâmico** - o Journey Optimizer agora oferece suporte à personalização completa/básica de URL para domínios predefinidos aceitos pelo Adobe. Esse recurso está disponível em Disponibilidade limitada para um conjunto de clientes. [Leia mais](../personalization/personalization-build-expressions.md#where)—Atualização em 21 de agosto: Aguardando eng. para confirmar quando implantado em prod.—>

   * **Suporte a atributos personalizados com URL de cancelar assinatura com um clique**: com o Journey Optimizer, se estiver gerenciando consentimento fora da Adobe, você poderá configurar um ponto de acesso externo personalizado definindo seu próprio link de cancelamento de inscrição com um clique na configuração do email. Quando os destinatários clicam no link de cancelar assinatura, o Journey Optimizer anexa alguns parâmetros específicos do perfil padrão ao evento de atualização de consentimento.

     Para personalizar ainda mais seu link de cancelamento de inscrição com um clique, agora é possível definir atributos personalizados que também serão anexados ao evento de consentimento. [Leia mais](../email/list-unsubscribe.md#custom-attributes)

* **Conjuntos de dados**

   * **Repositório de objetos do Experience Decisioning - Itens de oferta personalizados** - O conjunto de dados de exportação interno agora captura todos os atributos de oferta e o status do ciclo de vida, permitindo a personalização e os relatórios completos. [Leia mais](../data/export-datasets.md)

   * Verificação de versão introduzida por meio do campo `etag` para melhorar a consistência e rastrear alterações para oferecer itens com mais confiabilidade.

* **Decisão**

   * **Anexar fragmentos a itens de decisão** - O Journey Optimizer agora oferece a capacidade de anexar fragmentos a itens de decisão, que podem ser aproveitados em campanhas de experiência baseadas em código por meio de políticas de decisão. Esse recurso está disponível em Disponibilidade limitada para um conjunto de clientes. [Leia mais](../experience-decisioning/create-decision.md#fragments)

* **Jornadas**

   * **Operações em massa de jornada**: na lista de jornadas, agora é possível selecionar vários itens. Após a seleção, é possível pausar ou retomar até 10 jornadas por vez.

   * **Suporte a redirecionamento (302) em ações personalizadas**: as ações personalizadas agora podem processar redirecionamentos HTTP 302 por solicitação. Isso permite que as jornadas se integrem a APIs que redirecionam solicitações para URLs localizados ou específicos da região. Os redirecionamentos são seguidos automaticamente, garantindo que o conteúdo correto seja entregue sem configuração extra.

   * **Várias ações de entrada no jornada** - Para simplificar sua orquestração de jornadas, agora é possível definir várias ações de entrada em uma única jornada. Anteriormente disponível em campanhas, esse recurso permite que você forneça várias experiências baseadas em código, mensagens no aplicativo, Cartões de conteúdo ou ações da Web a locais diferentes ao mesmo tempo, cada ação contendo um conteúdo específico. [Leia mais](../building-journeys/journey-action.md#multi-action)

## Orquestração de campanha  

**Data de disponibilidade**: 4 de agosto de 2025

O Journey Optimizer agora inclui a **Orquestração de campanha**, um novo recurso criado especificamente para campanhas em lotes iniciadas pela marca. Esta versão apresenta uma tela de orquestração de campanhas e uma modelagem de dados aprimorada, que funcionam em conjunto para permitir que os profissionais de marketing planejem, direcionem e entreguem campanhas personalizadas entre canais.

>[!IMPORTANT]
>
>Para acessar a Orquestração de campanha, sua licença deve incluir o pacote **Journey Optimizer – Campanhas e jornadas** ou **Journey Optimizer – Campanhas**. Entre em contato com o representante da Adobe para confirmar sua licença e atualizá-la, se necessário.

![GIF da orquestração de campanhas](assets/do-not-localize/release.gif)

Inclui [Esquemas e conjuntos de dados relacionais](#oc-relational) e [Tela da campanha](#oc-canvas). Juntas, essas duas inovações proporcionam um novo padrão para orquestrar campanhas em lotes no Journey Optimizer. Os principais recursos estão listados abaixo.

### Principais recursos {#oc-capabilities}

* **Fluxos de trabalho em várias etapas**

  Crie campanhas sofisticadas em lotes em vários canais com a nova tela de orquestração de campanhas.

* **Públicos-alvo sob demanda**

  Segmente públicos-alvo sob demanda para ativação imediata.

* **Segmentação de várias entidades**

  Crie públicos-alvo com base no contexto comercial (dimensões que não sejam de pessoas), como produtos, lojas, renovações, reservas e muito mais.

* **Visibilidade pré-envio**

  Revise, refine e otimize públicos-alvo e campanhas antes do lançamento e enquanto as campanhas estão em execução

### Tela da campanha {#oc-canvas}

Uma interface de orquestração visual totalmente nova, criada especificamente para campanhas em lotes. Essa tela permite:

* Planejamento visual de fluxos de campanha em várias etapas e vários canais

* Compatibilidade com públicos-alvo sob demanda criados a partir de consultas relacionais

* Divisão avançada de públicos-alvo, esperas e lógica condicional

* Contagens precisas pré-envio após a aplicação de regras de negócios e filtros

### Esquemas e conjuntos de dados relacionais {#oc-relational}

O Adobe Journey Optimizer agora permite entidades relacionais (por exemplo: produtos, lojas, reservas, contratos) vinculadas a perfis com base em pessoas. Isso permite a segmentação e a personalização em estruturas de dados multidimensionais, permitindo casos de uso como:

* Uma mensagem por reserva, assinatura ou contrato

* Segmentação baseada em atributos da entidade relacionada (por exemplo, categoria do produto ou localização da loja)

* Capacidade de endereçamento aprimorada (por exemplo, enviar a todos os contatos conhecidos vinculados a uma entidade)

### Por que isso importa

Esta versão concede aos profissionais de marketing controle total sobre o marketing em lotes com base em públicos-alvo e iniciado pela marca, combinando uma modelagem de dados flexível com uma experiência de orquestração. Ela foi projetada especificamente para orquestração de campanhas em lotes para jornadas em tempo real, oferecendo personalização e capacidade de redimensionado avançadas.

### Saiba mais

Saiba mais na [documentação da orquestração de campanhas](../orchestrated/gs-orchestrated-campaigns.md).


