---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 128a56b543f470bf967fd195fde73ff7b32b2a17
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 34%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de agosto de 2024 {#e-2024}

**Data de lançamento**: 20-21 de agosto de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.


<table>
<thead>
<tr>
<th><strong>Configuração de canal guiada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A Configuração de canal guiada permite automatizar as etapas de configuração do canal móvel em uma experiência unificada para começar mais rápido com o Journey Optimizer. Essa configuração facilita a configuração rápida de canais de marketing, garantindo que todos os recursos necessários estejam prontamente disponíveis no Experience Platform, Journey Optimizer e Coleção de dados. Isso permite que sua equipe de marketing comece imediatamente com a criação de campanhas e jornadas.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Cartões de conteúdo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O cartão de conteúdo é um novo recurso de mensagem digital do Adobe Journey Optimizer que fornece conteúdo personalizado e envolvente diretamente em aplicativos e sites móveis. Diferentemente das notificações por push tradicionais, os Cartões de conteúdo se integram perfeitamente à interface do usuário, oferecendo atualizações persistentes e não intrusivas que melhoram a interação e a experiência do usuário.</p>
<p>Esse recurso permite que os profissionais de marketing apresentem conteúdo de mídia relevante e avançado para os usuários, aumentando o engajamento e garantindo que mensagens importantes sejam vistas sem interromper a jornada do usuário.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configurações de canal aprimoradas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os recursos atuais da superfície de canal foram aprimorados para oferecer uma abordagem consistente em todos os canais. Agora você pode definir, gerenciar e reutilizar essas configurações para qualquer um dos seus canais.</p>
<p><ul>
<li>Superfícies de canal agora são renomeadas para <strong>Configurações de canal</strong></li>
<li>No inventário Configurações de canal, agora é possível criar configurações de canal reutilizáveis para todos os canais, incluindo agora Web, Mensagens no aplicativo ou Experiência baseada em código</li>
<li>O OLAC (Object Level Access Control) agora está disponível para cada configuração de canal, permitindo que você decida quais dos seus usuários têm permissão para criar ou usar configurações específicas</li>
<li>Para alguns canais, você pode criar configurações de canal que direcionem várias plataformas. Um exemplo seria uma configuração de canal de mensagens no aplicativo que pode direcionar uma página da Web, um aplicativo do iOS e um aplicativo do Android.</li>
</ul></p>
<p>Para obter mais informações, consulte a <a href="../configuration/ip-warmup-gs.md">documentação detalhada</a>.</p>
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
<p>Os fragmentos agora podem consumir variáveis de entrada, tanto em <a href="../personalization/use-expression-fragments.md">fragmentos de expressão</a> quanto em <a href="../email/use-visual-fragments.md">fragmentos visuais</a>. Você pode usar essas variáveis para personalizar o conteúdo e os parâmetros das mensagens em suas campanhas e jornadas.</p>
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

**Jornadas**

* Na atividade **Condição**, por padrão, a condição Tempo agora é definida por hora, das 00:00 às 12:00. [Leia mais](../building-journeys/condition-activity.md#time_condition)
* Ao criar suas jornadas, os alertas agora são exibidos em uma lista suspensa, para se alinharem aos alertas de campanha e proporcionarem uma experiência de usuário consistente. [Leia mais](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* As opções de zoom na barra de ferramentas jornada foram aprimoradas: a porcentagem de zoom agora está visível e agora é possível redefinir facilmente o valor de zoom para 100%.

**Públicos-alvo**

* O uso de públicos-alvo a partir de uploads personalizados (arquivo CSV) agora está disponível para uso com o Privacy and Security Shield.
* Ao direcionar um público-alvo de upload personalizado (arquivo CSV), agora é possível usar atributos do arquivo em suas campanhas e jornadas. Esses atributos estão disponíveis no editor de personalização, para personalizar suas mensagens, e no editor de expressão avançado do jornada.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
