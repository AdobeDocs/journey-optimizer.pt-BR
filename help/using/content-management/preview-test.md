---
title: Visualizar e testar o conteúdo
description: Saiba como visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: ht
source-wordcount: '436'
ht-degree: 100%

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

## Sobre a visualização e teste {#about}

Depois que o conteúdo for definido, você poderá visualizá-lo antes de enviar a mensagem. Essa é uma etapa essencial para garantir que seja preciso, mas também esteja livre de erros no conteúdo e nas configurações de personalização.

Você também pode enviar entregas de teste das mensagens de email para destinatários ou assinantes específicos para teste e validação e verificar a renderização em clientes populares de desktop, dispositivos móveis e baseados na Web.

>[!CAUTION]
>
>Ao visualizar uma mensagem ou enviar provas, somente os dados de personalização do perfil serão exibidos. Personalização com base em dados de contexto, como informações de evento, só podem ser testados no contexto de uma jornada. Saiba como testar a personalização [neste caso de uso](../personalization/personalization-use-case.md).

Todas essas ações podem ser realizadas com o botão **[!UICONTROL Simular conteúdo]**, acessível na tela de edição de conteúdo da mensagem, ou nos designers de email e da Web dos canais de email e da Web.

![](../email/assets/email-preview-button.png)

Observe que é necessário ter a permissão **[!DNL Manage Simulate Content]** incluída no perfil de produto **[!DNL Content Library Manager]**. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager).

## Teste usando perfis de teste ou dados de entrada de exemplo {#methods}

Você pode visualizar e testar o conteúdo ao usar:

* **Perfis de teste**

  Use perfis de teste para visualizar o conteúdo, enviar provas de email e verificar a renderização de email. Se você adicionou campos personalizados, é possível verificar como são exibidos usando dados do perfil de teste. Para obter mais informações, consulte estas seções:

  ➡️ [Selecionar perfis de teste](test-profiles.md)

  ➡️ [Visualizar o conteúdo usando perfis de teste](preview.md)

  ➡️ [Enviar provas de email](proofs.md)

  ➡️ [Verificar renderização de email](rendering.md)

  ➡️ [Visualizar e realizar provas de email (vídeo)](#video-preview)

* **Dados de entrada de exemplo**

  O [!DNL Journey optimizer] permite testar diferentes variantes do conteúdo, possibilitando visualizar o conteúdo e enviar provas com dados de entrada de exemplo carregados a partir de um arquivo CSV/JSON ou adicionados manualmente.

  Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.

  ➡️ [Saiba como testar o conteúdo usando dados de entrada de exemplo](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >No momento, esse recurso está disponível para todos os clientes como um beta público para somente os canais de email, SMS e notificação por push.

## Vídeo tutorial {#video-preview}

Saiba como usar perfis de teste para testar a renderização de email nas caixas de entrada, visualizar emails personalizados em relação a perfis de teste e enviar provas.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
