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
source-git-commit: 61447b6400b65e29a9187790e74be47b09764c4a
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 98%

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
<p>Com as políticas de aprovação, agora é possível definir um processo de aprovação no Journey Optimizer para que as equipes de marketing garantam que as campanhas e jornadas sejam revisadas e aprovadas pelas partes interessadas apropriadas antes de serem publicadas.</p>
<p>Anteriormente disponíveis para apenas algumas organizações (disponibilidade limitada), as políticas de aprovação agora estão disponíveis a todos os usuários (disponibilidade geral).</p>
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
<p>Agora você pode definir subdomínios dinâmicos e parâmetros de cabeçalho personalizados ao criar configurações de canais de email para aumentar a flexibilidade e o controle sobre as configurações de email.</p><p>Usar uma configuração personalizada em uma campanha ou jornada permite visualizar o conteúdo do email para identificar possíveis erros das configurações dinâmicas que você definiu.</p>
<p>Anteriormente disponível para apenas algumas organizações (disponibilidade limitada), a personalização da configuração de email agora está disponível a todos os usuários (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../email/surface-personalization.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Teste seu conteúdo usando exemplos de dados de entrada (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite testar diferentes variantes do conteúdo de email, possibilitando visualizar o conteúdo e enviar provas com exemplos de dados de entrada carregados de um arquivo CSV ou adicionados manualmente. Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.</p>
<p>No momento, esse recurso está disponível em versão beta.</p>
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
<p>No Journey Optimizer, gerenciar o volume e o tempo das campanhas e jornadas é essencial para evitar sobrecarregar os clientes com muitas interações. O Journey Optimizer agora oferece várias ferramentas para gerenciamento de conflitos e priorização.</p><p><ul><li><b>Limite de frequência de jornada</b>: agora é possível criar conjuntos de regras para aplicar às suas jornadas, permitindo limitar o número de jornadas de um perfil por dia, semana ou mês, bem como controlar o número de jornadas simultâneas.</li>
<li><b>Pontuação de prioridade</b>: agora é possível atribuir uma pontuação de prioridade a uma campanha ou jornada, variando de 0 a 100. Um número maior indica uma prioridade mais alta. Quando duas campanhas ou ações de jornada usam a mesma configuração de canais, o Journey Optimizer seleciona aquela com a maior pontuação de prioridade. Se as campanhas tiverem a mesma pontuação, a campanha modificada menos recentemente será escolhida.</li>
<li><b>Exibir conflitos potenciais</b>: um novo botão “Exibir conflitos potenciais” agora permite identificar configurações conflitantes com outras jornadas ou campanhas, como a data inicial, o público-alvo ou a configuração de canais selecionada.</li>
<li><b>Arbitragem de jornada</b>: esse novo recurso permite priorizar as jornadas mais importantes para seus clientes. É possível criar uma regra para suprimir a entrada em uma jornada de menor prioridade quando um cliente se qualifica para uma jornada futura de maior prioridade.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Os recursos de gerenciamento de conflitos e prioridades estão em disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão lançados de forma gradual para mais usuários no futuro. Entre em contato com a equipe de conta se tiver interesse em participar da lista de espera desses recursos.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modo de edição não visual para o designer na web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Como alternativa à versão web do designer do Journey Optimizer, agora é possível adicionar modificações ao seu site usando um editor não visual. Ele permite inserir as alterações manualmente sem abrir as páginas no editor visual.
Esse modo de edição não visual é útil se você não puder instalar extensões de navegador, como o Adobe Experience Cloud Visual Helper, que é necessário para carregar páginas na versão web do designer.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>Anteriormente disponíveis para apenas algumas organizações (disponibilidade limitada), os experimentos em jornadas agora estão disponíveis para todos os usuários (disponibilidade geral).</p>
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
<p>O serviço de Decisão, anteriormente disponível para apenas algumas organizações (disponibilidade limitada) e conhecido como Escolha de experiências, agora está disponível a todos os usuários (disponibilidade geral). Ele simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de escolha sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa. Esses itens de decisão são perfeitamente integrados a uma grande variedade de superfícies de entrada por meio do canal de experiência baseado em código.</p>

<p>Por enquanto, o serviço de Decisão não está disponível para clientes que compraram as ofertas complementares Adobe Healthcare Shield e Privacy and Security Shield.</p>

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
<p>Agora é possível criar regras granulares de limite de frequência e aplicá-las às suas mensagens ou jornadas por meio de conjuntos de regras. Esse novo recurso permite controlar a frequência com que seus públicos-alvo recebem uma mensagem definindo regras entre canais que excluem automaticamente perfis excessivamente solicitados de mensagens e ações.</p><p>Também é possível limitar o número de jornadas por dia, semana ou mês, bem como controlar o número de jornadas executadas simultaneamente.</p>
<p>Os conjuntos de regras estão em disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão lançados de forma gradual para mais usuários no futuro. Entre em contato com a equipe de conta se tiver interesse em participar da lista de espera desse recurso.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<p>Com a disponibilidade geral, o conteúdo multilíngue agora pode ser acessado em todos os canais. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>Acelerar os fluxos de trabalho profissionais de clientes do Journey Optimizer que usam o Da Vinci para criação e o AJO para otimização e entrega</li>
<li>Otimizar modelos do Da Vinci com dados da Adobe.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
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
<p>Disponível desde 16 de outubro de 2024</p>
<p>Os relatórios do Journey Optimizer agora estão disponíveis para o público em geral e possuem uma interoperabilidade aprimorada com os recursos do Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e a confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.</p>
<p>Com a disponibilidade geral, quatro novos recursos foram introduzidos: a capacidade de criar métricas simples, criar e publicar públicos-alvo, fazer perguntas ad-hoc usando o Insight Builder e agendar relatórios para envio automático por email aos principais destinatários.</p>
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: a experiência atual de relatórios será descontinuada a partir de janeiro de 2025. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição tranquila. <a href="../reports/report-gs-cja.md">Saiba como começar a usar a nova interface de relatórios do Journey Optimizer</a></p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiências baseadas em código em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponível desde 1º de outubro de 2024</p>
<p>Com o novo canal de experiência com base em código, o Adobe Journey Optimizer permite realizar personalização e testes avançados para qualquer uma de suas propriedades de entrada. Isso possibilita a entrega perfeita de experiências personalizadas em diversos pontos de contato, como aplicativos Web, aplicativos móveis, aplicativos para desktop, consoles de vídeo, dispositivos conectados à TV, smart TVs, quiosques, caixas eletrônicos, dispositivos IoT, entre outros. O canal de experiência com base em código agora está disponível na tela da jornada.</p>
<p>Para obter mais informações, consulte a <a href="../code-based/create-code-based.md">documentação detalhada</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experiências da web em jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Disponível desde 1º de outubro de 2024</p>
<p>Com o canal da Web, o Adobe Journey Optimizer permite personalizar a experiência da Web fornecida aos clientes por meio de jornadas da Web de entrada. O canal da Web agora está disponível na tela da jornada.</p>
<p>Para obter mais informações, consulte a <a href="../web/create-web.md">documentação detalhada</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Canal SMS**

>[!AVAILABILITY]
>
>Os aprimoramentos a seguir estão disponíveis apenas com provedores Sinch e Infobip.

Introduzimos aprimoramentos de SMS para melhorar os recursos de mensagens:

* Você pode definir e gerenciar palavras-chave exclusivas para suas campanhas e jornadas de SMS, permitindo uma comunicação mais personalizada e eficiente.

* Você pode criar e enviar uma mensagem SMS padrão quando uma palavra-chave não for reconhecida.

* Agora é possível editar ou excluir uma configuração de canais de API de SMS.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Conjuntos de dados**

* **Medidas de proteção de tempo de vida**: a partir de 1º de novembro de 2024, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer em novas sandboxes e novas organizações da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada em sandboxes de clientes existentes posteriormente em uma segunda fase.

  Além disso, a partir de 1º de novembro, a segmentação de transmissão não será mais compatível com o uso de eventos de envio e abertura de conjuntos de dados de rastreamento e feedback. Essa alteração se aplicará a todas as sandboxes e organizações de clientes. [Saiba mais](../data/datasets-ttl.md)

* **Parâmetros em ações personalizadas** (data de disponibilidade: 3 de outubro de 2024): parâmetros NULL e opcionais agora são permitidos em ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Relatórios**

* **Relatórios de decisão** já está disponível, oferecendo insights essenciais sobre como os visitantes interagem com suas experiências.

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

* Os modelos de conteúdo agora estão disponíveis. Você pode acelerar a criação de experiências baseadas em código começando com um modelo de conteúdo criado por seus desenvolvedores. Usar um modelo de conteúdo permitirá que profissionais de marketing modifiquem apenas alguns valores ou campos, em vez de compor todo o conteúdo HTML ou JSON.

**Decisão**

Os usuários do [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR) agora podem escolher modelos personalizados para otimizar a configuração de um modelo de IA utilizando o serviço de Decisão (anteriormente conhecido como Escolha de experiências). É possível, por exemplo, otimizar uma tabela de “compras” personalizada em vez de definir restrições, como a taxa de cliques.
