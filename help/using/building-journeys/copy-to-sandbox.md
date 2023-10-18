---
solution: Journey Optimizer
product: journey optimizer
title: Copiar uma jornada para outra sandbox
description: Saiba como copiar uma jornada para outra sandbox
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: sandbox, jornada, cópia, ambiente
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 28a4f04ebcda27213d3bac763fb9bea8ea4a0146
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 20%

---

# Copiar uma jornada para outra sandbox {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copiar uma jornada para outra sandbox"
>abstract="O Journey Optimizer permite copiar uma jornada inteira de uma sandbox para outra. Por exemplo, você pode copiar uma jornada do ambiente de sandbox de preparo para a sandbox de produção. Além da própria jornada, o Journey Optimizer também copia a maioria dos objetos dos quais a jornada depende."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Detalhes da sandbox"
>abstract="Selecione a sandbox de destino para a qual deseja copiar a jornada. Somente as sandboxes da sua organização estão disponíveis."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Detalhes do objeto"
>abstract="Essa é a jornada que você vai copiar."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Objetos dependentes"
>abstract="Essa é a lista de objetos associados usados na jornada. Essa lista exibe o nome, o tipo de objeto e a ID interna do Journey Optimizer."

O Journey Optimizer permite copiar uma jornada inteira de uma sandbox para outra. Por exemplo, você pode copiar uma jornada do ambiente de sandbox do Stage para a sandbox de produção. Além da jornada em si, o Journey Optimizer também copia a maioria dos objetos dos quais a jornada depende: públicos-alvo, superfícies (ou seja, predefinições), esquemas, eventos e ações. Para obter mais detalhes sobre objetos copiados, consulte esta [seção](#limitations).

>[!CAUTION]
>
>Não garantimos que todos os elementos vinculados serão copiados para a sandbox de destino. É altamente recomendável executar uma verificação completa antes de publicar a jornada. Isso permitirá identificar qualquer objeto ausente em potencial.

Os objetos copiados na sandbox de destino são exclusivos e não há risco de substituir elementos existentes. A jornada jornada e qualquer mensagem dentro dela é trazida no modo de rascunho. Isso permite executar uma validação completa antes da publicação na sandbox de destino. O processo de cópia copia apenas os metadados sobre a jornada e os objetos nessa Jornada. Nenhum dado de perfil ou conjunto de dados está sendo copiado como parte desse processo.

Para copiar uma jornada para outra sandbox, siga estas etapas:

1. Na seção de menu GERENCIAMENTO de JORNADAS, clique em **[!UICONTROL Jornadas]**. A lista de jornadas é exibida.

2. Procure a jornada que deseja copiar, clique no link **Mais ações** (os três pontos ao lado do nome da jornada) e clique em **Copiar para sandbox**.

   ![](assets/copy-sandbox1.png)

   A variável **Copiar para sandbox** é exibida.

   ![](assets/copy-sandbox2.png)

3. Selecione o **Sandbox do Target** no campo suspenso. Somente as sandboxes da sua organização estão disponíveis.

4. Revise o **Objetos dependentes** seção. Essa é a lista de objetos associados usados na jornada. Essa lista exibe o nome, o tipo de objeto e a ID interna do Journey Optimizer.

5. Clique em **Copiar** no canto superior direito, para começar a copiar a jornada para a sandbox de destino.

   ![](assets/copy-sandbox3.png)

   O processo de cópia é iniciado e o progresso de cada objeto individual é exibido. O processo de cópia varia de acordo com a complexidade da jornada e com quantos objetos precisam ser copiados. Se um erro for encontrado, uma mensagem será exibida para o objeto relacionado.

   ![](assets/copy-sandbox4.png)

6. Quando a cópia estiver concluída, clique em **Fechar**.

7. Acesse sua sandbox de destino e execute uma verificação completa de todos os objetos copiados.

## Processo de cópia e limitações {#limitations}

Nem todos os elementos vinculados podem ser copiados para a sandbox de destino. A Adobe recomenda que você execute uma verificação completa. Identifique qualquer objeto ausente em potencial e crie-o manualmente antes de publicar a jornada.

Os seguintes objetos são copiados:

* Público-alvo

  Um público-alvo só pode ser copiado de uma sandbox para outra. Depois que um público-alvo é copiado, ele não pode ser editado na sandbox de destino.

* Esquema

  Os esquemas usados nesta jornada são copiados.

* Mensagem

  As atividades de ação do canal usadas na jornada. Os campos usados para personalização na mensagem não são verificados quanto à integridade. Os blocos de conteúdo não são copiados.

* Jornada - detalhes da tela

  A representação da jornada na tela, incluindo os objetos na jornada, como condições, ações, eventos, públicos-alvo de leitura etc. A atividade de salto é excluída da cópia.

* Evento

  Os eventos e os detalhes do evento usados na jornada são copiados.

* Ação

  As ações e os detalhes de ação usados na jornada são copiados.

As superfícies (ou seja, predefinições) não são copiadas. O sistema seleciona automaticamente a correspondência mais próxima possível na sandbox de destino, com base no tipo de mensagem e no nome da superfície. Se nenhuma superfície for encontrada na sandbox de destino, a cópia de superfície falhará. Isso significa que a cópia da mensagem também falhará, pois uma mensagem requer que uma superfície esteja disponível para configuração. Nesse caso, pelo menos uma superfície precisa ser criada para que o canal direito da mensagem funcione.

Para Esquemas, Políticas de mesclagem e Públicos-alvo, na segunda vez que esses objetos tentarem ser copiados, eles só serão referenciados. Eles serão tratados como objetos que já existem e serão copiados novamente. Isso significa que esses objetos só podem ser copiados uma vez.

Há um atraso de cinco minutos antes de a Adobe Journey Optimizer poder fazer referência a esquemas, políticas de mesclagem e públicos-alvo sem ver um erro na tela. Aguarde cinco minutos e essas referências estarão disponíveis.
