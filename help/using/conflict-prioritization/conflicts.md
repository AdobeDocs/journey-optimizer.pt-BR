---
title: Exibir possíveis conflitos em jornadas e campanhas
description: Saiba como identificar possíveis conflitos em jornadas e campanhas.
role: User
level: Beginner
badge: label="Disponibilidade limitada"
source-git-commit: 4ab4b48ba87c73552a15c9815877517934029d57
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 7%

---


# Detectar possíveis conflitos em jornadas e campanhas {#conflict}

>[!AVAILABILITY]
>
>Os recursos de conflito e priorização estão atualmente disponíveis em Disponibilidade limitada para um grupo selecionado de clientes. Observe que esses recursos serão lançados de forma gradual para mais usuários no futuro. Entre em contato com a equipe de conta se tiver interesse em participar da lista de espera desses recursos.

À medida que os profissionais de marketing aumentam o volume de Campanhas e Jornadas no Journey Optimizer, fica cada vez mais difícil para um profissional de marketing saber se estão bombardeando seus clientes com muitas interações de marketing. portanto, é essencial identificar facilmente quando há campanhas e jornadas sobrepostas para garantir que elas estejam alcançando o equilíbrio certo de comunicações de marketing e, ao mesmo tempo, reduzir o risco de fadiga do cliente.

As principais áreas a serem monitoradas quanto a possíveis sobreposições são:

* **Linha do Tempo** (datas de início e término): muitas jornadas estão sendo executadas simultaneamente?
* **Público-alvo**: que porcentagem do meu público-alvo de jornada também faz parte de outras jornadas?
* **Canal**: há outras comunicações agendadas para o mesmo período? Em caso afirmativo, quantas?
* **Conjunto de Regras de Limite**: que tipos de jornadas estou limitando e há sobreposição entre eles?
* **Configuração de Canal**: há outras jornadas ou campanhas usando qualquer configuração de canal que esteja sendo usada na mesma jornada ou campanha que possam impedir a exibição da jornada ou campanha ao usuário final?

➡️ [Descubra este recurso no vídeo](#video)

## Como o Journey Optimizer detecta conflitos {#detection}

Abaixo está um resumo de como o Journey Optimizer identifica possíveis conflitos para jornadas e campanhas:

* **Escopo de identificação de conflito**: os conflitos são mostrados somente para campanhas e jornadas ativas ou agendadas.
* **jornadas Unitárias**: se a jornada selecionada for unitária, outras jornadas que começam com o mesmo evento serão exibidas, pois esse evento acionará todas essas jornadas.
* **Qualificação de público-alvo e Público-alvo de leitura/Evento comercial** jornadas: se a jornada selecionada for uma qualificação de Público-alvo ou uma jornada de Evento comercial/Público de leitura, todas as outras jornadas do mesmo tipo com um público-alvo válido serão exibidas, pois pode haver sobreposições entre os públicos-alvo.
* **Campanhas**: como todas as campanhas estão direcionando públicos e não há nenhum conceito de eventos, todas as campanhas potencialmente entram em conflito com jornadas acionadas por segmento (começando com uma atividade Ler público).
* **Campanhas online/agendadas**: campanhas online e agendadas podem entrar em conflito devido a uma possível sobreposição de públicos. Para qualquer campanha, todas as campanhas ativas ou programadas são listadas no visualizador de conflitos.

## Exibir conflitos identificados para uma determinada jornada ou campanha {#view}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Exibir conflitos em potencial"
>abstract="Verifique sempre que houver uma possibilidade de sobreposição com outras campanhas. Os conflitos são exibidos somente para campanhas ativas e programadas. Observe que o botão fica disponível assim que você atribui qualquer uma das seguintes configurações: **[!UICONTROL Data de início/término]**, **[!UICONTROL Público-alvo]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuração de canal]** e **[!UICONTROL Conjunto de regras]**."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Exibir conflitos em potencial"
>abstract="Verifique sempre que houver a possibilidade de sobreposição com outras jornadas. Os conflitos são exibidos somente para jornadas ativas e programadas. Observe que o botão fica disponível assim que você atribui qualquer uma das seguintes configurações: **[!UICONTROL Data de início/término]**, **[!UICONTROL Público-alvo]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuração de canal]** e **[!UICONTROL Conjunto de regras]**."

Ao criar uma jornada ou campanha, o Journey Optimizer permite verificar sempre que há uma possibilidade de sobreposição com outras jornadas ou campanhas. Para fazer isso, siga estes passos:

1. No momento da criação de uma jornada ou campanha, clique no botão **[!UICONTROL Exibir Conflitos Potenciais]** nas propriedades da jornada ou campanha.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >O botão **[!UICONTROL Exibir conflitos potenciais]** ficará disponível para seleção assim que você atribuir qualquer uma das seguintes configurações: **[!UICONTROL Data de início/término]**, **[!UICONTROL Público-alvo]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuração de canal]** e **[!UICONTROL Conjunto de regras]**. Selecione **[!UICONTROL Salvar]** depois de atribuir essas configurações, pois o botão não poderá ser selecionado até que as alterações sejam salvas.

1. A janela **[!UICONTROL Conflitos potenciais]** é aberta, permitindo visualizar todos os elementos que estão sobrepondo a jornada/campanha atual.

   Você pode abrir uma jornada ou campanha sobreposta diretamente nesta tela selecionando o nome dela.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >As campanhas recém-publicadas podem levar até 5 minutos para serem exibidas no visualizador de conflitos, devido ao armazenamento em cache implementado

Para refinar ainda mais sua pesquisa por possíveis sobreposições, você pode filtrar sua lista de campanhas e jornadas com base nos campos relevantes. Para fazer isso, selecione o ícone de filtro na visualização de inventário. [Saiba como trabalhar com filtros](../start/search-filter-categorize.md#filter-lists)

## Resolver conflitos {#resolve}

Estas são algumas dicas para reduzir os possíveis conflitos depois de identificados:

* Ajuste as **datas de início/término** para evitar campanhas ou jornadas sobrepostas.
* Refine **direcionamento de público** para minimizar a sobreposição entre as jornadas.
* Implemente **limites de frequência** para evitar que os clientes recebam muitas comunicações.
* Reduza o número de **jornadas ativas** para gerenciar a experiência do cliente com mais eficiência.
* Defina **prioridades** em ações de entrada para garantir que a ação mais importante seja exibida para os clientes.

Ao aproveitar esses recursos, você pode garantir que seus esforços de marketing estejam alinhados e que você mantenha o equilíbrio certo em sua estratégia de comunicação.

## Vídeo tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435528?quality=12)
