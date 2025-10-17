---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a mensagens de texto (SMS/MMS/RCS)
description: Saiba como criar e enviar mensagens de texto no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 243d4e74c15057bc4bd334876a1bc87969d396e0
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 27%

---

# Introdução às mensagens de texto {#get-started-sms}

Use o [!DNL Journey Optimizer] para enviar mensagens de texto (SMS/MMS/RCS) para seus clientes em seus dispositivos móveis. É possível criar, personalizar e visualizar mensagens em formato de texto no editor de SMS/MMS/RCS.

As mensagens de texto podem ser criadas e enviadas em uma jornada ou em uma campanha. Para SMS, MMS e RCS, use a ação SMS.

* Em uma **jornada**. Crie uma jornada, adicione uma atividade de SMS e defina configurações básicas. Em seguida, navegue até o painel Ações de SMS à direita para criar o conteúdo para a mensagem SMS, MMS ou RCS. [Saiba como criar uma jornada](../building-journeys/journey-gs.md)

* Em uma **Campanha**. Crie uma campanha, selecione SMS como sua ação e defina as configurações básicas. Em seguida, edite o conteúdo da mensagem para definir a mensagem SMS, MMS ou RCS que será enviada. [Saiba como criar uma campanha](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>Se esta for a primeira vez que você cria mensagens de texto, verifique se o canal SMS foi configurado. [Saiba mais](sms-configuration.md)

## Recursos de mensagens de texto {#sms-capabilities}

O Adobe Journey Optimizer fornece recursos abrangentes de mensagem de texto para envolver seus clientes em vários canais:

**SMS (Serviço de Mensagens Curtas)**

Enviar mensagens somente texto com até 160 caracteres. O SMS é o formato de mensagem de texto mais compatível em todos os dispositivos móveis.

**MMS (Serviço de Mensagens Multimídia)**

Melhore sua comunicação com conteúdo multimídia, incluindo vídeos, imagens, clipes de áudio e GIFs. As mensagens MMS permitem até 1600 caracteres de texto além de arquivos de mídia. [Saiba mais sobre as limitações de MMS](../start/guardrails.md#sms-guardrails)

**RCS (Serviços de Comunicação Avançada)**

Envie mensagens interativas e de marca com recursos avançados, como carrosséis, cartões avançados, ações sugeridas e suporte de mídia aprimorado. O RCS fornece uma experiência de mensagens mais avançada em dispositivos compatíveis.

## Recursos principais {#key-features}

**Personalization e conteúdo dinâmico**

Crie mensagens de texto personalizadas usando o editor de personalização. Adicione atributos de perfil, conteúdo condicional e dados dinâmicos para adaptar mensagens a recipients individuais. [Saiba mais sobre a personalização](../personalization/personalize.md)

**Suporte a vários provedores**

O Adobe Journey Optimizer integra-se aos principais provedores de serviços SMS:

* **Sinch** - [Guia de configuração](sms-configuration-sinch.md)
* **Twilio** - [Guia de configuração](sms-configuration-twilio.md)
* **Infobip** - [Guia de configuração](sms-configuration-infobip.md)
* **Provedores personalizados** - Configure qualquer outro provedor SMS usando a integração de API personalizada. [Saiba mais](sms-configuration-custom.md)

**Encurtamento e Acompanhamento de URL**

Adicione URLs rastreáveis e encurtados às suas mensagens para monitorar o engajamento. A configuração de subdomínio é necessária para a funcionalidade de redução de URL. [Saiba como configurar subdomínios de SMS](sms-subdomains.md)

**Gerenciamento da opção de não participação**

Garanta a conformidade com os padrões e regulamentos do setor por meio do gerenciamento de recusa integrado. O Journey Optimizer lida automaticamente com palavras-chave padrão de recusa (PARAR, SAIR, CANCELAR etc.) para provedores Sinch e Infobip. [Saiba mais sobre o gerenciamento da opção de não participação](sms-opt-out.md)

**Visualização e teste**

Teste suas mensagens de texto antes de enviar usando perfis de teste e dados de amostra. Visualize a personalização, o conteúdo e a formatação para garantir que suas mensagens sejam exibidas corretamente. [Saiba como enviar mensagens](send-sms.md)

**Relatórios e análises**

Acompanhe o desempenho de suas campanhas e jornadas de SMS com recursos abrangentes de relatório:

* [Relatórios de campanha por SMS](../reports/campaign-global-report-cja-sms.md)
* [Relatórios de jornada por SMS](../reports/journey-global-report-cja-sms.md)

## Requisitos de configuração {#configuration-requirements}

Antes de enviar mensagens de texto, você deve:

1. **Escolha um provedor SMS** - Selecione Sinch, Twilio, Infobip ou configure um provedor personalizado
2. **Configurar credenciais de API** - Integre os tokens de API e as IDs de serviço do provedor à Journey Optimizer
3. **Criar configurações de canal** - Definir configurações de SMS para mensagens de marketing e transacionais
4. **Configurar subdomínios (opcional)** - Necessário somente se você planeja usar a redução de URL em suas mensagens

Normalmente, essas etapas de configuração são executadas por um Administrador do sistema. [Introdução à configuração de SMS](sms-configuration.md)

## Guia de início rápido {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Validação" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Configurar canal de SMS</strong></a>
</div>
<p>Definir o provedor de SMS e as configurações de canal</p>
</td>
<td>
<a href="create-sms.md">
<img alt="Lead" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>Criar uma mensagem de texto</strong></a>
</div>
<p>Projetar e personalizar conteúdo SMS, MMS ou RCS</p>
</td>
<td>
<a href="send-sms.md">
<img alt="Pouco frequente" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>Visualizar e enviar</strong></a>
</div>
<p>Testar e enviar suas mensagens de texto para o público-alvo</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validação" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Gerenciar opções de não participação</strong></a>
</div>
<p>Manipular solicitações de cancelamento de inscrição e garantir a conformidade</p>
</td>
</tr></table>

## Recursos adicionais {#additional-resources}

Navegue pelos tópicos abaixo para saber mais sobre mensagens de texto no Journey Optimizer.

+++Guias de configuração

Saiba como instalar e configurar seu ambiente SMS:

* [Visão geral da configuração do canal SMS](sms-configuration.md)
* [Criar configurações de canal de SMS](sms-configuration-surface.md)
* [Configurar subdomínios SMS para redução de URL](sms-subdomains.md)

+++

+++Guias de configuração do provedor

Configuração passo a passo para cada provedor de serviços SMS:

* [Configurar provedor Sinch](sms-configuration-sinch.md)
* [Configurar provedor Twilio](sms-configuration-twilio.md)
* [Configurar provedor Infobip](sms-configuration-infobip.md)
* [Configurar provedor de SMS personalizado](sms-configuration-custom.md)

+++

+++Criação e gerenciamento de conteúdo

Crie, personalize e gerencie o conteúdo da sua mensagem de texto:

* [Criar mensagens SMS/MMS](create-sms.md)
* [Pré-visualizar, testar e enviar mensagens](send-sms.md)
* [Personalization em mensagens de texto](../personalization/personalize.md)
* [Conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

+++

+++Conformidade e privacidade

Verifique se suas mensagens de texto estão em conformidade com os regulamentos e os padrões de privacidade:

* [Gerenciamento de recusa](sms-opt-out.md)
* [Privacidade e consentimento](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

+++

+++Rastreamento de desempenho

Monitore e analise suas campanhas de SMS e o desempenho do jornada:

* [Relatórios de campanha por SMS](../reports/campaign-global-report-cja-sms.md)
* [Relatórios de jornada por SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integração do Jornada e do Campaign

Saiba como incorporar o SMS nas jornadas e campanhas do cliente:

* [Adicionar mensagens SMS ao jornada](../building-journeys/journeys-message.md)
* [Criar campanhas de SMS](../campaigns/create-campaign.md)

+++

## Vídeos tutoriais {#videos}

**Configurar e enviar mensagens SMS**

Saiba como configurar, criar e incluir mensagens de SMS nas jornadas do cliente.

+++Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3422698?captions=por_br&learn=on)

+++

**Explorar recursos de mensagens móveis**

Descubra os recursos abrangentes de mensagens móveis que a Adobe Journey Optimizer oferece aos profissionais de marketing.

+++Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3430380?captions=por_br&quality=12&learn=on)

+++

**Enviar mensagens RCS com marca**

Saiba como configurar e enviar mensagens RCS interativas e alinhadas à marca no Adobe Journey Optimizer por meio de um provedor de SMS personalizado.

+++Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3464760?captions=por_br)

+++

**Tópicos relacionados**

* [Adicionar mensagens em jornadas](../building-journeys/journeys-message.md)
* [Criar campanhas de marketing](../campaigns/create-campaign.md)
* [Proteções e limitações](../start/guardrails.md#sms-guardrails)
