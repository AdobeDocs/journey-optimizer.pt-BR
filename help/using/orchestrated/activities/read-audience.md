---
solution: Journey Optimizer
product: journey optimizer
title: Usar a atividade Público-alvo de leitura
description: Saiba como usar a atividade Ler público em uma campanha orquestrada
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 16%

---


# Público-alvo de leitura {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Atividade Criar público-alvo"
>abstract="A Atividade **Público-alvo de leitura** permite selecionar o público-alvo que entrará na campanha orquestrada. Esse público-alvo pode ser um público-alvo existente da Adobe Experience Platform ou um público-alvo extraído de um arquivo CSV. Ao enviar mensagens no contexto de uma campanha orquestrada, o público-alvo da mensagem não é definido na atividade do canal, mas em uma atividade **Público-alvo de leitura** ou **Criar público-alvo**."

A atividade **[!UICONTROL Ler público-alvo]** permite recuperar um público-alvo existente, salvo ou importado anteriormente, e reutilizá-lo em uma campanha Orquestrada. Essa atividade é especialmente útil para direcionar um conjunto predefinido de perfis sem a necessidade de executar um novo processo de segmentação.

Depois que o público-alvo é carregado, você pode refiná-lo selecionando um campo de identidade exclusivo e enriquecendo o público-alvo com atributos de perfil adicionais para fins de direcionamento, personalização ou relatórios.

## Configurar a atividade Ler público {#read-audience-configuration}

Siga estas etapas para configurar a atividade **[!UICONTROL Ler público-alvo]**:

1. Antes de adicionar a atividade **[!UICONTROL Ler público-alvo]**, selecione uma **[!UICONTROL política de mesclagem]** nas configurações do Campaign.

   ![](../assets/read-audience-6.png)

1. Adicione uma atividade **[!UICONTROL Read audience]** à sua campanha Orquestrada.

   ![](../assets/read-audience-1.png)

1. Insira um **[!UICONTROL Rótulo]** para sua atividade. Esse rótulo servirá como o nome do público-alvo.

1. Clique em ![ícone de pesquisa de pasta](../assets/do-not-localize/folder-search.svg) para selecionar o público-alvo que deseja direcionar para sua campanha orquestrada.

   ![](../assets/read-audience-2.png)

1. Escolha uma **[!UICONTROL Entidade&#x200B;]** na Targeting dimension do Campaign. Essa configuração define a entidade de público-alvo e o atributo usado para reconciliar o público-alvo com o target dimension.

   ➡️ [Siga as etapas detalhadas nesta página para criar sua dimensão de Direcionamento de Campanha](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Selecione [!UICONTROL Adicionar atributo] para enriquecer o público-alvo selecionado com dados adicionais. Esta etapa permite adicionar atributos de perfil ao público-alvo, resultando em uma lista de recipients aprimorada com esses atributos.

1. Escolha os **[!UICONTROL Atributos]** que você deseja adicionar ao seu público-alvo. O seletor de atributos exibe campos do **Esquema de Perfil de União**:

   * Para públicos baseados em CSV, isso inclui atributos de **Perfil** e atributos de nível de público personalizados. Esses atributos podem ser encontrados no seguinte caminho de esquema:

     `<audienceid> > _ajobatchjourneystage > audienceEnrichment > CustomerAudienceUpload > <audienceid>`

   * Para públicos-alvo padrão do AEP, somente os atributos **Perfil** estão disponíveis, pois não apresentam campos específicos de público-alvo inseridos.

   >[!NOTE]
   >
   > Embora alguns atributos possam aparecer no seletor, sua disponibilidade no tempo de execução depende de os dados do público-alvo terem sido reconciliados e mesclados com êxito com o **Perfil do Adobe Experience Platform**.

   ![](../assets/read-audience-4.png)

Depois que um público-alvo é criado, ele é disponibilizado em modo somente leitura e não pode mais ser editado. Ele só poderá ser usado depois que o processo de criação for totalmente concluído.

## Exemplo

No exemplo abaixo, a atividade **[!UICONTROL Ler público-alvo]** é usada para recuperar um público-alvo criado e salvo anteriormente de perfis que assinaram o boletim informativo. O público-alvo é então enriquecido com o atributo **Loyalty subscription** para habilitar o direcionamento de usuários que são membros registrados do programa de fidelidade.

![](../assets/read-audience-5.png)
