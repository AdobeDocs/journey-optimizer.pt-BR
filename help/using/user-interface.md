---
title: Interface do usuário
description: Interface do usuário do Journey Optimizer
translation-type: tm+mt
source-git-commit: fb1170c5e16c54ff93411d93020336f8de334ae1
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 40%

---

# Interface do usuário {#cjm-user-interface}

![](assets/do-not-localize/badge.png)

Esta documentação é atualizada com frequência para refletir as alterações recentes no produto. No entanto, algumas capturas de tela podem diferir ligeiramente da interface do usuário.

## Espaço de trabalho {#cjm-workspace}

Depois de conectado a [Adobe Experience Cloud](http://experience.adobe.com), navegue até [!DNL Journey Optimizer].

>[!NOTE]
>
>Os principais conceitos ao navegar na interface do usuário são detalhados em [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html?lang=en#adobe-experience-platform-ui-guide).

Use os links à esquerda para procurar recursos.

![](assets/ajo-home.png)

>[!NOTE]
>
>Os recursos disponíveis podem variar dependendo de suas permissões e do contrato de licença.

Você pode encontrar abaixo a lista completa de entradas no painel à esquerda e links para a documentação associada.

**Início**

[!DNL Journey Optimizer] a página inicial contém os links e recursos principais a serem iniciados. A lista **[!UICONTROL Recents]** fornece atalhos para as mensagens, eventos e jornadas recém-criadas ou atualizadas. Esta lista mostra as datas de criação e modificação e o status.

**[!UICONTROL JOURNEY MANAGEMENT]**

* **[!UICONTROL Journeys]** - Crie, configure e orquestre as jornadas do cliente. Saiba mais [nesta seção](building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL Messages]** - Criar, projetar, testar e publicar mensagens de email e de push. Saiba mais [nesta seção](create-message.md)

**[!UICONTROL DECISION MANAGEMENT]**

* **[!UICONTROL Offers]** - Acesse suas fontes e conjuntos de dados recentes a partir desse menu. Use esta seção para criar novas ofertas. [Saiba mais](offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL Components]** - Criar disposições, regras e tags. Saiba mais [nesta seção](offers/offer-library/key-steps.md)

**[!UICONTROL CONTENT MANAGEMENT]**

* **[!UICONTROL Assets]** -  [!DNL Adobe Experience Manager Assets Essentials] é um repositório centralizado de ativos que podem ser usados para preencher suas mensagens. Saiba mais [nesta seção](assets-essentials.md)

**[!UICONTROL DATA MANAGEMENT]**

* **[!UICONTROL Schemas]** - Use o Adobe Experience Platform para criar e gerenciar esquemas do Experience Data Model (XDM) em uma tela visual interativa chamada de Editor de esquemas. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html)

* **[!UICONTROL Datasets]** - Todos os dados assimilados no Adobe Experience Platform são mantidos no Data Lake como conjuntos de dados. Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). [Saiba como visualizar e criar um conjunto de dados nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html)

* **[!UICONTROL Queries]** - Use o Serviço de query da Adobe Experience Platform para gravar e executar consultas, exibir consultas executadas anteriormente e acessar consultas salvas por usuários em sua organização. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/query/ui/overview.html)

* **[!UICONTROL Monitoring]** - Use esse menu para monitorar a assimilação de dados na interface do usuário do Adobe Experience Platform. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html)

**[!UICONTROL CONNECTIONS]**

* **[!UICONTROL Sources]** - Use esse menu para assimilar dados de várias fontes, como aplicativos Adobe, armazenamentos baseados em nuvem, bancos de dados e muito mais, e estruturar, rotular e aprimorar os dados recebidos. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=pt-BR)

**[!UICONTROL CUSTOMER]**

* **[!UICONTROL Segments]** - Crie e gerencie definições de segmento do Experience Platform e aproveite-as em suas jornadas. Saiba mais [nesta página](segment/about-segments.md)

* **[!UICONTROL Profiles]** - O Perfil do cliente em tempo real cria uma visualização holística de cada cliente individual, combinando dados de vários canais, incluindo dados online, offline, CRM e de terceiros. [Saiba mais nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html)

* **[!UICONTROL Identities]** - O Adobe Experience Platform Identity Service gerencia a identificação entre dispositivos, canais e quase em tempo real dos clientes no que é conhecido como um gráfico de identidade no Adobe Experience Platform. [Saiba como criar um namespace de identidade nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#manage-namespaces)

**[!UICONTROL ADMINISTRATION]**

* **[!UICONTROL Journey Administration]** - Use esse menu para configurar  [eventos](event/about-events.md),  [fontes ](datasource/about-data-sources.md) de dados e  [](action/action.md) ações para usar em suas jornadas.

* **[!UICONTROL Sandboxes]** - A Adobe Experience fornece sandboxes que particionam uma única instância da Platform em ambientes virtuais separados para ajudar a desenvolver aplicativos de experiência digital. [Saiba mais sobre sandboxes nesta documentação](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html)

## Suporte a navegador e idioma

A interface Adobe [!DNL Journey Optimizer] foi projetada para funcionar de maneira ideal na versão mais recente do Google Chrome. Você pode ter problemas ao usar determinados recursos em versões mais antigas ou outros navegadores.

A interface do usuário está disponível atualmente nos seguintes idiomas:

* Inglês
* Francês
* Alemão

O idioma padrão da interface é determinado pelo idioma preferencial especificado no perfil do usuário.

Para alterar seu idioma:

* Clique em **Editar Preferências** do seu avatar, na parte superior direita.
* Em seguida, clique em **Visit Adobe Account** para acessar o perfil do Adobe.
* Selecione a guia **Notifications** na parte superior e clique em **Preferences**.
* Selecione o idioma preferido e clique em **Save**.

>[!NOTE]
>
>Você precisa sair e entrar novamente em [!DNL Journey Optimizer] para aplicar as alterações.

## Pesquisar e filtrar{#section_lgm_hpz_pgb}

Na maioria das listas, uma barra de pesquisa permite procurar um item.

O **[!UICONTROL Filters]** é acessível com um clique no ícone de filtro na parte superior esquerda da lista. O menu de filtro permite filtrar os elementos exibidos de acordo com critérios diferentes. Você pode optar por exibir apenas elementos de um determinado tipo ou status, os que você criou ou os que foram modificados nos últimos 30 dias.

Na lista de jornadas, além de **[!UICONTROL Creation filters]**, você também pode filtrar as jornadas exibidas de acordo com seu status e versão (**[!UICONTROL Status and version filters]**). Você pode optar por exibir somente jornadas que usam um evento, grupo de campos ou ação específica (**[!UICONTROL Activity filters]** e **[!UICONTROL Data filters]**). O **[!UICONTROL Publication filters]** permite selecionar uma data de publicação ou um usuário. Você pode optar, por exemplo, por exibir as versões mais recentes das jornadas ativas que foram publicadas ontem. [Saiba mais](building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Observe que as colunas exibidas podem ser personalizadas usando o botão de configuração na parte superior direita das listas. A personalização é salva para cada usuário.

Use as colunas **[!UICONTROL Last update]** e **[!UICONTROL Last update by]** para verificar quando aconteceu a última atualização de suas jornadas e quem as salvou.

![](assets/journey74.png)

Nos painéis de configuração Evento, Fonte de dados e Ação , o campo **[!UICONTROL Used in]** exibe o número de jornadas que usam esse evento, grupo de campos ou ação em particular. Você pode clicar no botão **[!UICONTROL View journeys]** para exibir a lista de jornadas correspondentes.

![](assets/journey3bis.png)

Nas diferentes listas, é possível executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item.

![](assets/journey4.png)

## Navegue pelos campos Adobe Experience Platform {#friendly-names-display}

Ao definir a [carga útil do evento](event/about-creating.md#define-the-payload-fields), [carga útil do grupo de campo](datasource/configure-data-sources.md#define-field-groups) e selecionar campos no [editor de expressões](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html), o nome de exibição é exibido além do nome do campo. Essas informações são recuperadas a partir da definição do schema no modelo de dados de experiência.

Se descritores como &quot;xdm:alternateDisplayInfo&quot; forem fornecidos durante a configuração de schemas, os nomes de usuário simples substituirão os nomes de exibição. É especialmente útil ao trabalhar com &quot;eVars&quot; e campos genéricos. Você pode configurar descritores de nome amigáveis por meio de uma chamada de API. Para obter mais informações, consulte o [guia do desenvolvedor do Registro de Schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

![](assets/xdm-from-descriptors.png)

Se um nome simples estiver disponível, o campo será exibido como `<friendly-name>(<name>)`. Se nenhum nome simples estiver disponível, o nome de exibição será exibido, por exemplo `<display-name>(<name>)`. Se nenhum deles estiver definido, somente o nome técnico do campo será exibido `<name>`.

>[!NOTE]
>
>Os nomes simples não são recuperados ao selecionar campos de uma união de schemas.

## Acessibilidade{#cjm-accessibility}

Estes são os diferentes atalhos disponíveis na interface do [!DNL Journey Optimizer].

_Na lista de jornadas, ações, fontes de dados ou eventos:_

* Pressione **c** para criar uma nova jornada, ação, fonte de dados ou evento.

_Ao configurar uma atividade em uma jornada:_

A tela é salva automaticamente. Você pode ver, na parte superior esquerda da tela, o status de salvamento.

* Pressione **escape** para fechar o painel de configuração e descartar as alterações feitas. É equivalente ao botão **[!UICONTROL Cancel]**.
* Pressione **Enter** ou clique fora do painel para fechar o painel de configuração. As alterações são salvas. É equivalente ao botão **[!UICONTROL Ok]**.
* Se você pressionar **Delete** ou **backspace**, será possível pressionar **Enter** para confirmar a exclusão.

_Em janelas pop-ups:_

* Pressione **escape** para fechar (equivalente ao botão **[!UICONTROL Cancel]**).
* Pressione **Enter** para salvar ou confirmar (equivalente ao botão **[!UICONTROL Ok]** ou **[!UICONTROL Save]**).

_No painel de configuração do evento, fonte de dados ou ação:_

* Pressione **escape** para fechar o painel de configuração sem salvar.
* Pressione **Enter** para salvar as modificações e fechar o painel de configuração.
* Pressione **tab** para saltar entre os diferentes campos que serão configurados.

_No editor de expressões simples_

* Duplo clique em um campo, à esquerda, para adicionar uma query (equivalente a arrastar e soltar).

_Ao navegar pelos campos XDM:_

* Marcar um &quot;nó&quot; selecionará todos os campos do nó.

_Em todas as áreas de texto:_

* Use a combinação de teclas **Ctrl/Command + A** para selecionar o texto. Na pré-visualização de carga, é selecionada a carga útil.

_Em uma tela com uma barra de pesquisa:_

* Use a combinação de teclas **Ctrl/Command + F** para selecionar a barra de pesquisa.

_Na tela de uma jornada:_

* Use a combinação de teclas **Ctrl/Command + A** para selecionar todas as atividades.
* Quando uma ou várias atividades forem selecionadas, pressione **Delete** ou **backspace** para excluí-las. Pressione **Enter** na janela pop-up para confirmar.
* Clique duas vezes em uma atividade da paleta esquerda para adicioná-la à primeira posição disponível (de cima para baixo).

_Em uma jornada:_

* Pressione **T** para ativar/desativar o modo de teste.
* Em uma jornada baseada em eventos no modo de teste, pressione **E** para acionar um evento.
* Em uma jornada baseada em segmento, quando a opção **Single profile at a time** estiver selecionada no modo de teste, pressione **P** para acionar um evento.
* No modo de teste, pressione **L** para exibir os logs.
