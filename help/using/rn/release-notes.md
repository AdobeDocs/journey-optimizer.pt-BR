---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 75c3db704853b8d2d8920ddd0086681d1fb02a93
workflow-type: tm+mt
source-wordcount: '1624'
ht-degree: 48%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/latest){target="_blank"}.


## Notas de pré-lançamento de agosto de 2025 {#25-8-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Anteriormente lançado com disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
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
<li>Melhorias de design para a navegação em datas,</li>
<li>A capacidade de ver campanhas de rascunho se você tiver definido uma data de início e término,</li>
<li>Uma nova configuração para ocultar e mostrar os itens do calendário em execução por muito tempo.</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
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

<table>
<thead>
<tr>
<th><strong>Usar dados da Adobe Experience Platform para personalização</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveite os dados do [!DNL Adobe Experience Platform] no editor de personalização para personalizar seu conteúdo e atributos de decisão. Especificamente, isso permite estender a definição dos atributos para dados adicionais nos conjuntos de dados para atualizações em massa que mudam periodicamente, sem precisar atualizar manualmente os atributos, um de cada vez.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Esta versão de disponibilidade geral também inclui os seguintes aprimoramentos:</p>
<ul>
<li>Suporte de canais de entrada,</li>
<li>A função auxiliar "datasetLookup" agora pode ser usada em fragmentos de expressão e visuais para personalizar o conteúdo usando dados de conjuntos de dados do Adobe Experience Platform,</li>
<li>Uma opção no conjunto de dados agora permite habilitar conjuntos de dados para personalização de pesquisa, sem precisar executar uma chamada de API.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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

<table>
<thead>
<tr>
<th><strong>Otimização do caminho de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora capacita você com as ferramentas para otimizar suas jornadas, aproveitando estruturas de IA e experimentação e garantindo, ao mesmo tempo, usabilidade e diferenciação perfeitas entre as funcionalidades de condição e otimização.</p>
<p>Use a otimização de caminho para direcionar, experimentar ou usar a IA para determinar a sequência de comunicações, o tempo entre eles, as combinações de canais e tudo o que você pode sonhar na tela de jornada.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atividade de ação em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer é compatível com uma nova atividade de Ação genérica que permite configurar grupos de ações únicas e de ações de entrada múltiplas, permitindo uma configuração de ação simplificada na tela de jornada. Em especial, este novo recurso permite:</p>
<ul>
<li>Uma configuração de ação nativa simplificada na tela de jornada.</li>
<li>A capacidade de criar nós de entrada de várias ações.</li>
<li>A capacidade de adicionar otimização a qualquer ação de canal integrada.</li>
<li>A capacidade de adicionar opções de experimentação e multilíngues a qualquer ação.</li>
</ul>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>O Journey Optimizer agora permite criar formulários personalizados e aproveitá-los em páginas de aterrissagem para capturar atributos de perfil no conjunto de dados definido para cada formulário.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Otimização em campanhas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora fornece as ferramentas necessárias para oferecer conteúdo personalizado e otimizado para o público-alvo das suas campanhas, permitindo que você execute experimentos de conteúdo, crie direcionamentos com base em regras e use combinações avançadas de ambos para maximizar a eficiência das suas campanhas.</p>
<p>Com a otimização, você pode:</p>
<ul>
<li>Testar múltiplas variações de conteúdo para identificar as mensagens mais eficazes.</li>
<li>Fornecer conteúdo personalizado com base nos atributos dos usuários e dados contextuais.</li>
<li>Combinar direcionamento e experimentação para estratégias de campanha avançadas.</li>
<li>Filtrar usuários que não correspondem aos critérios da variante.</li>
<li>Garantir mecanismos de fallback para manter o engajamento dos usuários.</li>
</ul>
<P>Quando a campanha estiver ativa, os perfis serão avaliados em relação aos critérios definidos e, com base nos critérios de correspondência, serão entregues com a experiência ou o conteúdo apropriado da campanha.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Data de lançamento: 8 de agosto de 2025</p>
<p>Para mais informações, consulte a <a href="../campaigns/campaigns-message-optimization.md">documentação detalhada</a></p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#Aug-25-8-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

* **Administração**

   * **Alertas de monitoramento de configuração de canal** - Agora você pode assinar para receber alertas do sistema, por email ou na central de notificações da Journey Optimizer, caso ocorra uma falha de configuração de canal ou se um registro DNS estiver ausente.

* **Campanhas**

   * **Controle de taxa em campanhas de saída** - Agora é possível habilitar o controle de taxa de limitação para campanhas de saída (email, SMS, notificações por push), permitindo que você evite a sobrecarga em sistemas downstream, como páginas de aterrissagem ou plataformas de atendimento ao cliente.

   * **Agendamento de campanha de ação** - Os agendadores diários, semanais e mensais da campanha foram atualizados para melhorar a granularidade. Por exemplo, agora você pode definir o número de semanas/meses entre programações, definir em qual dia executar e decidir parar após um número específico de ocorrências ou em uma data específica.

   * **Campanhas de ação transacional agendadas** - As campanhas de ação transacional agendadas agora estão disponíveis para enviar comunicações transacionais em lote e baseadas em público por canais de email, SMS e push.

* **Canal - Push**

   * **Data de expiração da notificação por push** - Agora é possível especificar uma data de expiração para cada notificação por push, o que impede que mensagens com detecção de hora (como vendas de Black Friday) sejam enviadas após uma determinada data, evitando assim a entrega de uma experiência ruim aos clientes.

* **Canal - Email**

   * **Anexos do PDF para emails** - Agora é possível anexar arquivos estáticos do PDF a mensagens de email enviadas com o Journey Optimizer.

* **Canal - SMS**

   * **Recusa difusa** - Quando habilitada, a opção **Recusa difusa** detecta mensagens de entrada que se assemelham muito às palavras-chave de recusa definidas (por exemplo, &#39;CANCIL&#39;) e envia automaticamente uma resposta de confirmação para verificar a intenção de cancelamento de inscrição do usuário. Se o usuário confirmar por meio do prompt definido, a subscrição será cancelada.

     Observe que a **Não participação difusa** só está disponível com o Sinch e o Infobip.

   * **Verificar Conexão de SMS** - Agora é possível testar e verificar facilmente suas credenciais de API de SMS no Adobe Journey Optimizer, enviando uma mensagem de exemplo para um dispositivo designado.

* **Configuração**

   * **Suporte a domínio dinâmico** - O Journey Optimizer agora oferece suporte à personalização em URLs de rastreamento para domínios predefinidos listados no nível de configuração de canal.

   * **Os atributos personalizados são compatíveis com a URL de cancelamento de inscrição com um clique**. Com o Journey Optimizer, se você estiver gerenciando o consentimento fora do Adobe, poderá definir um ponto de extremidade personalizado externo definindo seu próprio link de cancelamento de inscrição com um clique na configuração do email. Quando os destinatários clicam no link de cancelamento de inscrição, o Journey Optimizer anexa alguns parâmetros específicos do perfil padrão ao evento de atualização de consentimento.

     Para personalizar ainda mais seu link de cancelamento de inscrição com um clique, agora é possível definir atributos personalizados que serão anexados ao evento de consentimento.

* **Decisão**

   * **Anexar fragmentos a itens de decisão** - O Journey Optimizer agora oferece a capacidade de anexar fragmentos a itens de decisão, que podem ser aproveitados em campanhas de experiência baseadas em código por meio de políticas de decisão.

* **Jornadas**

   * **Jornada operações em massa** - Na lista de jornadas, agora é possível selecionar vários itens. Após a seleção, é possível pausar ou retomar até 10 jornadas por vez.

   * **Suporte a Redirecionamento (302) em Ações Personalizadas** - As ações personalizadas agora podem lidar com redirecionamentos HTTP 302 com base em solicitações. Isso permite que as jornadas se integrem a APIs que redirecionam solicitações para URLs localizados ou específicos da região. Os redirecionamentos são seguidos automaticamente, garantindo que o conteúdo correto seja entregue sem configuração extra.

## Orquestração de campanha  

**Data de disponibilidade**: 4 de agosto de 2025

O Journey Optimizer agora inclui a **Orquestração de campanha**, um novo recurso criado especificamente para campanhas em lotes iniciadas pela marca. Esta versão apresenta uma tela de orquestração de campanhas e uma modelagem de dados aprimorada, que funcionam em conjunto para permitir que os profissionais de marketing planejem, direcionem e entreguem campanhas personalizadas entre canais.

>[!IMPORTANT]
>
>Para acessar o Campaign Orchestration, sua licença deve incluir o pacote **Journey Optimizer - Campanhas e Jornadas** ou **Journey Optimizer - Campanhas**. Entre em contato com o representante da Adobe para confirmar sua licença e atualizar, se necessário.

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

O Adobe Journey Optimizer agora é compatível com entidades relacionais (por exemplo, produtos, lojas, reservas, contratos) vinculadas a perfis com base em pessoas. Isso permite a segmentação e a personalização em estruturas de dados multidimensionais, permitindo casos de uso como:

* Uma mensagem por reserva, assinatura ou contrato

* Segmentação baseada em atributos da entidade relacionada (por exemplo, categoria do produto ou localização da loja)

* Capacidade de endereçamento aprimorada (por exemplo, enviar a todos os contatos conhecidos vinculados a uma entidade)

### Por que isso importa

Esta versão concede aos profissionais de marketing controle total sobre o marketing em lotes com base em públicos-alvo e iniciado pela marca, combinando uma modelagem de dados flexível com uma experiência de orquestração. Ela foi projetada especificamente para orquestração de campanhas em lotes para jornadas em tempo real, oferecendo personalização e capacidade de redimensionado avançadas.

### Saiba mais

Saiba mais na [documentação da orquestração de campanhas](../orchestrated/gs-orchestrated-campaigns.md).


