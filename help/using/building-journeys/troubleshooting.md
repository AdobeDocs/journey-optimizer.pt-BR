---
solution: Journey Optimizer
product: journey optimizer
title: Solucionar erros antes de testar ou publicar sua jornada
description: Saiba como solucionar erros antes de testar ou publicar sua jornada
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: solução de problemas, solução de problemas, jornada, verificação, erros
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DorhpVm3trSxHG-l77-DpwbLTNQQxET1SIMYX-8ClQc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 548
ht-degree: 33%

---

# Solucionar erros antes de testar a jornada {#troubleshooting}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como localizar e corrigir erros de atividade e configuração de jornada antes de testar ou publicar, para que sua jornada possa ser executada sem problemas.

>[!ENDSHADEBOX]

Nesta seção, saiba como solucionar problemas do jornada antes de testar ou publicar. Todos os controles enumerados a seguir podem ser efetuados quando a jornada estiver em modo de teste ou mesmo ativa. Recomenda-se que todas as verificações a seguir sejam feitas no modo de teste, para então prosseguir com a publicação. Saiba mais sobre o modo de teste em [esta página](../building-journeys/testing-the-journey.md).

Saiba como solucionar problemas de eventos do jornada, verificar se os perfis inseriram sua jornada, como eles navegam por ela e se as mensagens são enviadas [nesta página](troubleshooting-execution.md). Se nenhum perfil entrar em sua jornada baseada em eventos, apesar dos eventos serem assimilados, verifique se os [tipos de dados de condição de evento correspondem ao esquema do evento](troubleshooting-execution.md#verify-event-identity-and-rule-data-types).

Se você estiver usando ações de entrada, saiba como solucionar problemas deles [nesta página](troubleshooting-inbound.md).

## Erros nas atividades {#activity-errors}

Antes de testar e publicar sua jornada, verifique se todas as atividades estão configuradas corretamente. Não é possível executar testes ou publicações se os erros ainda forem detectados pelo sistema.

Os erros são exibidos com um símbolo de aviso na tela. Coloque o cursor no ponto de exclamação para exibir a mensagem de erro. Se você selecionar a atividade, verá a linha que contém o erro com um aviso. Por exemplo:

* se um campo obrigatório estiver vazio, um erro será exibido

  ![Erros de validação de Jornada exibidos na tela com indicadores de erro](assets/journey63.png)

* na tela, quando duas atividades são desconectadas, um aviso é exibido

  ![Ícone de aviso mostrando atividades desconectadas na tela do jornada](assets/canvas-disconnected.png)

## Erros na jornada {#canvas-errors}

Os erros também são visíveis no botão **[!UICONTROL Alertas]**, acima da tela. Esse botão permite que você veja erros detectados pelo sistema e que impedem a ativação do modo de teste ou a publicação do jornada.

O sistema detecta dois tipos de problemas: **erros** e **avisos**. Os erros bloqueiam a publicação e a ativação de teste. Os avisos indicam possíveis problemas que não estão bloqueando a ativação de teste ou a publicação. Você verá uma descrição do problema e uma ID de registro de problemas do tipo ERR_XXX_XXX. Isso pode ajudar a identificar o problema.

![Indicadores de erro e aviso no jornada com dicas de ferramentas de descrição](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Erros e avisos globais para a jornada aparecem primeiro na lista. Os erros e avisos relacionados a atividades específicas são listados depois, por ordem de atividade ou aparência na jornada, da esquerda para a direita. Na parte inferior da lista de alertas, o botão **[!UICONTROL Copiar detalhes]** permite copiar informações técnicas sobre a jornada, que são úteis para solucionar problemas. Para obter a lista de campos copiados (incluindo informações de pausa e retomada), consulte [Copiar detalhes técnicos](journey-properties.md#access-properties) nas propriedades da jornada.

## Adicionar um caminho alternativo {#canvas-add-path}

Você pode definir uma ação de fallback em caso de erro para as seguintes atividades de jornada: **[!UICONTROL Otimizar]** e **[!UICONTROL Ação]**.

A jornada de uma pessoa para quando ocorre um erro em uma ação ou condição. A única maneira de fazê-lo continuar é resolver a questão. Para evitar a interrupção da jornada, você também pode marcar a opção **[!UICONTROL Adicionar um caminho alternativo em caso de tempo limite ou erro]** nas propriedades da atividade. Saiba mais [nesta seção](../building-journeys/using-the-journey-designer.md#paths).
