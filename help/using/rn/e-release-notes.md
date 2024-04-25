---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: be758a577dbff2ae400d0642f9e898b423353f90
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 34%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de abril de 2024 {#e-2024}

**Data de lançamento**: 30 de abril de 2024

### Novo recurso {#e-features}

Essa versão traz os novos recursos detalhados abaixo.

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Experience Decisioning - Disponibilidade limitada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Experience Decisioning simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como "itens de decisão" e um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada indivíduo.</p>
<p>Esses itens de decisão são perfeitamente integrados em uma grande variedade de superfícies de entrada por meio do novo canal de experiência baseado em código, agora acessível nas campanhas do Journey Optimizer. As políticas de decisão do Experience Decisioning estão disponíveis para uso somente em campanhas de experiência baseadas em código.</p>
<p>No momento, o Experience Decisioning está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o representante da Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Serviço de Mensagens Multimídia (MMS) - todos os provedores</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o canal SMS, agora é possível aprimorar a comunicação enviando mensagens do Serviço de Mensagens Multimídia (MMS), o que permite o compartilhamento de imagens, GIFs ou vídeos com clientes. Inicialmente disponível apenas com Sinch, MMS agora também está disponível com Infobip e Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
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
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
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
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Gestão de decisões**

* A variável **Log de alterações** permite que você veja todas as alterações feitas em uma oferta ou em uma decisão que foi removida. As alterações relacionadas a ofertas e decisões agora podem ser vistas no **Auditorias** menu.

**Decisão da experiência**

De beta para LA, as seguintes melhorias foram adicionadas:

* Agora você pode aproveitar os dados de contexto do Adobe Experience Platform em suas regras de decisão usando o **Dados de contexto** guia.
* Uma nova permissão &quot;Gerenciar decisões de experiência&quot; agora está disponível para o recurso Gerenciamento de decisões. Ele permite gerenciar direitos relacionados ao Experience Decisioning.
* Agora é possível adicionar várias regras de limitação para uma oferta. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.
* Agora é possível adicionar várias regras de limitação para um determinado item de decisão no Experience Decisioning. Isso permite aumentar o nível de controle sobre a maneira como as ofertas são enviadas.
* Agora é possível criar painéis de relatórios personalizados para campanhas do Experience Decisioning usando o [!DNL Customer Journey Analytics].

**Jornadas**

* **Designer de Jornada aprimorado**

   * A interface aprimorada da tela fornece uma experiência do usuário mais intuitiva e eficiente.
   * As atividades são mais claras e apresentam mais informações sobre a tela de jornada com menos cliques.

* **Novo relatório ao vivo**: os relatórios das últimas 24 horas do jornada agora podem ser acessados diretamente na tela do Jornada.

**Configuração**

* Agora é possível selecionar uma ação de marketing no nível da superfície de canal. Quando usadas em uma superfície, todas as políticas de consentimento associadas a essa ação de marketing são aproveitadas para respeitar as preferências de clientes.
* O uso do Controle de acesso em nível de objeto agora está disponível para superfícies de canal.

