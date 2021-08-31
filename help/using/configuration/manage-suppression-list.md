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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 260513cd966ab8e579fa0af0fec0376110d0b53f
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 3%

---


# Gerenciar a lista de supressão {#manage-suppression-list}

Com [!DNL Journey Optimizer], você pode monitorar todos os endereços de email que são excluídos automaticamente do envio em uma jornada, como:

* Endereços inválidos (devoluções permanentes).
* Endereços que consistentemente dão soft-bounce e podem afetar negativamente sua reputação de email se você continuar a incluí-los em seus deliveries.
* Recipients que emitem uma reclamação de spam de algum tipo contra uma de suas mensagens de email.

Esses endereços de email são coletados automaticamente na lista de supressão **do Journey Optimizer**. Saiba mais sobre o conceito e o uso da lista de supressão [nesta seção](../suppression-list.md).

## Acessar a lista de supressão {#access-suppression-list}

Para acessar a lista detalhada de endereços de email excluídos, vá para **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** e selecione **[!UICONTROL Suppression list]**.

>[!CAUTION]
>
>As permissões para visualizar, exportar e gerenciar a lista de supressão estão restritas a [Administradores do Jornada](../administration/ootb-product-profiles.md#journey-administrator). Saiba mais sobre como gerenciar os direitos de acesso dos usuários [!DNL Journey Optimizer] em [esta seção](../administration/permissions-overview.md).

<!--![](../assets/suppression-list-link.png)

You can also display the suppression list content using the **[!UICONTROL View suppression list]** link through the **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** menu, but this view does not allow you to edit the list.-->

![](../assets/suppression-list-access.png)

Os filtros estão disponíveis para ajudar você a navegar pela lista.

<!--![](../assets/suppression-list-filters-temp.png)-->

![](../assets/suppression-list-filters.png)

Você pode filtrar no **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]** ou **[!UICONTROL Reason]**. Selecione as opções escolhidas para cada critério. Após a seleção, é possível limpar cada filtro ou todos os filtros exibidos na parte superior da lista.

![](../assets/suppression-list-filtering-example.png)

Se você adicionar manualmente um endereço de email ou um domínio por engano, o botão **[!UICONTROL Delete]** permitirá que você remova essa entrada.

>[!CAUTION]
>
>Nunca use o botão **[!UICONTROL Delete]** para remover domínios ou endereços de email suprimidos.

![](../assets/suppression-list-delete.png)

Excluir um endereço de email ou um domínio da lista de supressão significa que você recomeçará a fazer o delivery para esse endereço ou domínio. Consequentemente, isso pode ter graves impactos na capacidade de entrega e reputação do IP, o que pode eventualmente levar ao bloqueio do seu endereço IP ou domínio de envio. Saiba mais sobre a importância de manter uma lista de supressão em [this section](../suppression-list.md).

>[!NOTE]
>
>Continue com muito cuidado ao considerar a exclusão de qualquer endereço de email ou domínio. Em caso de dúvida, entre em contato com um especialista em deliverability.

Na exibição **[!UICONTROL Suppression list]**, também é possível editar as regras de supressão. [Saiba mais](retries.md)

Para exportar a lista de supressão como um arquivo CSV, selecione o botão **[!UICONTROL Download CSV]** .

![](../assets/suppression-list-download-csv.png)

## Categorias e motivos de supressão {#suppression-categories-and-reasons}

Quando uma mensagem falha ao ser entregue a um endereço de email, [!DNL Journey Optimizer] determina por que o delivery falhou e a associa a um **[!UICONTROL Suppression category]**.

As categorias de supressão são as seguintes:

* **Difícil**: O endereço de email é enviado imediatamente para a lista de supressão.

   >[!NOTE]
   >
   >Quando o erro é o resultado de uma reclamação de spam, ele também se enquadra na categoria **Hard**. O endereço de email do recipient que emitiu a reclamação é enviado imediatamente para a lista de supressão.

* **Suave**: Erros suaves enviam um endereço para a lista de supressão quando o contador de erros atinge o limite. [Saiba mais sobre tentativas](retries.md)

   <!--
    **Ignored**:
    * When the error occurred for a valid email address but is known to be temporary, such as a failed connection attempt or a temporary technical issue, the email address is added to the suppression list once the error counter reaches the limit threshold. [Learn more on retries](retries.md).
    * When the error is the result of a spam complaint, the email address of the recipient who issued the complaint is immediately sent to the suppression list.
    -->

* **Manual**: Você também pode adicionar manualmente um endereço de email ou um domínio à lista de supressão. [Saiba mais](#add-addresses-and-domains)

>[!NOTE]
>
>Saiba mais sobre devoluções temporárias e devoluções permanentes na seção [Delivery failure types](../suppression-list.md#delivery-failures).

Para cada endereço de email listado, você também pode verificar **[!UICONTROL Type]** (email ou domínio), **[!UICONTROL Reason]** para excluí-lo, quem o adicionou e a data/hora em que ele foi adicionado à lista de supressão.

![](../assets/suppression-list.png)

Os possíveis motivos para uma falha de delivery são:

| Motivo | Descrição | Categoria de supressão |
| --- | --- | --- |
| **[!UICONTROL Invalid Recipient]** | O recipient é inválido ou não existe. | Grave |
| **[!UICONTROL Soft Bounce]** | A mensagem retornou por um motivo diferente dos erros suaves listados nesta tabela, como ao enviar pela taxa permitida recomendada por um ISP. | Suave |
| **[!UICONTROL DNS Failure]** | A mensagem retornou devido a uma falha de DNS. | Suave |
| **[!UICONTROL Mailbox Full]** | A mensagem retornou devido à caixa de entrada do recipient estar cheia e não poder aceitar mais mensagens. | Suave |
| **[!UICONTROL Relaying Denied]** | A mensagem foi bloqueada pelo receptor porque a retransmissão não é permitida. | Suave |
| **[!UICONTROL Challenge-Response]** | A mensagem é um teste de resposta a desafio. | Suave |
| **[!UICONTROL Spam Complaint]** | A mensagem foi bloqueada porque foi marcada como spam pelo recipient. | Grave |

>[!NOTE]
>
>Os usuários sem assinatura não estão recebendo emails de [!DNL Journey Optimizer], portanto, seus endereços de email não podem ser enviados para a lista de supressão. A escolha é feita no nível do Experience Platform. [Saiba mais sobre a opção de não participação](../consent.md)

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Undetermined]** | The bounce reason received from the recipient domain Message Transfer Agent (MTA) could not be identified. | Ignored |
| **[!UICONTROL Too Large]** | The message bounced because it was too large for the recipient. [Retries](retries.md) will be performed: you can edit the message size and re-inject it for delivery. | Ignored |
| **[!UICONTROL Timeout]** | The message timed out, meaning it soft bounced and reached the message retry limit (3.5 days). | Ignored |
| **[!UICONTROL Admin Failure]** | The message was failed according to the policies configured by the sending system administrator. ///For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used. | Ignored |
| **[!UICONTROL Generic Bounce: No RCPT]** | No recipient could be determined for the message. | Ignored |
| **[!UICONTROL Generic Bounce]** | The message failed for unspecified reasons. | Ignored |
| **[!UICONTROL Mail Block]** | The message was blocked by the receiver (i.e. recipient MTA). | Ignored |
| **[!UICONTROL Spam Block]** | The message was blocked by the receiver as coming from a known spam source. It could be a sending IP block for example. | Ignored |
| **[!UICONTROL Spam Content]** | The message content was blocked by the receiver (recipient MTA) as spam. | Ignored |
| **[!UICONTROL Prohibited Attachment]** | The message was blocked by the receiver because it contained an attachment. | Ignored |
| **[!UICONTROL Auto-Reply]** | The message is an auto-reply/vacation mail. | Ignored |
| **[!UICONTROL Transient Failure]** | Message transmission has been temporarily delayed. | Ignored |
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list.-->

## Adicionar endereços e domínios manualmente {#add-addresses-and-domains}

Quando uma mensagem falha ao ser entregue a um endereço de email, esse endereço é adicionado automaticamente à lista de supressão com base na regra de supressão definida ou na contagem de rejeição.

No entanto, você também pode preencher manualmente a lista de supressão [!DNL Journey Optimizer] para excluir domínios e/ou endereços de email específicos do seu envio.

Você pode adicionar endereços de email ou domínios [um de cada vez](#add-one-address-or-domain) ou [no modo em massa](#upload-csv-file) por meio de um upload de arquivo CSV.

Para fazer isso, selecione o botão **[!UICONTROL Add email or domain]** e siga um dos métodos abaixo.

![](../assets/suppression-list-add-email.png)

### Adicionar um endereço ou domínio {#add-one-address-or-domain}

1. Selecione a opção **[!UICONTROL One by one]**.

   ![](../assets/suppression-list-add-email-address.png)

1. Escolha o tipo de endereço: **[!UICONTROL Email address]** ou **[!UICONTROL Domain address]**.

1. Insira o endereço de email ou domínio que deseja excluir do envio.

   >[!NOTE]
   >
   >Certifique-se de inserir um endereço de email válido (como abc@company) ou domínio (como abc.company.com).

1. Especifique um motivo, se necessário.

1. Clique em **[!UICONTROL Submit]**.

### Fazer upload de um arquivo CSV {#upload-csv-file}

1. Selecione a opção **[!UICONTROL Upload CSV]**.

   ![](../assets/suppression-list-upload-csv.png)

1. Baixe o modelo CSV a ser usado, que inclui as colunas e o formato abaixo:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```
   Também é possível baixar esse modelo na visualização principal **[!UICONTROL Suppression list]**.

   >[!CAUTION]
   >
   >Não altere os nomes das colunas no modelo CSV.
   >
   >O tamanho do arquivo não deve exceder 1 MB.

1. Preencha o modelo CSV com os endereços de email e/ou domínios que deseja adicionar à lista de supressão.

1. Depois de concluído, arraste e solte seu arquivo CSV e clique em **[!UICONTROL Upload file]**.

   ![](../assets/suppression-list-upload-file-button.png)

1. Clique em **[!UICONTROL Submit]**.

### Verificar o status de uploads recentes {#recent-uploads}

Você pode verificar a lista dos arquivos CSV mais recentes que você carregou.

Para fazer isso, na visualização **[!UICONTROL Suppression list]**, clique no botão **[!UICONTROL Recent uploads]**.

![](../assets/suppression-list-recent-uploads-button.png)

Os uploads mais recentes enviados e seus status correspondentes são exibidos.

Se um relatório de erros estiver associado a um arquivo, é possível baixá-lo para verificar os erros encontrados.

![](../assets/suppression-list-recent-uploads-error.png)

Abaixo está um exemplo do tipo de entradas que você pode encontrar no relatório de erro:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```



