---
solution: Journey Optimizer
product: journey optimizer
title: Notifique os usuários sobre a disponibilidade do produto
description: Notifique os usuários sobre a disponibilidade do produto
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 3%

---

# Notifique os usuários sobre a disponibilidade do produto {#product-availability-uc}

>[!BEGINSHADEBOX]

Este caso de uso mostra o envio em vários níveis: geração de um email distinto para cada item da lista de desejos usando o endereço de email armazenado com o item individual em vez do registro do recipient. Isso permite que os clientes recebam notificações separadas para cada produto em sua lista de desejos, mesmo que usem endereços de email diferentes para itens diferentes.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Crie uma notificação de devolução ao estoque para informar aos clientes quando os itens de sua Lista de desejos estiverem disponíveis novamente. Esta mensagem ajuda a reengajar os clientes interessados e os incentiva a concluir sua compra enquanto o inventário é reabastecido.

1. Comece criando uma nova campanha especificamente direcionada ao reengajamento na Lista de desejos. Isso garante que suas mensagens se concentrem nos clientes que já demonstraram a intenção de compra, salvando os produtos na lista de desejos.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Preencha suas **[!UICONTROL Configurações da campanha]**, como o nome da campanha, a descrição, as datas de início e término e as marcas relevantes.

1. Adicione uma atividade **[!UICONTROL Criar público]** com a Lista de desejos como **[!UICONTROL Dimensão de direcionamento]**.

   ![](assets/notify-1.png){zoomable="yes"}

1. Adicione sua condição para incluir apenas as listas de desejos criadas nos últimos 36 meses.

   ![](assets/notify-2.png){zoomable="yes"}

1. Adicione uma atividade **[!UICONTROL Change dimension]** para alternar das listas de desejos de volta para o respectivo cliente definido para direcionamento.

   ![](assets/notify-3.png){zoomable="yes"}

1. Depois de iniciar o modo de rascunho, visualize o público-alvo com os detalhes da Lista de desejos. Para obter insights mais profundos, clique em um resultado de saída e selecione **[!UICONTROL Visualizar resultados]**.

   Aqui, os dados exibem os recipients e seus itens da Lista de desejos. Alguns clientes têm vários itens da Lista de desejos e, por meio do envio de vários níveis, recebem um email separado para cada item. Em alguns casos, os clientes usam diferentes endereços de email para solicitações de devolução em estoque separadas.

   ![](assets/notify-4.png){zoomable="yes"}

1. Para enviar um email separado para cada item, verifique se [sua configuração de email](../orchestrated/target-dimension.md) está definida com `Recipients - email` como **[!UICONTROL Dimension de Destino de Perfil]** e `Wishlistitems` como **[!UICONTROL Dimensão secundária]**.

   Em seguida, no menu **[!UICONTROL Endereço de Execução]**, selecione `wishlist.email` como **[!UICONTROL Dimensão secundária]**. Cada item da Lista de desejos aciona um email separado, usando o endereço de email armazenado nos dados da Lista de desejos como a dimensão secundária.

   ![](assets/notify-5.png){zoomable="yes"}

1. Adicione uma atividade de **[!UICONTROL Email]** para criar uma mensagem de disponibilidade de produto. Clique em **[!UICONTROL Editar conteúdo]** para começar a criar seu conteúdo.

   ➡️ [Saiba mais sobre personalização de email](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Depois que a campanha for testada e estiver pronta, clique em **[!UICONTROL Publicar]** para colocá-la no ar.

Com essa campanha orquestrada, o cliente recebe um email separado para cada um de seus itens da lista de desejos. Cada mensagem é enviada para o endereço de email específico associado a essa lista de desejos, com conteúdo personalizado extraído dos detalhes desse item específico da lista de desejos.

