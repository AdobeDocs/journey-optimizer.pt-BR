---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 990e2d70954c7a2b1c0cdd2a0934b6ad20924e28
workflow-type: tm+mt
source-wordcount: 2408
ht-degree: 22%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** oferece continuamente novos recursos, melhorias nos recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] segue um modelo de entrega contínua, permitindo que a Adobe forneça novos recursos, melhorias e correções de forma contínua. Essa abordagem permite uma implantação escalável e em fases de recursos para garantir desempenho e estabilidade em todos os ambientes. Devido a esse modelo, as notas de versão são atualizadas entre as versões mensais. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](releases.md).

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

>[!NOTE]
>
>Os recursos listados nestas notas de versão incluem uma **Data de disponibilidade** indicando quando cada alteração se torna acessível no ambiente. As entradas nos acordeões **Em breve** são esperadas nos próximos dias ou semanas. As informações nessas seções estão sujeitas a alterações.

## Notas de versão de julho de 2026 {#july-26-updates}

### Desafios de fidelidade {#july-26-loyalty}

A Journey Optimizer apresenta os desafios de fidelidade, um novo recurso nesta versão.

<table>
<thead>
<tr>
<th><strong>Desafios de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os desafios de fidelidade transformam iniciativas de fidelidade em experiências envolventes e gamificadas que motivam os clientes a realizar ações valiosas, como fazer compras, escrever comentários ou qualquer comportamento desejado.</p>
<p>Os administradores podem usar o menu Admin de fidelidade para conectar o Journey Optimizer ao seu ecossistema de fidelidade, incluindo APIs de atendimento de recompensa, definições de eventos, inventário de produtos, exclusões e configurações de identidade. Em seguida, os profissionais de marketing podem projetar desafios padrão, sequenciais ou em sequência, definir tarefas e recompensas, fornecer cartões de conteúdo e mensagens de marca e monitorar o desempenho com painéis de relatórios alimentados por IA. A Journey Optimizer gera as jornadas que organizam cada desafio em segundo plano, para que as equipes possam se concentrar na experiência do cliente e nas metas de negócios.</p>
<p>A fidelização também apresenta habilidades de colegas de trabalho que permitem que as equipes executem operações de desafio principais com mais eficiência, incluindo a criação de desafios, a definição de propriedades de desafio, o gerenciamento de públicos-alvo e configurações relacionadas e a análise de insights para monitorar a participação de desafios e o desempenho de recompensas.</p>
<p>Esse recurso só está disponível para organizações licenciadas para o Journey Optimizer Loyalty. Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../loyalty-challenges/get-started.md">documentação detalhada</a>.</p>
<p> Data de disponibilidade: 28 de julho de 2026</p>
</td>
</tr>
</tbody>
</table>

### Canais de saída {#july-26-outbound-channels}

O recurso a seguir foi introduzido nesta versão.

<table>
<thead>
<tr>
<th><strong>Otimização de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar uma jornada ou ação de campanha para incluir vários canais de saída (Email, Push, SMS) e permitir que o Journey Optimizer forneça automaticamente por meio do melhor canal para cada cliente. Três modos de otimização estão disponíveis:</p>
<ul>
<li>Classificação manual: especifique a ordem de canal de sua preferência.</li>
<li>Preferência do cliente: use o canal de preferência do cliente em seu perfil (atributo Consentimentos e preferências do modelo de dados de experiência).</li>
<li>Classificação baseada em modelo de IA: use pontuações de propensão de aprendizado de máquina para inferir o canal mais eficaz por cliente.</li>
</ul>
<p>Quando o canal mais bem classificado estiver indisponível (não aceito, com limite de frequência ou não configurado), o sistema voltará para o próximo canal disponível.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p><img src="assets/do-not-localize/channel-optimization.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/channel-optimization.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 22 de julho de 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Em breve

* **Canal do WhatsApp: suporte a modelos de fluxo do WhatsApp** - Agora você pode enviar modelos de fluxo do WhatsApp no Adobe Journey Optimizer para fornecer experiências interativas em várias telas, como pesquisas e captura de leads. As respostas são capturadas no envio e armazenadas como cargas JSON brutas no novo conjunto de dados de evento de rastreamento de canal do Journey Optimizer.

* **Integrações aprimoradas do provedor personalizado - Dispositivo móvel** - As integrações personalizadas do provedor agora oferecem maior flexibilidade com mensagens principais e atualizações de cabeçalho:

  * Personalização de cabeçalho: Agora é possível editar o valor padrão do cabeçalho Content-Type e adicionar até 10 parâmetros de cabeçalho personalizados.

  * Suporte a carga SMS: adição de suporte para funções auxiliares do Adobe Journey Optimizer na carga SMS, incluindo encode64.

+++

### Jornadas {#july-26-journeys}

Os recursos e melhorias a seguir foram adicionados às jornadas nesta versão.
<table>
<thead>
<tr>
<th><strong>Nova interface de usuário</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma <b>nova interface de usuário</b> foi introduzida para a tela de jornada, oferecendo melhor desempenho para jornadas grandes, layout automático para melhorar a legibilidade e uma experiência de criação guiada.</p>
<p><img src="../building-journeys/assets/journey-new-canvas.png"></p>
<p>Para alternar para a nova interface, clique no botão <b>Nova experiência</b>. Essa configuração é salva no nível da jornada, para que a jornada reabra na nova experiência por padrão. Para reverter, clique em <b>Experiência antiga</b>. <a href="../building-journeys/using-the-journey-designer.md#canvas-capabilities">Saiba mais</a>.</p>
<p><img src="../building-journeys/assets/journey-new-experience-switch.png"></p>
<p> Data de disponibilidade: 16 de julho de 2026</p>
</td>
</tr>
</tbody>
</table>

* [!BADGE Descontinuação]{type=Negative} **Públicos-alvo em lote não são mais suportados no nó de Qualificação de Público-Alvo e nos Critérios de Saída** - A partir de setembro de 2026, a Journey Optimizer bloqueará a publicação de qualquer jornada usando um público-alvo em lote em um nó de Qualificação de Público-Alvo ou nos Critérios de Saída. Um aviso de validação já foi exibido na tela de jornada.  As jornadas ativas existentes não são afetadas. As jornadas novas, de rascunho e duplicadas que incluem essa configuração devem ser atualizadas antes de setembro de 2026. Use um público-alvo de transmissão no nó Qualificação do público-alvo ou alterne para uma atividade Ler público-alvo. Para Critérios de saída, use um público-alvo de transmissão. [Saiba como migrar suas jornadas](../building-journeys/aq-batch-audiences-migration.md)

+++ Em breve

* **Públicos-alvo externos na Simulação de Jornada** - A Simulação de Jornada agora oferece suporte a Públicos-alvo Externos. Ao simular jornadas direcionadas a públicos-alvo de CSV ou Composição de público-alvo federado, você pode simular atributos de enriquecimento desses públicos-alvo diretamente pelo formulário da interface ou por uma importação de JSON. A interface do usuário exibe dinamicamente apenas os atributos específicos de enriquecimento usados na lógica de jornada, permitindo a validação precisa das ramificações de decisão e regras de personalização antes da ativação.

+++

### Designer de email {#july-26-email}

Os seguintes recursos e melhorias foram adicionados ao canal de email nesta versão.

<table>
<thead>
<tr>
<th><strong>Módulos no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Designer de email agora inclui uma biblioteca de módulos de layout prontos para uso — como cabeçalhos, cartões de produto, blocos de informações e rodapés — que você pode arrastar e soltar diretamente na tela do email.</p>
<p>Cada módulo vem pré-configurado com propriedades editáveis (imagem, título, texto, botão, links) e pode ser totalmente personalizado por meio da interface WYSIWYG, acelerando a criação de emails sem exigir a construção de estruturas do zero.</p>
<p><img src="assets/do-not-localize/email-modules.gif"></p>
<p>Data de disponibilidade: 29 de julho de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verificação de conteúdo no Designer de email (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora inclui validação técnica automatizada diretamente no Designer de email, ajudando a detectar problemas no HTML e no CSS antes do envio.</p>
<p>As verificações abrangem elementos incompatíveis, como tags <code>&lt;script&gt;</code> e <code>&lt;base&gt;</code>, divs em branco que podem quebrar o layout no Microsoft Outlook, tags HTML meta refresh e limites de tamanho de CSS ou HTML que causam falhas de renderização no Gmail.</p>
<p>Os resultados são exibidos como erros, avisos ou avisos informativos diretamente no painel de criação, com detalhes contextuais e correções com um clique, quando disponíveis, para que os problemas possam ser resolvidos sem sair do editor.</p>
<p>Anteriormente em Disponibilidade limitada, esse recurso agora está disponível para todos os clientes.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>Para obter mais informações, consulte a <a href="../email/content-check.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 16 de julho de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Suporte a fragmentos de expressão em `<head>` de modelos de email** - Os fragmentos de expressão agora podem ser usados no `<head>` de modelos de email. Isso permite centralizar o estilo ou qualquer código personalizado em um único fragmento e reutilizá-lo em vários modelos. Quando um fragmento é atualizado e republicado, todos os emails criados a partir de modelos que fazem referência a ele herdam automaticamente o código mais recente, eliminando a necessidade de atualizar manualmente cada email individualmente. [Saiba mais](../personalization/use-expression-fragments.md)

### Campanhas {#campaigns}

+++ Em breve

* **Pastas para Campanhas** - Agora você pode organizar suas campanhas em pastas para melhorar a navegação e o gerenciamento na interface. Esse recurso está disponível somente para campanhas acionadas por Ação e API.

+++

### Campanhas orquestradas {#july-26-oc}

Os recursos e melhorias a seguir estão chegando às campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Segmentação baseada em arquivo em campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As campanhas orquestradas agora permitem carregar um <strong>arquivo CSV ou TXT</strong> diretamente na tela da campanha como público alvo, sem primeiro assimilar o arquivo na Adobe Experience Platform. Os dados do arquivo são consumidos no tempo de execução e não são mantidos como um conjunto de dados do Adobe Experience Platform. Durante a configuração do arquivo, você pode definir mapeamentos de coluna, tipos de dados, tratamento NULL e políticas de erro por coluna. As linhas que falharem na validação são rejeitadas e registradas antes da execução da campanha, mantendo o público-alvo limpo sem pré-processamento manual. Isso é particularmente adequado para envios ad hoc ou campanhas de lista de parceiros em que a criação de um pipeline de assimilação completo não é prática.</p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/load-file.md">documentação detalhada</a>.</p>
<p> Data de disponibilidade: 6 de julho de 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Em breve

* **Exibir permissão de Transições de Campanha Orquestradas** - Adicionada uma nova permissão **Exibir Transições de Campanha Orquestradas** para substituir a opção herdada **Exibir Arquivo em Campanhas Orquestradas**. Essa alteração permite ocultar os resultados de visualização nas transições da campanha para oferecer suporte à conformidade com informações de identificação pessoal.

+++

### Tomada de decisão {#decisioning}

* **Criação de regras de decisão a partir de expressão em linguagem natural** - Agora é possível descrever a regra de decisão que você deseja criar em linguagem simples e permitir que a IA a gere para você. Esse recurso está disponível para clientes com acesso aos recursos do Adobe AI.

  Esse recurso está disponível para organizações com acesso aos recursos do Adobe AI. Ela só está disponível para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.

  Data de disponibilidade: 29 de julho de 2026

  [Saiba mais](../experience-decisioning/rules.md#build-rule-with-ai)

* **Atributos personalizados dinâmicos de itens de decisão** - Os atributos personalizados de itens de decisão agora podem ser personalizados no momento da entrega usando dados de perfil, contextuais e de público-alvo. Isso elimina a necessidade de manter ofertas duplicadas para pequenas variações de conteúdo, permitindo que os profissionais de marketing gerenciem menos itens de decisão e mais flexíveis. [Leia mais](../experience-decisioning/items.md#attributes)

  Data de disponibilidade: 27 de julho de 2026

* **Simulação de regras de decisão e fórmulas de classificação** - Agora é possível simular suas regras de decisão e fórmulas de classificação diretamente do editor de regras ou fórmulas. Adicione variantes de teste manuais ou gere-as usando IA e, em seguida, execute a expressão com base nos dados de teste para validar a qualificação e revisar os resultados classificados, tudo antes de implantar na produção. A geração de variantes está disponível para clientes com acesso aos recursos do Adobe AI.

  Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.

  Data de disponibilidade: 29 de julho de 2026

  [Saiba mais sobre a simulação de regras](../experience-decisioning/rules.md) | [Saiba mais sobre a simulação de fórmulas de classificação](../experience-decisioning/ranking/ranking-formulas.md)

### Gerenciamento de conteúdo {#july-26-content}

Os seguintes recursos e melhorias foram adicionados ao gerenciamento de conteúdo nesta versão.

* **Atalhos de inicialização rápida no inventário Fragmentos** - Agora você pode acessar rapidamente ações comuns da lista Fragmentos usando o botão **[!UICONTROL Mais ações]**. Os atalhos disponíveis incluem editar o fragmento, abrir os detalhes e descartar a versão de rascunho. [Saiba mais](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* **Atalhos de inicialização rápida no inventário Modelos** - O botão **[!UICONTROL Mais ações]** da lista Modelos de Conteúdo agora fornece acesso rápido a ações comuns: editar detalhes do modelo, simular conteúdo e excluir um modelo. Para modelos de email, atalhos adicionais permitem editar a linha de assunto e o corpo do email, exibir ou enviar uma prova, executar um relatório de spam e renderizar o email. [Saiba mais](../content-management/access-content-templates.md#quick-launch-templates)

  ![](../content-management/assets/content-template-quick-launch.png)

* **Novas funções auxiliares em expressões de personalização** - Novas funções auxiliares agora estão disponíveis em expressões de personalização:

  * `appendQueryParams`: anexa um parâmetro de consulta a uma URL ou a substitui se a chave já existir.
  * `dateBetween`: Verifica se uma data está dentro de um intervalo de datas inicial e final (inclusive).
  * `equalsAnyIgnoreCase`: retorna verdadeiro quando uma cadeia de caracteres corresponde a qualquer valor fornecido, ignorando maiúsculas e minúsculas.
  * `getUrlFragment`: Extrai a parte do fragmento de uma URL (a parte após #).
  * `join`: Concatena elementos de matriz em uma única cadeia de caracteres usando um separador.
  * `decode64`: Decodifica uma cadeia de caracteres codificada em Base64. Se a entrada não for Base64 válida, a cadeia de caracteres de entrada original será retornada inalterada.
  * `parseJson`: analisa uma cadeia de caracteres JSON em uma variável estruturada que pode ser usada no modelo.
  * `valueAtPath`: atribui um valor de um caminho de dados a uma variável de modelo, com indexação opcional para extrair um elemento específico de matrizes ou coleções.
  * `abort`: Para a entrega de mensagens quando alcançada durante a renderização.

  A função `concat` também foi aprimorada e agora dá suporte a dois ou mais argumentos.

  Além disso, as seguintes Funções de migração de modelo agora estão disponíveis para ajudar na migração de modelos existentes para o Journey Optimizer:

  * `ampCompare`: compara dois valores usando o operador de comparação especificado.
  * `ampSubstr`: retorna uma parte de uma cadeia de caracteres entre os índices de início e término especificados.
  * `compareTo`: compara duas cadeias de caracteres lexicograficamente.

  [Saiba mais sobre funções auxiliares](../personalization/functions/functions.md)

  Data de disponibilidade: 28 de julho de 2026

+++ Em breve

* **Origem flexível de imagens para a geração de conteúdo de IA** - A geração de conteúdo no Journey Optimizer agora origina imagens aprovadas pela marca diretamente do Adobe Experience Manager Assets Essentials e superior. Três modos controlam o equilíbrio: Assets (Gerenciamento de ativos digitais-fonte, padrão), Balanceado (Gerenciamento de ativos digitais-primeiro, IA preenche lacunas) e Creative (AI-primeiro). Isso garante que cada visual seja preciso, compatível com a marca e pronto para produção para jornadas e campanhas.

* **Melhorias multilíngues** - As configurações de idioma agora podem ser duplicadas de uma configuração ativa existente, portanto, você não precisa mais recompilar totalmente uma configuração para fazer alterações. Você também pode copiar uma condição de um local para outro enquanto cria Configurações de idioma, simplificando a configuração para sites com muitos idiomas.

* **&quot;Assistente de IA&quot; renomeado para &quot;Gerar conteúdo&quot;** - O Assistente de IA foi renomeado para Gerar conteúdo em toda a Adobe Journey Optimizer. Esta atualização está limitada à nomenclatura e terminologia; nenhuma alteração funcional foi introduzida. Rótulos de navegação, botões, menus e caixas de diálogo para geração de conteúdo, geração de imagem, expressões de personalização e experimentação de conteúdo foram renomeados de &quot;Assistente de IA&quot; para &quot;Gerar conteúdo&quot;.

+++

### Conteúdo e integrações {#july-26-integration}

As seguintes melhorias estão chegando ao gerenciamento de conteúdo e integrações nesta versão.

* **Novas ferramentas do servidor MCP do AJO** - O servidor MCP [!DNL Adobe Journey Optimizer] agora expõe cinco **ferramentas de configuração de canal** adicionais somente leitura, permitindo que você consulte configurações de canal, recursos de suporte e ações de marketing diretamente do seu assistente de IA. Agora você pode usar **Configurações de Canal de Lista** (em todos os canais da AJO), **Obter Configuração de Canal**, **Recursos de Configuração de Lista**, **Obter Recurso de Configuração** e **Ações de Marketing de Lista**. [Leia mais](../integrations/ajo-mcp.md#mcp-tools)

  Data de disponibilidade: 9 de julho de 2026

### Relatório {#july-26-reporting}

A seguinte melhoria está chegando aos relatórios nesta versão.

* **Novas métricas de clique estimadas para relatórios de email** - Para fornecer uma visão mais precisa do engajamento real do cliente, novas métricas estimadas agora estão disponíveis nos relatórios do Jornada, de Campanhas e do Channel Live.

  * Estimated CTR (taxa de cliques): calculado como cliques estimados em relação ao número total de mensagens entregues.

  * Estimated CTOR (taxa de clique para abrir): calculado como cliques estimados em relação ao número total de aberturas estimadas.

    Data de disponibilidade: 29 de julho de 2026

### Administração {#july-26-administration}

As seguintes melhorias foram adicionadas à administração e ao gerenciamento de dados nesta versão.

* **Medidas de proteção de TTL (Time-to-live) do conjunto de dados — sandboxes existentes** - A medida de proteção TTL (time-to-live) para conjuntos de dados gerados pelo sistema da Journey Optimizer (90 dias no repositório de perfis, 13 meses no data lake) será aplicada em **sandboxes e organizações de clientes existentes** a partir de **1 de outubro de 2026**. [Saiba mais](../data/datasets-ttl.md#ttl-guardrail)

### Melhorias de usabilidade {#july-26-usability}

+++Em breve

* **Nova experiência de Simulação de Conteúdo para testes de conteúdo** - O fluxo de trabalho **Simular conteúdo** apresenta uma experiência reprojetada: todas as variantes agora são renderizadas juntas em uma única grade rolável (lado a lado, empilhadas ou com layouts dispostos), substituindo o modo de exibição uma variante de cada vez. Uma única barra de ação inferior consolida a navegação entre variantes de teste, o zoom, a alternância de visor (desktop/celular), a alternância de local, a adição de entradas de amostra, a geração de variantes com IA, a escolha e o salvamento de usuários simulados e a importação ou exportação de variantes. Remover o painel esquerdo e recolher camadas de cabeçalho extras oferece visualizações com muito mais espaço. A opção **Alternar para experiência clássica** na barra de ação inferior permite reverter para a experiência anterior a qualquer momento.

+++
