---
solution: Journey Optimizer
product: journey optimizer
title: Pré-visualizar, validar e enviar a mensagem LINE
description: Saiba como visualizar e validar uma mensagem LINE, resolver avisos e erros, solicitar aprovação quando necessário e ativá-la ou publicá-la em uma jornada ou campanha
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 94a7cd6e4e89b2c8a4a09cfb4fbfc173ca76c391
workflow-type: tm+mt
source-wordcount: 400
ht-degree: 2%

---


# Pré-visualizar, validar e enviar a mensagem LINE {#send-line}

>[!BEGINSHADEBOX]

**Nesta página:** visualize e valide a mensagem LINE, resolva avisos e erros, solicite aprovação quando necessário e conclua a configuração da jornada ou da campanha para enviar a mensagem.

>[!ENDSHADEBOX]

## Antes de começar {#before-you-start}

Antes de começar, verifique se:

* O LINE está ativado para sua organização. Se o LINE não estiver disponível, entre em contato com o representante da Adobe para solicitar a ativação.
* Uma configuração de canal LINE está disponível no Journey Optimizer. Consulte [Configurar o canal LINE](./line-configuration.md).
* Você adicionou uma ação LINE a uma jornada ou campanha e definiu o conteúdo da mensagem. Consulte [Criar uma mensagem LINE](./create-line.md).

## Pré-visualização da mensagem LINE {#preview-line}

Depois de definir o conteúdo da mensagem, use **[!UICONTROL Simular conteúdo]** para visualizar a mensagem antes de enviá-la.

Você pode usar uma das seguintes opções:

| Opção de simulação | Use-o para |
| --- | --- |
| **[!UICONTROL Simular conteúdo]** | Teste as variações de conteúdo com exemplos de dados de entrada ou geração automática de IA. |
| **[!UICONTROL Simular conteúdo]** > **[!UICONTROL Simular conteúdo (perfis do AEP)]** | Pré-visualizar a mensagem com perfis de teste. |

Revise cada variação e verifique se o conteúdo da mensagem e os valores personalizados são exibidos conforme esperado.

Para obter informações detalhadas sobre visualização e teste de conteúdo, consulte [Visualizar e testar conteúdo](../content-management/preview-test.md).

## Validar seu conteúdo {#line-validate}

Antes de continuar, revise os alertas mostrados na parte superior do editor de mensagens.

O Journey Optimizer exibe dois tipos de alertas:

* **Avisos** são recomendações ou sugestões de práticas recomendadas. Elas não impedem que você teste ou envie a mensagem.
* **Erros** identificam problemas que devem ser resolvidos antes que você possa testar ou ativar a jornada ou publicar a campanha.

Resolva todos os erros antes de continuar. Avisos de endereço quando eles indicarem que a mensagem pode não fornecer a experiência do cliente desejada.

## Solicitar aprovação quando necessário {#line-approval}

Se a campanha estiver sujeita a uma política de aprovação, solicite aprovação antes de enviar a mensagem.

Consulte [Saiba como solicitar aprovação](../test-approve/gs-approval.md).

## Enviar a mensagem LINE {#line-send}

Quando a mensagem estiver pronta, retorne à jornada ou campanha que contém a ação LINE e conclua a configuração:

* **Jornada:** conclua a configuração da jornada e ative-a.
* **Campanha:** conclua a configuração da campanha e publique a campanha.

Se não conseguir ativar a jornada ou publicar a campanha, retorne ao editor de mensagens e resolva os erros restantes.

## Tarefas relacionadas {#related-tasks}

* [Introdução ao LINE](./get-started-line.md)
* [Criar uma mensagem LINE](./create-line.md)
* [Configurar o canal LINE](./line-configuration.md)

{{$include /help/_includes/do-not-localize/line/ai-augmented-send-line.md}}
