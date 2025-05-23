---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Split
description: Saiba como usar a atividade de Split em uma campanha orquestrada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 84%

---

# Divisão {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Atividade Divisão"
>abstract="A atividade **Divisão** permite segmentar as populações recebidas em vários subconjuntos com base em diferentes critérios de seleção, como regras de filtragem ou tamanho da população."

A atividade de **Divisão** é uma atividade de **Direcionamento** que permite segmentar as populações recebidas em vários subconjuntos com base em diferentes critérios de seleção, como regras de filtragem ou tamanho da população.

## Configurar a atividade de divisão {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segmentos para atividade de divisão"
>abstract="Adicione quantos subconjuntos desejar para segmentar a população recebida.<br/></br>Quando a atividade **Divisão** é executada, a população é segmentada nos diferentes subconjuntos na ordem em que são adicionados à atividade. Antes de iniciar a campanha orquestrada, certifique-se de organizar os subconjuntos em uma ordem que atenda às suas necessidades usando os botões de seta."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Filtro da atividade de divisão"
>abstract="Para aplicar uma condição de filtragem ao subconjunto, clique em **[!UICONTROL Criar filtro]** e configure a regra de filtragem desejada usando o modelador de consultas. Por exemplo, inclua perfis da população recebida cujo endereço de email já exista no banco de dados."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="Limite da atividade de divisão"
>abstract="Para limitar o número de perfis selecionados pelo subconjunto, ative a opção **[!UICONTROL Habilitar limite]**, e especifique o número ou as porcentagens da população a serem incluídas."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="Classificação da atividade de divisão"
>abstract="Ao definir um limite de população para um subconjunto, é possível classificar os perfis selecionados com base em um atributo de perfil específico, em ordem crescente ou decrescente. Para fazer isso, ative a opção **Habilitar classificação**. Por exemplo, é possível restringir um subconjunto para incluir apenas os 50 perfis com o valor de compra mais alto."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="Divisão e geração de complemento"
>abstract="Após configurar todos os subconjuntos, é possível selecionar a população restante que não correspondeu a nenhum dos subconjuntos e incluí-la em uma transição de saída adicional. Para isso, ative a opção **Gerar complemento.**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="Gerar todos os subconjuntos na mesma tabela"
>abstract="Ative essa opção para agrupar todos os subconjuntos em uma única transição de saída."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="Ignorar transição vazia"
>abstract="Ative a opção **[!UICONTROL Ignorar transição vazia]** para desabilitar a transição de saída para este subconjunto se a população de entrada estiver vazia."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="Habilitar sobreposição de populações de saída"
>abstract=" A opção **[!UICONTROL Habilitar sobreposição de populações de saída]** permite gerenciar populações pertencentes a vários subconjuntos. Quando a caixa não está marcada, a atividade Divisão garante que um destinatário não possa estar presente em diversas transições de saída, mesmo que atenda aos critérios de vários subconjuntos. Eles estarão no público-alvo da primeira guia com critérios correspondentes. Quando a caixa for marcada, os destinatários poderão ser encontrados em vários subconjuntos se atenderem aos critérios de filtro. "

Siga estas etapas para configurar a atividade de **Divisão**:

1. Adicione uma atividade **Split** à sua campanha orquestrada.

1. O painel de configuração da atividade é aberto com um subconjunto padrão. Clique em **Adicionar segmento** para adicionar quantos subconjuntos desejar e segmentar a população recebida.

   ![](../assets/workflow-split.png)

   >[!IMPORTANT]
   >
   >Quando a Atividade de **divisão** é executada, a população é segmentada nos diferentes subconjuntos na ordem em que são adicionados à atividade. Por exemplo, se o primeiro subconjunto recuperar 70% da população inicial, o próximo subconjunto adicionado aplicará seus critérios de seleção somente aos 30% restantes e assim por diante.
   >
   >Antes de iniciar a campanha orquestrada, verifique se você solicitou os subconjuntos na ordem que atende às suas necessidades. Para fazer isso, use os botões de seta para alterar a posição de um subconjunto.

1. Após a adição dos subconjuntos, a atividade mostrará tantas transições de saída quanto houver subconjuntos. Recomendamos alterar o rótulo de cada subconjunto para identificá-los facilmente na tela de campanha orquestrada.

1. Configure como cada subconjunto deve filtrar a população recebida. Para fazer isso, siga estes passos:

   1. Abra o subconjunto para exibir suas propriedades.

   1. Para aplicar uma condição de filtragem ao subconjunto, clique em **[!UICONTROL Criar filtro]** e configure a regra de filtragem desejada usando o modelador de consultas. Por exemplo, inclua perfis da população recebida cujo endereço de email já exista no banco de dados.

   1. Para limitar o número de perfis selecionados pelo subconjunto, ative a opção **[!UICONTROL Habilitar limite]**, e especifique o número ou as porcentagens da população a serem incluídas.

   1. Para desabilitar uma transição se a população recebida estiver vazia, alterne a opção **[!UICONTROL Ignorar transição vazia]** para. Se nenhum perfil corresponder ao subconjunto, a campanha orquestrada não fará a transição para a próxima atividade.

      ![](../assets/workflow-split-subset.png)

1. Após configurar todos os subconjuntos, é possível selecionar a população restante que não correspondeu a nenhum dos subconjuntos e incluí-la em uma transição de saída adicional. Para isso, ative a opção **[!UICONTROL Gerar complemento.]**

   ![](../assets/workflow-split-complement.png)

   >[!NOTE]
   >
   >A opção **[!UICONTROL Generate all subsets in the same table]** permite agrupar todos os subconjuntos em uma única transição de saída.

1. A opção **[!UICONTROL Enable overlapping of output populations]** permite gerenciar populações pertencentes a vários subconjuntos:

   * Quando a caixa não está marcada, a atividade Divisão garante que um destinatário não possa estar presente em diversas transições de saída, mesmo que atenda aos critérios de vários subconjuntos. Eles estarão no target da primeira guia com critérios correspondentes.
   * Quando a caixa for marcada, os destinatários poderão ser encontrados em vários subconjuntos se atenderem aos critérios de filtro. A prática recomendada é usar critérios exclusivos.

A atividade agora está configurada. Na execução orquestrada da campanha, a população será segmentada em diferentes subconjuntos, na ordem em que foram adicionados à atividade.

## Exemplo{#split-example}

No exemplo a seguir, a atividade de **[!UICONTROL Divisão]** é usada para segmentar um público-alvo em subconjuntos distintos com base no canal de comunicação que queremos usar:

* **Subconjunto 1 “push”**: esse subconjunto inclui todos os perfis que instalaram nosso aplicativo móvel.
* **Subconjunto 2 “sms”**: usuários de celular: para a população restante que não se enquadrou no subconjunto 1, o subconjunto 2 aplica uma regra de filtragem para selecionar perfis com telefones celulares no banco de dados.
* **Transição de complemento**: essa transição captura todos os perfis restantes que não corresponderam ao subconjunto 1 nem ao subconjunto 2. Especificamente, inclui perfis que não instalaram o aplicativo móvel nem possuem um telefone celular, como usuários que não instalaram o aplicativo ou que não têm um número de celular registrado.

![](../assets/workflow-split-example.png)
