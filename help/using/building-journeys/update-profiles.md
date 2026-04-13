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
version: Journey Orchestration
source-git-commit: 5383e0af430188dadd3e9ee259253115f7f1992d
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 4%

---

# Atualizar perfil {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Atividade Atualizar perfil"
>abstract="A ação Atualizar perfil permite atualizar um perfil existente da [!DNL Adobe Experience Platform] com informações provenientes do evento, de uma fonte de dados ou usando um valor específico."

Use a atividade de ação **[!UICONTROL Atualizar Perfil]** para enriquecer ou corrigir um perfil [!DNL Adobe Experience Platform] existente à medida que um cliente avança em uma jornada. É possível definir valores de campo originados de um evento de jornada, uma fonte de dados configurada ou um valor estático — permitindo que você mantenha os dados do perfil precisos e acionáveis sem sair da tela de jornada. Antes de configurar esta atividade, leia as [medidas de proteção e limitações](#guardrails) aplicáveis.

## Seleção do conjunto de dados {#dataset-selection}

A atividade **[!UICONTROL Atualizar Perfil]** requer um conjunto de dados dedicado para armazenar atualizações. Como esta atividade atualiza apenas o [Repositório de Perfis](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"} (não o Datalake), todas as atualizações devem ser salvas em um [conjunto de dados habilitado para perfil](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} especificamente designado para as ações **[!UICONTROL Atualizar Perfil]**.

>[!CAUTION]
>
>Não use um conjunto de dados que também seja usado para assimilação em lote ou por transmissão. Outras execuções de assimilação substituirão as alterações feitas pela ação **[!UICONTROL Atualizar Perfil]**, fazendo com que os atributos de perfil desapareçam ou revertam para seus valores anteriores. Se você observar esse comportamento, verifique no Adobe Experience Platform se nenhuma outra assimilação está gravando no mesmo conjunto de dados. Para obter as etapas de solução de problemas, consulte [Resolvendo falhas de atualização de perfil no Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}.

Além disso, a configuração da atividade **[!UICONTROL Atualizar Perfil]** não requer um [namespace de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces){target="_blank"}. Dessa forma, verifique se o conjunto de dados selecionado usa o mesmo **[!UICONTROL namespace de identidade]** usado pela ação que iniciou a jornada, pois é esse namespace que essas atualizações usarão. O mapa de identidade também pode ser usado pelo conjunto de dados selecionado. Falha ao selecionar um conjunto de dados com o namespace de identidade correto ou um que usa o mapa de identidade causará a falha da atividade **[!UICONTROL Atualizar Perfil]**.

## Configurar a atividade de atualização de perfil {#use-profile-update}

Siga as etapas abaixo para configurar a atividade **[!UICONTROL Atualizar Perfil]** na sua jornada.

1. Comece a projetar sua jornada. Saiba mais em [Criar a primeira jornada](../building-journeys/journey-gs.md).

1. Na seção **[!UICONTROL Ação]** da paleta, solte a atividade **[!UICONTROL Atualizar Perfil]** na tela.

   ![Atualizar atividade de perfil na paleta de jornadas em Ações](assets/profileupdate0.png)

1. Selecione um esquema na lista.

   >[!NOTE]
   >
   >Somente os campos que já existem no esquema do Perfil XDM selecionado estão disponíveis para seleção. Se o campo necessário não estiver listado, adicione-o ao esquema no Adobe Experience Platform primeiro.

1. Clique em **[!UICONTROL Campo]** para selecionar o campo que deseja atualizar.

   ![Selecionando o campo a ser atualizado](assets/profileupdate2.png)

1. Selecione um conjunto de dados na lista.

   >[!NOTE]
   >
   >A ação **[!UICONTROL Atualizar Perfil]** atualiza os dados do perfil em tempo real, mas não atualiza os conjuntos de dados. A seleção do conjunto de dados é necessária, pois o perfil é um registro relacionado a um conjunto de dados.

1. Clique no campo **[!UICONTROL Value]** para definir o valor que você deseja usar:

   * Usando o editor de expressões simples, é possível selecionar um campo de uma fonte de dados ou do evento de entrada.

     ![Seletor de campo de modo simples para atualizações de atributo de perfil](assets/profileupdate4.png)

   * Para definir um valor específico ou aproveitar funções avançadas, selecione [**[!UICONTROL Modo avançado]**](expression/expressionadvanced.md).

     ![Editor de expressão de modo avançado para atualizações de perfil complexas](assets/profileupdate3.png)

1. Para atualizar atributos de perfil adicionais na mesma ação, clique em **[!UICONTROL Atualizar outro campo]** e repita a seleção de campo e valor. Você pode adicionar até cinco pares de campo/valor em uma única ação **[!UICONTROL Atualizar Perfil]**. Consulte [Medidas de proteção e limitações](#guardrails).

A atividade **[!UICONTROL Atualizar Perfil]** está configurada.

![Atividade de atualização de perfil no jornada com configuração de vários campos](assets/profileupdate1.png)


## Testar a atualização do perfil {#using-the-test-mode}

Esteja ciente de que no [modo de teste](testing-the-journey.md), as atualizações de perfil entram em vigor imediatamente no perfil de teste e não são simuladas.

Somente perfis de teste podem inserir uma jornada no modo de teste. Você pode criar um novo perfil de teste ou converter um perfil existente em um perfil de teste. No [!DNL Adobe Experience Platform], os atributos de perfil podem ser atualizados por uma importação de arquivo CSV ou chamadas de API. Uma alternativa mais rápida é usar uma atividade **[!UICONTROL Atualizar perfil]** dentro da própria jornada para definir o campo booleano do perfil de teste como verdadeiro.

Para obter mais informações sobre como transformar um perfil existente em um perfil de teste, consulte esta [seção](../audience/creating-test-profiles.md#create-test-profiles-csv).

## Medidas de proteção e limitações {#guardrails}

* A ação **[!UICONTROL Atualizar Perfil]** só pode ser usada em jornadas que tenham um [namespace](../event/about-creating.md#select-the-namespace).
* A ação atualiza apenas os campos existentes, não cria novos campos de perfil.
* A ação só oferece suporte a tipos de campos simples (sequência, número, booleano). Campos XDM definidos como enumerações, valores sugeridos, matrizes de objetos ou coleções complexas (por exemplo, listas de produtos) não são compatíveis.
* Você não pode usar a ação **[!UICONTROL Atualizar Perfil]** para gerar [eventos de experiência](../event/about-events.md), como uma compra.
* Como qualquer outra ação, você pode definir um [caminho alternativo em caso de erro ou tempo limite](using-the-journey-designer.md#paths). Duas ações não podem ser colocadas em paralelo.
* Não há garantias de que as atualizações de perfil estarão imediatamente disponíveis downstream na mesma jornada. Evite colocar uma ação que leia um campo diretamente após a ação **[!UICONTROL Atualizar Perfil]** que o grava, pois o valor atualizado pode não ser refletido ainda.
* A atividade **[!UICONTROL Atualizar perfil]** atualiza somente o [Repositório de Perfis](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, não o Data Lake.
* Até cinco pares de campo/valor podem ser atualizados em uma única ação **[!UICONTROL Atualizar Perfil]**. Use o botão **[!UICONTROL Atualizar outro campo]** para adicionar mais pares.
* Para obter um melhor desempenho, agrupe várias atualizações de atributo em uma única ação **[!UICONTROL Atualizar Perfil]** em vez de usar uma ação por atributo.
