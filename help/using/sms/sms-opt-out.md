---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de recusa de SMS
description: Saiba como gerenciar a recusa com mensagens SMS
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Gerenciamento de recusa de SMS {#sms-opt-out}

De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a assinatura. [Saiba mais sobre privacidade e gerenciamento de recusa](../privacy/opt-out.md)

Por padrão, o Adobe Journey Otimizer lida com mensagens de resposta em inglês padrão, como STOP, UNSTOP e START para mensagens de código longo e gratuito, de acordo com os padrões do setor para integração nativa, como Sinch e Twilio. Essas palavras-chave normalmente acionam uma resposta padrão automática do provedor de terceiros (por exemplo, Twilio, Sinch etc.). Você pode confirmar isso diretamente com seu provedor ou por meio do site da documentação.

Nenhuma etapa é necessária para garantir que os recursos de recusa de SMS estejam funcionando no Adobe Journey Otimizer, pois as respostas de palavra-chave PARAR, UNSTOP e START serão reconhecidas automaticamente.

Além do Adobe Journey Otimizer interromper o envio com base no status de recusa (para integrações diretas com Twilio ou Sinch), a maioria dos provedores de gateway SMS também mantém uma lista de bloqueios garantindo que uma mensagem SMS não será entregue a um indivíduo que optou por rejeitar. Se você estiver usando um provedor diferente de Sinch ou Twilio e enviar um SMS via [canal personalizado](../building-journeys/using-custom-actions.md), é necessário confirmar isso com o provedor.

>[!IMPORTANT]
>
>As campanhas de mensagem de texto podem estar sujeitas a vários requisitos de conformidade legal, dependendo da natureza de sua campanha de mensagens de texto, do local de onde você está enviando suas mensagens de texto e do local de seus recipients. <br>Embora o Adobe Journey Otimizer trate as mensagens em códigos longos e números de chamada gratuita, conforme detalhado acima, você deve consultar seu consultor jurídico para garantir que sua campanha de mensagem de texto esteja em conformidade com todos os requisitos de conformidade legal aplicáveis.

## Códigos curtos {#short-codes}

Por padrão, o Adobe Journey Otimizer não lidará com palavras-chave de opt-out, opt-in ou ajuda para números de código curtos.

Você deve garantir que seu código curto esteja em conformidade com todas as regras e regulamentos do setor para o controle de opt out.

## ID alfanumérica do remetente {#alphanumeric}

As IDs alfanuméricas do remetente são somente para mensagens unidirecionais e não podem receber mensagens de entrada. Como resultado, as palavras-chave SMS STOP, START, HELP do Adobe Journey Otimizer não são aplicáveis para IDs de remetente alfa. Você deve fornecer outras instruções, como escrever para a equipe de suporte, chamar uma linha telefônica de suporte ou enviar um texto com outro número de telefone ou código para permitir que os usuários optem por não receber mensagens enviadas por meio da ID alfanumérica do remetente.

## Vídeo {#video-sms}

Para saber mais sobre como o suporte nativo a palavras-chave de entrada (START, STOP e UNSTOP) funciona para SMS, consulte o seguinte vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
