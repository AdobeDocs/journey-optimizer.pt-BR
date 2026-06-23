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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 996
ht-degree: 8%

---

# Gerenciamento de fuso horário {#timezone_management}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba como definir o fuso horário de uma jornada — um fuso horário fixo ou um obtido de cada perfil — para controlar quando as atividades baseadas em tempo, como condições de tempo, condições de data e esperas personalizadas, são executadas.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Fuso horário da jornada"
>abstract="A configuração de fuso horário define o fuso horário da jornada. Ao usar um horário fixo, será definido o mesmo fuso para todas as pessoas que entram na jornada."


Você pode definir um fuso horário nas [propriedades](../building-journeys/journey-properties.md#timezone) da jornada.

Para acessar as propriedades da jornada, selecione o ícone de lápis na parte superior direita da tela.

Esse fuso horário será usado para cada atividade da jornada que contém um elemento de tempo, como:

* [Condição de tempo](../building-journeys/conditions.md#time_condition)
* [Condição de data](../building-journeys/conditions.md#date_condition)
* [Espera personalizada](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Você pode selecionar um [fuso horário fixo](#fixed-timezone) ou optar por usar o fuso horário [definido no perfil do usuário](#timezone-from-profiles).

## Definir um fuso horário fixo {#fixed-timezone}

O fuso horário pode ser corrigido. Limpe o fuso horário predefinido e escolha um na lista suspensa. Se você usar um fuso horário fixo, ele será o mesmo para todos os indivíduos que entram na jornada.

Para fazer isso, no painel **[!UICONTROL Propriedades de Jornada]**, selecione um fuso horário.

![Lista suspensa de seleção de fuso horário nas propriedades da jornada](assets/journey72.png)

## Usar fuso horário do perfil {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Usar fuso horário do perfil"
>abstract="Esta opção usa o fuso horário do perfil em tempo real nas atividades **Espera** e **Condição**. Se um fuso horário foi definido para um perfil, ele será recuperado e usado na jornada. Caso contrário, o fuso horário será aquele definido no campo de fuso acima."

Se o evento de entrada da jornada tiver um namespace, o que significa que a jornada pode acessar o serviço de Perfil de Cliente em Tempo Real do [!DNL Adobe Experience Platform], talvez você queira usar o fuso horário definido no nível do perfil. Para fazer isso, em **Propriedades**, marque **Usar fuso horário do perfil em esperas e condições**. Essa opção não está marcada por padrão.

Se um fuso horário tiver sido definido para um perfil, ele será recuperado e usado pela jornada. Caso contrário, o fuso horário usado é o definido no campo Time zone.

![Configuração de fuso horário do perfil em fontes de dados para tempo personalizado](assets/journey73.png)

>[!NOTE]
>
>O fuso horário do perfil funciona com o campo **timeZone** existente no grupo de campos **Detalhes da Preferência**.

## Usar fusos horários em expressões {#timezone-in-expressions}

As datas de início e término de uma jornada não podem ser vinculadas a um fuso horário específico. Eles são associados automaticamente ao fuso horário da instância.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** Esta página explica como definir as configurações de fuso horário nas propriedades do Adobe Journey Optimizer jornada, escolhendo entre um fuso horário fixo aplicado a todos os perfis ou um fuso horário por perfil originado no Perfil de Cliente em Tempo Real.

**Intenções:**
* Defina um fuso horário fixo em uma jornada para que todos os perfis sigam a mesma referência de tempo para condições e esperas
* Ative o fuso horário por perfil para que as atividades Aguardar e Condição usem a preferência de fuso horário armazenado de cada indivíduo
* Entenda quais atividades de jornada são afetadas pela configuração de fuso horário da jornada
* Identificar o grupo de campos de perfil que armazena o valor de fuso horário individual

**Glossário:**
* **Fuso horário fixo**: um único fuso horário selecionado nas Propriedades de Jornada que se aplica uniformemente a cada perfil que entra na jornada *(específico do produto)*
* **Fuso horário do perfil**: o fuso horário individual armazenado no campo `timeZone` do grupo de campos Detalhes da Preferência, usado quando a opção &quot;Usar fuso horário do perfil em esperas e condições&quot; está habilitada *(específico do produto)*
* **Grupo de campos de Detalhes da Preferência**: o grupo de campos XDM que contém o atributo `timeZone` usado para a resolução de fuso horário no nível do perfil

**Medidas de Proteção:**
* A opção &quot;Usar fuso horário do perfil em esperas e condições&quot; só estará disponível quando o evento de entrada da jornada tiver um namespace (ou seja, a jornada pode acessar o serviço de Perfil do cliente em tempo real)
* A opção não está marcada por padrão; o fuso horário fixo é usado, a menos que explicitamente habilitado
* Se a opção estiver ativada, mas nenhum fuso horário estiver definido no perfil, a jornada voltará para o fuso horário fixo definido nas propriedades da jornada
* As datas de início e término da jornada não podem ser vinculadas a um fuso horário específico; elas são associadas automaticamente ao fuso horário da instância

**Terminologia:**
* Nome canônico: Gerenciamento de fuso horário — Acrônimo: none — variantes: configuração de fuso horário, fuso horário de jornada
* Sinônimos: &quot;fuso horário fixo&quot; = &quot;igual para todos os indivíduos&quot;; &quot;fuso horário do perfil&quot; = &quot;Usar fuso horário do perfil em esperas e condições&quot;
* Não confunda: &quot;Fuso horário da jornada&quot; (aplica-se a atividades) ≠ &quot;fuso horário da instância&quot; (aplica-se às datas de início/término da jornada, definidas automaticamente)

**Perguntas frequentes:**
* **P: Onde posso definir o fuso horário de uma jornada?** — No painel Propriedades da Jornada, acessível por meio do ícone de lápis na parte superior direita da tela de jornada.
* **P: Quais atividades usam o fuso horário da jornada?** — Condições de tempo, condições de data e atividades personalizadas de espera.
* **P: Como faço para que cada perfil siga seu próprio fuso horário local?** — Em Propriedades de Jornada, ative a opção &quot;Usar fuso horário do perfil em esperas e condições&quot;. Isso requer que a jornada tenha um namespace para que possa alcançar o serviço de Perfil do cliente em tempo real.
* **P: O que acontece se um perfil não tiver fuso horário definido e a opção de fuso horário do perfil estiver habilitada?** — A jornada retorna ao fuso horário fixo definido no campo fuso horário em Propriedades da Jornada.
* **P: Qual campo de perfil armazena o fuso horário do indivíduo?** — O campo `timeZone` no grupo de campos Detalhes da Preferência no esquema de perfil.
* **P: Posso definir as datas de início e término da jornada para um fuso horário específico?** — Não. As datas de início e término da jornada são associadas automaticamente ao fuso horário da instância e não podem ser vinculadas a um fuso horário personalizado.

+++
