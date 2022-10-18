---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciamento de fuso horário
description: Saiba mais sobre o gerenciamento de fuso horário
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 2%

---

# Gerenciamento de fuso horário {#timezone_management}

Você pode definir um fuso horário na variável [propriedades](../building-journeys/journey-gs.md#change-properties) da sua jornada.

Para acessar as Propriedades da Jornada, clique no ícone de lápis na parte superior direita da tela.

Esse fuso horário será usado para cada atividade da jornada que contém um elemento de hora, como:

* [Condição de tempo](../building-journeys/condition-activity.md#time_condition)
* [Condição de data](../building-journeys/condition-activity.md#date_condition)
* [Aguardar personalizado](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Você pode selecionar um fuso horário ou optar por usar o fuso horário definido no perfil do usuário.

>[!NOTE]
>
>O fuso horário do perfil funciona com a variável **timeZone** existente na variável **Detalhes da Preferência** grupo de campos.

## Definir um fuso horário fixo {#fixed-timezone}

O fuso horário também pode ser corrigido. Limpe o fuso horário predefinido e escolha um na lista suspensa. Se você usar um fuso horário fixo, será o mesmo para todos os indivíduos que inseriram a jornada.

Para fazer isso, no **[!UICONTROL Propriedades da Jornada]** selecione um fuso horário.

![](assets/journey72.png)

## Usar perfis para definir o fuso horário da jornada {#timezone-from-profiles}

Se o evento de entrada da jornada tiver um namespace, o que significa que a jornada pode acessar o serviço de Perfil do cliente em tempo real do Adobe Experience Platform, você pode usar o fuso horário definido no nível do perfil. Para fazer isso, em **Propriedades**, verificar **Usar o fuso horário do perfil em esperas e condições**. Essa opção não está marcada por padrão.

Se um fuso horário tiver sido definido para um perfil, ele será recuperado e usado pela jornada. Caso contrário, o fuso horário usado será o definido no campo de fuso horário.

![](assets/journey73.png)

## Usar fusos horários em expressões {#timezone-in-expressions}

As datas de início e término de uma jornada não podem ser vinculadas a um fuso horário específico. Eles são associados automaticamente ao fuso horário da instância.
