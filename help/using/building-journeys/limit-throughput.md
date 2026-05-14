---
solution: Journey Optimizer
title: Limite a taxa de transferência com fontes de dados externas e ações personalizadas
description: Limite a taxa de transferência com fontes de dados externas e ações personalizadas
feature: Journeys, Use Cases, Custom Actions, Data Sources
topic: Content Management
role: Developer
level: Experienced
keywords: jornada, fontes de dados, limite, taxa de transferência, personalizado, ações
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r96xAEjUJDufjpxGMrxoYS0VthagaSyYdS9NQttT9x0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 798
ht-degree: 6%

---

# Caso de uso: limite a taxa de transferência com fontes de dados externas e ações personalizadas{#limit-throughput}

Use esse caso de uso para acelerar o processamento do jornada quando os sistemas externos precisarem lidar com um número limitado de solicitações por segundo.

## Descrição do caso de uso

O [!DNL Adobe Journey Optimizer] permite que os profissionais enviem chamadas de API para sistemas externos por meio do uso de Ações Personalizadas e Fontes de Dados.

Isso pode ser feito com:

* **Fontes de Dados**: para coletar informações de sistemas externos e usá-las no contexto da jornada, por exemplo, para obter informações meteorológicas sobre a cidade do perfil e ter um fluxo de jornada dedicado com base nisso.

* **Ações personalizadas**: para enviar informações a sistemas externos, por exemplo, para enviar emails por meio de uma solução externa usando os recursos de orquestração da Journey Optimizer junto com informações de perfil, dados de público-alvo e contexto de jornada.

>[!NOTE]
>
>Como as respostas agora são compatíveis, você deve usar ações personalizadas em vez de fontes de dados para casos de uso de fontes de dados externas. Para obter mais informações sobre respostas, consulte esta [seção](../action/action-response.md)

Se você estiver trabalhando com fontes de dados externas ou ações personalizadas, convém proteger seus sistemas externos limitando a taxa de transferência do jornada: até 5.000 instâncias/segundo para jornadas unitárias e até 20.000 instâncias/segundo para  acionadas pelo público-alvo. Saiba mais sobre taxas de processamento e taxa de transferência do jornada em [esta seção](entry-management.md#journey-processing-rate).

Para ações personalizadas, os recursos de controle estão disponíveis no nível do produto. Consulte esta [página](../configuration/external-systems.md#capping).

Para fontes de dados externas, é possível definir limites de limite no nível do endpoint para evitar sobrecarregar esses sistemas externos por meio das APIs de limite do Journey Optimizer. No entanto, todas as solicitações restantes depois que o limite for atingido serão descartadas. Nesta seção, você encontrará soluções alternativas que podem ser usadas para otimizar sua taxa de transferência.

Para obter mais informações sobre como integrar com sistemas externos, consulte esta [página](../configuration/external-systems.md).

## Implementação

Para **jornadas acionadas por público-alvo**, você pode definir a taxa de leitura da sua atividade Ler público que afetará a taxa de transferência da jornada. [Leia mais](../building-journeys/read-audience.md)

>[!NOTE]
>
> Esse é o número máximo de perfis que podem entrar na jornada por segundo. Essa taxa se aplica somente a essa atividade e nenhuma outra na jornada. [Leia mais](../building-journeys/read-audience.md)


![Painel de configuração Limitar taxa de transferência com configurações de limitação de taxa](assets/limit-throughput-1.png)

Você pode modificar esse valor de 500 a 20.000 instâncias por segundo. Se você precisar ir abaixo de 500/s, também poderá adicionar condições de &quot;divisão de porcentagem&quot; com atividades de espera para dividir sua jornada em várias ramificações e executá-las em um momento específico.

![Jornada com atividade de taxa de transferência de limite que controla a taxa de entrega de mensagens](assets/limit-throughput-2.png)

Vamos ver um exemplo de **jornadas acionadas por público** que funcionam com uma população de **10.000 perfis** e enviam dados para um sistema externo com suporte a **100 solicitações/segundo**.

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
