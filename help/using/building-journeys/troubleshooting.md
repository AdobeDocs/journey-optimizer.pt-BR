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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 995
ht-degree: 18%

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

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como identificar e resolver erros e avisos de configuração em uma jornada antes de entrar no modo de teste ou na publicação.

**Intenções:**

* Identificar erros de configuração no nível de atividade antes de testar ou publicar uma jornada
* Distinguir entre erros de bloqueio e avisos de não bloqueio no painel Alertas
* Use a ID de log de erros (formato ERR_XXX_XXX) para diagnosticar problemas de jornada
* Copie os detalhes da jornada técnica para compartilhar com os administradores e solucionar problemas
* Adicionar um caminho alternativo para impedir que jornadas individuais parem devido a um erro ou tempo limite

**Glossário:**

* **Botão Alertas**: Controle da tela que exibe todos os erros detectados pelo sistema e avisos bloqueando a publicação ou a ativação de teste *(específico do produto)*
* **ERR_XXX_XXX**: formato de ID de log de problemas atribuído a cada problema detectado, usado para identificar e comunicar erros *(específico do produto)*
* **Caminho alternativo**: uma ramificação de fallback adicionada a uma atividade de ação ou condição que continua a jornada quando ocorre um erro ou tempo limite *(específico do produto)*

**Medidas de Proteção:**

* Não é possível ativar o modo de teste ou publicar uma jornada se os erros de bloqueio permanecerem não resolvidos.
* Os avisos não bloqueiam a publicação ou a ativação de teste, mas indicam possíveis problemas.
* Caminhos alternativos só estão disponíveis para atividades Otimizar e Ação.

**Terminologia:**

* Nome canônico: Alertas — Acrônimo: none — variantes: painel Alertas, botão Alertas
* Sinônimos: &quot;erros&quot; = &quot;problemas de bloqueio&quot;; &quot;avisos&quot; = &quot;problemas de não bloqueio&quot;
* Não confundir: &quot;errors&quot; (publicação em bloco) ≠ &quot;warnings&quot; (não bloquear a publicação)

**Perguntas frequentes:**

* **P: Qual é a diferença entre um erro e um aviso no Journey Optimizer?** — Os erros bloqueiam a ativação do modo de teste e a publicação do jornada; os avisos indicam possíveis problemas, mas não impedem que sejam realizados testes ou publicações.
* **P: Onde posso ver todos os erros que afetam minha jornada?** — Clique no botão Alertas acima da tela para ver uma lista consolidada de todos os erros e avisos detectados pelo sistema.
* **P: O que devo fazer se não conseguir identificar um problema da descrição do erro?** — use o botão Copy details (Copiar detalhes) na parte inferior da lista Alerts (Alertas) para capturar informações técnicas e enviá-las ao administrador.
* **P: Posso manter uma jornada em execução para indivíduos mesmo se uma ação encontrar um erro?** — Sim, ative a opção &quot;Adicionar um caminho alternativo em caso de tempo limite ou erro&quot; nas propriedades da atividade para definir um caminho de fallback.
* **P: Quando devo executar essas verificações de solução de problemas?** — Todas as verificações podem ser executadas no modo de teste ou quando a jornada está ativa; a recomendação é resolver todos os problemas no modo de teste antes da publicação.

+++
