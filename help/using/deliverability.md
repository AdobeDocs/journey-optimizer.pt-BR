---
title: Monitoramento da execução da mensagem
description: Saiba mais sobre as diretrizes de monitoramento e entrega
feature: Capacidade de entrega
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 29%

---

# Gerenciar a capacidade de entrega {#manage-deliverability}

A capacidade de delivery é uma medida do sucesso dos deliveries em chegar às caixas de entrada dos recipients.

A **capacidade de delivery de email** refere-se ao conjunto de características que determinam a capacidade de uma mensagem de alcançar seu destino por meio de um endereço de email pessoal, dentro de um curto período e com a qualidade esperada em termos de conteúdo e formato. Essas características estão em quatro categorias principais: qualidade de dados, mensagem e conteúdo, infraestrutura de envio e reputação. Juntos, elas formam a base de um programa bem-sucedido de capacidade de fornecimento de email.

A **deliverability rate** é o número de mensagens que acessam as caixas de entrada dos recipients em comparação ao número de mensagens que foram entregues. Depende de vários fatores, especialmente:

* Limitadas reclamações de spam
* Taxas de rejeição rígidas
* A qualidade dos endereços de destino
* Conteúdo da mensagem
* Reputação do remetente

Para otimizar a capacidade de entrega de suas experiências [!DNL Journey Optimizer], recomendamos o uso das práticas recomendadas listadas nesta seção. Os problemas de capacidade de delivery estão geralmente vinculados à proteção contra spam implementada por provedores de serviços de Internet (ISPs) e administradores de servidores de email.

## Reduza a taxa de reclamação {#reduce-complaint-rate}

Geralmente, os provedores de internet têm um meio proeminente de reportar uma mensagem recebida como spam. Isso permite identificar fontes não confiáveis. Ao atender rapidamente às solicitações de recusa e, portanto, mostrar que você é um remetente confiável, é possível reduzir as taxas de reclamação. [Saiba mais sobre o gerenciamento](consent.md#opt-out-management) de não participação.

Como regra geral, não tente impedir os recipients que desejam fazer o opt-out exigindo que eles preencham campos como endereço de email ou nome, por exemplo. A landing page de unsubscription deve ter apenas um botão de validação.

Tenha cuidado extra ao solicitar confirmação adicional: um usuário pode ter dois endereços de email redirecionados para a mesma caixa (por exemplo: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se o perfil conseguir lembrar somente o primeiro endereço e desejar cancelar a assinatura por meio de uma mensagem enviada para o outro, o formulário recusará essa ação, pois o identificador criptografado e o endereço de email inserido não corresponderão.

## Listas de supressão de alavancagem {#suppression-lists}

[!DNL Journey Optimizer] O gerencia uma lista de supressão que reúne reclamações de spam, rejeições e devoluções temporárias que ocorrem de forma consistente.

Para proteger seu deliverability, os recipients cujos endereços estão na lista de supressão são excluídos por padrão de todos os deliveries futuros, porque o envio para esses contatos pode prejudicar sua reputação de envio.

[Saiba mais sobre a lista](suppression-list.md) de supressão.

## Usar ferramentas de monitoramento {#monitoring-tools}

Use os recursos oferecidos por [!DNL Journey Optimizer] para monitorar sua capacidade de delivery.

A guia **[!UICONTROL Executions]** da lista de mensagens permite verificar o desempenho dos deliveries por meio de um conjunto de indicadores em tempo real. Entre outras coisas, essa guia exibe:
* O número de mensagens executadas, enviadas e entregues com êxito.
* O número de mensagens que foram abertas e o número de mensagens/links que foram clicados.

[Saiba mais sobre como monitorar a execução](message-monitoring.md) de mensagens.

## Adaptar o conteúdo da mensagem {#adapt-message-content}

Em menor grau, o conteúdo de determinadas mensagens pode ser detectado como spam.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Para melhorar a taxa de delivery e garantir que seus emails cheguem aos recipients, siga os princípios abaixo ao projetar o conteúdo da mensagem:

* **Nome e endereço** do remetente: O endereço deve identificar explicitamente o remetente. O domínio deve ser de propriedade do remetente e registrado por ele. O registro de domínio não deve ser privatizado.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Cancelar assinatura do link e da landing page**: O link de cancelamento de inscrição é essencial. Deve ser visível e válido e o formulário deve ser funcional.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Saiba mais sobre como criar conteúdo](design-emails.md) de email.
