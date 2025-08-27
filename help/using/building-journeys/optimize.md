---
solution: Journey Optimizer
product: journey optimizer
title: Atividade de condição
description: Saiba mais sobre a atividade de condição
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: atividade, condição, tela, jornada, otimização
badge: label="Disponibilidade limitada" type="Informative"
hidefromtoc: true
hide: true
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
source-git-commit: 19130e9eb5a2144afccab9fa8e5632de67bc7157
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 3%

---

# Otimizar atividade {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Otimizar atividade"
>abstract="A atividade **Otimizar** permite definir como as pessoas avançam na sua jornada criando vários caminhos com base em critérios específicos, incluindo experimentação, direcionamento e condições específicas."

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o seu representante da Adobe para obter acesso.

A atividade **Otimizar** permite definir como as pessoas avançam na sua jornada criando vários **caminhos** com base em critérios específicos, incluindo experimentação, direcionamento e condições específicas, garantindo o máximo de envolvimento e sucesso na criação de jornadas altamente personalizadas e eficazes.

Um **caminho de jornada** pode consistir em qualquer um dos seguintes:

* Sequência das comunicações;
* tempo entre eles;
* número de comunicações;
* ou qualquer combinação dessas três variáveis.

Por exemplo, um caminho pode conter um email, outro pode conter duas mensagens SMS e um terceiro pode conter um email, um nó [Wait](wait-activity.md) de duas horas e, em seguida, uma mensagem SMS.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

Através da atividade **Otimizar**, você pode:

* Executar [experimentos de caminho](#experimentation)
* Aproveite as regras de [direcionamento](#targeting) em cada caminho de jornada
* Aplicar [condições](#conditions) aos seus caminhos

![](assets/journey-optimize.png)

Quando a jornada estiver ativa, os perfis serão avaliados de acordo com os critérios definidos e, com base nos critérios de correspondência, serão enviados pelo caminho apropriado da jornada.

## Usar experimentação {#experimentation}

A experimentação permite testar caminhos diferentes com base em uma divisão aleatória para determinar qual tem o melhor desempenho com base em métricas de sucesso predefinidas.

Para configurar a experimentação em uma jornada, siga as etapas abaixo.

Digamos que você deseje comparar três caminhos:

* um caminho com um email;
* um segundo caminho com um nó Wait de dois dias e um email;
* um terceiro caminho com um email e, em seguida, uma mensagem SMS.

1. Solte a atividade **[!UICONTROL Otimizar]** na tela de jornada.

1. Adicione um rótulo opcional para identificar a atividade nos relatórios e logs do modo de teste.

1. Selecione **[!UICONTROL Experimento]** na lista suspensa **[!UICONTROL Método]**.

   ![](assets/journey-optimize-experiment.png){width=85%}

1. Clique em **[!UICONTROL Configurações de experimento]**.

1. Projete e configure seu experimento conforme desejado. [Saiba como](../content-management/content-experiment.md)

   <!--
    ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}
    Replace with appropriate screenshot
    The experiment applies to all the activities in the journey.TBC
   -->

Quando a jornada estiver ativa, os usuários serão atribuídos aleatoriamente para percorrer caminhos diferentes. [!DNL Journey Optimizer] rastreia qual caminho gera mais compras e fornece insights acionáveis.

<!--Follow the success of your journey with the [Experimentation journey report](../reports/campaign-global-report-cja-experimentation.md). Is there a report specific to experimentation in journey?-->

### Casos de uso com o experimento {#uc-experiment}

Os exemplos a seguir mostram como usar a atividade **[!UICONTROL Otimizar]** com o método **[!UICONTROL Experimento]** para determinar qual caminho funciona melhor em geral.

**Eficácia do canal**

Teste se o envio da primeira mensagem por email ou por SMS gera conversões mais altas.

* Use a taxa de conversão como a métrica de otimização (por exemplo: compras, inscrições).

![](assets/journey-optimize-experiment-uc.png)

**Frequência da mensagem**

Execute um experimento para verificar se o envio de um email contra três emails em uma semana resulta em mais compras.

* Use compras ou a taxa de cancelamento de inscrição como a métrica de otimização.

**Tempo de espera entre comunicações**

Compare uma espera de 24 horas com uma de 72 horas antes de um acompanhamento para determinar qual tempo maximiza o engajamento.

* Use a taxa de click-through ou a receita como a métrica de otimização.

## Aproveitar o direcionamento {#targeting}

O direcionamento permite determinar regras ou qualificações específicas que devem ser atendidas para que um cliente seja qualificado para inserir um dos caminhos de jornada, com base em segmentos específicos de público-alvo<!-- depending on profile attributes or contextual attributes-->.

Ao contrário da experimentação, que é uma atribuição aleatória de um determinado caminho, o direcionamento é determinístico em termos de garantir que o público ou perfil correto entre no caminho especificado.

Com o direcionamento, regras específicas podem ser definidas com base em:

* **Atributos de perfil de usuário**, como localização (por exemplo, geolocalização), idade ou preferências. Por exemplo, os usuários nos EUA veem uma promoção &quot;Golden Gate&quot;, enquanto os usuários na França veem uma promoção &quot;Torre Eiffel&quot;.

* **Dados contextuais**, como tipo de dispositivo (por exemplo, direcionamento de dispositivo), hora do dia ou detalhes da sessão. Por exemplo, os usuários de desktop recebem conteúdo otimizado para desktop, enquanto os usuários móveis recebem conteúdo otimizado para dispositivos móveis.

* **Públicos-alvo** que podem ser usados para incluir ou excluir perfis que tenham uma associação de público-alvo específica.

Para configurar o direcionamento em uma jornada, siga as etapas abaixo.

1. Solte a atividade **[!UICONTROL Otimizar]** na tela de jornada.

1. Adicione um rótulo opcional para identificar a atividade nos relatórios e logs do modo de teste.

1. Selecione **[!UICONTROL Direcionamento]** na lista suspensa **[!UICONTROL Método]**.

   ![](assets/journey-optimize-targeting.png){width=85%}

1. Clique em **[!UICONTROL Criar regra de direcionamento]**.

1. Use o construtor de regras para definir seus critérios. Por exemplo, defina uma regra para residentes dos EUA, uma regra para residentes da França e uma regra para residentes da Índia.

   ![](assets/journey-targeting-rule.png)

1. Selecione o **[!UICONTROL Habilitar conteúdo de fallback]**, conforme necessário. O conteúdo de fallback permite que o público receba um conteúdo padrão quando nenhuma regra de direcionamento for qualificada. Se você não selecionar essa opção, qualquer público-alvo que não se qualifique para uma regra de direcionamento definida acima não inserirá um caminho de fallback.

1. Salve as configurações da regra de direcionamento.

1. De volta à jornada, solte ações específicas para personalizar cada caminho. Por exemplo, você pode criar um email específico para residentes dos EUA, outro email para residentes da França e assim por diante.

   ![](assets/journey-targeting-paths.png)

1. Crie o conteúdo apropriado para cada grupo definido pelas suas configurações de regra de direcionamento. Você pode navegar facilmente entre os diferentes caminhos.

   ![](assets/journey-targeting-design.png)

   Neste exemplo, projete um caminho específico para residentes dos EUA, um caminho diferente para residentes franceses e outro caminho para residentes da Índia.

Quando a jornada estiver ativa, o caminho especificado para cada segmento será processado para que os residentes dos EUA insiram um caminho específico, os residentes da França insiram um caminho diferente e assim por diante.

### Casos de uso com direcionamento {#uc-targeting}

Os exemplos a seguir mostram como usar a atividade **[!UICONTROL Otimizar]** com o método **[!UICONTROL Direcionamento]** para personalizar caminhos para diferentes subpúblicos.

**Canais específicos do segmento**

Os membros do programa de fidelidade com o status Gold podem receber ofertas personalizadas por email, enquanto todos os outros membros são direcionados a lembretes de SMS.

* Use a receita por perfil ou taxa de conversão como a métrica de otimização.

![](assets/journey-optimize-targeting-uc.png)

**Direcionamento baseado em comportamento**

Os clientes que abriram um email, mas não clicaram, podem receber uma notificação por push, enquanto aqueles que não abriram recebem um SMS.

* Use a taxa de click-through ou as conversões downstream como a métrica de otimização.

**Direcionamento do histórico de compras**

Os clientes que compraram recentemente podem entrar em um caminho curto de &quot;Obrigado + Venda cruzada&quot;, enquanto aqueles sem histórico de compra entram em uma jornada de criação mais longa.

* Use a taxa de repetição de compra ou a taxa de envolvimento como a métrica de otimização.

## Adicionar uma condição {#conditions}

Você pode adicionar uma condição para definir como as pessoas avançam pela jornada criando vários caminhos com base em critérios específicos. Você também pode configurar um caminho alternativo para lidar com tempos limite ou erros, garantindo uma experiência contínua.

![](assets/journey-condition.png)

Saiba como definir uma condição em [esta seção](conditions.md).

Os seguintes tipos de condições estão disponíveis:

* [Condição do Source de dados](condition-activity.md#data_source_condition)
* [Condição de tempo](condition-activity.md#time_condition)
* [Divisão de porcentagem](condition-activity.md#percentage_split)
* [Condição de data](condition-activity.md#date_condition)
* [Limite de perfil](condition-activity.md#profile_cap)
