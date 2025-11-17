---
solution: Journey Optimizer
product: journey optimizer
title: Notas de pré-lançamento do Journey Optimizer
description: Notas de pré-lançamento do Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d09fc3ed670a50b6a99bcf660353ee37d31c7501
workflow-type: ht
source-wordcount: '1089'
ht-degree: 100%

---

# Notas de pré-lançamento {#e-release-notes}

O [!DNL Adobe Journey Optimizer] fornece continuamente novos recursos, melhorias para os recursos existentes e correções de erros. Todas as alterações são consolidadas no fim de cada mês nas [notas de versão](release-notes.md).


## Notas de pré-lançamento de outubro de 2025 {#oct-25-10-rn}

**As notas de pré-lançamento abaixo estão sujeitas a alterações sem aviso prévio até a data de disponibilidade da versão**. Links, telas e a documentação atualizada são publicados nas notas de versão na data de lançamento.

Consulte também as [Notas de pré-lançamento da Adobe Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data de lançamento**: 22 de outubro de 2025

### Novos recursos {#oct-25-10-features}



<table>
<thead>
<tr>
<th><strong>Período de silêncio/ Exclusões com base no tempo</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Período de silêncio permite definir exclusões com base no tempo para canais de email, SMS, Push e WhatsApp. Elas garantem que nenhuma mensagem seja enviada durante períodos específicos, ajudando a respeitar as preferências do cliente e os requisitos de conformidade.</p>
<p>É possível aplicar o período de silêncio por meio de conjuntos de regras que podem ser atribuídas a ações individuais em campanhas ou jornadas para obter um controle preciso. Ao simplificar esses processos.</p>
<p>Esse recurso está disponível apenas para um conjunto de organizações (disponibilidade limitada). Para obter acesso, entre em contato com o representante da Adobe.</p>
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
<p>Novos conectores de origem agora estão disponíveis na Adobe Experience Platform para os aplicativos de fidelidade Talon.One, Capillary e Kobie. Esses conectores permitem transmitir dados de fidelidade continuamente para a Adobe Experience Platform e usar esses dados no Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

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
<p>Esse recurso está disponível somente para o canal de email e para organizações que adquiriram a oferta complementar de mensagens transacionais de alta transferência da Adobe. Entre em contato com o representante da Adobe para obter mais informações.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Regras de direcionamento reutilizáveis</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Journey Optimizer agora permite criar regras a partir de um menu da interface dedicado e aproveitá-las ao realizar o direcionamento, como parte da Otimização de conteúdo em uma campanha ou jornada ou na atividade Otimizar jornada.</p>
<p>As regras de direcionamento estão atualmente em Disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.</p>
<p>Observe que esse recurso só está disponível para organizações que adquiriram a oferta complementar da Tomada de decisões. Ele será implantado progressivamente para todos os clientes.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Temas no Designer de email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível aplicar temas pré-aprovados rapidamente para garantir a consistência da marca em todos os emails, acelerar o processo de criação de campanha e produzir emails de alta qualidade de forma independente, reduzindo a dependência de equipes de design.</p>
<p>Lançado anteriormente na versão beta, esse recurso agora está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com o representante da Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Para mais informações, consulte a <a href="../email/apply-email-themes.md">documentação detalhada</a></p>
<!--p>Availability date: October 22, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Novos alertas de jornada</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Novos alertas pré-configurados estão disponíveis para monitorar a execução da jornada:</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Taxa de descarte de perfil excedida</a>: a proporção de descartes de perfil em relação aos perfis inseridos nos últimos 5 minutos excedeu o limite.</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Taxa de erros de ação personalizada excedida</a>: a proporção de erros de ação personalizada em relação às chamadas HTTP bem-sucedidas nos últimos cinco minutos excedeu o limite</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Taxa de erro de perfil excedida</a>: a proporção de perfis com erro em relação aos perfis inseridos nos últimos cinco minutos excedeu o limite.</li></ul> <p>É possível modificar os valores limite e assinar alertas individuais em nível de jornada em vez de alertas globais.</p>
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
<p>Uma nova função auxiliar "executionMetadata" está disponível no editor de personalização. Ela permite anexar informações contextuais a qualquer ação nativa e capturá-las em um conjunto de dados para exportação a sistemas externos.</p>
<p>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.</p>
<p>Para mais informações, consulte a <a href="../personalization/functions/helpers.md#execution-metadata">documentação detalhada</a></p>
<p>Data de disponibilidade: 13 de outubro de 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>O Experimentation Agent está aqui!</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Viabilizado pelo <a href="https://experienceleague.adobe.com/pt-br/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, o agente de experimentação está disponível no Journey Optimizer.  </p>
<p>O Experimentation Agent é uma ferramenta viabilizada por IA que moderniza a execução e o gerenciamento de experimentos digitais em sites, emails, mensagens por push e aplicativos. Ele ajuda a executar experimentos com mais eficiência, organizar metas de negócios e gerar insights acionáveis, destacando o que funcionou, o que não funcionou e onde experimentar em seguida.</p>
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

**Tomada de decisões em emails por meio de modelos de IA**

Agora é possível usar modelos de IA para otimizar o melhor conteúdo do email por meio da Tomada de decisões. Por exemplo, esse recurso permite otimizar o melhor conteúdo com base em eventos personalizados como compras, cliques de botão, adicionar ao carrinho, etc.

**Campo de execução para o canal do WhatsApp**

Além de email e SMS, é possível atualizar o campo de execução padrão para as entregas do WhatsApp no nível da sandbox. Também é possível substituir o campo de execução definido globalmente, alterando-o nos parâmetros avançados da atividade de jornada do WhatsApp ou na configuração do canal do WhatsApp. <!-- [Read more](../FILE.md) -->

**Suporte a atributos personalizados para endereço Mailto (cancelar assinatura)**

Com o Journey Optimizer, se você estiver gerenciando consentimento fora da Adobe, é possível configurar pontos de acesso externos personalizados por definir seu próprio link de cancelamento de assinatura com um clique e um endereço de email de cancelamento de assinatura personalizado na configuração de email. Quando os destinatários clicam no link para cancelar a assinatura, o Journey Optimizer anexa alguns parâmetros padrão específicos do perfil ao evento de atualização de consentimento.

Para customizar ainda mais os pontos de acesso personalizados, agora é possível definir atributos personalizados que também serão anexados ao evento de consentimento. [Leia mais](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Esse recurso já está disponível para o **[!UICONTROL URL de cancelamento de assinatura com um clique]** personalizado desde agosto de 2025 e agora foi lançado para a opção **[!UICONTROL Mailto (cancelar assinatura)]** em disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Data de disponibilidade: 6 de outubro de 2025