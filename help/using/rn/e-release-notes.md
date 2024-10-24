---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 92ecd1261e6c734743c4ab5173969da6e54cd15a
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 37%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de outubro de 2024 {#e-2024}

**Data de lançamento**: 29 a 30 de outubro de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
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
<p>Anteriormente disponível para um conjunto de organizações (DL), as políticas de aprovação agora estão disponíveis para todos os usuários (DG).</p>
<p>Para obter mais informações, consulte a <a href="../test-approve/gs-approval.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personalização da configuração de email (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode definir subdomínios dinâmicos e parâmetros de cabeçalho personalizados ao criar configurações de canais de email, para aumentar a flexibilidade e o controle sobre suas configurações de email.</p><p>Usar uma configuração personalizada em uma campanha ou jornada permite que você visualize seu conteúdo de email para verificar possíveis erros com as configurações dinâmicas definidas.</p>
<p>Anteriormente disponível para um conjunto de organizações (DL), a personalização da configuração de email agora está disponível para todos os usuários (GA).</p>
<p>Para obter mais informações, consulte a <a href="../email/surface-personalization.md">documentação detalhada</a>.</p>
</td>
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
<p>O Jornada otimizer agora permite testar diferentes variantes do conteúdo de email visualizando-o e enviando provas usando dados de entrada de amostra carregados de um arquivo CSV ou adicionados manualmente. Todos os atributos de perfis usados em seu conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados para seus testes criarem várias variantes.</p>
<p>No momento, esse recurso está disponível como um beta.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
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
<p>No Journey Optimizer, gerenciar o volume e o tempo das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. O Journey Optimizer agora oferece várias ferramentas para o gerenciamento de conflitos e a priorização.</p><p><ul><li><b>Limite de frequência de Jornada</b>: agora é possível criar conjuntos de regras para serem aplicados às suas jornadas, permitindo limitar o número de jornadas de um perfil por dia, semana ou mês, bem como controlar o número de jornadas simultâneas executadas simultaneamente.</li>
<li><b>Pontuação de prioridade</b>: agora é possível atribuir uma pontuação de prioridade a uma campanha ou jornada, variando de 0 a 100. Um número mais alto indica uma prioridade mais alta. Quando duas campanhas ou ações de jornada usam a mesma configuração de canal, o Journey Optimizer seleciona aquela com a pontuação de prioridade mais alta. Se as campanhas tiverem a mesma pontuação, a campanha que foi modificada menos recentemente será escolhida.</li>
<li><b>Exibir conflitos potenciais</b>: um novo botão "Exibir conflitos potenciais" nas jornadas e campanhas agora permite identificar sobreposições com outras jornadas ou campanhas, como a data de início, o público-alvo ou a configuração de canal selecionada.</li>
<li><b>Arbitragem de Jornada</b>: esse novo recurso permite que você priorize as jornadas mais importantes para seus clientes. É possível criar uma regra para suprimir a entrada em uma jornada de prioridade mais baixa quando um cliente se qualifica para uma jornada futura de prioridade mais alta.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Os recursos de gerenciamento de conflitos e prioridades estão disponíveis em Disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão gradualmente lançados para mais usuários no futuro. Entre em contato com a equipe de conta, se estiver interessado em ser adicionado à lista de espera para esses recursos.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modo de edição não visual para o web designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como alternativa ao web designer do Journey Optimizer, agora é possível adicionar modificações ao seu site usando um editor não visual. Ela permite inserir as alterações manualmente sem abrir as páginas no editor visual.
Esse modo de edição não visual é útil se você não puder instalar extensões de navegador, como o Adobe Experience Cloud Visual Helper, que é necessário para carregar suas páginas no web designer.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>Anteriormente disponível para um conjunto de organizações (DL), os experimentos em jornadas agora estão disponíveis para todos os usuários (DG).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Decisioning (Disponibilidade Geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Decisioning, anteriormente disponível para um conjunto de organizações (DL) e conhecido como Experience Decisioning, agora está disponível para todos os usuários (GA). Ele simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como "itens de decisão" e um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada indivíduo. Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada por meio do canal de experiência baseado em código.</p>

<p>Por enquanto, o Decisioning está indisponível para clientes que compraram as ofertas complementares do Adobe Healthcare Shield e do Privacy and Security Shield.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Conjuntos de regras (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar regras granulares de limite de frequência e aplicá-las às suas mensagens ou jornadas por meio de conjuntos de regras. Esse novo recurso permite controlar a frequência com que seus públicos-alvo recebem uma mensagem definindo regras entre canais que excluem automaticamente perfis excessivamente solicitados de mensagens e ações.</p><p>Também permite limitar o número de jornadas por dia, semana ou mês, bem como controlar o número de jornadas simultâneas executadas simultaneamente.</p>
<p>Os conjuntos de regras estão disponíveis em Disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão gradualmente lançados para mais usuários no futuro. Entre em contato com a equipe de conta, se estiver interessado em ser adicionado à lista de espera para esse recurso.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


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
<p>Com a disponibilidade geral, o conteúdo multilíngue agora pode ser acessado em todos os canais. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>Acelere os fluxos de trabalho do profissional para clientes do Journey Optimizer que usam Da Vinci para criação e o AJO para otimização e entrega</li>
<li>Otimizar modelos Da Vinci com dados de Adobe.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
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
<p>Disponível desde 16 de outubro de 2024</p>
<p>Os relatórios do Journey Optimizer agora estão disponíveis no mercado (GA) e vêm com uma interoperabilidade melhorada com recursos Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.</p>
<p>Com a disponibilidade geral, quatro novos recursos são introduzidos: a capacidade de criar métricas simples, criar e publicar públicos, fazer perguntas ad hoc usando o Insight Builder e agendar relatórios para serem enviados automaticamente por email aos principais destinatários.</p>
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: a experiência atual de relatórios será removida a partir de janeiro de 2025. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição suave. <a href="../reports/report-gs-cja.md">Saiba como começar a usar a nova interface de relatórios do Journey Optimizer</a></p>
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
<p>Disponível desde 1 de outubro de 2024</p>
<p>Com o novo canal de experiência com base em código, o Adobe Journey Optimizer permite realizar personalização e testes avançados para qualquer uma de suas propriedades de entrada. Isso possibilita a entrega perfeita de experiências personalizadas em diversos pontos de contato, como aplicativos Web, aplicativos móveis, aplicativos para desktop, consoles de vídeo, dispositivos conectados à TV, smart TVs, quiosques, caixas eletrônicos, dispositivos IoT, entre outros. O canal de experiência com base em código agora está disponível na tela da jornada.</p>
<p>Para obter mais informações, consulte a <a href="../code-based/create-code-based.md">documentação detalhada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
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
<p>Disponível desde 1 de outubro de 2024</p>
<p>Com o canal da Web, o Adobe Journey Optimizer permite personalizar a experiência da Web fornecida aos clientes por meio de jornadas da Web de entrada. O canal da Web agora está disponível na tela da jornada.</p>
<p>Para obter mais informações, consulte a <a href="../web/create-web.md">documentação detalhada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Canal SMS**

Foram introduzidos aprimoramentos de SMS para melhorar os recursos de mensagens:

* Você pode definir e gerenciar palavras-chave exclusivas para suas campanhas e jornadas de SMS, permitindo uma comunicação mais personalizada e eficiente.

* Você pode criar e enviar uma mensagem SMS padrão quando uma palavra-chave não é reconhecida.

* Agora é possível editar ou excluir uma Configuração de canal de API de SMS.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Número máximo de jornadas ativas** - O Journey Optimizer agora tem uma garantia de 500 jornadas ativas em sandboxes de produção, em vez de 100. O número de jornadas ativas é visível na tela de jornada. <!-- DOCAC-10977-->

**Conjuntos de dados**

* **Grade de proteção de tempo de vida** - A partir de 1º de novembro de 2024, uma grade de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema da Journey Optimizer em novas sandboxes e novas organizações da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada em sandboxes de clientes existentes posteriormente em uma segunda fase.

  Além disso, a partir de 1º de novembro, a segmentação por transmissão não oferecerá mais suporte ao uso de eventos de envio e abertos a partir de conjuntos de dados de rastreamento e feedback. Essa alteração se aplicará a todas as sandboxes e organizações do cliente nesse momento. [Saiba mais](../data/datasets-ttl.md)

* **Parâmetros em ações personalizadas** (Data de disponibilidade: 3 de outubro de 2024) - agora há suporte para parâmetros NULL e opcionais em ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Relatórios**

* **Os relatórios do Experience Decisioning** agora estão disponíveis, oferecendo insights essenciais sobre como os visitantes interagem com suas experiências.

**Políticas de governança de dados e consentimento** - Data de disponibilidade: 7 de outubro de 2024

* A aplicação das **políticas de governança de dados** agora ocorre em todos os canais do Journey Optimizer. Para clientes que criaram políticas na Adobe Experience Platform, elas são aplicadas a ações de marketing como parte da definição das configurações de canal. Ao criar conteúdo usando uma configuração, o sistema verifica todos os campos de personalização para verificar se há violações de governança de dados. Se uma violação for encontrada, não será possível publicar uma jornada ou campanha. [Saiba mais](../action/action-privacy.md)

* **As políticas de consentimento personalizadas** agora se aplicam a todos os canais do Journey Optimizer. Na aplicação, antes de uma mensagem ser enviada ou uma experiência de entrada ser entregue, o sistema verifica se o usuário deu consentimento para usar campos de personalização no conteúdo que receberá. Se nenhum consentimento for dado, a experiência não será exibida. [Saiba mais](../action/consent.md)

  >[!NOTE]
  >
  >Atualmente, as políticas de consentimento estão disponíveis apenas para as organizações que compraram as ofertas complementares do Adobe **Healthcare Shield** ou do **Privacy and Security Shield** .

**Públicos-alvo** - Data de disponibilidade: 8 de outubro de 2024

* Ao direcionar um público-alvo de arquivo CSV, agora é possível usar atributos do arquivo no editor de personalização e no construtor de regras de jornadas e campanhas. [Saiba mais](../audience/about-audiences.md)

* O uso de públicos-alvo e de atributos dos uploads personalizados (arquivos CSV) está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield.

**Canal baseado em código**

* Os templates de conteúdo agora estão disponíveis. Você pode acelerar a criação de suas experiências baseadas em código, começando por um modelo de conteúdo criado por seus desenvolvedores. Usar um modelo de conteúdo permitirá que o profissional de marketing modifique apenas alguns valores ou campos, em vez de compor toda a carga de conteúdo HTML ou JSON.

**Decisão**

Os usuários do [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR) agora podem escolher modelos personalizados para otimizar ao configurar um modelo de IA no Decisioning (anteriormente conhecido como Experience Decisioning). Isso permite, por exemplo, otimizar em uma tabela de &quot;compras&quot; personalizada em vez de restrições definidas, como a taxa de cliques.&quot;
