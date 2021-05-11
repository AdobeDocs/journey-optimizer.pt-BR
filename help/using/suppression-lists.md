---
title: Monitoramento da execução da mensagem
description: Saiba mais sobre as diretrizes de monitoramento e entrega
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 3%

---

# Gerenciar listas de supressão {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

Uma lista de supressão consiste em endereços de email que você deseja excluir de seus deliveries, pois o envio para esses contatos pode prejudicar sua reputação de envio e as taxas de delivery.

A lista de supressão **do Journey Optimizer** é gerenciada no seu próprio nível de ambiente. Ele coleta reclamações de spam, devoluções permanentes e devoluções temporárias que ocorrem de forma consistente.

## Por que as listas de supressão? {#why-suppression-lists}

Para controlar as mensagens de email recebidas pelos proprietários da caixa de entrada e garantir que elas recebam somente as mensagens desejadas, os provedores de serviços de Internet (ISPs) e os filtros de spam comercial têm seus algoritmos proprietários para rastrear a reputação geral dos remetentes de email com base nos endereços IP e no(s) domínio(s) de envio que usam.

Se você não receber seus comentários (como reclamações de spam, devoluções etc.) em consideração, eles classificarão sua reputação como baixa. A lista de supressão ajuda você a honrar os comentários dos ISPs.

Os recipients cujos endereços de email são suprimidos são excluídos automaticamente do delivery de mensagens. Isso irá acelerar os deliveries, pois a taxa de erro tem um efeito significativo na velocidade do delivery.

### Reclamações de spam {#spam-complaints}

A lista de supressão coleta endereços de email que marcam sua mensagem como spam. Enviar para recipients depois que eles enviarem uma reclamação de spam pode ter um grande impacto na sua reputação de envio, porque isso informa aos ISPs que você pode enviar emails indesejados e pode não ouvir seus recipients.

Isso pode fazer com que seu endereço IP ou domínio de envio seja bloqueado, o que pode ser evitado com esses endereços na lista de supressão.

### Rejeições {#bounces}

Além disso, a lista de supressão contém endereços de email que foram rejeitados ou que foram rejeitados anteriormente, muitas vezes. Se você continuar enviando para esses endereços, isso pode afetar suas taxas de delivery, pois informa aos ISPs que talvez você não esteja seguindo as práticas recomendadas de manutenção da lista de endereços de email e, portanto, pode não ser um remetente confiável.

## Gerenciamento da lista de supressão {#suppression-list-management}

A lista de supressão do Journey Optimizer reúne endereços de email e domínios que são suprimidos em todas as malas diretas **em um único ambiente cliente**, o que significa que são específicos de uma ID de organização IMS associada a uma ID de sandbox.

A lista de supressão permite coletar automaticamente:
* Endereços de email inválidos ou que consistentemente sejam rejeitados e possam afetar negativamente sua reputação de email, caso continue a incluí-los nos deliveries.
* Recipients que emitem uma reclamação de spam de algum tipo contra uma de suas mensagens de email.

Por exemplo, se alguém escrever para um serviço de atendimento ao cliente solicitando para nunca receber email novamente de você, o endereço de email dessa pessoa será suprimido em sua instância e você não poderá mais enviar o email para esse endereço.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Falhas no delivery {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Há três tipos de erros quando um delivery falha:

* **Rejeição** forçada. Uma rejeição permanente indica um endereço de email inválido (ou seja, um endereço de email que não existe). Isso envolve uma mensagem de devolução do servidor de email de recebimento que declara explicitamente que o endereço é inválido, como &quot;unknown user&quot;.
* **Rejeição suave**. Esta é uma devolução temporária de email que ocorreu para um endereço de email válido.
* **Ignorado**. Trata-se de uma devolução de e-mail que ocorreu para um endereço de e-mail válido, mas é conhecido como temporário, como uma tentativa de conexão com falha, um problema temporário relacionado a spam (reputação de e-mail) ou um problema técnico temporário.

As devoluções permanentes e as devoluções temporárias podem ser um motivo para um endereço de email ser adicionado automaticamente à lista de supressão.

### O que está na lista de supressão? {#what-s-on-suppression-list}

Os endereços de email são adicionados à lista de supressão da seguinte maneira:

* Todos os **devoluções permanentes** e **reclamações de spam** enviam automaticamente os endereços de email correspondentes para a lista de supressão após uma única ocorrência.

* **As** devoluções temporárias não enviam imediatamente um endereço de email para a lista de supressão, mas incrementam um contador de erros. Quando o contador de erros atinge o limite, o endereço é adicionado à lista de supressão.

   O limite é definido em três erros:
   * Para o mesmo delivery, na terceira tentativa, o endereço é suprimido.
   * Se houver diferentes deliveries e dois erros ocorrerem pelo menos em 24 horas de intervalo, o contador de erros será incrementado a cada erro e o endereço também será suprimido na terceira tentativa.

   Quando um delivery é bem-sucedido após uma tentativa, o contador de erros do endereço é reinicializado.

### Tentativas {#retries}

Se uma mensagem falhar devido a uma rejeição temporária do tipo **Ignorado**, novas tentativas serão executadas por **3,5 dias** a partir do momento em que a mensagem foi adicionada à fila de email.

O atraso mínimo entre as tentativas e o número máximo de tentativas a serem executadas é <!--managed by the Enhanced MTA,--> baseado no desempenho histórico e atual de um IP em um determinado domínio.

Após 3,5 dias, qualquer mensagem na fila de tentativas será removida e enviada de volta como uma rejeição.
