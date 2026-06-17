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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 2279
ht-degree: 40%

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

## Notas de versão de junho de 2026 {#june-26-rn}

A versão de junho de 2026 traz vários recursos principais para a Disponibilidade geral — incluindo a **Simulação de Jornada**, o **Direcionamento de otimização de caminho de Jornada** e os **Fragmentos de Jornada** — juntamente com a nova criação assistida por IA em jornadas e conteúdo, o suporte à Decisão expandido para o canal de Correspondência direta e controles adicionais de segurança e administração. Os recursos e as melhorias abaixo são organizados por tema. Alterações adicionais também são esperadas nos próximos dias ou semanas.

### Jornadas {#june-26-journeys}

Os recursos e melhorias a seguir foram adicionados às jornadas nesta versão. Alterações adicionais também são esperadas nos próximos dias ou semanas.


<table>
<thead>
<tr>
<th><strong>Simulação de jornada (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode definir sua jornada como Simulação. Esse modo permite validar a lógica usando usuários simulados. São perfis temporários criados especificamente para a simulação, permitindo que você teste livremente sem precisar gerenciar perfis de teste persistentes na Adobe Experience Platform. </p>
<p>Anteriormente lançada com disponibilidade limitada, a Simulação de jornada agora está disponível para todos os ambientes. Com esta versão de Disponibilidade geral, agora é possível usar o Journey Agent para gerar usuários e eventos simulados diretamente no menu Simulação.</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/simulate-journey-gs.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 9 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Jornada fragmentos (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar <strong>Fragmentos de jornada</strong> no Adobe Journey Optimizer. Os fragmentos de jornada são conjuntos reutilizáveis de nós de jornada que você pode criar uma vez e soltar em qualquer jornada na sandbox. Seja uma verificação de elegibilidade, uma lógica de roteamento de canal preferencial ou uma sequência de boas-vindas, os fragmentos ajudam as equipes a agir mais rápido e a permanecer consistentes, sem reconstruir a mesma lógica do zero todas as vezes.</p>
<p>Depois de criados, os fragmentos são armazenados em um <strong>Inventário de fragmentos</strong> dedicado e podem ser inseridos em qualquer jornada usando a atividade <strong>Fragmentos de jornada</strong>.</p>
<p>Anteriormente disponível em Disponibilidade limitada, esse recurso agora está disponível para todos os clientes. Os fragmentos de jornada também são compatíveis com a <strong>ferramenta Sandbox</strong>, permitindo empacotar e exportar fragmentos em sandboxes.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/journey-fragments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 9 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Otimização do caminho de jornada - Direcionamento (Disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A <strong>atividade Otimizar</strong> agora oferece suporte a <strong>regras de direcionamento</strong> que permitem definir critérios específicos que os clientes devem atender para se qualificarem para um determinado caminho de jornada, com base em segmentos de público-alvo ou atributos de perfil.</p>
<p>Diferentemente da experimentação, em que os clientes são atribuídos a caminhos aleatoriamente, o direcionamento usa uma lógica determinística para garantir que o público-alvo ou perfil do cliente apropriado seja roteado para o caminho desejado.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/path-targeting.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 8 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente de IA para Expressões de jornada (Beta público)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA agora opera no editor de expressão avançado da jornada para converter prompts de linguagem natural em expressões válidas e lógica condicional. Descreva a expressão que deseja criar e o Assistente de IA gera um código pronto para uso que pode ser aplicado imediatamente ou refinado por meio de prompts complementares.</p>
<p>Esse recurso está disponível para todos os clientes como versão Beta pública.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/expression/expression-agent.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de junho de 2026</p> 
</td>
</tr>
</tbody>
</table>

* **Compatibilidade com identificador complementar para públicos-alvo externos**: agora, para públicos-alvo externos, os identificadores complementares são permitidos nas jornadas, incluindo públicos-alvo importados de um arquivo CSV e públicos-alvo criados com a composição de público-alvo federado. Você pode designar como identificador complementar qualquer atributo do público-alvo que não seja de identidade ou atributo de identidade que não seja de pessoa. Não é necessário rótulo de esquema. [Leia mais](../building-journeys/supplemental-identifier.md)

  Data de disponibilidade: 11 de junho de 2026

* **Interrupção automática para jornadas de Leitura de Público não recorrentes** - **Leitura de Público** Não recorrentes agora as jornadas fazem a transição automática para o status **Interrompido** quando o último perfil ativo existe. Anteriormente, essas jornadas permaneciam com status **Ativo** até que o tempo-limite global de 91 dias expirasse — mesmo sem nenhum fluxo de perfis. Com essa melhoria, o status da jornada reflete o estado de execução real assim que é concluída, mantendo o inventário da jornada preciso sem intervenção manual.

  Observe que esse comportamento não se aplica a jornadas que incluem nós que causam períodos de espera, como nós de espera, nós de reação ou transições acionadas por evento. Essas jornadas permanecem sujeitas ao tempo-limite global padrão de 91 dias. [Saiba mais](../building-journeys/end-journey.md#auto-stop-non-recurring)

  Data de disponibilidade: 9 de junho de 2026

* **Autenticação personalizada baseada em certificado em ações personalizadas**: agora as ações personalizadas permitem autenticação personalizada baseada em certificado. Ao adicionar `subType: "certificateCredential"` a uma configuração de autorização personalizada, o Journey Optimizer usa o certificado gerenciado da Adobe para assinar uma declaração de cliente JWT e trocá-la por um token de acesso — não é necessário nenhum segredo de cliente. Projetado para APIs empresariais que impõem a verificação de identidade baseada em certificados, como o Microsoft Entra ID. [Saiba mais](../datasource/external-data-sources.md#certificate-credential)

  Data de disponibilidade: 4 de junho de 2026

### Campanhas orquestradas {#june-26-oc}

Os seguintes recursos e melhorias estão chegando às campanhas orquestradas nesta versão.

+++ Em breve — **As informações abaixo estão sujeitas a alterações.**

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
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p> Data de disponibilidade: 30 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Personalização baseada em loop para dados relacionais** - O editor de personalização agora oferece suporte a um Bloco de loop que repete coleções relacionais, como pedidos, contas ou reservas, e renderiza um bloco de conteúdo por registro em um único email ou SMS. As coleções são configuradas por meio do seletor de dados usando tokens de personalização, sem a necessidade de gravação de expressão. [Leia mais](../orchestrated/add-personalization.md#enrichment-collections)

  Data de disponibilidade: final de junho de 2026

+++

### Tomada de decisão {#june-26-decisioning}

Os recursos e melhorias a seguir foram adicionados ao Decisioning nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte ao Serviço de decisão no canal de correspondência direta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar políticas de decisão em jornadas e campanhas de correspondência direta. As políticas de decisão são containers de ofertas que utilizam o mecanismo do Serviço de decisão para retornar dinamicamente o melhor conteúdo a cada membro do público-alvo. A decisão por correspondência direta também é compatível com casos de uso de decisão em lote, permitindo exportar os itens de oferta correspondentes para cada perfil em um determinado público-alvo da Adobe Experience Platform. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/use-decision-policy.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Em breve — **As informações abaixo estão sujeitas a alterações.**

* **Atributos de item dinâmico** - Os atributos personalizados de item de decisão agora podem ser personalizados no momento da entrega usando dados de perfil, contextuais e de público-alvo. Isso elimina a necessidade de manter ofertas duplicadas para variações de conteúdo secundárias, permitindo que os profissionais de marketing gerenciem um número menor de itens de decisão e mais flexíveis.

+++

### Gerenciamento de conteúdo {#june-26-content}

Os seguintes recursos e melhorias foram adicionados ao gerenciamento de conteúdo nesta versão.

<table>
<thead>
<tr>
<th><strong>Simular variações de conteúdo — experiência atualizada e geração de variantes de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Duas atualizações estão disponíveis para o fluxo de trabalho <strong>Simular conteúdo</strong>:</p>
<ul>
<li><strong>Novo caminho padrão</strong> — Clicar em <strong>Simular conteúdo</strong> agora abre a experiência <strong>Simular variações de conteúdo</strong> por padrão. Em uma única tela, é possível adicionar entradas de amostra manualmente ou de um arquivo CSV/JSON, reutilizar usuários simulados, pré-visualizar renderização e enviar provas. Para visualizar com perfis de teste do Adobe Experience Platform, envie provas com dados de perfil de teste ou verifique a renderização da caixa de entrada de email e relatórios de spam, clique em <strong>Simular conteúdo</strong> e selecione <strong>Simular conteúdo (perfis do AEP)</strong> na lista suspensa.</li>
<li><strong>Variantes de conteúdo geradas por IA</strong> — Na experiência <strong>Simular variações de conteúdo</strong>, clique em <strong>Gerar</strong> para usar a IA para criar variantes de conteúdo automaticamente. O sistema analisa a mensagem, detecta campos de personalização e ramificações condicionais e preenche valores realistas para que você possa validar a renderização sem criar cada variante manualmente.</li>
</ul>
<p>Para obter mais informações, consulte a <a href="../test-approve/simulate-sample-input.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 9 de junho de 2026</p>
</td>
</tr>
</tbody>
</table>

### Canal de email {#june-26-email}

As seguintes melhorias foram adicionadas ao canal de email nesta versão.

* **Criptografia de parâmetros de URL**: agora é possível criptografar parâmetros de URL em links de páginas de destino e rastreamento adicionados às suas mensagens de email. Isso fornece uma camada adicional de segurança para dados de parâmetros confidenciais. Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral). [Leia mais](../personalization/url-parameter-encryption.md)

  Data de disponibilidade: 1º de junho de 2026

* **Novas permissões para o registro de chaves**: agora são necessárias duas novas permissões para acessar e gerenciar as chaves necessárias para a criptografia de parâmetros de URL: **Gerenciar registro de chaves** e **Exibir registro de chaves**. [Leia mais](../administration/high-low-permissions.md#administration-permissions)

  Data de disponibilidade: 1º de junho de 2026

+++ Em breve — **as informações abaixo estão sujeitas a alterações.**

<table>
<thead>
<tr>
<th><strong>Verificações de qualidade de conteúdo no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora inclui validação técnica automatizada diretamente no Designer de email, ajudando você a detectar problemas no HTML e no CSS antes do envio.</p>
<p>As verificações abrangem elementos sem suporte, como tags <code>&lt;script&gt;</code> e <code>&lt;base&gt;</code>, divs vazios que podem quebrar o layout no Microsoft Outlook, tags de metaatualização do HTML e limites de tamanho de CSS ou HTML que acionam falhas de renderização no Gmail.</p>
<p>Os resultados são exibidos como erros, avisos ou avisos informativos diretamente no painel de criação, com detalhes contextuais e correções com um clique, quando disponíveis, para que os problemas possam ser resolvidos sem sair do editor.</p>
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
<p>O Journey Optimizer agora inclui uma opção para reduzir o tamanho do HTML do seu email removendo espaços em branco, comentários e códigos redundantes desnecessários — sem afetar a forma como o email é renderizado.</p>
<p>Isso pode melhorar a capacidade de delivery, evitando limites de tamanho que alguns provedores de email usam para sinalizar ou rejeitar mensagens e pode reduzir o tempo de carregamento dos recipients.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Rich text em campos editáveis para fragmentos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar rich text a fragmentos personalizáveis usados no conteúdo de emails.</p>
<p>Por exemplo, ao usar o componente de Texto como um campo editável no Designer de email, você pode formatar o conteúdo diretamente (por exemplo, negrito e itálico) e inserir hiperlinks.</p>
</td>
</tr>
</tbody>
</table>

+++

### Conteúdo e integrações {#june-26-integration}

Os seguintes recursos e melhorias estão chegando ao gerenciamento de conteúdo e integrações nesta versão.

+++ Em breve — **As informações abaixo estão sujeitas a alterações.**

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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente de IA para melhorias na geração de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esta versão aprimora a experiência de geração de conteúdo do <strong>Assistente de IA</strong> com uma edição de imagens mais forte, extração de marca mais confiável e suporte à autenticidade de conteúdo no fluxo de imagem:</p>
<ul>
<li><strong>A edição de imagens de IA</strong> agora está disponível no fluxo de geração de imagens, incluindo suporte a modelos de terceiros do Firefly, para que você possa refinar as imagens de origem sem sair do assistente.</li>
<li><strong>A extração de sinal da marca</strong> oferece resultados de maior qualidade. Quando as páginas selecionadas não têm sinal suficiente, os fallbacks aprimorados agora preenchem cores, tipografia, diretrizes de escrita e outros atributos da marca.</li>
<li><strong>A extração de marca baseada na Web</strong> é mais confiável. O manuseio aprimorado do tempo limite ajuda a impedir que páginas lentas, pop-ups e banners de cookies bloqueiem a extração.</li>
<li>Agora há suporte para a <strong>Autenticidade de conteúdo (CAI)</strong> no fluxo de imagem. Esta versão também corrige problemas de upload de imagem de referência e melhora o tratamento de imagens sem um manifesto C2PA existente.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### Administração {#june-26-administration}

As seguintes melhorias foram adicionadas à administração e ao gerenciamento de dados nesta versão.

* [!BADGE Importante]{type=Informative} **Conjunto de Dados do Evento de Feedback de Mensagens do AJO migrando para assimilação em lote** - O **Conjunto de Dados do Evento de Feedback de Mensagens do AJO** está migrando da assimilação de streaming para assimilação em lote. Como resultado, espere uma latência de dados de até 2 horas para esse conjunto de dados. Se você tiver criado relatórios no Customer Journey Analytics ou executado consultas usando esse conjunto de dados, considere esse aumento na latência a partir de agora. [Leia mais](../data/datasets-query-examples.md#message-feedback-event-dataset)

  Data de disponibilidade: 10 de junho de 2026

* **Alertas de clientes para eventos de ciclo de vida de campanha**: agora novos alertas do sistema notificam eventos importantes do ciclo de vida para campanhas acionadas por ação e API. Assine no nível da sandbox. [Leia mais](../reports/alerts.md)

  Data de disponibilidade: 1º de junho de 2026

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
