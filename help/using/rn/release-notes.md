---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6fc3e27f11fa95d9ee705c8a3aff8649f66dc44d
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 54%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Atualizações de setembro {#9-2024}

<table>
<thead>
<tr>
<th><strong>Configuração de canal guiada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Configuração de canal guiada permite automatizar e validar a configuração de canal em uma experiência unificada, acelerando o processo de introdução ao Journey Optimizer. Essa nova configuração guiada simplifica a configuração rápida do canal, garantindo que todos os recursos necessários sejam instalados e funcionem prontamente no Experience Platform, Journey Optimizer e Coleção de dados. Isso permite que as equipes de marketing, engenharia de produtos e dados comecem rapidamente com a criação de campanhas e jornadas.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/set-mobile-config.md">documentação detalhada</a>.</p>
</br>
<img src="assets/do-not-localize/guided-setup.gif"/>
</td>
</tr>
</tbody>
</table>

## Notas de versão de agosto de 2024 {#8-2024}

**Data de lançamento**: 20-21 de agosto de 2024

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

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
<li>Superfícies de canal agora são renomeadas para <strong>Configurações de canal</strong></li>
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
<th><strong>Variáveis em Fragmentos de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As variáveis globais de fragmento aprimoram a funcionalidade existente do fragmento para melhorar a eficiência na reutilização de conteúdo e nos casos de uso de script. Os fragmentos agora podem usar variáveis de entrada e criar variáveis de saída utilizáveis no conteúdo da campanha e da jornada. Os fragmentos podem consumir variáveis de entrada em <a href="../personalization/use-expression-fragments.md">fragmentos de expressão</a> e <a href="../email/use-visual-fragments.md">fragmentos visuais</a>. Você pode usar essas variáveis para personalizar o conteúdo e os parâmetros das mensagens em suas campanhas e jornadas.</p>
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

* Na atividade **Condição**, por padrão, a **[!UICONTROL Condição de tempo]** agora é definida por hora, das 00:00 às 12:00. [Leia mais](../building-journeys/condition-activity.md#time_condition)
* Ao criar suas jornadas, os alertas agora são exibidos pelo botão **Alertas**, para se alinharem a outros alertas e proporcionarem uma experiência consistente ao usuário. [Leia mais](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* As opções de zoom na barra de ferramentas jornada foram aprimoradas: a porcentagem de zoom agora está visível e você pode redefinir mais facilmente o valor de zoom.

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**Canal por push**

* Agora é possível adicionar suas credenciais de push do aplicativo móvel nas configurações de canal do Adobe Journey Optimizer. Não é mais necessário criar uma superfície de aplicativo na Coleção de dados da Adobe Experience Platform.

### Outras alterações {#changes}

**Relatórios**

* A experiência atual de relatórios será removida a partir da versão de outubro. Após essa data, a nova experiência de relatórios se tornará o padrão. Recomendamos que você se familiarize com os novos recursos e funcionalidades para garantir uma transição suave.

[Introdução à nova interface de relatórios do Journey Optimizer](../reports/report-gs-cja.md)

* Novos casos de uso foram adicionados à nova experiência de relatórios:

   * Crie métricas calculadas personalizadas diretamente dos seus relatórios.
   * Crie um Público-alvo com base nos dados de relatório.
   * Use a ferramenta de Análise Exploratória para criar facilmente tabelas e visualizações a partir dos **[!UICONTROL Dimension]** e **[!UICONTROL Métricas]** selecionados.

  Para obter mais informações, consulte a [documentação detalhada](../reports/report-cja-manage.md).
