---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 283983d98905b8e36d41823d1fae5d7a3c269ba3
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 28%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Notas de versão antecipadas de janeiro de 2024 {#jan-2024}

**Data de lançamento**: 30 a 31 de janeiro de 2024

### Novos recursos{#jan24-features}

Essa versão traz os novos recursos listados abaixo.

<table>
<thead>
<tr>
<th><strong>Atualizações de entregabilidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora é compatível com a tecnologia de autenticação DMARC.</p>
<p>A partir de 1º de fevereiro de 2024, o Google e o Yahoo! O exigirá um registro DMARC para qualquer domínio que você usar para enviar emails para eles. Verifique se você tem o registro DMARC configurado para todos os subdomínios que você delegou ou ou que estão delegando ao Adobe no Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/dmarc-record-update.md">documentação detalhada</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Playbooks de caso de uso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Aproveite um catálogo de manuais de casos de uso específicos do setor no Real-Time CDP e no Journey Optimizer para tratar de casos de uso comuns que você pode executar usando o Adobe Experience Platform e o Adobe Jornada Otimizer.</p><p>Depois de escolher o manual que melhor atende às suas necessidades, você pode habilitá-lo para gerar os ativos necessários para suportar o caso de uso, como jornadas, mensagens, esquemas ou segmentos, e personalizá-los no esquema para agilizar o tempo de implantação.</p>
<p>Para obter mais informações, consulte a <a href="../start/playbooks.md">documentação detalhada</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Melhorias {#jan24-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Relatórios**

* **Novos widgets de detalhamento baseados em domínio** - Novos widgets foram adicionados para aprimorar seus relatórios de Campanha e Jornada. A variável **Motivos de rejeição por domínio**, **Enviado e entregue por domínios**, **Aberturas e cliques por domínio** e **Rejeição e erros por domínio** os widgets fornecem um detalhamento detalhado no nível do domínio para as principais métricas de entrega e rastreamento de email. [Saiba mais](../reports/channel-report.md)

**Canal de SMS**

* **Aceitação dupla** - O fluxo de trabalho de Aceitação dupla de SMS garante que os usuários optem explicitamente por receber mensagens quando a solicitação for iniciada a partir de seus dispositivos. Os usuários iniciam o processo de consentimento enviando uma mensagem SMS de entrada. Após confirmar o consentimento, uma mensagem de acompanhamento é enviada, solicitando verificação final. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. [Saiba mais](../sms/sms-configuration.md#create-api)

  Observe que esse recurso está disponível com provedores de SMS Sinch e Infobip.

**Jornadas**

* **Duração dos eventos de reação** - A duração máxima que você pode definir no **Eventos de reação** agora é de 29 dias, em vez de 30. [Saiba mais](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Ler público**  - A **Ler público-alvo** A atividade do agora depende do conjunto de dados de instantâneo de perfil para segmentos em lote, que é gerado apenas uma vez por dia depois que o trabalho em lote diário programado é executado, portanto, os dados serão atualizados para esse último trabalho em lote diário. [Saiba mais](../building-journeys/read-audience.md)

* **Grupos de campos** - Esta versão corrige um problema que impedia que grupos de campos fossem salvos em determinados casos.

**Regras de frequência**

* **Limite de frequência semanal e diária** - Agora você pode especificar o número máximo de mensagens enviadas para um perfil de cliente em uma semana ou um dia, além do mês. O limite de frequência é baseado no período de calendário selecionado e redefinido no início do período correspondente. [Saiba mais](../configuration/frequency-rules.md#create-new-rule)

**Gestão de decisões**

* **Limite de frequência na borda** - O contador de limite de frequência agora é atualizado e disponibilizado em uma decisão da API do Edge Decisioning em menos de 3 segundos. [Saiba mais](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)