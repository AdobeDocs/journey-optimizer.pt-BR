---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 97b6041d4b8523b11b13dd78cd8b241a6410f1bc
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 78%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

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
<p>Disponível desde 1º de outubro de 2024</p>
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
<p>Disponível desde 1º de outubro de 2024</p>
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
<p>No Journey Optimizer, gerenciar o volume e o tempo das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. O Journey Optimizer agora oferece várias ferramentas para gerenciamento de conflitos e priorização. <p>Para obter mais informações, consulte a <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentação detalhada</a>.</p></p><p><ul><li><b>Limite de frequência de jornada</b>: agora é possível criar conjuntos de regras para aplicar às suas jornadas, permitindo limitar o número de jornadas de um perfil por dia, semana ou mês, bem como controlar o número de jornadas simultâneas.</li>
<li><b>Pontuação de prioridade</b>: agora é possível atribuir uma pontuação de prioridade a uma campanha ou jornada, variando de 0 a 100. Um número maior indica uma prioridade mais alta. Quando duas campanhas ou ações de jornada usam a mesma configuração de canais, o Journey Optimizer seleciona aquela com a maior pontuação de prioridade. Se as campanhas tiverem a mesma pontuação, a campanha modificada menos recentemente será escolhida.</li>
<li><b>Exibir conflitos potenciais</b>: um novo botão “Exibir conflitos potenciais” agora permite identificar configurações conflitantes com outras jornadas ou campanhas, como a data inicial, o público-alvo ou a configuração de canais selecionada.</li>
<li><b>Arbitragem de jornada</b>: esse novo recurso permite priorizar as jornadas mais importantes para seus clientes. É possível criar uma regra para suprimir a entrada em uma jornada de menor prioridade quando um cliente se qualifica para uma jornada futura de maior prioridade.</li>
<li><b>Limite de frequência por tipo de comunicação: </b>ao utilizar conjuntos de regras, agora é possível definir regras granulares por tipo de comunicação (por exemplo, Vendas, Promocional) para evitar sobrecarregar os clientes com mensagens semelhantes. Você pode controlar a frequência de vários canais, excluindo automaticamente perfis solicitados em excesso para garantir uma melhor experiência do cliente.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>Os recursos de gerenciamento de conflitos e prioridades estão em disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão lançados de forma gradual para mais usuários no futuro. Entre em contato com a equipe de conta se tiver interesse em participar da lista de espera desses recursos.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Integração do Movable Ink com o Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível integrar o Movable Ink Da Vinci com o Adobe Journey Optimizer. Essa nova integração permite: </p>
<p><ul><li>Aproveitar os recursos avançados do produto Movable Ink Da Vinci para reunir e personalizar variações de email para campanhas em lote</li>
<li>Acelere os fluxos de trabalho do profissional para clientes do Journey Optimizer que usam Da Vinci para criação e o Adobe Journey Optimizer para otimização e entrega</li>
<li>Otimizar modelos do Da Vinci com dados da Adobe.</li></ul></p>
<p>Para obter mais informações, consulte a <a href="https://movableink.com/adobe-and-movable-ink">documentação do Movable Ink Da Vinci</a>.</p>
</tr>
</tbody>
</table>

Anteriormente disponíveis para um conjunto de organizações (DL), os seguintes recursos agora estão disponíveis para todos os usuários (DG):

<table>
<thead>
<tr>
<th><strong>Personalização da configuração de email (disponibilidade geral) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para obter mais flexibilidade e controle sobre as configurações de email, defina subdomínios dinâmicos e parâmetros de cabeçalho personalizados ao criar configurações de canal de email.
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
<p>Com as políticas de aprovação, agora é possível definir um processo de aprovação no Journey Optimizer para que as equipes de marketing garantam que as campanhas e jornadas sejam revisadas e aprovadas pelas partes interessadas apropriadas antes de serem publicadas.</p>
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
<th><strong>Experimentação de conteúdo em jornadas (disponibilidade geral)</strong><br/></th>
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


<table>
<thead>
<tr>
<th><strong>Decisão (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O serviço de Decisão, anteriormente disponível para apenas algumas organizações (disponibilidade limitada) e conhecido como Escolha de experiências, agora está disponível a todos os usuários (disponibilidade geral), incluindo organizações que compraram as ofertas complementares do Adobe Healthcare Shield ou do Privacy and Security Shield.</p><p>O serviço de Decisão simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de escolha sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa. Esses itens de decisão são perfeitamente integrados a uma grande variedade de superfícies de entrada por meio do canal de experiência baseado em código.</p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/gs-experience-decisioning.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mensagens multilíngues em jornadas e campanhas (disponibilidade limitada)</strong><br/></th>
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
<th><strong>Experiência de relatórios atualizada (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os relatórios do Journey Optimizer agora estão disponíveis para o público em geral e possuem uma interoperabilidade aprimorada com os recursos do Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e a confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.</p>
<p>Com a Disponibilidade geral, quatro novos recursos são introduzidos: a capacidade de criar métricas simples, criar e publicar públicos-alvo, fazer perguntas ad hoc usando o Insight Builder e agendar relatórios para serem enviados automaticamente por email aos principais destinatários.</p>
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: a experiência atual de relatórios será removida a partir de janeiro de 2025. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição tranquila. <a href="../reports/report-gs-cja.md">Saiba como começar a usar a nova interface de relatórios do Journey Optimizer</a></p>
<p>Disponível desde 16 de outubro de 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Teste seu conteúdo usando exemplos de dados de entrada (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O otimizador de Jornada agora permite testar diferentes variantes do conteúdo, visualizando-o e enviando provas de email usando dados de entrada de amostra carregados de um arquivo ou adicionados manualmente. Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.</p>
<p>No momento, esse recurso está disponível para todos os clientes como um beta público para os canais de email, SMS e notificação por push.</p>
<p>Para obter mais informações, consulte a <a href="../test-approve/simulate-sample-input.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Usar dados do Adobe Experience Platform para personalização (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveite os dados do Adobe Experience Platform no editor de personalização para personalizar seu conteúdo. Para fazer isso, os conjuntos de dados necessários para a personalização da pesquisa devem primeiro ser habilitados por meio de uma chamada de API. Depois de concluído, você poderá usar os dados para personalizar o conteúdo no [!DNL Journey Optimizer].</p>
<p>Esse recurso está atualmente disponível para todos os clientes como uma versão beta pública.</p>
<p>Para obter mais informações, consulte a <a href="../personalization/lookup-aep-data.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#24-10-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Canal SMS**

* Agora é possível editar ou excluir uma Configuração de canal de API de SMS. [Saiba mais](../sms/sms-configuration.md)

* As seguintes melhorias foram introduzidas para melhorar os recursos de mensagens SMS com o Infobip e o Sinch:

   * Você pode definir e gerenciar palavras-chave exclusivas para suas campanhas e jornadas de SMS, permitindo uma comunicação mais personalizada e eficiente.

   * Você pode criar e enviar uma mensagem SMS padrão quando uma palavra-chave não for reconhecida.

  Saiba mais sobre essas melhorias na documentação de configuração de SMS do [Infobip](../sms/sms-configuration-infobip.md) e do [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Canal da Web**

* **Modo de edição não visual do web designer** - Como alternativa ao web designer do Journey Optimizer, agora é possível adicionar modificações ao seu site usando um editor não visual. Ela permite inserir as alterações manualmente sem abrir as páginas no editor visual. Esse modo de edição não visual é útil se você não puder instalar extensões de navegador, como o Adobe Experience Cloud Visual Helper, que é necessário para carregar suas páginas no web designer. [Saiba mais](../web/web-non-visual-editor.md)


**Conjuntos de dados**

* **Eventos de envio e abertura**: a partir de 1º de novembro de 2024, a segmentação de transmissão não será mais compatível com o uso de eventos de envio e abertura de conjuntos de dados de rastreamento e feedback do Journey Optimizer. Essa alteração se aplicará a todas as sandboxes e organizações do cliente. [Saiba mais](../data/datasets-ttl.md#segmentation-update)

* **Tempo de vida (TTL) do conjunto de dados**: a partir de fevereiro de 2025, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer em novas sandboxes e organizações da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada nas sandboxes de clientes existentes em uma fase futura. [Saiba mais](../data/datasets-ttl.md#ttl)

* **Parâmetros em ações personalizadas** - Data de disponibilidade: 3 de outubro de 2024 - Agora há suporte para parâmetros NULL e opcionais em ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Relatórios**

* **Relatórios de decisão** já está disponível, oferecendo insights essenciais sobre como os visitantes interagem com suas experiências. [Saiba mais](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Políticas de governança de dados e consentimento** - Data de disponibilidade: 7 de outubro de 2024

* A aplicação das **políticas de governança de dados** agora ocorre em todos os canais do Journey Optimizer. Para clientes que criaram políticas no Adobe Experience Platform, elas são aplicadas a ações de marketing como parte da configuração das configurações de canal. Ao criar conteúdo usando uma configuração, o sistema verifica todos os campos de personalização para verificar se há violações de governança de dados. Se uma violação for encontrada, não será possível publicar uma jornada ou campanha. [Saiba mais](../action/action-privacy.md)

* **As políticas de consentimento personalizadas** agora se aplicam a todos os canais do Journey Optimizer. Na aplicação, antes de uma mensagem ser enviada ou uma experiência de entrada ser entregue, o sistema verifica se o usuário deu consentimento para usar campos de personalização no conteúdo que receberá. Se nenhum consentimento for dado, a experiência não será exibida. [Saiba mais](../action/consent.md)

  >[!NOTE]
  >
  >Atualmente, as políticas de consentimento estão disponíveis apenas para as organizações que compraram as ofertas complementares do Adobe **Healthcare Shield** ou do **Privacy and Security Shield** .

**Públicos-alvo** - Data de disponibilidade: 8 de outubro de 2024

* Ao direcionar um público-alvo de arquivo CSV, agora é possível usar atributos do arquivo no editor de personalização e no construtor de regras de jornadas e campanhas. [Saiba mais](../audience/about-audiences.md)

* O uso de públicos-alvo e de atributos dos uploads personalizados (arquivos CSV) está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Configuração** - Data de disponibilidade: 23 de outubro de 2024

* Ao usar uma configuração personalizada em uma campanha ou jornada, agora é possível visualizar o conteúdo de email para verificar possíveis erros nas configurações dinâmicas que você definiu. [Saiba mais](../email/surface-personalization.md#check-configuration)

**Canal baseado em código**

* Os modelos de conteúdo agora estão disponíveis. Você pode acelerar a criação de experiências baseadas em código começando com um modelo de conteúdo criado por seus desenvolvedores. Usar um modelo de conteúdo permitirá que o profissional de marketing modifique apenas alguns valores ou campos, em vez de compor toda a carga de conteúdo HTML ou JSON. [Saiba mais](../content-management/content-templates.md)

**Decisão**

* Os usuários do [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR) agora podem escolher modelos personalizados para otimizar a configuração de um modelo de IA utilizando o serviço de Decisão (anteriormente conhecido como Escolha de experiências). Isso permite, por exemplo, otimizar em uma tabela de &quot;compras&quot; personalizada em vez de restrições definidas, como a taxa de cliques. [Saiba mais](../experience-decisioning/ranking.md)

* Ao adicionar uma política de decisão a uma campanha baseada em código com o Decisioning, agora é possível selecionar manualmente itens de decisão únicos, além de estratégias de seleção. Também é possível selecionar mais de uma oferta substituta. Isso garante o retorno de um certo número de itens de decisão. [Saiba mais](../experience-decisioning/create-decision.md)
