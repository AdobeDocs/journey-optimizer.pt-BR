---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 92ea7f4093184b0ca3a2ddb9adde26fc7eebb3a3
workflow-type: tm+mt
source-wordcount: '2784'
ht-degree: 79%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Notas de versão anteriores a 25 de fevereiro {#25-02-rn}

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados na data de lançamento.

**Data de lançamento**: 18 a 19 de fevereiro de 2025


### Novos recursos {#25-02-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Criar e gerenciar regras de negócios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar regras de negócios usando conjuntos de regras. Os conjuntos de regras são grupos de regras que ajudam a limitar as mensagens enviadas em campanhas e ações de jornada entre canais, além de controlar as entradas de perfis nas jornadas.<p>
<p><ul><li>Crie conjuntos de regras de canal para restringir o número de mensagens enviadas por um ou vários canais. Aplique-as a campanhas ou ações de jornada para aplicar as regras definidas no conjunto de regras. O conjunto de regras de canal permite aplicar regras de limitação com base nos tipos de comunicação. Por exemplo, defina uma regra definida para limitar "mensagens promocionais" e outra para "boletins informativos". Aplique o conjunto de regras apropriado em sua ação de campanha ou jornada, dependendo do tipo de comunicação que você está enviando.</li>
<li> Crie conjuntos de regras de jornada para controlar entradas de perfil nas jornadas. Limite a frequência com que um perfil pode inserir uma jornada em um determinado período ou o número de jornadas nas quais um perfil pode ser inscrito simultaneamente. Aplique-as no nível da jornada para garantir o gerenciamento de entradas adequado.</li></p>
<p>Anteriormente disponível para um conjunto de organizações (DL), as regras de negócios agora estão disponíveis para todos os usuários (DG).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerar páginas de aterrissagem com o Assistente de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode criar conteúdo atraente para suas páginas de aterrissagem, incluindo designs de página inteira, texto personalizado e visuais personalizados, com a ajuda do assistente de IA.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<!--p>For more information on AI Assistant, refer to the <a href="../email/generative-lp.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Diretrizes da marca (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode definir suas próprias diretrizes de marca para definir a identidade visual e verbal da sua marca. Observe que o recurso Marcas é lançado como um beta privado para um conjunto limitado de clientes. Ele estará progressivamente disponível para todos os clientes em versões futuras.</p>
<!--p>For more information, refer to the <a href="../content-management/brands.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelos do Customer Journey Analytics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há a opção de aprimorar os relatórios do Journey Optimizer utilizando modelos do Customer Journey Analytics. Esse novo recurso permite simplificar o processo de geração de relatórios com modelos projetados previamente e personalizados para suas necessidades de análise.
</p>
<img src="assets/do-not-localize/cja-templates.gif">
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md#cja-template">documentação detalhada</a>.</p>
<p>Data de disponibilidade: a partir de 15 de janeiro de 2025</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avaliação de público-alvo flexível (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A avaliação flexível do público-alvo permite executar um trabalho de segmentação sob demanda para públicos-alvo selecionados, garantindo que você sempre tenha os dados do público-alvo mais atualizados antes de direcioná-los para jornadas e campanhas do Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obter mais informações, consulte a <a href="../audience/about-audiences.md#flexible">documentação detalhada</a>.</p>
<p> A avaliação flexível do público só está disponível para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.</p>
<p>Data de disponibilidade: 28 de janeiro de 2025</p>
</tr>
</tbody>
</table>
</table>


### Melhorias {#25-02-improvements}

As melhorias abaixo vêm com a atualização de fevereiro.

* **Jornadas** - Agora é possível testar suas ações personalizadas enviando chamadas de API da seção de administração. Esse novo recurso ajuda você a solucionar problemas de ações personalizadas antes ou depois de usá-las em uma jornada.

* **Tempo de vida (TTL) do conjunto de dados** - A partir deste mês, uma proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema da Journey Optimizer em novas sandboxes e novas organizações, da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada nas sandboxes de clientes existentes em uma fase subsequente.

  Saiba mais sobre esta atualização em [as perguntas frequentes dedicadas](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Correspondência direta** - Um novo tipo de servidor, Zona de aterrissagem de dados, agora é compatível com o roteamento de arquivos na configuração do canal de correspondência direta.

* **SMS** - Agora é possível gerenciar a entrega de mensagens SMS de pontos de extremidade multirregionais substituindo as URLs de entrega, feedback, entrada e retorno de chamada. Para oferecer suporte a isso, um novo campo Substituir URL foi adicionado à configuração Credenciais da API. Essa alteração está disponível somente com o provedor Sinch. [Leia mais](../sms/sms-configuration-sinch.md)

* **Personalization** (Data de disponibilidade: 29 de janeiro de 2025) - Novas funções auxiliares de data/hora estão disponíveis para uso no editor de personalização. [Leia mais](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuração de email** - Se você estiver gerenciando o consentimento fora do Adobe, agora é possível definir um endereço de email de cancelamento de inscrição personalizado e uma URL de cancelamento de inscrição personalizada com um clique como parte das configurações do canal de email. [Leia mais](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisão** (Data de disponibilidade: 28 de janeiro de 2025) - A decisão agora oferece suporte a tipos de dados de objeto ao editar o esquema do catálogo de itens. [Leia mais](../experience-decisioning/catalogs.md)


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
<li>Acelerar os fluxos de trabalho profissionais de clientes do Journey Optimizer que usam o Da Vinci para criação e o Adobe Journey Optimizer para otimização e entrega</li>
<li>Otimizar modelos do Da Vinci com dados da Adobe.</li></ul></p>
<p>Para obter mais informações, consulte a <a href="https://movableink.com/adobe-and-movable-ink">documentação do Movable Ink Da Vinci</a>.</p>
</tr>
</tbody>
</table>

Anteriormente disponíveis para um conjunto de organizações (LA), os seguintes recursos agora estão disponíveis a todos os usuários (GA):

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
<p>Com a disponibilidade geral, quatro novos recursos são introduzidos: a capacidade de criar métricas simples, criar e publicar públicos-alvo, fazer perguntas ad-hoc usando o Insight Builder e agendar relatórios para envio automático por email aos principais destinatários.</p>
<p>Para obter mais informações, consulte a <a href="../reports/report-cja-manage.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Importante: a experiência atual de relatórios será descontinuada a partir de janeiro de 2025. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição tranquila. <a href="../reports/report-gs-cja.md">Saiba como começar a usar a nova interface de relatórios do Journey Optimizer</a></p>
<p>Disponível desde 16 de outubro de 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Teste o conteúdo usando exemplos de dados de entrada (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite testar diferentes variantes do conteúdo, visualizando-o e enviando provas por email com exemplos de dados de entrada enviados de um arquivo ou adicionados manualmente. Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.</p>
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
<th><strong>Usar dados da Adobe Experience Platform para personalização (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveite os dados da Adobe Experience Platform no editor de personalização para personalizar seu conteúdo. Para fazer isso, os conjuntos de dados necessários para a personalização da pesquisa devem primeiro ser habilitados por meio de uma chamada de API. Depois de concluído, você poderá usar os dados para personalizar o conteúdo no [!DNL Journey Optimizer].</p>
<p>Esse recurso está atualmente disponível para todos os clientes como uma versão beta pública.</p>
<p>Para obter mais informações, consulte a <a href="../personalization/lookup-aep-data.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#24-10-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Canal SMS**

* Agora é possível editar ou excluir uma configuração de canais da API de SMS. [Saiba mais](../sms/sms-configuration.md)

* As seguintes melhorias foram introduzidas para melhorar os recursos de mensagens SMS com o Infobip e o Sinch:

   * Você pode definir e gerenciar palavras-chave exclusivas para suas campanhas e jornadas de SMS, permitindo uma comunicação mais personalizada e eficiente.

   * Você pode criar e enviar uma mensagem SMS padrão quando uma palavra-chave não for reconhecida.

  Saiba mais sobre essas melhorias na documentação da configuração de SMS do [Infobip](../sms/sms-configuration-infobip.md) e do [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Canal da Web**

* **Modo de edição não visual para a versão web do designer**: como alternativa à versão web do designer do Journey Optimizer, agora é possível adicionar modificações ao seu site usando um editor não visual. Ele permite inserir as alterações manualmente sem abrir as páginas no editor visual. Esse modo de edição não visual é útil se você não puder instalar extensões de navegador, como o Adobe Experience Cloud Visual Helper, que é necessário para carregar páginas na versão web do designer. [Saiba mais](../web/web-non-visual-editor.md)


**Conjuntos de dados**

* **Eventos de envio e abertura**: a partir de 1º de novembro de 2024, a segmentação de transmissão não será mais compatível com o uso de eventos de envio e abertura de conjuntos de dados de rastreamento e feedback do Journey Optimizer. Essa alteração se aplicará a todas as sandboxes e organizações do cliente. [Saiba mais](../data/datasets-ttl.md#segmentation-update)

* **Tempo de vida (TTL) do conjunto de dados**: a partir de fevereiro de 2025, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer em novas sandboxes e organizações da seguinte maneira:

   * 90 dias para dados na loja de perfis
   * 13 meses para dados no data lake

  Essa alteração será implementada nas sandboxes de clientes existentes em uma fase futura. [Saiba mais](../data/datasets-ttl.md#ttl)

* **Parâmetros em ações personalizadas**: data de disponibilidade: 3 de outubro de 2024: agora parâmetros NULL e opcionais são compatíveis com as ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Relatórios**

* Os **relatórios de decisões** agora estão disponíveis e oferecem insights essenciais sobre como os visitantes interagem com suas experiências. [Saiba mais](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Políticas de governança de dados e consentimento** - Data de disponibilidade: 7 de outubro de 2024

* A aplicação das **políticas de governança de dados** agora ocorre em todos os canais do Journey Optimizer. Para clientes que criaram políticas na Adobe Experience Platform, elas são aplicadas a ações de marketing como parte da definição das configurações de canal. Ao criar conteúdo usando uma configuração, o sistema verifica todos os campos de personalização para verificar se há violações de governança de dados. Se uma violação for encontrada, não será possível publicar uma jornada ou campanha. [Saiba mais](../action/action-privacy.md)

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

* Os modelos de conteúdo agora estão disponíveis. Você pode acelerar a criação de experiências baseadas em código começando com um modelo de conteúdo criado por seus desenvolvedores. Usar um modelo de conteúdo permitirá que profissionais de marketing modifiquem apenas alguns valores ou campos, em vez de compor todo o conteúdo HTML ou JSON. [Saiba mais](../content-management/content-templates.md)

**Decisão**

* Os usuários do [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR) agora podem escolher modelos personalizados para otimizar a configuração de um modelo de IA utilizando o serviço de Decisão (anteriormente conhecido como Escolha de experiências). É possível, por exemplo, otimizar uma tabela de “compras” personalizada em vez de definir restrições, como a taxa de cliques. [Saiba mais](../experience-decisioning/ranking.md)

* Ao adicionar uma política de decisão a uma campanha baseada em código com o serviço de Decisão, agora é possível selecionar manualmente itens de decisão individuais, além de estratégias de seleção. Também é possível selecionar mais de uma oferta substituta. Isso garante o retorno de um certo número de itens de decisão. [Saiba mais](../experience-decisioning/create-decision.md)
