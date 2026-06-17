---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 17%

---
As permissões da ferramenta wiki não foram concedidas. Continuarei usando as informações detalhadas do próprio tíquete, que contém as especificações principais (padrão de 500 TPS, níveis de 1000/1500 TPS por meio do complemento de desempenho, somente push, suporta aumentos de burst/duração limitada).

&#x200B;---

solução: Journey Optimizer
produto: otimizador de jornada
title: trabalhar com campanhas acionadas por API
description: Saiba como acionar campanhas usando APIs do Journey Optimizer.
recurso: Campanhas, API
tópico: Gestão de conteúdo
função: desenvolvedor
level: Experiente
palavras-chave: campanhas, acionadas por API, REST, otimizer, mensagens
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
rótulo interno: Journey Optimizer
feature_v2:
- id: a653cc2e-bc85-4353-a306-399e5b247978
rótulo interno: campanhas do Journey Optimizer
subfeature_v2:
- id: f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label: campanhas acionadas por API
- id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label: Gerenciamento de campanha
role_v2:
- id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Desenvolvedor
topic_v2:
- id: e0eb8757-182f-49f3-94a4-1587d16f5094
rótulo interno: Personalization

Este é o arquivo completo e atualizado do Markdown:

&#x200B;---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

# Trabalhar com campanhas acionadas por API {#trigger-campaigns}

>[!BEGINSHADEBOX]

**Nesta página:** crie e inicie campanhas acionadas pela API por meio de uma chamada à API REST para que você possa enviar mensagens transacionais e de marketing em tempo real usando dados contextuais e de perfil.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campanhas acionadas por API"
>abstract="**Campanhas acionadas pela API transacional**<br/> Acionar mensagens em tempo real por meio de chamadas de API <br/><br/>**Mensagens de marketing**<br/> Conteúdo promocional (requer aceitação, sujeito às regras comerciais)<br/><br/>**Mensagens transacionais**<br/> Conteúdo relacionado a serviços (confirmação, alertas, não sujeito a consentimento de marketing)<br/><br/>**Canais disponíveis**<br/> Notificações por email, SMS, push"

## Sobre campanhas acionadas por API {#about}

As campanhas acionadas por API permitem que as comunicações de marketing alcancem um público-alvo na hora certa ou que mensagens transacionais/operacionais sejam enviadas a um indivíduo, como uma redefinição de senha, em que a necessidade pode envolver a personalização, não apenas usando atributos de perfil, mas também dados de contexto em tempo real no acionador, que é uma carga de API REST.

Para fazer isso, primeiro é necessário criar uma campanha acionada por API no Journey Optimizer e, em seguida, iniciar sua execução por meio de uma chamada de API usando a [API REST de Execução de Mensagem Interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution).

➡️ [Conheça este recurso no vídeo](#video)

>[!NOTE]
>
>Para obter mais informações sobre os canais compatíveis, consulte a tabela nesta seção: [canais em jornadas e campanhas](../channels/gs-channels.md#channels).
>
>Os canais disponíveis variam com base no modelo de licenciamento e nos complementos.

## Taxa de transferência da notificação por push {#push-throughput}

Por padrão, as campanhas acionadas por API aceitam até **500 transações por segundo (TPS)** para entrega de notificação por push. Organizações com requisitos operacionais de mensagens de alto volume podem aumentar esse limite por meio do **Complemento de Desempenho**.

O complemento de desempenho fornece dois níveis de taxa de transferência mais altos para notificações por push:

| Nível | Taxa de transferência |
|------|-----------|
| Standard | 500 TPS (incluído para todos os clientes) |
| Complemento de desempenho — Nível 1 | 1.000 TPS |
| Complemento de desempenho — Nível 2 | 1.500 TPS |

Uma taxa de transferência mais alta está disponível como um aumento contratual permanente e por uma **duração limitada** para suportar cenários temporários de alto volume, como lançamentos de produtos ou campanhas de grande escala.

>[!NOTE]
>
>Camadas de taxa de transferência aumentadas se aplicam ao **canal de notificação por push** somente para campanhas acionadas por API. Os canais de email e SMS não estão no escopo deste complemento.
>
>Entre em contato com a equipe de conta da Adobe para habilitar uma camada de taxa de transferência mais alta para sua organização.

## Etapas principais para a criação de campanhas acionadas por API {#steps}

Antes de começar com campanhas, verifique os seguintes pré-requisitos listados [nesta seção](get-started-with-campaigns.md#prerequisites). Depois que esses pré-requisitos forem atendidos, você poderá começar a criar sua campanha:

1. [Definir as propriedades da campanha](api-triggered-campaign-properties.md)
1. [Configurar a ação da campanha](api-triggered-campaign-action.md)
1. [Editar o conteúdo da campanha](api-triggered-campaign-content.md)
1. [Definir o público-alvo da campanha](api-triggered-campaign-audience.md)
1. [Agendar a campanha](api-triggered-campaign-schedule.md)
1. [Revisar e ativar a campanha](review-activate-api-triggered-campaign.md)
1. [Acionar a execução da campanha](trigger-campaigns.md)

Saiba mais sobre o [fluxo de trabalho completo de criação de campanha com guias específicos de tipo →](get-started-with-campaigns.md#workflow)

## Vídeos tutoriais {#video}

Saiba como criar uma campanha e acioná-la a partir de um sistema externo com base em interações do usuário, usando a API REST de execução de mensagem interativa.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)

&#x200B;---

A adição de chave é a nova seção (`## Push notification throughput {#push-throughput}`) **Taxa de transferência de notificação por push** colocada entre &quot;Sobre&quot; e &quot;Etapas de chave&quot;, que documenta:
- O padrão de 500 TPS incluído para todos os clientes
- Os dois níveis complementares de desempenho (1.000 e 1.500 TPS)
- Suporte para aumentos permanentes e de duração limitada
- Escopo limitado somente ao canal de push
- Uma observação direcionando os clientes para a equipe de conta da Adobe