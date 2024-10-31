---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7f7edaa8d3bb917e7020bb79eb72f7807cf46622
workflow-type: tm+mt
source-wordcount: '1910'
ht-degree: 39%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nestas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Versão de outubro de 2024 {#24-10-rn}

**Data de lançamento**: 29 a 30 de outubro de 2024

### Novos recursos {#24-10-features}

Essa versão traz os novos recursos detalhados abaixo:

<table>
<thead>
<tr>
<th><strong>Bloqueio de conteúdo de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite bloquear o conteúdo em modelos de email, bloqueando todo o modelo ou estruturas e componentes específicos. Isso permite evitar edições ou exclusões não intencionais, dando a você maior controle sobre a personalização do modelo e melhorando a eficiência e a confiabilidade de suas campanhas de email.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-locking.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>Disponível desde 24 de outubro de 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiências com base em código em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o novo canal de experiência com base em código, o Adobe Journey Optimizer permite realizar personalização e testes avançados para qualquer uma de suas propriedades de entrada. Isso possibilita a entrega perfeita de experiências personalizadas em diversos pontos de contato, como aplicativos Web, aplicativos móveis, aplicativos para desktop, consoles de vídeo, dispositivos conectados à TV, smart TVs, quiosques, caixas eletrônicos, dispositivos IoT, entre outros. O canal de experiência com base em código agora está disponível na tela da jornada.</p>
<p>Para obter mais informações, consulte a <a href="../code-based/create-code-based.md">documentação detalhada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Disponível desde 1 de outubro de 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiências da Web em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o canal da Web, o Adobe Journey Optimizer permite personalizar a experiência da Web fornecida aos clientes por meio de jornadas da Web de entrada. O canal da Web agora está disponível na tela da jornada.</p>
<p>Para obter mais informações, consulte a <a href="../web/create-web.md">documentação detalhada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Disponível desde 1 de outubro de 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gerenciamento de conflitos e prioridades (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No Journey Optimizer, gerenciar o volume e o tempo das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. O Journey Optimizer agora oferece várias ferramentas para o gerenciamento de conflitos e a priorização. <p>Para obter mais informações, consulte a <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentação detalhada</a>.</p></p><p><ul><li><b>Limite de frequência de Jornada</b>: agora é possível criar conjuntos de regras para serem aplicados às suas jornadas, permitindo limitar o número de jornadas de um perfil por dia, semana ou mês, bem como controlar o número de jornadas simultâneas executadas simultaneamente.</li>
<li><b>Pontuação de prioridade</b>: agora é possível atribuir uma pontuação de prioridade a uma campanha ou jornada, variando de 0 a 100. Um número mais alto indica uma prioridade mais alta. Quando duas campanhas ou ações de jornada usam a mesma configuração de canal, o Journey Optimizer seleciona aquela com a pontuação de prioridade mais alta. Se as campanhas tiverem a mesma pontuação, a campanha que foi modificada menos recentemente será escolhida.</li>
<li><b>Exibir conflitos potenciais</b>: um novo botão "Exibir conflitos potenciais" nas jornadas e campanhas agora permite identificar sobreposições com outras jornadas ou campanhas, como a data de início, o público-alvo ou a configuração de canal selecionada.</li>
<li><b>Arbitragem de Jornada</b>: esse novo recurso permite que você priorize as jornadas mais importantes para seus clientes. É possível criar uma regra para suprimir a entrada em uma jornada de prioridade mais baixa quando um cliente se qualifica para uma jornada futura de prioridade mais alta.</li>
<li><b>Limite de frequência por tipo de comunicação: </b>Com conjuntos de regras, agora é possível definir regras granulares por tipo de comunicação (por exemplo, Vendas, Promocional) para evitar sobrecarga de clientes com mensagens semelhantes. Você pode controlar a frequência em vários canais, excluindo automaticamente perfis excessivamente solicitados para garantir uma melhor experiência do cliente.</li></ul>

<p>Os recursos de gerenciamento de conflitos e prioridades estão disponíveis em Disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão gradualmente lançados para mais usuários no futuro. Entre em contato com a equipe de conta, se estiver interessado em ser adicionado à lista de espera para esses recursos.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Integração de tinta móvel e Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível integrar o Movable Ink Da Vinci e o Adobe Journey Optimizer. Com essa nova integração, você pode: </p>
<p><ul><li>Aproveite os recursos avançados do produto Da Vinci da Movable Ink para reunir e personalizar variações de email para campanhas em lote</li>
<li>Acelere os fluxos de trabalho do profissional para clientes do Journey Optimizer que usam Da Vinci para criação e o Adobe Journey Optimizer para otimização e entrega</li>
<li>Otimizar modelos Da Vinci com dados de Adobe.</li></ul></p>
<p>Para obter mais informações, consulte a <a href="https://movableink.com/adobe-and-movable-ink">documentação do Movable Ink Da Vinci</a>.</p>
</tr>
</tbody>
</table>

Anteriormente disponíveis para um conjunto de organizações (DL), os seguintes recursos agora estão disponíveis para todos os usuários (DG):

<table>
<thead>
<tr>
<th><strong>Personalização da configuração de email (Disponibilidade geral) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para obter mais flexibilidade e controle sobre as configurações de email, você pode definir subdomínios dinâmicos e parâmetros de cabeçalho personalizados ao criar configurações de canal de email.
</p>
<p>Para obter mais informações, consulte a <a href="../email/surface-personalization.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Disponível desde 23 de outubro de 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Aprovações em jornadas e campanhas (Disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com as políticas de aprovação, agora é possível configurar um processo de aprovação no Journey Optimizer para que as equipes de marketing garantam que as campanhas e jornadas sejam revisadas e aprovadas pelas partes interessadas apropriadas antes de serem publicadas.</p>
<p>Para obter mais informações, consulte a <a href="../test-approve/gs-approval.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Disponível desde 22 de outubro de 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experimentação de conteúdo no jornada (Disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Já disponível em campanhas, o Adobe Journey Optimizer agora oferece suporte a experimentos em jornadas. Experimentos são ensaios aleatórios, o que, no contexto de testes online, significa que você expõe alguns usuários selecionados aleatoriamente a uma determinada variação de uma mensagem e outro conjunto de usuários selecionados aleatoriamente a outra variação ou tratamento. Após a exposição, é possível medir as métricas de resultado em que está interessado, como abertura de emails, assinaturas ou compras.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-experiment.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Mensagens multilíngues em jornadas e campanhas (Disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora ficou mais fácil criar conteúdo em vários idiomas em uma única campanha ou jornada. Com esse recurso, é possível alternar entre idiomas ao editar a campanha ou a jornada, simplificando todo o processo de edição e melhorando sua capacidade de gerenciar com eficiência o conteúdo multilíngue.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/multilingual-gs.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experiência de relatório atualizada (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os relatórios do Journey Optimizer agora estão disponíveis no mercado (GA) e vêm com uma interoperabilidade melhorada com recursos Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.</p>
<p>Com a Disponibilidade geral, quatro novos recursos são introduzidos: a capacidade de criar métricas simples, criar e publicar públicos-alvo, fazer perguntas ad hoc usando o Insight Builder e agendar relatórios para serem enviados automaticamente por email aos principais destinatários.</p>
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: a experiência atual de relatórios será removida a partir de janeiro de 2025. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição suave. <a href="../reports/report-gs-cja.md">Saiba como começar a usar a nova interface de relatórios do Journey Optimizer</a></p>
<p>Disponível desde 16 de outubro de 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Teste o conteúdo usando dados de entrada de exemplo (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O otimizador de Jornada agora permite testar diferentes variantes do conteúdo, visualizando-o e enviando provas usando dados de entrada de amostra carregados de um arquivo ou adicionados manualmente. Todos os atributos de perfis usados em seu conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados para seus testes criarem várias variantes.</p>
<p>No momento, esse recurso está disponível para todos os clientes como um beta público para os canais de email, SMS e notificação por push.</p>
<p>Para obter mais informações, consulte a <a href="../test-approve/simulate-sample-input.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:

<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Melhorias {#24-10-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Canal SMS**

* Agora é possível editar ou excluir uma Configuração de canal de API de SMS.

* As seguintes melhorias foram introduzidas para melhorar os recursos de mensagens SMS com o Infobip e o Sinch:

   * Você pode definir e gerenciar palavras-chave exclusivas para suas campanhas e jornadas de SMS, permitindo uma comunicação mais personalizada e eficiente.

   * Você pode criar e enviar uma mensagem SMS padrão quando uma palavra-chave não é reconhecida.

  Saiba mais sobre essas melhorias na documentação de configuração de SMS do [Infobip](../sms/sms-configuration-infobip.md) e do [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Número máximo de jornadas ativas** - O Journey Optimizer agora tem uma garantia de 500 jornadas ativas em sandboxes de produção, em vez de 100. O número de jornadas ativas é visível na tela de jornada. <!-- DOCAC-10977-->

**Canal da Web**

* **Modo de edição não visual do web designer** - Como alternativa ao web designer do Journey Optimizer, agora é possível adicionar modificações ao seu site usando um editor não visual. Ela permite inserir as alterações manualmente sem abrir as páginas no editor visual. Esse modo de edição não visual é útil se você não puder instalar extensões de navegador, como o Adobe Experience Cloud Visual Helper, que é necessário para carregar suas páginas no web designer. [Saiba mais](../web/web-non-visual-editor.md)


**Conjuntos de dados**

* **Enviar e abrir eventos** - A partir de 1º de novembro de 2024, a segmentação por transmissão não oferecerá mais suporte ao uso de eventos de envio e abertura de conjuntos de dados de rastreamento e feedback do Journey Optimizer. Essa alteração se aplicará a todas as sandboxes e organizações do cliente. [Saiba mais](../data/datasets-ttl.md#segmentation-update)

* **Tempo de vida (TTL) do conjunto de dados** - A partir de fevereiro de 2025, uma garantia de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema da Journey Optimizer em novas sandboxes e novas organizações, da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada nas sandboxes de clientes existentes em uma fase subsequente. [Saiba mais](../data/datasets-ttl.md#ttl)

* **Parâmetros em ações personalizadas** (Data de disponibilidade: 3 de outubro de 2024) - agora há suporte para parâmetros NULL e opcionais em ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Relatórios**

* **Os relatórios do Experience Decisioning** agora estão disponíveis, oferecendo insights essenciais sobre como os visitantes interagem com suas experiências. [Saiba mais](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Políticas de governança de dados e consentimento** - Data de disponibilidade: 7 de outubro de 2024

* A aplicação das **políticas de governança de dados** agora ocorre em todos os canais do Journey Optimizer. Para clientes que criaram políticas no Adobe Experience Platform, elas são aplicadas a ações de marketing como parte da configuração das configurações de canal. Ao criar conteúdo usando uma configuração, o sistema verifica todos os campos de personalização para verificar se há violações de governança de dados. Se uma violação for encontrada, não será possível publicar uma jornada ou campanha. [Saiba mais](../action/action-privacy.md)

* **As políticas de consentimento personalizadas** agora se aplicam a todos os canais do Journey Optimizer. Na aplicação, antes de uma mensagem ser enviada ou uma experiência de entrada ser entregue, o sistema verifica se o usuário deu consentimento para usar campos de personalização no conteúdo que receberá. Se nenhum consentimento for dado, a experiência não será exibida. [Saiba mais](../action/consent.md)

  >[!NOTE]
  >
  >Atualmente, as políticas de consentimento estão disponíveis apenas para as organizações que compraram as ofertas complementares do Adobe **Healthcare Shield** ou do **Privacy and Security Shield** .

**Públicos-alvo** - Data de disponibilidade: 8 de outubro de 2024

* Ao direcionar um público-alvo de arquivo CSV, agora é possível usar atributos do arquivo no editor de personalização e no construtor de regras de jornadas e campanhas. [Saiba mais](../audience/about-audiences.md)

* O uso de públicos-alvo e de atributos dos uploads personalizados (arquivos CSV) está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Configuração** - Data de disponibilidade: 23 de outubro de 2024

* Ao usar uma configuração personalizada em uma campanha ou jornada, agora é possível visualizar seu conteúdo de email para verificar possíveis erros com as configurações dinâmicas definidas. [Saiba mais](../email/surface-personalization.md#check-configuration)

**Canal baseado em código**

* Os templates de conteúdo agora estão disponíveis. Você pode acelerar a criação de suas experiências baseadas em código, começando por um modelo de conteúdo criado por seus desenvolvedores. Usar um modelo de conteúdo permitirá que o profissional de marketing modifique apenas alguns valores ou campos, em vez de compor toda a carga de conteúdo HTML ou JSON. [Saiba mais](../content-management/content-templates.md)

**Decisão**

<!--* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) users can now choose custom models to optimize on when setting up an AI model in Decisioning (formerly known as Experience Decisioning). This allows you, for example, to optimize on a custom "purchases" table rather than defined constraints such as clickthrough rate."-->

* Ao adicionar uma política de decisão a uma campanha baseada em código com o Experience Decisioning, agora é possível selecionar manualmente itens de decisão únicos, além de estratégias de seleção. Além disso, agora é possível selecionar mais de uma oferta substituta. Isso garante que haja um determinado número de itens de decisão retornados. [Saiba mais](../experience-decisioning/create-decision.md)
