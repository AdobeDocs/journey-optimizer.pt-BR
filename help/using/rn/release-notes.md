---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b2459757d1f1964c7d0b59de814bed29b0a394bb
workflow-type: ht
source-wordcount: '1244'
ht-degree: 100%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Notas de versão de julho de 2024 {#27-4-2024}

**Data de lançamento**: 30 a 31 de julho de 2024

### Novos recursos {#27-4-features}

Essa versão traz os novos recursos detalhados abaixo.

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

<!--**Audiences**

* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield.-->

## Notas de versão de junho de 2024 {#24-6-2024}

**Data de lançamento**: 18 a 19 de junho de 2024

### Novos recursos {#june-24-features}

Essa versão traz os novos recursos detalhados abaixo.

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
<p>No momento, o conteúdo multilíngue está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
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
<p>No momento, a experimentação em jornadas está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
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

