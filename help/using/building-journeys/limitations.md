---
title: Limitações da jornada
description: Saiba mais sobre as limitações do Jornada
feature: Jornadas
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Limitações {#journey-limitations}

![](../assets/do-not-localize/badge.png)

Estas são limitações relacionadas ao uso de jornadas.

## Limitações da lista de jornadas

* Na lista jornadas, filtros, pesquisas e seleção de coluna são redefinidos na atualização da página.

## Limitações de ações gerais

* Não há limitação de envio. 
* Duas tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida. 
* O evento integrado **Reaction** permite reagir a ações predefinidas (consulte esta [página](../building-journeys/reaction-events.md)). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado. 
* Não há integração produzida pela Adobe Campaign Classic.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.

## Limitações da ação de mensagem

* A atividade **Message** não permite usar dados contextuais provenientes da jornada. A personalização das mensagens é executada diretamente ao projetar a mensagem no Journey Optimizer.

* Ao adicionar uma mensagem multicanal, duas mensagens serão enviadas.

## Limitações das versões do Jornada {#journey-versions-limitations}

* uma jornada que inicia com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com um evento de **Qualificação de segmento**.
* uma jornada que começa com uma atividade **Segment Qualification** em v1 deve sempre começar com uma **Segment Qualification** em outras versões.
* O segmento e o namespace escolhidos em **Segment qualification** (primeiro nó) não podem ser alterados em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões do jornada.
* Uma jornada que começa com um **Ler segmento** não pode começar com outro evento nas próximas versões.
 

## Limitações de ações personalizadas

* O URL de ação personalizada não suporta parâmetros dinâmicos. 
* Somente métodos de chamada POST e PUT são compatíveis. 
* O nome do parâmetro de consulta ou cabeçalho não deve começar com &quot;.&quot; ou &quot;$&quot;. 
* Endereços IP não são permitidos. 
* Endereços Adobe internos (.adobe.) não são permitidas.
 

## Limitações de eventos

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada à carga de transmissão que entra no Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.
 

## Limitações das fontes de dados

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e podem lidar com o volume de solicitações.

## Jornadas que começam ao mesmo tempo que uma criação de perfil {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API no Adobe Experience Platform. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a assimilação até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma Jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera após o primeiro evento para conceder ao Adobe Experience Platform o tempo necessário para executar a assimilação no Serviço de perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada foi projetada para confirmar a criação de uma conta, o evento de experiência pode conter as informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc.).

## Ler limitações do segmento

* Não é possível acionar uma jornada baseada em segmento em um período de tempo menor que 1 hora.
* Os segmentos continuados estão sempre atualizados, mas os segmentos em lote não serão calculados no momento da recuperação. Só são avaliados todos os dias no momento da avaliação diária do lote.
