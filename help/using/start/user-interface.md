---
solution: Journey Optimizer
product: journey optimizer
title: Interface do usuário
description: Saiba mais sobre a interface do usuário do Journey Otimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 681532f8-1149-465e-92c8-2b5366abc3aa
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Interface do usuário {#cjm-user-interface}

Conectar-se a [Adobe Experience Cloud](http://experience.adobe.com) e navegue até [!DNL Journey Optimizer].

Os principais conceitos ao navegar na interface do usuário são comuns à Adobe Experience Platform. Consulte [Documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html#adobe-experience-platform-ui-guide){target=&quot;_blank&quot;} para obter mais detalhes.

Os componentes e recursos disponíveis na interface do usuário dependem do [permissões](../administration/permissions.md) e no seu [pacote de licenciamento](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}. Para qualquer pergunta, entre em contato com o Gerente de sucesso do cliente da Adobe.

>[!NOTE]
>
>Essa documentação é atualizada com frequência para refletir as alterações mais recentes na interface do usuário do produto. No entanto, algumas capturas de tela podem diferir ligeiramente da interface do usuário.


## Navegação à esquerda {#left-nav}

Navegue pelos links à esquerda para acessar o [!DNL Journey Optimizer] recursos.

![](assets/ajo-home.png)

>[!NOTE]
>
>Os recursos disponíveis podem variar dependendo de suas permissões e do contrato de licença.

Você pode encontrar abaixo a lista completa de serviços e recursos disponíveis na navegação à esquerda e links para as páginas de ajuda associadas.

**Início**

[!DNL Journey Optimizer] a página inicial contém os links e recursos principais a serem iniciados. O **[!UICONTROL Recents]** A lista fornece atalhos para os eventos e jornadas criados recentemente. Esta lista mostra as datas de criação e modificação e o status.

**[!UICONTROL JOURNEY MANAGEMENT]**

* **[!UICONTROL Journeys]** - Crie, configure e orquestre as jornadas dos clientes. [Saiba mais](../building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL Landing pages]** - Criar, projetar, testar e publicar landing pages. [Saiba mais](../landing-pages/get-started-lp.md)

**[!UICONTROL DECISION MANAGEMENT]**

* **[!UICONTROL Offers]** - Acesse suas fontes e conjuntos de dados recentes a partir desse menu. Use esta seção para criar novas ofertas. [Saiba mais](../offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL Components]** - Criar disposições, regras e tags. [Saiba mais](../offers/offer-library/key-steps.md)

**[!UICONTROL CONTENT MANAGEMENT]**

* **[!UICONTROL Assets]** - [!DNL Adobe Experience Manager Assets Essentials] O é um repositório centralizado de ativos que pode ser usado para preencher suas mensagens. [Saiba mais](../email/assets-essentials.md)

**[!UICONTROL DATA MANAGEMENT]**

* **[!UICONTROL Schemas]** - Use a Adobe Experience Platform para criar e gerenciar esquemas do Experience Data Model (XDM) em uma tela visual interativa chamada de Editor de esquemas. [Saiba mais](../data/get-started-schemas.md)

* **[!UICONTROL Datasets]** - Todos os dados assimilados na Adobe Experience Platform são mantidos no Data Lake como conjuntos de dados. Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). [Saiba mais](../data/get-started-datasets.md)

* **[!UICONTROL Queries]** - Use o Serviço de query da Adobe Experience Platform para gravar e executar consultas, exibir consultas executadas anteriormente e acessar consultas salvas por usuários em sua organização. [Saiba mais](../data/get-started-queries.md)

* **[!UICONTROL Monitoring]** - Use esse menu para monitorar a assimilação de dados na interface do usuário da Adobe Experience Platform. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html){target=&quot;_blank&quot;}

**[!UICONTROL CONNECTIONS]**

* **[!UICONTROL Sources]** - Use esse menu para assimilar dados de várias fontes, como aplicativos da Adobe, armazenamentos baseados em nuvem, bancos de dados e muito mais, e estruturar, rotular e aprimorar os dados recebidos. [Saiba mais](get-started-sources.md)

**[!UICONTROL CUSTOMER]**

* **[!UICONTROL Segments]** - Crie e gerencie definições de segmentos da Experience Platform e aproveite-as em suas jornadas. [Saiba mais](../segment/about-segments.md)

* **[!UICONTROL Profiles]** - O Perfil do cliente em tempo real cria uma visualização holística de cada cliente individual, combinando dados de vários canais, incluindo dados online, offline, CRM e de terceiros. [Saiba mais](../segment/get-started-profiles.md)

* **[!UICONTROL Identities]** - O Adobe Experience Platform Identity Service gerencia a identificação entre dispositivos, canais e quase em tempo real dos clientes, no que é conhecido como um gráfico de identidade na Adobe Experience Platform. [Saiba mais](../segment/get-started-identity.md)

**[!UICONTROL ADMINISTRATION]**

* **[!UICONTROL Journey Administration]** - Use este menu para configurar [events](../event/about-events.md), [fontes de dados](../datasource/about-data-sources.md) e [ações](../action/action.md) para usar em suas jornadas.

* **[!UICONTROL Sandboxes]** - A Adobe Experience Platform fornece sandboxes que particionam uma única instância em ambientes virtuais separados para ajudar a desenvolver aplicativos de experiência digital. [Saiba mais](../administration/sandboxes.md)

* **[!UICONTROL Alerts]** - A interface do usuário permite visualizar um histórico de alertas recebidos com base em métricas reveladas pelos Insights de capacidade de observação da Adobe Experience Platform. A interface do usuário também permite exibir, ativar e desativar as regras de alerta disponíveis. [Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html){target=&quot;_blank&quot;}


## Casos de uso no produto {#in-product-uc}

Aproveitamento [!DNL Adobe Journey Optimizer] casos de uso da página inicial e forneça algumas informações rápidas para criar uma jornada do cliente.

![](assets/use-cases-home.png)

Os casos de uso disponíveis são:

* **Criar perfis de teste**, para criar perfis de teste usando nosso template CSV para testar mensagens e jornadas personalizadas. Saiba como implementar este caso de uso [nesta página](../segment/creating-test-profiles.md#use-case-1).
* **Enviar uma mensagem de aniversário para os clientes**, para enviar um email automaticamente para desejar aos clientes aniversário. (em breve)
* **Enviar emails para novos clientes integrados**, para enviar facilmente até dois emails de boas-vindas aos clientes recém-registrados. (em breve)
* **Enviar mensagens de push para a lista de clientes importados**, para enviar uma notificação por push rapidamente para uma lista de clientes importados de um arquivo CSV. (em breve)

Clique em **[!UICONTROL View details]** para saber mais sobre cada caso de uso.

Clique no botão **[!UICONTROL Begin]** para iniciar o caso de uso.

Você pode acessar casos de uso executados a partir da variável **[!UICONTROL View use case library]** botão.

## Acessibilidade{#accessibility}

Os recursos de acessibilidade em [!DNL Adobe Journey Optimizer] são herdadas da Adobe Experience Platform:

* Acessibilidade do teclado
* Contraste de cores
* Validação de campos obrigatórios

[Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html){target=&quot;_blank&quot;} na documentação da Adobe Experience Platform.

Você pode usar esses atalhos de teclado comuns no [!DNL Journey Optimizer]:

| Ação | Atalho |
| --- | --- |
| Mover entre elementos da interface do usuário, seções e grupos de menu | Tabulação |
| Recuar entre elementos da interface do usuário, seções e grupos de menu | Shift + Guia |
| Mover dentro de seções para definir o foco de elementos individuais | Seta |
| Selecionar ou limpar um elemento em foco | Inserir ou Barra de espaço |
| Cancelar uma seleção, recolher um painel ou fechar uma caixa de diálogo | Esc |

[Saiba mais](https://experienceleague.adobe.com/docs/experience-platform/accessibility/custom.html){target=&quot;_blank&quot;} na documentação da Adobe Experience Platform.

Você pode usar esses atalhos em partes específicas do Journey Otimizer:

<table>
  <thead>
    <tr>
      <th>Elemento da interface</th>
      <th>Ação</th>
      <th>Atalho</th>
    </tr>
  </thead>
  <tr>
    <td>Lista de jornadas, ações, fontes de dados ou eventos</td>
    <td>Criar uma jornada, uma ação, uma fonte de dados ou um evento</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">Tela de jornada no status de rascunho</td>
    <td>Adicionar uma atividade da paleta esquerda na primeira posição disponível, de cima para baixo</td>
    <td>Clique duas vezes na atividade</td>
  </tr>
  <tr>
    <td>Selecionar todas as atividades</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td>Excluir as atividades selecionadas</td>
    <td>Excluir ou Backspace, em seguida, Inserir para confirmar a exclusão</td>
  </tr>
  <tr>
  <td rowspan="3">

Painel de configuração desses elementos:

<ul>
  <li>Atividade em uma jornada</li>
  <li>Evento</li>
  <li>Fonte de dados</li>
  <li>Ação</li>
</ul>

</td>
    <td>Mover para o próximo campo a ser configurado</td>
    <td>Tabulação</td>
  </tr>
  <tr>
    <td>Salve as alterações e feche o painel de configuração</td>
    <td>Enter</td>
  </tr>
  <tr>
    <td>Descartar alterações e fechar o painel de configuração</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td rowspan="4">Jornada no modo de teste</td>
    <td>Ative ou desative o modo de teste</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Acionar um evento em uma jornada baseada em eventos</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

Acionar um evento em uma jornada baseada em segmentos para a qual a variável **[!UICONTROL Single profile at a time]** está ativada

</td>
    <td>P</td>
  </tr>
  <tr>
    <td>Exibir os logs de teste</td>
    <td>L</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>Campo de texto</td>
    <td>Selecionar todo o texto no campo selecionado</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">Janela pop-up</td>
    <td>Salvar alterações ou confirmar a ação</td>
    <td>Enter</td>
  </tr>
  <tr>
    <td>Feche a janela</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td>Editor de expressão simples</td>
    <td>Selecionar e adicionar um campo</td>
    <td>Clique duas vezes em um campo</td>
  </tr>
  <tr>
    <td>Navegação pelos campos XDM</td>
    <td>Selecionar todos os campos de um nó</td>
    <td>Selecione o nó pai</td>
  </tr>
  <tr>
    <td>Visualização da carga útil</td>
    <td>Selecionar a carga</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
</table>

## Buscar ajuda e suporte {#find-help}

Acesse as páginas de ajuda da chave do Adobe Journey Otimizer na seção inferior da página inicial.

Use o **Ajuda** para acessar páginas de ajuda, entre em contato com o suporte e compartilhe comentários. Você pode pesquisar artigos e vídeos de ajuda no campo de pesquisa.

![](assets/ajo-help.png)

## Navegadores compatíveis {#browsers}

Adobe [!DNL Journey Optimizer] A interface do foi projetada para funcionar de maneira ideal na versão mais recente do Google Chrome. Você pode ter problemas ao usar determinados recursos em versões mais antigas ou outros navegadores.

## Preferências de idioma {#language-pref}

A interface do usuário está disponível atualmente nos seguintes idiomas:

* Inglês
* Francês
* Alemão
* Italiano
* Espanhol
* Português (Brasil)
* Japonês
* Coreano

O idioma padrão da interface é determinado pelo idioma preferencial especificado no perfil do usuário.

Para alterar seu idioma:

* Clique em **Preferências** do seu avatar, no canto superior direito.
   ![](assets/preferences.png)
* Em seguida, clique no idioma exibido sob seu endereço de email
* Selecione o idioma preferido e clique em **Salvar**. Você pode selecionar um segundo idioma caso o componente que está usando não esteja localizado em seu primeiro idioma.
   ![](assets/select-language.png)

## Pesquisar{#unified-search}

Em qualquer lugar da interface do Adobe Journey Otimizer, use o recurso de pesquisa unificado da Adobe Experience Cloud no centro da barra superior para localizar ativos, jornadas, conjuntos de dados e muito mais em suas sandboxes.

Comece a inserir conteúdo para exibir os principais resultados. Artigos de ajuda sobre as palavras-chave inseridas também são exibidos nos resultados.

![](assets/unified-search.png)

Press **Enter** para acessar todos os resultados e filtrar por objeto comercial.

![](assets/search-and-filter.png)

## Listas de filtros{#filter-lists}

Na maioria das listas, uma barra de pesquisa permite procurar um item específico e selecionar critérios de filtragem.

Os filtros podem ser acessados clicando no ícone de filtro na parte superior esquerda da lista. O menu de filtro permite filtrar os elementos exibidos de acordo com critérios diferentes. Você pode optar por exibir apenas elementos de um determinado tipo ou status, os que você criou ou os que foram modificados nos últimos 30 dias. As opções diferem dependendo do contexto.

Na lista de jornadas, você pode filtrar jornadas de acordo com seu status, tipo e versão do **[!UICONTROL Status and version filters]**. O tipo pode ser: **[!UICONTROL Unitary event]**, **[!UICONTROL Segment qualification]**, **[!UICONTROL Read segment]**, **[!UICONTROL Business event]** ou **[!UICONTROL Burst]**. Você pode optar por exibir somente as jornadas que usam um evento, grupo de campos ou ação específico da **[!UICONTROL Activity filters]** e **[!UICONTROL Data filters]**. O **[!UICONTROL Publication filters]** permite selecionar uma data de publicação ou um usuário. Você pode optar, por exemplo, por exibir as versões mais recentes de jornadas ao vivo que foram publicadas ontem. [Saiba mais](../building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Observe que as colunas exibidas podem ser personalizadas usando o botão de configuração na parte superior direita das listas. A personalização é salva para cada usuário.

Use o **[!UICONTROL Last update]** e **[!UICONTROL Last update by]** colunas para verificar quando aconteceu a última atualização de suas jornadas e quem a salvou.

![](assets/filter-journeys.png)

Nos painéis de configuração Evento, Fonte de dados e Ação , a variável **[!UICONTROL Used in]** exibe o número de jornadas que usam esse evento, grupo de campos ou ação em particular. Você pode clicar no botão **[!UICONTROL View journeys]** para exibir a lista de jornadas correspondentes.

![](assets/journey3bis.png)

Nas listas, é possível executar ações básicas em cada elemento. Por exemplo, você pode duplicar ou excluir um item.

![](assets/journey4.png)
