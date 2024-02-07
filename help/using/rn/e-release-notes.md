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
source-git-commit: 97967e8043df9b75d3120e4a7bfccff700f5d57f
workflow-type: ht
source-wordcount: '558'
ht-degree: 100%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de janeiro de 2024 {#e-2024}

**Data de lançamento**: 20 a 31 de janeiro de 2024

### Novos recursos{#e-features}

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
<p>A partir de 1º de fevereiro de 2024, o Google e o Yahoo! exigirão um registro DMARC para qualquer domínio que você usar para enviar emails para eles. Certifique-se de que você tenha o registro DMARC configurado para todos os subdomínios que delegou ou está delegando à Adobe no Journey Optimizer.</p>
<!--img src="assets/channel-reports.png"/-->
<p>Para obter mais informações, consulte a <a href="../configuration/dmarc-record.md">documentação detalhada</a>.</p>
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
<p>Aproveite um catálogo de manuais de casos de uso específicos do setor na Real-Time CDP e no Journey Optimizer para abordar casos de uso comuns que você pode executar usando a Adobe Experience Platform e o Adobe Journey Optimizer.</p><p>Depois de escolher o manual de estratégia que melhor atende às suas necessidades, você pode habilitá-lo para gerar os ativos necessários que darão suporte ao seu caso de uso, como jornadas, mensagens, esquemas ou segmentos, e personalizá-los de acordo com o esquema para agilizar resultados relevantes.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### Melhorias {#e-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Relatórios**

* **Novos dispositivos de detalhamento baseados em domínio**: novos dispositivos foram adicionados para aprimorar seus relatórios de campanha e de jornada. Os dispositivos **Motivos de rejeição por domínio**, **Enviado e entregue por domínio**, **Aberturas e cliques por domínio** e **Rejeição e erros por domínio** fornecem um detalhamento no nível do domínio para as principais métricas de entrega e rastreamento de email. [Saiba mais](../reports/channel-report.md)

**Canal SMS**

* **Aceitação dupla**: o fluxo de trabalho de Aceitação dupla de SMS garante que os usuários e usuárias optem explicitamente por receber mensagens quando a solicitação for iniciada a partir de seus dispositivos. Os usuários e usuárias iniciam o processo de consentimento enviando uma mensagem SMS de entrada. Após confirmar o consentimento, uma mensagem de acompanhamento é enviada, solicitando a verificação final. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. [Saiba mais](../sms/sms-configuration.md#create-api)

  Observe que isso se aplica somente aos provedores de SMS Sinch e Infobip.

**Jornadas**

* **Duração dos eventos de reação**: a duração máxima que você pode definir nos **Eventos de reação** agora é de 29 dias, em vez de 30. [Saiba mais](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Público-alvo de leitura**: a atividade Público-alvo de leitura agora depende do conjunto de dados de instantâneo de perfil para segmentos em lote, o que é gerado apenas uma vez por dia depois que o processo em lote diário programado é executado, portanto, os dados serão atualizados até esse último processo em lote diário.

* **Grupos de campos**: corrigido um problema que impedia que Grupos de campos fossem salvos em determinados casos.

* **Editor de expressão**: agora oferecemos suporte ao tipo de dados listObject em todas as expressões e em funções adicionais. [Mais informações](../building-journeys/expression/functions.md)

**Regras de frequência**

* **Limite de frequência semanal e diária**: agora você pode especificar o número máximo de mensagens a serem enviadas para um perfil de cliente em uma semana, em um dia ou em um mês. O limite de frequência é baseado no período do calendário selecionado e redefinido no início do período correspondente. [Saiba mais](../configuration/frequency-rules.md#create-new-rule)

**Gestão de decisões**

* **Limite de frequência no Edge**: o contador de limite de frequência agora é atualizado e disponibilizado em uma decisão da API de decisão do Edge em menos de 3 segundos. 