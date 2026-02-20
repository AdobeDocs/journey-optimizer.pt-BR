---
solution: Journey Optimizer
product: journey optimizer
title: Enviar usando ondas
description: Programe mensagens de campanha de saída para serem entregues em lotes controlados ao longo do tempo. O envio de onda oferece suporte à capacidade de entrega e ajuda a manter a reputação do remetente.
feature: Campaigns
topic: Campaign scheduling
role: User
level: Intermediate
keywords: ondas, lotes, programação, campanha, jornada, deliverability
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# Enviar usando ondas em campanhas {#send-using-waves}

Você pode dividir o delivery de mensagens de campanha de saída em vários lotes (ondas) e agendá-los ao longo do tempo. O envio de ondas ajuda a balancear a carga, evitar sistemas downstream esmagadores (como centrais de atendimento ou páginas de aterrissagem) e oferecer suporte à capacidade de entrega e à reputação do remetente, especialmente para envios de alto volume.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

O Journey Optimizer permite definir o número de ondas, seu tamanho (como uma porcentagem do público ou como números absolutos) e quando cada onda é executada.

## Limitações e medidas de proteção {#limitations-guardrails}

* O envio de onda se aplica somente a **ações de saída** (email, SMS, push, correspondência direta).
* Você deve definir pelo menos **2 ondas** e pode adicionar até **10 ondas**.
* O intervalo mínimo entre o início de duas ondas é de **30 minutos**.
* Um início de onda não pode ser anterior ao início da campanha ou no passado.

## Configurar envio de onda {#configure-wave-sending}

Para configurar como e quando enviar ondas em uma campanha, siga as etapas abaixo.

1. Crie ou abra uma [Campanha de ação](create-campaign.md) que contenha uma ação de saída (por exemplo, Email, SMS, Push).

1. Na guia **[!UICONTROL Agendar]** da campanha, selecione **[!UICONTROL Entregar ações de campanha em ondas]**.

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >A opção **[!UICONTROL Deliver campaign actions in waves]** só é exibida quando uma ação de saída é selecionada na guia **[!UICONTROL Actions]** da campanha. [Saiba mais](campaign-action.md)

1. Defina o número de ondas que deseja enviar (por exemplo, 4).

   >[!NOTE]
   >
   >Você deve definir pelo menos 2 ondas e pode adicionar até 10 ondas.

1. Escolha como definir o tamanho e o tempo da onda conforme detalhado abaixo.

### Ondas iguais {#equal-waves}

Por padrão, o público-alvo é dividido em ondas de tamanho igual. Agende a hora da primeira onda e defina um intervalo fixo entre o início de cada onda (por exemplo, 2 horas).

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>O intervalo mínimo entre o início de duas ondas é de **30 minutos**.

O sistema então agenda ondas subsequentes automaticamente (por exemplo, primeira onda às 9:00 AM, segunda às 11:00 AM, terceira às 1:00 PM, quarta às 3:00 PM).

### Distribuição personalizada {#custom-distribution}

Selecione a opção **[!UICONTROL Custom distribution]** para definir o tamanho de cada onda como uma porcentagem do público total (por exemplo, 15%, 20%, 25%, 40%).

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>O total em todas as ondas deve ser igual a 100%. Se esse não for o caso, uma mensagem de aviso será exibida.<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

Selecione **[!UICONTROL Números]** para definir o tamanho de cada onda como um número absoluto de perfis (por exemplo, 10.000; 50.000).

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>Ao usar números, o sistema não valida se a soma cobre todo o público-alvo. Você deve garantir que seus tamanhos de onda cubram o público-alvo para o qual você pretende enviar. Saiba mais nas [Perguntas frequentes](#faq).

### Agendamento personalizado {#custom-schedule}

Selecione **[!UICONTROL Agendar cada onda]** para definir uma data e hora de início específicas para cada onda. As ondas não precisam ter espaçamento uniforme (por exemplo, 9h00, 11h00, 17h00, 24h20, 20h30).:00:00:00:30

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>O intervalo mínimo entre o início de duas ondas é de **30 minutos**.

## Casos de uso {#use-cases}

O envio de onda ajuda você a controlar quando e quantas mensagens são enviadas, o que pode melhorar a capacidade de entrega, proteger a reputação do remetente e alinhar os envios à sua capacidade operacional. Considere usar ondas nestes cenários:

* **Call center ou gestor de resposta:** limite quantas mensagens saem por dia ou por hora para que as equipes downstream (por exemplo, atendimento ao cliente) possam lidar com as respostas. Por exemplo, envie 20 mensagens por dia para corresponder à capacidade da central de atendimento.

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **Alto volume e capacidade de entrega:** Evite enviar uma campanha muito grande de uma só vez. Espalhe a entrega ao longo do tempo para ajudar a manter a reputação do remetente e reduzir o risco de ser sinalizado como spam.

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **Aumento:** ao usar uma nova plataforma ou IP, aumente progressivamente o volume (por exemplo, 10% na primeira onda, depois 15%, 20% e assim por diante) para criar a reputação gradualmente.

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## Perguntas frequentes {#faq}

+++ O que acontece se a soma dos tamanhos de onda não for igual ao público total?

* Se a soma dos tamanhos das ondas **exceder** o público-alvo (por exemplo, você agendar 100.000 na primeira onda para um público-alvo de 100.000), a primeira onda enviará para o público-alvo completo e as ondas restantes não terão mais para enviar; elas não serão executadas.
* Se a soma **for menor** do que o público-alvo (por exemplo, você define quatro ondas totalizando 40.000 perfis para um público-alvo de 100.000), somente os perfis incluídos nessas ondas receberão a mensagem. O restante do público-alvo não receberá a comunicação e não será repetido em ondas posteriores.

+++

+++ Posso atribuir diferentes segmentos ou critérios a ondas individuais?

Você só pode definir o tamanho e o tempo das ondas. A seleção de recipients é a mesma para toda a campanha; não é possível atribuir segmentos ou critérios diferentes a ondas individuais.

+++

## Próximas etapas {#next}

* [Agendar a Campanha de ação](campaign-schedule.md) — definir data de início, data de término, frequência e controle de taxa.
* [Revise e ative a campanha](review-activate-campaign.md)—verifique a campanha e entre em produção.
