---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à capacidade de entrega
description: Saiba mais sobre as diretrizes de entrega
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 13%

---

# Introdução à capacidade de entrega {#manage-deliverability}

A capacidade de entrega é uma medida do sucesso das entregas em chegar às caixas de entrada dos destinatários.

>[!NOTE]
>
>Para clientes que licenciam o Healthcare Shield, o Adobe usa o Transport Layer Security (TLS) 1.2 para proteger a troca de dados entre os sistemas dos usuários (destinatários) e a Journey Optimizer (remetente). Se o servidor de email de recebimento não for compatível com TLS 1.2, os clientes enfrentarão problemas de capacidade de entrega, incluindo email retornando ao remetente de origem.

**Entregabilidade por email** refere-se ao conjunto de características que determinam a capacidade de uma mensagem de alcançar seu destino por meio de um endereço de email pessoal, dentro de um curto período e com a qualidade esperada em termos de conteúdo e formato. Essas características estão em quatro categorias principais: qualidade de dados, mensagem e conteúdo, infraestrutura de envio e reputação. Juntos, elas formam a base de um programa bem-sucedido de capacidade de fornecimento de email.

A variável **taxa de entrega** é o número de mensagens que chegam nas caixas de entrada dos destinatários em comparação ao número de mensagens que foram entregues. Depende de vários fatores, especialmente:

* Reclamações limitadas de spam
* Baixas taxas de rejeição de disco rígido
* A qualidade dos endereços de destino
* Conteúdo da mensagem
* Reputação do remetente

Para otimizar a capacidade de delivery do seu [!DNL Journey Optimizer] recomendamos usar as práticas recomendadas listadas nesta seção. Os problemas de capacidade de delivery estão geralmente vinculados à proteção contra spam implementada por provedores de serviços de Internet (ISPs) e administradores de servidores de email.

Para aprofundar o assunto e saber mais sobre os termos, conceitos e abordagens principais da capacidade de delivery, consulte [Guia de práticas recomendadas de capacidade de delivery do Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=pt-BR){target="_blank"}.

## Reduzir a taxa de reclamação {#reduce-complaint-rate}

Geralmente, os provedores de internet têm um meio proeminente de reportar uma mensagem recebida como spam. Isso permite identificar fontes não confiáveis. Ao atender rapidamente às solicitações de recusa e, portanto, mostrar que você é um remetente confiável, é possível reduzir as taxas de reclamação. [Saiba mais sobre o gerenciamento de recusa](../privacy/opt-out.md#opt-out-management)

Como regra geral, não tente impedir os destinatários que desejam fazer o opt-out exigindo que eles preencham campos como endereço de email ou nome, por exemplo. A landing page de cancelamento de subscrição deve ter apenas um botão de validação.

Tenha cuidado extra ao solicitar confirmação adicional: um usuário pode ter dois endereços de email redirecionados para a mesma caixa (por exemplo: firstname.lastname@club.com e firstname.lastname@internet-club.com). Se o perfil conseguir lembrar somente o primeiro endereço e desejar cancelar a inscrição por meio de uma mensagem enviada para o outro, o formulário recusará essa ação, pois o identificador criptografado e o endereço de email digitado não corresponderão.

## Aproveitar listas de supressão {#suppression-lists}

[!DNL Journey Optimizer] O gerencia uma lista de supressão que reúne reclamações de spam, rejeições permanentes e rejeições temporárias que ocorrem de forma consistente.

Para proteger sua capacidade de delivery, os recipients cujos endereços estão na lista de supressão são excluídos por padrão de todos os deliveries futuros, pois o envio para esses contatos pode prejudicar sua reputação de envio.

[Saiba mais sobre a lista de supressão](suppression-list.md)

## Usar ferramentas de monitoramento {#monitoring-tools}

Use os recursos oferecidos pelo [!DNL Journey Optimizer] para monitorar a capacidade de delivery.

A variável **[!UICONTROL Execuções]** A guia da lista de mensagens permite verificar o desempenho de seus deliveries por meio de um conjunto de indicadores em tempo real. Entre outras coisas, essa guia exibe:
* O número de mensagens executadas, enviadas e entregues com êxito.
* O número de mensagens que foram abertas e o número de mensagens/links que foram clicados.

## Adaptar conteúdo da mensagem {#adapt-message-content}

Em menor grau, o conteúdo de determinadas mensagens pode ser detectado como spam.

Para melhorar a taxa de delivery e garantir que seus emails cheguem aos recipients, siga os princípios abaixo ao criar o conteúdo da mensagem:

* **Nome e endereço do remetente**: o endereço deve identificar explicitamente o remetente. O domínio deve ser de propriedade do remetente e registrado por ele. O registro de domínio não deve ser privatizado.

* **Link de cancelamento de inscrição e página de aterrissagem**: o link de cancelamento de inscrição é essencial. Deve ser visível e válido e o formulário deve ser funcional.

[Saiba mais sobre design de conteúdo de email](../email/get-started-email-design.md)

## Estabelecer sua reputação como remetente {#reputation}

Se você mudou recentemente para outro provedor de serviços de email, endereço IP, domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients.

Para aquecer seu IP, você pode aumentar gradualmente o número de deliveries. Saiba mais nesta página [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).

## Implementar DMARC {#dmarc}

Para ajudar você a reduzir o risco de emails legítimos serem marcados como spam ou rejeitados e evitar problemas de entrega, [!DNL Journey Optimizer] permite configurar o registro DMARC para todos os subdomínios que você delega ao Adobe.

O DMARC (Domain-based Message Authentication, Reporting, and Conformance) é um método de autenticação de email que permite que os proprietários de domínios protejam seus domínios contra o uso não autorizado por agentes mal-intencionados.

[Saiba mais sobre o registro DMARC](../configuration/dmarc-record.md)

## Saiba mais sobre loops de comentários {#feedback-loops}

Um loop de feedback (FBL) é um serviço oferecido por alguns ISPs que permite que o remetente de email seja notificado automaticamente quando o usuário que recebe um email optar por marcá-lo como spam (também conhecido como &quot;reclamação&quot;).

Depois que um usuário final gera uma reclamação que é enviada de volta ao Adobe pelo ISP, o endereço de email é adicionado automaticamente ao [lista de supressão](../reports/suppression-list.md) e excluídos de deliveries futuros. Na verdade, o envio de emails para usuários que os marcaram como spam afeta negativamente a reputação do remetente e pode causar problemas de entrega. [Saiba mais sobre reclamações de spam](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Nem todos os ISPs fornecem um FBL tradicional, como o Gmail. O Gmail não oferece feedback de nível individual e não pode ser usado para rastrear reclamações de spam para recipients individuais, concentrando-se em relatórios de nível agregado nas Ferramentas de postmaster do Google. [Saiba mais](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Todos os clientes do Adobe são automaticamente inscritos nos FBLs tradicionais dos seguintes ISPs:

* 1&amp;1

* AOL

* BlueTime

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackspace

* SEZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* Telecom Itália

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* Virgin Media

* Yahoo

* Ziggo

O Adobe audita esses FBLs regularmente para garantir que os FBLs disponíveis mais recentes sejam adicionados.
