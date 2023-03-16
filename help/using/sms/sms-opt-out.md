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
source-git-commit: 63237c02f632d289dba845acdcd0859f2d6de9c9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 31%

---

# Gerenciamento de recusa de SMS {#sms-opt-out}

De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. [Saiba mais sobre privacidade e gerenciamento de recusa](../privacy/opt-out.md)

>[!IMPORTANT]
>
>As comunicações de mensagens de texto podem estar sujeitas a vários requisitos de conformidade legal, dependendo de sua natureza, do local de onde você está enviando suas mensagens de texto e do local dos recipients. Embora o Adobe Journey Optimizer trate as mensagens em códigos longos e números de chamada gratuita, conforme detalhado abaixo, consulte seu consultor jurídico para garantir que suas comunicações de mensagens de texto estejam em conformidade com todos os requisitos de conformidade legal aplicáveis.

## Palavras-chave de entrada nativas{#sms-native-keywords}

Por padrão, o Adobe Journey Optimizer processa as seguintes mensagens de resposta em inglês padrão para mensagens de código gratuito e longo: PARAR, DESPARAR, INICIAR, SAIR, CANCELAR, TERMINAR E CANCELAR A SUBSCRIÇÃO. Observe que somente o Sinch suporta palavras-chave nativas quando usado com o Journey Optimizer.

Normalmente, essas palavras-chave acionam uma resposta padrão automática do provedor de terceiros. Você pode confirmar isso diretamente com seu provedor ou por meio do site de documentação dele.

Nenhuma etapa é necessária para garantir que os recursos de recusa de SMS estejam funcionando no Adobe Journey Optimizer, à medida que as respostas de palavra-chave PARAR, UNSTOP, START, SAIR, CANCEL, END e UNSUBSCRIBE são reconhecidas automaticamente. Os status de recusa de perfis são atualizados em tempo real no Adobe Journey Optimizer.


## listas de bloqueios{#sms-blocklists}

Além de Adobe Journey Optimizer interromper o envio com base no status de recusa (para integrações diretas com Twilio ou Sinch), a maioria dos provedores de gateway SMS também mantém uma  lista de bloqueios, garantindo que uma mensagem SMS não seja entregue a um indivíduo que optou por não participar. Se você estiver usando um provedor diferente de Sinch ou Twilio e enviar um SMS via [canal personalizado](../building-journeys/using-custom-actions.md), é necessário confirmar isso com o provedor.


## Códigos curtos {#short-codes}

Por padrão, palavras-chave de aceitação ou ajuda para números de código curtos não são tratadas pela Adobe Journey Optimizer. Para garantir a conformidade com os regulamentos do setor e as regras de controle de opt-out, é essencial verificar se o código curto segue todas as diretrizes.

No entanto, o Journey Optimizer oferece suporte a opções globais com base em palavras-chave recebidas com diferentes IDs de remetente.

## ID alfanumérica do remetente {#alphanumeric}

As IDs alfanuméricas do remetente são somente para mensagens unidirecionais e não podem receber mensagens de entrada. Como resultado, as palavras-chave STOP, START e HELP usadas em mensagens no Adobe Journey Optimizer não se aplicam às IDs do remetente alfa. Você deve fornecer outras instruções, seja escrevendo para a equipe de suporte, ligando para um número de suporte ou enviando um texto através de outro número de telefone ou código para permitir que os usuários recusem o recebimento de mensagens enviadas por meio da ID alfanumérica do remetente.

## Vídeo {#video-sms}

Para saber mais sobre como o suporte nativo a palavras-chave de entrada (START, STOP e UNSTOP) funciona para SMS, assista ao seguinte vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
