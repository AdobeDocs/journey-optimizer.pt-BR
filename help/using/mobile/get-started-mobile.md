---
solution: Journey Optimizer
product: journey optimizer
title: Introdução a mensagens móveis
description: Saiba como criar e enviar mensagens de texto no Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c13ff12d-60f1-49cd-833a-d43359628223
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7b5244e8bdbbe7458f283ac883cfaf1d695b332e
workflow-type: tm+mt
source-wordcount: 1005
ht-degree: 30%

---

# Introdução a mensagens móveis {#get-started-sms}

>[!IMPORTANT]
>
>Se esta for a primeira vez que você cria mensagens móveis, verifique se o Canal de mensagens móveis foi configurado. [Saiba mais](mobile-configuration.md)

Use o [!DNL Journey Optimizer] para enviar mensagens móveis aos seus clientes por três canais, o **SMS**, o **MMS** e o **RCS**, a partir de um único editor de SMS/MMS/RCS, onde você pode criar, personalizar e visualizar seu conteúdo.

* **SMS (Short Message Service)**: envia mensagens somente texto de até 160 caracteres, com suporte em todos os dispositivos móveis.
* **MMS (Serviço de Mensagens Multimídia)**: enriqueça suas mensagens com imagens, vídeos, clipes de áudio e GIFs, além de até 1.600 caracteres de texto. [Saiba mais sobre as limitações de MMS](../start/guardrails.md#sms-guardrails)
* O **RCS (Serviços de Comunicação Avançada)**:Deliver apresenta conteúdo interativo e de marca diretamente no aplicativo de mensagens nativo de seus clientes, sem a necessidade de baixar mais aplicativos.

As mensagens móveis podem ser criadas e enviadas em uma jornada ou em uma campanha usando a ação Mensagem móvel:

* Em uma **Jornada**: adicione uma ação de mensagem móvel à jornada, defina as configurações básicas e escreva o conteúdo no painel Ações de mensagem móvel à direita. [Saiba como criar uma jornada](../building-journeys/journey-gs.md)

* Em uma campanha **Campanha**:Create, selecione Mensagem móvel como ação, defina configurações básicas e edite o conteúdo da mensagem. Saiba como criar [uma campanha de ação](../campaigns/campaign-action.md#action-campaign-action) | [uma campanha acionada por API](../campaigns/api-triggered-campaigns.md) | [uma campanha orquestrada](../orchestrated/create-orchestrated-campaign.md#create)


## Recursos principais {#key-features}

| Recurso | Descrição |
|---|---|
| **Personalização** | Personalize mensagens com atributos de perfil, conteúdo condicional e dados dinâmicos usando o editor de personalização. [Saiba mais](../personalization/personalize.md) |
| **Suporte do provedor** | Conecte-se com [Sinch](mobile-configuration-sinch.md), [Twilio](mobile-configuration-twilio.md), [Infobip](mobile-configuration-infobip.md) ou qualquer [provedor personalizado](mobile-configuration-custom.md) por meio da integração de API. |
| **Encurtamento de URL** | Adicione URLs rastreáveis e encurtados para monitorar o engajamento. Requer configuração de subdomínio. [Saiba mais](mobile-subdomains.md) |
| **Gerenciamento de recusa** | Manuseio integrado de palavras-chave de recusa padrão (PARAR, SAIR, CANCELAR etc.) Sinch e Infobip. [Saiba mais](mobile-opt-out.md) |
| **Visualização e teste** | Valide o conteúdo com perfis de teste e dados de amostra antes de enviar. [Saiba mais](send-mobile-message.md) |
| **Relatórios** | Acompanhe o desempenho da campanha e da jornada com os [relatórios de campanha](../reports/campaign-global-report-cja-sms.md) e os [relatórios de jornada](../reports/journey-global-report-cja-sms.md) dedicados. |

## Requisitos de configuração {#configuration-requirements}

Antes de enviar mensagens de texto, faça o seguinte:

1. **Escolha um provedor SMS**: selecione Sinch, Twilio, Infobip ou configure um provedor personalizado
2. **Configurar credenciais de API**: integre os tokens de API e as IDs de serviço do seu provedor ao Journey Optimizer
3. **Criar configurações de canal**: definir configurações de SMS para mensagens de marketing e transacionais
4. **Configurar subdomínios (opcional)**: obrigatório somente se você planeja usar a redução de URL em suas mensagens

Essas etapas de configuração são normalmente realizadas pela administração do sistema. [Introdução à configuração de SMS](mobile-configuration.md)

### Requisitos para RCS {#requirement-rcs}

Os seguintes pré-requisitos são necessários para usar o RCS no Journey Optimizer:

* **Credenciais da API RCS Sinch**: um administrador deve configurar as credenciais da API para o fornecedor Sinch RCS (ID do Projeto, ID do Aplicativo e Token da API). [Saiba mais](mobile-configuration-sinch.md)
* **Configuração do canal de mensagens móveis**: um administrador deve criar uma configuração de canal com uma credencial habilitada para RCS selecionada, para que as mensagens sejam entregues como RCS em vez de SMS. [Saiba mais](mobile-configuration.md)
* **SMS de fallback**: recomendado. Os recipients cujos dispositivos não suportam RCS não receberão a mensagem, a menos que o fallback de SMS esteja disponível. Os clientes sem volume de SMS existente devem comprar um SMS e um código curto. [Saiba mais](design-mobile.md#rcs-content)
* **Fornecedor com suporte**: a criação de RCS nativo requer Sinch RCS (revenda ou venda direta da Adobe). Twilio, Infobip e outros provedores devem usar uma integração de provedor personalizada.
* **Suporte a dispositivo**: a entrega RCS tem suporte em dispositivos Android e iOS. A disponibilidade da operadora e da região varia, o RCS não está universalmente disponível globalmente.

## Recursos adicionais {#additional-resources}

Navegue pelos tópicos abaixo para saber mais sobre mensagens de texto no Journey Optimizer.

+++Guias de configuração

Saiba como configurar o ambiente de SMS:

* [Visão geral da configuração do canal de SMS](mobile-configuration.md)
* [Criar configurações do canal de SMS](mobile-configuration-surface.md)
* [Configurar subdomínios SMS para encurtamento de URL](mobile-subdomains.md)

+++

+++Guias de configuração do provedor

Configuração passo a passo para cada provedor de serviços SMS:

* [Configurar provedor Sinch](mobile-configuration-sinch.md)
* [Configurar provedor Twilio](mobile-configuration-twilio.md)
* [Configurar provedor Infobip](mobile-configuration-infobip.md)
* [Configurar um provedor de SMS personalizado](mobile-configuration-custom.md)

+++

+++Criação e gerenciamento de conteúdo

Crie, personalize e gerencie o conteúdo da mensagem de texto:

* [Criar mensagens SMS/MMS](create-mobile-message.md)
* [Visualizar, testar e enviar mensagens](send-mobile-message.md)
* [Personalização em mensagens de texto](../personalization/personalize.md)
* [Conteúdo dinâmico](../personalization/get-started-dynamic-content.md)
* [Gere conteúdo de SMS com o Assistente de IA](../content-management/generative-text.md)

+++

+++Conformidade e privacidade

Verifique se as mensagens de texto estão em conformidade com regulamentos e padrões de privacidade:

* [Gerenciamento de recusa](mobile-opt-out.md)
* [Privacidade e consentimento](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Acompanhamento de desempenho

Monitore e analise o desempenho das campanhas e da jornada de SMS:

* [Relatórios de campanha de SMS](../reports/campaign-global-report-cja-sms.md)
* [Relatórios de jornada de SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integração de jornada e campanha

Saiba como incorporar SMS nas jornadas e campanhas do cliente:

* [Adicionar mensagens SMS em jornadas](../building-journeys/journey-action.md)
* [Criar campanhas SMS](../campaigns/create-campaign.md)

+++

+++Perguntas frequentes sobre o RCS

**As mensagens do RCS nativo estão disponíveis com Twilio ou Infobip?**

Não. O designer RCS nativo no Journey Optimizer não está disponível ao usar provedores SMS de terceiros, como Twilio ou Infobip. No entanto, as mensagens RCS podem ser enviadas por meio de uma [integração de provedor personalizada](mobile-configuration-custom.md).

**Por que comprar SMS junto com o RCS?**

O volume de SMS e um código curto devem ser adquiridos para habilitar o fallback de SMS, que é o caminho recomendado. Se o SMS não estiver configurado, os perfis cujo dispositivo ou operadora não oferece suporte ao RCS não receberão a mensagem.

**As mensagens RCS nativas estão disponíveis para clientes Sinch direct?**

Sim. Os clientes que usam a API de conversação da Sinch têm acesso à criação RCS nativa, incluindo clientes de revenda e Sinch direto da Adobe.

**O RCS está disponível em todos os lugares?**

Não. A adoção de operadoras continua a crescer globalmente, mas o RCS não é universalmente suportado em todas as operadoras e regiões. A disponibilidade regional e o suporte à operadora devem ser pesquisados no planejamento de campanhas RCS.

**Onde as mensagens do RCS aparecem no dispositivo?**

As mensagens RCS aparecem no mesmo lugar que as mensagens SMS padrão — no aplicativo de mensagens nativo do dispositivo. Eles chegam de um remetente marcado e verificado, dando aos recipients sinais de confiança para saber se a mensagem é legítima.

**Quais são os limites de caracteres para uma mensagem RCS?**

Os tipos de mensagem Rich Media (Único) são compatíveis com até 3.072 caracteres, significativamente mais do que o limite de 160 caracteres para SMS padrão. Os tipos básicos de mensagem RCS são limitados a 160 caracteres, correspondendo ao limite padrão de SMS.

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
