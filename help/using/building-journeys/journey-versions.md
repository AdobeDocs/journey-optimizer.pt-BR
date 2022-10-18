---
solution: Journey Optimizer
product: journey optimizer
title: Versões de jornada
description: Saiba mais sobre as versões do jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8d5ea4c1-bf23-4b58-8654-c251b90c3458
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 3%

---

# Versões de jornada{#journey-versions}

Na lista jornada, todas as versões do jornada são exibidas com o número da versão. Consulte [esta página](../building-journeys/using-the-journey-designer.md).

Quando você pesquisa por uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida no topo da interface da edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Na maioria dos casos, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá inserir uma jornada novamente, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada. [Leia mais](../building-journeys/journey-end.md)

Se precisar modificar para uma jornada ao vivo, será necessário criar uma nova versão da jornada.

>[!NOTE]
>
>Para saber mais sobre as medidas de proteção e limitações das versões do jornada, consulte [esta página](../start/guardrails.md#journey-versions-limitations)

1. Abra a versão mais recente da jornada dinâmica e clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Você só pode criar uma nova versão a partir da versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publicar]** e confirme.

   ![](assets/journeyversions3.png)

A partir do momento em que a jornada for publicada, os indivíduos começarão a fluir para a versão mais recente da jornada. As pessoas que já entraram em uma versão anterior ficam nela até terminarem a jornada. Se, posteriormente, eles digitarem novamente a mesma jornada, acessarão a versão mais recente.

As versões do Jornada podem ser interrompidas individualmente. Todas as versões do jornada têm o mesmo nome.

>[!NOTE]
>
>Ao publicar uma nova versão de uma jornada, a versão anterior automaticamente termina e alterna para a **Fechado** status. Nenhuma entrada na jornada acontecerá. Mesmo que você pare a versão mais recente, a versão anterior permanecerá fechada.
