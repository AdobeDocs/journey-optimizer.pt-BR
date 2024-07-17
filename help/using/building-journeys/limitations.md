---
solution: Journey Optimizer
product: journey optimizer
title: Limitações do Jornada
description: Saiba mais sobre as limitações do Jornada
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: jornadas, limitação
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 47%

---

# Limitações {#journey-limitations}

Estas são as limitações relacionadas ao uso de jornadas do.

## Limitações gerais de ações {#action-limitations}

* Não há limitação de envio. 
* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida. 
* O evento **Reação** interno permite que você reaja a ações predefinidas (consulte esta [página](../building-journeys/reaction-events.md)). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado. 
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.

## Limitações de versões do Jornada {#journey-versions-limitations}

* Uma jornada que começa com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com um evento de **Qualificação de público-alvo**.
* Uma jornada que começa com uma atividade **Qualificação de público-alvo** em v1 deve sempre começar com uma **Qualificação de público-alvo** em outras versões.
* O público-alvo e o namespace escolhidos em **Qualificação de Público-Alvo** (primeiro nó) não podem ser alterados em novas versões.
* A regra de reentrada precisa ser a mesma em todas as versões da jornada.
* Uma jornada que começa com um **Público-alvo de leitura** não pode começar com outro evento nas próximas versões.

## Limitações de ações personalizadas {#custom-actions-limitations}

* O URL de ação personalizada não aceita parâmetros dinâmicos. 
* Somente os métodos de chamada POST e PUT são suportados. 
* O nome do parâmetro de consulta ou cabeçalho não deve começar com “.” ou &quot;$&quot;. 
* Endereços IP não são permitidos. 
* Endereços da Adobe internos (.adobe.) não são permitidos.

## Limitações de eventos {#events-limitations}

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada ao conteúdo de transmissão que entra no Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.

## Limitações das fontes de dados {#data-sources-limitations}

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e poder lidar com o volume de solicitações.

## Jornadas que começam ao mesmo tempo que a criação de um perfil {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API na Adobe Experience Platform. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a ingestão até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma Jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera depois do primeiro evento para conceder à Adobe Experience Platform o tempo necessário para executar a ingestão no Serviço de Perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento da experiência pode conter informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc).

## Ler limitações de público {#read-audiences-limitations}

* Os públicos-alvo transmitidos estão sempre atualizados, mas os públicos-alvo em lote não serão calculados no momento da recuperação. Eles só são avaliados diariamente no momento da avaliação diária do lote.
