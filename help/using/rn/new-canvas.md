---
solution: Journey Optimizer
product: journey optimizer
title: Nova interface da jornada
feature: Release Notes
topic: Content Management
description: Nova interface da jornada
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: 6b9044117dcdd7554dea0c5f791a6dcfb0218010
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 2%

---

# Damos as boas-vindas ao Designer de jornada aprimorado {#new-canvas}

O Journey Optimizer agora oferece uma **modelo de jornada simplificado** que visa melhorar a experiência do usuário e os processos internos. A partir da versão de abril, você poderá se beneficiar dos seguintes recursos:

* A **tela de jornada recriada** criado para uma experiência de interface modernizada
* A **relatórios ao vivo** Interface do usuário diretamente disponível na tela de jornada

>[!NOTE]
>
>Esteja ciente de que a implantação desse recurso será progressiva. Talvez você não veja as alterações imediatamente.

## Atualizações no modelo de jornada

O novo modelo de jornada conterá o existente, o que significa que haverá jornadas usando **dois modelos diferentes**:

* O modelo herdado
* O novo modelo

Todas as jornadas no modelo herdado permanecerão nele. Você ainda poderá editá-los, testá-los ou publicá-los. Qualquer nova versão criada de uma jornada no modelo herdado também permanecerá nela. Há **nenhuma alteração funcional** ao redor dessas jornadas.

Como você vê na captura de tela abaixo, os nós são em forma de rodada, que é a interface antiga para jornadas no modelo herdado.

![](assets/new-canvas.png)

No entanto, quando você **criar uma nova jornada** ou **duplicar um existente**, estará no novo modelo. As jornadas no modelo herdado ainda serão compatíveis até que a maioria dos clientes faça a transição para o novo.

Há uma limitação para o novo modelo de jornada; ela **não será possível copiar e colar atividades do modelo herdado para o novo e vice-versa**. Se desejar fazer isso, recomendamos que você duplique sua jornada herdada para alterná-la para o novo modelo e, em seguida, copie suas atividades.

Na captura de tela abaixo, é possível ver a interface do usuário reprojetada para a tela de jornada (disponível somente com o novo modelo):

![](assets/new-canvas2.png)

**Qualquer novo recurso adicionado ao designer da jornada (incluindo relatórios em tempo real) só estará disponível para jornadas no novo modelo a partir de agora.**

## Aprimoramento do design da tela de jornada

Com o novo modelo de jornada, estamos introduzindo um novo e aprimorado **Interface do usuário da tela de jornada**, que se encaixa perfeitamente no ecossistema de soluções e aplicativos da Adobe Experience Cloud, proporcionando uma experiência do usuário intuitiva e eficiente. Qualquer jornada no novo modelo estará nesse novo design.

![](assets/new-canvas3.gif)

As atividades agora serão representadas por caixas quadradas com os seguintes recursos:

* A primeira linha que representa o tipo de atividade que geralmente será substituída por informações mais contextuais (em Ler públicos, ela conterá o nome do público selecionado) ou por um rótulo personalizado, se você definir um.
* A segunda linha sempre representa o tipo de atividade.

![](assets/new-canvas4.png)

Essa nova interface melhora a legibilidade da tela de jornada ao fornecer **rótulos e tipos de atividades mais claros**.

Também permite que a equipe de produtos adicione mais informações à tela com menos cliques. Um exemplo de &quot;mais informações&quot; seria a inclusão de relatórios ao vivo na tela de jornada, onde é possível ver os perfis que entram e saem das atividades devido a erros.

![](assets/new-canvas5.png)

## Relatórios ao vivo na tela de jornada

Além do layout aprimorado da tela de jornada, um novo recurso está sendo introduzido para permitir que os usuários visualizem métricas de relatórios em tempo real do **as últimas 24 horas**, chamado de relatórios em tempo real, diretamente na tela de jornada.

Para cada atividade em cada jornada ativa usando o novo modelo, você tem acesso a:


* A contagem de perfis que entram nesta atividade.
* A contagem de perfis que saem desta atividade devido a um erro.

![](assets/new-canvas6bis.png)

<!--`
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
