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
source-git-commit: c58b70fa5f792e2fa1448034559ad7210e3e10d4
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 21%

---


# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

<table>
<thead>
<tr>
<th><strong>Channel optimization (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add multiple outbound channels (Email, Push, SMS) to a single journey action and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available: manual ranking, customer profile preference (XDM attribute), and AI model-based ranking using propensity scores. When the top-ranked channel is unavailable, the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../building-journeys/channel-optimization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

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

<!-- Documentation link: TBD -->

### Campanhas {#july-26-campaigns}

Os recursos e melhorias a seguir foram adicionados às campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Anexos personalizados do PDF em emails acionados por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora é compatível com a anexação de até cinco PDFs específicos do recipient por email em campanhas acionadas por API. Os arquivos do PDF são buscados com segurança do armazenamento do Azure ou do AWS e anexados no momento do envio, com o local de cada arquivo transmitido diretamente na carga da API. Isso permite que os sistemas de geração de documentos upstream existentes permaneçam em vigor, com o Journey Optimizer lidando com a entrega.</p>
<p>Os casos de uso suportados incluem faturas, demonstrativos, tíquetes, contratos, etiquetas de remessa e documentos semelhantes que variam de acordo com o recipient. Os anexos personalizados do PDF estão disponíveis somente em campanhas acionadas por API e não são compatíveis com jornadas ou outros tipos de campanha (ação, orquestrada).</p>
<p>Volumes e tamanhos de anexo maiores são suportados por meio do complemento de anexo do PDF; para obter mais informações, entre em contato com o representante da Adobe.</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

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
[GIF placeholder: to be added]
[Documentation link: TBD]
</td>
</tr>
</tbody>
</table>

-->

### Campanhas orquestradas {#july-26-oc}

As seguintes melhorias foram adicionadas às campanhas orquestradas nesta versão.


<!--
* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.
-->

<!--
### Optimization {#july-26-optimization}

<table>
<thead>
<tr>
<th><strong>Channel optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now configure a journey or campaign action to include multiple outbound channels (Email, Push, SMS) and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available:</p>
<ul>
<li>Manual ranking: specify your preferred channel order.</li>
<li>Customer preference: use the customer's preferred channel from their profile (Experience Data Model Consents & Preferences attribute).</li>
<li>AI model-based ranking: use machine learning propensity scores to infer the most effective channel per customer.</li>
</ul>
<p>When the top-ranked channel is unavailable (not opted-in, frequency-capped, or not configured), the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

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

-->

### Canais {#july-26-channels}

Os seguintes recursos e melhorias foram adicionados aos canais nesta versão.

<table>
<thead>
<tr>
<th><strong>Canal de saída personalizado</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora apresenta os Canais personalizados, um novo recurso que permite aos administradores trazer qualquer canal de mensagens baseado em HTTP de saída — como WeChat, Kakao Talk, Messenger ou um provedor proprietário — diretamente para o Journey Optimizer por meio de um Construtor de canal sem código.</p >
<p>Depois de configurados, os canais personalizados ficam disponíveis em campanhas, jornadas e campanhas orquestradas, com o mesmo conjunto completo de recursos dos canais nativos: personalização com o editor de expressão, experimentação de conteúdo, pré-visualização e prova, relatórios prontos para uso e aplicação de consentimento e governança.</p>
<p>Isso preenche uma lacuna anteriormente abordada por ações personalizadas, que são limitadas apenas a jornadas e não têm recursos de canal dedicados.</p>
<p>Os canais de saída personalizados estão disponíveis no momento como Disponibilidade limitada. Para obter acesso, entre em contato com um representante da Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Complemento de desempenho para taxa de transferência - Push** - Um novo modo de mensagens transacionais de alta taxa de transferência está disponível em campanhas acionadas por API. Esse modo é projetado para mensagens transacionais em tempo real de grande escala e aceita até 5.000 transações por segundo com maior disponibilidade. Anteriormente disponível apenas para o canal de email, esse recurso agora também está disponível para o canal de push, para organizações que compraram a oferta complementar de Mensagens transacionais de alta capacidade da Adobe. Entre em contato com seu representante da Adobe para obter mais detalhes. <!-- Documentation link: TBD -->



### Tomada de decisão {#july-26-decisioning}

As seguintes melhorias foram adicionadas à Decisão nesta versão.

* **Personalization no nível da oferta** - Os atributos personalizados do item de decisão agora podem ser personalizados no momento da entrega usando dados de perfil, contextuais e de público-alvo. Isso elimina a necessidade de manter ofertas duplicadas para variações de conteúdo secundárias, permitindo que os profissionais de marketing gerenciem um número menor de itens de decisão e mais flexíveis. <!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### Gerenciamento de conteúdo {#july-26-content}

As seguintes melhorias foram adicionadas ao gerenciamento de conteúdo nesta versão.

* **Suporte a fragmentos de expressão em `<head>` de modelos de email** - Os fragmentos de expressão agora podem ser usados no `<head>` de modelos de email. Isso permite centralizar o estilo ou qualquer código personalizado em um único fragmento e reutilizá-lo em vários modelos. Quando um fragmento é atualizado e republicado, todos os emails criados a partir de modelos que fazem referência a ele herdam automaticamente o código mais recente, eliminando a necessidade de atualizar manualmente cada email individualmente. <!-- Documentation link: TBD -->
<!-- Documentation link: TBD -->



<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### Personalização {#july-26-personalization}

As seguintes melhorias foram adicionadas à personalização nesta versão.

* **Gerenciar domínios para personalização completa/básica da URL** - Agora é possível criar e gerenciar domínios aprovados para personalização completa e básica da URL diretamente das configurações de Administração no Adobe Journey Optimizer, sem precisar entrar em contato com o Suporte da Adobe. <!-- Documentation link: TBD -->

<!-- Documentation link: TBD -->

### Designer de email {#july-26-email}

O recurso a seguir foi adicionado ao canal de email nesta versão.

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


### Administração {#july-26-administration}

Os recursos a seguir foram adicionados à administração nesta versão.

<table>
<thead>
<tr>
<th><strong>Lista de permissões de IP do Firewall do Aplicativo Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Adobe Journey Optimizer agora oferece suporte à lista de permissões de IP do Web Application Firewall para páginas de aterrissagem, permitindo que as organizações façam com que todas as solicitações recebidas sejam roteadas exclusivamente por meio de sua infraestrutura configurada do Web Application Firewall. Com esse aprimoramento, os clientes podem configurar o Journey Optimizer para rejeitar qualquer solicitação direta que ignore a camada do Web Application Firewall, garantindo que as políticas de segurança definidas em ferramentas como o Imperva sejam aplicadas consistentemente.</p>
<p>Esse recurso fortalece a postura de segurança para empresas com requisitos rigorosos de acesso à rede, dando a elas controle total sobre o fluxo de tráfego para as páginas de aterrissagem hospedadas pela Journey Optimizer.</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### Melhorias de usabilidade {#july-26-usability}

As seguintes melhorias de usabilidade estão chegando nesta versão.

* **Atalhos de inicialização rápida para canais SMS, Push, No Aplicativo e Codebase em Modelos de Conteúdo** - O botão **Mais ações** na lista Modelos de Conteúdo agora fornece atalhos adicionais específicos do canal. Para modelos SMS, edite rapidamente a mensagem ou verifique a contagem/segmentos de caracteres. Para modelos de push, edite o título, o corpo ou a mídia. Para modelos no aplicativo, edite o cabeçalho da mensagem, o corpo da mensagem ou o URL da mídia. Para modelos de canal de base de código, edite o código diretamente. Esses atalhos estendem os atalhos de inicialização rápida do Canal de email já disponíveis. <!-- Documentation link: TBD -->
