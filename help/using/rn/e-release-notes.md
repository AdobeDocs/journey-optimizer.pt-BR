---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 70ffd26772ae9907278af92a46af30b9d1bb1309
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 44%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).


## Notas de pré-lançamento de 25 de outubro {#25-10-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: quinta-feira, 22 de outubro de 2025

### Novos recursos {#oct-25-10-features}



<table>
<thead>
<tr>
<th><strong>Período de Silêncio/Exclusões Baseadas no Tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Quiet hours permite definir exclusões com base no tempo para canais de email, SMS, push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando você a respeitar as preferências do cliente e os requisitos de conformidade.</p>
<p>Você pode aplicar horas de silêncio por meio de conjuntos de regras, que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso. Simplificando esses processos.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com um representante da Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento e relatórios de ação personalizada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Esse recurso fornece melhor visibilidade sobre a integridade e a execução da jornada, incluindo status do ciclo de vida e alertas de desempenho. Agora você pode entender rapidamente quando, onde e por que uma situação anômala está ocorrendo em uma ação personalizada.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Nova API para recuperar Campanhas de ação</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível, permitindo recuperar e inspecionar programaticamente dados relacionados à campanha, como detalhes, versões e configurações.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos conectores de origem para aplicativos de fidelidade</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos conectores de origem agora estão disponíveis no Adobe Experience Platform para os aplicativos de fidelidade Talon.One, Capillary e Kobie. Esses conectores permitem transmitir dados de fidelidade facilmente para o Adobe Experience Platform e aproveitar esses dados no Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte à decisão no canal de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, você pode adicionar políticas de decisão a campanhas e jornadas por email. As políticas de decisão são recipientes para as suas ofertas que utilizam o mecanismo de tomada de decisão para retornar dinamicamente o melhor conteúdo a ser entregue a cada membro do público-alvo.</p>
<p> Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modo de alta taxa de transferência para campanhas de email acionadas por API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Um novo modo de taxa de transferência alta está disponível agora em campanhas acionadas por API. Este modo foi projetado para mensagens em larga escala e em tempo real (até 5.000 transações por segundo) e oferece maior disponibilidade com menor latência.</p>
<p>Esse recurso está disponível somente para o canal de email e para organizações que adquiriram a oferta complementar de mensagens transacionais de alta transferência da Adobe. Entre em contato com seu representante da Adobe para obter mais informações.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Novos alertas de Jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos alertas pré-configurados estão disponíveis para monitorar a execução do jornada:</p>
<ul><li><a href="./reports/alerts.md#alert-discard-rate">Taxa de Descarte de Perfil Excedida</a>: Taxa de descartes de perfil para perfis inseridos nos últimos 5 minutos excedeu o limite</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Taxa de Erro de Ação Personalizada Excedida</a>: Taxa de erros de ação personalizada para chamadas HTTP bem-sucedidas nos últimos 5 minutos excedeu o limite</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Taxa de Erro de Perfil Excedida</a>: Taxa de perfis com erro em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite</li>.</ul> <p>É possível modificar os valores limite e assinar alertas individuais em nível de jornada em vez de alertas globais.</p>
<p>Para mais informações, consulte a <a href="../reports/alerts.md">documentação detalhada</a></p>
<p>Data de disponibilidade: 14 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Auxiliar de metadados de execução</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova função auxiliar "executionMetadata" está disponível no editor de personalização. Ele permite anexar informações contextuais a qualquer ação nativa e capturá-las em um conjunto de dados para exportação para sistemas externos.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.</p>
<p>Para mais informações, consulte a <a href="../personalization/functions/helpers.md#execution-metadata">documentação detalhada</a></p>
<p>Data de disponibilidade: 13 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>O agente de experimentação está aqui!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Com a tecnologia <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, o Agente de experimentação está disponível na Journey Optimizer. </p>
<p>O Agente de experimentação é uma ferramenta alimentada por IA que moderniza como você pode executar e gerenciar experimentos digitais em sites, emails, mensagens por push e aplicativos. Ele ajuda você a executar experimentos com mais eficiência, organizar metas de negócios e gerar insights acionáveis, destacando o que funcionou, o que não funcionou e onde experimentar em seguida.</p>
<p>Para mais informações, consulte a <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=pt-BR" target="_blank">documentação detalhada</a></p>
<p>Data de disponibilidade: 10 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Anexos de PDF para emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível anexar um arquivo PDF estático a uma mensagem de email enviada com o Journey Optimizer.</p>
<ul>
<li>É possível enviar até 6 mensagens com um anexo PDF por perfil em um ano.</li>
<li>O tamanho máximo para cada anexo é 5 MB.</li>
<li>Para qualquer tamanho ou volume adicional, é possível comprar o complemento Anexos em PDF. Para obter mais informações, entre em contato com um representante da Adobe.</li>
</ul>
<p>Anteriormente lançado em disponibilidade limitada, este recurso já está disponível para todos os ambientes (disponibilidade geral).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Para mais informações, consulte a <a href="../email/pdf-attachments.md">documentação detalhada</a></p>
<p>Data de disponibilidade: 30 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API pública para recuperar jornadas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Uma nova API do Journey Optimizer agora está disponível para recuperar jornadas e seus objetos associados, como campanhas e superfícies.</p>
<p>Para mais informações, consulte a <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentação detalhada</a></p>
<p>Data de disponibilidade: 25 de setembro de 2025</p>
</td>
</tr>
</tbody>
</table>


### Aprimoramentos

**Selecionar regras reutilizáveis no Direcionamento**

Agora você pode aproveitar o construtor de regras ao usar as regras de direcionamento com o recurso de Otimização de mensagem em jornadas e campanhas. <!-- [Read more](../FILE.md) -->

**Campo de execução para o canal do WhatsApp**

Além de e-mail e SMS, agora é possível atualizar o campo de execução padrão do WhatsApp. Também é possível substituir o campo de execução definido globalmente nos parâmetros avançados da atividade de jornada do WhatsApp ou na configuração do canal do WhatsApp. <!-- [Read more](../FILE.md) -->

**Suporte a atributos personalizados para o endereço Mailto (cancelar inscrição)**

Com o Journey Optimizer, se você estiver gerenciando o consentimento fora do Adobe, é possível definir endpoints personalizados externos ao definir seu próprio link de cancelamento de inscrição com um clique e um endereço de email de cancelamento de inscrição personalizado na configuração de email. Quando os destinatários clicam no link para cancelar assinatura, o Journey Optimizer anexa alguns parâmetros padrão específicos do perfil ao evento de atualização de consentimento.

Para personalizar ainda mais os endpoints personalizados, agora é possível definir atributos personalizados que também serão anexados ao evento de consentimento. [Leia mais](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esse recurso já está disponível para a **[!UICONTROL URL para Cancelamento de Inscrição com Um Clique]** personalizada desde agosto de 25 e agora é lançado para a opção **[!UICONTROL Mailto (cancelar inscrição)]** em Disponibilidade Limitada. Entre em contato com o seu representante da Adobe para obter acesso.

Data de disponibilidade: 6 de outubro de 2025