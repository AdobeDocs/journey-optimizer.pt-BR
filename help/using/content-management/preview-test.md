---
title: Visualizar e testar o conteúdo
description: Saiba como visualizar e testar o conteúdo.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: ht
source-wordcount: '500'
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

Depois que o conteúdo for definido, você poderá visualizá-lo antes de enviar a mensagem. Essa é uma etapa essencial para garantir que seja preciso, mas também esteja livre de erros no conteúdo e nas configurações de personalização.

Você também pode enviar entregas de teste das mensagens de email para destinatários ou assinantes específicos para teste e validação e verificar a renderização em clientes populares de desktop, dispositivos móveis e baseados na Web.

Todas essas ações podem ser realizadas com o botão **[!UICONTROL Simular conteúdo]**, acessível pela tela de edição de conteúdo da mensagem ou pelos designers dos canais de email e da web.

![](../email/assets/email-preview-button.png)

## Testar usando dados de perfis de teste ou dados de exemplo. {#methods}

O Journey Optimizer fornece duas experiências para testar o conteúdo:

* **Testar conteúdo usando dados de perfis de teste**

  É possível usar perfis de teste para visualizar o conteúdo, enviar provas de email e verificar a renderização de email. Se você adicionou campos personalizados, é possível verificar como eles são exibidos usando dados de perfil de teste. Para obter mais informações, consulte estas seções:

  ➡️ [Selecionar perfis de teste](test-profiles.md)
➡️ [Visualizar usando perfis de teste](preview.md)
➡️ [Enviar provas de email](proofs.md)
➡️ [Verificar a renderização de email](rendering.md)
➡️ [Visualizar e revisar seu email (vídeo)](#video-preview)

* **Testar variações de conteúdo usando dados de exemplo**

  O [!DNL Journey optimizer] permite visualizar e enviar provas para diferentes variações do conteúdo usando dados de exemplo carregados por meio de um arquivo CSV/JSON ou adicionados manualmente.

  Todos os atributos de perfil usados no conteúdo para personalização são detectados automaticamente pelo sistema e podem ser usados nos testes para criar diversas variantes.

  ➡️ [Simular variações de conteúdo](../test-approve/simulate-sample-input.md)

## Leitura obrigatória

* **Permissões necessárias** - É necessário ter a permissão **[!DNL Manage Simulate Content]** incluída no perfil de produto do **[!DNL Content Library Manager]**. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager).

  Para enviar provas, é necessário ter as permissões **Aprovar e publicar** para o recurso específico (campanha ou jornada) associado ao email. Além disso, para enviar provas em uma jornada, a permissão **Publicar jornada** também é necessária. [Saiba mais sobre permissões](../administration/ootb-permissions.md).

* **Personalização sem dados de contexto** - Ao visualizar uma mensagem ou enviar provas, somente os dados de personalização do perfil serão exibidos. A personalização com base em dados de contexto, como informações de evento, só pode ser testada no contexto de uma jornada. Saiba como fazer isso [neste caso de uso](../personalization/personalization-use-case.md).

* **Visualizar conteúdo com diversas variantes condicionais** - Ao simular ou renderizar provas de emails que contêm diversas variantes condicionais, o Journey Optimizer pode exigir mais tempo de processamento. Se você observar falhas de tempo-limite ou mensagens de erro, considere reduzir o número total de variantes ou simplificar as regras condicionais. Saiba mais sobre conteúdo condicional [nesta página](../personalization/dynamic-content.md).

## Vídeo tutorial {#video-preview}

Saiba como usar perfis de teste para testar a renderização de email nas caixas de entrada, visualizar emails personalizados em relação a perfis de teste e enviar provas.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
