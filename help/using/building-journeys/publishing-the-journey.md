---
solution: Journey Optimizer
product: journey optimizer
title: Publicar a jornada
description: Saiba como publicar uma jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, jornada, ao vivo, validade, verificar
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 42%

---

# Publicar a jornada {#publishing-the-journey}

Você deve publicar uma jornada para ativá-la e disponibilizá-la para que novos perfis possam entrar na jornada. Antes de publicar sua jornada, verifique se ela é válida e se não há erros. Não é possível publicar uma jornada com erros.

➡️ [Conheça este recurso no vídeo](#video)

## Processo de publicação {#journey-publication}

As etapas para publicar uma jornada são detalhadas abaixo:

1. Antes de publicar sua jornada, verifique se ela é válida e se não há erros. Não é possível publicar uma jornada com erros.

   * Saiba como testar sua jornada em [esta página](testing-the-journey.md).
   * Saiba como solucionar erros do jornada [nesta seção](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

1. Para publicar a jornada, clique na opção **[!UICONTROL Publicar]**, localizada no menu suspenso no canto superior direito.

   >[!NOTE]
   >
   > Se sua jornada estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para publicar sua jornada. [Saiba mais](../test-approve/gs-approval.md)

   ![](assets/journeyuc1_18.png)

Quando a jornada é publicada, ela está no modo **somente leitura**. No modo somente leitura, você só pode modificar os rótulos e as descrições da atividade, o nome da jornada e a descrição da jornada. Se precisar fazer modificações adicionais em uma jornada publicada, crie [uma nova versão](journey-ui.md#journey-versions) da jornada.

Quando você interrompe uma jornada, ela é interrompida permanentemente. Todos os indivíduos que fluem pela jornada são permanentemente interrompidos e a jornada para de permitir novas entradas. Se precisar executar a jornada novamente, duplique-a e publique a nova jornada.

>[!IMPORTANT]
>
>Se forem feitas alterações em uma decisão de oferta usada na mensagem de uma jornada, será necessário desfazer a publicação da jornada e republicá-la. Isso garante que as alterações sejam incorporadas à mensagem da jornada e que ela seja consistente com as atualizações mais recentes.

## Versões de jornada {#journey-versions}

Na lista da jornada, todas as versões da jornada são exibidas com o número da versão. Quando você pesquisa uma jornada, as versões mais recentes são exibidas na parte superior da lista na primeira vez que o aplicativo é aberto. Em seguida, você pode definir a classificação desejada e o aplicativo a manterá como uma preferência de usuário. A versão da jornada também é exibida na parte superior da interface de edição da jornada, acima da tela.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Normalmente, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo, para todas as versões ativas da jornada. Se a reentrada estiver habilitada, um perfil poderá ser inserido em uma jornada novamente, mas não poderá fazer isso até que tenha saído totalmente da instância anterior da jornada. [Leia mais](entry-management.md).

### Criar uma nova versão de uma jornada {#journey-create-new-version}

Se precisar modificar para uma jornada em tempo real, crie uma nova versão da jornada. Para criar uma nova versão de uma jornada existente, siga as etapas abaixo:

1. Abra a versão mais recente da jornada ativa, clique em **[!UICONTROL Criar uma nova versão]** e confirme.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Só é possível criar uma nova versão com base na versão mais recente de uma jornada.

1. Faça as modificações, clique em **[!UICONTROL Publicar]** e confirme.

A partir do momento em que a jornada for publicada, pessoas físicas começarão a acessar a versão mais recente da jornada. As pessoas que já acessaram uma versão anterior permanecerão nela até que concluam a jornada. Se mais tarde entrarem novamente na mesma jornada, a versão mais recente será acessada.

As versões da jornada podem ser interrompidas individualmente. Todas as versões das jornadas possuem o mesmo nome.

Ao publicar uma nova versão de uma jornada, a versão anterior encerra automaticamente e alterna para o status **Fechado**. Nenhuma entrada na jornada pode acontecer. Mesmo que você interrompa a versão mais recente, a versão anterior permanecerá fechada.


>[!NOTE]
>
>Medidas de proteção e limitações específicas se aplicam ao controle de versão das jornadas. Saiba mais [nesta página](../start/guardrails.md#journey-versions-journey-versions-g).


## Vídeo tutorial {#video}

Saiba como publicar uma jornada neste vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)