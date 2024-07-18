---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f0b08b9cb9c12f7920e5a26a565b34b4bec8c84a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 32%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

**As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento**.  Links, telas e a documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de julho de 2024 {#e-2024}

**Data de lançamento**: 30 a 31 de julho de 2024

### Novos recursos {#e-features}

Essa versão traz os novos recursos detalhados abaixo.

<table>
<thead>
<tr>
<th><strong>Fluxo de trabalho de aquecimento de IP (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Se você estiver enviando emails em um novo endereço IP, agora é possível executar facilmente fluxos de trabalho de aquecimento de IP diretamente da interface do usuário. O Adobe Journey Optimizer oferece uma maneira padronizada e eficiente de aquecer seus endereços IP que segue as práticas recomendadas para uma capacidade de entrega otimizada.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Canal SMS com qualquer provedor</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar provedores de SMS adicionais no Journey Optimizer, além dos provedores padrão Sinch, Infobip e Twilio.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>ação personalizada de Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode integrar o Adobe Journey Optimizer com o Adobe Marketo Engage para criar seus casos de uso B2B. Em uma jornada, uma nova ação personalizada permite assimilar dados na Marketo.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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

* (Disponibilidade: 8 de julho) Agora você pode aproveitar o editor de expressão avançado ao configurar um evento, permitindo definir expressões mais complexas ou usar funções na condição ID do evento. [Saiba mais](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

**Canal SMS**

* Agora você pode modificar as configurações de SMS existentes.

**Canal no aplicativo**

* Fragmentos de expressão agora estão disponíveis para o canal no aplicativo.

**Canal por push**

* Agora é possível adicionar suas credenciais de push do aplicativo móvel nas configurações de canal do Adobe Journey Optimizer. Não é mais necessário criar uma superfície de aplicativo na Coleção de dados da Adobe Experience Platform.

**Públicos-alvo**

* O uso de públicos-alvo e atributos da composição de público-alvo e do upload personalizado (arquivo CSV) agora está disponível para uso com o Healthcare Shield ou o Privacy and Security Shield.