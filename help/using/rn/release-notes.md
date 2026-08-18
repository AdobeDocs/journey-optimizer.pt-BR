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
source-git-commit: 8e72cd3a4172a96eadbb9918bf44156324e592ad
workflow-type: tm+mt
source-wordcount: 1386
ht-degree: 25%

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

## Notas de versão de agosto de 2026 {#aug-26-updates}

<!--
### Loyalty {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Loyalty Insights skill</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer introduces <strong>Loyalty Insights</strong>, a new CX Coworker skill for asking questions about challenge performance and other loyalty program data ingested into the Loyalty field groups in Adobe Experience Platform.</p>
<p>For more information, refer to the <a href="../start/ajo-coworker-skills.md">detailed documentation</a>.</p>
<p>Availability date: August 12, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

### Gerenciamento de conteúdo

Os seguintes recursos e melhorias foram introduzidos ao Gerenciamento de conteúdo nesta versão.

<table>
<thead>
<tr>
<th><strong>Origem flexível de imagens para a geração de conteúdo de IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gerar conteúdo no Journey Optimizer agora origina imagens aprovadas pela marca diretamente do Adobe Experience Manager Assets Essentials e superior. Três modos controlam o equilíbrio: Balanceado (Gerenciamento de ativos digitais - primeiro, IA preenche lacunas, padrão), Assets (Gerenciamento de ativos digitais - originado) e Creative (AI).</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>Para obter mais informações, consulte a <a href="../content-management/generative-uc.md#image-mode">documentação detalhada</a>.</p>
<p> Data de disponibilidade: 5 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

### Jornadas {#aug-26-journeys}

* **Novas funções de lista no editor de expressão avançado** - Duas novas funções estão disponíveis no editor de expressão avançado: `mergeLists` combina duas listas, com ou sem eliminação de duplicação, e `differenceLists` retorna os itens de uma lista que não estão presentes em outra. [Saiba mais](../building-journeys/functions/list-functions.md)

  Data de disponibilidade: 13 de agosto de 2026

* **Otimização de Tempo de Envio na atividade de Espera** - A Otimização de Tempo de Envio agora está disponível na atividade de Espera, permitindo que a IA da Adobe determine o momento ideal para continuar com qualquer atividade de downstream. [Saiba mais](../building-journeys/wait-activity.md#sto-wait)

  Data de disponibilidade: 13 de agosto de 2026

### Campanhas {#aug-26-campaigns}

Os recursos e melhorias a seguir foram introduzidos nas Campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Anexos personalizados do PDF em emails acionados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora oferece suporte a até <b>cinco anexos do PDF</b> no total por email em campanhas acionadas por API, incluindo PDFs estáticos e específicos de destinatários. Os arquivos PDF específicos do recipient são buscados com segurança da Data Landing Zone e anexados no momento do envio, com o local de cada arquivo transmitido diretamente na carga da API. Isso permite que os sistemas de geração de documentos upstream existentes permaneçam em vigor, com o Journey Optimizer lidando com a entrega.</p>
<p>Os casos de uso suportados incluem faturas, demonstrativos, tíquetes, contratos, etiquetas de remessa e documentos semelhantes que variam de acordo com o recipient. Os anexos personalizados do PDF estão disponíveis somente para campanhas de email transacionais acionadas por API e não são compatíveis com jornadas ou campanhas orquestradas.</p>
<p>Volumes e tamanhos de anexo maiores são suportados por meio do complemento de anexo do PDF; para obter mais informações, entre em contato com o representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../email/pdf-attachments.md#personalized-attachments">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Assinaturas de alerta de ciclo de vida por campanha** - Agora é possível assinar alertas de ciclo de vida de campanha com suporte para uma única campanha, além da assinatura em nível de sandbox existente. Isso permite monitorar campanhas individuais de alta prioridade sem receber o mesmo alerta para cada campanha na sandbox. [Saiba mais](../reports/alerts.md#subscribe-alerts)
Data de disponibilidade: 13 de agosto de 2026

### Campanhas orquestradas {#august-26-oc}

Os recursos e melhorias a seguir foram introduzidos nas Campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte para o Quiet Hours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar o Período de Silêncio. O Quiet Hours permite definir exclusões com base no tempo para evitar que as mensagens sejam enviadas durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade em casos de uso da orquestração de campanha.</p>
<p>Para obter mais informações, consulte a <a href="../conflict-prioritization/quiet-hours.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envio usando ondas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode programar mensagens de saída para serem entregues em lotes controlados ao longo do tempo. Ideal para campanhas de alto volume ou sensíveis ao tempo, o envio de ondas também oferece suporte a uma melhor capacidade de entrega e ajuda a manter uma sólida reputação do remetente, reduzindo o risco de ser sinalizado como spam. </p>
<p>Para obter mais informações, consulte a <a href="../delivery/send-using-waves.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 18 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte ao canal LINE (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível adicionar ações LINE nas campanhas orquestradas. Essa nova atividade permite criar e fornecer conteúdo altamente personalizado, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens avançadas do Flex, para envolver seus clientes perfeitamente na plataforma LINE. Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../orchestrated/activities/channels.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 12 de agosto de 2026</p>
</td>
</tr>
</tbody>
</table>

* **Capacidade de Gerenciar Dimensões de Destino do Perfil** - Agora é possível excluir um Dimension de Destino do Perfil ou editar e trocar seu namespace de identidade configurado, fornecendo maior controle e flexibilidade sobre as configurações de dados. [Saiba mais](../orchestrated/target-dimension.md)

  Data de disponibilidade: 18 de agosto de 2026

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizar detalhes do remetente de email por destinatário e campanha (Disponibilidade limitada)** - As campanhas orquestradas agora oferecem suporte à personalização de campos de cabeçalho de email, incluindo Nome de origem, Prefixo de email de origem, Nome de resposta e Email de resposta, bem como endereço de execução, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o consultor, o local ou a filial relevante para cada destinatário, em vez de encaminhar todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso. [Saiba mais](../orchestrated/activities/channels.md#configuration)

  Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada).

  Data de disponibilidade: 18 de agosto de 2026

* **Simplificação da dimensão de público-alvo** - A dimensão de público-alvo ativa agora é mostrada na tela do fluxo de trabalho, para que você possa ver qual dimensão é usada por uma atividade de canal. O fluxo de segmentação de várias entidades é mais simples, pois você não precisa mais de uma atividade &quot;Alterar dimensão&quot; separada. Além disso, agora você pode escolher explicitamente se as mensagens são enviadas no nível do perfil ou em um nível de dimensão secundário. [Saiba mais](../orchestrated/activities/channels.md#add)

  Data de disponibilidade: 18 de agosto de 2026

### Canais {#august-26-channels}

* **Complemento de desempenho para taxa de transferência - Push** - Um novo modo de mensagens transacionais de alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real de grande escala e aceita até 5.000 transações por segundo com maior disponibilidade. Anteriormente disponível apenas para o canal de email, esse recurso agora também está disponível para o canal de push, para organizações que compraram a oferta complementar de Mensagens transacionais de alta capacidade da Adobe. Entre em contato com o representante da Adobe para obter mais informações. [Saiba mais](../campaigns/api-triggered-high-throughput.md)

  Data de disponibilidade: 11 de agosto de 2026

### Melhorias de usabilidade {#august-26-usability}

* **Operações em massa no inventário de jornadas** - Agora é possível executar novas ações em massa diretamente da lista de inventário de jornadas, agilizando o gerenciamento de várias jornadas de uma só vez. Selecione várias jornadas e aplique qualquer uma destas novas ações em uma única etapa: **adicionar ao pacote**, **excluir**, **mover para a pasta**, **editar marcas** ou **gerenciar acesso**. Isso reduz a necessidade de repetir a mesma ação uma jornada por vez, simplificando o gerenciamento de jornadas para equipes que trabalham com um grande número de jornadas. [Saiba mais](../building-journeys/journey-ui.md)

  Data de disponibilidade: 12 de agosto de 2026

* **Nova experiência de Simulação de Conteúdo para testes de conteúdo** - O fluxo de trabalho **Simular conteúdo** apresenta uma experiência reprojetada: todas as variantes agora são renderizadas juntas em uma única grade rolável (lado a lado, empilhadas ou com layouts dispostos), substituindo o modo de exibição uma variante de cada vez. Uma única barra de ação inferior consolida a navegação entre variantes de teste, o zoom, a alternância de visor (desktop/celular), a alternância de local, a adição de entradas de amostra, a geração de variantes com IA, a escolha e o salvamento de usuários simulados e a importação ou exportação de variantes. Remover o painel esquerdo e recolher camadas de cabeçalho extras oferece visualizações com muito mais espaço. A opção **Alternar para experiência clássica** na barra de ação inferior permite reverter para a experiência anterior a qualquer momento. [Saiba mais](../test-approve/simulate-content-variations.md)

  Data de disponibilidade: 11 de agosto de 2026

* **Várias seleções na nova tela de jornada** - A nova experiência de tela de jornada apresenta uma seleção simplificada de vários nós: mantenha a tecla Shift pressionada e arraste para selecionar vários nós de uma só vez, em vez de selecioná-los individualmente. Isso permite que ações em massa, como copiar, excluir ou salvar como um fragmento de jornada, sejam executadas com eficiência em vários nós. [Saiba mais](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  Data de disponibilidade: 17 de agosto de 2026

### Tomada de decisão {#decisioning-august}

* **Mirror pages em fragmentos visuais** - Agora é possível inserir mirror pages em um fragmento visual. Os atributos de decisão são renderizados corretamente no link da mirror page, mesmo quando o fragmento é usado em uma campanha de email que usa a Decisão. A mirror page deve ser adicionada ao fragmento visual antes de o fragmento ser publicado para que os atributos de decisão sejam exibidos.

  Data de disponibilidade: 11 de agosto de 2026

  [Saiba mais](../email/message-tracking.md#decisioning-mirror-page)