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
TQID: https://experienceleague.adobe.com/ifDBXoNDryXLKMkm59mVqT7-unQYG1JKTfMN7zAoWsA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1491
ht-degree: 4%

---

# Atualizar perfil {#update-profile}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como usar a atividade de ação Atualizar Perfil para enriquecer ou corrigir um perfil existente do Adobe Experience Platform à medida que um cliente avança em uma jornada.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Atividade Atualizar perfil"
>abstract="A ação Atualizar perfil permite atualizar um perfil existente da [!DNL Adobe Experience Platform] com informações provenientes do evento, de uma fonte de dados ou usando um valor específico."

Use a atividade de ação **[!UICONTROL Atualizar Perfil]** para enriquecer ou corrigir um perfil [!DNL Adobe Experience Platform] existente à medida que um cliente avança em uma jornada. É possível definir valores de campo originados de um evento de jornada, uma fonte de dados configurada ou um valor estático — permitindo que você mantenha os dados do perfil precisos e acionáveis sem sair da tela de jornada. Antes de configurar esta atividade, leia as [medidas de proteção e limitações](#guardrails) aplicáveis.

## Seleção do conjunto de dados {#dataset-selection}

A atividade **[!UICONTROL Atualizar Perfil]** requer um conjunto de dados dedicado para armazenar atualizações. Como esta atividade atualiza apenas o [Repositório de Perfis](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR#profile-data-store){target="_blank"} (não o Datalake), todas as atualizações devem ser salvas em um [conjunto de dados habilitado para perfil](https://experienceleague.adobe.com/pt-br/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} especificamente designado para as ações **[!UICONTROL Atualizar Perfil]**.

>[!CAUTION]
>
>Não use um conjunto de dados que também seja usado para assimilação em lote ou por transmissão. Outras execuções de assimilação substituirão as alterações feitas pela ação **[!UICONTROL Atualizar Perfil]**, fazendo com que os atributos de perfil desapareçam ou revertam para seus valores anteriores. Se você observar esse comportamento, verifique no Adobe Experience Platform se nenhuma outra assimilação está gravando no mesmo conjunto de dados. Para obter as etapas de solução de problemas, consulte [Resolvendo falhas de atualização de perfil no Adobe Journey Optimizer](https://experienceleague.adobe.com/pt-br/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}.

Além disso, a configuração da atividade **[!UICONTROL Atualizar Perfil]** não requer um [namespace de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces){target="_blank"}. Dessa forma, verifique se o conjunto de dados selecionado usa o mesmo **[!UICONTROL namespace de identidade]** usado pela ação que iniciou a jornada, pois é esse namespace que essas atualizações usarão. O mapa de identidade também pode ser usado pelo conjunto de dados selecionado. Falha ao selecionar um conjunto de dados com o namespace de identidade correto ou um que usa o mapa de identidade causará a falha da atividade **[!UICONTROL Atualizar Perfil]**.

## Configurar a atividade de atualização do perfil {#use-profile-update}

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

Somente perfis de teste podem entrar em uma jornada no modo de teste. Você pode criar um novo perfil de teste ou converter um perfil existente em um perfil de teste. No [!DNL Adobe Experience Platform], os atributos de perfil podem ser atualizados por uma importação de arquivo CSV ou chamadas de API. Uma alternativa mais rápida é usar uma atividade **[!UICONTROL Atualizar perfil]** dentro da própria jornada para definir o campo booleano do perfil de teste como verdadeiro.

Para obter mais informações sobre como transformar um perfil existente em um perfil de teste, consulte esta [seção](../audience/creating-test-profiles.md#create-test-profiles-csv).

## Medidas de proteção e limitações {#guardrails}

* A ação **[!UICONTROL Atualizar Perfil]** só pode ser usada em jornadas que tenham um [namespace](../event/about-creating.md#select-the-namespace).
* A ação atualiza apenas os campos existentes, não cria novos campos de perfil.
* A ação só oferece suporte a tipos de campos simples (sequência, número, booleano). Campos XDM definidos como enumerações, valores sugeridos, matrizes de objetos ou coleções complexas (por exemplo, listas de produtos) não são compatíveis.
* Você não pode usar a ação **[!UICONTROL Atualizar Perfil]** para gerar [eventos de experiência](../event/about-events.md), como uma compra.
* Como qualquer outra ação, você pode definir um [caminho alternativo em caso de erro ou tempo limite](using-the-journey-designer.md#paths). Duas ações não podem ser colocadas em paralelo.
* Não há garantias de que as atualizações de perfil estarão imediatamente disponíveis downstream na mesma jornada. Evite colocar uma ação que leia um campo diretamente após a ação **[!UICONTROL Atualizar Perfil]** que o grava, pois o valor atualizado pode não ser refletido ainda.
* A atividade **[!UICONTROL Atualizar perfil]** atualiza somente o [Repositório de Perfis](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR#profile-data-store){target="_blank"}, não o Data Lake.
* Até cinco pares de campo/valor podem ser atualizados em uma única ação **[!UICONTROL Atualizar Perfil]**. Use o botão **[!UICONTROL Atualizar outro campo]** para adicionar mais pares.
* Para obter um melhor desempenho, agrupe várias atualizações de atributo em uma única ação **[!UICONTROL Atualizar Perfil]** em vez de usar uma ação por atributo.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página explica como configurar a atividade Atualizar Perfil para enriquecer ou corrigir um perfil do Adobe Experience Platform existente com dados de eventos de jornada, fontes de dados ou valores estáticos à medida que um cliente avança em uma jornada.

**Intenções:**

* Configure a atividade Atualizar perfil para modificar atributos de perfil existentes durante uma jornada
* Selecionar um conjunto de dados habilitado para perfil dedicado às ações Atualizar perfil
* Mapear valores de campo de eventos de jornada, fontes de dados ou valores estáticos para atributos de perfil
* Atualizar vários atributos de perfil (até cinco) em uma única atividade
* Atualizações de perfil de teste no modo de teste do jornada

**Glossário:**

* **Atualizar atividade do perfil**: uma atividade de ação que grava novos valores em campos existentes em um perfil do Adobe Experience Platform em tempo real, conforme um perfil passa por uma jornada *(específico do produto)*
* **Repositório de Perfis**: o repositório da Adobe Experience Platform que armazena dados de perfil do cliente em tempo real, distintos do Data Lake *(específico do produto)*
* **Namespace de identidade**: um rótulo que distingue contextos de identidade (por exemplo, email, ID de CRM) usados para corresponder ao perfil que está sendo atualizado *(específico do produto)*
* **Conjunto de dados habilitado para perfil**: um conjunto de dados Adobe Experience Platform configurado para contribuir com registros para o perfil unificado *(específico do produto)*

**Medidas de Proteção:**

* A ação Atualizar Perfil só pode ser usada em jornadas que tenham um namespace definido.
* A ação atualiza apenas campos XDM existentes; não é possível criar novos campos de perfil.
* Somente tipos de campos simples são suportados (string, número, booleano); enumerações, arrays de objetos e coleções complexas não são suportados.
* A ação não pode gerar eventos de experiência como compras.
* Até cinco pares de campo/valor podem ser atualizados em uma única ação Atualizar perfil.
* Não compartilhe o conjunto de dados dedicado com processos de assimilação em lote ou por transmissão, pois outras execuções de assimilação substituirão as alterações no Perfil de atualização.
* As atualizações de perfil podem não estar imediatamente disponíveis downstream na mesma execução da jornada.
* A atividade atualiza somente o Repositório de perfis, não o Data Lake.

**Terminologia:**

* Nome canônico: Atualizar Perfil — Acrônimo: none — variantes: Atualizar atividade do perfil, Atualizar ação do perfil
* Sinônimos: &quot;Loja de perfis&quot; = &quot;Loja de perfis do cliente em tempo real&quot;
* Não confunda: &quot;Armazenamento de perfis&quot; (atualizado por esta atividade) ≠ &quot;Data Lake&quot; (não atualizado por esta atividade)

**Perguntas frequentes:**

* **P: A atividade Atualizar Perfil pode criar novos campos de perfil?** — Não, ele só pode atualizar campos que já existem no esquema de perfil XDM selecionado.
* **P: Por que devo usar um conjunto de dados dedicado para ações de Atualização de Perfil?** — Compartilhar o conjunto de dados com assimilação em lote ou por transmissão pode fazer com que outras execuções de assimilação substituam as alterações feitas pela atividade Atualizar perfil.
* **P: As atualizações de perfil estão imediatamente visíveis para atividades downstream na mesma jornada?** — Não, os valores atualizados podem não ser refletidos ainda se uma ação ler o mesmo campo imediatamente após a atividade Atualizar perfil grava-o.
* **P: Quantos campos posso atualizar em uma única ação Atualizar Perfil?** — Até cinco pares de campo/valor podem ser configurados em uma única atividade usando o botão &quot;Atualizar outro campo&quot;.
* **P: As atualizações de perfil se aplicam ao modo de teste?** — Sim, no modo de teste, as atualizações entram em vigor imediatamente no perfil de teste e não são simuladas.

+++
