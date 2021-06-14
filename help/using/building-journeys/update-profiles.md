---
title: Atualizar perfil
description: Saiba como usar a atividade Update profile em um jornada
feature: Jornadas
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: 70d3bdaeec2a7a8f282b0e1a79bc751f7f837663
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---

# Atualizar perfil {#update-profile}

![](../assets/do-not-localize/badge.png)

A atividade de ação **[!UICONTROL Update profile]** permite atualizar um perfil do Adobe Experience Platform existente com informações provenientes do evento, uma fonte de dados ou usando um valor específico.

## Observações importantes

* A ação **Atualizar perfil** só pode ser usada em jornadas que comecem com um evento que tenha um namespace.
* A ação atualiza apenas os campos existentes, mas não cria novos campos de perfil.
* Você não pode usar a ação **Atualizar perfil** para gerar eventos de experiência, por exemplo, uma compra.
* Assim como qualquer outra ação, você pode definir um caminho alternativo em caso de erro ou tempo limite e não pode colocar duas ações em paralelo.
* A solicitação de atualização enviada para a Platform será rápida, mas não imediata/dentro de um segundo. Em geral, levará alguns segundos, mas às vezes mais sem garantia. Como resultado, por exemplo, se uma ação estiver usando um &quot;campo 1&quot; atualizado por uma ação Atualizar perfil posicionada anteriormente, você não deve esperar que o &quot;campo 1&quot; seja atualizado na ação.
* As fontes de dados têm uma noção da duração do cache, no nível do grupo de campos. Se você espera aproveitar, em uma jornada, um campo de perfil atualizado recentemente, tenha cuidado para definir uma duração de cache muito curta.

## Uso do modo de teste {#using-the-test-mode}

No modo de teste, a atualização do perfil não será simulada. A atualização será executada no perfil de teste.

Somente perfis de teste podem inserir uma jornada no modo de teste. Você pode criar um novo perfil de teste ou transformar um perfil existente em um perfil de teste. Na Adobe Experience Platform, você pode atualizar atributos de perfil por meio de uma importação de arquivo csv ou chamadas de API. Um método mais simples é usar uma atividade de ação **Update profile** e alterar o campo booleano do perfil de teste de false para true.

Para obter mais informações sobre como transformar um perfil existente em um perfil de teste, consulte esta [seção](../building-journeys/creating-test-profiles.md#create-test-profiles-csv).

## Usar a atualização de perfil

1. Crie a jornada começando com um evento. Consulte esta [seção](../building-journeys/journey.md).

1. Na seção **Action** da paleta, solte a atividade **Update profile** na tela.

   ![](../assets/profileupdate0.png)

1. Selecione um schema na lista.

1. Clique em **Fields** para selecionar o campo que deseja atualizar. Somente um campo pode ser selecionado.

   ![](../assets/profileupdate2.png)

1. Selecione um conjunto de dados na lista.

   >[!NOTE]
   >
   >A ação **Atualizar perfil** atualiza os dados do perfil em tempo real, mas não atualiza os conjuntos de dados. A seleção do conjunto de dados é necessária, pois o perfil é um registro relacionado a um conjunto de dados.

1. Clique no campo **Value** para definir o valor que deseja usar:

   * Usando o editor de expressão simples, é possível selecionar um campo de uma fonte de dados ou do evento de entrada.

      ![](../assets/profileupdate4.png)

   * Se desejar definir um valor específico ou aproveitar funções avançadas, clique em **Modo avançado**.

      ![](../assets/profileupdate3.png)

O **Atualizar perfil** agora está configurado.

![](../assets/profileupdate1.png)
