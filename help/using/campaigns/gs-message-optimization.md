---
solution: Journey Optimizer
product: journey optimizer
title: Introdução à otimização de conteúdo
description: Saiba como usar a otimização de conteúdo para fornecer conteúdo personalizado e otimizado em suas campanhas e jornadas.
feature: Experimentation, Targeting
topic: Content Management
role: User
level: Beginner
keywords: otimização, direcionamento, experimentação, teste A/B, campanhas, jornadas, personalização
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: fec72c63d41a41adce5107082c50a68a7b8c0af2
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 8%

---

# Introdução à otimização de conteúdo {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="Otimização de conteúdo"
>abstract="A otimização de conteúdo no Journey Optimizer permite testar diferentes versões do conteúdo e determinar qual tem melhor desempenho. Você pode usar o direcionamento para fornecer conteúdo personalizado a segmentos específicos, experimentação para testar várias variações ou combinar ambas as abordagens para estratégias de otimização sofisticadas."

A otimização de conteúdo oferece as ferramentas necessárias para enviar a mensagem certa ao público-alvo certo, na hora certa. Ao combinar insights orientados por dados com recursos avançados de personalização, você pode maximizar o engajamento e as conversões em suas campanhas e jornadas.

A otimização de conteúdo está disponível em [campanhas](../campaigns/create-campaign.md) e [jornadas](../building-journeys/journey-gs.md), permitindo que você aplique as mesmas estratégias de otimização em todos os pontos de contato do cliente.

➡️ [Saiba como aproveitar a otimização de conteúdo em uma campanha neste vídeo](#video)

## Recursos de otimização {#capabilities}

Com a otimização de conteúdo no Journey Optimizer, você pode:

* [Use o direcionamento](optimization-targeting.md) para fornecer conteúdo personalizado a segmentos específicos de público com base em atributos de perfil, dados contextuais ou associação de público.

* [Execute experimentos](optimization-experimentation.md) para testar várias variações de conteúdo e identificar qual tem melhor desempenho com base em suas métricas de sucesso.

* [Combine ambas as abordagens](optimization-combination.md) para criar estratégias de otimização sofisticadas onde você testa variações diferentes para cada segmento direcionado.

## Direcionamento versus experimentação {#targeting-vs-experimentation}

Entender a diferença entre direcionamento e experimentação ajuda você a escolher a abordagem de otimização correta para suas metas.

**O direcionamento** usa regras determinísticas para fornecer conteúdo personalizado a segmentos específicos com base em atributos de perfil conhecidos, contexto ou associação de público-alvo. Ela garante que a mensagem certa chegue ao público-alvo correto.

**A experimentação** usa atribuição aleatória para testar várias variações de conteúdo e descobrir qual tem melhor desempenho. Ele ajuda você a saber o que mais corresponde ao seu público-alvo por meio de testes orientados por dados.

A tabela abaixo resume as principais diferenças:

| Recurso | Direcionamento | Experimentação |
|--------|-----------|-----------------|
| **Método de atribuição** | Determinístico - com base em regras | Aleatório - com base na alocação de tráfego |
| **Baseado em** | Atributos de perfil, contexto, públicos-alvo | Distribuição aleatória |
| **Caso de uso** | Fornecer conteúdo relevante a segmentos conhecidos | Descubra qual conteúdo tem melhor desempenho |
| **Exemplo** | Mostrar promoções diferentes por localização | Teste 2 linhas de assunto para ver quais ficam mais abertas |
| **Recomendado para** | Personalization em escala | Otimização e aprendizado |

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Casos de uso comuns {#use-cases}

Estes são alguns cenários típicos em que a otimização de conteúdo pode ajudar você a obter melhores resultados:

Direcionamento:

* **Direcionamento geográfico** - Envie ofertas específicas de localização com base na localização dos clientes. Por exemplo, promova casacos de inverno em regiões mais frias e maiôs em climas mais quentes.

* **Otimização do dispositivo** - Forneça conteúdo específico do dispositivo, como layouts otimizados para desktop para usuários de desktop e layouts otimizados para dispositivos móveis para usuários de smartphone.

Experimentação:

* **Teste A/B** - Teste diferentes linhas de assunto do email, botões do call-to-action ou ofertas promocionais para descobrir quais geram mais conversões.

* **Marketing do ciclo de vida** - teste mensagens de integração diferentes para novos clientes em comparação às ofertas de retenção para clientes existentes.

Combinação:

* **Segmentação avançada** - Direcione clientes por nível de fidelidade e teste mensagens de recompensa diferentes em cada nível para maximizar o engajamento em todos os segmentos.

## Introdução {#get-started}

Para começar a otimizar seu conteúdo:

1. **Criar uma campanha ou jornada**: configure sua [campanha](../campaigns/create-campaign.md) ou a [jornada](../building-journeys/journey-gs.md) e adicione pelo menos uma ação.

1. **Escolha sua abordagem de otimização**:
   * [Use o direcionamento](optimization-targeting.md) para personalizar o conteúdo de segmentos específicos.
   * [Use a experimentação](optimization-experimentation.md) para testar várias variações.
   * [Combine ambos](optimization-combination.md) para otimização avançada.

1. **Definir seu conteúdo**: crie as diferentes variações de conteúdo para sua estratégia de otimização.

1. **Ativar e monitorar**: inicie sua campanha ou jornada otimizada e acompanhe o desempenho nos [relatórios](../reports/campaign-global-report-cja.md).

## Como funciona {#how-it-works}

Assim que a jornada ou campanha estiver ativa, os perfis serão avaliados de acordo com os critérios definidos. Com base nessas avaliações, cada perfil recebe a versão de conteúdo mais apropriada:

1. **Avaliação do perfil** - Quando um perfil entra em sua campanha ou jornada, a Journey Optimizer avalia seus atributos e contexto.

1. **Atribuição de conteúdo** - Com base na sua configuração de otimização:
   * Para o **direcionamento**, os perfis que correspondem a critérios específicos recebem o conteúdo personalizado correspondente.
   * Para **experimentação**, os perfis são atribuídos aleatoriamente a diferentes variações de conteúdo com base nas configurações de alocação de tráfego.
   * Para **combinações**, os perfis primeiro correspondem a uma regra de direcionamento e, em seguida, são atribuídos aleatoriamente a uma das variações de experimento para esse segmento.

1. **Rastreamento de desempenho** - O Journey Optimizer rastreia automaticamente as métricas de envolvimento e os dados de conversão para ajudar você a identificar qual conteúdo tem melhor desempenho.

## Vídeo tutorial {#video}

Saiba como aproveitar a otimização de conteúdo em campanhas acionadas por ação ou API. Você aprenderá a direcionar subconjuntos do público-alvo, criar variações de mensagem por local, habilitar o conteúdo de fallback e executar vários experimentos em uma mesma campanha. Este tutorial também aborda como gerenciar campanhas com vários canais e, ao mesmo tempo, manter a consistência das mensagens.

>[!VIDEO](https://video.tv.adobe.com/v/3470373?captions=por_br&quality=12)

**Tópicos relacionados**

* [Criar uma campanha](../campaigns/create-campaign.md)
* [Criar uma jornada](../building-journeys/journey-gs.md)
* [Experimento de conteúdo](../content-management/get-started-experiment.md)
