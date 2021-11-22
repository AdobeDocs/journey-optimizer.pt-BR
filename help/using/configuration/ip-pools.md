---
title: Criar pools de IP
description: '"Saiba como gerenciar ip-pools"'
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
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 7d7c1b72530d99b8cceb1067f2576ad66c0052a6
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---

# Criar pools de IP

## Sobre pools de IP {#about-ip-pools}

Com o Journey Optimizer, você pode criar pools de IP para agrupar os endereços IP dos subdomínios.

A criação de pools de IP é altamente recomendável para a capacidade de delivery de email. Ao fazer isso, é possível evitar que a reputação de um subdomínio afete seus outros subdomínios.

Por exemplo, uma prática recomendada é ter um pool de IP para suas mensagens de marketing e outro para suas mensagens transacionais. Dessa forma, se uma de suas mensagens de marketing tiver um desempenho ruim e for declarada como spam por um cliente, isso não afetará as mensagens transacionais enviadas para esse mesmo cliente, que ainda receberá mensagens transacionais (confirmações de compra, mensagens de recuperação de senha etc.).

## Criar um pool IP {#create-ip-pool}

Para criar um pool IP, siga estas etapas:

1. Acesse o **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** , em seguida, clique em **[!UICONTROL Create IP Pool]**.

   ![](../assets/ip-pool-create.png)

1. Forneça um nome e uma descrição (opcional) para o pool de IP.

   >[!NOTE]
   >
   >O nome do subdomínio deve começar com uma letra (A-Z) e incluir somente caracteres alfanuméricos ou caracteres especiais ( _, ., - ).

1. Selecione os endereços IP a serem incluídos no pool na lista suspensa e clique em **[!UICONTROL Submit]**.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Todos os endereços IP provisionados com sua instância estão disponíveis na lista.

O pool IP agora é criado e exibido na lista. Você pode selecioná-la para acessar suas propriedades e exibir a predefinição de mensagem associada. Para obter mais informações sobre como associar uma predefinição de mensagem a um pool de IP, consulte [esta seção](message-presets.md)).

![](../assets/ip-pool-created.png)

## Editar um pool de IP {#edit-ip-pool}

Para editar um pool IP:

1. Na lista, clique no nome do pool de IP para abri-lo.

   ![](../assets/ip-pool-list.png)

1. Edite as propriedades conforme desejado. Você pode modificar a descrição e adicionar ou remover endereços IP.

   ![](../assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Continue com muito cuidado ao considerar a exclusão de um IP, pois isso colocará carga adicional nos outros IPs e poderá ter impactos graves na capacidade de entrega. Em caso de dúvida, entre em contato com um especialista em deliverability.

1. Salve as alterações.

>[!NOTE]
>
>O nome do pool IP não é editável. Se quiser modificá-lo, é necessário excluir o pool de IP e criar outro com o nome de sua escolha.

A atualização entra em vigor imediatamente ou de forma assíncrona, dependendo do pool de IP que está sendo associado a um [predefinição de mensagem](message-presets.md) ou não:

* Se o pool IP for **not** selecionada em uma predefinição de mensagem, a atualização é instantânea (**[!UICONTROL Success]** status).
* Se o pool IP **é** selecionada em uma predefinição de mensagem, a atualização pode demorar de 7 a 10 dias úteis (**[!UICONTROL Processing]** status).

<!--If a message preset has been associated with the IP pool, you first need to remove it before editing the IP pool. Once the your modifications have been done, you can associate the message preset again.-->

Para verificar o status de atualização do pool de IP, clique no botão **[!UICONTROL More actions]** e selecione **[!UICONTROL Recent updates]**.

![](../assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Depois que um Pool de IP for atualizado com êxito, talvez seja necessário aguardar:
>* alguns minutos antes de ser consumido pelas mensagens unitárias,
>* até o próximo lote para que o pool de IP seja eficaz em mensagens em lote.


Também é possível usar a variável **[!UICONTROL Delete]** para excluir um pool IP. Observe que não é possível excluir um pool de IP que foi associado a uma predefinição de mensagem.

