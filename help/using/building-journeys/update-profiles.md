---
solution: Journey Optimizer
product: journey optimizer
title: Atualizar perfil
description: Saiba como usar a atividade Atualizar perfil em uma jornada
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: perfil, atualização, jornada, atividade
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 6%

---

# Atualizar perfil {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Atividade Atualizar perfil"
>abstract="A ação Atualizar perfil permite atualizar um perfil da Adobe Experience Platform existente com informações provenientes do evento, de uma fonte de dados ou usando um valor específico."

Use a atividade de ação **[!UICONTROL Atualizar Perfil]** para atualizar um perfil do Adobe Experience Platform existente com informações provenientes de um evento, uma fonte de dados ou com um valor específico.

## Principais conceitos {#key-concepts}

* A ação **Atualizar Perfil** só pode ser usada em jornadas que tenham um namespace.
* A ação atualiza apenas os campos existentes, não cria novos campos de perfil.
* Você não pode usar a ação **Atualizar Perfil** para gerar eventos de experiência, por exemplo, uma compra.
* Como qualquer outra ação, é possível definir um caminho alternativo em caso de erro ou tempo limite, e não é possível colocar duas ações em paralelo.
* A solicitação de atualização enviada para o Adobe Experience Platform é imediata/em um segundo. Normalmente, levará alguns segundos, mas às vezes mais, sem garantia. Como resultado, por exemplo, se uma ação estiver usando o &quot;campo 1&quot; atualizado por uma ação **Atualizar perfil** posicionada logo antes, você não deve esperar que o &quot;campo 1&quot; seja atualizado na ação.
* A atividade **Atualizar perfil** não oferece suporte a campos XDM definidos como enumerações ou valores sugeridos.
* A atividade **[!UICONTROL Atualizar perfil]** atualiza somente o [Repositório de Perfis](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, não o Data Lake.

## Seleção do conjunto de dados {#dataset-selection}

A atividade **Atualizar Perfil** requer um conjunto de dados dedicado para armazenar atualizações. Como esta atividade atualiza apenas o repositório de Perfis (não o Datalake), todas as atualizações devem ser salvas em um conjunto de dados habilitado para perfil designado especificamente para as ações **Atualizar Perfil**. Usar um conjunto de dados usado para assimilação em lote ou por streaming resultará na substituição dos dados recém-integrados pelas alterações feitas pela ação **Atualizar Perfil**.

Além disso, a configuração da atividade **Atualizar Perfil** não requer um namespace de identidade. Dessa forma, verifique se o conjunto de dados selecionado usa o mesmo **namespace de identidade** usado pela ação que iniciou a jornada, pois é esse namespace que essas atualizações usarão. O mapa de identidade também pode ser usado pelo conjunto de dados selecionado. Se você não selecionar um conjunto de dados com o namespace correto ou um que use o mapa de identidade, a atividade Atualizar perfil falhará.

## Uso da atualização de perfil

1. Projete sua jornada iniciando com um evento. Consulte esta [seção](../building-journeys/journey.md).

1. Na seção **Ação** da paleta, solte a atividade **Atualizar Perfil** na tela.

   ![](assets/profileupdate0.png)

1. Selecione um esquema na lista.

1. Clique em **Campo** para selecionar o campo que deseja atualizar. Somente um campo pode ser selecionado.

   ![](assets/profileupdate2.png)

1. Selecione um conjunto de dados na lista.

   >[!NOTE]
   >
   >A ação **Atualizar Perfil** atualiza os dados do perfil em tempo real, mas não atualiza os conjuntos de dados. A seleção do conjunto de dados é necessária, pois o perfil é um registro relacionado a um conjunto de dados.

1. Clique no campo **Value** para definir o valor que você deseja usar:

   * Usando o editor de expressões simples, é possível selecionar um campo de uma fonte de dados ou do evento de entrada.

     ![](assets/profileupdate4.png)

   * Para definir um valor específico ou aproveitar funções avançadas, selecione **Modo avançado**.

     ![](assets/profileupdate3.png)

O **Perfil de Atualização** está configurado agora.

![](assets/profileupdate1.png)


## Uso do modo de teste {#using-the-test-mode}

No modo de teste, a atualização do perfil não será simulada. A atualização será executada no perfil de teste.

Somente perfis de teste podem inserir uma jornada no modo de teste. Você pode criar um novo perfil de teste ou transformar um perfil existente em um perfil de teste. No Adobe Experience Platform, você pode atualizar atributos de perfis por meio de uma importação de arquivo csv ou chamadas de API. Um método mais simples é usar uma atividade de ação **Atualizar perfil** e alterar o campo booleano do perfil de teste de falso para verdadeiro.

Para obter mais informações sobre como transformar um perfil existente em um perfil de teste, consulte esta [seção](../audience/creating-test-profiles.md#create-test-profiles-csv).
