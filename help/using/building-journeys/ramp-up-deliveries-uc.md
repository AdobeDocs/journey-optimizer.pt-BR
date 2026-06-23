---
solution: Journey Optimizer
product: journey optimizer
title: Aumente seus deliveries
description: Saiba como incrementar suas entregas
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: capacidade de entrega, jornada, caso de uso, email, reputação
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 807
ht-degree: 2%

---

# Caso de uso: incremente seus deliveries{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como criar uma jornada que amplie gradualmente suas entregas de email usando a atividade Otimizar e um limite de perfis, ajudando você a aquecer um novo endereço IP e a estabelecer a reputação do remetente.

>[!ENDSHADEBOX]

Se você mudou recentemente para outro provedor de serviços de email, endereço IP, domínio de email ou subdomínio, é necessário estabelecer sua reputação como remetente. Caso contrário, seus deliveries poderão ser bloqueados ou movidos para a pasta de spam da caixa de correio dos recipients. Saiba como aumentar sua reputação de email com o aquecimento de IP no [Guia de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=pt-BR){target="_blank"}.

Para aquecer seu IP, você pode aumentar gradualmente o número de deliveries. Leia mais sobre [otimização da entrega no Journey Optimizer](../reports/deliverability.md).

O objetivo deste caso de uso é criar uma jornada para incrementar suas entregas de email. Para configurar essa jornada, siga estas etapas:

1. Criar uma jornada. [Leia mais](journey-gs.md).

1. Adicione uma atividade **[!UICONTROL Otimizar]** à jornada. [Leia mais](optimize.md).

1. Nas configurações da atividade **[!UICONTROL Condição]**, defina o número máximo de destinatários para sua entrega:

   1. Nas configurações de atividade **[!UICONTROL Otimizar]**, selecione o método **[!UICONTROL Condições]** e defina o campo **[!UICONTROL Tipo]** como **[!UICONTROL Limite de perfis]**. [Leia mais](conditions.md#profile_cap).

   1. Defina o campo **[!UICONTROL Limit]** para o número máximo de destinatários desta entrega.

   ![Configuração da condição de limite de perfil para controlar o volume de entrega](assets/profile-cap-condition.png)

   É possível aumentar gradualmente esse limite até o número total de assinantes.

1. Adicione uma atividade de ação **[!UICONTROL Email]** ao caminho nominal após a atividade **[!UICONTROL Condição]**.

   ![Configuração de mensagem de email na jornada de entrega rampada](assets/ramp-up-deliveries-message.png)

   Quando a jornada for executada, a mensagem será enviada para os perfis de entrada, até o número máximo de perfis especificado. Quando esse limite é atingido, os perfis que entram pegam o caminho alternativo.

1. Conclua a jornada com as atividades de sua escolha.

Após o aquecimento do IP, é possível remover essa condição.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

- **TL;DR:** este caso de uso descreve como criar uma jornada do Adobe Journey Optimizer que aumenta gradualmente o volume de entrega de emails usando uma condição de limite de perfil para proteger a reputação do remetente durante o aquecimento de IP.

**Intenções:**
- Crie uma jornada para aumentar gradualmente o volume de entrega de emails para o aquecimento de IP
- Configure uma condição de Limite de perfil para limitar o número de recipients por execução de delivery
- Proteger a reputação do remetente ao alternar para um novo provedor de serviços de email, endereço IP ou domínio
- Remova a condição de limite de volume depois que o IP estiver totalmente aquecido

**Glossário:**
- **Aquecimento de IP**: o processo de aumentar gradualmente o volume de envio de email a partir de um novo endereço IP ou domínio para criar a reputação do remetente com os provedores de caixa de correio *(específico do produto)*
- **Limite de perfis**: um tipo de condição na atividade Otimize que limita o número máximo de perfis que recebem uma mensagem em uma determinada execução de jornada *(específico do produto)*
- **Atividade Otimizar**: uma atividade de tela de jornada usada para aplicar condições, regras de direcionamento ou experimentação para controlar como os perfis fluem por uma jornada *(específico do produto)*

**Medidas de Proteção:**
- Uma condição de Limite de perfil deve ser definida no método Conditions da atividade de Otimização para controlar o volume do delivery.
- Os perfis que excedem a limitação usam o caminho alternativo definido na jornada.
- O limite de perfil deve ser aumentado gradualmente ao longo do tempo até o número total de assinantes.

**Terminologia:**
- Nome canônico: Aumento dos deliveries — Acrônimo: nenhum — variantes: Aquecimento de IP, Aquecimento de IP, Aumento do delivery
- Sinônimos: &quot;Aquecimento de IP&quot; = &quot;Aquecimento de IP&quot; = &quot;criação de reputação do remetente&quot;
- Não confunda: &quot;Limite de perfil&quot; ≠ &quot;Limite de tamanho do público-alvo&quot; (O limite de perfil é um limite de delivery por execução; o tamanho do público-alvo é o número total de perfis qualificados)

**Perguntas frequentes:**
- **P: Por que preciso aumentar as entregas ao alternar para um novo IP ou domínio?** — um novo IP ou domínio não tem histórico de envio, portanto, os provedores de caixa de correio podem bloquear ou remover mensagens de pastas de spam até que uma reputação positiva seja estabelecida por meio de um volume gradativo e crescente.
- **P: Como a condição de limite de perfil controla o volume de entrega?** — Define um número máximo de perfis que podem receber a mensagem em uma única execução de jornada; os perfis além desse limite tomam um caminho alternativo.
- **P: Quando posso remover a condição de limite de perfil?** — Quando o IP estiver totalmente aquecido e a reputação do remetente estiver estabelecida, você poderá remover a condição da jornada.
- **P: Posso aumentar o limite gradualmente ao longo do tempo?** — Sim; você pode atualizar o campo Limite na condição Limite de perfil para aumentar progressivamente o número de recipients por execução até a contagem completa de assinantes.

+++
