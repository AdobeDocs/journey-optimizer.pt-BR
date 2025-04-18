---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 08b9c2daa61a13de2d0f1ce6174c80a16459b8b1
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 69%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão. O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

## Atualizações de abril de 2025

### Novos recursos {#25-04-feature}

<table>
<thead>
<tr>
<th><strong>Métricas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As métricas de Jornada agora estão disponíveis, permitindo medir o impacto das suas atividades nas métricas principais da sua empresa e fornecer insights mais claros sobre o seu desempenho.</p>
<p>Para obter mais informações, consulte a <a href="../building-journeys/success-metrics.md">documentação detalhada</a>.</p>
<p>Data de disponibilidade: 9 de abril de 2025</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

### Melhorias {#25-04-improv}

* **Ferramentas de sandbox** - Data de disponibilidade: 3 de abril de 2025

  Agora é possível copiar campanhas em várias sandboxes usando recursos de exportação e importação de pacotes. As campanhas são copiadas junto com todos os itens relacionados ao perfil, público-alvo, esquema, mensagens embutidas e objetos dependentes. Alguns itens não são copiados, como itens de decisão, rótulos de uso de dados e configurações de idioma. [Leia mais](../configuration/copy-objects-to-sandbox.md)

* **Personalization** - Data de disponibilidade: 2 de abril de 2025

  O painel de atributos no editor de personalização agora mostra apenas atributos preenchidos por padrão. Para exibir todos os atributos, use o botão de configurações para desativar a opção **[!UICONTROL Mostrar apenas atributos preenchidos]**. [Leia mais](../personalization/personalization-build-expressions.md)

* **Gerenciamento de conteúdo** - Data de disponibilidade: 2 de abril de 2025

  Para gerenciar facilmente seus modelos e fragmentos de conteúdo, agora é possível usar pastas para organizá-los com mais eficiência em uma hierarquia estruturada. Saiba mais nas seções [Modelos de conteúdo](../content-management/access-content-templates.md#folders) e [Fragmentos](../content-management/manage-fragments.md#folders).

  >[!AVAILABILITY]
  >
  >Esta melhoria está disponível apenas para um conjunto de organizações (disponibilidade limitada).

* **Email Designer** - Data de disponibilidade: 1 de abril de 2025

  Para aprimorar a acessibilidade no Journey Optimizer, dois novos campos agora estão disponíveis no Designer de email: eles correspondem ao elemento `<title>` e ao atributo `lang` no elemento `<html>` do seu conteúdo de email. Você pode definir essas configurações além do campo **[!UICONTROL Pré-cabeçalho]**, na seção email **[!UICONTROL Corpo]**. [Leia mais](../email/email-metadata.md)


## Notas de versão de março de 2025 {#25-3-rn}


### Novos recursos {#25-03-features}

Os novos recursos incluídos nesta versão são detalhados abaixo.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integração com o Dynamic Media (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os ativos do Dynamic Media agora estão diretamente disponíveis e acessíveis no Journey Optimizer. Essa integração permite:
<ul>
<li>Gerenciar ativos centralmente com atualizações em tempo real</li>
<li>Modificar instantaneamente suas configurações de ativos, como largura e altura</li>
<li>Personalizar modelos do Dynamic Media atualizando o conteúdo e adicionando campos de personalização</li>
</ul>
<p>
<p>Esta integração está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.</p>
<p>Para obter mais informações, consulte a <a href="../integrations/aem-dynamic.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integração com o Adobe GenStudio (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Para aprimorar a eficiência do marketing e manter a consistência da marca, agora é possível integrar perfeitamente as experiências do GenStudio para marketing de desempenho com o Journey Optimizer. Isso permite que você aproveite a criação de conteúdo com inteligência artificial do GenStudio juntamente com os recursos avançados de orquestração do Journey Optimizer.<p>
<p>O uso da integração do GenStudio no Journey Optimizer está atualmente indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield (disponibilidade limitada).</p>
<p>Para obter mais informações, consulte a <a href="../integrations/genstudio.md">documentação detalhada</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Avaliação de público-alvo flexível (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Anteriormente disponível para um conjunto de organizações (DL), a Avaliação flexível de público-alvo agora está disponível para todos os usuários (DG). Esse recurso permite executar um trabalho de segmentação sob demanda para públicos selecionados, garantindo que você sempre tenha os dados do público mais atualizados antes de direcioná-los para jornadas e campanhas do Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Para obter mais informações, consulte a <a href="../audience/creating-a-segment-definition.md#flexible">documentação detalhada</a>.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Melhorias {#25-03-improv}

**Editor de personalização** (data de disponibilidade: 12 de março)

O editor de personalização do Journey Optimizer foi atualizado com novos recursos:
* **Design do editor de código atualizado**: uma interface mais simples e moderna para melhorar a usabilidade e o foco.
* **Pesquisar e substituir**: adição da funcionalidade para localizar e substituir rapidamente o conteúdo no editor.
* **Desfazer e refazer**: permite reverter ou reaplicar facilmente as alterações.
* **Tamanho de fonte personalizável**: permite ajustar o tamanho da fonte do editor para facilitar a leitura.
* **Validação JSON em linha**: fornece validação do lado do cliente em tempo real para conteúdo JSON, a fim de acelerar a detecção de erros.
* **Preenchimento automático para atributos de perfil e contexto**: oferece sugestões inteligentes para simplificar a criação de conteúdo.
* **Realce de sintaxe aprimorado**: melhora a legibilidade por tornar a estrutura do código mais visualmente distinta.

![Vídeo mostrando o novo recurso no editor de personalização](assets/do-not-localize/personalization-editor.gif)

Para obter mais informações, consulte a [documentação detalhada](../personalization/personalization-build-expressions.md).

**Aprovações**

Ao definir as condições para uma política de aprovação, agora há a opção de filtrar por tag e/ou categoria de objeto.

Para obter mais informações, consulte a [documentação detalhada](../test-approve/approval-policies.md).

**Configuração**

* Agora é possível atribuir tags unificadas da Adobe Experience Platform às configurações de canais. Isso permite classificá-las facilmente e melhorar a pesquisa e a navegação em todas as listas. [Saiba mais](../configuration/channel-surfaces.md#channel-config-tags)

* Ao configurar ou editar um subdomínio de email no Journey Optimizer, agora você pode optar por gerenciar o registro DMARC associado por conta própria, se disponível no domínio principal. [Saiba mais](../configuration/dmarc-record.md#set-up-dmarc)

**Regras de negócios**

Agora você pode usar o limite de frequência diário em jornadas e campanhas com segmentação em lote. Para garantir a precisão das regras diárias de limite de frequência, escolha o namespace de prioridade mais alta ao criar uma campanha ou jornada. Saiba mais sobre a prioridade de namespace no [guia do Platform Identity Service](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Como lembrete, o limite de frequência diária em conjuntos de regras está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o(a) representante da Adobe.

Para obter mais informações sobre regras de negócios, consulte a [documentação detalhada](../configuration/rule-sets.md).

<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->


