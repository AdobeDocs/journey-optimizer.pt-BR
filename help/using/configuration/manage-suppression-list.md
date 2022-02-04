---
title: Gerenciar a lista de supressão
description: Saiba como acessar e gerenciar a lista de supressão do Journey Optimizer
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 3%

---

# Gerenciar a lista de supressão {#manage-suppression-list}

Com [!DNL Journey Optimizer], é possível monitorar todos os endereços de email que são excluídos automaticamente do envio em uma jornada, como:

* Endereços inválidos (devoluções permanentes).
* Endereços que consistentemente dão soft-bounce e podem afetar negativamente sua reputação de email se você continuar a incluí-los em seus deliveries.
* Recipients que emitem uma reclamação de spam de algum tipo contra uma de suas mensagens de email.

Esses endereços de email são coletados automaticamente na Journey Optimizer **lista de supressão**. Saiba mais sobre o conceito e o uso da lista de supressão em [esta seção](../messages/suppression-list.md).

## Acessar a lista de supressão {#access-suppression-list}

Para acessar a lista detalhada de endereços de email excluídos, acesse **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** e selecione **[!UICONTROL Suppression list]**.

>[!CAUTION]
>
>As permissões para visualizar, exportar e gerenciar a lista de supressão estão restritas a [Administradores do Jornada](../administration/ootb-product-profiles.md#journey-administrator). Saiba mais sobre como gerenciar [!DNL Journey Optimizer] direitos de acesso dos usuários em [esta seção](../administration/permissions-overview.md).

![](../assets/suppression-list-access.png)

Os filtros estão disponíveis para ajudar você a navegar pela lista.

![](../assets/suppression-list-filters.png)

Você pode filtrar na variável **[!UICONTROL Suppression category]**, **[!UICONTROL Address type]** ou **[!UICONTROL Reason]**. Selecione as opções escolhidas para cada critério. Após a seleção, é possível limpar cada filtro ou todos os filtros exibidos na parte superior da lista.

![](../assets/suppression-list-filtering-example.png)

Se você adicionar manualmente um endereço de email ou um domínio por engano, a variável **[!UICONTROL Delete]** permite remover essa entrada.

>[!CAUTION]
>
>Nunca use o **[!UICONTROL Delete]** para remover domínios ou endereços de email suprimidos.

![](../assets/suppression-list-delete.png)

Excluir um endereço de email ou um domínio da lista de supressão significa que você recomeçará a fazer o delivery para esse endereço ou domínio. Consequentemente, isso pode ter graves impactos na capacidade de entrega e reputação do IP, o que pode eventualmente levar ao bloqueio do seu endereço IP ou domínio de envio. Saiba mais sobre a importância de manter uma lista de supressão em [esta seção](../messages/suppression-list.md).

>[!NOTE]
>
>Continue com muito cuidado ao considerar a exclusão de qualquer endereço de email ou domínio. Em caso de dúvida, entre em contato com um especialista em deliverability.

No **[!UICONTROL Suppression list]** , também é possível editar as regras de supressão. [Saiba mais](retries.md)

Para exportar a lista de supressão como um arquivo CSV, selecione o **[!UICONTROL Download CSV]** botão.

![](../assets/suppression-list-download-csv.png)

## Categorias e motivos de supressão {#suppression-categories-and-reasons}

Quando uma mensagem não é entregue a um endereço de email, [!DNL Journey Optimizer] determina por que o delivery falhou e associa-o a um **[!UICONTROL Suppression category]**.

As categorias de supressão são as seguintes:

* **Disco rígido**: O endereço de email é enviado imediatamente para a lista de supressão.

   >[!NOTE]
   >
   >Quando o erro é o resultado de uma reclamação de spam, ele também se enquadra no **Disco rígido** categoria . O endereço de email do recipient que emitiu a reclamação é enviado imediatamente para a lista de supressão.

* **Suave**: Erros suaves enviam um endereço para a lista de supressão quando o contador de erros atinge o limite. [Saiba mais sobre tentativas](retries.md)

* **Manual**: Você também pode adicionar manualmente um endereço de email ou um domínio à lista de supressão. [Saiba mais](#add-addresses-and-domains)

>[!NOTE]
>
>Saiba mais sobre devoluções temporárias e devoluções permanentes na [Tipos de falha de delivery](../messages/suppression-list.md#delivery-failures) seção.

Para cada endereço de email listado, você também pode verificar a variável **[!UICONTROL Type]** (email ou domínio), **[!UICONTROL Reason]** para excluí-lo, quem o adicionou e a data/hora em que foi adicionado à lista de supressão.

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
>Usuários sem assinatura não recebem emails de [!DNL Journey Optimizer], portanto, seus endereços de email não podem ser enviados para a lista de supressão. A escolha é feita no nível do Experience Platform. [Saiba mais sobre a opção de não participação](../messages/consent.md)

## Adicionar endereços e domínios manualmente {#add-addresses-and-domains}

Quando uma mensagem falha ao ser entregue a um endereço de email, esse endereço é adicionado automaticamente à lista de supressão com base na regra de supressão definida ou na contagem de rejeição.

No entanto, também é possível preencher manualmente a variável [!DNL Journey Optimizer] lista de supressão para excluir domínios e/ou endereços de email específicos do seu envio.

Você pode adicionar endereços de email ou domínios [uma de cada vez](#add-one-address-or-domain)ou [no modo em massa](#upload-csv-file) por meio de um upload de arquivo CSV.

Para fazer isso, selecione o **[!UICONTROL Add email or domain]** , em seguida, siga um dos métodos abaixo.

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
   Também é possível baixar esse modelo na **[!UICONTROL Suppression list]** visualização principal.

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

Para fazer isso, no **[!UICONTROL Suppression list]** , clique no botão **[!UICONTROL Recent uploads]** botão.

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
