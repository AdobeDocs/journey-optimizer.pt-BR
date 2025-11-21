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
source-git-commit: 46a46fb25c1ef985a0bdea8974aa009e3699c7a3
workflow-type: tm+mt
source-wordcount: '1833'
ht-degree: 0%

---

# Enviar emails somente em dias da semana {#send-emails-only-on-weekdays}

Esse caso de uso demonstra como configurar uma jornada no Adobe Journey Optimizer que envia emails somente em dias da semana (de segunda a sexta-feira). Para perfis que entram na jornada nos fins de semana (sábado ou domingo), os emails são automaticamente enfileirados e enviados na segunda-feira em um horário especificado. Isso garante o envolvimento ideal ao enviar mensagens durante a semana de trabalho.

## Visão geral do caso de uso

**O desafio**: garantir que os emails sejam enviados somente nos dias da semana, mesmo que os perfis possam entrar na jornada nos finais de semana. Para entradas no fim de semana, os emails devem ser enfileirados e enviados na segunda-feira em um horário específico.

**A Solução**: use uma atividade de condição para identificar o dia da semana. Para entradas no fim de semana, Aguarde as atividades com fórmulas personalizadas atrasarem o email até segunda-feira. As entradas de dias da semana prosseguem diretamente para a etapa de envio de email.

Essa abordagem mostra como usar uma atividade de condição para verificar se o dia atual é sábado ou domingo, implementar atividades de espera com fórmulas personalizadas para entradas de fim de semana, enfileirar emails de fim de semana para entrega de segunda-feira em uma hora específica e enviar emails imediatamente para entradas de dias da semana (segunda-feira a sexta-feira).

Essa abordagem é ideal para campanhas de email B2B (B2B), informativos e comunicações profissionais, anúncios relacionados a negócios, atualizações de produtos relacionadas ao trabalho e qualquer campanha de marketing em que a entrega no fim de semana não seja desejada.

➡️ Assista passo a passo ao [tutorial em vídeo](#how-to-video)

>[!NOTE]
>
>Para implementar este caso de uso, você precisa de uma instância ativa do Adobe Journey Optimizer com uma [superfície de canal de email](../configuration/channel-surfaces.md) configurada, um [público-alvo](../audience/about-audiences.md) ou [evento](../event/about-events.md) para acionar a jornada e uma compreensão básica das [condições de jornada](condition-activity.md) e [expressões](expression/expressionadvanced.md).





## Etapas de implementação

### Etapa 1: criar sua jornada

1. Navegue até **[!UICONTROL Gerenciamento de Jornadas]** > **[!UICONTROL Jornadas]** no Adobe Journey Optimizer.

1. Clique em **[!UICONTROL Criar Jornada]** para criar uma nova jornada. [Saiba mais sobre como criar jornadas](journey-gs.md)

1. Configure as propriedades da jornada:
   * **Nome**: Campanha Por Email Durante A Semana
   * **Descrição**: envia emails somente em dias da semana (de segunda a sexta-feira)
   * Defina o namespace apropriado para seu caso de uso

[Saiba mais sobre as propriedades do jornada](journey-properties.md)

1. Escolha seu ponto de entrada de jornada:
   * **[Ler público-alvo](read-audience.md)**: para campanhas em lote direcionadas a um público-alvo específico
   * **[Evento](../event/about-events.md)**: para jornadas acionadas em tempo real com base no comportamento do cliente

### Etapa 2: adicionar uma atividade de Condição para verificar o dia da semana

Logo após o início da jornada, adicione uma atividade **[!UICONTROL Condição]** para verificar se o dia atual é sábado ou domingo. Isso ramificará o fluxo de trabalho de acordo.

1. Arraste e solte uma atividade **[!UICONTROL Condição]** na tela após o ponto de entrada. [Saiba mais sobre Atividades de condição](condition-activity.md)

1. Clique na atividade Condição para abrir seu painel de configuração.

1. Na seção **[!UICONTROL Tipo de condição]**, selecione **[!UICONTROL Condição de Source de Dados]**. [Saiba mais sobre tipos de condição](condition-activity.md#data_source_condition)

   ![Configurando a condição Saturday no editor de expressão](assets/weekday-email-uc-condition-expression.png)


### Etapa 3: configure a condição para identificar o sábado

Crie o primeiro caminho de condição para identificar entradas de sábado.

1. Clique em **[!UICONTROL Modo avançado]** para abrir o editor de expressão. [Saiba mais sobre o editor de expressão](expression/expressionadvanced.md)

1. Informe a seguinte expressão para verificar se o dia atual é sábado:

   ```javascript
   dayOfWeek(now()) == 7
   ```

   Isto usa a função `dayOfWeek()` com `now()` para obter o dia atual. [Saiba mais sobre funções de data](functions/date-functions.md)


1. Clique em **[!UICONTROL Ok]** para salvar a condição.

1. Rotule esse caminho como &quot;Sábado&quot;.

### Etapa 4: adicionar um segundo caminho de condição para domingo

1. Na atividade Condition, clique em **[!UICONTROL Add a path]** para criar uma segunda condição.

1. No editor de expressão do segundo caminho, digite:

   ```javascript
   dayOfWeek(now()) == 1
   ```

   Isso verifica se o dia atual é domingo.

1. Rotule esse caminho como &quot;Domingo&quot;.

1. Marque **[!UICONTROL Mostrar caminho para casos diferentes dos mencionados acima]** para criar um caminho para entradas durante a semana (de segunda a sexta).


>[!NOTE]
>
>A função `dayOfWeek()` retorna um número inteiro que representa o dia da semana, em que 1 é domingo e 7 é sábado. Isso segue o padrão ISO-8601 para numeração de dias.

### Etapa 5: configurar atividades de espera para entradas do fim de semana

Para perfis que entram no sábado ou domingo, use as atividades Aguardar com fórmulas personalizadas para atrasar o email até segunda-feira na hora desejada.


**Para o caminho de sábado:**

1. Adicione uma atividade **[!UICONTROL Wait]**. [Saiba mais sobre as atividades de espera](wait-activity.md)

1. Selecione **[!UICONTROL Duração]** como o tipo de espera.

1. Clique em **[!UICONTROL Modo avançado]** para inserir uma fórmula personalizada.

1. Informe a seguinte fórmula para aguardar até segunda-feira às 9h:

   ```javascript
   toDuration("PT" + (48 - getHourOfDay(now())) + "H")
   ```

   Ou use esta fórmula alternativa:

   ```javascript
   setHours(nowWithDelta(2, "days"), 9)
   ```

   ![Jornada com três caminhos de condição - Sábado, Domingo e Dias da Semana](assets/weekday-email-uc-paths.png)

   **Explicação**: esta fórmula calcula o tempo de espera de sábado a segunda-feira às 9h. O valor X=2 representa 2 dias à frente (sábado + 2 dias = segunda-feira). [Saiba mais sobre funções de data](functions/date-functions.md#nowWithDelta)

**Para o caminho de domingo:**

1. Adicione uma atividade **[!UICONTROL Wait]**.

1. Selecione **[!UICONTROL Duração]** como o tipo de espera.

1. Clique em **[!UICONTROL Modo avançado]** para inserir uma fórmula personalizada.

1. Informe a seguinte fórmula para aguardar até segunda-feira às 9h:

   ```javascript
   setHours(nowWithDelta(1, "days"), 9)
   ```

   **Explicação**: esta fórmula aguarda 1 dia (domingo + 1 dia = segunda-feira) e define o horário como 9:00 AM. O valor X=1 representa 1 dia adiante e H=9 representa 9:00 AM.

>[!TIP]
>
>Você pode personalizar o parâmetro de hora (H) a qualquer momento em que desejar que o email seja enviado na segunda-feira. Por exemplo, altere de 9 para 10 para 10 AM ou para 14 para 2 PM.

### Etapa 6: configurar o caminho do dia da semana

Para o **caminho do dia da semana** (de segunda a sexta-feira):

1. Continue diretamente para adicionar uma atividade de ação **[!UICONTROL Email]**. Nenhuma atividade Wait é necessária para entradas de dias da semana. [Saiba mais sobre ações de email](journeys-message.md)

1. Configurar sua mensagem de email:
   * Selecione ou crie seu [conteúdo de email](../email/get-started-email-design.md)
   * Configurar os [parâmetros de email](../email/email-settings.md)
   * Configure a [personalização](../personalization/personalize.md) conforme necessário

1. Adicione uma atividade **[!UICONTROL End]** após o email.

### Etapa 7: mesclar caminhos de fim de semana ao email

Após as atividades Wait nos caminhos sábado e domingo, mescle-as à mesma atividade Email action:

1. Na atividade Aguardar sábado, adicione uma ação **[!UICONTROL Email]**.

1. Na atividade de espera de domingo, conecte-se à mesma ação de email.

1. O caminho do dia da semana também deve fluir para esta ação Email.

### Etapa 8: testar a jornada

Antes de publicar, teste completamente sua lógica de jornada no modo de teste do Adobe Journey Optimizer para confirmar se tudo funciona conforme o esperado:

1. Clique no botão **[!UICONTROL Testar]** no canto superior direito.

1. Ativar modo de teste. [Saiba como testar sua jornada](testing-the-journey.md)

1. Criar [perfis de teste](../audience/creating-test-profiles.md) com tempos de entrada simulados em diferentes dias da semana:
   * **Entrada de sábado**: verifique se o perfil segue o caminho de sábado, aguarda e recebe email na segunda-feira na hora especificada
   * **Entrada de domingo**: verifique se o perfil segue o caminho de domingo, aguarda e recebe email na segunda-feira na hora especificada
   * **Entradas de segunda a sexta-feira**: verifique se os emails são enviados imediatamente, sem qualquer espera

1. Revise a visualização da jornada para garantir que os perfis sigam os caminhos condicionais corretos (sábado, domingo ou dia da semana).

1. Verifique se há erros ou avisos na jornada. [Saiba mais sobre como solucionar problemas do jornada](troubleshooting.md)

1. Verifique se as fórmulas de Espera calculam a duração correta para o tempo de delivery desejado na segunda-feira.

>[!IMPORTANT]
>
>Sempre teste a lógica de jornada completamente antes de publicar na produção. Use o Modo de teste para simular diferentes cenários de entrada e validar se as entradas do fim de semana estão corretamente enfileiradas para entrega na segunda-feira. [Saiba mais sobre as práticas recomendadas de teste do jornada](testing-the-journey.md)

### Etapa 9: publicar sua jornada

Quando o teste for concluído:

1. Clique em **[!UICONTROL Publicar]** no canto superior direito.

1. Confirme a publicação. [Saiba mais sobre a publicação de jornadas](publish-journey.md)

1. Monitore o desempenho da jornada usando [relatórios de Jornada](report-journey.md) e [relatórios ao vivo](../reports/journey-live-report.md).

## Práticas recomendadas e considerações

+++**Otimizar fluxo de trabalho com fórmulas aprimoradas**

Para aprimorar seu fluxo de trabalho e lidar com requisitos comerciais mais complexos, você pode estender as fórmulas para considerar feriados, fusos horários ou horários comerciais específicos além da verificação básica durante a semana. Ajuste o parâmetro de hora (H) na fórmula de Espera para corresponder ao seu tempo de envio ideal; por exemplo, se 10h mostrar melhores taxas de engajamento, altere a fórmula para usar a hora 10. Para suporte a vários fusos horários, considere criar jornadas separadas para diferentes regiões geográficas para garantir o delivery na segunda-feira no fuso horário local de cada recipient.

+++

+++**Gerenciamento de fuso horário**

A função `now()` e a execução da jornada usam o fuso horário configurado no nível da jornada. Verifique se o fuso horário da jornada corresponde às suas necessidades, configurando-o nas propriedades da jornada antes da publicação ([Saiba mais sobre o gerenciamento de fuso horário](timezone-management.md)). Se o público-alvo passar por vários fusos horários, observe que a verificação do dia da semana acontece no fuso horário configurado da jornada, não no fuso horário local do recipient. Para uma entrega específica de fuso horário, crie jornadas separadas para regiões diferentes ou use as configurações de fuso horário na atividade Ler público.

+++

+++**Entrada e tempo de Jornada**

Para jornadas em lote, [agende a Leitura de Público](read-audience.md#schedule) para disparar em um horário que faça sentido para o seu público-alvo. As execuções matinais (por exemplo, às 6:00 AM) são comuns para comunicações comerciais. Para jornadas baseadas em eventos, a condição será avaliada imediatamente quando o evento for recebido, e os perfis que entram nos finais de semana aguardarão automaticamente até segunda-feira ([Saiba mais sobre eventos](../event/about-events.md)). Verifique se as [configurações de tempo limite da jornada](journey-properties.md#timeout) acomodam o período máximo de espera (até 2 dias de sábado a segunda-feira).

+++

+++**Testes são essenciais**

Conforme enfatizado no guia de implementação, sempre teste a lógica da jornada para confirmar se tudo funciona conforme esperado. Use o **Modo de Teste** para simular diferentes cenários de entrada sem enviar emails reais. Teste todos os três caminhos (entradas de sábado, entradas de domingo e entradas de dias da semana), verifique se os cálculos de duração da espera estão corretos, confirme se o delivery de segunda-feira ocorre na hora especificada e verifique a visualização do jornada para garantir o roteamento adequado do caminho.

+++

+++**Reentrada e frequência**

Para campanhas recorrentes, defina as configurações de **[!UICONTROL Reentrada]** apropriadamente ([Saiba mais sobre configurações de reentrada](entry-management.md)). Se os perfis puderem entrar na jornada novamente, eles estarão sujeitos à verificação do dia da semana toda vez, garantindo que as entradas do fim de semana sejam sempre enfileiradas para segunda-feira. Considere adicionar [regras de limite de frequência](../conflict-prioritization/journey-capping.md) para evitar mensagens excessivas se os perfis puderem entrar novamente com frequência.

+++

## Variações avançadas

+++**Direcionamento específico de dia**

Para enviar emails somente em dias específicos (por exemplo, terças e quintas-feiras), modifique a condição:

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

Para todos os outros dias, adicione uma atividade Wait que calcula o número de dias até a próxima terça ou quinta-feira.

+++

+++**Diferentes horários de envio para dias diferentes**

Você pode criar vários caminhos com diferentes fórmulas de espera para diferentes comportamentos de fim de semana. Por exemplo, use `nowWithDelta(4, "days")` para entrega de sábado a quarta-feira ou `nowWithDelta(2, "days")` para entrega de domingo a terça-feira. Isso permite mais flexibilidade na programação de envio.

+++

+++**Entrega no horário comercial**

Para garantir a entrega durante o horário comercial, ajuste o parâmetro de hora na fórmula de Espera. Por exemplo, para uma entrega às 14h em vez de às 9h:

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

Você também pode adicionar uma segunda condição após a espera para verificar se o horário atual está dentro do horário comercial antes do envio.

+++

+++**Exclusão de feriado**

Para excluir feriados, adicione um caminho de condição adicional que verifique datas específicas:

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

Se a condição corresponder a um feriado, adicione uma atividade Aguardar para atrasar até o próximo dia útil. [Saiba mais sobre as funções de comparação de datas](functions/date-functions.md)

+++

## Tópicos relacionados

* [Sobre as atividades de Condição](condition-activity.md) - Saiba como criar caminhos diferentes na jornada
* [Usar condições em uma jornada](conditions.md) - Guia detalhado sobre condições de jornada
* [Atividade de espera](wait-activity.md) - Configurar durações e fórmulas de espera
* [Funções de data](functions/date-functions.md) - Referência completa para funções de data e hora
* [Editor de expressão](expression/expressionadvanced.md) - Criar expressões complexas
* [Testar sua jornada](testing-the-journey.md) - Valide a lógica de jornada antes de publicar
* [Gerenciamento de fuso horário](timezone-management.md) - Lidar com fusos horários diferentes no jornada
* [Práticas recomendadas do Jornada](journey-gs.md#best-practices) - Abordagens recomendadas para o design do jornada

## Vídeo tutorial

Saiba como enviar emails somente em dias da semana usando o Adobe Journey Optimizer. Este vídeo demonstra a implementação passo a passo de atividades de condição e fórmulas de Espera para enfileirar entradas de fim de semana para entrega na segunda-feira.

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## Recursos adicionais

* [Documentação do editor de expressões](expression/expressionadvanced.md) - Compilar e validar expressões de jornada
* [guia do designer de Jornadas](using-the-journey-designer.md) - Domine a tela de jornada
* [Visão geral dos casos de uso do Jornada](jo-use-cases.md) - Explore mais padrões e exemplos de jornada
* [Publicação do blog da comunidade: como enviar emails somente em dias de semana](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400?profile.language=pt){target="_blank"} - Publicação do blog original com exemplos detalhados

