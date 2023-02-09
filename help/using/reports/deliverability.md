---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à capacidade de entrega
description: Saiba mais sobre as diretrizes de deliverability
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 28%

---

# Introdução à capacidade de entrega {#manage-deliverability}

A capacidade de delivery é uma medida do sucesso dos deliveries em chegar às caixas de entrada dos recipients.

>[!NOTE]
>
>Para clientes que licenciam o Healthcare Shield, o Adobe usa o Transport Layer Security (TLS) 1.2 para proteger a troca de dados entre os sistemas (recipients) e o Journey Optimizer (remetente) dos usuários. Se o servidor de email de recebimento não for compatível com TLS 1.2, os clientes enfrentarão problemas de deliverability, incluindo o email devolvido ao remetente de origem.

A **capacidade de delivery de email** refere-se ao conjunto de características que determinam a capacidade de uma mensagem de alcançar seu destino por meio de um endereço de email pessoal, dentro de um curto período e com a qualidade esperada em termos de conteúdo e formato. Essas características estão em quatro categorias principais: qualidade de dados, mensagem e conteúdo, infraestrutura de envio e reputação. Juntos, elas formam a base de um programa bem-sucedido de capacidade de fornecimento de email.

O **taxa de entrega** é o número de mensagens que acessaram as caixas de entrada dos recipients em comparação ao número de mensagens que foram entregues. Depende de vários fatores, especialmente:

* Limitadas reclamações de spam
* Taxas de rejeição rígidas
* A qualidade dos endereços de destino
* Conteúdo da mensagem
* Reputação do remetente

Para otimizar a capacidade de entrega de seu [!DNL Journey Optimizer] experiências, recomendamos usar as práticas recomendadas listadas nesta seção. Os problemas de capacidade de delivery estão geralmente vinculados à proteção contra spam implementada por provedores de serviços de Internet (ISPs) e administradores de servidores de email.

Para aprofundar o assunto e saber mais sobre os termos, conceitos e abordagens principais da capacidade de delivery, consulte o [Manual de práticas recomendadas de capacidade de delivery da Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=pt-BR){target="_blank"}.

## Reduza a taxa de reclamação {#reduce-complaint-rate}

Geralmente, os provedores de internet têm um meio proeminente de reportar uma mensagem recebida como spam. Isso permite identificar fontes não confiáveis. Ao atender rapidamente às solicitações de recusa e, portanto, mostrar que você é um remetente confiável, é possível reduzir as taxas de reclamação. [Saiba mais sobre o gerenciamento de não participação](../privacy/opt-out.md#opt-out-management).

Como regra geral, não tente impedir os recipients que desejam fazer o opt-out exigindo que eles preencham campos como endereço de email ou nome, por exemplo. A landing page de unsubscription deve ter apenas um botão de validação.

Tenha cuidado extra ao solicitar confirmação adicional: um usuário pode ter dois endereços de email redirecionados para a mesma caixa (por exemplo: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se o perfil conseguir lembrar somente o primeiro endereço e desejar cancelar a assinatura por meio de uma mensagem enviada para o outro, o formulário recusará essa ação, pois o identificador criptografado e o endereço de email inserido não corresponderão.

## Listas de supressão de alavancagem {#suppression-lists}

[!DNL Journey Optimizer] O gerencia uma lista de supressão que reúne reclamações de spam, rejeições e devoluções temporárias que ocorrem de forma consistente.

Para proteger seu deliverability, os recipients cujos endereços estão na lista de supressão são excluídos por padrão de todos os deliveries futuros, porque o envio para esses contatos pode prejudicar sua reputação de envio.

[Saiba mais sobre a lista de supressão](suppression-list.md).

## Usar ferramentas de monitoramento {#monitoring-tools}

Use os recursos oferecidos por [!DNL Journey Optimizer] para monitorar sua capacidade de delivery.

O **[!UICONTROL Execuções]** da lista de mensagens permite verificar o desempenho dos deliveries por meio de um conjunto de indicadores em tempo real. Entre outras coisas, essa guia exibe:
* O número de mensagens executadas, enviadas e entregues com êxito.
* O número de mensagens que foram abertas e o número de mensagens/links que foram clicados.

## Adaptar o conteúdo da mensagem {#adapt-message-content}

Em menor grau, o conteúdo de determinadas mensagens pode ser detectado como spam.

Para melhorar a taxa de delivery e garantir que seus emails cheguem aos recipients, siga os princípios abaixo ao projetar o conteúdo da mensagem:

* **Nome e endereço do remetente**: O endereço deve identificar explicitamente o remetente. O domínio deve ser de propriedade do remetente e registrado por ele. O registro de domínio não deve ser privatizado.

* **Cancelar assinatura do link e da landing page**: O link de cancelamento de inscrição é essencial. Deve ser visível e válido e o formulário deve ser funcional.

[Saiba mais sobre como criar conteúdo de email](../email/get-started-email-design.md).

## Estabelecer sua reputação como remetente

Se você mudou recentemente para outro provedor de serviços de email, endereço IP ou domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients.

Para aquecer o IP, você pode aumentar gradualmente o número de deliveries. Veja isso [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).
