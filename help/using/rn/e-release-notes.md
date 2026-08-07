---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: fcf7ea6d5d6ceaa02490e8cbaf807b9f670c63cc
workflow-type: tm+mt
source-wordcount: 2157
ht-degree: 20%

---


# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de agosto de 2026 {#august-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas poderão ser implantadas posteriormente.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 18 a 19 de agosto de 2026

### Integração {#august-26-onboarding}

O recurso a seguir foi adicionado à integração nesta versão.

<table>
<thead>
<tr>
<th><strong>Recursos guiados para integração de emails e jornadas (disponibilidade geral)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A transição para o Adobe Journey Optimizer a partir de outra plataforma de marketing é mais fácil com recursos guiados que ajudam a mover o conteúdo e as jornadas de email existentes para o Journey Optimizer. Um espaço de trabalho dedicado permite reutilizar o que você tem, em vez de reconstruir do zero.</p>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Jornadas {#august-26-journeys}

Os recursos e melhorias a seguir foram adicionados às jornadas nesta versão.

<table>
<thead>
<tr>
<th><strong>controle em nível de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar um grupo de controle para suas jornadas diretamente das propriedades do jornada. Uma validação é uma porcentagem configurável do público-alvo que é excluído da entrada na jornada e não recebe nenhuma comunicação. Ao comparar perfis de controle com perfis ativos nos relatórios do Customer Journey Analytics, é possível medir o aumento incremental - o impacto real - que a jornada oferece.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15162">DOCAC-15162</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Adicionar nova função dateDiff no editor de expressão de jornada** - O editor de expressão de jornada agora inclui a função `dateDiff`, que calcula a diferença entre duas datas em número de dias. Essa função é útil para uma lógica baseada no tempo, como criar prazos, calcular durações de ciclo de vida do cliente ou criar cronômetros de contagem regressiva em condições de jornada. <a href="https://jira.corp.adobe.com/browse/DOCAC-15293">DOCAC-15293</a> <!-- Documentation link: TBD -->

* **Datas de início e término no cabeçalho da jornada** - Quando as datas de início e/ou término são configuradas em uma jornada, elas agora são exibidas no cabeçalho da jornada ao lado da notificação de status. O rótulo exibido se adapta com base no fato de cada data ser futura ou já ter passado. <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">DOCAC-14702</a> <!-- Documentation link: TBD -->

### Campanhas {#august-26-camp}

Os recursos e melhorias a seguir foram adicionados às campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Simulação de experiência de entrada em campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível simular ações de canal de entrada em Campanhas de ação antes de entrar em atividade. Use o modo de simulação para testar sua configuração com usuários simulados e visualizar a experiência renderizada, incluindo um URL gerado e um código QR, para que você possa validar regras, decisões e renderização de conteúdo de ponta a ponta.</p>
<p>No momento, esse recurso está em beta privado e disponível para um conjunto limitado de organizações. Entre em contato com o representante da Adobe para obter mais informações.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Pastas para Campanhas** - Agora você pode organizar suas campanhas em pastas para melhorar a navegação e o gerenciamento na interface. <a href="https://jira.corp.adobe.com/browse/DOCAC-15098">DOCAC-15098</a> <!-- Documentation link: TBD -->

* **Pontuação de alinhamento da marca no painel do Campaign**: agora é possível avaliar a pontuação de alinhamento da marca diretamente no painel do Campaign para garantir que o conteúdo permaneça consistente com a marca. Isso permite verificar as diretrizes rapidamente sem precisar abrir o designer de conteúdo. <a href="https://jira.corp.adobe.com/browse/DOCAC-14516">DOCAC-14516</a> <!-- Documentation link: TBD -->

* **Substituir o campo de execução padrão em campanhas**: agora é possível substituir o campo de execução padrão definido globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da campanha, possibilidade que antes estava disponível no nível de jornada. <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">DOCAC-14718</a> <!-- Documentation link: TBD -->

### Campanhas orquestradas {#august-26-oc}

Os recursos e melhorias a seguir foram adicionados às campanhas orquestradas nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte Quiet Hours para campanhas orquestradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar horas de silêncio a campanhas orquestradas. As horas de silêncio permitem definir exclusões com base no tempo para evitar que as mensagens sejam enviadas durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade em casos de uso de orquestração de campanha.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Capacidade de Gerenciar Dimensões de Destino do Perfil** - Agora é possível excluir um Dimension de Destino do Perfil ou editar e trocar seu namespace de identidade configurado, fornecendo maior controle e flexibilidade sobre as configurações de dados. <a href="https://jira.corp.adobe.com/browse/DOCAC-15018">DOCAC-15018</a> <!-- Documentation link: TBD -->

* **Suporte para Line (Disponibilidade Limitada)** - Agora é possível adicionar ações LINE diretamente às suas campanhas Orquestradas. Essa nova atividade permite criar e fornecer conteúdo altamente personalizado, incluindo texto, adesivos, imagens, vídeos, dados de localização e mensagens avançadas do Flex, para envolver seus clientes perfeitamente na plataforma LINE. Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe. <a href="https://jira.corp.adobe.com/browse/DOCAC-14905">DOCAC-14905</a> <!-- Documentation link: TBD -->

* **Novas APIs públicas de campanhas orquestradas** - Novas especificações de API agora estão disponíveis para campanhas orquestradas. Essas APIs permitem criar, gerenciar e acionar campanhas orquestradas de forma programática, permitindo uma integração mais profunda com sistemas externos e pipelines de automação. <a href="https://jira.corp.adobe.com/browse/DOCAC-14308">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **Personalizar detalhes do remetente de email por destinatário e campanha** - As campanhas orquestradas agora oferecem suporte à personalização de campos de cabeçalho de email, incluindo Nome do remetente, Endereço do remetente e Responder para, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o consultor, o local ou a filial relevante para cada destinatário, em vez de encaminhar todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso. <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">DOCAC-13761</a> <!-- Documentation link: TBD -->

* **Simplificação da dimensão de público alvo em campanhas orquestradas** - A dimensão de direcionamento ativa agora é mostrada na tela do fluxo de trabalho, para que você possa ver qual dimensão é usada por uma atividade de canal. O fluxo de segmentação de várias entidades é mais simples, pois você não precisa mais de uma atividade &quot;Alterar dimensão&quot; separada. Além disso, agora você pode escolher explicitamente se as mensagens são enviadas no nível do perfil ou em um nível de dimensão secundário. <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">DOCAC-13554</a> <!-- Documentation link: TBD -->

* **Enviar usando ondas em campanhas orquestradas** - Agora é possível agendar mensagens de saída de campanhas orquestradas para serem entregues em lotes controlados ao longo do tempo. Ideal para campanhas de alto volume ou sensíveis ao tempo, o envio de ondas também oferece suporte a uma melhor capacidade de entrega e ajuda a manter uma sólida reputação do remetente, reduzindo o risco de ser sinalizado como spam. <a href="https://jira.corp.adobe.com/browse/DOCAC-13990">DOCAC-13990</a> <!-- Documentation link: TBD -->

### Canais {#august-26-channels}

Os seguintes recursos e melhorias foram adicionados aos canais nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal da Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A decisão agora está disponível para o canal da Web. Você pode usar políticas de decisão diretamente no editor visual da Web para fornecer as ofertas mais relevantes a cada visitante.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anexos personalizados do PDF em emails acionados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora é compatível com a anexação de até cinco PDFs específicos do recipient por email em campanhas acionadas por API. Os arquivos do PDF são obtidos com segurança da Data Landing Zone e anexados no momento do envio, com o local de cada arquivo transmitido diretamente na carga da API. Isso permite que os sistemas de geração de documentos upstream existentes permaneçam em vigor, com o Journey Optimizer lidando com a entrega.</p>
<p>Os casos de uso suportados incluem faturas, demonstrativos, tíquetes, contratos, etiquetas de remessa e documentos semelhantes que variam de acordo com o recipient. Os anexos personalizados do PDF estão disponíveis somente em campanhas acionadas por API e não são compatíveis com jornadas ou campanhas orquestradas.</p>
<p>Volumes e tamanhos de anexo maiores são suportados por meio do complemento de anexo do PDF; para obter mais informações, entre em contato com o representante da Adobe.</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Canal LINE - alterações de criação**: a interface do canal LINE foi atualizada com recursos avançados de criação de mensagens. Essa versão apresenta suporte para vários formatos de mensagem, incluindo Texto, Imagem, Imagemap, Carrossel e Flex (Editor JSON), juntamente com visualizações de dispositivos em tempo real. Os usuários agora podem gerenciar mensagens agrupadas com até cinco mensagens ordenadas (com controles para adicionar, remover e reordenar) e aproveitar o editor de personalização integrado para criar mensagens dinâmicas e validadas. <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">DOCAC-14869</a> <!-- Documentation link: TBD -->

* **Complemento de desempenho para taxa de transferência - Push** - Um novo modo de mensagens transacionais de alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real de grande escala e aceita até 5.000 transações por segundo com maior disponibilidade. Anteriormente disponível apenas para o canal de email, esse recurso agora também está disponível para o canal de push, para organizações que compraram a oferta complementar de Mensagens transacionais de alta capacidade da Adobe. Entre em contato com o representante da Adobe para obter mais informações. <a href="https://jira.corp.adobe.com/browse/DOCAC-14717">DOCAC-14717</a> <!-- Documentation link: TBD -->

### Tomada de decisão {#august-26-decisioning}

As seguintes melhorias foram adicionadas à Decisão nesta versão.

* **Limite de frequência no nível de posicionamento na Decisão** - As regras de limite de frequência na Decisão agora podem ser segmentadas para posicionamentos individuais, fornecendo controle mais fino sobre a frequência com que uma oferta é exibida em determinada superfície. Dois modos estão disponíveis: limite específico de posicionamento, que define um limite que se aplica somente quando a oferta é exibida em um posicionamento selecionado, e limite por posicionamento, que aplica um limite independentemente em cada posicionamento em que a oferta é exibida, de modo que cada posicionamento mantém seu próprio contador de limite. Observe que o limite relacionado à disposição não se aplica a ofertas limitadas usando regras baseadas em dados do Adobe Experience Platform. <a href="https://jira.corp.adobe.com/browse/DOCAC-14980">DOCAC-14980</a> <!-- Documentation link: TBD -->

### Designer de email {#august-26-email}

A seguinte melhoria foi adicionada ao Designer de email nesta versão.

* **Novo componente Tabela no Designer de email** - O Designer de email agora inclui um componente Tabela interno, permitindo que você estruture o conteúdo em linhas e colunas diretamente no seu email. Arraste e solte o componente na tela, personalize o número de linhas e colunas e estilize cada célula independentemente para criar layouts claros e organizados sem depender de HTML personalizados. <a href="https://jira.corp.adobe.com/browse/DOCAC-15093">DOCAC-15093</a> <!-- Documentation link: TBD -->

### Administração {#august-26-administration}

As seguintes melhorias foram adicionadas à administração nesta versão.

* **Processo OTP de Loop de Comentários para subdomínios personalizados** - O processo de configuração de subdomínio personalizado FBL (Loop de Comentários) foi aprimorado ao exibir a OTP (Senha Ocasional) do hub do remetente do Yahoo diretamente na interface do usuário do produto. Os usuários agora podem recuperar e exibir automaticamente o OTP gerado durante a verificação de propriedade de domínio do hub do remetente do Yahoo. <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">DOCAC-14815</a> <!-- Documentation link: TBD -->

### Melhorias de usabilidade {#august-26-usability}

As seguintes melhorias foram adicionadas à usabilidade nesta versão.

* **Nova experiência de simulação de conteúdo para variantes de conteúdo** - O fluxo de trabalho **Simular conteúdo** apresenta uma experiência reprojetada: todas as variantes agora são renderizadas juntas em uma única grade rolável (lado a lado, layouts empilhados ou encapsulados), substituindo a exibição uma variante de cada vez. Uma única barra de ação inferior consolida a navegação entre variantes de teste, o zoom, a alternância de visor (desktop/celular), a alternância de local, a adição de entradas de amostra, a geração de variantes com IA, a escolha e o salvamento de usuários simulados e a importação ou exportação de variantes. Remover o painel esquerdo e recolher camadas de cabeçalho extras oferece visualizações com muito mais espaço. A opção **Alternar para experiência clássica** na barra de ação inferior permite reverter para a experiência anterior a qualquer momento. <a href="https://jira.corp.adobe.com/browse/DOCAC-15285">DOCAC-15285</a> <!-- Documentation link: TBD -->

* **Operações em massa no inventário de jornadas** - Agora é possível executar novas ações em massa diretamente da lista de inventário de jornadas, agilizando o gerenciamento de várias jornadas de uma só vez. Selecione várias jornadas e aplique qualquer uma das seguintes novas ações em uma única etapa: adicionar ao pacote, excluir, mover para pasta, editar tags ou gerenciar acesso. Isso reduz a necessidade de repetir a mesma ação uma jornada por vez, simplificando o gerenciamento de jornadas para equipes que trabalham com um grande número de jornadas. <a href="https://jira.corp.adobe.com/browse/DOCAC-15358">DOCAC-15358</a> <!-- Documentation link: TBD -->

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## Notas de pré-lançamento de 26 de julho {#july-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas poderão ser implantadas posteriormente.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 28 a 29 de julho de 2026

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### Jornadas {#july-26-journeys}

As seguintes melhorias foram adicionadas às jornadas nesta versão.


### Campanhas {#july-26-campaigns}

Os recursos e melhorias a seguir foram adicionados às campanhas nesta versão.

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

### Campanhas orquestradas {#july-26-oc}

As seguintes melhorias foram adicionadas às campanhas orquestradas nesta versão.

<!--

<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.

-->

### Canais {#july-26-channels}

Os seguintes recursos e melhorias foram adicionados aos canais nesta versão.

### Tomada de decisão {#july-26-decisioning}

As seguintes melhorias foram adicionadas à Decisão nesta versão.

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### Gerenciamento de conteúdo {#july-26-content}

As seguintes melhorias foram adicionadas ao gerenciamento de conteúdo nesta versão.

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### Personalização {#july-26-personalization}

As seguintes melhorias foram adicionadas à personalização nesta versão.


### Designer de email {#july-26-email}

O recurso a seguir foi adicionado ao canal de email nesta versão.


### Administração {#july-26-administration}

Os recursos a seguir foram adicionados à administração nesta versão.


### Melhorias de usabilidade {#july-26-usability}

As seguintes melhorias de usabilidade estão chegando nesta versão.

* **Atalhos de inicialização rápida para canais SMS, Push, No Aplicativo e Codebase em Modelos de Conteúdo** - O botão **Mais ações** na lista Modelos de Conteúdo agora fornece atalhos adicionais específicos do canal. Para modelos SMS, edite rapidamente a mensagem ou verifique a contagem/segmentos de caracteres. Para modelos de push, edite o título, o corpo ou a mídia. Para modelos no aplicativo, edite o cabeçalho da mensagem, o corpo da mensagem ou o URL da mídia. Para modelos de canal de base de código, edite o código diretamente. Esses atalhos estendem os atalhos de inicialização rápida do Canal de email já disponíveis. <!-- Documentation link: TBD -->
