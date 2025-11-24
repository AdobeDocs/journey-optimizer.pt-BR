---
solution: Journey Optimizer
product: journey optimizer
title: Enviar emails somente em dias da semana
description: Saiba como configurar uma jornada para enviar emails somente em dias da semana no Adobe Journey Optimizer
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: jornada, caso de uso, dias da semana, condição, email, agendamento
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: eee9a460fc443be29c1ef407a02c5645869ca11d
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 0%

---

# Enviar emails somente em dias da semana {#send-emails-only-on-weekdays}

Esse caso de uso demonstra como configurar uma jornada no Adobe Journey Optimizer que envia emails somente em dias da semana (de segunda a sexta-feira). Para perfis que entram na jornada nos fins de semana (sábado ou domingo), os emails são automaticamente enfileirados e enviados na segunda-feira em um horário especificado. Isso garante o envolvimento ideal ao enviar mensagens durante a semana de trabalho.

## Visão geral do caso de uso

**O desafio**: garantir que os emails sejam enviados somente nos dias da semana, mesmo que os perfis possam entrar na jornada nos finais de semana. Para entradas no fim de semana, os emails devem ser enfileirados e enviados na segunda-feira em um horário específico.

**A Solução**: use uma atividade de condição para identificar o dia da semana. Para entradas no fim de semana, Aguarde as atividades com fórmulas personalizadas atrasarem o email até segunda-feira. As entradas de dias da semana prosseguem diretamente para a etapa de envio de email.

Essa abordagem mostra como usar uma atividade de condição para verificar se o dia atual é sábado ou domingo, implementar atividades de espera com fórmulas personalizadas para entradas de fim de semana, enfileirar emails de fim de semana para entrega de segunda-feira em uma hora específica e enviar emails imediatamente para entradas de dias da semana (segunda-feira a sexta-feira).

Essa abordagem é ideal para campanhas de email B2B (B2B), informativos e comunicações profissionais, anúncios relacionados a negócios, atualizações de produtos relacionadas ao trabalho e qualquer campanha de marketing em que a entrega no fim de semana não seja desejada.

>[!NOTE]
>
>Para implementar este caso de uso, você precisa de uma instância ativa do Adobe Journey Optimizer com uma [superfície de canal de email](../configuration/channel-surfaces.md) configurada, um [público-alvo](../audience/about-audiences.md) ou [evento](../event/about-events.md) para acionar a jornada e uma compreensão básica das [condições de jornada](condition-activity.md) e [expressões](expression/expressionadvanced.md).


## Etapas de implementação

### Etapa 1: criar sua jornada

1. Navegue até **[!UICONTROL Gerenciamento de Jornadas]** > **[!UICONTROL Jornadas]** no Adobe Journey Optimizer.

1. Clique em **[!UICONTROL Criar Jornada]** para [criar uma nova jornada](journey-gs.md).

1. Configure as [propriedades de jornada](journey-properties.md).

1. Escolha seu ponto de entrada de jornada:
   * **[Ler público-alvo](read-audience.md)**: para campanhas em lote direcionadas a um público-alvo específico
   * **[Evento](../event/about-events.md)**: para jornadas acionadas em tempo real com base no comportamento do cliente

### Etapa 2: adicionar uma atividade de Condição para verificar o dia da semana

Logo após o início da jornada, adicione uma atividade **[!UICONTROL Condição]** para verificar se o dia atual é sábado ou domingo. Isso ramificará o fluxo de trabalho de acordo.

1. Arraste e solte uma atividade [**[!UICONTROL Condição &#x200B;]**](condition-activity.md) na tela após o ponto de entrada.

1. Clique na atividade **[!UICONTROL Condição]** para abrir seu painel de configuração.

1. Selecione **[!UICONTROL Condição de tempo]** como o tipo de condição.

1. Selecione **[!UICONTROL Dia da semana]** como a opção de filtragem de tempo.

1. Para o **primeiro caminho (sábado)**, selecione somente **sábado**. Rotule esse caminho como &quot;Sábado&quot;.

1. Clique em **[!UICONTROL Adicionar um caminho]** para criar uma segunda condição.

1. Para o **segundo caminho (domingo)**, selecione **[!UICONTROL Dia da semana]** e escolha somente **Domingo**. Rotule esse caminho como &quot;Domingo&quot;.

   ![Configurando as condições de sábado e domingo no editor de expressão](assets/weekday-email-uc-condition-expression.png)


1. Marque **[!UICONTROL Mostrar caminho para casos diferentes dos mencionados acima]** para criar um caminho para entradas durante a semana (de segunda a sexta).

>[!NOTE]
>
>O fuso horário usado para a avaliação do dia da semana é definido no nível da jornada nas propriedades da jornada, não no nível da condição. A jornada [timezone](timezone-management.md) usada na fórmula é o fuso horário configurado pela jornada, não do destinatário.

### Etapa 3: configurar atividades de espera para entradas do fim de semana

Para perfis que entram no sábado ou domingo, use as atividades de **[!UICONTROL Aguardar]** com fórmulas personalizadas para atrasar o email até segunda-feira na hora desejada.

Na atividade **[!UICONTROL Wait]**, use a seguinte fórmula:

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Em que:

* **X** é o número de dias de espera:
   * Usar **2** para sábado (aguardar até segunda-feira)
   * Usar **1** para domingo (aguardar até segunda-feira)
* **H** é a hora que você deseja enviar (por exemplo, **9** para a 9h)


**Exemplo para sábado:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Exemplo para domingo:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Para implementar isso em sua jornada:

1. No **caminho de sábado**, adicione uma atividade **[!UICONTROL Wait]** após a condição.

1. Selecione **[!UICONTROL Duração]** como o tipo de espera.

1. Clique em **[!UICONTROL Modo avançado]** para inserir a fórmula personalizada.

1. Digite: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Jornada com três caminhos de condição - Sábado, Domingo e Dias da Semana](assets/weekday-email-uc-paths.png)

1. Repita as mesmas etapas para o **caminho de domingo**, usando: `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Para horários comerciais mais complexos (por exemplo, enviar somente entre 9h e 17h em dias da semana), você pode aprimorar ainda mais a fórmula e as condições.

### Etapa 4: ramificação de dia da semana

Para perfis que entram de segunda a sexta-feira, prossiga para a etapa de envio de email como de costume.

1. No caminho **Dia da semana** (o caminho &quot;outros casos&quot;), prossiga diretamente para adicionar uma atividade de ação **[!UICONTROL Email]**. Nenhuma atividade **[!UICONTROL Wait]** é necessária para entradas durante a semana.

1. Configure sua mensagem de e-mail conforme necessário.

### Etapa 5: concluir o fluxo de jornada

Após as atividades de **[!UICONTROL Aguardar]** nos caminhos de sábado e domingo, todos os três caminhos (sábado, domingo e dias da semana) deverão fluir para a mesma atividade de ação de **[!UICONTROL Email]**. Adicione uma atividade **[!UICONTROL End]** após o email.

### Visão geral do fluxo de trabalho

O fluxo de trabalho completo do jornada segue essa lógica:

* **Início** → **[!UICONTROL Condição]**: É sábado ou domingo?
   * **Sim (sábado):** **[!UICONTROL Aguardar]** até segunda-feira, 9h → **[!UICONTROL Enviar email]**
   * **Sim (domingo):** **[!UICONTROL Aguardar]** até segunda-feira, 9h → **[!UICONTROL Enviar email]**
   * **Não (segunda a sexta-feira):** **[!UICONTROL Enviar email]** imediatamente

Isso garante que todos os emails sejam enviados somente em dias úteis, com entradas de fim de semana automaticamente enfileiradas para entrega na segunda-feira.

### Etapa 6: testar a jornada

Antes de publicar, teste completamente sua lógica de jornada no modo de teste do Adobe Journey Optimizer para confirmar se tudo funciona conforme o esperado:

1. Clique no botão **[!UICONTROL Testar]** no canto superior direito.

1. Habilitar [modo de teste](testing-the-journey.md).

1. Criar [perfis de teste](../audience/creating-test-profiles.md) com tempos de entrada simulados em diferentes dias da semana:
   * **Entrada de sábado**: verifique se o perfil segue o caminho de sábado, aguarda e recebe email na segunda-feira na hora especificada
   * **Entrada de domingo**: verifique se o perfil segue o caminho de domingo, aguarda e recebe email na segunda-feira na hora especificada
   * **Entradas de segunda a sexta-feira**: verifique se os emails são enviados imediatamente, sem qualquer espera

1. Revise a visualização da jornada para garantir que os perfis sigam os caminhos condicionais corretos (sábado, domingo ou dia da semana).

1. Verifique se há [erros ou avisos](troubleshooting.md) na jornada.

1. Verifique se as fórmulas de Espera calculam a duração correta para o tempo de delivery desejado na segunda-feira.

>[!IMPORTANT]
>
>Sempre teste a lógica da jornada no modo de teste para garantir que as atividades de espera se comportem conforme esperado. Use o Modo de teste para simular diferentes cenários de entrada e validar se as entradas do fim de semana estão corretamente enfileiradas para entrega na segunda-feira. Consulte [práticas recomendadas de teste do jornada](testing-the-journey.md) para obter mais detalhes.

### Etapa 7: publicar sua jornada

Quando o teste for concluído:

1. Clique em **[!UICONTROL Publicar]** no canto superior direito.

1. Confirme a [publicação](publish-journey.md).

1. Monitore o desempenho da jornada usando [relatórios de Jornada](report-journey.md) e [relatórios ao vivo](../reports/journey-live-report.md).


## Tópicos relacionados

* Saiba como criar caminhos diferentes em sua jornada com [atividades de condição](condition-activity.md)
* Guia detalhado sobre [uso das condições em uma jornada](conditions.md)
* Configurar durações e fórmulas de espera com a [Atividade de espera](wait-activity.md)
* Referência completa para [funções de data](functions/date-functions.md)
* Criar expressões complexas com o [Editor de expressão](expression/expressionadvanced.md)
* Abordagens recomendadas para [design e práticas recomendadas do jornada](journey-gs.md#best-practices)
