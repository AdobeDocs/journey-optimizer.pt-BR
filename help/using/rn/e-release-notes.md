---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: b0901a86eaa1d9a0482caf689043a1029313f6c5
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 34%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).


## Notas de pré-lançamento de agosto de 2025 {#25-8-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**. Links, telas e documentação atualizada são publicados nas notas de versão, na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 19 de agosto de 2025


### Novos recursos {#Aug-25-8-features}

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
<p>Aproveite os dados da Adobe Experience Platform no editor de personalização para personalizar seu conteúdo. Para fazer isso, os conjuntos de dados necessários para a personalização da pesquisa devem primeiro ser habilitados por meio de uma chamada de API. Depois de concluído, você poderá usar os dados para personalizar o conteúdo no [!DNL Journey Optimizer].</p>
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
<p>O Journey Optimizer é compatível com uma nova atividade de Ação genérica que permite configurar ações únicas e ações de saída de vários canais, permitindo uma configuração de ação simplificada na tela de jornada. Com essa nova atividade, você também tem a capacidade de adicionar otimização de direcionamento, experimentos e variantes de idioma multilíngues a qualquer ação de canal integrada.</p>
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

* **Configuração**

   * **Suporte a domínio dinâmico** - O Journey Optimizer agora oferece suporte à personalização em URLs de rastreamento para domínios predefinidos listados no nível de configuração de canal.

   * **Os atributos personalizados são compatíveis com a URL de cancelamento de inscrição com um clique**. Com o Journey Optimizer, se você estiver gerenciando o consentimento fora do Adobe, poderá definir um ponto de extremidade personalizado externo definindo seu próprio link de cancelamento de inscrição com um clique na configuração do email. Quando os destinatários clicam no link de cancelamento de inscrição, o Journey Optimizer anexa alguns parâmetros específicos do perfil padrão ao evento de atualização de consentimento.

     Para personalizar ainda mais seu link de cancelamento de inscrição com um clique, agora é possível definir atributos personalizados que serão anexados ao evento de consentimento.

* **Jornadas**

   * **Jornada operações em massa** - Na lista de jornadas, agora é possível selecionar vários itens. Após a seleção, é possível pausar ou retomar até 10 jornadas por vez.
