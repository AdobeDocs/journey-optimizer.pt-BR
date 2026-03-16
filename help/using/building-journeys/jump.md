---
solution: Journey Optimizer
product: journey optimizer
title: Mudar de uma jornada para outra
description: Mudar de uma jornada para outra
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: jump, activity, jornada, split, dividir
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
version: Journey Orchestration
source-git-commit: 302db58525a7b2648bb9c44bc9b42da787ca9c43
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 7%

---

# Mudar de uma jornada para outra {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Atividade Salto"
>abstract="A ação “Saltar” permite enviar pessoas de uma jornada para outra. Esse recurso permite simplificar o design de jornadas muito complexas e criar jornadas com base em padrões de jornadas comuns e reutilizáveis."

A atividade de ação **[!UICONTROL Pular]** permite enviar indivíduos de uma jornada para outra. Esse recurso permite:

* simplificar o design de jornadas muito complexas dividindo-as em várias jornadas
* criar jornadas com base em padrões de jornada comuns e reutilizáveis

Na jornada de origem, adicione uma atividade **[!UICONTROL Jump]** e selecione uma jornada de destino. Quando o indivíduo entra na etapa **[!UICONTROL Jump]**, um evento interno é enviado para o primeiro evento da jornada de destino. Se a ação **[!UICONTROL Jump]** for bem-sucedida, o indivíduo continuará progredindo na jornada. O comportamento é semelhante a outras ações.

Na jornada de destino, o primeiro evento acionado internamente pela atividade **[!UICONTROL Jump]** gera o fluxo individual na jornada.

## Ciclo de vida {#jump-lifecycle}

Suponha que você tenha adicionado uma atividade de **[!UICONTROL salto]** na jornada A para a jornada B. A Jornada A é a **jornada de origem** e a jornada B é a **jornada de destino**.

Estas são as diferentes etapas do processo de execução:

A **Jornada A** é disparada de um evento externo:

1. A jornada A recebe um evento externo relacionado a um indivíduo.
1. O indivíduo atinge a etapa **[!UICONTROL Salto]**.
1. O indivíduo é encaminhado para a jornada B e avança para as próximas etapas da jornada A, após a etapa **[!UICONTROL Jump]**.

Na jornada B, o primeiro evento é acionado internamente por meio da atividade **[!UICONTROL Jump]** da jornada A:

1. A jornada B recebe um evento interno da jornada A.
1. O indivíduo começa a fluir na jornada B.

>[!NOTE]
>
>A jornada B também pode ser acionada por meio de um evento externo.

## Práticas recomendadas e limitações {#jump-limitations}

Use essas diretrizes para manter o comportamento da atividade de salto previsível e seguro.

### Criação {#jump-limitations-authoring}

* A atividade **[!UICONTROL Jump]** só está disponível em jornadas que usam um namespace.
* Você só pode pular para uma jornada que use o mesmo namespace que a jornada de origem.
* Você não pode ir para uma jornada que começa com um evento de **Qualificação de público-alvo** ou **Ler público-alvo**.
* Você não pode ter uma atividade de **[!UICONTROL Salto]** e um evento de **Qualificação de público** ou **Ler público** na mesma jornada.
* Você pode incluir quantas atividades de **[!UICONTROL Salto]** forem necessárias em uma jornada. Após um **[!UICONTROL Jump]**, você pode adicionar qualquer atividade necessária.
* Você pode ter quantos níveis de salto forem necessários. Por exemplo, a jornada A salta para a jornada B, que salta para a jornada C e assim por diante.
* A jornada de destino também pode incluir quantas atividades **[!UICONTROL Jump]** forem necessárias.
* Não há suporte para padrões de loop. Não há como vincular duas ou mais jornadas, o que criaria um loop infinito. A tela de configuração de atividade **[!UICONTROL Jump]** impede que você faça isso.

### Execução {#jump-limitations-exec}

* Quando a atividade **[!UICONTROL Jump]** é executada, a versão mais recente da jornada de destino é acionada.
* Um indivíduo único só pode estar presente uma vez na mesma jornada. Como resultado, se o indivíduo enviado da jornada de origem já estiver na jornada de destino, ele não entrará na jornada de destino. Nenhum erro será relatado na atividade de **[!UICONTROL Salto]** porque esse é um comportamento normal.

## Estratégia de design: sub-jornadas de tamanho reduzido {#jump-strategy}

Jornadas complexas do cliente podem se tornar rapidamente difíceis de criar e manter, especialmente quando canais ou pontos de contato adicionais são introduzidos. Mesmo uma jornada com alguns marcos pode expor 20 ou mais caminhos únicos que um cliente pode tomar e essa complexidade cresce exponencialmente a cada adição.

Uma abordagem prática para gerenciar isso é dividir grandes jornadas em sub-jornadas menores e focadas, uma por fase de negócios ou marco, e conectá-las usando a atividade **[!UICONTROL Jump]**. Isso mantém cada jornada legível, testável e com manutenção independente.

**Etapa 1 — Visualizar a jornada de ponta a ponta**

Mapear a jornada completa do cliente e identificar suas fases de alto nível. Por exemplo, uma jornada de integração de fidelidade pode incluir três fases distintas: baixar o aplicativo móvel, fazer uma primeira transação e fazer uma segunda transação.

**Etapa 2 — Anotar fases e definir subjornadas**

Marcar o limite de cada fase e definir seu objetivo comercial. Cada fase se torna uma subjornada candidata com uma condição de entrada e meta claras.

**Etapa 3 — Criar e conectar subjornadas**

Crie cada fase como uma jornada separada no Journey Optimizer e use as atividades **[!UICONTROL Jump]** para transmitir perfis de uma subjornada para a próxima. O resultado é um conjunto de jornadas mais simples e reutilizáveis que se combinam para produzir a experiência completa, com menos risco de apresentar erros.

>[!TIP]
>
>Para obter uma apresentação detalhada dessa abordagem, consulte [Práticas recomendadas para jornadas avançadas no Journey Optimizer](https://experienceleague.adobe.com/pt-br/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

## Configuração da atividade Jump {#jump-configure}

1. Projete sua **jornada de origem**.

   ![Atividade de salto na paleta do jornada para transição entre jornadas](assets/jump1.png)

1. Em qualquer etapa da jornada, adicione uma atividade de **[!UICONTROL Salto]**, da categoria **[!UICONTROL AÇÕES]**. Adicione um rótulo e uma descrição.

   ![Lista suspensa de seleção de jornada de destino na configuração da atividade de salto](assets/jump2.png)

1. Clique dentro do campo **jornada de destino**.
A lista exibe todas as versões do jornada que são modo de rascunho, ativo ou de teste. As jornadas que usam um namespace diferente ou que começam com um evento **Qualificação de público-alvo** não estão disponíveis. As jornadas do Target que criariam um padrão de loop também são filtradas.

   ![Atividade de salto mostrando a jornada de destino e os parâmetros de ação](assets/jump3.png)

   >[!NOTE]
   >
   >Você pode clicar no ícone **Abrir jornada de destino**, no lado direito, para abrir a jornada de destino em uma nova guia.

1. Selecione a jornada de destino para a qual deseja ir.
O campo **Primeiro evento** é preenchido previamente com o nome do primeiro evento da jornada de destino. Se a sua jornada de destino incluir vários eventos, o **[!UICONTROL Jump]** só será permitido no primeiro evento.

   ![Configuração de mapeamento de parâmetros para a atividade de salto com o editor de expressão](assets/jump4.png)

1. A seção **Parâmetros de ação** exibe todos os campos do evento de destino. Mapeie cada campo com campos do evento de origem ou da fonte de dados, como com outros tipos de ações. Essas informações serão passadas para a jornada de destino no tempo de execução.
1. Adicione as próximas atividades para concluir a jornada de origem.

   ![Interface de modo de teste para testar atividade de salto entre jornadas](assets/jump5.png)


   >[!NOTE]
   >
   >A identidade do indivíduo é mapeada automaticamente. Essas informações não estão visíveis na interface.

Sua atividade **[!UICONTROL Jump]** está configurada. Assim que a jornada estiver ativa ou em modo de teste, os indivíduos que atingirem a etapa **[!UICONTROL Jump]** serão encaminhados para a jornada de destino.

Quando uma atividade de **[!UICONTROL Jump]** é configurada em uma jornada, um ícone de entrada **[!UICONTROL Jump]** é adicionado automaticamente no início da jornada de destino. Isso ajuda a identificar que a jornada pode ser acionada externamente, mas também internamente, a partir de uma atividade de **[!UICONTROL Salto]**.

![Fluxo de Jornada mostrando salto da jornada de origem para a jornada de destino](assets/jump7.png)

## Solução de problemas {#jump-troubleshoot}

Ocorrem erros se:

* A jornada de destino não existe mais
* A jornada de destino está em rascunho, fechada ou parada
* O primeiro evento da jornada de destino foi alterado e o mapeamento foi interrompido

![Análise de Jornada mostrando as métricas de execução da atividade de salto](assets/jump6.png)
