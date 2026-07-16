---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações do Journey Optimizer
description: Saiba mais sobre as medidas de proteção do Journey Optimizer
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: fa7bbe1ed725874467ac3bb6c7e432b3afda52b5
workflow-type: tm+mt
source-wordcount: 4612
ht-degree: 94%

---


# Medidas de proteção e limitações {#limitations}

>[!BEGINSHADEBOX]

**Nesta página:** revise os limites de sistema, jornada, público-alvo, canal e conteúdo do Adobe Journey Optimizer para planejar implantações que sejam dimensionadas sem falhas.

>[!ENDSHADEBOX]

Abaixo são encontradas medidas de proteção e limitações ao usar o [!DNL Adobe Journey Optimizer].

Os direitos, as limitações e as medidas de proteção de desempenho estão listados na [página de descrição do Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

>[!CAUTION]
>
>* [As medidas de proteção para dados e segmentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/guardrails){target="_blank"} também se aplicam ao Adobe Journey Optimizer.
>
>* Consulte também [Medidas de proteção para a ingestão de dados no perfil do cliente em tempo real](https://experienceleague.adobe.com/pt-br/docs/experience-platform/ingestion/guardrails){target="_blank"}


## Sistema e plataforma {#system-platform}

### Navegadores compatíveis {#browsers}

A interface do Adobe [!DNL Journey Optimizer] foi projetada para funcionar de maneira ideal na versão mais recente do Google Chrome. Você pode ter problemas ao usar determinados recursos em versões mais antigas ou outros navegadores.

### Medidas de proteção de conjuntos de dados {#datasets-guardrails}

A partir de fevereiro de 2025, uma medida de proteção de tempo de vida (TTL) será implantada nos conjuntos de dados gerados pelo sistema do Journey Optimizer para **novas sandboxes e organizações** da seguinte maneira:

* **90 dias** para os dados na loja de perfis
* **13 meses** para dados no data lake

Essa alteração será implementada nas **sandboxes de clientes existentes** em uma próxima fase. [Saiba mais sobre as medidas de proteção de tempo de vida (TTL) dos conjuntos de dados](../data/datasets-ttl.md)

## Jornadas {#journeys-guardrails}

Esta seção aborda medidas de proteção e limitações para jornadas, incluindo limitações gerais de jornada, componentes de jornada (ações, eventos, fontes de dados), atividades de jornada e recursos específicos, como ações personalizadas e o editor de expressão.

### Medidas de proteção gerais da jornada {#journeys-guardrails-journeys}

* O limite do número de atividades em uma jornada é de **50**. O número de atividades é exibido na seção superior esquerda da tela da jornada.

  Com as jornadas próximas a esse limite, o desempenho de edição e publicação pode ser degradado e podem ocorrer falhas de salvamento ou validação. Se isso acontecer, divida a jornada em subjornadas menores com [atividades de salto](../building-journeys/jump.md) ou recrie-a em uma nova versão. O limite de atividades não pode ser aumentado.

* O número de jornadas ativas, fechadas, pausadas e de execução a seco que podem estar ativas ao mesmo tempo é limitado a **200** em sandboxes de produção e **100** em sandboxes de desenvolvimento. Esse limite é aplicado quando você publica uma jornada. O número atual de jornadas é exibido acima da tela de jornada.

  À medida que você publica jornadas, dimensionaremos e ajustaremos automaticamente para garantir uma máxima taxa de transferência e estabilidade. As jornadas fechadas são contadas somente se forem criadas após a implantação dessa garantia.

>[!NOTE]
>
>Para medidas de proteção em tempo de publicação, as organizações que já excedem um limite quando a medida de proteção é introduzida recebem uma exceção. As jornadas existentes não serão afetadas.

* Ao usar uma qualificação de público-alvo em uma jornada, essa atividade de qualificação de público-alvo pode levar até **10 minutos** para ficar ativa e detectar os perfis que entram ou saem do público-alvo.

* Uma instância de jornada para um perfil tem tamanho máximo de **1 MB**. Todos os dados coletados como parte da execução da jornada são armazenados nessa instância da jornada. Portanto, dados de um evento de entrada, informações de perfil recuperadas da Adobe Experience Platform, respostas de ações personalizadas etc., são armazenados nessa instância da jornada e afetam o tamanho da jornada. É aconselhável, quando uma jornada inicia com um evento, limitar o tamanho máximo do conteúdo desse evento (por exemplo: abaixo de **800 KB**) para evitar atingir esse limite após algumas atividades durante a execução da jornada. Quando esse limite é atingido, o perfil fica com status de erro e será excluído da jornada.

* Para cada perfil e versão da jornada, o tempo de execução da jornada mantém uma fila interna de até **10 eventos pendentes** enquanto um está sendo processado. Se esse limite for atingido, eventos adicionais serão descartados com o motivo `maxInstanceStackEventsReached` até que a pilha seja esgotada. Consulte [Eventos descartados devido a uma instância de jornada bloqueada](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* Além do tempo limite usado em atividades de jornada, também há um tempo-limite de jornada global que não é exibido na interface e não pode ser alterado. Esse tempo-limite global interrompe o progresso das pessoas na jornada **91 dias** após a sua entrada. [Leia mais](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**O que isso significa para você:** O **limite de 50 atividades** e o **limite de jornadas ativas** são as duas medidas de proteção que a maioria das equipes encontra primeiro ao dimensionar. Planeje a divisão da jornada antecipadamente e divida os momentos de início do Público-alvo de leitura com pelo menos 5 a 10 minutos de intervalo para evitar a contenção da taxa de transferência da sandbox.

#### Validação de tamanho do conteúdo da jornada {#journey-payload-size}

Ao salvar ou publicar uma jornada, o Journey Optimizer valida o tamanho total do conteúdo da jornada para preservar a estabilidade e o desempenho.

| Cenário | Limite | Comportamento |
|---|---|---|
| Conteúdo &lt; 90% do limite | Aviso abaixo | A jornada é salva e publicada com sucesso. Nenhum aviso ou erro é exibido. |
| Conteúdo em 90% a 99% do limite | Aviso (leve) | A jornada é salva e publicada com um aviso: **Aviso**: o tamanho do conteúdo da jornada está próximo ao limite. Maior nó: &#39;[NodeName]&#39; (tipo: &#39;[NodeType]&#39;, tamanho: [N] bytes). |
| Conteúdo ≥ 100% do limite | **Erro (grave)** | Salvamento ou publicação bloqueado. Retorna **HTTP 413 Entidade da solicitação muito grande**. Erro: o tamanho do conteúdo da jornada excede o limite. Maior nó: &#39;[NodeName]&#39; (tipo: &#39;[NodeType]&#39;, tamanho: [N] bytes). |

**Configuração padrão**

* **Tamanho máximo de solicitação padrão**:**2 MB** (2.000.000 bytes). Algumas organizações podem ter limites personalizados configurados pela Adobe.
* **Limite de aviso**: 90% do limite máximo.
* **Limite de erro**: 100% do limite máximo.

**Solução de problemas e recomendações**

* Revise o maior nó destacado no aviso ou erro.
* Simplifique condições, reduza mapeamentos de dados e remova etapas ou parâmetros desnecessários.
* Considere dividir a jornada em jornadas menores, se necessário.
* Se você acredita que sua organização precisa de um limite mais alto, entre em contato com o representante da Adobe.

Para monitorar o tamanho do conteúdo atual da jornada antes da publicação, use o indicador **[!UICONTROL Tamanho do conteúdo da jornada atual]** no painel de propriedades da jornada. [Saiba como verificar o tamanho do conteúdo da jornada](../building-journeys/journey-properties.md#journey-payload-size)

### Comparação de pacotes de licenças {#select-package-limitations}

>[!NOTE]
>
>As limitações do pacote Seleção abaixo não se aplicam às jornadas Público-alvo de leitura ou Evento de negócios. Se precisar de uma lógica de jornada mais complexa com várias ações, condições ou atividades de espera, considere atualizar o pacote de licenças ou usar jornadas Público-alvo de leitura, quando aplicável.

Para clientes com o pacote de licenças **Seleção**, as seguintes limitações adicionais se aplicam, especificamente, a jornadas unitárias (jornadas que começam com um evento ou uma qualificação de público-alvo):

| Limitação | Código de erro | Descrição |
|---|---|---|
| Apenas uma ação permitida | `ERR_PKG_SELECT_8` | As jornadas unitárias podem conter apenas **uma** atividade de ação. Várias atividades de email, push, SMS ou outras atividades de ação não são permitidas na mesma jornada. |
| Nenhuma condição permitida | `ERR_PKG_SELECT_7` | As Atividades de condição não podem ser usadas em jornadas unitárias. A jornada deve seguir um único caminho linear sem lógica de ramificação. |
| Nenhuma atividade de espera | `ERR_PKG_SELECT_6` | As Atividades de espera não podem ser adicionadas a jornadas unitárias. As ações devem ser executadas imediatamente, sem atrasos. |
| As transições de tempo-limite/erro devem ir para o nó final | `ERR_PKG_SELECT_2` | Se você configurar transições de tempo-limite ou de erro para uma ação (por exemplo, uma ação de email), esses caminhos deverão apontar diretamente para um nó final. Eles não podem se conectar a outras atividades ou ações na jornada. |

>[!TIP]
>
>**O que isso significa para você:** se estiver no pacote Select e precisar de lógica de ramificação, atividades de espera ou várias ações, use uma jornada de Público-alvo de leitura ou entre em contato com o representante da Adobe para saber como atualizar o pacote.

### Versões de jornada {#journey-versions-g}

As seguintes medidas de proteção se aplicam às [versões da jornada](../start/user-interface.md):

* Uma jornada que começa com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com um evento de **Qualificação de público-alvo**.
* Uma jornada que começa com uma atividade de **Qualificação de público-alvo** em v1 deve sempre começar com uma **Qualificação de público-alvo** em outras versões.
* O público-alvo e o namespace escolhidos na **Qualificação de público-alvo** (primeiro nó) não podem ser alterados em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões da jornada.
* Uma jornada que começa com um **Público-alvo de leitura** não pode começar com outro evento nas próximas versões.
* Não é possível criar uma nova versão de uma jornada de público-alvo de leitura com leitura incremental. Você precisa duplicar a jornada.

### Criação de jornadas e perfis {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API na Adobe Experience Platform. A Meta de nível de serviço (SLT), em termos de latência, é inferior a 1 minuto da ingestão até o Perfil unificado para o percentil 95 das solicitações, em um volume de **20 mil solicitações por segundo (RPS)**.

Se uma jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera depois do primeiro evento para conceder à Adobe Experience Platform o tempo necessário para executar a ingestão no Serviço de Perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento de experiência pode conter informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc.).

### Eventos {#events-g}

As seguintes medidas de proteção se aplicam aos [eventos](../event/about-events.md) de jornadas:

* A Journey Optimizer oferece suporte a um volume máximo de **5.000 eventos de jornada de entrada por segundo** para eventos unitários e de **5.000 eventos de jornada de entrada por segundo** para eventos de jornada baseados em Leitura de público-alvo, em todas as sandboxes. Saiba mais sobre essa limitação [nesta página](../event/about-events.md#event-thoughput).
* As jornadas acionadas por evento podem levar até **5 minutos** para processar a primeira ação na jornada.
* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada ao conteúdo de transmissão que entra na Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.
* Os eventos de negócios não podem ser usados junto com eventos unitários ou atividades de qualificação de público-alvo.
* Um único evento pode ser referenciado por no máximo **25** jornadas a qualquer momento, em todas as jornadas ativas e fechadas. Quando esse limite for atingido, a publicação de qualquer jornada adicional que use esse evento será bloqueada.
* Um único esquema XDM pode ser referenciado por no máximo **100** eventos em todas as jornadas ativas e fechadas de uma só vez. Quando esse limite for atingido, a publicação de qualquer jornada com um nó de evento que faça referência a esse esquema será bloqueada.
* As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada do perfil é temporariamente bloqueada por **5 minutos**. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (seja o mesmo evento ou outro que está acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.
* O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço Principal de Coleção de Dados (DCCS) para acionar uma jornada. Eventos assimilados em lote, eventos inseridos via **Serviço de consulta**, ou eventos de conjuntos de dados internos do Journey Optimizer (Feedback de mensagens, Rastreamento de email etc.) não podem ser usados para acionar uma jornada. Para casos de uso nos quais não é possível obter os eventos transmitidos, é necessário criar um público-alvo com base nesses eventos e usar a atividade **Público-alvo de leitura**. A qualificação de público-alvo pode ser tecnicamente utilizada, mas não é recomendada, pois pode causar problemas posteriores com base nas ações usadas.

### Fontes de dados {#data-sources-g}

As seguintes medidas de proteção se aplicam às [fontes de dados](../datasource/about-data-sources.md) de jornadas:

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e poder lidar com o volume de solicitações.
* Endereços internos da Adobe (`.adobe.*`) não são permitidos em URLs e APIs.

>[!NOTE]
>
>Como as respostas agora são compatíveis, você deve usar ações personalizadas em vez de fontes de dados para casos de uso de fontes de dados externas.

### Ações gerais {#general-actions-g}

As seguintes medidas de proteção se aplicam às [ações](../building-journeys/about-journey-activities.md) de jornadas:

* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida. Novas tentativas são executadas para todos os erros HTTP, exceto para HTTP 401, 403 e 404.
* O evento **Reação** integrado permite que você reaja a ações predefinidas. Saiba mais [nesta página](../building-journeys/reaction-events.md). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.
* Um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo, em todas as [versões ativas da jornada](../building-journeys/publish-journey.md#journey-create-new-version). Se a reentrada estiver habilitada, um perfil poderá entrar novamente em uma jornada, mas não até que tenha saído totalmente da instância anterior da jornada. [Leia mais](../building-journeys/end-journey.md)

### Ações personalizadas {#custom-actions-g}

As seguintes medidas de proteção se aplicam às [ações personalizadas](../action/action.md) de jornadas:

* Um limite de **300.000 chamadas em um minuto** é definido para todas as ações personalizadas, por host e por sandbox. Esse limite é aplicado como uma janela deslizante por sandbox e por ponto de acesso para pontos de acesso com tempos de resposta inferiores a 0,75 segundos. Módulos no Designer de emailPara pontos de acesso com tempos de resposta maiores que 0,75 segundo, um limite separado de **150.000 chamadas por 30 segundos** (também uma janela deslizante) é aplicado.
* O URL de ação personalizada não aceita parâmetros dinâmicos.
* Os métodos de chamada POST, PUT e GET são compatíveis.
* O nome do parâmetro de consulta ou cabeçalho não deve começar com “.” ou &quot;$&quot;.
* Endereços IP não são permitidos em URLs. Em vez disso, use nomes de host.
* Endereços internos da Adobe (`.adobe.*`) não são permitidos em URLs e APIs.
* As ações personalizadas integradas não podem ser removidas.
* As ações personalizadas são compatíveis com o formato JSON somente ao usar conteúdos de solicitação ou resposta. Consulte [esta página](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Qualquer ponto de acesso alvo de uma ação personalizada deve aceitar pelo menos **200 TPS**. Tenha cuidado, pois uma configuração de limitação não pode ficar abaixo de 200 TPS. Dependendo da taxa de transferência esperada, ter um tempo de resposta alto pode afetar a taxa de transferência real.

>[!TIP]
>
>**O que isso significa para você:** o limite padrão de 300.000 chamadas/min protege seus pontos de acesso externos contra sobrecarga da taxa de transferência da jornada. Se o seu ponto de acesso puder manipular mais carga, você poderá aumentar esse limite usando a [API de limite](../configuration/capping.md) ou a [API de limitação](../configuration/throttling.md). Para obter uma visão geral mais ampla de como o Journey Optimizer se conecta a sistemas externos, consulte [esta página](../configuration/external-systems.md). Entre em contato com o representante da Adobe se precisar de um limite organizacional mais alto.

### Identificadores suplementares {#supplemental}

Existem medidas de proteção específicas para o uso de identificadores suplementares em jornadas. Elas são listadas [nesta página](../building-journeys/supplemental-identifier.md#guardrails).

### Editor de expressão {#expression-editor}

As seguintes medidas de proteção se aplicam ao [editor de expressão da jornada](../building-journeys/expression/expressionadvanced.md):

* Os grupos de campos de evento de experiência não podem ser usados em jornadas que comecem com atividades de público-alvo de leitura, qualificação de público-alvo ou de evento de negócios. É necessário criar um novo público-alvo e usar uma condição `inaudience` na jornada.
* Não é possível usar atributos `timeSeriesEvents` no editor de expressão. Para acessar eventos de experiência em nível de perfil, crie um novo grupo de campos com base em um esquema `XDM ExperienceEvent`.

### Atividades de jornada {#activities}

#### Atividade de qualificação de público-alvo {#audience-qualif-g}

As seguintes medidas de proteção se aplicam à atividade de jornada [Qualificação de público-alvo](../building-journeys/audience-qualification-events.md):

* A atividade Qualificação de público-alvo não pode ser usada com atividades do Adobe Campaign.
* Identificadores suplementares não são aceitos para jornadas de qualificação de público-alvo.
* Uma sandbox pode incluir no máximo **300** nós de qualificação de público-alvo em todas as jornadas ativas e fechadas. Quando esse limite é atingido, a publicação de jornadas com nós de Qualificação de público-alvo adicionais é bloqueada.

Saiba mais sobre taxas de processamento e limites de taxa de transferência da jornada [nesta seção](../building-journeys/entry-management.md#journey-processing-rate).

Medidas de proteção adicionais — incluindo recomendações sobre públicos-alvo de streaming x em lote e limitações de público de composição — estão listadas [nesta página](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails).

#### Atividades do Campaign {#ac-g}

As seguintes medidas de proteção se aplicam às atividades do **[!UICONTROL Campaign v7/v8]** e **[!UICONTROL Campaign Standard]**:

* As atividades do Adobe Campaign não podem ser usadas com uma atividade Público-alvo de leitura ou Qualificação de público-alvo.
* As atividades do **[!UICONTROL Campaign Standard]** não podem ser usadas com outras atividades de canal: Cartão, Experiência baseada em código, Email, Push, SMS, Mensagens no aplicativo, Web.
* As atividades do **[!UICONTROL Campaign v7/v8]** podem ser usadas junto com atividades de canal nativas na mesma jornada.

#### Eventos de reação {#reaction-events-g}

Medidas de proteção específicas se aplicam a eventos de **[!UICONTROL Reação]**, incluindo o requisito de colocar a atividade imediatamente após uma ação de canal e a incapacidade de rastrear mensagens enviadas em uma jornada diferente. Elas são listadas [nesta página](../building-journeys/reaction-events.md#guardrails-limitations).

#### Atividade no aplicativo {#in-app-activity-limitations}

As seguintes medidas de proteção se aplicam à ação de **[!UICONTROL mensagem no aplicativo]**. Saiba mais sobre mensagens no aplicativo [nesta página](../in-app/create-in-app.md).

* No momento, esse recurso não está disponível para clientes do Healthcare.

* A personalização pode conter apenas atributos de perfil.

* A atividade no aplicativo não pode ser usada com atividades do **[!UICONTROL Campaign Standard]**.

* A exibição no aplicativo está vinculada à duração da jornada, o que significa que, quando a jornada terminar para um perfil, todas as mensagens no aplicativo dentro dessa jornada deixarão de ser exibidas para esse perfil. Consequentemente, não é possível interromper uma mensagem no aplicativo diretamente de uma atividade da jornada. Em vez disso, será necessário encerrar toda a jornada para impedir que as mensagens No aplicativo sejam exibidas no perfil.

* No modo de teste, a exibição no aplicativo depende da duração da jornada. Para evitar que a jornada termine muito cedo durante o teste, ajuste o valor **[!UICONTROL Tempo de espera]** em suas atividades de **[!UICONTROL Espera]**.

* As atividades de **[!UICONTROL Reação]** não podem ser usadas para reagir a uma abertura ou clique no aplicativo.

* Um atraso na ativação pode ocorrer entre o momento em que um perfil de usuário ou usuária alcança uma atividade no aplicativo na tela e o momento em que começa a visualizar essa mensagem no aplicativo.

* O tamanho do conteúdo das mensagens no aplicativo é limitado a **2 MB**. A inclusão de imagens grandes pode prejudicar o processo de publicação.

#### Atividade de decisão de conteúdo {#content-decision-g}

Medidas de proteção específicas se aplicam à atividade de **[!UICONTROL Decisão de conteúdo]**, incluindo um atraso de 48 horas antes que as políticas de consentimento atualizadas entrem em vigor nas políticas de decisão. Elas são listadas [nesta página](../building-journeys/content-decision.md#guardrails).

#### Atividade Salto {#jump-g}

Medidas de proteção específicas se aplicam à atividade **[!UICONTROL Salto]**. Elas são listadas [nesta página](../building-journeys/jump.md#jump-limitations).

#### Atividade Ler público-alvo {#read-segment-g}

As seguintes medidas de proteção se aplicam à atividade de [leitura de público-alvo](../building-journeys/read-audience.md) da jornada:

* Os públicos-alvo transmitidos estão sempre atualizados, mas os públicos-alvo em lote não serão calculados no momento da recuperação. Eles só são avaliados diariamente no momento da avaliação diária do lote.
* Na entrada da jornada, os perfis usam valores de atributo do instantâneo de público-alvo em lote. No entanto, quando um perfil atinge uma atividade de **Espera**, a jornada atualiza automaticamente os atributos do perfil, buscando os dados mais recentes do Serviço de perfil unificado (UPS). Isso significa que os atributos de perfil podem mudar durante a execução da jornada.
* A atividade de **público-alvo de leitura** não pode ser usada com atividades do Adobe Campaign.
* A atividade **Ler público-alvo** só pode ser usada como a primeira atividade em uma jornada ou após uma atividade de evento de negócios.
* Uma jornada só pode ter uma atividade de **público-alvo de leitura**.
* A atividade **Ler público-alvo** pode direcionar somente um público-alvo por jornada. Se vários públicos-alvo forem necessários, mescle-os em um único público-alvo primeiro. [Saiba como combinar públicos-alvo usando fluxos de trabalho de composição](../audience/get-started-audience-orchestration.md).
* Cada organização pode executar até **cinco** instâncias do **Público-alvo de leitura** simultaneamente (agendadas ou acionadas por evento de negócios) em todas as sandboxes e jornadas. Evite ter mais de cinco jornadas com a atividade **Ler público-alvo** começando exatamente ao mesmo tempo; distribua-as com 5 a 10 minutos de intervalo. Saiba mais sobre taxas de processamento de jornada [nesta seção](../building-journeys/entry-management.md#journey-processing-rate).
* Taxa de transferência da sandbox: o sistema gerencia o processamento por sandbox com um máximo de **20.000 perfis por segundo** compartilhados em todas as atividades de **Público-alvo de leitura**. Atividades individuais podem ser configuradas com **500 a 20.000 perfis por segundo**. Se os limites da sandbox forem atingidos, os processos podem ser enfileirados.
* Tempo-limite de execução de processo: os processos de **Público-alvo de leitura** que não podem ser executados em **12 horas** são automaticamente limpas e não serão realizados.
* As novas tentativas são aplicadas por padrão em jornadas acionadas por público-alvo ao recuperar o processo de exportação. Se ocorrer um erro durante a criação do processo de exportação, serão feitas tentativas a cada 10 minutos, por um período máximo de **1 hora**. Depois disso, a jornada é considerada com falha e, portanto, pode ser executada até 1 hora após o horário agendado.
* Para jornadas que usam IDs complementares, a taxa de leitura da atividade **Ler público-alvo** para cada instância de jornada é limitada a um máximo de **500 perfis por segundo**.

>[!TIP]
>
>**O que isso significa para você:** o limite de 5 instâncias simultâneas é uma limitação rígida em toda a organização. Se você tiver várias equipes programando jornadas de leitura de público-alvo, coordene os tempos de início com cuidado. Os processos que perdem a janela de processamento de 12 horas são ignorados silenciosamente — sempre confirme a execução bem-sucedida nos logs da jornada.

Consulte também [recomendações e configuração](../building-journeys/read-audience.md#must-read) para a atividade Ler público-alvo.

#### Atividade Atualizar perfil {#update-profile-g}

Medidas de proteção específicas se aplicam à atividade **[!UICONTROL Atualizar perfil]**. Elas são listadas [nesta página](../building-journeys/update-profiles.md).

#### Pausa na jornada {#pause-g}

Medidas de proteção específicas se aplicam a **jornadas em pausa**, incluindo uma duração máxima de pausa de **14 dias** e um limite de **10 milhões de perfis** em todas as jornadas em pausa na sua organização. Elas são listadas [nesta página](../building-journeys/journey-pause.md#journey-pause-guardrails).

#### Execução de teste da jornada {#dry-run-g}

Medidas de proteção específicas se aplicam a **Execução de teste da jornada**, incluindo a contagem para perfis engajáveis e cotas de jornada ativas. Elas são listadas [nesta página](../building-journeys/journey-dry-run.md#journey-dry-run-limitations).

#### Fragmentos de jornada {#fragments-journey-g}

Medidas de proteção específicas se aplicam a **Fragmentos de jornada**, incluindo no máximo **20 nós por fragmento** e **200 fragmentos ativos por sandbox**. Elas são listadas [nesta página](../building-journeys/journey-fragments.md#guardrails).

#### Envio usando ondas {#waves-g}

Medidas de proteção específicas se aplicam ao **envio em ondas em jornadas**, incluindo um intervalo de 2-10 ondas e um **intervalo mínimo de 30 minutos** entre ondas. Elas são listadas [nesta página](../building-journeys/send-using-waves.md#limitations-guardrails).

#### Simulação de jornada {#simulation-g}

Medidas de proteção específicas se aplicam à **simulação de jornada**. Elas são listadas [nesta página](../building-journeys/simulate-journey.md#limitations).

## Públicos-alvo e perfis {#audiences-profiles}

Esta seção aborda medidas de proteção para gerenciamento de público-alvo, tratamento de perfil e considerações sobre o perfil engajável.

### Medidas de proteção de públicos-alvo e perfis {#audience}

* Você pode publicar até **10 composições de público-alvo** em uma determinada sandbox. Se tiver atingido esse limite, será necessário excluir uma composição para liberar espaço e publicar uma nova.

  Saiba mais sobre a composição de público-alvo [nesta página](../audience/get-started-audience-orchestration.md).

* Ao assimilar dados, os emails fazem distinção entre maiúsculas e minúsculas. Isso significa que perfis duplicados podem ser criados (por exemplo, um perfil para John.Greene@luma.com, outro perfil para john.greene@luma.com) e usados ao direcionar o destinatário correspondente em suas jornadas e campanhas do [!DNL Journey Optimizer].

* Ao direcionar perfis pseudônimos (visitantes não autenticados) com canais de entrada, considere configurar um tempo de vida (TTL) para exclusão automática de perfis com o fim gerenciar a contagem de perfis engajáveis e os custos associados. [Saiba mais](#profile-management-inbound)

## Canais e mensagens {#channel-guardrails}

Esta seção abrange as medidas de proteção para todos os canais de comunicação, incluindo email, SMS, canais de entrada (web, no aplicativo, baseado em código, cartões de conteúdo) e mensagens transacionais.

>[!NOTE]
>
>Em raras circunstâncias, interrupções temporárias em uma região específica podem resultar na exclusão de perfis válidos das jornadas ou de emails marcados incorretamente como rejeições. Depois que os serviços forem restaurados, verifique novamente os registros de jornada, os campos do perfil de consentimento e publique novamente a jornada, se necessário. No caso de uma interrupção do ISP, saiba como remover perfis da lista de supressão [nesta seção](../configuration/manage-suppression-list.md#remove-from-suppression-list).

### Medidas de proteção de email {#message-guardrails}

As seguintes medidas de proteção se aplicam ao [canal de email](../email/get-started-email.md):

* Não é possível usar o mesmo domínio de envio para enviar mensagens de email do [!DNL Adobe Journey Optimizer] e de outro produto, como o [!DNL Adobe Campaign] ou o [!DNL Adobe Marketo Engage] por exemplo.

Ao criar mensagens de email, o sistema verifica as principais configurações e exibe alertas de avisos (recomendações e práticas recomendadas) e erros (bloqueando problemas que impedem teste ou ativação). Saiba mais sobre alertas de email e requisitos de validação [nesta seção](../email/create-email.md#check-email-alerts).

#### Tamanho do conteúdo da mensagem para publicação no jornada {#message-content-size}

Ao publicar jornadas com mensagens de email, o tamanho total do conteúdo da mensagem não deve exceder **2 MB** após o processamento no backend. Durante a publicação, o sistema processa automaticamente o conteúdo da mensagem corrigindo links, imagens e aplicando transformações, o que aumenta o tamanho do conteúdo além do tamanho do conteúdo criado.

>[!CAUTION]
>
>Se o conteúdo final da mensagem processada exceder **2 MB**, a publicação da jornada falhará. Mantenha o conteúdo da sua mensagem bem abaixo de 2 MB — de preferência abaixo de **1 MB** — para permitir uma margem de segurança de 300 a 400 KB para sobrecarga de processamento no servidor.

**Práticas recomendadas para evitar falhas de publicação:**

* Mantenha o conteúdo do email abaixo de **1 MB**
* Minimizar o número de variantes de conteúdo
* Otimizar e compactar imagens antes de adicioná-las a mensagens
* Remover ativos não utilizados e elementos desnecessários do HTML
* Testar o tamanho da mensagem antes de publicar as jornadas na produção

Se a publicação da jornada falhar devido ao tamanho do conteúdo, reduza o conteúdo da mensagem e publique a jornada novamente.

### Medidas de proteção de SMS {#sms-guardrails}

As seguintes medidas de proteção se aplicam ao [canal de SMS](../mobile/get-started-mobile.md):

* Os arquivos de mídia para MMS podem ser incluídos por meio de um URL compatível. Verifique se o arquivo de mídia foi enviado separadamente.
* A sincronização de feedback da mensagem não está disponível no momento para MMS.
* O gerenciamento de consentimento opera no nível do canal SMS para MMS.

### Medidas de proteção de canal de entrada {#inbound-guardrails}

* Para usar ações de [experiência baseada em código](../code-based/get-started-code-based.md) no [!DNL Journey Optimizer] e entregar conteúdo de código que pode ser usado por seus aplicativos, siga os pré-requisitos detalhados [nesta página](../code-based/code-based-prerequisites.md).

* Para acessar e criar [páginas da web](../web/get-started-web.md) na interface do [!DNL Journey Optimizer], siga os pré-requisitos listados [nesta página](../web/web-prerequisites.md).

* Para enviar mensagens no aplicativo nas jornadas e campanhas com o [!DNL Journey Optimizer], siga os pré-requisitos de entrega listados [nesta página](../in-app/inapp-configuration.md).

* Para que o Adobe Journey Optimizer exiba corretamente os cartões de conteúdo, é necessário definir as configurações da Adobe Experience Platform listadas [nesta página](../content-card/content-card-configuration-prereq.md).

* O Journey Optimizer aceita um volume máximo de **5.000 solicitações de entrada por segundo**. Essa medida de proteção se aplica a todas as solicitações de entrada, que podem se originar de qualquer um dos canais de entrada compatíveis com o Journey Optimizer ([web](../web/get-started-web.md), [no aplicativo](../in-app/get-started-in-app.md), [experiências baseadas em código](../code-based/get-started-code-based.md), [cartões de conteúdo](../../rp_landing_pages/content-card-landing-page.md)).

* O Journey Optimizer aceita um máximo de **500 ações de entrada ativas** a qualquer momento. Essas ações de entrada são contadas se fizerem parte de uma campanha ativa ou se forem um nó usado em uma jornada ativa. Ao atingir esse número, é preciso desativar campanhas ou jornadas mais antigas que estejam usando ações de entrada antes de poder lançar novas.

#### Gerenciamento de perfis com canais de entrada {#profile-management-inbound}

Os canais de entrada do [!DNL Journey Optimizer] podem direcionar perfis pseudônimos, ou seja, perfis que ainda não foram autenticados ou conhecidos por não terem sido engajados anteriormente em outros canais. Esse é o caso, por exemplo, ao direcionar todos os visitantes ou públicos-alvo com base em IDs temporárias, como ECID.

Isso aumentará a contagem total de perfis engajáveis, o que pode ter implicações de custo se o número contratual de perfis engajáveis adquiridos for excedido. As métricas de licença de cada pacote estão listadas na página [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. É possível verificar o número de perfis engajáveis no [painel de uso de licença](../audience/license-usage.md).

Para manter os perfis que podem ser engajados dentro de limites razoáveis, a Adobe recomenda configurar um tempo de vida (TTL) para excluir automaticamente perfis pseudônimos do Perfil do cliente em tempo real se eles não tiverem sido vistos ou engajados em uma janela de tempo específica. A Adobe recomenda definir o valor de TTL para **14 dias** para corresponder ao TTL atual do perfil do Edge.

>[!NOTE]
>
>Saiba como configurar a expiração de dados para perfis pseudônimos na [documentação da Experience Platform](https://experienceleague.adobe.com/pt-br/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

### Medidas de proteção de mensagens transacionais {#transactional-message-guardrails}

O Journey Optimizer aceita um volume máximo de **500 mensagens transacionais por segundo** em campanhas.

## Conteúdo e ativos {#content-assets}

Esta seção aborda as medidas de proteção para a criação e o gerenciamento de conteúdo, incluindo páginas de destino, subdomínios e fragmentos.

### Medidas de proteção do Assistente de IA {#ai-assistant-g}

As medidas de proteção e limitações para a **geração de conteúdo do Assistente de IA** — incluindo limitações dos canais com suporte (email, push, web, SMS) e do editor de personalização — estão listadas [nesta página](../content-management/gs-generative.md#generative-guardrails).

### Medidas de proteção das páginas de destino {#lp-guardrails}

As seguintes medidas de proteção se aplicam às [páginas de destino](../landing-pages/get-started-lp.md):

* Somente um componente de **Formulário** pode ser usado em uma única página principal.
* O componente de **Formulário** não pode ser usado em subpáginas.
* Não é possível adicionar um pré-cabeçalho a uma página de destino.
* Não é possível selecionar a opção **Codifique você mesmo** ao criar uma página de destino principal.

### Medidas de proteção de subdomínios {#subdomain-guardrails}

As medidas de proteção e limitações aplicáveis à delegação de subdomínios no Journey Optimizer estão detalhadas [nesta página](../configuration/delegate-subdomain.md#guardrails).

### Medidas de proteção de fragmentos {#fragments-guardrails}

As seguintes medidas de proteção se aplicam aos [fragmentos](../content-management/fragments.md):

* Para criar, editar, arquivar e publicar fragmentos, você precisa das permissões de **[!DNL Manage library items]** e **[Publicar fragmento]** inclusas no perfil do produto **[!DNL Content Library Manager]**. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)
* Os fragmentos visuais só estão disponíveis para o canal de email.
* Os fragmentos de expressão não estão disponíveis para o canal interno do aplicativo.
* Fragmentos visuais não podem exceder **100 KB**. Fragmentos de expressão não podem exceder **200 KB**.
* Para usar um fragmento em uma jornada ou campanha, ele precisa estar no status **Ativo**.
* [Atributos contextuais](../personalization/personalization-build-expressions.md) não são permitidos dentro de fragmentos.
* Fragmentos visuais não são compatíveis entre os modos de uso de temas e estilo manual. Para poder usar um fragmento em um conteúdo ao qual deseja aplicar um tema, esse fragmento precisa ser criado no modo de uso de temas. [Saiba mais sobre temas](../email/apply-email-themes.md)
* Quando o rastreamento é habilitado em uma jornada ou campanha, se você adicionar links a um fragmento e esse fragmento for usado em uma mensagem, esses links serão rastreados como todos os outros links inclusos na mensagem. [Saiba mais sobre links e rastreamento](../email/message-tracking.md)

## Gestão de decisões {#decision-management}

### Medidas de proteção de decisão e gestão de decisões {#decisioning-guardrails}

Medidas de proteção e limitações que devem ser consideradas ao trabalhar com o Serviço de decisão ou a Gestão de decisões estão detalhadas nestas seções de Decisão e Gestão de decisões:

* [Medidas de proteção e limitações do serviço de decisão](../experience-decisioning/decisioning-guardrails.md)
* [Medidas de proteção e limitações da gestão de decisões](../offers/decision-management-guardrails.md)

## Orquestração de campanha {#campaign-orchestration}

### Proteções da orquestração de campanhas {#orchestration-guardrails}

As medidas de proteção e limitações que precisam ser consideradas ao trabalhar com a orquestração de campanhas estão detalhadas nesta seção: [Medidas de proteção e limitações](../orchestrated/guardrails.md).
