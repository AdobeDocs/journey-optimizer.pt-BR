---
solution: Journey Optimizer
product: journey optimizer
title: Enviar usando ondas no jornada
description: Programe mensagens de jornada de saída para serem entregues em lotes controlados (ondas) ao longo do tempo. O envio de ondas em jornadas de leitura de público ajuda a balancear a carga e oferecer suporte à capacidade de entrega.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
keywords: ondas, lotes, programação, jornada, ler público, entregabilidade
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# Enviar usando ondas no jornada {#send-using-waves-journeys}

>[!AVAILABILITY]
>
>Este recurso está em Disponibilidade Limitada. Entre em contato com o representante da Adobe para obter acesso.

Você pode entregar mensagens de saída de uma jornada em lotes (ondas) ao longo do tempo, em vez de todas de uma só vez. O envio de ondas ajuda a balancear a carga, evitar sistemas downstream esmagadores (como centrais de atendimento ou páginas de aterrissagem) e oferecer suporte à capacidade de entrega e reputação do remetente, especialmente para jornadas de alto volume de público-alvo de leitura.

<!--
>[!CAUTION]
>
>Wave sending is available for read audience journeys only and applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Você a configura no nível da jornada ao definir como o público-alvo entra e como as ações são agendadas. Você define o número de ondas, seu tamanho (como uma porcentagem do público ou como números absolutos) e quando cada onda é executada.

## Limitações e medidas de proteção {#limitations-guardrails}

* O envio de onda só está disponível para jornadas de público-alvo de leitura com os tipos de agendador **[!DNL As soon as possible]** e **[!UICONTROL Once]**. Saiba mais sobre o [cronograma de jornadas](read-audience.md#schedule).
* O envio de onda não está disponível para jornadas recorrentes, acionadas por eventos, de eventos comerciais, de modo de teste ou de simulação.
* Você deve definir pelo menos **2 ondas** e pode adicionar até **10 ondas**.
* O intervalo mínimo entre o início de duas ondas é de **30 minutos**.
* Um início de onda não pode ser anterior ao início da jornada ou no passado.
* A divisão do público em ondas pode levar até 1 hora. Os perfis não podem entrar na jornada até lá.
* Em uma única versão do jornada, duas ondas nunca são executadas ao mesmo tempo. A próxima onda começa somente após a conclusão da onda anterior. Por exemplo, se as ondas forem agendadas com 1 hora de diferença, mas a primeira onda ocorrer por 2 horas, a segunda onda começará quando a primeira onda terminar, não no horário agendado.
* Os inícios de onda podem ser atrasados quando a plataforma aplicar limites de cota ou quando a capacidade do sistema estiver sob carga pesada.

## Configurar o envio de ondas em uma jornada {#configure-wave-sending}

1. Inicie sua jornada com uma atividade [Ler público-alvo](read-audience.md).

1. Clique duas vezes na atividade **[!UICONTROL Ler público-alvo]** para abrir suas propriedades e selecione a opção **[!UICONTROL Fornecer ação de jornada em ondas]**.

   ![](assets/journey-wave-option.png){width="100%"}

1. Defina o **número de ondas** (por exemplo, 4).

   ![](assets/journey-wave-number.png){width="80%"}

   >[!NOTE]
   >
   >Você deve definir pelo menos 2 ondas e pode adicionar até 10 ondas.

1. Escolha como definir o tamanho e o tempo da onda conforme detalhado abaixo.

### Ondas iguais {#equal-waves}

Por padrão, o público-alvo é dividido em ondas de tamanho igual. Defina um intervalo fixo entre o início de cada onda (por exemplo, 2 horas).

![](assets/journey-equal-waves.png){width="70%"}

>[!NOTE]
>
>O intervalo mínimo entre o início de duas ondas é de **30 minutos**.

O sistema então agenda ondas subsequentes automaticamente (por exemplo, primeira onda às 9:00 AM, segunda às 11:00 AM, terceira às 1:00 PM, quarta às 3:00 PM).

### Distribuição personalizada {#custom-distribution}

Selecione a opção **[!UICONTROL Custom distribution]** para definir o tamanho de cada onda como uma porcentagem do público total (por exemplo, 15%, 20%, 25%, 40%).

![](assets/journey-wave-percentage.png){width="70%"}

>[!NOTE]
>
>O total em todas as ondas deve ser igual a 100%. Se esse não for o caso, uma mensagem de aviso será exibida.<!--are the waves actually sent or does the system prevent user from saving the journey?-->

Selecione **[!UICONTROL Números]** para definir o tamanho de cada onda como um número absoluto de perfis (por exemplo, 10.000; 50.000).

![](assets/journey-wave-numbers.png){width="70%"}

>[!NOTE]
>
>Ao usar números, o sistema não valida se a soma cobre todo o público-alvo. Você deve garantir que seus tamanhos de onda cubram o público-alvo para o qual você pretende enviar. Saiba mais nas [Perguntas frequentes](#faq).

### Agendamento personalizado {#custom-schedule}

Selecione **[!UICONTROL Agendar cada onda]** para definir uma data e hora de início específicas para cada onda. As ondas não precisam ter espaçamento uniforme (por exemplo, 9h00, 11h00, 17h00, 24h20, 20h30).:00:00:00:30

![](assets/journey-wave-custom-schedule.png){width="70%"}

>[!NOTE]
>
>O intervalo mínimo entre o início de duas ondas é de **30 minutos**.

## Casos de uso {#use-cases}

O envio de onda ajuda você a controlar quando e quantas mensagens são enviadas, o que pode melhorar a capacidade de entrega, proteger a reputação do remetente e alinhar os envios à sua capacidade operacional. Considere usar ondas nestes cenários:

* **Call center ou gestor de resposta:** limite quantas mensagens saem por dia ou por hora para que as equipes downstream (por exemplo, atendimento ao cliente) possam lidar com as respostas. Por exemplo, envie 20 mensagens por dia para corresponder à capacidade da central de atendimento.

  ![](assets/journey-waves-ex-call-center.png){width="55%"}

* **Alto volume e capacidade de entrega:** Evite enviar uma jornada muito grande de uma só vez. Espalhe a entrega ao longo do tempo para ajudar a manter a reputação do remetente e reduzir o risco de ser sinalizado como spam.

  ![](assets/journey-waves-ex-high-volume.png){width="55%"}

* **Aumento:** ao usar uma nova plataforma ou IP, aumente progressivamente o volume (por exemplo, 10% na primeira onda, depois 15%, 20% e assim por diante) para criar a reputação gradualmente.

  ![](assets/journey-waves-ex-ramp-up.png){width="55%"}

## Perguntas frequentes {#faq}

+++ O que acontece se a soma dos tamanhos de onda não for igual ao público total?

* Se a soma dos tamanhos das ondas **exceder** o público-alvo (por exemplo, você agendar 100.000 na primeira onda para um público-alvo de 100.000), a primeira onda enviará para o público-alvo completo e as ondas restantes não terão mais para enviar; elas não serão executadas.
* Se a soma **for menor** do que o público-alvo (por exemplo, você define quatro ondas totalizando 40.000 perfis para um público-alvo de 100.000), somente os perfis incluídos nessas ondas receberão a mensagem. O restante do público-alvo não receberá a comunicação e não será repetido em ondas posteriores.

+++

+++ Posso atribuir diferentes segmentos ou critérios a ondas individuais?

Você só pode definir o tamanho e o tempo das ondas. O mesmo público-alvo flui pela jornada; não é possível atribuir segmentos ou critérios diferentes a ondas individuais.

+++

## Consulte também {#see-also}

* [Usar um público em uma jornada](read-audience.md)—configure a atividade Ler Público.
