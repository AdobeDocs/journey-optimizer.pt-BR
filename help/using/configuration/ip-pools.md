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
feature: Configurações do aplicativo
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Criar pools de IP

## Sobre pools de IP

Com o Journey Optimizer, você pode criar pools de IP para agrupar os endereços IP dos subdomínios.

A criação de pools de IP é altamente recomendável para a capacidade de delivery de email. Ao fazer isso, é possível evitar que a reputação de um subdomínio afete seus outros subdomínios.

Por exemplo, uma prática recomendada é ter um pool de IP para suas mensagens de marketing e outro para suas mensagens transacionais. Dessa forma, se uma de suas mensagens de marketing tiver um desempenho ruim e for declarada como spam por um cliente, isso não afetará as mensagens transacionais enviadas para esse mesmo cliente, que ainda receberá mensagens transacionais (confirmações de compra, mensagens de recuperação de senha etc.).

## Criar um pool IP

Para criar um pool IP, siga estas etapas:

1. Acesse o menu **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** e clique em **[!UICONTROL Create IP Pool]**.

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

Para editar um pool IP, abra-o e edite suas propriedades conforme desejado.

>[!NOTE]
>
>Se uma predefinição de mensagem tiver sido associada ao pool de IP, primeiro é necessário removê-la antes de editar o pool de IP. Depois que as modificações forem feitas, você poderá associar a predefinição de mensagem novamente.
