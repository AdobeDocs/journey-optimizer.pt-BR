---
solution: Journey Optimizer
product: journey optimizer
title: Registros PTR
description: Saiba como gerenciar registros PTR
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 1%

---

# Registros PTR {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="Registros PTR de subdomínios"
>abstract="Um registro de ponteiro (PTR) é um tipo de registro DNS que fornece o nome de domínio vinculado a um endereço IP, o que ajuda os servidores de email de recebimento a verificar os endereços IP dos remetentes. Edite apenas um registro de PTR após considerações e discussões apropriadas com seu especialista em deliverability."

## Sobre registros PTR {#about-ptr-records}

Um registro de ponteiro (PTR) é um tipo de registro de Sistema de Nome de Domínio (DNS) que fornece o nome de domínio vinculado a um endereço IP.

Com registros PTR, os servidores de email de recebimento podem verificar a autenticidade do envio de servidores de email identificando se seus endereços IP correspondem aos nomes aos quais os servidores se conectam.

## Acesse os registros PTR dos subdomínios {#access-ptr-records}

Uma vez [um subdomínio é delegado](delegate-subdomain.md) no Adobe Journey Optimizer, um registro PTR é criado e associado automaticamente a este subdomínio. Você pode acessá-lo pelo **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Configuração de email]** > **[!UICONTROL Registros PTR]** menu.

![](assets/ptr-records.png)

A lista mostra os registros PTR gerados para cada subdomínio delegado, usando a sintaxe abaixo:

* &quot;r&quot; para registro,
* &quot;xx&quot; para os dois últimos algarismos do endereço IP,
* nome do subdomínio.

Você pode abrir um registro PTR na lista para exibir o nome do subdomínio associado e o endereço IP.

## Editar um registro PTR {#edit-ptr-record}

Você pode modificar um registro PTR para editar o subdomínio associado a um endereço IP.

>[!CAUTION]
>
>Continue com muito cuidado ao editar registros de PTR. Em caso de dúvidas, entre em contato com um especialista em capacidade de delivery.<!--why?-->

>[!NOTE]
>
>Não é possível modificar o **[!UICONTROL IP]** e **[!UICONTROL Registro PTR]** campos.

### Subdomínios totalmente delegados {#fully-delegated-subdomains}

Para editar um registro PTR com um subdomínio que esteja [plenamente delegado](delegate-subdomain.md#full-subdomain-delegation) para o Adobe, siga as etapas abaixo.

1. Na lista, clique em um nome de registro PTR para abri-lo.

   ![](assets/ptr-record-select.png)

1. Selecionar um subdomínio [plenamente delegado](delegate-subdomain.md#full-subdomain-delegation) para Adobe da lista.

   ![](assets/ptr-record-subdomain.png)

1. Clique em **[!UICONTROL Salvar]** para confirmar as alterações.

### Subdomínios delegados usando o método CNAME {#edit-ptr-subdomains-cname}

Para editar um registro PTR com um subdomínio que é delegado ao Adobe usando o [método CNAME](delegate-subdomain.md#cname-subdomain-delegation)siga as etapas abaixo.

1. Na lista, clique em um nome de registro PTR para abri-lo.

   ![](assets/ptr-record-select-cname.png)

1. Selecione um subdomínio delegado ao Adobe usando o [método CNAME](delegate-subdomain.md#cname-subdomain-delegation) na lista.

   ![](assets/ptr-record-subdomain-cname.png)

1. Você precisa criar um novo registro de DNS de encaminhamento na plataforma de hospedagem. Para fazer isso, copie o registro gerado pelo Adobe. Depois de concluído, marque a caixa &quot;Confirmo...&quot;.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Caso receba esta mensagem: &quot;Crie o DNS de encaminhamento primeiro e tente novamente&quot;, siga as etapas abaixo:
   >   * Verifique o provedor DNS se o registro de DNS de encaminhamento foi criado com êxito.
   >   * Os registros no DNS podem não sincronizar imediatamente. Aguarde alguns minutos e tente novamente.


1. Clique em **[!UICONTROL Salvar]** para confirmar as alterações.

## Verificar detalhes de atualização do registro PTR {#check-ptr-record-update}

Depois de confirmar a edição do registro PTR, a variável **[!UICONTROL Processamento]** ícone é exibido ao lado do nome do registro PTR na lista.

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>O [processamento de atualização](#processing) pode levar até 3 horas.

Para verificar os detalhes de atualização do registro PTR, clique no ícone ao lado dele. Saiba mais sobre os status associados aos diferentes ícones em [esta seção](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

Você pode ver informações como o status da atualização e as alterações solicitadas.

![](assets/ptr-record-updates.png)

## Status de atualização de registro PTR {#ptr-record-update-statuses}

Uma atualização de registro PTR pode ter os seguintes status:

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL Processamento]**: A atualização do registro PTR foi enviada e está passando por um processo de verificação.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Sucesso]**: O registro PTR atualizado foi verificado e o novo subdomínio agora está associado ao endereço IP.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Falha]**: Uma ou várias verificações falharam durante a verificação de atualização de registro PTR.

### Processamento {#processing}

Várias verificações de deliverability serão executadas para verificar se o novo subdomínio a ser associado ao endereço IP é válido. Isso pode levar até 3 horas.

>[!NOTE]
>
>Não é possível modificar um registro PTR enquanto a atualização estiver em curso. Você ainda pode clicar no nome, mas a variável **[!UICONTROL Subdomínio]** está acinzentado. As alterações não serão refletidas até que a atualização seja bem-sucedida.

Durante o processo de validação, o subdomínio antigo ainda estará associado ao endereço IP.

### Sucesso {#success}

Depois que o processo de validação for bem-sucedido, o novo subdomínio será associado automaticamente ao endereço IP.

### Falha {#failes}

Se o processo de validação falhar, o registro PTR mais antigo será exibido. O subdomínio válido que foi associado anteriormente ao endereço IP permanece inalterado.

Os possíveis tipos de erro de atualização são os seguintes:
* Falha ao criar um novo DNS de encaminhamento para o registro PTR
* Falha ao atualizar o registro
* Falha na reintegração das afinidades

Quando a atualização falhar, o registro PTR poderá ser editado novamente. Você pode clicar em seu nome e atualizar o subdomínio novamente.
