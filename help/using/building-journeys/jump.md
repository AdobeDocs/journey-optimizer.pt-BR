---
solution: Journey Optimizer
product: journey optimizer
title: Saltando de uma jornada para outra
description: Saltando de uma jornada para outra
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Passar de uma jornada a outra {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Atividade Jump"
>abstract="A atividade Jump permite encaminhar indivíduos de uma jornada para outra. Esse recurso permite simplificar o design de jornadas muito complexas e criar jornadas com base em padrões de jornada comuns e reutilizáveis."

O **[!UICONTROL Jump]** A atividade de ação permite enviar indivíduos de uma jornada para outra. Esse recurso permite:

* simplifique o design de jornadas muito complexas dividindo-as em várias
* criar jornadas com base em padrões de jornada comuns e reutilizáveis

Na jornada de origem, basta adicionar um **[!UICONTROL Jump]** e selecione uma jornada de destino. Quando o indivíduo entra no **[!UICONTROL Jump]** , um evento interno é enviado para o primeiro evento da jornada de destino. Se a variável **[!UICONTROL Jump]** Se a ação for bem sucedida, o indivíduo continuará a progredir na jornada. O comportamento é semelhante a outras ações.

Na jornada do target, o primeiro evento acionado internamente pelo **[!UICONTROL Jump]** A atividade fará com que o fluxo individual ocorra na jornada.

## Vida útil

Digamos que você adicionou um **[!UICONTROL Jump]** atividade de uma jornada A para uma jornada B. Jornada A é a **jornada de origem** e a viagem B, a **jornada do target**.
Estas são as diferentes etapas do processo de execução:

**Jornada A** é acionado de um evento externo:

1. A jornada A recebe um evento externo relacionado a um indivíduo.
1. O indivíduo alcança o **[!UICONTROL Jump]** etapa.
1. O indivíduo é encaminhado para a Jornada B e avança para as próximas etapas da Jornada A, após a **[!UICONTROL Jump]** etapa.

Na jornada B, o primeiro evento é acionado internamente, por meio da variável **[!UICONTROL Jump]** Atividade da jornada A:

1. A jornada B recebeu um evento interno da jornada A.
1. O indivíduo começa a fluir na Jornada B.

>[!NOTE]
>
>A jornada B também pode ser acionada por meio de um evento externo.

## Práticas recomendadas e limitações

### Criação

* O **[!UICONTROL Jump]** A atividade só está disponível em jornadas que usam um namespace.
* Você só pode ir para uma jornada que use o mesmo namespace da jornada de origem.
* Não é possível saltar para uma jornada que começa com uma **Qualificação do segmento** evento ou **Ler segmento**.
* Não é possível ter um **[!UICONTROL Jump]** e uma **Qualificação do segmento** evento ou **Ler segmento** na mesma jornada.
* É possível incluir quantas **[!UICONTROL Jump]** atividades necessárias em uma jornada. Depois de um **[!UICONTROL Jump]**, é possível adicionar qualquer atividade necessária.
* Você pode ter quantos níveis de salto forem necessários. Por exemplo, a Jornada A vai para a jornada B, que vai para a jornada C e assim por diante.
* A jornada do target também pode incluir tantas **[!UICONTROL Jump]** conforme necessário.
* Os padrões de loop não são suportados. Não há como vincular duas ou mais jornadas que criariam um loop infinito. O **[!UICONTROL Jump]** a tela de configuração de atividade impede que você faça isso.

### Execução

* Quando a variável **[!UICONTROL Jump]** for executada, a versão mais recente da jornada de destino será acionada.
* Como de costume, um indivíduo único só pode estar presente uma vez em uma mesma jornada. Como resultado, se o indivíduo enviado da jornada de origem já estiver na jornada de destino, o indivíduo não entrará na jornada de destino. Nenhum erro será relatado na variável **[!UICONTROL Jump]** atividade porque esse é um comportamento normal.

## Configuração da atividade Jump

1. Crie seu **jornada de origem**.

   ![](assets/jump1.png)

1. Em qualquer etapa da jornada, adicione um **[!UICONTROL Jump]** da **[!UICONTROL ACTIONS]** categoria . Adicione um rótulo e uma descrição.

   ![](assets/jump2.png)

1. Clique dentro do **Jornada do target** campo.
A lista exibe todas as versões de jornada que estão em modo de rascunho, em tempo real ou de teste. Jornadas que usam um namespace diferente ou que começam com um **Qualificação do segmento** não estão disponíveis. As jornadas do Target que criariam um padrão de loop também são filtradas.

   ![](assets/jump3.png)

   >[!NOTE]
   >
   >Você pode clicar no botão **Abrir jornada do target** no lado direito, para abrir a jornada do target em uma nova guia.

1. Selecione a jornada de destino para a qual você deseja ir.
O **Primeiro evento** O campo é preenchido com o nome do primeiro evento da jornada de destino. Se sua jornada do target incluir vários eventos, a variável **[!UICONTROL Jump]** é permitido somente no primeiro evento.

   ![](assets/jump4.png)

1. O **Parâmetros de ação** exibe todos os campos do evento de destino. Da mesma forma que para outros tipos de ações, mapeie cada campo com campos do evento de origem ou fonte de dados. Essas informações serão passadas para a jornada de destino no tempo de execução.
1. Adicione as próximas atividades para concluir a jornada de origem.

   ![](assets/jump5.png)


   >[!NOTE]
   >
   >A identidade do indivíduo é mapeada automaticamente. Essas informações não estão visíveis na interface.

Seu **[!UICONTROL Jump]** está configurada. Assim que sua jornada estiver em tempo real ou no modo de teste, os indivíduos que atingem o **[!UICONTROL Jump]** será enviada da para a jornada do público-alvo.

Quando uma **[!UICONTROL Jump]** é configurada em uma jornada, uma **[!UICONTROL Jump]** o ícone de entrada é adicionado automaticamente no início da jornada de destino. Isso ajuda a identificar que a jornada pode ser acionada externamente, mas também internamente, a partir de um **[!UICONTROL Jump]** atividade .

![](assets/jump7.png)

## Solução de problemas

Quando a jornada é publicada ou no modo de teste, os erros acontecerão se:
* a jornada de destino não existe mais
* a jornada de destino é rascunho, fechado ou interrompido
* se o primeiro evento da jornada de destino tiver sido alterado e o mapeamento estiver quebrado

![](assets/jump6.png)
