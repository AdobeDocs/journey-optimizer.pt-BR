---
solution: Journey Optimizer
product: journey optimizer
title: Solucionar erros antes de testar ou publicar sua jornada
description: Saiba como solucionar erros antes de testar ou publicar sua jornada
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: solução de problemas, solução de problemas, jornada, verificação, erros
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 61498b61f7f05e0553fe575c980fd1bee08500a3
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 40%

---

# Solucionar erros antes de testar a jornada {#troubleshooting}

Nesta seção, saiba como solucionar problemas do jornada antes de testar ou publicar. Todos os controles enumerados a seguir podem ser efetuados quando a jornada estiver em modo de teste ou mesmo ativa. Recomenda-se que todas as verificações a seguir sejam feitas no modo de teste, para então prosseguir com a publicação. Saiba mais sobre o modo de teste em [esta página](../building-journeys/testing-the-journey.md).

Saiba como solucionar problemas de eventos do jornada, verificar se perfis entraram na sua jornada, como eles navegam por ela e se as mensagens são enviadas [nesta página](troubleshooting-execution.md).

Se você estiver usando ações de entrada, saiba como solucionar problemas deles [nesta página](troubleshooting-inbound.md).

## Erros nas atividades {#activity-errors}

Antes de testar e publicar sua jornada, verifique se todas as atividades estão configuradas corretamente. Não é possível executar testes ou publicações se os erros ainda forem detectados pelo sistema.

Os erros são exibidos com um símbolo de aviso na tela. Coloque o cursor no ponto de exclamação para exibir a mensagem de erro. Se você selecionar a atividade, verá a linha que contém o erro com um aviso. Por exemplo:

* se um campo obrigatório estiver vazio, um erro será exibido

  ![](assets/journey63.png)

* na tela, quando duas atividades são desconectadas, um aviso é exibido

  ![](assets/canvas-disconnected.png)

## Erros na jornada {#canvas-errors}

Os erros também são visíveis no botão **[!UICONTROL Alertas]**, acima da tela. Esse botão permite que você veja erros detectados pelo sistema e que impedem a ativação do modo de teste ou a publicação do jornada.

O sistema detecta dois tipos de problemas: **erros** e **avisos**. Os erros bloqueiam a publicação e a ativação de teste. Os avisos indicam possíveis problemas que não estão bloqueando a ativação de teste ou a publicação. Você verá uma descrição do problema e uma ID de registro de problemas do tipo ERR_XXX_XXX. Isso pode ajudar a identificar o problema.

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Erros e avisos globais para a jornada aparecem primeiro na lista. Os erros e avisos relacionados a atividades específicas são listados depois, por ordem de atividade ou aparência na jornada, da esquerda para a direita. Na parte inferior da lista de alertas, o botão **[!UICONTROL Copiar detalhes]** permite copiar informações técnicas sobre a jornada, que são úteis para solucionar problemas.

## Adicionar um caminho alternativo {#canvas-add-path}

Você pode definir uma ação de fallback em caso de erro para as seguintes atividades de jornada: **[!UICONTROL Condição]** e **[!UICONTROL Ação]**.

A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. A única maneira de fazê-lo continuar é resolver a questão. Para evitar a interrupção da jornada, você também pode marcar a opção **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]** nas propriedades da atividade. Saiba mais [nesta seção](../building-journeys/using-the-journey-designer.md#paths).
