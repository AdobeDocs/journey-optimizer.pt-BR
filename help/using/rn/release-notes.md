---
title: Notas de versão
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 09c285fb4481d00008627f31e3fdfbb516d63fd6
workflow-type: tm+mt
source-wordcount: '2416'
ht-degree: 98%

---

# Notas de versão {#release-notes}

Esta página lista todos os novos recursos e melhorias do [!DNL Journey Optimizer]. Também é possível consultar a página das [atualizações mais recentes da documentação](documentation-updates.md) para conhecer mais alterações.


## Versão de janeiro de 2022 {#january-2022-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Jornadas - otimize seu incremento de IP com condições de limite de perfis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ao configurar uma atividade de <strong>Condição</strong> em uma jornada, agora é possível definir um limite de perfis. Esse novo tipo de condição permite definir um número máximo de perfis para um caminho de jornada. Quando esse limite é atingido, os perfis que entram pegam um caminho alternativo. Isso permite incrementar o volume das suas entregas (incremento de IP). Por exemplo, você pode querer incrementar suas entregas em um domínio dividindo a execução: enviar 1000 mensagens no dia 1, 2000 no dia 2, etc.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/condition-activity.md#profile_cap">documentação detalhada</a> e o <a href="../building-journeys/ramp-up-deliveries-uc.md">caso de uso de exemplo</a> relacionado.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Jornadas - melhorias no segmento de leitura</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A opção <strong>Leitura incremental</strong> foi adicionada às atividades recorrentes de <strong>Ler segmento</strong>. Essa opção permite direcionar somente aos indivíduos que entraram no segmento desde a última execução da jornada. A primeira execução sempre direciona a todos os membros do segmento.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentação detalhada</a>.
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Os eventos de etapa do Journey Optimizer agora podem ser vinculados a outros conjuntos de dados no [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=pt-BR). O campo **profileID**, no esquema incorporado Journey Step Event, agora está definido como um campo de identidade. [Saiba mais](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* Ao atualizar uma oferta, oferta substituta, coleção de ofertas ou decisão de oferta que é mencionada direta ou indiretamente em uma mensagem publicada, as atualizações agora são refletidas automaticamente na mensagem correspondente, sem a necessidade de publicá-la novamente. [Saiba mais](../offers/offers-e2e.md#insert-decision-in-email)

* Ao simular quais ofertas serão entregues para um determinado perfil de teste, agora é possível modificar as configurações padrão da simulação e exibir o código correspondente às suas simulações que podem ser usadas para fins de solução de problemas. [Saiba mais](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administração**

* Agora, os administradores podem editar registros PTR com um subdomínio CNAME configurado. [Saiba mais](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personalização**

* **Adicionar aos favoritos** - para ajudar a melhorar a eficiência ao trabalhar com personalização, introduzimos o conceito de salvar favoritos. Adicionar atributos diferentes ao menu de favoritos fornece acesso rápido aos itens usados com mais frequência. [Saiba mais](../personalization/personalize.md#fav)

## Versão de novembro de 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>Delegação de subdomínio CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora é compatível com CNAMEs. Um registro CNAME ou Nome canônico é um registro que aponta para outro endereço de domínio em vez de um endereço IP. A delegação de subdomínio CNAME permite criar um subdomínio e usar CNAMEs para apontar para registros específicos da Adobe. Com essa configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS para configurar o ambiente para enviar, renderizar e rastrear emails.</p>
<p>Esse método é recomendado se as políticas de sua organização restringirem o método completo de delegação de subdomínio.</p>
<p>Saiba mais sobre a delegação de subdomínio CNAME na <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


## Versão de outubro de 2021 {#oct-2021-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Gerenciamento de decisões - Simulações de ofertas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível simular quais ofertas serão entregues a um perfil de teste para um determinado posicionamento na interface do Journey Optimizer. Isso permite validar facilmente a sua lógica de decisão, incluindo restrições de qualificação e algoritmos de classificação, antes de colocá-los em produção. Esse recurso permite que usuários técnicos e não técnicos testem rapidamente o Offer Decisioning e solucionem possíveis problemas.</p>
<p>Para obter mais informações, consulte a <a href="../offers/offer-activities/simulation.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerenciamento de decisões - Personalize as suas ofertas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível personalizar o conteúdo de suas ofertas usando atributos e segmentos de perfil da Adobe Experience Platform, usando o mesmo componente do editor de expressão encontrado na interface do Journey Optimizer. </p>
<p>Para obter mais informações, consulte a <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


Consulte também as [Notas de versão de outubro da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=pt-BR){target=&quot;_blank&quot;} para mais alterações.

### Melhorias

**Jornadas**

* **Editor de expressão** - Como um usuário avançado, agora você pode usar funções para trabalhar com mapas. Esse recurso pode ser aproveitado com as listas de assinaturas. Como exemplo de um segmento, agora é possível obter um endereço de email de uma lista de assinaturas. [Saiba mais neste exemplo ](../building-journeys/message-to-subscribers-uc.md)

* **Monitoramento** - Os eventos de etapa para jornadas ativas e modo de teste foram aprimorados. [Novos campos](../reports/sharing-field-list.md#serviceevents) foram adicionados relacionados a trabalhos de exportação de perfil. Para obter uma melhor experiência do usuário, os campos de evento de etapa agora estão organizados em categorias diferentes. Todos os campos de eventos de etapa anteriores ainda estão disponíveis na categoria [stepEvents](../reports/sharing-legacy-fields.md).
* **Acessibilidade** - As melhorias de acessibilidade foram implementadas nas jornadas.
* **Coleções** - Matrizes de objetos que contêm subobjetos agora são compatíveis. [Leia mais](../building-journeys/collections.md)
* **Listas** - As telas de listas foram aprimoradas para jornadas, eventos, ações e fontes de dados.

**Relatórios**

* **Formato de dados na Visualização global** - Agora é possível alternar entre números e porcentagens na **Visualização global** da guia de **Execução**. [Saiba mais](../messages/message-monitoring.md)


**Administração**

* **Editar predefinições de mensagem** - Agora é possível editar predefinições de mensagens e monitorar o status de atualização dessas predefinições. [Saiba mais](../configuration/message-presets.md#edit-message-preset)
* **Editar registros PTR** - Agora é possível editar os registros PTR e monitorar o status de atualização de cada registro. [Saiba mais](../configuration/ptr-records.md#edit-ptr-record)

**Personalização**

* **Nova função auxiliar para a formatação de data** - Agora é possível especificar como uma cadeia de caracteres de data deve ser representada. [Saiba mais](../personalization/functions/dates.md#format-date)


**Gerenciamento de decisão**

* **Sequência de avaliação** - O fluxo de criação de decisões novo e aprimorado permite navegar não somente entre os objetos de decisão com mais facilidade, mas também fornece um controle completo de como as coleções de ofertas são avaliadas pelo mecanismo de decisão. Isso inclui quais coleções são avaliadas juntas e separadamente e em que ordem as coleções devem ser avaliadas. [Saiba mais](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correções

* Correção de um problema que impedia a exibição da lista de Jornadas, da lista de Mensagens e do Designer de email quando o idioma do navegador não estava em inglês.
* Correção de um erro de sintaxe que ocorria ao adicionar personalização usando uma expressão no Designer de email: os caracteres eram evitados incorretamente.
* Correção de um problema que resultava em um erro 404 ao navegar no menu **Administração**.
* Correção de um problema que acionava outras jornadas ativas ao testar uma jornada usando um evento comercial.


## Versão de setembro de 2021 {#september-2021-release}

### Novos recursos

<table>
<thead>
<tr>

<th><strong>Relatórios - Melhor insight para o público-alvo</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Novas métricas estão disponíveis nos relatórios: Segmentado e Excluído para mensagens de email &amp; e por push estão visíveis nos relatórios ao vivo e global. </br> Para ter acesso às métricas mais recentes, observe que será necessário redefinir os diferentes painéis de relatórios para cada canal e tipo de relatório. Para obter mais informações sobre a personalização de painéis, consulte a <a href="../reports/live-report.md">documentação detalhada.</a></p>
<p>Uma nova coluna na lista de execução de mensagens exibe o número de perfis segmentados para cada execução de mensagem. </p>
<p>Para obter mais informações, consulte a <a href="../messages/message-monitoring.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Transmita listas de dados dinamicamente usando ações personalizadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível enviar coleções ou uma lista de dados nos parâmetros de ação personalizados que serão preenchidos dinamicamente no tempo de execução. Há suporte para dois tipos de coleções: coleções simples e coleções de objetos. As ações personalizadas criadas anteriormente continuarão funcionando. </p>
<p>Para mais informações sobre coleções, consulte a <a href="../building-journeys/collections.md"> documentação detalhada</a>. </p>
<p>As funções de filtro e interseção foram adicionadas à lista de funções disponíveis no editor de expressão avançado. Isso oferece mais possibilidades para filtragem e comparação de coleção.</p>
<p>Consulte a documentação nas funções <a href="../building-journeys/functions/functionfilter.md">filtro</a> e <a href="../building-journeys/functions/functionintersect.md">interseção</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* Os esquemas e conjuntos de dados gerados pelo sistema que foram criados durante o provisionamento para eventos da etapa agora estão no modo somente leitura, protegendo contra qualquer modificação inadvertida em esquemas críticos. [Saiba mais](../reports/sharing-overview.md)
* Rotule claramente a atividade **Aguardar** com um rótulo que será exibido na tela. O rótulo também é usado em logs de relatórios e modos de teste para identificar claramente o que você está fazendo. [Saiba mais](../building-journeys/about-journey-activities.md#best-practices)
* Encontre os seus eventos e ações com mais rapidez filtrando os elementos nas categorias **Eventos** e **Ação** usando a pesquisa. As atividades de orquestração não são mais filtradas. [Saiba mais](../building-journeys/using-the-journey-designer.md)
* Ao definir uma condição de ID de evento em um evento com base em regras ou de negócios, o operador &quot;contém&quot; agora está disponível para tipos de cadeias de caracteres de campos. [Saiba mais](../event/about-creating.md)

**Configuração de email**

* Quando um pool de IP tiver sido associado a uma predefinição de mensagem, você poderá editá-lo, sendo a atualização assíncrona. Você também pode verificar cada status de atualização do pool de IP. [Saiba mais](../configuration/ip-pools.md#edit-ip-pool)


## Versão de agosto de 2021 {#august-2021-release}

### Novos recursos

<table>
<thead>
<tr>

<th><strong>Envie mensagens na melhor hora - Otimização do tempo de envio</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envie sua mensagem por push ou de email automaticamente na melhor hora para cada cliente com quem você interagir usando o Adobe Journey Optimizer. A Otimização de tempo de envio, viabilizada pelos serviços de IA da Adobe, prevê o melhor momento para enviar um email ou mensagem por push. Isso maximiza o engajamento com base no histórico das taxas de abertura e de cliques pronto para uso.</p>
<p>No momento, esse recurso está na versão beta e só está disponível para clientes beta. Para participar do programa beta, entre em contato com o Atendimento ao cliente da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journeys-message.md#send-time-optimization"> documentação detalhada </a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Aproveite relacionamentos entre esquemas em eventos de negócios - Gerenciamento de tabela de pesquisa</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aproveitar os relacionamentos entre esquemas ao configurar um evento de negócios. Além disso, você ainda tem a capacidade de aproveitar os campos de tabelas vinculadas ao configurar um evento unitário, ao usar condições em uma jornada, na personalização de mensagens e na personalização de ações.</p>
<p>Para obter mais informações, consulte a <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>URLs personalizados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os URLs personalizados levam os recipients para páginas específicas de um site ou para um microsite personalizado, dependendo dos atributos do perfil. No Adobe Journey Optimizer, agora é possível adicionar personalização a URLs no conteúdo da mensagem. A personalização de URLs pode ser aplicada ao texto e às imagens, e usar dados do perfil ou dados contextuais.</p>
<p>Para obter mais informações, consulte a <a href="../personalization/personalization-syntax.md#perso-urls">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Certifique-se de que seus emails cheguem aos seus usuários - Nova tentativa de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível predefinir o período de nova tentativa para garantir que as novas tentativas não sejam mais executadas quando não forem mais necessárias. Por exemplo, é possível definir o período de nova tentativa para 24 horas para uma mensagem transacional de redefinição de senha contendo um link válido por apenas um dia. Observe que as configurações de nova tentativa se aplicam somente ao canal de email.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/retries.md#retry-duration">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Definir endereços a serem excluídos do envio - Lista de supressão</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A adição de endereços de email e domínios à lista de supressão agora está disponível na interface do usuário, seja um por um, seja em massa, por meio de upload de um arquivo CSV.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


### Melhorias

**Jornadas**

* **Cabeçalhos dinâmicos** - Agora é possível transferir dados dinâmicos em parâmetros de cabeçalho HTTP. Esses parâmetros podem ser usados pelos sistemas de integração que recebem as chamadas HTTP da ação de jornada, por exemplo, carimbo de data e hora ou ID de rastreamento.   [Saiba mais](../action/about-custom-action-configuration.md#url-configuration)
* **Caminhos dinâmicos de URL** - Agora é possível configurar caminhos dinâmicos de URL para ações personalizadas. [Saiba mais](../action/about-custom-action-configuration.md#url-configuration)
* A taxa de limitação geral para ler segmentos foi alterada de 17.000 para 20.000 mensagens por segundo. [Saiba mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interface do usuário**

* **Pesquisa** - Em cada página, agora é possível pesquisar objetos de negócios e artigos de ajuda diretamente do campo de pesquisa inificada da Experience Cloud. [Saiba mais](../start/user-interface.md#unified-search)
* **Recentes** - A exibição de elementos recentes da página inicial do Adobe Journey Optimizer agora se estende a objetos comerciais adicionais. Com essa atualização, os atalhos para o que você acessou recentemente incluem Mensagens, Jornadas, Segmentos, Esquemas, Conjuntos de dados, Fontes de dados, Eventos, Ações, Fontes e Destinos. [Saiba mais](../action/about-custom-action-configuration.md#passing-collection)

**Design de conteúdo**

* **Plano de fundo** - Imagens de planos de fundo agora são compatíveis com a pré-visualização ao vivo. [Saiba mais](../messages/preview.md)
* **Link para opção de não participação com um clique** - É possível inserir um novo tipo de link no conteúdo de email: o link para **opção de não participação** permite que os usuários cancelem o recebimento de suas comunicações com apenas um clique, sem serem redirecionados para uma página de aterrissagem para confirmar a recusa. [Saiba mais](../messages/consent.md#one-click-opt-out-link)

**Personalização**

* **Editor de expressão** - Agora é possível adicionar facilmente um valor de fallback ao definir a personalização: quando o campo de personalização estiver vazio para um perfil, o valor de fallback será exibido. [Saiba mais](../personalization/functions/helpers.md)

**Configuração de email**

* **Lista de permissões** - A lista de permissões agora pode ser ativada e desativada em uma sandbox de não produção por meio de uma chamada de API. [Saiba mais](../messages/allow-list.md#enable-allow-list)
* **Navegação** - A lista de supressão, que estava acessível no menu **Administração > Canais > Configuração de email > Geral**, foi movido para o novo submenu **Lista de supressão**, que reúne todos os recursos relacionados para facilitar o acesso. [Saiba mais](../configuration/manage-suppression-list.md#access-suppression-list)

**Gerenciamento de decisão**

* A maneira de adicionar e configurar representações ao criar uma oferta foi atualizada para melhorar a experiência do usuário. Especificamente, a Biblioteca de ativos agora é exibida somente quando você define o conteúdo do tipo imagem para uma representação. [Saiba mais](../offers/offer-library/creating-personalized-offers.md#representations)

### Correções

* Correção de um problema de acessibilidade na navegação da guia de mensagem.
* Correção de um problema de localização nos rótulos do designer de email.
* Correção de um problema ao selecionar mais de um nó em uma jornada e clicar em Excluir no painel de propriedades.
* Correção de um problema que impedia a adição de um novo cabeçalho a uma ação usada em uma jornada.
* Agora você pode descobrir o motivo pelo qual uma criação de predefinição de mensagem falhou por meio de um aviso mais explícito na interface do usuário.


## Versão de julho de 2021 {#july-2021-release}

### Novos recursos

<table>
<thead>
<tr>
<th><strong>Use metadados em suas mensagens - Gerenciamento da tabela de pesquisa</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Enriqueça as suas experiências com dados de referência carregados no Journey Optimizer. Os exemplos incluem pesquisar metadados em uma ID de reserva em um evento de experiência ou encontrar informações do produto de uma SKU em um evento de experiência para uso na tela. </p>
<p>Agora você pode aproveitar os relacionamentos entre esquemas para usar um conjunto de dados como uma tabela de pesquisa para outro. Em seguida, você pode aproveitar todos os campos das tabelas vinculadas ao configurar um evento unitário, ao usar condições em uma jornada, na personalização da mensagem e na personalização da ação customizada.</p>
<p>Para obter mais informações, consulte a <a href="../event/experience-event-schema.md#leverage_schema_relationships"> documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lista de permissões</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir uma lista específica de segurança de envio no nível da sandbox, para ter um ambiente seguro para fins de teste. Em uma instância de não produção, em que podem ocorrer erros, a lista de permissões garante que você não tenha risco de enviar mensagens indesejadas para os seus clientes. Esse recurso é habilitado por meio das APIs de supressão.</p>
<p>Para obter mais informações, consulte a <a href="../messages/allow-list.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias

**Jornadas**

* A taxa de limitação geral de todos os segmentos de leitura executados simultaneamente na mesma sandbox é limitada a 17.000 mensagens por segundo. [Leia mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* O campo **Duração do cache** foi removido do painel de configuração da fonte de dados. [Leia mais](../datasource/about-data-sources.md)
* Para fontes de dados externas, uma regra de limitação de 15 chamadas por segundo agora é definida automaticamente. [Leia mais](../configuration/external-systems.md#capping)
* Para as jornadas em tempo real, a tela de propriedades da jornada agora exibe a data da publicação e o nome do usuário que publicou a jornada. [Leia mais](../building-journeys/journey-gs.md#change-properties)
* Na tela da lista de jornadas, o filtro Tipo de jornada foi adicionado. [Leia mais](../start/user-interface.md#filter-lists)
* O parâmetro **[!UICONTROL Throttling rate]** foi adicionado na atividade Ler segmento. [Leia mais](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Pré-visualizar e testar mensagens**

* A identidade e o namespace agora estão visíveis na **[!UICONTROL Preview]** tela. [Leia mais](../messages/preview.md#preview-your-messages)
* O número de emails de teste para provas agora está restrito a 10.
* Caracteres permitidos nas provas de **prefixo da linha de assunto** agora são limitadas. [Leia mais](../messages/preview.md#send-proofs)

**Editor de expressão de personalização**

* A lista suspensa de ajuda foi renomeada e reordenada.

### Correções

* Correção de um problema que gerava mensagens duplicadas sendo entregues para delivery de emails em lote.
* Agora os eventos são gerados adequadamente quando o envio de email não é executado após o término do período de nova tentativa.
* Correção de um problema em que as informações de IP estavam ausentes na tela Registros PTR .
* A localização no painel de ofertas no Editor de expressão agora está implementada.
* Corrigido o espaçamento incorreto em pop-ups de informações.
* Correção de um problema no Designer de email ao fazer upload de um arquivo HTML no qual a folha de estilos interna com as propriedades `background-image` não era suportada.
