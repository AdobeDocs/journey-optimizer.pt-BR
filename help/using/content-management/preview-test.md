---
title: Visualizar e testar o conteúdo
description: Saiba como visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 57%

---

# Visualizar e testar o conteúdo {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Verificar como o conteúdo está sendo renderizado"
>abstract="Depois que o conteúdo for definido, você poderá usar perfis de teste para visualizá-lo e verificar se a renderização está correta, de acordo com o canal que está usando."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Verificar como o conteúdo está sendo renderizado"
>abstract="Depois que o conteúdo for definido, você poderá visualizá-lo e verificar se a renderização está correta de acordo com o canal que está usando."

Depois que o conteúdo for definido, você poderá visualizá-lo antes de enviar a mensagem. Essa é uma etapa essencial para garantir que seja preciso, mas também esteja livre de erros no conteúdo e nas configurações de personalização.

Você também pode enviar entregas de teste das mensagens de email para destinatários ou assinantes específicos para teste e validação e verificar a renderização em clientes populares de desktop, dispositivos móveis e baseados na Web.

Todas essas ações podem ser realizadas com o botão **[!UICONTROL Simular conteúdo]**, acessível na tela de edição de conteúdo da mensagem, ou nos designers de email e da Web dos canais de email e da Web.

![](../email/assets/email-preview-button.png)

## Teste usando dados de perfis de teste ou dados de entrada de amostra {#methods}

O Journey Optimizer fornece duas experiências para testar o conteúdo:

* **Testando conteúdo usando dados de perfis de teste**

  Você pode usar perfis de teste para pré-visualizar seu conteúdo, enviar provas de email e verificar a renderização de email. Se você tiver adicionado campos personalizados, poderá verificar como eles são exibidos usando dados de perfil de teste. Para obter mais informações, consulte estas seções:

  ➡️ [Selecionar perfis de teste](test-profiles.md)
➡️ [Visualizar usando perfis de teste](preview.md)
➡️ [Enviar provas de email](proofs.md)
➡️ [Verificar renderização de email](rendering.md)
➡️ [Visualizar e revisar seu email (vídeo)](#video-preview)

* **Testando variações de conteúdo usando dados de entrada de exemplo**

  O [!DNL Journey optimizer] permite que você visualize e envie provas de diferentes variações do seu conteúdo usando dados de entrada de exemplo carregados de um arquivo CSV/JSON ou adicionados manualmente.

  Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.

  ➡️ [Simular variações de conteúdo](../test-approve/simulate-sample-input.md)

## Leitura obrigatória

* **Permissões necessárias** - Você precisa ter a permissão **[!DNL Manage Simulate Content]** incluída no perfil de produto **[!DNL Content Library Manager]**. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager).

  Para enviar provas, você deve ter **permissões Aprovar e publicar** para o recurso específico (campanha ou jornada) associado ao email. Além disso, para enviar provas em uma jornada, a permissão **Publicar jornada** também é necessária. [Saiba mais sobre permissões](../administration/ootb-permissions.md).

* **Personalization com dados de contexto** - Ao visualizar uma mensagem ou enviar provas, somente os dados de personalização do perfil são exibidos. Personalização com base em dados de contexto, como informações de evento, só podem ser testados no contexto de uma jornada. Saiba mais sobre [este caso de uso](../personalization/personalization-use-case.md).

* **Visualizar conteúdo com várias variantes condicionais** - Ao simular ou renderizar provas para emails que contêm várias variantes condicionais, o Journey Optimizer pode exigir mais tempo de processamento. Se você observar falhas de tempo-limite ou mensagens de erro, considere reduzir o número total de variantes ou simplificar as regras condicionais. Saiba mais sobre conteúdo condicional [nesta página](../personalization/dynamic-content.md).

## Vídeo tutorial {#video-preview}

Saiba como usar perfis de teste para testar a renderização de email nas caixas de entrada, visualizar emails personalizados em relação a perfis de teste e enviar provas.

>[!VIDEO](https://video.tv.adobe.com/v/3430342?quality=12&captions=por_br)
