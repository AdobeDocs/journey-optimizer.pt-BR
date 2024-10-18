---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão de 2024
description: Notas de versão do Journey Optimizer 2024
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: f316ec79958ac23e0e416f0cafd49c017f2b6d4c
workflow-type: tm+mt
source-wordcount: '3842'
ht-degree: 100%

---

# Notas de versão de 2024 {#release-notes-2024}

Esta página lista todos os recursos e melhorias do [!DNL Journey Optimizer] lançado em 2024.


## Versão de agosto de 2024 {#8-2024}

**Data de lançamento**: 20-21 de agosto de 2024

### Novos recursos {#8-features}

Essa versão traz os novos recursos detalhados abaixo.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Configurações de canais aprimoradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os recursos atuais de superfície de canal foram aprimorados para oferecer uma abordagem consistente em todos os canais. Agora é possível definir, gerenciar e reutilizar essas configurações para qualquer um dos canais, incluindo Web, mensagens no aplicativo ou experiência baseada em código.</p>
<p><ul>
<li>Superfícies de canal foram renomeadas para <strong>Configurações de canal</strong></li>
<li>Você pode anexar uma ou várias ações de marketing para aplicar políticas de consentimento e governança de dados</li>
<li>O controle de acesso no nível do objeto (OLAC) agora está disponível para cada configuração de canal, permitindo que você decida quais dos seus usuários têm permissão para criar ou usar configurações específicas</li>
<li>Para alguns canais, você pode criar configurações de canal que direcionem várias plataformas. Um exemplo seria uma configuração de canal de mensagens no aplicativo que pode direcionar uma página da Web, um aplicativo do iOS ou do Android.</li>
</ul></p>
<p>Para obter mais informações, consulte a <a href="../configuration/channel-surfaces.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ação personalizada do Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode integrar o Adobe Journey Optimizer com o Adobe Marketo Engage para criar seus casos de uso B2B. Em uma jornada, uma nova ação personalizada permite assimilar dados no Marketo.</p>
<p>Para obter mais informações, consulte a <a href="../action/marketo-engage.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variáveis em fragmentos de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As variáveis globais de fragmentos aprimoram a funcionalidade do fragmento para melhorar a eficiência na reutilização de conteúdo e nos casos de uso de script. Os fragmentos agora podem usar variáveis de entrada e criar variáveis de saída utilizáveis em conteúdos de campanhas e jornadas. Os fragmentos podem consumir variáveis de entrada, tanto em <a href="../personalization/use-expression-fragments.md">fragmentos de expressão</a> quanto em <a href="../email/use-visual-fragments.md">fragmentos visuais</a>. Você pode usar essas variáveis para personalizar o conteúdo e os parâmetros das mensagens em suas campanhas e jornadas.</p>
<p>Para obter mais informações, consulte a <a href="../personalization/use-expression-fragments.md">documentação detalhada</a>.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Fluxo de trabalho de aquecimento de IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Data de disponibilidade: 13 de agosto</p>
<p>Se você estiver enviando emails em um novo endereço IP, agora é possível executar facilmente fluxos de trabalho de aquecimento de IP diretamente da interface do usuário. O Adobe Journey Optimizer oferece uma maneira padronizada e eficiente de aquecer seus endereços IP que segue as práticas recomendadas para uma capacidade de entrega otimizada.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/ip-warmup-gs.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#8-improvements}

Essa versão traz as melhorias listadas abaixo.

**Jornadas**

* Na atividade **Condição**, por padrão, a **[!UICONTROL condição Tempo]** agora é definida por hora, das 00:00 às 12:00. [Leia mais](../building-journeys/condition-activity.md#time_condition)
* Ao criar as jornadas, os alertas agora são exibidos ao selecionar o botão **Alertas**, para que se alinhar a outros alertas e proporcionar uma experiência consistente aos usuários. [Leia mais](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* As opções de zoom na barra de ferramentas da jornada foram aprimoradas: a porcentagem de zoom agora está visível e é possível redefinir mais facilmente o valor do zoom.

**Canal de push**

* Agora é possível adicionar suas credenciais de push do aplicativo móvel nas configurações de canal do Adobe Journey Optimizer. Não é mais necessário criar uma superfície de aplicativo na Coleção de dados da Adobe Experience Platform.

### Outras alterações {#changes}

**Relatórios**

* Novos casos de uso foram adicionados à nova experiência de relatórios:

   * Crie métricas calculadas personalizadas diretamente dos seus relatórios.
   * Crie um público-alvo a partir dos dados de relatório.
   * Use a ferramenta de Análise Exploratória para criar facilmente tabelas e visualizações a partir das **[!UICONTROL Dimensões]** e **[!UICONTROL Métricas]** selecionadas.

  Para obter mais informações, consulte a [documentação detalhada](../reports/report-cja-manage.md).



## Versão de julho de 2024 {#24-7-2024}

**Data de lançamento**: 30 a 31 de julho de 2024

### Novos recursos {#27-4-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Canal de SMS com qualquer provedor (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível configurar provedores de SMS adicionais no Journey Optimizer, além dos provedores padrão Sinch, Infobip e Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Para obter mais informações, consulte a <a href="../sms/sms-configuration-custom.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composição de público-alvo federado (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Composição de público-alvo federado agora está disponível no Adobe Journey Optimizer. Ela permite que empresas componham dados para uma melhor utilização em vários casos de uso. Com essa nova abordagem, usuários da Adobe Real-Time Customer Data Platform e/ou do Adobe Journey Optimizer podem federar conjuntos de dados diretamente do seu data warehouse para criar e enriquecer públicos-alvo e atributos da Adobe Experience Platform em um único sistema.</p>
<p>Para obter mais informações, consulte a <a href="https://experienceleague.adobe.com/pt-br/docs/federated-audience-composition/using/home"  target="_blank">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

### Melhorias {#27-4-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Jornadas**

* (Data de disponibilidade: 8 de julho) **Editor de expressão avançado na configuração de eventos de jornada**: agora você pode aproveitar o editor de expressão avançado ao configurar um evento, permitindo definir expressões mais complexas ou usar funções na condição de ID do evento. [Saiba mais](../event/about-creating.md#adv-exp-editor)



## Versão de junho de 2024 {#24-6-2024}

**Data de lançamento**: 18 a 19 de junho de 2024

### Novos recursos {#june-24-features}

Essa versão traz os novos recursos detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Customização de fragmentos de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir campos específicos em um fragmento que podem ser editados quando o fragmento é adicionado a uma campanha ou jornada. Isso permite o ajuste de partes do conteúdo no momento do uso, fornecendo flexibilidade para substituir valores padrão por detalhes específicos do contexto.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Para obter mais informações, consulte a <a href="../content-management/customizable-fragments.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Relatórios com o Customer Journey Analytics (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os relatórios do Journey Optimizer vêm com uma interoperabilidade aprimorada com os recursos do Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e a confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Para obter mais informações, consulte a <a href="../reports/report-gs-cja.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistente de IA no Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Assistente de IA é um recurso da interface do usuário que você pode usar para navegar e entender conceitos da Adobe e obter insights operacionais para seu ambiente específico. Ele está disponível em vários produtos na Adobe Experience Cloud, incluindo o Adobe Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../start/ai-assistant.md">documentação detalhada</a>.</p>
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
<p>No momento, o conteúdo multilíngue está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Experimentação em jornadas (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Já disponível em campanhas, o Adobe Journey Optimizer agora oferece suporte a experimentos em jornadas. Experimentos são ensaios aleatórios, o que, no contexto de testes online, significa que você expõe alguns usuários selecionados aleatoriamente a uma determinada variação de uma mensagem e outro conjunto de usuários selecionados aleatoriamente a outra variação ou tratamento. Após a exposição, é possível medir as métricas de resultado em que está interessado, como abertura de emails, assinaturas ou compras.</p>
<p>No momento, a experimentação em jornadas está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Melhorias {#june24-improvements}

Esta versão vem com as melhorias listadas abaixo.

#### Gestão de decisões

* **Compatibilidade com várias regras na gestão de decisões** – Agora você pode adicionar até 10 regras de limitação para uma determinada oferta na gestão de decisões. Isso permite aumentar o nível de controle sobre como as ofertas são enviadas. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Fragmentos de conteúdo 

>[!AVAILABILITY]
>
>Observe que essas melhorias serão implementadas gradualmente ao longo de vários dias após o lançamento inicial. Embora alguns usuários tenham acesso imediato, outros poderão enfrentar um atraso antes que as melhorias sejam disponibilizadas em seus ambientes.

* Agora os fragmentos podem ser editados e as alterações podem ser propagadas por todas as jornadas e campanhas ativas em que são usados.
* Foram introduzidos novos status para fragmentos de conteúdo: **Rascunho**, **Ativo**, **Publicando** e **Arquivado**.
* Para usar um fragmento em uma jornada ou campanha, agora ele deve estar no status **ativo**. Uma nova etapa foi adicionada ao processo de criação de fragmento, permitindo que o fragmento seja publicado e disponibilizado para uso em jornadas e campanhas. Observe que a publicação de fragmento requer uma nova permissão.

  **Cuidado**: Como os status **Rascunho** e **Ativo** foram introduzidos com a versão de junho do Journey Optimizer, todos os fragmentos criados antes desta versão têm o status **Rascunho** mesmo se forem usados em uma jornada ou campanha. Ao fazer qualquer alteração nesses fragmentos, será necessário [publicá-los](../content-management/create-fragments.md#publish) para torná-los “Ativos” e propagar as alterações para as campanhas e jornadas associadas. Também é necessário criar uma nova versão da jornada/campanha e publicá-la. 

Leia mais na documentação dos [fragmentos de conteúdo](../content-management/fragments.md).

#### Jornadas

* O tempo-limite global de jornadas foi estendido para 91 dias. [Leia mais](../building-journeys/journey-properties.md#global_timeout)

  Qualquer nova jornada criada terá esse novo tempo-limite. Consulte esta [seção de perguntas frequentes](../building-journeys/journey-properties.md#timeout-faq) para saber mais. Observe que essas alterações serão implementadas gradualmente durante o mês de junho.


* O Adobe Journey Optimizer agora é compatível com solicitações de exclusão/acesso de privacidade, bem como com solicitações de gerenciamento do ciclo de vida dos dados. [Leia mais](../privacy/requests.md)
* Agora é possível redimensionar as colunas nos inventários das jornadas.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **Políticas de mesclagem** agora é GA: as políticas de mesclagem usadas por uma jornada agora estão visíveis e são consistentes em toda a jornada. [Leia mais](../building-journeys/journey-properties.md#merge-policies)


#### Campanhas

* Ao criar uma campanha no Adobe Journey Optimizer, agora é possível escolher o tipo de campanha (agendada ou acionada) em um novo modal. [Leia mais](../campaigns/create-campaign.md)

#### Canal de email

* **Cancelar inscrição em lista**: após os anúncios recentes do Gmail e do Yahoo para remetentes em massa, o Journey Optimizer se tornou compatível com a opção “post/1-click” para cancelar inscrição em lista. Consulte as seguintes páginas: [gerenciamento de recusa de email](../email/email-opt-out.md#unsubscribe-header) e [definir configurações de email](../email/email-settings.md#list-unsubscribe).

  **OBSERVAÇÃO**: em novas superfícies de canal, a opção “Cancelar inscrição na lista” está ativada por padrão. Em superfícies existentes, a opção “URL de cancelamento de inscrição com um clique” está desmarcada por padrão nas configurações da superfície de canal. Se você estava usando um URL de recusa com um clique no corpo do email anteriormente, essa configuração ainda é válida. Se a opção “URL de cancelamento de inscrição com um clique” estiver marcada nas configurações da superfície de canal, o Adobe Journey Optimizer usará o URL  padrão gerado nas configurações.

#### Canal de SMS

* Agora é possível adicionar códigos curtos exclusivos para cada sandbox com uma única configuração de API, tornando o processo mais eficiente e simplificado. [Saiba mais](../sms/sms-configuration.md)

* Após a criação, o campo **Token de API** na página **Detalhes da credencial da API** fica mascarado.

<!--* You can now modify existing SMS configurations.-->

#### Canal no aplicativo

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Agora você pode usar o plug-in Edge Delivery para obter as informações necessárias para entender e solucionar problemas em suas implementações de entrada. [Saiba mais na exibição Edge Delivery](https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### Canal de correspondência direta

* O canal de correspondência direta agora está disponível para todos os clientes. [Leia mais](../direct-mail/get-started-direct-mail.md)



## Versão de maio de 2024 {#may-2024}

**Data de lançamento**: 21 a 22 de maio de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Escolha de experiências - Disponibilidade limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Escolha de experiências simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.</p>
<p>Esses itens de decisão são perfeitamente integrados a uma ampla variedade de configurações de entrada por meio do novo canal de experiência baseado em código, agora acessível nas campanhas do Journey Optimizer. As políticas de decisão da Escolha de experiências estão disponíveis para uso somente em campanhas de experiência baseadas em código.</p>
<p>No momento, a Escolha de experiências está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Para obter mais informações, consulte a <a href="../experience-decisioning/gs-experience-decisioning.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personalização da configuração de email – Disponibilidade limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode definir subdomínios dinâmicos e parâmetros de cabeçalho personalizados ao criar configurações de canais de email, para aumentar a flexibilidade e o controle sobre suas configurações de email.</p>
<p>No momento, a personalização da configuração de email está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../email/surface-personalization.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Escolha de experiências** (disponibilidade limitada)

As seguintes melhorias foram adicionadas desde a versão beta até a versão atual:

* **Escolha de experiências + Experiências baseadas em código**: agora é possível aproveitar o recurso Escolha de experiências para usar itens de decisão em campanhas baseadas em código. Observação: o canal Experiência baseada em código e a Escolha de experiências não estão disponíveis para organizações que compraram as ofertas complementares do Adobe Healthcare Shield e Privacy and Security Shield. [Leia mais](../code-based/get-started-code-based.md)
* **Dados de contexto**: agora é possível aproveitar os dados de contexto da Adobe Experience Platform em suas regras de decisão e nas fórmulas de classificação. [Leia mais](../experience-decisioning/context-data.md)
* **Nova permissão**: a permissão “Gerenciar escolha de experiências” agora está disponível para o recurso Gestão de decisões. Isso permite gerenciar direitos relacionados à Escolha de experiências. [Leia mais](../experience-decisioning/gs-experience-decisioning.md)
* **Regras de limite**: agora é possível adicionar várias regras de limite para um determinado item de decisão na Escolha de experiências. Isso permite aumentar o nível de controle sobre como as ofertas são enviadas. [Leia mais](../experience-decisioning/items.md#capping)
* **Relatórios**: agora é possível criar painéis de relatórios personalizados para campanhas da Escolha de experiências usando o [!DNL Customer Journey Analytics].  [Leia mais](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canal de email**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Pontuação de spam** (Beta): agora é possível verificar sua pontuação de spam de conteúdo em um relatório dedicado. Com o SpamAssassin, o Adobe Journey Optimizer testa seu conteúdo de email e atribui uma pontuação para indicar se os ISPs ou provedores de caixa de correio o consideram como spam ou não. [Leia mais](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >No momento, esse recurso está na versão beta, disponível apenas para clientes beta. Para participar do programa beta, entre em contato com seu representante da Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Jornadas**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Suporte a mTLS**: a autenticação mTLS agora é compatível com ações personalizadas. Não é necessária uma configuração adicional da ação personalizada ou jornada para ativar o mTLS; isso ocorre automaticamente ao detectar um ponto de acesso habilitado para mTLS. [Leia mais](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tabelas de pesquisa em eventos**: agora é possível aproveitar os dados de um conjunto de dados de pesquisa após definir uma relação usando um atributo de uma matriz de objetos. Os valores de pesquisa estarão disponíveis em jornadas (condições, ações personalizadas etc.) e na personalização de mensagens. [Leia mais](../event/experience-event-schema.md#relationships_limitations)
* **Editor de expressão avançado na configuração de evento** (disponibilidade limitada): agora é possível utilizar o editor de expressão avançado ao configurar um evento, o que permite definir expressões mais complexas ou usar funções na condição de ID de evento. Esse recurso foi lançado com disponibilidade limitada para clientes selecionados. [Leia mais](../event/about-creating.md#adv-exp-editor)
* **Políticas de mesclagem** (disponibilidade limitada): as políticas de mesclagem usadas por uma jornada agora estão visíveis e são consistentes em toda a jornada. Esse recurso foi lançado com disponibilidade limitada para clientes selecionados. [Leia mais](../building-journeys/journey-properties.md#merge-policies)

**Globalização**

Como parte do nosso esforço contínuo em fornecer uma experiência de usuário unificada, harmonizamos a terminologia usada nos produtos e aplicativos da Adobe Experience Cloud. Isso afeta o termo alemão “Titel”, que é alterado para “Label” quando se refere ao nome de um objeto. As alterações serão progressivamente implementadas na interface e na documentação.


## Versão de abril de 2024 {#apr-2024}

**Data de lançamento**: 2 de maio de 2024

### Novos recursos {#apr-features}

Essa versão traz os novos recursos detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Serviço de mensagens multimídia (MMS): todos os provedores</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o canal SMS, agora é possível aprimorar a comunicação enviando mensagens do serviço de mensagens multimídia (MMS), o que permite o compartilhamento de imagens, GIFs ou vídeos para clientes. Inicialmente disponível apenas com o Sinch, o MMS agora também está disponível com Infobip e Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Designer de jornada e relatórios em tempo real aprimorados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Essa versão vem com uma interface de usuário de tela aprimorada para jornada e fornece uma experiência do usuário mais intuitiva e eficiente. As atividades são mais claras e apresentam mais informações sobre a tela de jornada com menos cliques.</p>
<img src="assets/new-canvas3.gif"/>
<p>Juntamente com o design aprimorado da tela de jornada, estamos introduzindo a capacidade de ver métricas de relatórios das últimas 24 horas diretamente na tela de jornada. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Nota</strong>: essas alterações serão gradualmente implementadas em todos os ambientes a partir da versão de abril.</p>
<p>Para obter mais informações, consulte a <a href="new-canvas.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI Assistant. You can now use the AI Assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel configurations, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Melhorias {#apr-improvements}

Esta versão vem com as melhorias listadas abaixo.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO channel configuration**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel configuration through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configuração**

* Agora é possível selecionar uma ação de marketing no nível da configuração de canais. Quando usadas em uma configuração, todas as políticas de consentimento associadas a essa ação de marketing são aproveitadas para respeitar as preferências dos seus clientes. [Leia mais](../action/consent.md#surface-marketing-actions)
* O uso do Controle de acesso em nível de objeto agora está disponível para configurações de canal. [Leia mais](../configuration/channel-surfaces.md#create-channel-surface)
* Ao habilitar o cancelamento de inscrição da lista em uma configuração de canais, agora é possível definir o nível de consentimento para se alinhar à forma como você gerencia o consentimento de todas as outras fontes. [Leia mais](../email/email-settings.md#list-unsubscribe)

**Gestão de conteúdo**

* Agora é possível simular modelos de conteúdo para todos os canais. [Leia mais](../content-management/content-templates.md#test-templates)

**Personalização**

* A nova função auxiliar **toInt** está disponível no Editor de expressão. Ela permite converter tipos (como number, double, int, long, float, short, byte, boolean, string) em um número inteiro. [Leia mais](../personalization/functions/math.md#to-int)



## Versão de março de 2024 {#mar-2024}

**Data de lançamento**: 19 a 20 de março de 2024

### Novo recurso {#mar-features}

Essa versão traz o novo recurso listado abaixo.

<table>
<thead>
<tr>
<th><strong>Experiências baseadas em código</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o novo canal de Experiência baseada em código, o Adobe Journey Optimizer permite realizar personalizações e testes avançados para qualquer uma de suas propriedades de entrada, possibilitando a entrega perfeita de experiências personalizadas em diversos touchpoints, como aplicativos web, aplicativos móveis, aplicativos para desktop, consoles de vídeo, dispositivos conectados à TV, Smart TVs, quiosques, ATMs e dispositivos IoT, entre outros.</p>
<P>Os principais recursos incluem:</p>
<ul><li> Personalização universal: estenda as experiências personalizadas em todos os touchpoints, garantindo uma jornada de usuário coesa e personalizada</li>
<li>Precisão de edição granular: edite conteúdo específico em locais individuais em seus aplicativos ou páginas da Web</li>
<li>Implementação versátil: suporte para os métodos de implementação do lado do servidor, baseados em API ou baseados em SDK para integração contínua com o seu ambiente de desenvolvimento.</li></ul></p>
<p>Para obter mais informações, consulte a <a href="../code-based/get-started-code-based.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Melhorias {#mar-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Modelos de conteúdo**

* **Miniaturas**: um modo de **visualização em grade** agora está disponível para modelos de conteúdo, exibindo miniaturas para acesso visual aprimorado. Atualmente, apenas modelos HTML de email são compatíveis. [Saiba mais](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Esse recurso foi lançado com disponibilidade limitada (DL) para um pequeno conjunto de clientes.

**Jornadas**

Novos status intermediários foram adicionados ao ciclo de vida de criação de jornada:

* Status **Publicando** entre o status **Rascunho** e o status **Ativo**
* Status **Interrompendo** entre o status **Ativo** e o status **Parado** 
* Os status **Ativando o modo de teste** ou **Desativando o modo de teste** entre o status **Rascunho** e o status **Rascunho (teste)**

Quando uma jornada está em um estado intermediário, ela fica como somente de leitura. [Saiba mais](../building-journeys/journey-gs.md#filter)

## Versão de fevereiro de 2024 {#feb-2024}

**Data de lançamento**: 21 e 22 de fevereiro de 2024

### Novos recursos{#feb-features}

Essa versão traz os novos recursos listados abaixo.


<table>
<thead>
<tr>
<th><strong>Mensagens Web no aplicativo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o novo recurso de mensagens Web no aplicativo para exibir conteúdo personalizado diretamente em sites, por meio de mensagens de sobreposição modal. Esse recurso permite que você interaja efetivamente com visitantes da Web, melhorando a interação de usuários, a retenção e as taxas de conversão.<br/><br/></p>
<p>Para obter mais informações, consulte a <a href="../in-app/create-in-app-web.md">documentação detalhada</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelos de conteúdo multicanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além do Email, os modelos de conteúdo agora estão disponíveis para os seguintes canais: Push, No aplicativo, SMS e Correspondência direta. Cada canal com tipos de modelos dedicados. Para Email, agora é possível selecionar o Tipo de conteúdo, que permite salvar a linha de assunto como parte do modelo de email. <br/><br/></p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-templates.md">documentação detalhada</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### Melhorias {#feb-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* **Listas de seeds**: as variantes agora são compatíveis ao usar **listas de seeds**. Os seed addresses recebem uma cópia de todas as variantes da mesma mensagem (como os diferentes tratamentos de um experimento de conteúdo). [Leia mais](../configuration/seed-lists.md)

Anteriormente disponível como Beta, as seguintes melhorias agora estão disponíveis para todos os usuários:

* Agora é possível direcionar **públicos-alvo criados por meio da composição de público-alvo** e aproveitar os atributos de enriquecimento em jornadas. [Saiba mais](../building-journeys/read-audience.md)

* Agora é possível direcionar **públicos-alvo enviados a partir de um arquivo CSV** para jornadas e campanhas. [Saiba mais](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* O públicos-alvo e os atributos da composição de público-alvo e do upload personalizado (arquivo CSV) estão atualmente indisponíveis para uso com o Healthcare Shield ou o Privacy and Security Shield.
  >* A melhoria no **upload do público-alvo de um arquivo CSV** está sendo implementada gradualmente ao longo de vários dias após o lançamento inicial. Embora alguns usuários tenham acesso imediato, outros podem sofrer um atraso antes que ele fique disponível em seu ambiente.

**Jornadas**

* **Filtre suas jornadas**: agora você pode usar o inventário **datas personalizadas para filtrar as jornadas**, além dos filtros de data predefinidos. Isso permite refinar a lista ao exibir jornadas criadas ou publicadas em uma data específica, em um mês específico, durante um ano inteiro ou em intervalos de tempo especificados. [Leia mais](../building-journeys/journey-gs.md#filter)
* **Ações personalizadas**: agora você pode atualizar o cabeçalho **tipo de conteúdo**. Este novo **tipo de conteúdo** deve fazer referência ao conteúdo JSON. [Leia mais](../action/about-custom-action-configuration.md#url-configuration)
* **Configuração**: o atributo identityMap em stepEvents agora é pré-preenchido. A identidade principal é definida como “primary = true”. [Leia mais](../reports/sharing-field-list.md)
* **Interface**: a barra superior, nas telas da jornada, foi reorganizada para fornecer uma experiência aprimorada. Entre as diferentes atualizações, observe que o ícone de “lápis” que permite acessar as propriedades da jornada agora é exibido à esquerda da barra superior, ao lado do nome da jornada. [Leia mais](../building-journeys/journey-properties.md)

**Canal SMS**

* **Palavras-chave de aceitação/recusa**: ao configurar seu canal de SMS, agora é possível personalizar as **Palavras-chave de aceitação e recusa** de acordo com suas preferências. O Journey Optimizer aciona a resposta com base nessas palavras-chave especificadas. [Saiba mais](../sms/sms-configuration.md)

**Campanhas**

* **Campanhas acionadas por API**: o código cURL gerado após a ativação de uma campanha acionada por API foi aprimorado. Agora, todas as variáveis de personalização (perfil e contexto) usadas na mensagem estão presentes. [Leia mais](../campaigns/api-triggered-campaigns.md#execute)

**Regras de frequência**

* Além de Email e Push, agora é possível criar regras de frequência para canais de SMS e de correspondência direta. As regras de frequência excluem automaticamente perfis excessivamente solicitados de mensagens e ações quando o limite de frequência é atingido. [Leia mais](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Versão de janeiro de 2024 {#jan-2024}

**Data de lançamento**: 30 e 31 de janeiro de 2024

### Novos recursos{#jan24-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Atualizações de capacidade de entrega</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora é compatível com a tecnologia de autenticação DMARC.</p>
<p>Desde 1º de fevereiro de 2024, o Google e o Yahoo! estão exigindo um registro DMARC para qualquer domínio que você usar para enviar emails a eles. Certifique-se de que você tenha o registro DMARC configurado para todos os subdomínios que delegou ou está delegando à Adobe no Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/dmarc-record-update.md">documentação detalhada</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Manuais de casos de uso </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveite um catálogo de manuais de estratégia de casos de uso específicos do setor na Real-Time CDP e no Journey Optimizer para abordar casos de uso comuns que você pode executar usando a Adobe Experience Platform e o Adobe Journey Optimizer.</p><p>Depois de escolher o manual de estratégia que melhor atende às suas necessidades, você pode habilitá-lo para gerar os ativos necessários que darão suporte ao seu caso de uso, como jornadas, mensagens, esquemas ou segmentos, e personalizá-los de acordo com o esquema para agilizar resultados relevantes.</p>
<p>Para obter mais informações, consulte a <a href="../start/playbooks.md">documentação detalhada</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Melhorias {#jan24-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Relatórios**

* **Novos dispositivos de detalhamento baseados em domínio**: novos dispositivos foram adicionados para aprimorar seus relatórios de campanha e de jornada. Os dispositivos **Motivos de rejeição por domínio**, **Enviado e entregue por domínio**, **Aberturas e cliques por domínio** e **Rejeição e erros por domínio** fornecem um detalhamento no nível do domínio para as principais métricas de entrega e rastreamento de email. [Saiba mais](../reports/channel-report-cja.md)

**Canal SMS**

* **Aceitação dupla**: o fluxo de trabalho de Aceitação dupla de SMS garante que os usuários e usuárias optem explicitamente por receber mensagens quando a solicitação for iniciada a partir de seus dispositivos. Os usuários e usuárias iniciam o processo de consentimento enviando uma mensagem SMS de entrada. Após confirmar o consentimento, uma mensagem de acompanhamento é enviada, solicitando a verificação final. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. [Saiba mais](../sms/sms-configuration.md)

  Observe que esse recurso está disponível nos provedores de SMS Sinch e Infobip.

**Jornadas**

* **Duração dos eventos de reação**: a duração máxima que você pode definir nos **Eventos de reação** agora é de 29 dias, em vez de 30. [Saiba mais](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Público-alvo de leitura**: a atividade **Público-alvo de leitura** agora depende do conjunto de dados de instantâneo de perfil para segmentos em lote, o que é gerado apenas uma vez por dia depois que o processo em lote diário programado é executado. Portanto, os dados serão atualizados até esse último processo em lote diário. [Saiba mais](../building-journeys/read-audience.md)

* **Grupos de campos**: esta versão corrige um problema que impedia que Grupos de campos fossem salvos em determinados casos.

* O suporte de `<listObject>` foi modificado em várias funções.

**Regras de frequência**

* **Limite de frequência semanal**: agora é possível especificar o número máximo de mensagens enviadas para um perfil de cliente por semana, além de por mês. O limite de frequência é baseado no período do calendário selecionado e redefinido no início do período correspondente. [Saiba mais](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >O limite de frequência diária também está disponível por demanda. Entre em contato com seu representante Adobe. 

**Gestão de decisões**

* **Limite de frequência no Edge**: o contador de limite de frequência agora é atualizado e disponibilizado em uma decisão da API de decisão do Edge em menos de 3 segundos. [Saiba mais](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
