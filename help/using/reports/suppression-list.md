---
solution: Journey Optimizer
product: journey optimizer
title: Lista de supressão
description: Saiba como usar a lista de supressão é
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 11%

---

# Lista de supressão {#suppression-list}

A lista de supressão consiste em endereços e domínios que você deseja excluir de suas entregas, pois o envio para esses contatos pode prejudicar sua reputação de envio e as taxas de entrega.

A lista de supressão [!DNL Journey Optimizer] é gerenciada em seu próprio nível de ambiente, ou seja, para uma determinada sandbox.

Ele reúne endereços de email e domínios que são suprimidos em todas as correspondências em um único ambiente de cliente, o que significa que são específicos para uma ID de organização associada a uma ID de sandbox.

>[!NOTE]
>
>O Adobe mantém uma lista atualizada de endereços inválidos conhecidos que comprovadamente prejudicam a reputação de engajamento e mala direta e garante que os emails não sejam entregues a eles. Essa lista é gerenciada em uma lista de supressão global comum a todos os clientes da Adobe. Os endereços e os nomes de domínio contidos na lista de supressão global estão ocultos. Somente o número de destinatários excluídos é indicado nos relatórios de entrega.

Além disso, é possível aproveitar a **API REST de supressão** do Journey Optimizer para controlar as mensagens enviadas usando listas de supressão e de permissões. [Aprenda a trabalhar com a API REST de supressão](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## Por que uma lista de supressão? {#why-suppression-list}

Para controlar as mensagens de email recebidas pelos proprietários de sua caixa de entrada e garantir que elas recebam apenas aqueles que desejam, os provedores de serviços de Internet (ISPs) e os filtros comerciais de spam têm seus algoritmos proprietários para rastrear a reputação geral dos remetentes de email com base nos endereços IP e nos domínios de envio que usam.

Se você não considerar seus comentários (como reclamações de spam, rejeições etc.), eles classificarão sua reputação como insatisfatória. A lista de supressão ajuda a honrar o feedback dos ISPs.

Os recipients cujos endereços de email são suprimidos são excluídos automaticamente do delivery de mensagens. Isso irá acelerar as entregas, pois a taxa de erro tem um efeito significativo na velocidade da entrega.

## O que está na lista de supressão? {#what-s-on-suppression-list}

Os endereços são adicionados à lista de supressão da seguinte maneira:

* Todas as **rejeições permanentes** e **reclamações de spam** enviam automaticamente os endereços correspondentes para a lista de supressão após uma única ocorrência. Saiba mais sobre reclamações de spam em [esta seção](#spam-complaints).

* **As rejeições temporárias** não enviam um endereço imediatamente para a lista de supressão, mas incrementam um contador de erros. Várias [tentativas](../configuration/retries.md) são executadas e, quando o contador de erros atinge o limite, o endereço é adicionado à lista de supressão.

* Você também pode [**adicionar manualmente** um endereço ou um domínio](../configuration/manage-suppression-list.md#add-addresses-and-domains) à lista de supressão.

Saiba mais sobre rejeições permanentes e rejeições temporárias em [esta seção](#delivery-failures).

>[!NOTE]
>
>Endereços de usuários não assinados não podem ser enviados para a lista de supressão porque não estão recebendo emails de [!DNL Journey Optimizer]. A escolha é feita no nível da Experience Platform. Saiba mais sobre [recusa](../privacy/opt-out.md).

Para cada endereço, o motivo básico para ser suprimido e a categoria de supressão (flexível, permanente etc.) são exibidos na lista de supressão. Saiba mais sobre como acessar e gerenciar a lista de supressão em [esta seção](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Os perfis com status **[!UICONTROL Suprimido]** são excluídos durante o processo de envio da mensagem. Portanto, enquanto os **relatórios de Jornada** mostrarão esses perfis como tendo sido movidos pela jornada ([Ler público-alvo](../building-journeys/read-audience.md) e [atividades de mensagem](../building-journeys/journeys-message.md)), os **relatórios de email** não os incluirão nas métricas **[!UICONTROL Enviados]**, pois eles são filtrados antes do envio de email.
>
>Saiba mais sobre o [Relatório ao vivo](../reports/live-report.md) e o [Relatório do Customer Journey Analytics](../reports/report-gs-cja.md). Para descobrir o motivo de todos os casos de exclusão, você pode usar o [Serviço de Consulta do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}.

### Falhas de entrega {#delivery-failures}

Há dois tipos de erros quando um delivery falha:

* **Rejeição permanente**. Uma rejeição permanente indica um endereço de email inválido (ou seja, um endereço de email que não existe). Isso envolve uma mensagem de rejeição do servidor de email de recebimento que declara explicitamente que o endereço é inválido.
* **Rejeição leve**. Esta é uma rejeição de email temporária que ocorreu para um endereço de email válido.

Uma **rejeição permanente** adiciona automaticamente o endereço de email à lista de supressão.

Uma **rejeição temporária** <!--or an **ignored** error--> que ocorre muitas vezes também envia o endereço de email para a lista de supressão após várias tentativas. [Saiba mais sobre tentativas](../configuration/retries.md)

Se você continuar enviando para esses endereços, poderá afetar suas taxas de entrega, pois isso informa aos ISPs que você pode não estar seguindo as práticas recomendadas de manutenção da lista de endereços de email e, portanto, pode não ser um remetente confiável.

### Reclamações de spam {#spam-complaints}

A lista de supressão coleta endereços de email que marcam sua mensagem como spam. Por exemplo, se alguém escrever para um serviço de atendimento ao cliente solicitando para nunca receber emails de você novamente, o endereço de email dessa pessoa será suprimido em sua instância e você não poderá mais entregar para esse endereço.

Enviar para recipients depois que eles enviarem uma reclamação de spam pode ter um enorme impacto na sua reputação de envio, pois informa aos ISPs que você pode enviar emails indesejados e pode não ouvir seus recipients.

Isso pode fazer com que seu endereço IP ou domínio de envio seja bloqueado, o que pode ser evitado com esses endereços na lista de supressão.

Alguns ISPs oferecem um loop de comentários (FBL) que permite que o remetente de email seja notificado automaticamente quando o usuário que recebe um email optar por marcá-lo como spam. [Saiba mais](deliverability.md#feedback-loops)
