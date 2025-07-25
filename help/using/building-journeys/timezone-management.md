---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de fuso horário
description: Saiba mais sobre o gerenciamento de fuso horário
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: time zone, properties, jornada, condition, time, date, custom
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 28%

---

# Gerenciamento de fuso horário {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Fuso Horário"
>abstract="Selecione o fuso horário da jornada. Ao usar um horário fixo, será definido o mesmo fuso para todas as pessoas que entram na jornada."


Você pode definir um fuso horário nas [propriedades](../building-journeys/journey-properties.md#timezone) da jornada.

Para acessar as propriedades da jornada, selecione o ícone de lápis na parte superior direita da tela.

Esse fuso horário será usado para cada atividade da jornada que contém um elemento de tempo, como:

* [Condição de tempo](../building-journeys/condition-activity.md#time_condition)
* [Condição de data](../building-journeys/condition-activity.md#date_condition)
* [Espera personalizada](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Você pode selecionar um [fuso horário fixo](#fixed-timezone) ou optar por usar o fuso horário [definido no perfil do usuário](#timezone-from-profiles).

## Definir um fuso horário fixo {#fixed-timezone}

O fuso horário pode ser corrigido. Limpe o fuso horário predefinido e escolha um na lista suspensa. Se você usar um fuso horário fixo, ele será o mesmo para todos os indivíduos que entram na jornada.

Para fazer isso, no painel **[!UICONTROL Propriedades de Jornada]**, selecione um fuso horário.

![](assets/journey72.png)

## Usar fuso horário de perfis {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Usar fuso horário do perfil"
>abstract="Marque a caixa para usar o fuso horário do perfil em tempo real em atividades de espera e de condição. Se um fuso horário tiver sido definido para um perfil, ele será recuperado e usado pela jornada. Caso contrário, o fuso horário será aquele definido no campo fuso horário acima."

Se o evento de entrada da jornada tiver um namespace, o que significa que a jornada pode acessar o serviço de Perfil do cliente em tempo real do Adobe Experience Platform, você pode usar o fuso horário definido no nível do perfil. Para fazer isso, em **Propriedades**, marque **Usar fuso horário do perfil em esperas e condições**. Essa opção não está marcada por padrão.

Se um fuso horário tiver sido definido para um perfil, ele será recuperado e usado pela jornada. Caso contrário, o fuso horário usado será aquele definido no campo timezone.

![](assets/journey73.png)

>[!NOTE]
>
>O fuso horário do perfil funciona com o campo **timeZone** existente no grupo de campos **Detalhes da Preferência**.

## Usar fusos horários em expressões {#timezone-in-expressions}

As datas de início e término de uma jornada não podem ser vinculadas a um fuso horário específico. Eles são associados automaticamente ao fuso horário da instância.
