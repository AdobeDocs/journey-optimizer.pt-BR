---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de recusa para mensagens móveis
description: Saiba como gerenciar o cancelamento com mensagens SMS/RCS/MMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
TQID: https://experienceleague.adobe.com/mQVaZ8jb-hBBPxDnztkayDEI4vj0KvMTREI0KxOgAf0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 701
ht-degree: 13%

---

# Gerenciamento de recusa para mensagens móveis {#sms-opt-out}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como o Adobe Journey Optimizer gerencia a opção de não participação de mensagens SMS, MMS e RCS por meio de palavras-chave de entrada nativas, listas de bloqueios, códigos curtos e IDs alfanuméricas de remetentes.

>[!ENDSHADEBOX]

De acordo com os padrões e regulamentos do setor, todas as mensagens de marketing por SMS devem conter uma maneira de os destinatários cancelarem facilmente a inscrição. [Saiba mais sobre privacidade e gerenciamento de recusa](../privacy/opt-out.md)

>[!IMPORTANT]
>
>As comunicações de mensagens móveis podem estar sujeitas a vários requisitos de conformidade legal, dependendo de sua natureza, do local de onde você está enviando suas mensagens móveis e do local de seus recipients. Enquanto a Adobe Journey Optimizer lida com mensagens em códigos curtos, códigos longos e números de chamada gratuita conforme detalhado abaixo, consulte seu departamento jurídico para garantir que suas comunicações de mensagens móveis estejam em conformidade com todos os requisitos de conformidade legal aplicáveis.
>

## Palavras-chave de entrada nativas {#sms-native-keywords}

>[!NOTE]
>
> Somente Sinch e Infobip são compatíveis com palavras-chave nativas quando usadas com o Journey Optimizer.

Por padrão, o Adobe Journey Optimizer lida com as seguintes mensagens de resposta padrão em inglês para mensagens de códigos curtos, gratuitas e de código longo:

* **Recusa**: PARAR, SAIR, CANCELAR, ENCERRAR, CANCELAR ASSINATURA, NÃO.
* **Aceitação**: ASSINAR, SIM, REINICIAR, INICIAR, CONTINUAR, RETOMAR, INICIAR.
* **Ajuda**: AJUDA.

Essas palavras-chave normalmente acionam uma resposta padrão automática do provedor de terceiros. Você pode confirmar isso diretamente com seu provedor ou por meio do site de documentação dele.

Ao usar Infobip, certifique-se de que a ação de encaminhamento esteja definida como Configuração de extração.

Nenhuma etapa é necessária para garantir que os recursos de recusa de SMS funcionem no Adobe Journey Optimizer, pois as respostas com palavras-chave STOP, UNSTOP, START, QUIT, CANCEL, END e UNSUBSCRIBE são reconhecidas automaticamente. Os status de recusa de perfis são atualizados em tempo real no Adobe Journey Optimizer.

Se você definir palavras-chave de recusa personalizadas nas credenciais da API do SMS, elas substituirão as palavras-chave de entrada padrão listadas acima. Para manter funcionais as palavras-chave padrão, como PARAR, SAIR, CANCELAR, ENCERRAR e CANCELAR INSCRIÇÃO, inclua-as explicitamente junto com suas palavras-chave personalizadas no campo Palavras-chave de recusa da sua configuração de SMS. Caso contrário, somente suas palavras-chave personalizadas serão reconhecidas, e as palavras-chave padrão não acionarão mais ações de recusa.

Observe que se um cliente responder PARAR para uma mensagem móvel, o provedor bloqueará todo o SMS subsequente da ID do remetente específica (código curto ou número longo), incluindo mensagens transacionais. Para garantir o delivery ininterrupto de SMS transacional, use uma ID do remetente separada que não tenha sido recusada anteriormente.


>[!NOTE]
>
>Se você planeja usar SMS bidirecional (responder com PARAR, SAIR etc.), verifique se enviou primeiro pelo menos um SMS unidirecional para estabelecer o número de telefone para o mapeamento de perfil. Credenciais de provedor expiradas ou configuradas incorretamente impedirão que palavras-chave de entrada atualizem o perfil do usuário, resultando em registros de recusa ausentes ou atrasados. As respostas de entrada são armazenadas no conjunto de dados do sistema _Conjunto de dados de rastreamento de email do AJO_. [Saiba mais](../data/get-started-datasets.md#system-datasets)


## ➡ Incluis na lista de bloqueios {#sms-blocklists}

Além de o Adobe Journey Optimizer interromper o envio com base no status de recusa (para integrações diretas com o Twilio, Infobip ou Sinch), a maioria dos provedores de gateway de SMS também mantém um incluo na lista de bloqueios, garantindo que uma mensagem SMS não seja entregue a um indivíduo que recusou-se a participar. Se você estiver usando um provedor que não seja o Sinch ou Twilio e enviar um SMS por meio do [canal personalizado](../building-journeys/using-custom-actions.md), será necessário confirmar isso com o provedor.


## Códigos curtos {#short-codes}

Por padrão, as palavras-chave de aceitação ou ajuda para números de código curtos não são tratadas pela Adobe Journey Optimizer. Para garantir a conformidade com os regulamentos do setor e as regras para o tratamento de recusa, é essencial verificar se o código curto segue todas as diretrizes.

No entanto, o Journey Optimizer oferece suporte a opções de não participação globais com base em palavras-chave recebidas com IDs de remetente diferentes.

## ID alfanumérica do remetente {#alphanumeric}

As IDs alfanuméricas do remetente são somente para mensagens unidirecionais e não podem receber mensagens de entrada. Como resultado, as palavras-chave STOP, START e HELP do Adobe Journey Optimizer não se aplicam às IDs do remetente do Alpha. Você deve fornecer outras instruções, seja escrevendo para a equipe de suporte, ligando para um número de suporte ou enviando um texto através de outro número de telefone ou código para permitir que os usuários recusem o recebimento de mensagens enviadas por meio da ID alfanumérica do remetente.

## Vídeo {#video-sms}

* O vídeo abaixo ajuda você a saber como configurar a aceitação dupla de SMS.

  +++ Ver vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

  +++
