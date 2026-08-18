---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 8119b2ae6eeafbd6e973efb94074af5a4982c9db
workflow-type: tm+mt
source-wordcount: 1099
ht-degree: 17%

---


# Notas de pré-lançamento {#e-release-notes}

O Adobe Journey Optimizer fornece de forma contínua novos recursos, melhorias para os recursos já existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).

## Notas de pré-lançamento de agosto de 2026 {#august-26-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e documentação atualizada são publicados assim que as alterações são ativadas na produção. Embora a maioria das alterações seja fornecida na data de lançamento, algumas poderão ser implantadas posteriormente.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 18 a 19 de agosto de 2026

<!--
### Onboarding {#august-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### Jornadas {#august-26-journeys}

Os recursos e melhorias a seguir estão chegando às jornadas nesta versão.

<table>
<thead>
<tr>
<th><strong>controle no nível da jornada (disponibilidade limitada)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode configurar um grupo de controle para suas jornadas diretamente das propriedades do jornada. Uma validação é uma porcentagem configurável do público-alvo que é excluído da entrada na jornada e não recebe nenhuma comunicação. Ao comparar perfis de controle com perfis ativos nos relatórios do Customer Journey Analytics, é possível medir o aumento incremental - o impacto real - que a jornada oferece.</p>
<p> Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Adicionar nova função dateDiff no editor de expressão de jornada** - O editor de expressão de jornada agora inclui a função `dateDiff`, que calcula a diferença entre duas datas em número de dias. Essa função é útil para uma lógica baseada no tempo, como criar prazos, calcular durações de ciclo de vida do cliente ou criar cronômetros de contagem regressiva em condições de jornada. <!-- Documentation link: TBD -->

* **Datas de início e término no cabeçalho da jornada** - Quando as datas de início e/ou término são configuradas em uma jornada, elas agora são exibidas no cabeçalho da jornada ao lado da notificação de status. O rótulo exibido se adapta com base no fato de cada data ser futura ou já ter passado. <!-- Documentation link: TBD -->

### Canais {#august-26-channels}

As seguintes melhorias estão chegando para as Campanhas nesta versão:

* **Metadados de execução de atividade ao vivo (executionMetadata)** - As campanhas de atividade ao vivo acionadas por API (Transacional e Marketing) agora oferecem suporte a um campo executionMetadata opcional em cada destinatário. Isso permite anexar dados de chave/valor personalizados, como uma ID de pedido, camada de fidelidade ou código de região, a uma execução.

### Campanhas {#august-26-camp}

Os seguintes recursos e melhorias estão chegando às Campanhas nesta versão.

<table>
<thead>
<tr>
<th><strong>Simulação de experiência de entrada em campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível simular ações de canal de entrada em Campanhas de ação antes de entrar em atividade. Use o modo de simulação para testar sua configuração com usuários simulados e visualizar a experiência renderizada, incluindo um URL gerado e um código QR, para que você possa validar regras, decisões e renderização de conteúdo de ponta a ponta.</p>
<p>No momento, esse recurso está em beta privado e disponível para um conjunto limitado de organizações. Entre em contato com o representante da Adobe para obter mais informações.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Redesign do fluxo de criação da Campanha de Ação** - O fluxo de criação da Campanha de Ação do Adobe Journey Optimizer foi reprojetado para fornecer uma experiência do usuário significativamente mais intuitiva, eficiente e contínua.

* **Pastas para Campanhas de Ação** - Agora você pode organizar suas Campanhas de Ação em pastas para melhorar a navegação e o gerenciamento na interface. <!-- Documentation link: TBD -->

<!--* **Brand alignment score in Action Campaign dashboard** - You can now assess your brand alignment score directly within your Action Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.  Documentation link: TBD -->

* **Substituir os campos de execução padrão em Campanhas de ação** - Anteriormente disponíveis no nível de jornada, agora é possível substituir os campos de execução padrão configurados globalmente para suas entregas de email, SMS e WhatsApp nos parâmetros da Campanha de ação. <!-- Documentation link: TBD -->

### Campanhas orquestradas {#august-26-oc}

Os seguintes recursos e melhorias estão chegando ao Orchestrated Campaigns nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte para o Quiet Hours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode aplicar o Período de Silêncio. O Quiet Hours permite definir exclusões com base no tempo para evitar que as mensagens sejam enviadas durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade em casos de uso da orquestração de campanha.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envio usando ondas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode programar mensagens de saída para serem entregues em lotes controlados ao longo do tempo. Ideal para campanhas de alto volume ou sensíveis ao tempo, o envio de ondas também oferece suporte a uma melhor capacidade de entrega e ajuda a manter uma sólida reputação do remetente, reduzindo o risco de ser sinalizado como spam. </p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Capacidade de Gerenciar Dimensões de Destino do Perfil** - Agora é possível excluir um Dimension de Destino do Perfil ou editar e trocar seu namespace de identidade configurado, fornecendo maior controle e flexibilidade sobre as configurações de dados. <!-- Documentation link: TBD -->

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **Personalizar detalhes do remetente de email por destinatário e campanha (Disponibilidade limitada)** - As campanhas orquestradas agora oferecem suporte à personalização de campos de cabeçalho de email, incluindo Nome de origem, Prefixo de email de origem, Nome de resposta e Email de resposta, bem como endereço de execução, usando atributos de perfil ou dados relacionais. Isso permite que os detalhes do remetente reflitam o consultor, o local ou a filial relevante para cada destinatário, em vez de encaminhar todos os envios por meio de um único endereço corporativo. Os valores do cabeçalho podem ser definidos no nível do canal e substituídos por campanha usando dados contextuais para obter um controle mais preciso.
Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada).
  <!-- Documentation link: TBD -->

* **Simplificação da dimensão de público-alvo** - A dimensão de público-alvo ativa agora é mostrada na tela do fluxo de trabalho, para que você possa ver qual dimensão é usada por uma atividade de canal. O fluxo de segmentação de várias entidades é mais simples, pois você não precisa mais de uma atividade &quot;Alterar dimensão&quot; separada. Além disso, agora você pode escolher explicitamente se as mensagens são enviadas no nível do perfil ou em um nível de dimensão secundário. <!-- Documentation link: TBD -->



### Tomada de decisão {#august-26-decisioning}

Os seguintes recursos e melhorias estão chegando à Decisão nesta versão.

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal da Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A decisão agora está disponível para o canal da Web. Você pode usar políticas de decisão diretamente no editor visual da Web para fornecer as ofertas mais relevantes a cada visitante.</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Limite de frequência no nível de posicionamento na Decisão** - As regras de limite de frequência na Decisão agora podem ser segmentadas para posicionamentos individuais, fornecendo controle mais fino sobre a frequência com que uma oferta é exibida em determinada superfície. Dois modos estão disponíveis: limite específico de posicionamento, que define um limite que se aplica somente quando a oferta é exibida em um posicionamento selecionado, e limite por posicionamento, que aplica um limite independentemente em cada posicionamento em que a oferta é exibida, de modo que cada posicionamento mantém seu próprio contador de limite. Observe que o limite relacionado à disposição não se aplica a ofertas limitadas usando regras baseadas em dados do Adobe Experience Platform. <!-- Documentation link: TBD -->

* **Mirror pages em Fragmentos Visuais** - Agora é possível inserir mirror pages em um Fragmento Visual. Os atributos de decisão são renderizados corretamente no link da mirror page, mesmo quando o fragmento é usado em uma campanha de email que usa a Decisão. A mirror page deve ser adicionada ao fragmento visual antes de o fragmento ser publicado para que os atributos de decisão sejam exibidos. <!-- Documentation link: TBD -->

### Administração {#august-26-administration}

O aprimoramento a seguir está chegando para a administração nesta versão.

* **Processo OTP de Loop de Comentários para subdomínios personalizados** - O processo de configuração de subdomínio personalizado FBL (Loop de Comentários) foi aprimorado ao exibir a OTP (Senha Ocasional) do hub do remetente do Yahoo diretamente na interface do usuário do produto. Os usuários agora podem recuperar e exibir automaticamente o OTP gerado durante a verificação de propriedade de domínio do hub do remetente do Yahoo. <!-- Documentation link: TBD -->

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


