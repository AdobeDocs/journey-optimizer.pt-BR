---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de recusa para mensagens de texto
description: Saiba como gerenciar o cancelamento com mensagens SMS/MMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d7b784f10e267878fd0df9360ed0d1be24699a53
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 19%

---

# Gerenciamento de recusa para mensagens de texto {#sms-opt-out}

De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os recipients cancelarem facilmente a inscrição. [Saiba mais sobre privacidade e gerenciamento de recusa](../privacy/opt-out.md)

>[!IMPORTANT]
>
>As comunicações de mensagem de texto podem estar sujeitas a vários requisitos de conformidade legal, dependendo da natureza, do local de onde você está enviando suas mensagens de texto e do local de seus destinatários. Enquanto a Adobe Journey Optimizer lida com as mensagens em códigos curtos, códigos longos e números de chamada gratuita conforme detalhado abaixo, consulte seu departamento jurídico para garantir que suas comunicações de mensagem de texto estejam em conformidade com todos os requisitos de conformidade legal aplicáveis.
>

## Palavras-chave de entrada nativas {#sms-native-keywords}

>[!NOTE]
>
> Somente Sinch e Infobip são compatíveis com palavras-chave nativas quando usadas com o Journey Optimizer.

Por padrão, o Adobe Journey Optimizer lida com as seguintes mensagens de resposta padrão em inglês para mensagens de códigos curtos, gratuitas e de código longo:

* **Recusar**: PARAR, SAIR, CANCELAR, ENCERRAR, CANCELAR INSCRIÇÃO, NÃO.
* **Opt-In**: ASSINAR, SIM, REINICIAR, INICIAR, CONTINUAR, RETOMAR, INICIAR.
* **Ajuda**: AJUDA.

Essas palavras-chave normalmente acionam uma resposta padrão automática do provedor de terceiros. Você pode confirmar isso diretamente com seu provedor ou por meio do site de documentação dele.

Ao usar Infobip, certifique-se de que a ação de encaminhamento esteja definida como Configuração de extração.

Nenhuma etapa é necessária para garantir que os recursos de recusa de SMS funcionem no Adobe Journey Optimizer, pois as respostas com palavras-chave STOP, UNSTOP, START, QUIT, CANCEL, END e UNSUBSCRIBE são reconhecidas automaticamente. Os status de recusa de perfis são atualizados em tempo real no Adobe Journey Optimizer.


## ➡ Incluis na lista de bloqueios {#sms-blocklists}

Além de o Adobe Journey Optimizer interromper o envio com base no status de recusa (para integrações diretas com o Twilio ou Sinch), a maioria dos provedores de gateway de SMS também mantém uma inclui na lista de bloqueios, garantindo que uma mensagem SMS não seja entregue a um indivíduo que recusou-se a participar. Se você estiver usando um provedor que não seja o Sinch ou Twilio e enviar um SMS por [canal personalizado](../building-journeys/using-custom-actions.md), é necessário confirmar isso com o provedor.


## Códigos curtos {#short-codes}

Por padrão, as palavras-chave de aceitação ou ajuda para números de código curtos não são tratadas pela Adobe Journey Optimizer. Para garantir a conformidade com os regulamentos do setor e as regras para o tratamento de recusa, é essencial verificar se o código curto segue todas as diretrizes.

No entanto, o Journey Optimizer oferece suporte a opções de não participação globais com base em palavras-chave recebidas com IDs de remetente diferentes.

## ID alfanumérica do remetente {#alphanumeric}

As IDs alfanuméricas do remetente são somente para mensagens unidirecionais e não podem receber mensagens de entrada. Como resultado, as palavras-chave STOP, START e HELP do Adobe Journey Optimizer não se aplicam às IDs do remetente do Alpha. Você deve fornecer outras instruções, seja escrevendo para a equipe de suporte, ligando para um número de suporte ou enviando um texto através de outro número de telefone ou código para permitir que os usuários recusem o recebimento de mensagens enviadas por meio da ID alfanumérica do remetente.

## Vídeo {#video-sms}

* O vídeo abaixo mostra como o suporte nativo a palavras-chave de entrada (START, STOP e UNSTOP) funciona para SMS.

+++ Ver vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

+++

* O vídeo abaixo ajuda você a saber como configurar a aceitação dupla de SMS.

+++ Ver vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

+++
