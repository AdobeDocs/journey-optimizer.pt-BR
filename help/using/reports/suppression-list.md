---
solution: Journey Optimizer
product: journey optimizer
title: Lista de supressão
description: Saiba como usar a lista de supressão
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 8%

---

# Lista de supressão {#suppression-list}

Uma lista de supressão consiste em endereços e domínios que você deseja excluir de seus deliveries, pois o envio para esses contatos pode prejudicar sua reputação de envio e as taxas de delivery.

O [!DNL Journey Optimizer] a lista de supressão é gerenciada no seu próprio nível de ambiente, ou seja, para uma determinada sandbox.

Ele reúne endereços de email e domínios que são suprimidos em todas as correspondências em um único ambiente de cliente, ou seja, são específicos de uma ID da organização associada a uma ID de sandbox.

>[!NOTE]
>
>O Adobe mantém uma lista atualizada de endereços inválidos conhecidos que comprovadamente são prejudiciais ao engajamento e à reputação de endereçamento, e garante que os emails não sejam entregues a eles. Essa lista é gerenciada em uma lista de supressão global comum a todos os clientes da Adobe. Os endereços e os nomes de domínio contidos na lista de supressão global estão ocultos. Somente o número de destinatários excluídos é indicado nos relatórios de entrega.

## Por que uma lista de supressão? {#why-suppression-list}

Para controlar as mensagens de email recebidas pelos proprietários da caixa de entrada e garantir que elas recebam somente as mensagens desejadas, os provedores de serviços de Internet (ISPs) e os filtros de spam comercial têm seus algoritmos proprietários para rastrear a reputação geral dos remetentes de email com base nos endereços IP e no(s) domínio(s) de envio que usam.

Se você não receber seus comentários (como reclamações de spam, devoluções etc.) em consideração, eles classificarão sua reputação como baixa. A lista de supressão ajuda você a honrar os comentários dos ISPs.

Os recipients cujos endereços de email são suprimidos são excluídos automaticamente do delivery de mensagens. Isso irá acelerar os deliveries, pois a taxa de erro tem um efeito significativo na velocidade do delivery.

## O que está na lista de supressão? {#what-s-on-suppression-list}

Os endereços são adicionados à lista de supressão da seguinte maneira:

* Todos **devoluções permanentes** e **reclamações de spam** envie automaticamente os endereços correspondentes para a lista de supressão após uma única ocorrência.

* **Rejeições suaves** não envie um endereço imediatamente para a lista de supressão, mas incrementam um contador de erros. Vários [tentativas](../configuration/retries.md) são executados e, quando o contador de erros atinge o limite, o endereço é adicionado à lista de supressão.

* Você também pode [**manualmente** adicionar um endereço ou um domínio](../configuration/manage-suppression-list.md#add-addresses-and-domains) à lista de supressão.

Saiba mais sobre devoluções permanentes e devoluções temporárias em [esta seção](#delivery-failures).

>[!NOTE]
>
>Os endereços de usuários sem assinatura não podem ser enviados para a lista de supressão, pois não estão recebendo emails de [!DNL Journey Optimizer]. A escolha é feita no nível do Experience Platform. Saiba mais sobre [opt out](../privacy/opt-out.md).

Para cada endereço, o motivo básico para a supressão e a categoria de supressão (macia, dura etc.) são exibidas na lista de supressão. Saiba mais sobre como acessar e gerenciar a lista de supressão em [esta seção](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Os perfis com **[!UICONTROL Suprimido]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto a variável **Relatórios de Jornada** mostrará esses perfis como tendo sido movidos pela jornada ([Ler segmento](../building-journeys/read-segment.md) e [atividades de mensagem](../building-journeys/journeys-message.md)), **Relatórios de email** não os incluirá no **[!UICONTROL Enviado]** métricas como são filtradas antes do envio do email.
>
>Saiba mais sobre o [Relatório ao vivo](../reports/live-report.md) e [Relatório Global](../reports/global-report.md). Para descobrir o motivo de todos os casos de exclusão, é possível usar a variável [Serviço de query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### Falhas de entrega {#delivery-failures}

Há dois tipos de erros quando um delivery falha:

* **Rejeição permanente**. Uma rejeição permanente indica um endereço de email inválido (ou seja, um endereço de email que não existe). Isso envolve uma mensagem de devolução do servidor de email de recebimento que declara explicitamente que o endereço é inválido.
* **Rejeição suave**. Esta é uma devolução temporária de email que ocorreu para um endereço de email válido.

A **devolução permanente** adiciona automaticamente o endereço de email à lista de supressão.

A **devolução temporária** <!--or an **ignored** error--> que ocorre muitas vezes também envia o endereço de email para a lista de supressão após várias tentativas. [Saiba mais sobre tentativas](../configuration/retries.md)

Se você continuar enviando para esses endereços, isso pode afetar suas taxas de delivery, pois informa aos ISPs que talvez você não esteja seguindo as práticas recomendadas de manutenção da lista de endereços de email e, portanto, pode não ser um remetente confiável.

### Reclamações de spam {#spam-complaints}

A lista de supressão coleta endereços de email que marcam sua mensagem como spam. Por exemplo, se alguém escrever para um serviço de atendimento ao cliente solicitando para nunca receber email novamente de você, o endereço de email dessa pessoa será suprimido em sua instância e você não poderá mais enviar o email para esse endereço.

Enviar para recipients depois que eles enviarem uma reclamação de spam pode ter um grande impacto na sua reputação de envio, porque isso informa aos ISPs que você pode enviar emails indesejados e pode não ouvir seus recipients.

Isso pode fazer com que seu endereço IP ou domínio de envio seja bloqueado, o que pode ser evitado com esses endereços na lista de supressão.
