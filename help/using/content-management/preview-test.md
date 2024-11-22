---
title: Visualizar e testar o conteúdo
description: Saiba como pré-visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: a5eacd7a746b2f17804062b23aee3146db0434c9
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 26%

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

## Sobre visualização e teste {#about}

Depois que o conteúdo for definido, você poderá visualizar seu conteúdo antes de enviar a mensagem. Essa é uma etapa essencial para garantir que ela seja precisa, mas também esteja livre de erros nas configurações de conteúdo e personalização.

Você também pode enviar deliveries de teste de suas mensagens de email para recipients ou assinantes específicos para teste e validação e verificar a renderização em clientes populares de desktop, dispositivos móveis e baseados na Web.

>[!CAUTION]
>
>Ao visualizar uma mensagem ou enviar provas, somente os dados de personalização do perfil são exibidos. Personalization com base em dados de contexto, como informações de evento, só podem ser testadas no contexto de uma jornada. Saiba como testar a personalização em [este caso de uso](../personalization/personalization-use-case.md).

Todas essas ações podem ser executadas com o botão **[!UICONTROL Simular Conteúdo]**, acessível na tela de edição de conteúdo da sua mensagem, ou nos designers de email e da Web dos canais de email e da Web.

![](../email/assets/email-preview-button.png)

Observe que você precisa ter a permissão **[!DNL Manage Simulate Content]** incluída no perfil de produto **[!DNL Content Library Manager]**. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager).

## Teste usando perfis de teste ou dados de entrada de amostra {#methods}

Você pode visualizar e testar o conteúdo usando:

* **Perfis de teste**

  Use perfis de teste para pré-visualizar seu conteúdo, enviar provas de email e verificar a renderização de email. Se você adicionou campos personalizados, é possível verificar como eles são exibidos usando dados de perfil de teste. Para obter mais informações, consulte esta seção.

  ➡️ [Selecionar perfis de teste](test-profiles.md)

  ➡️ [Visualizar seu conteúdo usando perfis de teste](preview.md)

  ➡️ [Enviar provas de email](proofs.md)

  ➡️ [Verificar renderização de email](rendering.md)

  ➡️ [Visualizar e revisar seu email (vídeo)](#video-preview)

* **Dados de entrada de exemplo**

  O [!DNL Journey optimizer] permite testar diferentes variantes do seu conteúdo, visualizando-o e enviando provas com dados de entrada de exemplo carregados de um arquivo CSV/JSON ou adicionados manualmente.

  Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.

  ➡️ [Saiba como testar seu conteúdo usando dados de entrada de exemplo](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >No momento, esses recursos estão disponíveis para todos os clientes como um beta público somente para os canais de Email, SMS e Notificação por push.

## Vídeo tutorial {#video-preview}

Saiba como usar perfis de teste para testar a renderização de email nas caixas de entrada, visualizar emails personalizados em relação a perfis de teste e enviar provas.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
