---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o programa de fidelidade
description: Saiba como configurar provedores de recompensa, definições de eventos e configurações no nível da organização para seu programa de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 2%

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
>Este recurso está atualmente em **beta privado**. Para obter detalhes completos sobre o ciclo de lançamento e as fases de disponibilidade, consulte o [ciclo de lançamento do Journey Optimizer](../rn/releases.md).

A seção **[!UICONTROL Administrador de Fidelidade]** é onde você configura como o Journey Optimizer se conecta aos seus sistemas de fidelidade externos. Os profissionais de marketing usam o **[!UICONTROL Loyalty Challenges (Beta)]** para projetar desafios, tarefas, conteúdo e mensagens. O **[!UICONTROL Administrador de Fidelidade]** é uma área separada, somente de administrador, para preenchimento de premiação, mapeamento de eventos e inventário de produtos.

Quando um cliente conclui um desafio ou atinge um marco de recompensa, a Journey Optimizer chama o provedor de recompensa configurado para fornecer pontos ou outras recompensas. A configuração em **[!UICONTROL Admin de Fidelidade]** não afeta as configurações de desafio **[!UICONTROL Conteúdo]**, **[!UICONTROL Mensagens]** ou **[!UICONTROL Público]** — elas permanecem sob o controle do profissional de marketing.

## O que você configura aqui em relação aos desafios de fidelidade {#scope}

| Área | Configurado no Administrador de fidelidade | Configurado em desafios de fidelidade |
|------|----------------------------|----------------------------------|
| API de atendimento de premiação | Sim — provedores de recompensa | Não — selecionar somente provedor e valores |
| Mapeamento de eventos para atividades personalizadas | Sim — definições de evento | Não — selecione o nome do evento nas tarefas de evento Personalizadas |
| Mapeamentos do grupo de produtos | Sim — inventário de produtos | Não — use grupos ao criar tarefas de Compra/Gasto |
| Estrutura de desafio, conteúdo, público-alvo | Não | Sim |

O Adobe Journey Optimizer envia chamadas de atendimento para seu provedor de premiação quando os clientes recebem recompensas. Sua plataforma de fidelidade é responsável por creditar a conta do membro.

## Pré-requisitos {#prerequisites}

O **[!UICONTROL Administrador de Fidelidade]** destina-se a um pequeno número de administradores por organização. Além das permissões necessárias para [Desafios de Fidelidade](get-started.md#prerequisites), você precisa de acesso de nível de administrador para sua instância do Journey Optimizer. Entre em contato com o administrador do Adobe para solicitar acesso.

## Acessar administrador de fidelidade {#access-loyalty-admin}

Para abrir o **[!UICONTROL Administrador de Fidelidade]**, selecione-o na navegação à esquerda no Journey Optimizer.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

O **[!UICONTROL Administrador de Fidelidade]** está organizado em guias: **[!UICONTROL Configurações globais]**, **[!UICONTROL Provedores de recompensa]**, **[!UICONTROL Definições de eventos]** e **[!UICONTROL Inventário de produtos]**. As guias disponíveis para você dependem das permissões da organização e da configuração de recursos.

## Configurações globais {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configurações globais"
>abstract="Selecione o namespace de identidade da Adobe Experience Platform para seu programa de fidelidade e copie sua ID de configuração. Essas configurações no nível da organização são necessárias antes que os provedores de recompensa possam cumprir as recompensas corretamente."

Use as **[!UICONTROL Configurações globais]** para definir as opções de toda a organização para os Desafios de Fidelidade.

1. Abra a guia **[!UICONTROL Configurações globais]**.

1. Na lista suspensa **[!UICONTROL Namespace]**, selecione o [namespace de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces) usado pelo seu programa de fidelidade.

1. Selecione **[!UICONTROL Salvar]** para aplicar o namespace à sua configuração de Desafios de Fidelidade.

1. Copie a **[!UICONTROL ID de Configuração]** quando precisar compartilhá-la com sua equipe de implementação ou sistemas externos — por exemplo, ao configurar a entrega de eventos de entrada.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Provedores de recompensa {#reward-providers}

Um **provedor de premiação** informa à Journey Optimizer para onde enviar chamadas de atendimento quando o progresso do desafio é registrado ou um desafio é concluído — por exemplo, uma API que credita pontos de fidelidade ou estrelas a uma conta de membro.

Uma configuração de provedor de premiação inclui:

* Detalhes básicos da conexão (nome, descrição, URL da API, cabeçalhos)
* **[!UICONTROL Definições de recompensa]** — os tipos de recompensa que este provedor pode emitir (por exemplo, estrelas ou milhas)
* **[!UICONTROL Proxies de recompensa]** (opcional) — um proxy intermediário através do qual as chamadas são roteadas em vez do seu ponto de extremidade diretamente
* **[!UICONTROL Geradores de token de autenticação]** — o mecanismo que a Journey Optimizer usa para obter tokens de acesso antes de chamar sua API

### Criar um provedor de premiação {#create-reward-provider}

1. Abra a guia **[!UICONTROL Provedores de recompensa]** e selecione **[!UICONTROL Criar provedor de recompensa]**.

1. Insira um **[!UICONTROL Nome]**, **[!UICONTROL Descrição]** e a **[!UICONTROL URL da API]** que recebe solicitações de atendimento.

1. Adicione **[!UICONTROL Cabeçalhos]** conforme necessário para sua API (por exemplo, chaves de API ou tipos de conteúdo).

1. Configurar **[!UICONTROL Definições de recompensa]** — uma entrada por tipo de recompensa que seu provedor suporta (por exemplo, pontos de programa ou estrelas). Para cada definição:

   * Especifique a **carga** enviada com chamadas de atendimento.
   * Opcionalmente, marque uma definição como **padrão** para este provedor.

1. Opcionalmente, configure um **[!UICONTROL Proxy de recompensa]** para rotear chamadas de atendimento por meio de um servidor intermediário:

   * **[!UICONTROL Nome]**, **[!UICONTROL Descrição]** e se o proxy está **habilitado**
   * **[!UICONTROL Host]**, **[!UICONTROL Porta]** e credenciais

1. Configure um **[!UICONTROL Gerador de token de autenticação]** se sua API exigir um token de portador para autenticação:

   * URL do ponto de extremidade do token e método HTTP (por exemplo, **POST** para fluxos no estilo OAuth)
   * **[!UICONTROL Chave do token]** na resposta (por exemplo, `access_token`)
   * Cabeçalhos exigidos pelo endpoint do token

   O Journey Optimizer usa essa configuração para obter um token novo antes de chamar a API de recompensa.

1. Selecione **[!UICONTROL Criar provedor de premiação]**. O provedor e todos os recursos secundários configurados são salvos juntos.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Depois de salvar, o provedor é exibido na lista de provedores de premiação. Os profissionais de marketing selecionam esse provedor ao [configurar recompensas por desafio](create-challenges.md#rewards).

Para editar um provedor de premiação existente, abra a guia **[!UICONTROL Provedores de premiação]**, selecione o provedor e atualize os campos no local. As alterações nos recursos secundários (definições de recompensa, proxies, geradores de token de autenticação) são salvas ao atualizá-los.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL Traga seus próprios dados]** Os desafios preenchem as recompensas por meio de sua própria integração de dados. Os provedores de recompensa configurados aqui não se aplicam a esses desafios. [Saiba mais sobre como Trazer seus próprios desafios de dados](create-challenges.md#create-the-challenge).

## Definições de evento (opcional) {#event-definitions}

**[!UICONTROL Definições de eventos]** mapeie os eventos de experiência dos seus sistemas (em qualquer formato JSON ou XDM que sua marca use) para atividades nas quais os Desafios de Fidelidade podem agir, principalmente as tarefas de **[!UICONTROL Evento personalizado]**. Quando os eventos chegam, o Journey Optimizer usa essas definições para decidir se eles devem ser processados. Eventos que não correspondem a nenhuma definição são ignorados.

### Criar uma definição de evento {#create-event-definition}

1. Abra a guia **[!UICONTROL Definições de eventos]** e crie uma nova definição.

1. Insira um **[!UICONTROL Nome]** para o evento (por exemplo, `Coffee purchase`). Esse é o nome que os profissionais de marketing veem ao configurar uma tarefa de **[!UICONTROL Evento personalizado]**.

1. Especifique como identificar o evento nas cargas recebidas:

   * **[!UICONTROL Caminho do identificador]** — Caminho JSON para o campo que identifica o evento ou membro (por exemplo, `data.memberId`)
   * **[!UICONTROL Valores de identificador]** — valores que devem estar presentes para que esta definição corresponda

1. Opcionalmente, especifique uma **[!UICONTROL ID do esquema XDM]** se suas cargas de evento estiverem em conformidade com um esquema do Experience Platform.

1. Opcionalmente, use os campos **[!UICONTROL Esquema]** e **[!UICONTROL Transformador]** para fornecer strings de esquema e transformação personalizadas para analisar e validar o JSON recebido.

   Você pode fornecer uma ID de esquema XDM, um caminho de identificador ou ambos, dependendo de como seus eventos são estruturados.

1. Salve a definição do evento.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

A maioria das organizações cria várias definições de evento — uma por atividade que desejam rastrear (por exemplo, compra, check-in ou visita ao local). [Saiba como usar tarefas de evento personalizadas em desafios](create-tasks.md#choose-activity).

## Inventário do produto (opcional) {#product-inventory}

Use a guia **[!UICONTROL Inventário de produto]** para carregar um arquivo CSV que mapeie identificadores de produto ou item (por exemplo, IDs MPG) para grupos de produtos. Em seguida, os profissionais de marketing podem fazer referência a esses grupos nas regras de qualificação de tarefa, em vez de digitar SKUs individuais.

1. Abra a guia **[!UICONTROL Inventário de produto]**.

1. Faça upload do seu arquivo de mapeamento.

1. Revise os mapeamentos importados na lista de inventário. Selecione um grupo de produtos para ver todos os itens desse grupo ou use a pesquisa para localizar itens por nome ou ID.

1. Use o **[!UICONTROL Histórico de carregamento]** para ver os carregamentos anteriores.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Exclusões globais]** para o inventário de produtos estão planejadas para uma versão futura e não estão documentadas aqui.
