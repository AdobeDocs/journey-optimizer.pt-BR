---
title: Monitoramento da execução da mensagem
description: Saiba mais sobre as diretrizes de monitoramento e entrega
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 0184614fb3203a1b5fee7603acd173042f223578
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 28%

---

# Gerenciar a capacidade de entrega {#manage-deliverability}

A capacidade de delivery é uma medida do sucesso dos deliveries em chegar às caixas de entrada dos recipients.

A **capacidade de delivery de email** refere-se ao conjunto de características que determinam a capacidade de uma mensagem de alcançar seu destino por meio de um endereço de email pessoal, dentro de um curto período e com a qualidade esperada em termos de conteúdo e formato. Essas características estão em quatro categorias principais: qualidade de dados, mensagem e conteúdo, infraestrutura de envio e reputação. Juntos, elas formam a base de um programa bem-sucedido de capacidade de fornecimento de email.

O **taxa de entrega** é o número de mensagens que acessaram as caixas de entrada dos recipients em comparação ao número de mensagens que foram entregues. Depende de vários fatores, especialmente:

* Limitadas reclamações de spam
* Taxas de rejeição rígidas
* A qualidade dos endereços de destino
* Conteúdo da mensagem
* Reputação do remetente

Para otimizar a capacidade de entrega de seu [!DNL Journey Optimizer] experiências, recomendamos usar as práticas recomendadas listadas nesta seção. Os problemas de capacidade de delivery estão geralmente vinculados à proteção contra spam implementada por provedores de serviços de Internet (ISPs) e administradores de servidores de email.

Para um mergulho mais profundo sobre o que é a capacidade de entrega e para saber mais sobre os principais termos, conceitos e abordagens da capacidade de entrega, consulte [Guia de práticas recomendadas de capacidade de entrega do Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=pt-BR){target=&quot;_blank&quot;}.

## Reduza a taxa de reclamação {#reduce-complaint-rate}

Geralmente, os provedores de internet têm um meio proeminente de reportar uma mensagem recebida como spam. Isso permite identificar fontes não confiáveis. Ao atender rapidamente às solicitações de recusa e, portanto, mostrar que você é um remetente confiável, é possível reduzir as taxas de reclamação. [Saiba mais sobre o gerenciamento de não participação](consent.md#opt-out-management).

Como regra geral, não tente impedir os recipients que desejam fazer o opt-out exigindo que eles preencham campos como endereço de email ou nome, por exemplo. A landing page de unsubscription deve ter apenas um botão de validação.

Tenha cuidado extra ao solicitar confirmação adicional: um usuário pode ter dois endereços de email redirecionados para a mesma caixa (por exemplo: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se o perfil conseguir lembrar somente o primeiro endereço e desejar cancelar a assinatura por meio de uma mensagem enviada para o outro, o formulário recusará essa ação, pois o identificador criptografado e o endereço de email inserido não corresponderão.

## Listas de supressão de alavancagem {#suppression-lists}

[!DNL Journey Optimizer] O gerencia uma lista de supressão que reúne reclamações de spam, rejeições e devoluções temporárias que ocorrem de forma consistente.

Para proteger seu deliverability, os recipients cujos endereços estão na lista de supressão são excluídos por padrão de todos os deliveries futuros, porque o envio para esses contatos pode prejudicar sua reputação de envio.

[Saiba mais sobre a lista de supressão](suppression-list.md).

## Usar ferramentas de monitoramento {#monitoring-tools}

Use os recursos oferecidos por [!DNL Journey Optimizer] para monitorar sua capacidade de delivery.

O **[!UICONTROL Executions]** da lista de mensagens permite verificar o desempenho dos deliveries por meio de um conjunto de indicadores em tempo real. Entre outras coisas, essa guia exibe:
* O número de mensagens executadas, enviadas e entregues com êxito.
* O número de mensagens que foram abertas e o número de mensagens/links que foram clicados.

[Saiba mais sobre como monitorar a execução de mensagens](message-monitoring.md).

## Adaptar o conteúdo da mensagem {#adapt-message-content}

Em menor grau, o conteúdo de determinadas mensagens pode ser detectado como spam.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Para melhorar a taxa de delivery e garantir que seus emails cheguem aos recipients, siga os princípios abaixo ao projetar o conteúdo da mensagem:

* **Nome e endereço do remetente**: O endereço deve identificar explicitamente o remetente. O domínio deve ser de propriedade do remetente e registrado por ele. O registro de domínio não deve ser privatizado.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Cancelar assinatura do link e da landing page**: O link de cancelamento de inscrição é essencial. Deve ser visível e válido e o formulário deve ser funcional.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Saiba mais sobre como criar conteúdo de email](design-emails.md).

<!--
## Establish your reputation as a sender

If you recently moved to another email service provider, IP address, or email domain or subdomain, you need to establish your reputation as a sender. Otherwise, your deliveries might be blocked or moved to the spam folder of the recipients' mailbox.

To warm up your IP, you can gradually ramp up the number of your deliveries. See this [use case](building-journeys/ramp-up-deliveries-uc.md).
-->