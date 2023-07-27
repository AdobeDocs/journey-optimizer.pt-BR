---
solution: Journey Optimizer
title: Limite a taxa de transferência com Fontes de dados externas e Ações personalizadas
description: Limite a taxa de transferência com Fontes de dados externas e Ações personalizadas
feature: Journeys
topic: Content Management
role: User, Developer
level: Experienced
keywords: jornada, fontes de dados, limite, taxa de transferência, personalizado, ações
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 4%

---

# Caso de uso: limite a taxa de transferência com Fontes de dados externas e Ações personalizadas{#limit-throughput}

## Descrição do caso de uso

O Adobe Journey Optimizer permite que os profissionais enviem chamadas de API para sistemas externos por meio do uso de Ações personalizadas e Fontes de dados.

Isso pode ser feito com:

* **Fontes de dados**: para coletar informações de sistemas externos e usá-las no contexto da jornada, por exemplo, para obter informações meteorológicas sobre a cidade do perfil e ter um fluxo de jornada dedicado com base nisso.

* **Ações Personalizadas**: para enviar informações a sistemas externos, por exemplo, para enviar emails por meio de uma solução externa usando os recursos de orquestração do Journey Optimizer junto com informações de perfil, dados de público-alvo e contexto de jornada.

Se estiver trabalhando com fontes de dados externas ou ações personalizadas, talvez você queira proteger seus sistemas externos limitando a taxa de transferência do jornada: até 5000 instâncias/segundo para jornadas unitárias e até 20000 instâncias/segundo para  acionadas pelo público-alvo.

Para ações personalizadas, os recursos de controle estão disponíveis no nível do produto. Consulte esta [página](../configuration/external-systems.md#capping).

Para fontes de dados externas, é possível definir limites de limite no nível do endpoint para evitar sobrecarregar esses sistemas externos por meio das APIs de limite do Journey Optimizer. No entanto, todas as solicitações restantes depois que o limite for atingido serão descartadas. Nesta seção, você encontrará soluções alternativas que podem ser usadas para otimizar sua taxa de transferência.

Para obter mais informações sobre como integrar com sistemas externos, consulte esta [página](../configuration/external-systems.md).

## Implementação

Para **jornadas acionadas pelo público**, você pode definir a taxa de limitação da sua atividade Read Audience que afetará a taxa de transferência da jornada. [Leia mais](../building-journeys/read-audience.md)

>[!NOTE]
>
> Este é o número máximo de perfis que podem entrar no público-alvo de leitura por segundo. Essa taxa se aplica somente a essa atividade e não a outras atividades na jornada. [Leia mais](../building-journeys/read-audience.md)

![](assets/limit-throughput-1.png)

Você pode modificar esse valor de 500 a 20.000 instâncias por segundo. Se você precisar ir abaixo de 500/s, também poderá adicionar condições de &quot;divisão de porcentagem&quot; com atividades de espera para dividir sua jornada em várias ramificações e executá-las em um momento específico.

![](assets/limit-throughput-2.png)

Vamos ver um exemplo de **jornadas acionadas pelo público** trabalhar com uma população de **10.000 perfis** e enviar dados para um sistema externo que suporte **100 solicitações/segundo**.

1. Você pode definir seu Público-alvo de leitura para ler perfis com uma taxa de transferência de 500 perfis/segundo, o que significa que levará 20 segundos para ler todos os perfis. No segundo 1, você lerá 500 deles, no segundo mais 2 500, etc.

1. Em seguida, você pode adicionar uma atividade de Condição &quot;divisão de porcentagem&quot; com uma divisão de 20% para ter a cada segundo 100 perfis em cada ramificação.

1. Depois disso, adicione as atividades Wait com um temporizador específico em cada ramificação. Aqui, configuramos uma espera de 30 segundos para cada um. A cada segundo, 100 perfis fluirão para cada ramificação.

   * Na ramificação 1, eles aguardarão 30 segundos, o que significa que:
      * no segundo 1, 100 perfis aguardarão pelo segundo 31
      * no segundo 2, 100 perfis aguardarão o segundo 32, etc.

   * Na ramificação 2, eles aguardarão 60 segundos, o que significa que:
      * No segundo 1, 100 perfis aguardarão o segundo 61 (1&#39;01&#39;&#39;)
      * No segundo 2, 100 perfis aguardarão o segundo 62 (1&#39;02&#39;&#39;) etc.

   * Sabendo que esperamos 20 segundos no máximo para ler todos os perfis, não haverá sobreposição entre cada ramificação, sendo os últimos 20 segundos em que os perfis fluirão para a condição. Entre o segundo 31 e o segundo 51, todos os perfis na ramificação 1 serão processados. Entre os segundos 61 (1&#39;01&#39;&#39;) e 81 (1&#39;21&#39;&#39;), todos os perfis na ramificação 2 serão processados etc.

   * Como proteção, você também pode adicionar uma sexta ramificação para ter menos de 100 perfis por ramificação, especialmente se o sistema externo oferecer suporte apenas a 100 solicitações por segundo.

>[!IMPORTANT]
>
>Como em qualquer solução alternativa, teste essa solução completamente antes de entrar em produção para garantir que ela faça o que você deseja.

Como proteção adicional, você também pode usar os recursos de Limite.

>[!NOTE]
>
>Ao contrário dos recursos de Limite, que protegem um endpoint por serem globais para todas as jornadas de uma sandbox, essa solução alternativa funciona somente no nível da jornada. Isso significa que, se várias jornadas estiverem sendo executadas em paralelo e estiverem direcionadas para o mesmo endpoint, será necessário considerar isso ao projetar a jornada. Portanto, essa solução alternativa não é adequada para cada caso de uso.
