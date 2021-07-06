---
title: Gerenciar a lista de supressão
description: 'Saiba como acessar e gerenciar a lista de supressão do Journey Optimizer '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Configurações do aplicativo
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 5%

---


# Gerenciar a lista de supressão {#manage-suppression-list}

Com [!DNL Journey Optimizer], você pode monitorar todos os endereços de email que são excluídos automaticamente do envio em uma jornada, como:

* Endereços inválidos (devoluções permanentes) ou que retornam consistentemente e podem afetar negativamente sua reputação do email se você continuar a incluí-los nos deliveries.
* Recipients que emitem uma reclamação de spam de algum tipo contra uma de suas mensagens de email.

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Esses endereços de email são coletados automaticamente na lista de supressão **do Journey Optimizer**. Saiba mais [nesta seção](../suppression-list.md).

## Acessar a lista de supressão {#access-suppression-list}

Para acessar a lista detalhada de endereços de email excluídos, abra o menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** e clique no link **[!UICONTROL View suppression lists]**.

![](../assets/suppression-list-link.png)

Os filtros estão disponíveis para ajudar você a navegar pela lista.

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## Categorias e motivos de supressão {#suppression-categories-and-reasons}

Quando uma mensagem falha ao ser entregue a um endereço de email, o Journey Optimizer determina por que o delivery falhou e a associa a uma categoria de supressão.

As categorias de supressão são as seguintes:

* **Difícil**: O endereço de email é enviado imediatamente para a lista de supressão.

* **Suave**: Erros suaves enviam um endereço para a lista de supressão quando o contador de erros atinge o limite. [Saiba mais sobre tentativas](retries.md)

* **Ignorado**:
   * Quando o erro ocorreu para um endereço de email válido, mas é conhecido como temporário, como uma tentativa de conexão com falha ou um problema técnico temporário, o endereço de email é adicionado à lista de supressão assim que o contador de erros atingir o limite. [Saiba mais sobre tentativas](retries.md).
   * Quando o erro é o resultado de uma reclamação de spam, o endereço de email do recipient que emitiu a reclamação é enviado imediatamente para a lista de supressão.

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>Saiba mais sobre devoluções temporárias e devoluções permanentes na seção [Delivery failure types](../suppression-list.md#delivery-failures).

Para cada endereço de email listado, você também pode verificar **[!UICONTROL Reason]** para excluí-lo e a data/hora em que ele foi adicionado à lista de supressão.

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

Os possíveis motivos para uma falha de delivery são:

| Motivo | Descrição | Categoria de supressão |
---------|----------|--------- |
| **[!UICONTROL Undetermined]** | Não foi possível identificar o motivo da devolução recebido do Agente de Transferência de Mensagens (MTA) do domínio de recipient. | Ignorado |
| **[!UICONTROL Invalid Recipient]** | O recipient é inválido ou não existe. | Grave |
| **[!UICONTROL Soft Bounce]** | A mensagem retornou por um motivo diferente dos erros suaves listados nesta tabela, como ao enviar pela taxa permitida recomendada por um ISP. | Suave |
| **[!UICONTROL DNS Failure]** | A mensagem retornou devido a uma falha de DNS. | Suave |
| **[!UICONTROL Mailbox Full]** | A mensagem retornou devido à caixa de entrada do recipient estar cheia e não poder aceitar mais mensagens. | Suave |
| **[!UICONTROL Too Large]** | A mensagem retornou porque era muito grande para o recipient. [](retries.md) As verificações serão realizadas: você pode editar o tamanho da mensagem e reinjetá-la para entrega. | Ignorado |
| **[!UICONTROL Timeout]** | A mensagem atingiu o tempo limite, o que significa que ela retornou e atingiu o limite de nova tentativa de mensagem (3,5 dias). | Ignorado |
| **[!UICONTROL Admin Failure]** | A mensagem falhou de acordo com as políticas configuradas pelo administrador do sistema de envio. <!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | Ignorado |
| **[!UICONTROL Generic Bounce: No RCPT]** | Nenhum recipient pôde ser determinado para a mensagem. | Ignorado |
| **[!UICONTROL Generic Bounce]** | A mensagem falhou por motivos não especificados. | Ignorado |
| **[!UICONTROL Mail Block]** | A mensagem foi bloqueada pelo receptor (ou seja, MTA do recipient). | Ignorado |
| **[!UICONTROL Spam Block]** | A mensagem foi bloqueada pelo receptor como proveniente de uma fonte de spam conhecida. Pode ser um bloco IP de envio, por exemplo. | Ignorado |
| **[!UICONTROL Spam Content]** | O conteúdo da mensagem foi bloqueado pelo receptor (MTA do recipient) como spam. | Ignorado |
| **[!UICONTROL Prohibited Attachment]** | A mensagem foi bloqueada pelo receptor porque continha um anexo. | Ignorado |
| **[!UICONTROL Relaying Denied]** | A mensagem foi bloqueada pelo receptor porque a retransmissão não é permitida. | Suave |
| **[!UICONTROL Auto-Reply]** | A mensagem é um email de resposta automática/de férias. | Ignorado |
| **[!UICONTROL Transient Failure]** | A transmissão de mensagens foi temporariamente adiada. | Ignorado |
| **[!UICONTROL Challenge-Response]** | A mensagem é um teste de resposta a desafio. | Suave |

>[!NOTE]
>
>Os usuários sem assinatura não estão recebendo emails de [!DNL Journey Optimizer], portanto, seus endereços de email não podem ser enviados para a lista de supressão. A escolha é feita no nível do Experience Platform. Saiba mais sobre [opt-out](../consent.md).

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


