---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 101796a9221beeb1fa4950d806a91997ee6c9ae4
workflow-type: tm+mt
source-wordcount: '2138'
ht-degree: 62%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades?"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.


## Notas de versão antecipadas de junho de 2025 {#25-6-rn}


**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados na data de lançamento.

**Data de lançamento**: 17 a 18 de junho de 2025

Consulte também [Notas de pré-lançamento do Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Novos recursos {#25-06-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.


<table>
<thead>
<tr>
<th><strong>Mensagens RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O envio de mensagens por RCS (Serviços de Comunicação Avançada) agora é suportado no Journey Optimizer, habilitando os seguintes recursos de envio de mensagens aprimorados sujeitos ao suporte do provedor e da operadora:</p>
<ul>
<li>Suporte a remetente marcado e verificado: envie mensagens usando perfis comerciais verificados com elementos de marca (logotipo, nome do remetente etc.).</li>
<li>Insights de delivery de mensagens: receba relatórios de delivery detalhados, incluindo atualizações de status de mensagem (por exemplo, enviado, entregue, lido).</li>
<li>Rastreamento de link: incorpore e rastreie URLs em mensagens do RCS para análise de engajamento.</li>
<li>Fallback para SMS: fallback automático para SMS quando o dispositivo do perfil não dá suporte a RCS ou está temporariamente inacessível via RCS.</li>
<li>Composição básica de mensagem: envia mensagens RCS baseadas em texto com mídia opcional e elementos avançados, dependendo do suporte do provedor.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campos de formulário no conteúdo de experiência baseado em código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir campos editáveis específicos em modelos de conteúdo JSON ou HTML que permitem que usuários não técnicos editem facilmente o conteúdo em uma exibição de formulário na criação do canal de experiência baseado em código, sem a necessidade de manipular qualquer código. Mais do que isso, ao definir os modelos de conteúdo de experiência baseados em código, agora é possível inserir políticas de decisão no modelo, aumentando a reutilização e a facilidade de uso.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Método de delegação personalizado para subdomínios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além da delegação completa e do método CNAME, um novo método de configuração de subdomínio está disponível: o método de delegação Personalizado, que permite controlar e manter totalmente todos os aspectos do DNS necessários para entregar, renderizar e rastrear mensagens.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Atividade do Content Decisioning no jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível incluir ofertas personalizadas em suas jornadas por meio de uma atividade dedicada de Decisão de conteúdo na tela de jornada e usá-las em atividades de jornada, incluindo condições e ações personalizadas.</p>
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Execução de prática da jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Jornada Dry run é um modo de publicação de jornada especial no Adobe Journey Optimizer que permite que os profissionais de jornada testem uma jornada usando dados de produção reais sem entrar em contato com clientes reais ou atualizar informações de perfil. Esse recurso ajuda os profissionais de jornada a ganhar confiança no design da jornada e no direcionamento de público-alvo antes de publicá-la ao vivo.</p>
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Pausar e retomar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode pausar e retomar suas jornadas. Esse recurso oferece aos profissionais de jornadas maior controle e flexibilidade, permitindo que as jornadas ativas sejam temporariamente suspensas sem interromper a experiência do cliente. Quando pausada, nenhuma comunicação é enviada e os perfis permanecem em um estado suspenso até que a jornada seja retomada.</p>
<p>Você pode pausar e retomar apenas uma jornada ou executar operações de pausa e retomada em massa para um grupo de jornadas.</p>
<p>Além disso, é possível aplicar filtros globais a jornadas pausadas para excluir perfis com base em seus atributos.</p>
<p>Esse recurso só está disponível para um conjunto de organizações (disponibilidade limitada) e será lançado globalmente em uma versão futura.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dimensionar o vencedor do experimento</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dimensione o vencedor da experimentação para implantar automática ou manualmente a variação vencedora de um experimento em todo o público-alvo. Esse recurso garante que, após identificar o melhor desempenho, seja possível maximizar seu alcance e eficácia sem necessidade de supervisão manual constante.</p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-experiment.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 2 de junho de 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflito e priorização</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No Journey Optimizer, gerenciar o volume e o momento de início das campanhas e jornadas é essencial para não sobrecarregar clientes com muitas interações. O Journey Optimizer agora oferece várias ferramentas para o gerenciamento de conflitos e a priorização, antes disponíveis apenas para um número limitado de organizações (disponibilidade limitada), mas que agora estão em disponibilidade geral.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Esta versão de disponibilidade geral também inclui os seguintes aprimoramentos:</p>
<ul>
<li>Suporte estendido: as ferramentas de gerenciamento de conflitos agora oferecem suporte às jornadas unitárias, jornadas de qualificação de público-alvo e jornadas de público-alvo de leitura.</li>
<li>Solução de problemas aprimorada: agora há dois novos campos de evento de etapa disponíveis no serviço de consulta, permitindo analisar por que um perfil foi rejeitado de uma jornada ou campanha.</li>
<li>Relatórios aprimorados: os relatórios agora indicam qual regra específica excluiu um perfil de uma jornada ou campanha, fornecendo maior transparência e insights acionáveis.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 3 de junho de 2025</p>
</td>
</tr>
</tbody>
</table>


### Aprimoramentos {#25-06-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.

* **Conjuntos de regras de canal**

   * **Janela de duração personalizada** para limitação - Um novo campo **Contagem de Repetição** está disponível na tela de configuração de conjuntos de regras de canal, permitindo que você aplique regras de limitação de frequência em vários dias, semanas ou meses, dependendo da duração especificada.

   * **Duração por hora** - Agora é possível aplicar o limite de hora em hora para conjuntos de regras de canal.

* **Experiências baseadas em código**

  As políticas de decisão agora estão disponíveis em modelos de conteúdo de experiência baseados em código e no painel direito do editor de código.

* **Designer de email**

   * **Suporte a CSS personalizado** - o Journey Optimizer agora permite que você adicione CSS personalizado ao seu conteúdo de email diretamente no Designer de email.
   * **Suporte para o modo escuro** - O designer de email do Journey Optimizer agora oferece a capacidade de alternar para o modo escuro, onde é possível definir configurações específicas.


* **Decisão** - Data de disponibilidade: 3 de junho de 2025

  Os objetos de decisão agora podem ser copiados entre sandboxes, simplificando os fluxos de trabalho de teste e implantação. [Leia mais](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Suporte a atributos de item de decisão para regras de decisão** - Data de disponibilidade: 4 de junho de 2025

  Agora você pode aproveitar os atributos de item de decisão para criar regras de decisão. [Leia mais](../experience-decisioning/rules.md#create)

* **Atualização da API de execução de mensagem interativa** - Data de disponibilidade: 6 de junho de 2025

  A API de execução de mensagem interativa agora permite excluir a programação da execução de campanhas futuras. [Leia mais](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}

## Notas de versão de maio de 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Novos recursos {#25-05-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Exibição de calendário para inventários de campanha e jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora há uma exibição de calendário disponível nas listas de jornadas e campanhas. Ela permite ver todas as ativações de jornadas e campanhas nas respectivas listas.</p>
<p>No momento, essa alteração está disponível apenas para algumas organizações (disponibilidade limitada). Para solicitar acesso, use <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">este formulário</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Para obter mais informações, consulte estas seções: <a href="../building-journeys/journey-ui.md">Procurar e filtrar suas jornadas</a>, <a href="../campaigns/modify-stop-campaign.md">Acessar campanhas</a>.</p>
<p>Data de disponibilidade: quinta-feira, 28 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração de fragmentos de conteúdo do Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a integração do Adobe Experience Manager e do Adobe Journey Optimizer, agora é possível usar com facilidade os fragmentos de conteúdo do Adobe Experience Manager no conteúdo do Journey Optimizer. Essa conexão perfeita facilita o acesso e o uso do conteúdo do AEM diretamente no Journey Optimizer.</p>
<p>Anteriormente disponível para um conjunto limitado de organizações (DL), esse recurso agora está disponível para o público geral com o seguinte aprimoramento: agora é possível definir espaços reservados e mapear valores de personalização na assinatura do fragmento usando o modo Editor.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Para obter mais informações, consulte a <a href="../integrations/aem-fragments.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Integração do Dynamic Media com o Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os ativos do Dynamic Media agora estão diretamente disponíveis e acessíveis no Journey Optimizer. Essa integração permite:</p>
<ul>
<li>Gerenciar ativos centralmente com atualizações em tempo real.</li>
<li>Modificar instantaneamente suas configurações de ativos, como largura e altura.</li>
<li>Personalizar modelos do Dynamic Media atualizando o conteúdo e adicionando campos de personalização.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Para obter mais informações, consulte a <a href="../integrations/aem-dynamic.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID complementar para jornadas acionadas por eventos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar jornadas usando uma ID de perfil juntamente com outro identificador, como uma ID de pedido, ID de assinatura ou ID de prescrição, permitindo que o mesmo perfil esteja na mesma jornada várias vezes ao mesmo tempo. Isso possibilita cenários como o gerenciamento de vários pedidos ou assinaturas em paralelo, com cada instância seguindo seu próprio caminho pela jornada.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/supplemental-identifier.md">documentação detalhada</a>.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simular variações de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes. Com esta versão de disponibilidade geral, o recurso agora inclui suporte para conteúdo multilíngue e experimentos de conteúdo, permitindo testar variações em diferentes idiomas e tratamentos. Além disso, agora ele é compatível com atributos contextuais (além dos atributos de perfil), permitindo testes de conteúdo ainda mais dinâmicos e específicos.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Para obter mais informações, consulte a <a href="../test-approve/simulate-sample-input.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 23 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Sincronizar a programação do público-alvo de leitura com o trabalho de segmentação em lote</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível acionar execuções diárias da jornada após a conclusão da segmentação em lote Essa opção agora está disponível em jornadas agendadas diariamente para todos os clientes. Ela permite definir uma janela de tempo de até 6 horas para aguardar os dados de público-alvo de trabalhos de segmentação em lote, garantindo que as jornadas sejam executadas com os dados mais atualizados ou sejam ignoradas, se não estiverem prontas. </p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Para obter mais informações, consulte a <a href="../building-journeys/read-audience.md#schedule">documentação detalhada</a>.</p>
<p>Data de disponibilidade: quarta-feira, 20 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Provedor de SMS personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite configurar provedores de SMS adicionais além das opções padrão: Sinch, Infobip e Twilio. Com a configuração personalizada do provedor SMS, é possível integrar diretamente provedores de terceiros, aproveitar a personalização avançada de conteúdo para gerar mensagens dinâmicas e gerenciar preferências de consentimento (aceitação e recusa) para garantir a conformidade.</p>
<p>Para obter mais informações, consulte a <a href="../sms/sms-configuration-custom.md">documentação detalhada</a>.</p>
<p>Anteriormente lançado com disponibilidade limitada, esse recurso agora está disponível para todos os ambientes (disponibilidade geral).</p>
<p>Data de disponibilidade: quarta-feira, 20 de maio de 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível aplicar temas pré-aprovados rapidamente para garantir a consistência da marca em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de forma independente, reduzindo a dependência de equipes de design.</p>
<p>No momento, esse recurso está na versão beta e disponível apenas para clientes beta. Para participar do programa beta, entre em contato com seu representante da Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para obter mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 14 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisão - Novo construtor de fórmulas de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível criar fórmulas de classificação de decisão específicas por definir e combinar critérios a partir de uma interface nova e aprimorada. Em vez de contar apenas com uma prioridade de oferta estática, é possível definir fórmulas de classificação personalizadas que combinam pontuações do modelo de IA, prioridades de oferta, atributos de perfil, atributos de oferta e sinais contextuais por meio de uma interface guiada.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/exd-ranking-formulas.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 14 de maio de 2025</p>
</td>
</tr>
</tbody>
</table>

### Aprimoramentos {#25-05-improv}

Os aprimoramentos incluídos nesta versão estão listados abaixo.


* **Suporte a novos objetos de campanha para cópia da sandbox** - Data de disponibilidade: 15 de maio de 2025

  Ao copiar campanhas em várias sandboxes usando os recursos de exportação e importação de pacotes, as seguintes dependências agora também são copiadas: configurações de canal, variantes e configurações de experimento, políticas e itens de decisão. [Leia mais](../configuration/copy-objects-to-sandbox.md)

* **Pastas para páginas de destino** - Data de disponibilidade: 9 de maio de 2025

  Para gerenciar facilmente as páginas de destino, agora é possível usar pastas para organizá-las com mais eficiência em uma hierarquia estruturada. [Leia mais](../landing-pages/manage-lp.md)

* **Correspondência direta: suporte à chave SSH para conexões SFTP** - Data de disponibilidade: 5 de maio de 2025

  Na configuração de roteamento do arquivo de correspondência direta, além do SFTP existente com autenticação por senha, agora é possível exportar o arquivo de correspondência direta para um servidor SFTP com autenticação por chave SSH. [Leia mais](../direct-mail/direct-mail-configuration.md)

* **Ativação de pílulas para personalização** - Data de disponibilidade: 5 de maio de 2025

  Um novo botão “Pílulas” foi adicionado ao editor de personalização. Quando habilitado, os atributos contextuais e de perfil são exibidos como pílulas, melhorando a legibilidade do código. [Leia mais](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Esse recurso será implantado gradualmente em todos os ambientes nos próximos 30 dias.

* Suporte a &#39;Redirecionar para URL&#39; do **no canal da Web** - Data de disponibilidade: 20 de maio de 2025

  O canal da web do Journey Optimizer agora permite redirecionar visitantes para outro URL existente, em vez de criar uma nova variação no editor visual. Esse recurso pode ser usado para realizar experimentos comparando duas páginas completamente diferentes, em vez de apenas alterar alguns elementos em uma página. [Leia mais](../web/create-web.md#web-redirect-to-url)

* **Pastas para modelos e fragmentos** - Data de disponibilidade: 20 de maio de 2025

  As pastas permitem organizar objetos com mais facilidade e eficácia, usando uma hierarquia estruturada. Anteriormente disponíveis para apenas algumas organizações (disponibilidade limitada), as pastas agora estão disponíveis para todos os usuários (disponibilidade geral), permitindo o gerenciamento de modelos e fragmentos de conteúdo. Saiba mais nas seções [Modelos de conteúdo](../content-management/access-content-templates.md#folders) e [Fragmentos](../content-management/manage-fragments.md#folders).

* **Rastreamento de cliques em modelos de email** - Data de disponibilidade: 20 de maio de 2025

  O rastreamento de cliques em elementos `<area>` nos mapas de imagem de conteúdos de email agora é um recurso nativo do [!DNL Journey Optimizer]. Isso visa garantir que as áreas do mapa de imagem recebam o mesmo tratamento de rastreamento que os hiperlinks padrão, o que envolve a inclusão de códigos, dados e parâmetros de rastreamento. [Saiba mais sobre o rastreamento de mensagens](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Painel direito na lista de campanhas** - Data de disponibilidade: 20 de maio de 2025

  Agora, selecionar uma campanha na lista abre um painel que exibe seus detalhes.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

