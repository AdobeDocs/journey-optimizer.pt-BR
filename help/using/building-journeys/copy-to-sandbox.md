---
title: Copiar uma jornada para outra sandox
description: Saiba como copiar uma jornada para outro sandox
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# Copiar uma jornada para outra sandbox {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copiar uma jornada para outra sandbox"
>abstract="O Journey Optimizer permite copiar uma jornada inteira de uma sandbox para outra. Por exemplo, você pode copiar uma jornada do ambiente de sandbox de preparo para a sandbox de produção. Além da própria Jornada, o Journey Optimizer também copia a maioria dos objetos dos quais a jornada depende."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Detalhes da sandbox"
>abstract="Selecione a sandbox de destino para a qual deseja copiar a jornada. Somente sandboxes na organização de IMS estão disponíveis."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Detalhes do objeto"
>abstract="Esta é a jornada que você vai copiar."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Objetos dependentes"
>abstract="Esta é a lista de objetos associados usados na jornada. Essa lista exibe o nome, o tipo de objeto e a Journey Optimizer ID interna."

O Journey Optimizer permite copiar uma jornada inteira de uma sandbox para outra. Por exemplo, você pode copiar uma jornada do ambiente de sandbox de Preparo para a sandbox de Produção. Além da própria jornada, o Journey Optimizer também copia a maioria dos objetos dos quais a jornada depende: segmentos, superfícies (ou seja, predefinições), esquemas, eventos e ações. Consulte a [limitações](../building-journeys/copy-to-sandbox.md#limitations)

>[!CAUTION]
>
>Não garantimos que todos os elementos vinculados sejam copiados para a sandbox de destino. Recomendamos que você faça uma verificação completa antes de publicar a jornada. Isso permitirá identificar qualquer objeto em potencial ausente.

Os objetos copiados na sandbox de destino são exclusivos e não há risco de substituir elementos existentes. Tanto a jornada quanto as mensagens dentro da jornada são trazidas para o modo de rascunho. Isso permite executar uma validação completa antes da publicação na sandbox de destino. O processo de cópia copia apenas os metadados sobre a jornada e os objetos nessa Jornada. Nenhum perfil ou conjunto de dados está sendo copiado como parte desse processo.

Para copiar uma jornada para outra sandbox, siga estas etapas:

1. Na seção do menu GERENCIAMENTO DE JORNADAS , clique em **[!UICONTROL Journeys]**. A lista de jornadas é exibida.

2. Procure a jornada que deseja copiar, clique no botão **Mais ações** ícone (os três pontos ao lado do nome da jornada) e clique em **Copiar para sandbox**.

   ![](assets/copy-sandbox1.png)

   O **Copiar para sandbox** será exibida.

   ![](assets/copy-sandbox2.png)

3. Selecione o **sandbox de destino** no campo suspenso . Somente sandboxes na organização de IMS estão disponíveis.

4. Revise o **Objetos dependentes** seção. Esta é a lista de objetos associados usados na jornada. Essa lista exibe o nome, o tipo de objeto e a Journey Optimizer ID interna.

5. Clique no botão **Copiar** , no canto superior direito, para começar a copiar a jornada para a sandbox de destino.

   ![](assets/copy-sandbox3.png)

   O processo de cópia começa e o progresso de cada objeto individual é exibido. O processo de cópia varia com base na complexidade da jornada e em quantos objetos precisam ser copiados. Se um erro for encontrado, uma mensagem será exibida para o objeto relacionado.

   ![](assets/copy-sandbox4.png)

6. Quando a cópia estiver concluída, clique em **Fechar**.

7. Acesse a sandbox de destino e faça uma verificação completa de todos os objetos copiados.

## Copiar processo e limitações {#limitations}

Não garantimos que todos os elementos vinculados sejam copiados para a sandbox de destino. Recomendamos que você faça uma verificação completa. Identifique qualquer objeto potencialmente ausente e crie-o manualmente antes de publicar a jornada.

Os seguintes objetos são copiados:

* Segmento

   Um segmento só pode ser copiado uma vez de uma sandbox para outra. Depois que um segmento é copiado, ele não é editável na sandbox de destino.

* Esquema

   Os esquemas usados nessa jornada são copiados.

* Mensagem

   As atividades de ação do canal usadas na jornada. Os campos usados para personalização na mensagem não são verificados quanto à integridade. Os blocos de conteúdo não são copiados.

* Jornada - detalhes da tela

   A representação da jornada na tela, incluindo os objetos na jornada, como condições, ações, eventos, segmentos de leitura, etc. A atividade Jump é excluída da cópia.

* Evento

   Os eventos e os detalhes do evento usados na jornada são copiados.

* Ação

   As ações e os detalhes de ação usados na jornada são copiados.

As superfícies (ou seja, as predefinições) não são copiadas. O sistema seleciona automaticamente a correspondência mais próxima possível na sandbox de destino, com base no tipo de mensagem e no nome da superfície. Se não houver superfícies encontradas na sandbox de destino, a cópia da superfície falhará. Isso significa que a cópia da mensagem também falhará porque uma mensagem requer que uma superfície esteja disponível para configuração. Nesse caso, pelo menos uma superfície precisa ser criada, para o canal correto da mensagem, para que a cópia funcione.

Para Esquemas, Mesclar Políticas e Segmentos, na segunda vez que esses objetos tentarem ser copiados, eles só serão referenciados. Eles serão tratados como objetos que já existem e serão copiados novamente. Isso significa que esses objetos só podem ser copiados uma vez.

Há um atraso de cinco minutos antes que o Adobe Journey Optimizer possa fazer referência aos Esquemas, às Políticas e aos Segmentos de Mesclagem sem ver um erro na tela. Aguarde cinco minutos e essas referências estarão disponíveis.
