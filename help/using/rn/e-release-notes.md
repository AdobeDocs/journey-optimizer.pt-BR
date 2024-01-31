---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão anteriores
description: Notas de versão antecipadas do Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: fe4c51a74431bf8ab66aa2c9c3bd07404d971bbf
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 17%

---

# Notas de versão antecipadas {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas na última semana de cada mês nas [notas de versão](release-notes.md).

As notas de versão antecipadas abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade do lançamento. Links, telas e documentação atualizada são publicados nas [notas de versão](release-notes.md), na data de lançamento.

## Notas de versão antecipadas de janeiro de 2024 {#oct-jan-2024}

**Data de lançamento**: 30 a 31 de janeiro de 2024

### Novos recursos{#jan-2024-features}

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
<img src="assets/do-not-localize/dmarc.gif"/>
<p>Para obter mais informações, consulte a <a href="../configuration/dmarc-record-update.md">documentação detalhada</a>.</p>
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
<img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### Melhorias {#jan-2024-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Relatórios**

* **Novos widgets de detalhamento baseados em domínio** - Novos widgets foram adicionados para aprimorar seus relatórios de Campanha e Jornada. A variável **Motivos de rejeição por domínio**, **Enviado e entregue por domínios**, **Aberturas e cliques por domínio** e **Rejeição e erros por domínio** os widgets fornecem um detalhamento detalhado no nível do domínio para as principais métricas de entrega e rastreamento de email.

**Canal de SMS**

* **Aceitação dupla** - O fluxo de trabalho de Aceitação dupla de SMS garante que os usuários optem explicitamente por receber mensagens quando a solicitação for iniciada a partir de seus dispositivos. Os usuários iniciam o processo de consentimento enviando uma mensagem SMS de entrada. Após confirmar o consentimento, uma mensagem de acompanhamento é enviada, solicitando verificação final. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida.

  Observe que isso se aplica somente aos provedores de SMS Sinch e Infobip.

**Jornadas**

* **Duração dos eventos de reação** - A duração máxima que você pode definir no **Eventos de reação** agora é de 29 dias, em vez de 30.

* **Filtros de data** - Agora você pode usar datas personalizadas para filtrar o inventário do jornada, além dos filtros de data predefinidos existentes. Isso permite refinar a lista ao exibir jornadas publicadas em uma data específica, em um mês específico, durante um ano inteiro ou dentro de intervalos de tempo especificados.

* **Ler público**  - A atividade Ler público-alvo agora depende do conjunto de dados de instantâneo de perfil para segmentos em lote, que é gerado apenas uma vez por dia depois que o trabalho em lote diário programado é executado, portanto, os dados serão atualizados para esse último trabalho em lote diário.

**Regras de frequência**

* **Limite de frequência semanal e diária** - Agora você pode especificar o número máximo de mensagens enviadas para um perfil de cliente em uma semana ou um dia, além do mês. O limite de frequência é baseado no período de calendário selecionado e redefinido no início do período correspondente.


**Gestão de decisões**

* **Limite de frequência na borda** - O contador de limite de frequência agora é atualizado e disponibilizado em uma decisão da API do Edge Decisioning em menos de 3 segundos.