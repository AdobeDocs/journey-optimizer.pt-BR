---
solution: Journey Optimizer
product: journey optimizer
title: Experimentação de caminho
description: Saiba como usar a experimentação de caminho no jornada
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: experimentação, experimento, jornada, caminho, otimização, teste A/B, bandit multiarmado, dimensionar o vencedor
exl-id: 7241ade3-577c-4bb3-b0c3-017133871ca5
feature_v2: []
subfeature_v2: []
source-git-commit: a37b536bb4210a615995f5c5c8ec710b516de934
workflow-type: tm+mt
source-wordcount: 1308
ht-degree: 6%

---

# Usar experimentação de caminho {#experimentation}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como configurar a experimentação de caminho com a atividade Otimizar para testar diferentes caminhos de jornada usando experimentos A/B ou de bandit com vários braços, identificar o tratamento com melhor desempenho por métrica de sucesso e dimensionar o vencedor.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_path_experiment_success_metric"
>title="Métricas de sucesso"
>abstract="As métricas de sucesso são usadas para controlar e avaliar o tratamento com melhor desempenho em um experimento."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/success-metrics" text="Configurar e rastrear as métricas da jornada"

A experimentação permite testar caminhos diferentes com base em uma divisão aleatória para determinar qual tem o melhor desempenho com base em métricas de sucesso predefinidas.

Para configurar a experimentação de caminho em uma jornada, siga as etapas abaixo.

Digamos que você deseje comparar três caminhos:

* um caminho com um email;
* um segundo caminho com um nó **[!UICONTROL Wait]** de dois dias e um email;
* um terceiro caminho com um email e, em seguida, uma mensagem SMS.

1. Na seção **[!UICONTROL Orquestração]**, arraste e solte a atividade **[!UICONTROL Otimizar]** na tela de jornada.

1. Adicione um rótulo opcional, que pode ser útil para identificar a atividade em relatórios e logs do modo de teste.

1. Selecione **[!UICONTROL Experimento]** na lista suspensa **[!UICONTROL Método]**.

   ![Painel de configuração de experimento de caminho](assets/journey-optimize-experiment.png){width=65%}

1. Clique em **[!UICONTROL Criar experimento]**.

1. Selecione a **[!UICONTROL Métrica de sucesso]** que você deseja definir para o seu experimento. Saiba mais sobre as métricas disponíveis e como configurar a lista em [esta seção](success-metrics.md).

   ![Seleção de métricas primárias e adicionais para o experimento](assets/journey-optimize-experiment-metrics.png){width=80%}

1. Selecione o **[!UICONTROL Tipo de experimento]** para o seu experimento de caminho:

   * **[!UICONTROL Experimento A/B]** — Defina a divisão de tráfego entre tratamentos no início do teste. O desempenho é avaliado com base na métrica primária escolhida; os relatórios mostram o aumento observado entre os tratamentos.

   * **[!UICONTROL Bandit multi-armed]** — o tráfego dividido entre tratamentos é manipulado automaticamente. A cada 7 dias, o desempenho na métrica primária é revisado e os pesos são ajustados de acordo. Os relatórios continuam a mostrar aumento, assim como para testes A/B.

   ![Lista suspensa de tipos de experimento no experimento de caminho](assets/journey-path-experiment-type.png){width=80%}

   ➡️ [Saiba mais sobre a diferença entre experimentos A/B e Multi-armed bandit](../content-management/mab-vs-ab.md)

1. Você pode optar por adicionar um grupo de **[!UICONTROL Contenção]** à sua entrega. Este grupo não irá inserir nenhum caminho a partir deste experimento.

   >[!NOTE]
   >
   >A ativação da barra de alternância ocupará automaticamente 10% da sua população. Você pode ajustar essa porcentagem, se necessário.

1. Você pode alocar uma porcentagem precisa para cada **[!UICONTROL Tratamento]** ou simplesmente alternar na barra de alternância **[!UICONTROL Distribuir uniformemente]**.

   ![Controle deslizante de alocação de tratamento com distribuição de porcentagem](assets/journey-optimize-experiment-treatments.png){width=80%}

1. Ative o experimento de dimensionamento automático para implantar automaticamente a variação vencedora do seu experimento. [Saiba mais sobre como dimensionar o vencedor](#scale-winner)

1. Clique em **[!UICONTROL Criar]**.

1. Defina os elementos desejados para cada ramificação resultante do experimento, por exemplo:

   * Arraste e solte uma atividade [Email](../email/create-email.md) na primeira ramificação (**Tratamento A**).

   * Arraste e solte uma atividade [Aguardar](wait-activity.md) de dois dias na primeira ramificação, seguida por uma atividade [Email](../email/create-email.md) (**Tratamento B**).

   * Arraste e solte uma atividade [Email](../email/create-email.md) na terceira ramificação, seguida por uma atividade [SMS](../mobile/create-mobile-message.md) (**Tratamento C**).

   ![Exemplo de experimento de caminho com três caminhos de tratamento](assets/journey-optimize-experiment-ex.png){width=100%}

1. Opcionalmente, use o **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]** para definir uma ação de fallback. [Saiba mais](using-the-journey-designer.md#paths)

1. [Publique](publish-journey.md) sua jornada.

Quando a jornada estiver ativa, os usuários serão atribuídos aleatoriamente para percorrer caminhos diferentes. [!DNL Journey Optimizer] rastreia qual caminho tem melhor desempenho e fornece insights acionáveis.

Siga o sucesso da sua jornada com o relatório Experimento de caminho de Jornada. [Saiba mais](../reports/journey-global-report-cja-experimentation.md)

## Atribuição de caminho na reentrada da jornada {#path-assignment}

A atribuição de caminho é persistente para um perfil em várias entradas na mesma versão do jornada. Por exemplo, se um perfil entrar em uma jornada no dia 1 e for atribuído ao caminho A e entrar novamente na jornada no dia 2, ele será atribuído novamente ao caminho A. Isso garante uma experiência consistente para o usuário e é necessário para relatórios e análises estatisticamente válidos.

No entanto, as atribuições só são persistentes em uma determinada versão do jornada. Depois de publicar uma nova versão do jornada, a aleatoriedade é alterada e um perfil pode acabar sendo atribuído a um caminho diferente.

Se você tiver várias atividades de experimentação de caminho em uma jornada, cada atividade aplicará uma atribuição aleatória independente.

## Casos de uso de experimentos {#uc-experiment}

Os exemplos a seguir mostram como usar a atividade **[!UICONTROL Otimizar]** com o método **[!UICONTROL Experimento]** para determinar qual caminho funciona melhor em geral.

+++Eficácia do canal

Teste se o envio da primeira mensagem por email ou por SMS gera conversões mais altas.

➡️ Use a taxa de conversão como métrica de sucesso (por exemplo: compras, inscrições).

![Experimento de eficácia de canal comparando email com SMS](assets/journey-optimize-experiment-uc-channel.png)

+++

+++Frequência da mensagem

Execute um experimento para verificar se o envio de um email contra três emails em uma semana resulta em mais compras.

➡️ Use compras ou a taxa de cancelamento de inscrição como métrica de sucesso.

![Experimento de frequência de mensagem testando um email em comparação a três emails](assets/journey-optimize-experiment-uc-frequency.png)

+++

+++Tempo de espera entre as comunicações

Compare uma espera de 24 horas com uma de 72 horas antes de um acompanhamento para determinar qual tempo maximiza o engajamento.

➡️ Use a taxa de click-through ou a receita como métrica de sucesso.

![Experimento de tempo de espera comparando atrasos de 24 horas com atrasos de 72 horas](assets/journey-optimize-experiment-uc-wait.png)

+++

## Dimensionar o vencedor {#scale-winner}

>[!AVAILABILITY]
>
>Para experimentos de caminho, o recurso Dimensionar o vencedor está disponível apenas em jornadas unitárias (acionadas por eventos e qualificações de público-alvo).
>
>Não está disponível para jornadas Ler público-alvo.

A opção “Dimensionar o vencedor” permite implantar de forma automática ou manual a variação vencedora de um experimento em todo o seu público-alvo. Esse recurso garante que, uma vez determinado o vencedor, você possa ampliar seu alcance e eficácia sem monitorar constantemente o experimento.

Você pode escolher entre dois modos:

* **Dimensionamento automático**: defina as configurações de dimensionamento automático ao criar seu experimento escolhendo o tempo e as condições para dimensionar o tratamento vencedor ou uma opção de fallback se nenhum vencedor surgir.

* **Escala Manual**: analise manualmente os resultados do experimento e inicie a implantação do tratamento vencedor, mantendo o controle total sobre o tempo e as decisões.

### Dimensionamento automático {#autoscaling}

O dimensionamento automático permite definir regras predefinidas para quando implantar o tratamento vencedor ou um fallback, com base nos resultados do experimento.

Observe que após o dimensionamento automático, o dimensionamento manual não estará mais disponível.

Para ativar a escala automática em seus experimentos:

1. Defina sua jornada e configure seu experimento conforme necessário. [Saiba mais](#experimentation)

1. Ative a opção de dimensionamento automático ao configurar seu experimento.

   ![Opção de dimensionamento automático no experimento de caminho](assets/journey-optimize-autoscale.png)

1. Selecione quando o vencedor deve ser dimensionado:

   * Assim que o vencedor for encontrado.
   * Após o experimento ficar ativo pelo tempo selecionado.

   A hora de dimensionamento automático deve ser agendada antes da data de término do experimento. Se for definido para um período posterior à data de término, um aviso de validação será exibido e a jornada não será publicada.

   ![Seleção de tempo de dimensionamento automático no experimento de caminho](assets/journey-optimize-autoscale-time.png)

1. Escolha o comportamento de fallback se nenhum vencedor for encontrado por tempo de escala:

   * Continue o experimento até que ele termine como programado.
   * Dimensione o tratamento alternativo após um tempo especificado.

Depois que todos os parâmetros forem atendidos, o tratamento vencedor ou alternativo será enviado para o público-alvo.

### Dimensionamento manual {#manual-scaling}

O dimensionamento manual oferece a capacidade de analisar os resultados do experimento e decidir quando implantar o tratamento vencedor de acordo com seu próprio cronograma.

Observe que, se você dimensionar manualmente o vencedor antes do tempo de dimensionamento automático programado, a dimensionamento automático será cancelada.

Para dimensionar manualmente o vencedor de seus experimentos:

1. Defina sua jornada e configure seu experimento conforme necessário. [Saiba mais](#experimentation)

1. Deixe o experimento ser executado até que um vencedor seja identificado ou até que a significância estatística seja alcançada.

1. Abra a jornada e selecione a atividade **[!UICONTROL Otimizar]** que contém o experimento de caminho.

   Revise os resultados na exibição **[!UICONTROL Experimento de caminho]** para identificar o tratamento com melhor desempenho.

   ![Vencedor da escala manual no experimento de caminho](assets/journey-optimize-manual-scale-winner.png)

1. Clique em **[!UICONTROL Dimensionar tratamento]** para encaminhar o tratamento vencedor ao restante do público-alvo.

   <!--![](assets/journey-optimize-scale-treatment.png)-->

1. Selecione o tratamento que deseja dimensionar no menu suspenso e clique em **[!UICONTROL Escala]**.

   ![Seleção de tratamento de escala no experimento de caminho](assets/journey-optimize-scale-treatment.png){width=80%}

Observe que o dimensionamento do tratamento pode levar até uma hora. Você receberá uma notificação quando o processo de dimensionamento manual for concluído.
