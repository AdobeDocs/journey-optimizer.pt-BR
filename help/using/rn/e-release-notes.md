---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 1f3adcb8c636ccd1a354af910441f4bda57015d7
workflow-type: tm+mt
source-wordcount: 1809
ht-degree: 10%

---


# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de 26 de junho {#june-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas podem ser lançadas posteriormente — consulte a Data de disponibilidade listada para cada entrada para obter detalhes.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 16 a 17 de junho de 2026


### Jornadas {#june-26-journeys}

Os seguintes recursos e melhorias estão chegando às jornadas nesta versão.

<table>
<thead>
<tr>
<th><strong>Arbitragem de Jornada - Fórmulas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar <strong>fórmulas</strong> para <strong>priorizar e arbitrar jornadas</strong> automaticamente com base nos atributos do perfil do cliente e em fatores contextuais, garantindo que os clientes insiram as jornadas mais relevantes.</p>
<p>Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14719">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Limite de jornadas ao vivo aumentado e novas medidas de proteção** - Agora você pode ter até **200 jornadas ativas**, maior que o limite anterior de 100.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14826">Vincular à tarefa DOCAC JIRA</a>

* **Datas de início e término no cabeçalho da jornada** - Quando as datas de início e/ou término são configuradas em uma jornada em tempo real, elas agora são exibidas no **cabeçalho da jornada** ao lado da notificação de status em tempo real. O rótulo exibido se adapta com base no fato de cada data ser futura ou já ter passado.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">Vincular à tarefa DOCAC JIRA</a>

* **Parar ou fechar uma jornada pausada diretamente** - Agora você pode **parar uma jornada ou fechá-la em novas entradas** diretamente do estado **Pausado**. Anteriormente, uma jornada pausada tinha que ser retomada para Ativa antes de ser interrompida ou fechada.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14229">Vincular à tarefa DOCAC JIRA</a>

* **Suporte de identificador complementar para públicos externos** - Os identificadores complementares no jornada agora têm suporte para públicos externos, incluindo públicos importados de um arquivo CSV e públicos criados com a Composição de Público Federado. Você pode designar qualquer atributo que não seja de identidade ou atributo de identidade que não seja de pessoa do público-alvo como a ID complementar; nenhum rótulo de esquema é necessário.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14541">Vincular à tarefa DOCAC JIRA</a>

### Campanhas orquestradas {#june-26-oc}

Os seguintes recursos e melhorias estão chegando às campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Atividade de carregamento de arquivo em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora permitem carregar um <strong>arquivo CSV ou TXT</strong> diretamente na tela da campanha como público alvo, sem primeiro assimilar o arquivo na Adobe Experience Platform. Os dados do arquivo são consumidos no tempo de execução e não são mantidos como um conjunto de dados do Adobe Experience Platform. Durante a configuração do arquivo, você pode definir mapeamentos de coluna, tipos de dados, tratamento NULL e políticas de erro por coluna. Isso oferece suporte a envios ad hoc ou campanhas de lista de parceiros em que a criação de um pipeline de assimilação completo não é prática.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14704">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Personalização baseada em loop para dados relacionais em campanhas orquestradas** - O editor de personalização agora oferece suporte a um **Bloco de loop** que repete coleções relacionais, como pedidos, contas ou reservas, e renderiza um bloco de conteúdo por registro em um único email ou SMS. As coleções são configuradas por meio do seletor de dados usando tokens de personalização, sem a necessidade de gravação de expressão.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14703">Vincular à tarefa DOCAC JIRA</a>

* **Personalizar detalhes do remetente de email por destinatário e campanha** - As campanhas orquestradas agora oferecem suporte à personalização de **campos de cabeçalho de email**, incluindo Do nome, Do endereço e Responder para, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o supervisor, o local ou a ramificação relevante para cada destinatário, em vez de rotear todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">Vincular à tarefa DOCAC JIRA</a>

* **Simplificação da dimensão de público alvo em campanhas orquestradas** - A **targeting dimension** ativa agora é mostrada na tela do fluxo de trabalho para que você possa ver qual dimensão é usada por uma atividade de canal. O fluxo de segmentação de várias entidades é mais simples, pois você não precisa mais de uma atividade &quot;Alterar dimensão&quot; separada. Além disso, agora você pode escolher explicitamente se as mensagens são enviadas no nível do perfil ou em um nível de dimensão secundário.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">Vincular à tarefa DOCAC JIRA</a>

### Tomada de decisão {#june-26-decisioning}

O recurso a seguir está chegando à Decisão nesta versão.

<table>
<thead>
<tr>
<th><strong>Aproveitar o fragmento de conteúdo do Adobe Experience Manager na Decisão</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode mapear <strong>fragmentos de conteúdo do Adobe Experience Manager</strong> para <strong>itens de decisão</strong> na Decisão e aproveitá-los nas políticas de decisão para fornecer o fragmento certo ao cliente certo na hora certa.</p>
<p>Anteriormente lançado em disponibilidade limitada para uso em jornadas, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14885">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Canal de email {#june-26-email}

Os seguintes recursos e melhorias estão chegando ao canal de email nesta versão.

<!--
<table>
<thead>
<tr>
<th><strong>Advanced Components</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Email Designer now includes a library of ready-to-use layout components — such as Headers, Product Cards (1, 2, or 3 columns), Information blocks, and Footers — that you can drag and drop directly into your email canvas. Each component comes pre-configured with editable properties (image, title, text, button, links) and can be fully customized through the WYSIWYG interface, speeding up email creation without requiring you to build structures from scratch.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14877">Link to DOCAC JIRA task</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Verificação de conteúdo no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite que os usuários validem sua <strong>qualidade do conteúdo de email</strong> - incluindo legibilidade, eficácia e coesão de conteúdo - diretamente na interface do Designer de email.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14870">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Habilitar redução de tamanho de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta nova opção permite <strong>reduzir o tamanho da HTML</strong> em um email removendo espaços em branco, comentários e códigos redundantes desnecessários — sem alterar a aparência do email. Isso ajuda a melhorar a capacidade de entrega (alguns provedores de email rejeitam ou sinalizam emails superdimensionados) e pode acelerar o tempo de carregamento dos recipients.</p>
<p>Data de disponibilidade: 10 de junho de 2026</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14777">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

* **Suporte ao modo de texto em fragmentos** - Para oferecer suporte a fluxos de trabalho de email baseados em texto, agora é possível criar e gerenciar versões de texto dos fragmentos visuais para uso ideal na versão de texto sem formatação dos emails que incluem esse fragmento. Ao usar um fragmento que foi criado antes da versão atual, a versão do texto do fragmento pode ser renderizada incorretamente — tanto no Designer de email quanto no email final entregue aos recipients. Para obter melhores resultados com fragmentos mais antigos, edite, salve e republique cada fragmento.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14204">Vincular à tarefa DOCAC JIRA</a>

* **Os benchmarks de taxa de transferência de término de lote foram atualizados com cenários voltados para o cliente** - Os benchmarks de taxa de transferência de envio de lote da Adobe Journey Optimizer foram atualizados para refletir o desempenho de nível de produção em vários cenários de personalização — desde envios básicos até conteúdo dinâmico complexo com lógica condicional. As métricas atualizadas agora estão disponíveis na documentação do produto para ajudar os clientes a planejar com precisão seus volumes de mensagens.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14816">Vincular à tarefa DOCAC JIRA</a>

* **Processo OTP de Loop de Comentários para subdomínios personalizados** - O processo de configuração de subdomínio personalizado FBL (Loop de Comentários) foi aprimorado ao exibir o hub do remetente do Yahoo **OTP (Senha ocasional)** diretamente na interface do usuário do produto. Os usuários agora podem recuperar e exibir automaticamente o OTP gerado durante a verificação de propriedade de domínio do hub do remetente do Yahoo.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">Vincular à tarefa DOCAC JIRA</a>

### Mensagens por dispositivo móvel (SMS, MMS, RCS e LINE) {#june-26-mobile}

As seguintes melhorias estão chegando para o sistema de mensagens móveis nesta versão.

* **Cliques únicos para relatórios de SMS** - Um novo módulo **Cliques únicos** foi introduzido nos relatórios de SMS, trazendo o mesmo nível de rastreamento de desempenho granular para o SMS que está disponível atualmente para relatórios de Email.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14895">Vincular à tarefa DOCAC JIRA</a>

* **Canal LINE - Alterações de criação** - A interface do canal LINE foi atualizada com recursos avançados de criação de mensagens. Esta versão apresenta suporte para **vários formatos de mensagem**, incluindo Texto, Imagem, Imagemap, Carrossel e Flex (Editor JSON), além de visualizações de dispositivos em tempo real. Os usuários agora podem gerenciar mensagens agrupadas de até cinco mensagens ordenadas (com controles para adicionar, remover e reordenar) e aproveitar o editor de personalização integrado para mensagens dinâmicas validadas.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">Vincular à tarefa DOCAC JIRA</a>

* **SMS - Exibir Métricas de Uso** - Para clientes que compram SMS diretamente pelo Adobe Journey Optimizer, foi introduzido um novo **painel de uso de SMS**. Agora é possível visualizar e rastrear os últimos 90 dias de métricas de envio de mensagens, categorizadas por mensagens Originadas por dispositivos móveis (MO) e Terminadas por dispositivos móveis (MT). Esses dados também estão disponíveis para download via CSV, fornecendo maior visibilidade e controle sobre o gasto com SMS.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14345">Vincular à tarefa DOCAC JIRA</a>

### Conteúdo e integrações {#june-26-content}

Os seguintes recursos e melhorias estão chegando ao gerenciamento de conteúdo e integrações nesta versão.

<table>
<thead>
<tr>
<th><strong>Melhorias nos fragmentos de conteúdo do Adobe Experience Manager no Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta versão traz várias melhorias para tornar os <strong>Fragmentos de conteúdo do Adobe Experience Manager</strong> mais utilizáveis, controláveis e prontos para produção nos fluxos de trabalho de criação do Journey Optimizer:</p>
<ul>
<li>O Journey Optimizer agora é compatível com a busca de fragmentos de conteúdo de várias configurações do Adobe Experience Manager, incluindo níveis de criação, publicação e publicação autenticada.</li>
<li>Depois que um fragmento é selecionado, seu contexto é preservado em toda a mensagem, permitindo que os autores reutilizem campos de fragmento nos blocos de conteúdo sem fazer nova seleção.</li>
<li>Uma nova página dedicada de listagem de fragmentos de conteúdo foi introduzida no Journey Optimizer para melhorar o gerenciamento do ciclo de vida; os usuários podem identificar fragmentos fora de sincronia e acionar sincronizações manuais para se manterem atualizados.</li>
<li>O suporte a local e variação agora permite que os profissionais de marketing trabalhem com versões alternativas do mesmo Fragmento de conteúdo mais deliberadamente.</li>
<li>Agora você tem flexibilidade em como o Adobe Journey Optimizer acessa o conteúdo do Adobe Experience Manager. Esta versão apresenta a capacidade de <strong>alternar o repositório de origem</strong> para fragmentos de conteúdo usados em suas jornadas e campanhas.</li>
<li>Agora compatível com o <b>Managed Services</b>, você pode visualizar, acessar e usar os Fragmentos de conteúdo do Adobe Experience Manager diretamente no Journey Optimizer para personalização. Basta adicionar o URL do repositório do Adobe Experience Manager Managed Services nas definições de configuração do como uma configuração única.</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14686">Link para a tarefa DOCAC no JIRA</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14821">Link para a tarefa DOCAC no JIRA</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14684">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do assistente de IA com o Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA agora busca automaticamente <b>imagens aprovadas pela marca</b> diretamente da sua Adobe Experience Manager Assets ao gerar emails, páginas da Web e notificações por push. Isso elimina a necessidade de pesquisar manualmente o Assets ou confiar em fallbacks de IA genéricos, garantindo que cada visual seja perfeitamente preciso e compatível com a marca.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14761">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Canais personalizados {#june-26-channels}

O recurso a seguir está chegando aos canais nesta versão.

<table>
<thead>
<tr>
<th><strong>Canal de saída personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora apresenta os <strong>Canais personalizados</strong>, um novo recurso que permite aos administradores trazer qualquer canal de mensagens baseado em HTTP de saída — como WeChat, Kakao Talk, Messenger ou um provedor proprietário — diretamente para o Journey Optimizer por meio de um construtor de canal sem código.</p>
<p>Depois de configurados, os canais personalizados ficam disponíveis em campanhas, jornadas e campanhas orquestradas, com o mesmo conjunto completo de recursos dos canais nativos: personalização com o editor de expressão, experimentação de conteúdo, pré-visualização e prova, relatórios prontos para uso e aplicação de consentimento e governança. Isso preenche a lacuna anteriormente abordada por ações personalizadas, que estavam limitadas a jornadas e não tinham criação de conteúdo dedicado.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11381">Link para a tarefa DOCAC no JIRA</a></p>
</td>
</tr>
</tbody>
</table>

### Campanhas {#june-26-campaigns}

O aprimoramento a seguir está chegando às campanhas nesta versão.

* **Substituir o campo de execução padrão em campanhas** - Anteriormente disponível no nível de jornada, agora você pode substituir o **campo de execução** padrão definido globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da campanha.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">Vincular à tarefa DOCAC JIRA</a>

### Relatório {#june-26-reporting}

Os seguintes aprimoramentos estão chegando aos relatórios nesta versão.

* **Novas métricas de clique estimadas para relatórios de email e SMS** - Para fornecer uma visão mais precisa do engajamento real do cliente, novas métricas estimadas agora estão disponíveis nos relatórios de Jornadas, Campanhas e Canais. Essas métricas ajudam a filtrar interações não humanas (NHI) e cliques de bot a partir de dados de relatórios:
   * Estimated Clicks: Total de cliques contados após a remoção do tráfego identificado de bot e não humano.
   * Estimated CTR: Cliques estimados em relação ao total de deliveries.
   * CTOR estimado somente para email: Estimativa de cliques relativos a Aberturas estimadas.

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14354">Vincular à tarefa DOCAC JIRA</a>

### Configuração {#june-26-configuration}

As seguintes melhorias estão chegando à configuração e administração nesta versão.

* **Listas de permissões de IP do WAF (Firewall de Aplicativo Web)** - O Adobe Journey Optimizer agora oferece suporte à lista de permissões de IP do WAF para páginas de aterrissagem, permitindo que as organizações garantam que todas as solicitações recebidas sejam roteadas exclusivamente por meio de sua infraestrutura configurada do WAF. Com esse aprimoramento, os clientes podem configurar o Journey Optimizer para rejeitar qualquer solicitação direta que ignore a camada do WAF, garantindo que as políticas de segurança definidas em ferramentas como o Imperva sejam aplicadas de forma consistente. Esse recurso fortalece a postura de segurança para empresas com requisitos rigorosos de acesso à rede, dando a elas controle total sobre o fluxo de tráfego para as páginas de aterrissagem hospedadas pela Journey Optimizer.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">Vincular à tarefa DOCAC JIRA</a>

* **Conjunto de dados passando do modo de streaming para o modo de lote** - O Conjunto de Dados de Evento de Feedback de Mensagens do AJO está passando do modo de streaming para o **modo de assimilação em lote**. Essa alteração garante que a assimilação de dados não exceda os limites de assimilação de streaming. Se você usar esse conjunto de dados nos relatórios do Customer Journey Analytics ou executar consultas nele, espere um aumento na latência de dados de até 2 horas no futuro.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14771">Vincular à tarefa DOCAC JIRA</a>

### Melhorias de usabilidade {#june-26-usability}

A seguinte melhoria de usabilidade está chegando nesta versão.

* **Pastas para Jornadas e Campanhas** - Agora você pode organizar suas jornadas e campanhas em **pastas** para melhorar a navegação e o gerenciamento na interface.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">Vincular à tarefa DOCAC JIRA</a>

