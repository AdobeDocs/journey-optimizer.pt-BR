---
solution: Journey Optimizer
product: journey optimizer
title: Configurar o programa de fidelidade
description: Saiba como configurar provedores de recompensa, definições de eventos e configurações de organização para seu programa de fidelidade no Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privado" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: aea783bd8f2351d4a5d8aa6b84c24a713a6c0306
workflow-type: tm+mt
source-wordcount: '1221'
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

A seção **[!UICONTROL Administrador de Fidelidade]** é onde você configura como o Journey Optimizer se conecta ao back-end do seu programa de fidelidade. Os profissionais de marketing usam o **[!UICONTROL Loyalty Challenges (Beta)]** para projetar desafios, tarefas, conteúdo e mensagens; o Loyalty Admin é uma configuração separada e única para cumprimento de premiação e mapeamento de eventos.

Quando um cliente conclui um desafio (ou atinge um marco de premiação), a Journey Optimizer chama o provedor de premiação configurado aqui para fornecer pontos ou outras recompensas. As configurações de **[!UICONTROL Conteúdo]**, **[!UICONTROL Mensagens]** e **[!UICONTROL Público]** do desafio não são afetadas pela configuração de Administrador de Fidelidade.

## Acessar administrador de fidelidade {#access-loyalty-admin}

Para abrir o Administrador de Fidelidade, entre no Journey Optimizer e selecione **[!UICONTROL Administrador de Fidelidade]** na navegação à esquerda.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

A interface do administrador é organizada em guias. Dependendo da sua organização, você pode ver **[!UICONTROL Configurações globais]**, **[!UICONTROL Provedores de recompensa]**, **[!UICONTROL Definições de eventos]** e **[!UICONTROL Inventário de produtos]**.

## Configurações globais {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Configurações globais"
>abstract="Selecione o namespace de identidade da Adobe Experience Platform para seu programa de fidelidade e copie sua ID de configuração. Essas configurações no nível da organização são necessárias antes que os provedores de recompensa possam cumprir as recompensas corretamente."

Use **[!UICONTROL Configurações globais]** para configurar opções em toda a organização para Desafios de Fidelidade.

1. Abra a guia **[!UICONTROL Configurações globais]**.

1. No menu suspenso **[!UICONTROL Namespace]**, selecione o [namespace de identidade](https://experienceleague.adobe.com/pt-br/docs/experience-platform/identity/features/namespaces) da Adobe Experience Platform que seu programa de fidelidade usa. Selecione **[!UICONTROL Salvar]** para atualizar o namespace na configuração de Desafios de Fidelidade da sua organização.

1. Copie a **[!UICONTROL ID de Configuração]** se precisar compartilhá-la com sua equipe de implementação ou sistemas externos.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Provedores de recompensa {#reward-providers}

Um **provedor de premiação** informa à Journey Optimizer para onde enviar chamadas de atendimento quando o progresso do desafio é registrado ou um desafio é concluído, por exemplo, uma API que credita pontos de fidelidade ou estrelas a uma conta de membro.

Um provedor de premiação inclui:

* Detalhes básicos da conexão (nome, descrição, URL da API, cabeçalhos)
* **[!UICONTROL Definições de recompensa]** — tipos de recompensa que este provedor pode emitir (por exemplo, estrelas ou milhas)
* **[!UICONTROL Proxies de recompensa]** (opcional) — encaminhe chamadas através de um proxy em vez de diretamente para o seu ponto de extremidade
* **[!UICONTROL Geradores de token de autenticação]** — como a Journey Optimizer obtém tokens de acesso antes de chamar sua API

### Criar um provedor de premiação {#create-reward-provider}

Siga estas etapas para registrar um novo provedor de premiação e seus recursos relacionados.

1. Abra a guia **[!UICONTROL Provedores de recompensa]** e comece a criar um provedor.

1. Insira um **[!UICONTROL Nome]** e uma **[!UICONTROL Descrição]** e a **[!UICONTROL URL da API]** para onde as solicitações de atendimento são enviadas.

1. Adicione **[!UICONTROL Cabeçalhos]** conforme necessário para sua API (por exemplo, chaves de API ou tipos de conteúdo). É possível adicionar ou remover linhas de cabeçalho na interface do usuário do.

1. Configurar **[!UICONTROL definições de recompensa]**:

   * Defina cada tipo de premiação que seu provedor aceita (por exemplo, pontos ou estrelas do programa).
   * Opcionalmente, marque uma definição como **padrão** para esse provedor.
   * Especifique a **carga** enviada com chamadas de preenchimento para cada definição.

1. Opcionalmente, configure um **[!UICONTROL Proxy de recompensa]**:

   * **[!UICONTROL Host]**, **[!UICONTROL Porta]** e credenciais
   * **[!UICONTROL Nome]**, **[!UICONTROL Descrição]** e se o proxy está **habilitado**

1. Configure um **[!UICONTROL Gerador de token de autenticação]** se sua API exigir um token antes de cada chamada:

   * URL do ponto de extremidade do token e método HTTP (por exemplo, **POST** para fluxos no estilo OAuth)
   * **[!UICONTROL Chave do token]** na resposta (por exemplo, `access_token`)
   * Cabeçalhos exigidos pelo endpoint do token

   O Journey Optimizer solicita um token dessa configuração antes de chamar sua API de recompensa para que as chamadas usem uma credencial atual.

1. Selecione **[!UICONTROL Criar Provedor de Premiação]**. O provedor e seus recursos secundários (definições, proxy e gerador de token) são criados juntos.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Após a criação, o provedor será exibido na lista de provedores de recompensa. Os profissionais de marketing selecionam esse provedor ao [configurar recompensas por desafio](create-challenges.md#rewards).

### Editar um provedor de premiação {#edit-reward-provider}

1. Abra a guia **[!UICONTROL Provedores de recompensa]** e selecione um provedor.

1. Atualize o nome, a descrição, o URL ou os cabeçalhos do provedor, conforme necessário.

1. Para alterar as **[!UICONTROL Definições de recompensa]**, os **[!UICONTROL Proxies de recompensa]** ou os **[!UICONTROL Geradores de token de autenticação]**, abra a seção correspondente e edite os campos. As alterações nesses recursos secundários são salvas ao atualizá-las no local.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>Para **[!UICONTROL Traga seus próprios dados]** desafios nos quais tarefas e recompensas são totalmente provenientes de sua integração de dados, os provedores de recompensa configurados aqui podem não se aplicar. [Saiba mais sobre como Trazer seus próprios desafios de dados](create-challenges.md#create-the-challenge).

## Definições de evento {#event-definitions}

**[!UICONTROL Definições de eventos]** mapeie os eventos de experiência recebidos no formato da sua marca para atividades que os Desafios de Fidelidade podem usar, especialmente as tarefas de **[!UICONTROL Evento personalizado]**. Quando os dados chegam de seus canais, o Journey Optimizer usa essas definições para decidir se um evento é relevante e como interpretá-lo. Eventos que não correspondem a nenhuma definição são ignorados.

### Criar uma definição de evento {#create-event-definition}

1. Abra a guia **[!UICONTROL Definições de eventos]** e crie uma nova definição.

1. Digite um **[!UICONTROL Nome]** para o evento (por exemplo, `Coffee purchase`). Esse nome é o que os profissionais de marketing selecionam quando configuram uma tarefa de **[!UICONTROL Evento personalizado]**.

1. Especifique como identificar o evento nas cargas recebidas:

   * **[!UICONTROL Caminho do identificador]** — Caminho JSON para o campo que identifica o evento ou membro (por exemplo, `data.memberId`)
   * **[!UICONTROL Valores de identificador]** — valores que devem estar presentes para que esta definição corresponda

1. Opcionalmente, especifique uma **[!UICONTROL ID de esquema XDM]** e/ou use os campos **[!UICONTROL Esquema]** e **[!UICONTROL Transformador]** para colar cadeias de caracteres de esquema e transformação que sua equipe usa para analisar e validar o JSON recebido antes do processamento.

   Você pode fornecer uma ID de esquema XDM, um caminho de identificador ou ambos, dependendo de como seus eventos são estruturados.

1. Salve a definição do evento.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

A maioria das organizações cria várias definições de evento — uma por atividade que desejam rastrear (por exemplo, compra, check-in ou visita ao local). [Saiba como usar tarefas de evento personalizadas em desafios](create-tasks.md#choose-activity).

## Estoque de produto {#product-inventory}

A guia **[!UICONTROL Estoque de produto]** permite carregar um arquivo CSV para mapear identificadores de produto ou item (por exemplo, IDs MPG) para grupos de produtos usados na qualificação de tarefas. Isso oferece suporte a cenários em que as tarefas fazem referência a produtos agrupados, em vez de SKUs individuais digitadas manualmente.

1. Abra a guia **[!UICONTROL Inventário de produto]**.

1. Faça upload do arquivo de mapeamento arrastando-o para a área de upload ou navegando para selecioná-lo.

1. Revise os mapeamentos importados na lista de inventário. Selecione um grupo de produtos para ver todos os itens desse grupo. Use a pesquisa para localizar itens por nome ou ID.

1. Use o **[!UICONTROL Histórico de carregamento]** para ver os carregamentos anteriores.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Exclusões globais]** para o inventário de produtos estão planejadas para uma versão futura e não estão documentadas aqui.

## Como o administrador de fidelidade se relaciona com os desafios {#how-admin-relates-to-challenges}

| Área | Configurado no Administrador de fidelidade | Configurado em desafios de fidelidade |
|------|----------------------------|----------------------------------|
| API de atendimento de premiação | Sim — provedores de recompensa | Não — selecionar somente provedor e valores |
| Mapeamento de eventos para atividades personalizadas | Sim — definições de evento | Não — selecione o nome do evento nas tarefas de evento Personalizadas |
| Mapeamentos do grupo de produtos | Sim — inventário de produtos | Não — use grupos ao criar tarefas de Compra/Gasto |
| Estrutura de desafio, conteúdo, público-alvo | Não | Sim |

Ordem de configuração típica:

1. Defina as **[!UICONTROL Configurações globais]** e pelo menos um **[!UICONTROL Provedor de recompensa]** no Administrador de Fidelidade.
1. Opcionalmente, adicione as **[!UICONTROL Definições de evento]** e o **[!UICONTROL Inventário de produto]** se o programa usar eventos personalizados ou grupos de produtos baseados em CSV.
1. Crie [tarefas](create-tasks.md) e [desafios](create-challenges.md) em **[!UICONTROL Desafios de Fidelidade (Beta)]**, selecionando o provedor de premiação e as definições configuradas.

O Adobe Journey Optimizer envia chamadas de atendimento para seu provedor quando os clientes ganham recompensas; sua plataforma de fidelidade é proprietária do crédito na conta do membro.

## Pré-requisitos {#prerequisites}

O Administrador de fidelidade destina-se a um pequeno conjunto de administradores em sua organização. Além das permissões necessárias para [Desafios de Fidelidade](get-started.md#prerequisites), você precisa de acesso para definir as configurações de fidelidade no nível da organização.

Entre em contato com o administrador se o **[!UICONTROL Administrador de Fidelidade]** não aparecer na navegação à esquerda ou se você não puder salvar configurações globais ou provedores de premiação.
