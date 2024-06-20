---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 63%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.


## Notas de versão de junho de 2024 {#24-6-2024}

**As notas de versão anteriores abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.

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
<th><strong>Relatório com Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os relatórios do Journey Optimizer agora estão totalmente integrados com as capacidades de Customer Journey Analytics, padronizando os relatórios em ambas as plataformas e melhorando a consistência e confiabilidade dos dados. Essa integração perfeita entre o Journey Optimizer e o Customer Journey Analytics fornece uma visão mais clara das métricas de desempenho, permitindo que os usuários tomem decisões mais conscientes.</p>
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

<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>Multilingual content is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
<p>Experimentation in journeys is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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

### Melhorias {#june24-improvements}

Esta versão vem com as melhorias listadas abaixo.


**Gestão de decisões**

* **Compatibilidade com várias regras na gestão de decisões** – Agora você pode adicionar até 10 regras de limitação para uma determinada oferta na gestão de decisões. Isso permite aumentar o nível de controle sobre como as ofertas são enviadas. [Saiba mais](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**Fragmentos de conteúdo**

>[!AVAILABILITY]
>
>Observe que essas melhorias serão implementadas gradualmente durante vários dias após o lançamento inicial. Embora alguns usuários tenham acesso imediato, outros podem enfrentar um atraso antes que ele se torne disponível em seus ambientes.

* Agora os fragmentos podem ser editados e as alterações podem ser propagadas por todas as jornadas e campanhas ativas em que são usados.
* Foram introduzidos novos status para fragmentos de conteúdo: **Rascunho**, **Ativo**, **Publicando** e **Arquivado**.
* Para usar um fragmento em uma jornada ou campanha, agora ele deve estar no status **ativo**. Uma nova etapa foi adicionada ao processo de criação de fragmento, permitindo que o fragmento seja publicado e disponibilizado para uso em jornadas e campanhas. Observe que a publicação de fragmento requer uma nova permissão.

  **Cuidado**: Como os status **Rascunho** e **Ativo** foram introduzidos com a versão de junho do Journey Optimizer, todos os fragmentos criados antes desta versão têm o status **Rascunho** mesmo se forem usados em uma jornada ou campanha. Saiba como atualizar seus fragmentos nesta seção.

Leia mais na seção [fragmento de conteúdo](../content-management/fragments.md) documentação.

**Jornadas**

* O tempo limite global do Jornada foi estendido para 91 dias. [Leia mais](../building-journeys/journey-properties.md#global_timeout)

  Qualquer nova jornada criada terá esse novo tempo limite refletido. Consulte esta página [seção de perguntas frequentes](../building-journeys/journey-properties.md#timeout-faq) para saber mais. Observe que essas alterações serão implementadas gradualmente durante o mês de junho.


* O Adobe Journey Optimizer agora é compatível com solicitações de exclusão/acesso de privacidade, bem como com solicitações de gerenciamento do ciclo de vida dos dados. [Leia mais](../privacy/requests.md)
* Agora é possível redimensionar as colunas no inventário de jornadas.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **Políticas de mesclagem** agora é GA: as políticas de mesclagem usadas por uma jornada agora estão visíveis e são consistentes em toda a jornada. [Leia mais](../building-journeys/journey-properties.md#merge-policies)



**Campanhas**

* Ao criar uma campanha no Adobe Journey Optimizer, agora é possível escolher o tipo de campanha (agendada ou acionada) em um novo modal. [Leia mais](../campaigns/create-campaign.md)

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**Canal SMS**

* Agora é possível adicionar códigos curtos exclusivos para cada sandbox com uma única configuração de API, tornando o processo mais eficiente e simplificado. [Saiba mais](../sms/sms-configuration.md)

* Após a criação, a variável **Token de API** no campo **Detalhes da credencial da API** agora está mascarada.

<!--* You can now modify existing SMS configurations.-->

**Canal no aplicativo**

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Agora você pode usar o plug-in Edge Delivery para obter as informações necessárias para entender e solucionar problemas de suas implementações de entrada. [Saiba mais sobre a exibição Entrega de borda](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


**Canal de correspondência direta**

* O canal de correspondência direta agora está disponível para organizações que compraram o Adobe **Healthcare Shield** e **Escudo de Proteção e Privacidade** ofertas complementares.
