---
solution: Journey Optimizer
product: journey optimizer
title: Otimização de tempo de envio para mensagens móveis
description: Saiba como configurar e usar a Otimização de tempo de envio para mensagens móveis no Adobe Journey Optimizer.
feature: SMS
topic: Send Time Optimization
role: User
level: Intermediate
exl-id: 56ff1000-7799-40ff-8f03-2f5868d05e7b
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: f03a3a13-9e99-4c7c-a1ae-0f4d07ced35c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 1%

---


# Otimização de tempo de envio para mensagens móveis {#sms-send-time-optimization}

>[!AVAILABILITY]
>
>A Otimização de tempo de envio para mensagens móveis (SMS, RCS e WhatsApp) está disponível a partir do segundo semestre de 2026 e se aplica a Jornadas e campanhas.

## Visão geral {#overview}

A Otimização de tempo de envio (STO) para mensagens móveis permite que os profissionais de marketing ultrapassem o agendamento de &quot;lote e explosão&quot; usando insights orientados por IA para determinar o tempo de entrega ideal para cada perfil individual. Em vez de enviar mensagens para todo o público-alvo de uma só vez, o Adobe Journey Optimizer analisa os padrões históricos de engajamento de cada perfil e prevê quando é mais provável que esse indivíduo abra, clique ou responda a uma mensagem SMS, RCS ou WhatsApp.

Ao enviar mensagens no momento de maior envolvimento previsto, o STO ajuda a aumentar as taxas de abertura, as taxas de click-through e o ROI geral da campanha, sem exigir a segmentação manual do público-alvo por fuso horário ou coorte comportamental. O STO para mensagens móveis é compatível com canais SMS, RCS e WhatsApp e está disponível nos contextos de execução do Jornada e do Campaign.

## Pré-requisitos {#prerequisites}

Antes de ativar a Otimização de tempo de envio para mensagens móveis, verifique o seguinte:

- Sua organização está provisionada para o Adobe Journey Optimizer e para pelo menos um dos canais SMS, RCS ou WhatsApp.
- Existe um volume suficiente de dados históricos do engajamento móvel — incluindo eventos de envio, aberturas, cliques em links e respostas — para o público-alvo no Adobe Experience Platform (AEP). O modelo de IA exige um histórico de interação anterior para gerar previsões confiáveis por perfil.
- A superfície de canal relevante (SMS, RCS ou WhatsApp) está configurada e ativa na instância do AJO. Consulte [Configurar superfícies de canal de SMS](../sms/sms-configuration.md) para obter instruções de instalação.
- Para casos de uso baseados em Jornada, a Jornada deve ser projetada de modo que o nó de ação da mensagem não seja restrito por nós de espera de upstream ou de evento cujos tempos limite entrem em conflito com a janela de delivery STO.

>[!NOTE]
>
>Perfis com dados históricos de engajamento insuficientes retornam a um tempo de envio padrão definido durante a configuração. As previsões STO são geradas e pontuadas em nível de perfil individual.

## Como funciona {#how-it-works}

O STO para mensagens móveis depende de um modelo de IA criado com propósitos específicos que processa os sinais de engajamento histórico de cada perfil para prever a janela de entrega ideal. As etapas a seguir descrevem o fluxo de ponta a ponta.

### &#x200B;1. Assimilação de dados e treinamento de modelo

O modelo de IA assimila continuamente eventos de envolvimento móvel armazenados no Adobe Experience Platform, incluindo carimbos de data e hora de abertura de mensagens, eventos de clique em links, tempos de resposta e registros históricos de entrega. Esses sinais formam os dados de treinamento usados para aprender padrões comportamentais para cada perfil — como horas de interação preferidas, tendências de dia da semana e capacidade de resposta em fusos horários. O modelo é retreinado continuamente para permanecer sensível a mudanças no comportamento de engajamento.

### &#x200B;2. Pontuação de previsão por perfil

Depois de treinado, o modelo classifica cada perfil no público-alvo e produz uma janela de tempo de envio ideal. Essa previsão é gravada de volta no perfil no AEP como um atributo calculado, disponibilizando-o para Jornadas e Campanhas no tempo de execução sem exigir chamadas de API adicionais ou pesquisas em tempo real durante o envio da mensagem.

### &#x200B;3. Agendamento do tempo de execução do Jornada

Quando uma Jornada contendo um nó de ação de SMS, RCS ou WhatsApp habilitado para STO está ativa, o tempo de execução da Jornada lê cada atributo de tempo de envio previsto do perfil qualificado à medida que o perfil atinge o nó de ação. A mensagem é mantida dentro da janela de otimização configurada e despachada quando o tempo ideal previsto chega. Se o tempo previsto já tiver passado ou cair fora da janela, o comportamento de fallback configurado será aplicado.

### &#x200B;4. Distribuição de envio de campanha

Para Campanhas, o STO distribui o envio pelo público com base em previsões por perfil em vez de emitir um único despacho em massa. O AJO distribui a entrega pela janela de envio configurada da campanha, respeitando o tempo ideal previsto de cada perfil e permanecendo dentro dos limites da janela definidos.

>[!NOTE]
>
>Se o tempo ideal previsto de um perfil sair da janela de envio configurada, a mensagem será enviada no limite mais próximo — o início ou o fim da janela — o que estiver mais próximo da previsão.

## Configurar a otimização de tempo de envio {#configure}

### Ativar o STO em uma campanha {#configure-campaign}

1. No Journey Optimizer, navegue até **Campanhas** e crie uma nova campanha ou abra um rascunho existente.
2. Selecione **SMS**, **RCS** ou **WhatsApp** como canal e conclua as etapas de conteúdo do público-alvo e da mensagem.
3. Na seção **Agendamento**, selecione **Otimização de hora de envio** em vez de uma data e hora de envio fixas.
4. Use a opção **Enviar Otimização de Tempo** para habilitar o recurso.
5. Configurar a **Janela de envio**: defina as horas de início e término nas quais o AJO tem permissão para entregar mensagens. A janela deve durar pelo menos uma hora e pode se estender até 24 horas.
6. Defina um **Tempo de envio de fallback** para perfis que não têm histórico de envolvimento suficiente para gerar uma previsão. Você pode optar por enviar imediatamente na janela aberta ou em um horário fixo dentro da janela.
7. Conclua as etapas de limite de frequência, revisão e ativação e, em seguida, ative a campanha.

### Ativar STO em uma Jornada {#configure-journey}

1. Abra ou crie uma Jornada na tela de Jornada.
2. Adicione ou selecione um nó de ação **SMS**, **RCS** ou **WhatsApp**.
3. No painel de configuração do nó de ação, expanda as configurações de **Tempo de envio**.
4. Ative **Enviar Otimização de Tempo** para o estado habilitado.
5. Defina a **Janela de otimização**: a duração máxima (em horas) que o tempo de execução pode conter uma mensagem enquanto aguarda o tempo de entrega ideal previsto. A janela padrão é de seis horas; o máximo é de 24 horas.
6. Configure o **Comportamento de fallback** — envie imediatamente quando um perfil entrar no nó ou aguarde até a próxima janela prevista disponível — para perfis que não têm dados de previsão.
7. Salve a configuração do nó e publique a Jornada.

>[!NOTE]
>
>Quando o STO está ativo em um nó de ação de Jornada, o tempo de delivery efetivo de um perfil pode ser diferente do momento em que o perfil entra no nó por até o tamanho total da janela de otimização configurada. Considere esse atraso ao projetar nós de espera upstream e definir tempos limite em nível de Jornada para evitar saídas prematuras de jornada.

## Medidas de proteção e limitações {#guardrails}

- O STO se aplica somente a mensagens de saída SMS, RCS e WhatsApp. Os fluxos de resposta de entrada e as sessões de mensagens bidirecionais não estão sujeitos à programação STO.
- Cada nó de ação de campanha ou Jornada oferece suporte a uma superfície de canal por mensagem habilitada para STO. A coordenação entre canais STO (por exemplo, SMS e WhatsApp em um único nó) não é compatível.
- O modelo de IA exige um mínimo de 30 dias de dados históricos do engajamento móvel por perfil para produzir uma previsão. Os perfis abaixo desse limite usam o tempo de envio de fallback configurado.
- O STO interage com regras de limite de frequência. Se a janela de entrega prevista de um perfil limitado entrar em conflito com um limite de limite, a mensagem será suprimida de acordo com a regra de limite e não será reagendada para uma janela posterior.
- Sinalizadores de consentimento, registros de recusa e listas de supressão global são sempre aplicados independentemente da programação STO. Uma mensagem mantida para entrega otimizada ainda está sujeita a verificações de consentimento no momento do envio.
- O STO não está disponível para mensagens transacionais em que a entrega imediata é exigida por requisitos comerciais ou normativos.

## Tópicos relacionados {#related-topics}

- [Introdução a SMS, RCS e WhatsApp no Journey Optimizer](../sms/create-sms.md)
- [Configurar superfícies de canal de SMS](../sms/sms-configuration.md)
- [Otimização de tempo de envio para notificações por email e por push](../building-journeys/send-time-optimization.md)
- [Classificação baseada em IA no Journey Optimizer](../offers/offer-activities/ai-ranking.md)
- [Notas de versão do Journey Optimizer](../rn/release-notes.md)
