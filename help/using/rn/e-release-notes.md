---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 26%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de outubro de 2023 {#oct-rn-2023}

**Data de lançamento**: 25 a 26 de outubro de 2023

### Novos recursos{#oct-2023-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Ferramentas de sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As ferramentas de sandbox permitem copiar objetos em várias sandboxes aproveitando a exportação e a importação de pacotes. Um pacote pode consistir em um único objeto ou em vários objetos. Todos os objetos incluídos em um pacote devem ser da mesma sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>Serviço de Mensagens Multimídia (MMS) em SMS (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com o Canal SMS, agora é possível aprimorar sua comunicação enviando mensagens do Serviço de Mensagens Multimídia (MMS), permitindo o compartilhamento de imagens, GIF ou vídeos com seus clientes. Observe que esse recurso está disponível atualmente na versão Beta somente com o Sinch.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Melhorias {#oct-2023-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* Agora é possível direcionar públicos-alvo carregados de um arquivo CSV para jornadas e campanhas.
* Agora é possível direcionar públicos-alvo criados por meio da composição de públicos-alvo e aproveitar os atributos de enriquecimento no Jornada.

>[!AVAILABILITY]
>
>No momento, esses recursos estão disponíveis como um beta privado.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campanhas**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Quando ocorre um erro em uma de suas campanhas, um ícone de aviso agora é exibido na lista de campanhas ao lado do status da campanha.

**Jornadas**

* A duração máxima que você pode definir em qualquer tempo de espera agora é de 29 dias, em vez de 30. Isso se aplica a:

   * o **Quantidade de tempo** no campo [atividade de espera](../building-journeys/wait-activity.md)
   * o **Período de espera de reentrada** in [jornada propriedades](../building-journeys/journey-gs.md#entrance)
   * o **Aguardar** na definição de tempo limite de [geral](../building-journeys/general-events.md#events-specific-time) e [reação](../building-journeys/reaction-events.md) eventos.

**Consentimento na configuração do canal**

* Agora é possível selecionar uma ação de marketing no nível da superfície de canal. Quando usadas em uma superfície, todas as políticas de consentimento associadas a essa ação de marketing são aproveitadas para respeitar as preferências dos clientes.

**Gestão de decisões**

* Vários rótulos relacionados ao limite de oferta na interface da gestão de decisões foram atualizados.
