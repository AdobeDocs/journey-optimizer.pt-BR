---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar a lista de supressão
description: Saiba como acessar e gerenciar a lista de supressão do Journey Optimizer
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: supressão, lista, rejeição, email, otimizador, quarentena
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 0ba1af43f5447df861e419b56f34a418cfbce241
workflow-type: tm+mt
source-wordcount: '1599'
ht-degree: 21%

---

# Gerenciar a lista de supressão {#manage-suppression-list}

Com [!DNL Journey Optimizer], você pode monitorar todos os endereços de email que são excluídos automaticamente do envio de uma jornada ou campanha, como rejeições permanentes, rejeições temporárias e reclamações de spam.

Esses endereços de email são coletados automaticamente na Journey Optimizer **lista de supressão**. Uma lista de supressão consiste em endereços e domínios a serem excluídos de seus públicos-alvo. Ele reúne endereços de email e domínios que são suprimidos em todas as correspondências em um único ambiente de cliente, o que significa que são específicos para uma ID de organização associada a uma ID de sandbox.

Saiba mais sobre o conceito e o uso da lista de supressão no [nesta seção](../reports/suppression-list.md).

>[!NOTE]
>
>O Adobe mantém uma lista atualizada de endereços inválidos conhecidos que comprovadamente prejudicam a reputação de engajamento e mala direta e garante que os emails não sejam entregues a eles. Essa lista é gerenciada em uma lista de supressão global comum a todos os clientes da Adobe. Os endereços e os nomes de domínio contidos na lista de supressão global estão ocultos. Somente o número de destinatários excluídos é indicado nos relatórios de entrega.

Além disso, você pode aproveitar o Journey Optimizer **API REST de supressão** para controlar as mensagens de saída usando supressão e listas de permissões. [Saiba como trabalhar com a API REST de supressão](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Acessar a lista de supressão {#access-suppression-list}

Para acessar a lista detalhada de domínios e endereços de email excluídos, navegue até **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** e selecione **[!UICONTROL Lista de supressão]**.


![](assets/suppression-list-access.png)

>[!CAUTION]
>
>As permissões para exibir, exportar e gerenciar a lista de supressão são restritas a [Administradores do Jornada](../administration/ootb-product-profiles.md#journey-administrator). Saiba mais sobre gerenciamento [!DNL Journey Optimizer] direitos de acesso dos usuários no [nesta seção](../administration/permissions-overview.md).


Há filtros disponíveis para ajudar na navegação pela lista.

![](assets/suppression-list-filters.png)

Você pode filtrar no campo **[!UICONTROL Categoria de supressão]**, **[!UICONTROL Tipo de endereço]** ou **[!UICONTROL Motivo]**. Selecione uma ou mais opções para cada critério. Depois de selecionado, você pode limpar cada filtro ou todos os filtros exibidos na parte superior da lista.

![](assets/suppression-list-filtering-example.png)


## Entender os motivos de falha {#suppression-categories-and-reasons}

Quando uma mensagem não é entregue a um endereço de email, [!DNL Journey Optimizer] determina por que o delivery falhou e o associa a um **[!UICONTROL Categoria de supressão]**.

As categorias de supressão são as seguintes:

* **Rígido**: uma rejeição permanente indica um endereço de email inválido (ou seja, um endereço de email que não existe). Isso envolve uma mensagem de rejeição do servidor de email de recebimento que declara explicitamente que o endereço é inválido. O endereço de email é enviado imediatamente para a lista de supressão.

  Quando o erro é o resultado de uma reclamação de spam, ele também entra na **Rígido** categoria. O endereço de email do recipient que emitiu a reclamação é enviado imediatamente para a lista de supressão.

* **Suave**: uma rejeição temporária é uma rejeição de email que ocorreu para um endereço de email válido. O endereço de email é adicionado à lista de supressão após várias tentativas. Os erros suaves enviam um endereço para a lista de supressão assim que o contador de erros atinge o limite. [Saiba mais sobre tentativas](retries.md)

* **Manual**: erros manuais foram adicionados manualmente à lista de supressão. [Saiba mais](#add-addresses-and-domains)

Para cada endereço de email listado, você também pode verificar o **[!UICONTROL Tipo]** (email ou domínio), **[!UICONTROL Motivo]** para excluí-lo, quem o adicionou e a data/hora em que foi adicionado à lista de supressão.

![](assets/suppression-list.png)

Os possíveis motivos para uma falha de delivery são:

| Motivo | Descrição | Categoria |
| --- | --- | --- |
| **[!UICONTROL Destinatário inválido]** | O destinatário é inválido ou não existe. | Grave |
| **[!UICONTROL Rejeição leve]** | A mensagem teve rejeição temporária por um motivo diferente dos erros temporários listados nesta tabela, como ao enviar acima da taxa permitida recomendada por um ISP. | Suave |
| **[!UICONTROL Falha de DNS]** | A mensagem foi rejeitada devido a uma falha de DNS. | Suave |
| **[!UICONTROL Caixa de entrada cheia]** | A mensagem foi rejeitada porque a caixa de entrada do destinatário está cheia e não pode receber mais mensagens. | Suave |
| **[!UICONTROL Retransmissão negada]** | A mensagem foi bloqueada pelo destinatário porque a retransmissão não é permitida. | Suave |
| **[!UICONTROL Desafio-resposta]** | A mensagem é uma prova de desafio-resposta. | Suave |
| **[!UICONTROL Reclamação de spam]** | A mensagem foi bloqueada porque foi marcada como spam pelo destinatário. | Grave |

>[!NOTE]
>
>Os usuários que cancelaram a inscrição não estão recebendo emails do [!DNL Journey Optimizer], portanto, seus endereços de email não podem ser enviados para a lista de supressão. Sua escolha é feita no nível da Experience Platform. [Saiba mais sobre recusa](../privacy/opt-out.md)


### Regras de supressão  {#suppression-rules}

No **[!UICONTROL Lista de supressão]** também é possível editar o parâmetro de nova tentativa associado às regras de supressão do **[!UICONTROL Editar regras de supressão]** botão. Use essa opção para atualizar o limite de novas tentativas da sandbox atual. [Saiba mais sobre tentativas](retries.md).


## Adicionar endereços e domínios à lista de supressão{#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_header"
>title="Adicionar emails ou domínios à lista de supressão"
>abstract="Você pode preencher manualmente a lista de supressão do Journey Optimizer para excluir domínios e/ou endereços de email específicos do envio."

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="Adicionar emails ou domínios à lista de supressão"
>abstract="Para preencher a lista de supressão, é possível adicionar manualmente endereços de email ou domínios: um de cada vez ou no modo em massa por meio de um upload de arquivo CSV. Esses domínios e/ou endereços de email específicos serão excluídos do envio."

Quando ocorre uma falha na entrega de uma mensagem a um endereço de email, esse endereço é adicionado automaticamente à lista de supressão com base na regra de supressão definida ou na contagem de rejeição.

No entanto, também é possível preencher manualmente a variável [!DNL Journey Optimizer] lista de supressão para excluir domínios e/ou endereços de email específicos do seu envio.

>[!NOTE]
>
>Pode levar até 60 minutos para [!DNL Journey Optimizer] para considerar os endereços suprimidos nos emails de saída.

Você pode adicionar os endereços de email ou domínios [um de cada vez](#add-one-address-or-domain) ou [em massa](#upload-csv-file) por meio do upload de um arquivo CSV.

### Adicionar um endereço ou domínio {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="Adicionar um item à lista de supressão"
>abstract="Você pode preencher a lista de supressão adicionando endereços de email e/ou domínios, um por um."

Para adicionar um endereço de email ou um domínio à lista de supressão, siga as etapas abaixo:

1. Selecione o **[!UICONTROL Adicionar email ou domínio]** botão.

   ![](assets/suppression-list-add-email.png)

1. Escolha o **[!UICONTROL Um por um]** opção.

   ![](assets/suppression-list-add-email-address.png)

1. Selecione o tipo de endereço: **[!UICONTROL E-mail]** ou **[!UICONTROL Domínio]**.

1. Insira o endereço de email ou domínio que deseja excluir do envio.

   >[!NOTE]
   >
   >Certifique-se de inserir um endereço de email (como abc@empresa.com) ou de domínio (como abc.empresa.com) válido.

1. (opcional) Informe um motivo. Todos os caracteres ASCII imprimíveis compreendidos entre 32 e 126 são permitidos neste campo.

1. Use o **[!UICONTROL Enviar]** botão para confirmar.

### Fazer upload de um arquivo CSV {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="Fazer upload do CSV para adicionar itens à lista de supressão"
>abstract="Você pode preencher a lista de supressão carregando um arquivo CSV preenchido com os endereços de email/domínios que deseja excluir."

Para adicionar um grupo de endereços de email ou um domínio à lista de supressão, siga as etapas abaixo:

1. Selecione o **[!UICONTROL Adicionar email ou domínio]** botão.
1. Escolha o **[!UICONTROL Fazer upload de CSV]** opção.

   ![](assets/suppression-list-upload-csv.png)

1. Baixe o modelo CSV a ser usado, que inclui as colunas e o formato abaixo:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```

1. Preencha o modelo CSV com os endereços de email e/ou domínios que serão adicionados à lista de supressão. Todos os caracteres ASCII imprimíveis compreendidos entre 32 e 126 são permitidos na **COMENTÁRIO** coluna.

   >[!CAUTION]
   >
   >Não altere o nome das colunas no modelo CSV.
   >
   >O tamanho do arquivo não pode exceder a 1 MB.
   >

1. Depois de concluído, arraste e solte seu arquivo CSV e use o **[!UICONTROL Enviar]** botão para confirmar.

   ![](assets/suppression-list-upload-csv-submit.png)

Quando o upload estiver concluído, você poderá verificar seu status no [Uploads recentes](#recent-uploads) conforme detalhado abaixo.

### Verificar status dos uploads {#recent-uploads}

Use o **[!UICONTROL Uploads recentes]** botão para verificar o status dos arquivos CSV carregados mais recentemente.

![](assets/suppression-list-recent-uploads-button.png)

Os status possíveis são:

* **[!UICONTROL Pendente]**: o upload do arquivo está sendo processado.
* **[!UICONTROL Erro]**: o processo de upload do arquivo falhou devido a um problema técnico ou a um erro no formato do arquivo.
* **[!UICONTROL Concluído]**: o processo de upload de arquivo foi concluído com sucesso.

Durante o upload, se alguns endereços não estiverem no formato correto, eles não serão adicionados ao [!DNL Journey Optimizer] lista de supressão.

Nesse caso, quando o upload é concluído, ele é associado a um relatório. Você pode baixá-lo para verificar os erros encontrados<!-- and understand why they were not added to the suppression list-->.

![](assets/suppression-list-recent-uploads-report.png)

Veja abaixo um exemplo dos tipos de entradas que você pode encontrar no relatório de erros:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```

## Remover um endereço da lista de supressão{#remove-from-suppression-list}

Você pode atualizar manualmente a lista de supressão. A remoção de um endereço de email da quarentena é uma operação delicada e pode afetar a reputação do IP e as taxas de capacidade de delivery. Prossiga com cuidado.

Ao excluir um endereço de email ou um domínio da lista de supressão, o Adobe Journey Optimizer pode iniciar novamente a entrega para esse endereço ou domínio.  Saiba mais sobre a capacidade de entrega no [nesta seção](../reports/deliverability.md).

Para remover um endereço da lista de supressão, use o **[!UICONTROL Excluir]** botão.

![](assets/suppression-list-delete.png)


>[!NOTE]
>
>Continue com muito cuidado ao considerar a exclusão de qualquer endereço de email ou domínio. Em caso de dúvidas, entre em contato com um especialista em capacidade de entrega.

Por exemplo, no caso de uma interrupção do provedor de serviços de Internet (ISP), os emails são marcados incorretamente como rejeições permanentes porque não podem ser entregues com êxito ao recipient. Esses endereços de email devem ser removidos da lista de supressão.

Para recuperar esses endereços, execute uma consulta específica com parâmetros personalizados, com base no contexto da interrupção. [Saiba mais neste exemplo](../data/datasets-query-examples.md#isp-outage-query).

Depois que os endereços de email afetados forem identificados, filtre a lista de supressão para exibi-los. Por exemplo, se uma interrupção de ISP tiver ocorrido de 11 de novembro de 2022 a 13 de novembro de 2022 no **test.com** domínio, filtre os endereços adicionados à lista de supressão nesse período, conforme abaixo:

![](assets/remove-from-supp-list.png)

Você pode remover endereços de email em quarentena da lista de supressão usando o **[!UICONTROL Excluir]** botão.

## Baixar a lista de supressão {#download-suppression-list}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_download"
>title="Export the list as a CSV file"
>abstract="To download the suppression list, Qou can either export the current list by generating a new file, or download the file that was previously generated."
-->

Para exportar a lista de supressão como um arquivo CSV, siga as etapas abaixo:

1. Selecione o **[!UICONTROL Baixar CSV]** botão.

   ![](assets/suppression-list-download-csv.png)

1. Espere até que o arquivo seja gerado.

   ![](assets/suppression-list-download-generate.png)

   >[!NOTE]
   >
   >O tempo de download depende do tamanho do arquivo, o que significa o número de endereços que estão na lista de supressão.
   >
   >Uma solicitação de download pode ser processada de cada vez para uma determinada sandbox.

1. Depois que o arquivo for gerado, você receberá uma notificação. Clique no ícone de sino na parte superior direita da tela para exibi-lo.

1. Clique na própria notificação para baixar o arquivo.

   ![](assets/suppression-list-download-notification.png)

   >[!NOTE]
   >
   >O link é válido por 24 horas.

<!--When downloading the CSV file, you can choose to either:

* Download the file that was previously generated by another user or yourself.

* Generate a new file in order to export the current suppression list.-->