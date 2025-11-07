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
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 99%

---

# Introdução às mensagens de texto {#get-started-sms}

Use o [!DNL Journey Optimizer] para enviar mensagens de texto (SMS/MMS/RCS) para seus clientes em seus dispositivos móveis. É possível criar, personalizar e visualizar mensagens em formato de texto no editor de SMS/MMS/RCS.

As mensagens de texto podem ser criadas e enviadas em uma jornada ou em uma campanha. Para SMS, MMS e RCS, use a ação SMS.

* Em uma **jornada**. Crie uma jornada, adicione uma atividade de SMS e defina configurações básicas. Em seguida, navegue até o painel Ações de SMS à direita para criar o conteúdo da mensagem SMS, MMS ou RCS. [Saiba como criar uma jornada](../building-journeys/journey-gs.md)

* Em uma **Campanha**. Crie uma campanha, selecione SMS como sua ação e defina as configurações básicas. Em seguida, edite o conteúdo da mensagem para definir a mensagem SMS, MMS ou RCS que será enviada. [Saiba como criar uma campanha](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>Se esta for a primeira vez que cria mensagens de texto, certifique-se de que o canal de SMS foi configurado. [Saiba mais](sms-configuration.md)

## Recursos de mensagens de texto {#sms-capabilities}

O Adobe Journey Optimizer fornece recursos abrangentes de mensagem de texto para engajar clientes em vários canais:

**SMS (Serviço de Mensagens Curtas)**

Envie mensagens somente texto com até 160 caracteres. O SMS é o formato de mensagem de texto com maior compatibilidade em todos os dispositivos móveis.

**MMS (Serviço de Mensagens Multimídia)**

Melhore a comunicação com conteúdo multimídia, incluindo vídeos, imagens, clipes de áudio e GIFs. As mensagens MMS permitem até 1600 caracteres de texto, além de arquivos de mídia. [Saiba mais sobre as limitações de MMS](../start/guardrails.md#sms-guardrails)

**RCS (Serviços de Comunicação Avançada)**

Envie mensagens interativas com a sua marca utilizando recursos avançados como carrosséis, cartões multimídia, ações sugeridas e suporte de mídia aprimorado. O RCS fornece uma experiência de mensagens mais avançada em dispositivos compatíveis.

## Recursos principais {#key-features}

**Personalização e conteúdo dinâmico**

Crie mensagens de texto personalizadas com o editor de personalização. Adicione atributos de perfil, conteúdo condicional e dados dinâmicos para adaptar mensagens a destinatários individuais. [Saiba mais sobre personalização](../personalization/personalize.md)

**Suporte a vários provedores**

O Adobe Journey Optimizer integra-se aos principais provedores de serviços SMS:

* **Sinch** - [Guia de configuração](sms-configuration-sinch.md)
* **Twilio** - [Guia de configuração](sms-configuration-twilio.md)
* **Infobip** - [Guia de configuração](sms-configuration-infobip.md)
* **Provedores personalizados**: configure qualquer outro provedor SMS com a integração de API personalizada. [Saiba mais](sms-configuration-custom.md)

**Encurtamento e rastreamento de URL**

Adicione URLs rastreáveis e encurtados às mensagens para monitorar o engajamento. A configuração de subdomínio é necessária para a funcionalidade de encurtamento de URL. [Saiba como configurar subdomínios SMS](sms-subdomains.md)

**Gerenciamento da recusa**

Garanta a conformidade com os padrões e regulamentos do setor por meio do gerenciamento de recusa integrado. O Journey Optimizer lida automaticamente com palavras-chave de recusa padrão (PARAR, SAIR, CANCELAR, etc.) de provedores Sinch e Infobip. [Saiba mais sobre o gerenciamento de recusa](sms-opt-out.md)

**Visualização e teste**

Teste as mensagens de texto antes de enviar usando perfis de teste e dados de amostra. Visualize a personalização, o conteúdo e a formatação para garantir que as mensagens sejam exibidas corretamente. [Saiba como enviar mensagens](send-sms.md)

**Relatórios e análises**

Acompanhe o desempenho das campanhas e jornadas de SMS com recursos abrangentes de relatório:

* [Relatórios de campanha de SMS](../reports/campaign-global-report-cja-sms.md)
* [Relatórios de jornada de SMS](../reports/journey-global-report-cja-sms.md)

## Requisitos de configuração {#configuration-requirements}

Antes de enviar mensagens de texto, faça o seguinte:

1. **Escolha um provedor SMS**: selecione Sinch, Twilio, Infobip ou configure um provedor personalizado
2. **Configure as credenciais da API**: integre os tokens da API e as IDs de serviço do provedor ao Journey Optimizer
3. **Crie configurações de canal**: defina configurações de SMS para mensagens de marketing e transacionais
4. **Configure subdomínios (opcional)**: necessário somente se planeja usar o encurtamento de URL em mensagens

Essas etapas de configuração são normalmente realizadas pela administração do sistema. [Introdução à configuração de SMS](sms-configuration.md)

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
<p>Testar e enviar as mensagens de texto para o público-alvo</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validação" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Gerenciar recusas</strong></a>
</div>
<p>Processar solicitações de cancelamento de assinatura e garantir a conformidade</p>
</td>
</tr></table>

## Recursos adicionais {#additional-resources}

Navegue pelos tópicos abaixo para saber mais sobre mensagens de texto no Journey Optimizer.

+++Guias de configuração

Saiba como configurar o ambiente de SMS:

* [Visão geral da configuração do canal de SMS](sms-configuration.md)
* [Criar configurações do canal de SMS](sms-configuration-surface.md)
* [Configurar subdomínios SMS para encurtamento de URL](sms-subdomains.md)

+++

+++Guias de configuração do provedor

Configuração passo a passo para cada provedor de serviços SMS:

* [Configurar provedor Sinch](sms-configuration-sinch.md)
* [Configurar provedor Twilio](sms-configuration-twilio.md)
* [Configurar provedor Infobip](sms-configuration-infobip.md)
* [Configurar um provedor de SMS personalizado](sms-configuration-custom.md)

+++

+++Criação e gerenciamento de conteúdo

Crie, personalize e gerencie o conteúdo da mensagem de texto:

* [Criar mensagens SMS/MMS](create-sms.md)
* [Visualizar, testar e enviar mensagens](send-sms.md)
* [Personalização em mensagens de texto](../personalization/personalize.md)
* [Conteúdo dinâmico](../personalization/get-started-dynamic-content.md)

+++

+++Conformidade e privacidade

Verifique se as mensagens de texto estão em conformidade com regulamentos e padrões de privacidade:

* [Gerenciamento de recusa](sms-opt-out.md)
* [Privacidade e consentimento](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

+++

+++Acompanhamento de desempenho

Monitore e analise o desempenho das campanhas e da jornada de SMS:

* [Relatórios de campanha de SMS](../reports/campaign-global-report-cja-sms.md)
* [Relatórios de jornada de SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integração de jornada e campanha

Saiba como incorporar SMS nas jornadas e campanhas do cliente:

* [Adicionar mensagens SMS em jornadas](../building-journeys/journeys-message.md)
* [Criar campanhas SMS](../campaigns/create-campaign.md)

+++

## Vídeos tutoriais {#videos}

**Configurar e enviar mensagens SMS**

Saiba como configurar, criar e incluir mensagens de SMS nas jornadas do cliente.

+++Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**Explorar recursos de mensagens móveis**

Descubra os recursos abrangentes de mensagens móveis que o Adobe Journey Optimizer oferece aos profissionais de marketing.

+++Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**Enviar mensagens RCS com sua marca**

Saiba como configurar e enviar mensagens RCS interativas e alinhadas à marca no Adobe Journey Optimizer por meio de um provedor de SMS personalizado.

+++Ver vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**Tópicos relacionados**

* [Adicionar mensagens em jornadas](../building-journeys/journeys-message.md)
* [Criar campanhas de marketing](../campaigns/create-campaign.md)
* [Medidas de proteção e limitações](../start/guardrails.md#sms-guardrails)
* [Tutoriais de SMS e mensagens móveis](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/channels/sms-channel/sms-mms-messages-overview){target="_blank"}
