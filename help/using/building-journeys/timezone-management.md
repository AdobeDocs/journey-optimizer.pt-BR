---
title: Gerenciamento de fuso horário
description: Saiba mais sobre o gerenciamento de fuso horário
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 2%

---

# Gerenciamento de fuso horário {#timezone_management}

Você pode definir um fuso horário na variável [propriedades](../building-journeys/journey-gs.md#change-properties) da sua jornada.

Para acessar Propriedades, clique no ícone de lápis na parte superior direita da tela.

Esse fuso horário será usado para cada atividade da jornada que contém um elemento de hora, como:

* [Condição de tempo](../building-journeys/condition-activity.md#time_condition)
* [Condição de data](../building-journeys/condition-activity.md#date_condition)
* [Aguardar personalizado](../building-journeys/wait-activity.md#custom)
* [Data de espera fixa](../building-journeys/wait-activity.md#fixed_date)

Você pode selecionar um fuso horário ou optar por usar o fuso horário definido no perfil do usuário.

>[!NOTE]
>
>O fuso horário do perfil funciona com a variável **timeZone** existente na variável **Detalhes da Preferência** grupo de campos.

## Definição de fuso horário fixo {#fixed-timezone}

O fuso horário também pode ser corrigido. Limpe o fuso horário predefinido e escolha um na lista suspensa. Se você usar um fuso horário fixo, será o mesmo para todos os indivíduos que inseriram a jornada.

Para fazer isso, no **[!UICONTROL Journey Properties]** selecione um fuso horário.

![](assets/journey72.png)

## Uso de perfis para definir o fuso horário da jornada {#timezone-from-profiles}

Se o evento de entrada da jornada tiver um namespace, o que significa que a jornada pode acessar o serviço de Perfil do cliente em tempo real do Adobe Experience Platform, o fuso horário será predefinido com o especificado no perfil do indivíduo que flui na jornada.

Se um fuso horário for definido no perfil do Adobe Experience Platform, ele poderá ser recuperado na jornada.

Se o perfil do indivíduo não contiver um fuso horário, o fuso horário recuperado será aquele definido no campo timezone.

Para fazer isso, em **[!UICONTROL Properties]**, verificar **[!UICONTROL Use Profile timezone in waits and conditions]**.

![](assets/journey73.png)

## Uso de fusos horários em expressões {#timezone-in-expressions}

As datas de início e término de uma jornada não podem ser vinculadas a um fuso horário específico. Eles são associados automaticamente ao fuso horário da instância.
