---
solution: Journey Optimizer
product: journey optimizer
title: Notas de versão
feature: Release Notes
topic: Content Management
description: Notas de versão do Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2dfcbd1631c7fefccaf02782a3218c9a1c1dc7aa
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 96%

---

# Notas de versão {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novidades"
>abstract="O **Adobe Journey Optimizer** está sempre fornecendo novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão."

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Na última semana de cada mês, todas as alterações são consolidadas nessas notas de versão.

O [!DNL Adobe Journey Optimizer] é construído nativamente na [!DNL Adobe Experience Platform] e herda suas mais recentes inovações e melhorias. Saiba mais sobre essas alterações nas [Notas de versão da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=pt-BR){target="_blank"}.

![Informativo](../assets/do-not-localize/nl-icon.png) Assine o [informativo trimestral do Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} hoje e receba as últimas atualizações de produtos, histórias interessantes, casos de uso, dicas e muito mais, entregues diretamente à sua caixa de entrada a cada trimestre.

## Notas da versão de fevereiro de 2024 {#feb-2024}

**Data de lançamento**: 21 e 22 de fevereiro de 2024

### Novos recursos{#feb-features}

Essa versão traz os novos recursos listados abaixo.


<table>
<thead>
<tr>
<th><strong>Mensagens Web no aplicativo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode usar o novo recurso de mensagens Web no aplicativo para exibir conteúdo personalizado diretamente em sites, por meio de mensagens de sobreposição modal. Esse recurso permite que você interaja efetivamente com visitantes da Web, melhorando a interação de usuários, a retenção e as taxas de conversão.<br/><br/></p>
<p>Para obter mais informações, consulte a <a href="../in-app/create-in-app-web.md">documentação detalhada</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modelos de conteúdo multicanal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Além do Email, os modelos de conteúdo agora estão disponíveis para os seguintes canais: Push, No aplicativo, SMS e Correspondência direta. Cada canal com tipos de modelos dedicados. Para Email, agora é possível selecionar o Tipo de conteúdo, que permite salvar a linha de assunto como parte do modelo de email. <br/><br/></p>
<p>Para obter mais informações, consulte a <a href="../content-management/content-templates.md">documentação detalhada</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif">
</tr>
</tbody>
</table>


### Melhorias {#feb-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Públicos-alvo**

* **Listas de seeds**: as variantes agora são compatíveis ao usar **listas de seeds**. Os seed addresses recebem uma cópia de todas as variantes da mesma mensagem (como os diferentes tratamentos de um experimento de conteúdo). [Leia mais](../configuration/seed-lists.md)

Anteriormente disponível como Beta, as seguintes melhorias agora estão disponíveis para todos os usuários:

* Agora é possível direcionar **públicos-alvo criados por meio da composição de público-alvo** e aproveitar os atributos de enriquecimento em jornadas. [Saiba mais](../building-journeys/read-audience.md)

* Agora é possível direcionar **públicos-alvo enviados a partir de um arquivo CSV** para jornadas e campanhas. [Saiba mais](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* O públicos-alvo e os atributos da composição de público-alvo e do upload personalizado (arquivo CSV) estão atualmente indisponíveis para uso com o Healthcare Shield ou o Privacy and Security Shield.
  >* A melhoria no **upload do público-alvo de um arquivo CSV** está sendo implementada gradualmente ao longo de vários dias após o lançamento inicial. Embora alguns usuários tenham acesso imediato, outros podem sofrer um atraso antes que ele fique disponível em seu ambiente.

**Jornadas**

* **Filtre suas jornadas**: agora você pode usar o inventário **datas personalizadas para filtrar as jornadas**, além dos filtros de data predefinidos já existentes. Isso permite refinar a lista ao exibir jornadas criadas ou publicadas em uma data específica, em um mês específico, durante um ano inteiro ou em intervalos de tempo especificados. [Leia mais](../building-journeys/journey-gs.md#filter)
* **Ações personalizadas**: agora você pode atualizar o cabeçalho **tipo de conteúdo**. Este novo **tipo de conteúdo** deve fazer referência ao conteúdo JSON. [Leia mais](../action/about-custom-action-configuration.md#url-configuration)
* **Configuração**: o atributo identityMap em stepEvents agora é pré-preenchido. A identidade principal é definida como “primary = true”. [Leia mais](../reports/sharing-field-list.md)
* **Interface**: a barra superior, nas telas da jornada, foi reorganizada para fornecer uma experiência aprimorada. Entre as diferentes atualizações, observe que o ícone de “lápis” que permite acessar as propriedades da jornada agora é exibido à esquerda da barra superior, ao lado do nome da jornada. [Leia mais](../building-journeys/journey-gs.md#change-properties)

**Canal SMS**

* **Palavras-chave de aceitação/recusa**: ao configurar seu canal de SMS, agora é possível personalizar as **Palavras-chave de aceitação e recusa** de acordo com suas preferências. O Journey Optimizer aciona a resposta com base nessas palavras-chave especificadas. [Saiba mais](../sms/sms-configuration.md#create-api)

**Campanhas**

* **Campanhas acionadas por API**: o código cURL gerado após a ativação de uma campanha acionada por API foi aprimorado. Agora, todas as variáveis de personalização (perfil e contexto) usadas na mensagem estão presentes. [Leia mais](../campaigns/api-triggered-campaigns.md#execute)

**Regras de frequência**

* Além de Email e Push, agora é possível criar regras de frequência para canais de SMS e de correspondência direta. As regras de frequência excluem automaticamente perfis excessivamente solicitados de mensagens e ações quando o limite de frequência é atingido. [Leia mais](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Notas da versão de janeiro de 2024 {#jan-2024}

**Data de lançamento**: 30 e 31 de janeiro de 2024

### Novos recursos{#jan24-features}

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
<p>Desde 1º de fevereiro de 2024, o Google e o Yahoo! estão exigindo um registro DMARC para qualquer domínio que você usar para enviar emails a eles. Certifique-se de que você tenha o registro DMARC configurado para todos os subdomínios que delegou ou está delegando à Adobe no Journey Optimizer.</p>
<p>Para obter mais informações, consulte a <a href="../configuration/dmarc-record-update.md">documentação detalhada</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
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
<p>Aproveite um catálogo de manuais de estratégia de casos de uso específicos do setor na Real-Time CDP e no Journey Optimizer para abordar casos de uso comuns que você pode executar usando a Adobe Experience Platform e o Adobe Journey Optimizer.</p><p>Depois de escolher o manual de estratégia que melhor atende às suas necessidades, você pode habilitá-lo para gerar os ativos necessários que darão suporte ao seu caso de uso, como jornadas, mensagens, esquemas ou segmentos, e personalizá-los de acordo com o esquema para agilizar resultados relevantes.</p>
<p>Para obter mais informações, consulte a <a href="../start/playbooks.md">documentação detalhada</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Melhorias {#jan24-improvements}

Esta versão vem com as melhorias listadas abaixo.

**Relatórios**

* **Novos dispositivos de detalhamento baseados em domínio**: novos dispositivos foram adicionados para aprimorar seus relatórios de campanha e de jornada. Os dispositivos **Motivos de rejeição por domínio**, **Enviado e entregue por domínio**, **Aberturas e cliques por domínio** e **Rejeição e erros por domínio** fornecem um detalhamento no nível do domínio para as principais métricas de entrega e rastreamento de email. [Saiba mais](../reports/channel-report.md)

**Canal SMS**

* **Aceitação dupla**: o fluxo de trabalho de Aceitação dupla de SMS garante que os usuários e usuárias optem explicitamente por receber mensagens quando a solicitação for iniciada a partir de seus dispositivos. Os usuários e usuárias iniciam o processo de consentimento enviando uma mensagem SMS de entrada. Após confirmar o consentimento, uma mensagem de acompanhamento é enviada, solicitando a verificação final. Se um perfil de usuário não existir, ele será criado após a confirmação bem-sucedida. [Saiba mais](../sms/sms-configuration.md#create-api)

  Observe que esse recurso está disponível nos provedores de SMS Sinch e Infobip.

**Jornadas**

* **Duração dos eventos de reação**: a duração máxima que você pode definir nos **Eventos de reação** agora é de 29 dias, em vez de 30. [Saiba mais](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Público-alvo de leitura**: a atividade **Público-alvo de leitura** agora depende do conjunto de dados de instantâneo de perfil para segmentos em lote, o que é gerado apenas uma vez por dia depois que o processo em lote diário programado é executado. Portanto, os dados serão atualizados até esse último processo em lote diário. [Saiba mais](../building-journeys/read-audience.md)

* **Grupos de campos**: esta versão corrige um problema que impedia que Grupos de campos fossem salvos em determinados casos.

* O suporte de `<listObject>` foi modificado em várias funções.

**Regras de frequência**

* **Limite de frequência semanal** - Agora você pode especificar o número máximo de mensagens enviadas a um perfil de cliente por semana, além do mês. O limite de frequência é baseado no período do calendário selecionado e redefinido no início do período correspondente. [Saiba mais](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >O limite de frequência diária também está disponível sob demanda. Entre em contato com o representante da Adobe.

**Gestão de decisões**

* **Limite de frequência no Edge**: o contador de limite de frequência agora é atualizado e disponibilizado em uma decisão da API de decisão do Edge em menos de 3 segundos. [Saiba mais](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
