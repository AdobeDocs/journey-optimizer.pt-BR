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
source-git-commit: 817f9c16ae48b1127e5092add6fbcefa8dd3ba9f
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 10%

---

# Mudar de uma jornada para outra {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Atividade saltar"
>abstract="A ação “Saltar” permite enviar pessoas de uma jornada para outra. Esse recurso permite simplificar o design de jornadas muito complexas e criar jornadas com base em padrões de jornadas comuns e reutilizáveis."

A atividade de ação **[!UICONTROL Pular]** permite enviar indivíduos de uma jornada para outra. Esse recurso permite:

* simplificar o design de jornadas muito complexas dividindo-as em várias jornadas
* criar jornadas com base em padrões de jornada comuns e reutilizáveis

Na jornada de origem, basta adicionar uma atividade **[!UICONTROL Jump]** e selecionar uma jornada de destino. Quando o indivíduo entra na etapa **[!UICONTROL Jump]**, um evento interno é enviado para o primeiro evento da jornada de destino. Se a ação **[!UICONTROL Jump]** for bem-sucedida, o indivíduo continuará progredindo na jornada. O comportamento é semelhante a outras ações.

Na jornada de destino, o primeiro evento acionado internamente pela atividade **[!UICONTROL Jump]** fará com que o fluxo individual seja feito na jornada.

## Ciclo de vida {#jump-lifecycle}

Digamos que você tenha adicionado uma atividade de **[!UICONTROL salto]** em uma jornada A para uma jornada B. A Jornada A é a **jornada de origem** e a jornada B, a **jornada de destino**.
Estas são as diferentes etapas do processo de execução:

A **Jornada A** é disparada de um evento externo:

1. A jornada A recebe um evento externo relacionado a um indivíduo.
1. O indivíduo atinge a etapa **[!UICONTROL Salto]**.
1. O indivíduo é encaminhado para a Jornada B e avança para as próximas etapas da Jornada A, após a etapa **[!UICONTROL Jump]**.

Na jornada B, o primeiro evento é acionado internamente, por meio da atividade **[!UICONTROL Jump]** da jornada A:

1. A jornada B recebeu um evento interno da Jornada A.
1. O indivíduo começa a fluir na Jornada B.

>[!NOTE]
>
>A jornada B também pode ser acionada por meio de um evento externo.

## Práticas recomendadas e limitações {#jump-limitations}

### Criação {#jump-limitations-authoring}

* A atividade **[!UICONTROL Jump]** só está disponível em jornadas que usam um namespace.
* Você só pode pular para uma jornada que use o mesmo namespace que a jornada de origem.
* Você não pode ir para uma jornada que começa com um evento de **Qualificação de público-alvo** ou **Ler público-alvo**.
* Você não pode ter uma atividade de **[!UICONTROL Salto]** e um evento de **Qualificação de público** ou **Ler público** na mesma jornada.
* Você pode incluir quantas atividades de **[!UICONTROL Salto]** forem necessárias em uma jornada. Após um **[!UICONTROL Jump]**, você pode adicionar qualquer atividade necessária.
* Você pode ter quantos níveis de salto forem necessários. Por exemplo, a Jornada A salta para a jornada B, que salta para a jornada C e assim por diante.
* A jornada de destino também pode incluir quantas atividades **[!UICONTROL Jump]** forem necessárias.
* Não há suporte para padrões de loop. Não há como vincular duas ou mais jornadas, o que criaria um loop infinito. A tela de configuração de atividade **[!UICONTROL Jump]** impede que você faça isso.

### Execução {#jump-limitations-exec}

* Quando a atividade **[!UICONTROL Jump]** é executada, a versão mais recente da jornada de destino é acionada.
* Como de costume, um indivíduo único só pode estar presente uma vez na mesma jornada. Como resultado, se o indivíduo enviado da jornada de origem já estiver na jornada de destino, ele não entrará na jornada de destino. Nenhum erro será relatado na atividade de **[!UICONTROL Salto]** porque esse é um comportamento normal.

## Configuração da atividade Jump {#jump-configure}

1. Projete sua **jornada de origem**.

   ![](assets/jump1.png)

1. Em qualquer etapa da jornada, adicione uma atividade de **[!UICONTROL Salto]**, da categoria **[!UICONTROL AÇÕES]**. Adicione um rótulo e uma descrição.

   ![](assets/jump2.png)

1. Clique dentro do campo **jornada de destino**.
A lista exibe todas as versões do jornada que são modo de rascunho, ativo ou de teste. As jornadas que usam um namespace diferente ou que começam com um evento **Qualificação de público-alvo** não estão disponíveis. As jornadas do Target que criariam um padrão de loop também são filtradas.

   ![](assets/jump3.png)

   >[!NOTE]
   >
   >Você pode clicar no ícone **Abrir jornada de destino**, no lado direito, para abrir a jornada de destino em uma nova guia.

1. Selecione a jornada de destino para a qual deseja ir.
O campo **Primeiro evento** é preenchido previamente com o nome do primeiro evento da jornada de destino. Se a sua jornada de destino incluir vários eventos, o **[!UICONTROL Jump]** só será permitido no primeiro evento.

   ![](assets/jump4.png)

1. A seção **Parâmetros de ação** exibe todos os campos do evento de destino. Da mesma forma que para outros tipos de ações, mapeie cada campo com campos do evento de origem ou da fonte de dados. Essas informações serão passadas para a jornada de destino no tempo de execução.
1. Adicione as próximas atividades para concluir a jornada de origem.

   ![](assets/jump5.png)


   >[!NOTE]
   >
   >A identidade do indivíduo é mapeada automaticamente. Essas informações não estão visíveis na interface.

Sua atividade **[!UICONTROL Jump]** está configurada. Assim que a jornada estiver ativa ou em modo de teste, os indivíduos que atingirem a etapa **[!UICONTROL Jump]** serão encaminhados para a jornada de destino.

Quando uma atividade de **[!UICONTROL Jump]** é configurada em uma jornada, um ícone de entrada **[!UICONTROL Jump]** é adicionado automaticamente no início da jornada de destino. Isso ajuda a identificar que a jornada pode ser acionada externamente, mas também internamente, a partir de uma atividade de **[!UICONTROL Salto]**.

![](assets/jump7.png)

## Solução de problemas {#jump-troubleshoot}

Ocorrerão erros se:
* a jornada de destino não existe mais
* a jornada de destino é rascunho, fechada ou interrompida
* se o primeiro evento da jornada de destino tiver sido alterado e o mapeamento for interrompido

![](assets/jump6.png)
