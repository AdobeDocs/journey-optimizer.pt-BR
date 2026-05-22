---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o programa de fidelidade
description: Saiba como configurar provedores de recompensa, definições de eventos e configurações no nível da organização para seu programa de fidelidade no Adobe [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: e4ee70a9c918bffb372ab7cee567ae7422c3720c
workflow-type: tm+mt
source-wordcount: '1456'
ht-degree: 0%

---

# Configurar o programa de fidelidade {#loyalty-admin}

>[!BEGINSHADEBOX]

**Documentação de Desafios de Fidelidade:**

* [Introdução aos desafios de fidelidade](get-started.md)
* [Acessar e gerenciar desafios e tarefas](access-loyalty-challenges.md)
* [Criar desafios](create-challenges.md)
* [Criar tarefas](create-tasks.md)
* [Monitorar o desempenho de desafio de fidelidade](loyalty-reporting.md)
* **Configurar o programa de fidelidade** ◀︎ **Você está aqui**
* [Referência da API de desafios de fidelidade](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade em [!DNL Journey Optimizer], consulte [ciclo de lançamento](../rn/releases.md).

Use a configuração do programa de fidelidade no [!DNL Journey Optimizer] para se conectar aos seus sistemas de fidelidade externos. Os profissionais de marketing usam o **[!UICONTROL Loyalty Challenges (Beta)]** para projetar desafios, tarefas, conteúdo e mensagens. A configuração do programa de fidelidade é uma área separada, somente de administrador, para cumprimento de premiação, mapeamento de eventos, inventário de produtos e exclusões.

## Pré-requisitos {#prerequisites}

A configuração do programa de fidelidade destina-se a administradores. Além das permissões necessárias para Desafios de Fidelidade, você precisa de acesso de nível de administrador à sua instância [!DNL Journey Optimizer]. Entre em contato com o administrador do Adobe para solicitar acesso.

## Acessar configuração do programa de fidelidade {#access-loyalty-admin}

Navegue até **[!UICONTROL Fidelidade]** e selecione **[!UICONTROL Administrador fiel]** para acessar a interface de configuração do programa de fidelidade.

A interface é organizada em guias:

* **Configurações globais** — Defina o namespace de identidade da Experience Platform. [Saiba como definir configurações globais](#global-settings)
* **Provedores de recompensa** — Conecte APIs externas que atendem a recompensas, incluindo tipos de recompensa, proxies e autenticação. [Saiba como configurar provedores de premiação](#reward-providers)
* **Definições de eventos** — Mapeie os eventos de experiência recebidos para atividades que você pode usar nas tarefas **[!UICONTROL Evento personalizado]**. [Saiba como configurar definições de evento](#event-definitions)
* **Estoque de produtos** — carregue mapeamentos de item para grupo para poder usar grupos de produtos nas regras de qualificação de tarefa. [Saiba como configurar o inventário de produtos](#product-inventory)
* **Exclusões** — carregue exclusões de itens e grupos em toda a organização que se aplicam quando os profissionais de marketing configuram tarefas. [Saiba como configurar exclusões](#exclusions)

## Configurações globais {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configurações globais"
>abstract="Selecione o namespace de identidade da Adobe Experience Platform para seu programa de fidelidade."

Abra a guia **[!UICONTROL Configurações globais]**. Por enquanto, a configuração principal disponível nesta guia é selecionar o namespace de identidade da Adobe Experience Platform usado por seu programa de fidelidade na lista suspensa **[!UICONTROL Namespace]**.

![](assets/admin-global-settings.png)

➡️ [Saiba como trabalhar com namespaces de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Provedores de recompensa {#reward-providers}

Um **provedor de premiação** informa a [!DNL Journey Optimizer] para onde enviar chamadas de atendimento quando o progresso do desafio é registrado ou um desafio é concluído, por exemplo, uma API que credita pontos de fidelidade ou estrelas a uma conta de membro.

Uma configuração de provedor de premiação inclui:

![](assets/admin-reward.png)

* Detalhes básicos da conexão (nome, descrição, URL, cabeçalhos).
* **[!UICONTROL Definições de recompensa]** — os tipos de recompensa que este provedor pode emitir (por exemplo, estrelas ou milhas).
* **[!UICONTROL Proxies de premiação]** — um proxy intermediário através do qual as chamadas são roteadas em vez do seu ponto de extremidade diretamente.
* **[!UICONTROL Geradores de token de autenticação]** — o mecanismo [!DNL Journey Optimizer] usa para obter tokens de acesso antes de chamar sua API.

Para criar um provedor de premiação, siga estas etapas:

1. Abra a guia **[!UICONTROL Provedores de recompensa]** e selecione **[!UICONTROL Criar provedor de recompensa]**.

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]**.

1. No campo **[!UICONTROL URL]**, insira a URL da API que recebe solicitações de atendimento.

1. Adicione **[!UICONTROL Cabeçalhos]** conforme necessário para sua API (por exemplo, chaves de API ou tipos de conteúdo).

1. Configure os recursos abaixo associados ao seu provedor de premiação. Expanda cada seção para obter mais informações:

   +++Definições de recompensa - Uma entrada por recompensa que é suportada pelo seu provedor (por exemplo, pontos ou estrelas do programa, crédito monetário)

   Para cada definição:

   * Forneça um nome e uma descrição.
   * Especifique se a definição é **[!UICONTROL Habilitada]**.
   * Ative a opção **![!UICONTROL Default]** para marcar uma definição como padrão para este provedor.
   * Especifique a **carga** enviada com chamadas de atendimento.

   ![](assets/admin-reward-definition.png)

   +++

   +++Proxy de recompensa - Encaminha chamadas de atendimento por meio de um servidor intermediário em vez de diretamente para o endpoint

   * Forneça um nome e uma descrição.
   * Insira as informações de **[!UICONTROL Host]**, **[!UICONTROL Porta]**.
   * Especifique se o proxy está **[!UICONTROL Habilitado]**.
   * Adicione a **[!UICONTROL Credencial]** do proxy.

   ![](assets/admin-reward-proxies.png)

   +++

   +++Gerador de token de autenticação - Se a API exigir um token de portador para autenticação

   * Insira um nome e uma descrição.
   * No campo Tipo de autenticação, digite o tipo de autenticação (por exemplo, Portador).
   * Selecione o método HTTP a ser usado (por exemplo, POST).
   * Insira o URL do ponto de extremidade do token. e adicione a **[!UICONTROL Chave do token]** na resposta (por exemplo, `access_token`).
   * Especifique se o gerador de token de autenticação é **[!UICONTROL Habilitado]**.
   * Adicione cabeçalhos exigidos pelo endpoint do token, se necessário.

   O [!DNL Journey Optimizer] usa essa configuração para obter um token novo antes de chamar a API de recompensa.

   ![](assets/admin-reward-auth.png)

   +++

1. Selecione **[!UICONTROL Criar provedor de premiação]**. O provedor e todos os recursos configurados são salvos juntos.

Depois de salvar, o provedor é exibido na lista de provedores de premiação. Os profissionais de marketing podem selecionar esse provedor ao configurar recompensas por desafio. [Saiba como configurar recompensas por desafio](create-challenges.md#rewards)

Para editar um provedor de premiação existente, abra a guia **[!UICONTROL Provedores de premiação]**, selecione o provedor e atualize os campos no local. As alterações nos recursos secundários (definições de recompensa, proxies, geradores de token de autenticação) são salvas ao atualizá-los.

>[!NOTE]
>
>**[!UICONTROL Traga seus próprios dados]** Os desafios preenchem as recompensas por meio de sua própria integração de dados. Os provedores de recompensa configurados aqui não se aplicam a esses desafios. [Saiba como criar e trazer seus próprios desafios de dados](create-challenges.md#create-the-challenge)

## Definições de evento (opcional) {#event-definitions}

**[!UICONTROL Definições de eventos]** mapeiam eventos de experiência de seus sistemas (por exemplo, compra, check-in de hotel) para atividades nas quais os Desafios de Fidelidade podem agir, principalmente **[!UICONTROL Tarefas de evento personalizado]**. Quando os eventos chegam, [!DNL Journey Optimizer] usa essas definições para decidir se eles devem ser processados. Eventos que não correspondem a nenhuma definição são ignorados.

### Criar uma definição de evento {#create-event-definition}

1. Abra a guia **[!UICONTROL Definições de eventos]** e crie uma nova definição.

   ![](assets/admin-event-definition.png)

1. Insira um **[!UICONTROL Nome]** para o evento (por exemplo, `Coffee purchase`). Esse é o nome que os profissionais de marketing veem ao configurar uma tarefa de **[!UICONTROL Evento personalizado]**.

1. Especifique como [!DNL Journey Optimizer] reconhece o evento nas cargas de entrada. Forneça um **[!UICONTROL Caminho do identificador]**, uma **[!UICONTROL ID do esquema XDM]** ou ambos:

   * **[!UICONTROL Caminho do identificador]** — Caminho para o campo que identifica o evento ou membro (por exemplo, `data.memberId`). Use isso ao corresponder eventos por valores na carga.
   * **[!UICONTROL Valores de identificador]** — Valores no caminho do identificador que devem estar presentes para que esta definição seja compatível.
   * **[!UICONTROL ID do esquema XDM]** — ID do esquema XDM do Experience Platform para este tipo de evento. Use esta opção quando os eventos forem capturados em um esquema conhecido.

1. Quando as marcas enviam eventos em seu próprio formato JSON, cole as cadeias de caracteres no **[!UICONTROL Esquema]** e no **[!UICONTROL Transformador]** para que o [!DNL Journey Optimizer] possa identificar os dados, analisá-los e decidir se deseja rastreá-los.

   * **[!UICONTROL Esquema]** — Cadeia de caracteres de validação para a carga de entrada.
   * **[!UICONTROL Transformador]** — Expressão de transformação (por exemplo, JSONata) que mapeia sua carga no formato esperado por Desafios de Fidelidade.

1. Salve a definição do evento. Ele aparece na lista **[!UICONTROL Definições de evento]**. Agora você pode usá-lo em desafios. [Saiba como criar desafios](create-challenges.md)

## Estoque de produto {#product-inventory}

A guia **[!UICONTROL Inventário de produto]** permite agrupar itens de catálogo para que você possa direcioná-los em tarefas sem listar cada ID de item. Você carregou um **arquivo CSV** que mapeia cada identificador de item para um ou mais **grupos de produtos** (o mesmo item pode aparecer em vários grupos). Após a importação, esses grupos ficam disponíveis quando você configura a qualificação de tarefas. [Saiba como criar tarefas](create-tasks.md)

1. Prepare um arquivo CSV que mapeie cada identificador de item para um ou mais grupos de produtos. Expanda a seção abaixo para ver um exemplo.

   +++Exemplo de CSV de inventário de produtos

   ![](assets/admin-inventory-csv.png)

   +++

1. Abra a guia **[!UICONTROL Inventário de produto]**.

1. Clique no botão **[!UICONTROL Carregar]** e selecione seu arquivo CSV.

   ![](assets/admin-inventory-upload.png)

1. Revise o arquivo importado na lista de inventário. A lista mostra uma linha por item. Na coluna **[!UICONTROL Grupos incluídos]**, você verá todos os grupos de produtos aos quais o item pertence. Cada grupo aparece como um comprimido (vários comprimidos se o item estiver em vários grupos).

   ![](assets/admin-inventory-imported.png)

1. Para ver todos os itens de um grupo de produtos, selecione a pílula desse grupo na coluna **[!UICONTROL Grupos incluídos]** em qualquer linha. A exibição de detalhes do grupo lista todos os itens no grupo, não apenas o item na linha selecionada.

   ![](assets/admin-inventory-group.png)

1. Use o **[!UICONTROL Histórico de carregamento]** para ver os carregamentos anteriores de arquivos CSV.

## Exclusões {#exclusions}

A guia **[!UICONTROL Exclusões]** permite definir itens de catálogo e grupos que são excluídos em seu programa de fidelidade sem listar cada ID de item em cada tarefa. Você carrega um **arquivo CSV** que mapeia cada identificador de item para um ou mais **grupos de exclusão** (o mesmo item pode aparecer em vários grupos). Após a importação, esses itens e grupos ficam disponíveis no construtor de tarefas: os itens excluídos são marcados automaticamente e não podem ser incluídos em uma tarefa; os grupos de exclusão só podem ser adicionados à lista de exclusão da tarefa, não à lista de inclusão. [Saiba como definir itens qualificados e exclusões em tarefas](create-tasks.md#eligible-items-exclusions)

1. Prepare um arquivo CSV que mapeie cada identificador de item para um ou mais grupos de exclusão. Expanda a seção abaixo para ver um exemplo.

   +++Exemplo de CSV de exclusões

   ![](assets/admin-exclusions-csv.png)

   +++

1. Abra a guia **[!UICONTROL Exclusões]**.

1. Clique no botão **[!UICONTROL Carregar]** e selecione seu arquivo CSV.

   ![](assets/admin-exclusions-upload.png)

1. Revise o arquivo importado na lista de exclusões. A lista mostra uma linha por item. Na coluna **[!UICONTROL Grupos incluídos em]**, você verá todos os grupos de exclusão aos quais o item pertence. Cada grupo aparece como um comprimido (vários comprimidos se o item estiver em vários grupos).

1. Para ver cada item em um grupo de exclusão, selecione o comprimido desse grupo na coluna **[!UICONTROL Grupos incluídos em]** em qualquer linha. A exibição de detalhes do grupo lista todos os itens no grupo, não apenas o item na linha selecionada.

1. Use o **[!UICONTROL Histórico de carregamento]** para ver os carregamentos anteriores de arquivos CSV.
