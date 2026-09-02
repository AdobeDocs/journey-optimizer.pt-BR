---
solution: Journey Optimizer
product: journey optimizer
title: Nova interface da jornada
feature: Release Notes
topic: Content Management
description: Saiba mais sobre o novo modelo de jornada simplificado, a interface de tela de jornada reprojetada e os relatórios em tempo real introduzidos no Journey Optimizer jornada.
keywords: Tela de jornada, novo modelo de jornada, relatórios ao vivo, designer de jornada
role: User
level: Beginner, Intermediate
hide: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
TQID: https://experienceleague.adobe.com/-QKSnBRN9yPYEq5ay9wD-uf4lLduJqmtlFWDnLYt1gk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 1f2a71d3323b6a64b346a83aa58b23aed035eb29
workflow-type: tm+mt
source-wordcount: 727
ht-degree: 1%

---

# Damos as boas-vindas ao Designer de jornada aprimorado {#new-canvas}

[!DNL Journey Optimizer] agora oferece um **modelo de jornada simplificado** que visa melhorar a experiência do usuário e os processos internos. A partir da versão de abril, você poderá se beneficiar dos seguintes recursos:

* Uma **tela de jornada reprojetada** para uma experiência de interface do usuário modernizada
* Uma interface de usuário do **live reporting** diretamente disponível na tela de jornada

>[!NOTE]
>
>Esteja ciente de que a implantação desse recurso será progressiva. Talvez você não veja as alterações imediatamente.

Para saber mais sobre como criar jornadas na nova tela, consulte [usando o designer de jornadas](../building-journeys/using-the-journey-designer.md#canvas-capabilities).

## Atualizações no modelo de jornada {#updates-journey-model}

O novo modelo de jornada conterá o existente, o que significa que haverá jornadas usando **dois modelos diferentes**:

* O modelo herdado
* O novo modelo

Todas as jornadas no modelo herdado permanecerão nele. Você ainda poderá editá-los, testá-los ou publicá-los. Qualquer nova versão criada de uma jornada no modelo herdado também permanecerá nela. Não há **alterações funcionais** entre essas jornadas.

Como você vê na captura de tela abaixo, os nós são em forma de rodada, que é a interface antiga para jornadas no modelo herdado.

![Tela de jornada herdada mostrando nós de atividade em forma de rodada para AirportBeacon e Email, conectados em um fluxo horizontal simples](assets/new-canvas.png)

No entanto, quando você **criar uma nova jornada** ou **duplicar uma existente**, ela estará no novo modelo. As jornadas no modelo herdado ainda serão compatíveis até que a maioria dos clientes faça a transição para o novo.

Há uma limitação para o novo modelo de jornada; **não será possível copiar e colar atividades do modelo herdado para o novo e vice-versa**. Se desejar fazer isso, recomendamos que você duplique sua jornada herdada para alterná-la para o novo modelo e, em seguida, copie suas atividades.

Na captura de tela abaixo, é possível ver a interface do usuário reprojetada para a tela de jornada (disponível somente com o novo modelo):

![Tela de jornada reprojetada mostrando caixas de atividade quadradas (membros de fidelidade leem público, Condição) se ramificando em email de boas-vindas e atividades de mensagem de Slack](assets/new-canvas2.png)

**Qualquer novo recurso adicionado ao designer do jornada (incluindo relatórios ao vivo) só estará disponível para jornadas no novo modelo a partir de agora.**

## Aprimoramento do design da tela de jornada {#improved-canvas-design}

Com o novo modelo do jornada, estamos introduzindo uma nova e aprimorada **interface do usuário da tela do jornada**, que se encaixa perfeitamente nas soluções do [!DNL Adobe CX Enterprise] e no ecossistema de aplicativos, proporcionando uma experiência do usuário intuitiva e eficiente. Qualquer jornada no novo modelo estará nesse novo design.

![Demonstração animada do novo design da tela de jornada, mostrando uma jornada com Início, uma atividade de público-alvo de leitura dos membros de Fidelidade e nós de Término](assets/new-canvas3.gif)

As atividades agora serão representadas por caixas quadradas com os seguintes recursos:

* A primeira linha representa o tipo de atividade que geralmente será substituído por informações mais contextuais (em Ler públicos, ela conterá o nome do público selecionado) ou por um rótulo personalizado, se você definir um.
* A segunda linha sempre representa o tipo de atividade.

![Caixa Atividade mostrando o rótulo de atividade &quot;Membros de fidelidade&quot; na primeira linha e o tipo de atividade &quot;Ler público-alvo&quot; na segunda linha](assets/new-canvas4.png)

Esta nova interface melhora a legibilidade da tela de jornada ao fornecer **rótulos e tipos de atividades mais claros**.

Também permite que a equipe de produtos adicione mais informações à tela com menos cliques. Um exemplo de &quot;mais informações&quot; seria a inclusão de relatórios ao vivo na tela de jornada, onde é possível ver os perfis que entram e saem das atividades devido a erros.

![Caixa Atividade com métricas de relatórios ao vivo mostrando 56 perfis inseridos e 0 erros para a atividade de membros de Fidelidade](assets/new-canvas5.png)

## Relatórios ao vivo na tela de jornada {#live-reporting-canvas}

Além do layout aprimorado da tela de jornada, um novo recurso está sendo introduzido para permitir que os usuários visualizem métricas de relatórios em tempo real das **últimas 24 horas**, chamadas de relatórios em tempo real, diretamente na tela de jornada. Isso complementa o [relatório ao vivo do jornada](../reports/journey-live-report.md) existente.

Para cada atividade em cada jornada ativa usando o novo modelo, você tem acesso a:


* A contagem de perfis que entram nesta atividade.
* A contagem de perfis que saem desta atividade devido a um erro.

![A tela do Live jornada mostrando as contagens de erros e entradas para cada atividade, incluindo Perfis de teste, Condição e várias ações personalizadas do Slack em caminhos diferentes](assets/new-canvas6bis.png)

<!--
`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
