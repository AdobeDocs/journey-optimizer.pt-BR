---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações do Journey Optimizer
description: Saiba mais sobre as medidas de proteção do Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 5b16e3a89a9a39723a2443345c4e8180a490112e
workflow-type: tm+mt
source-wordcount: '2476'
ht-degree: 94%

---

# Medidas de proteção e limitações {#limitations}

Abaixo você encontrará medidas de proteção e limitações adicionais para o uso do [!DNL Adobe Journey Optimizer].

Os direitos, as limitações de produto e as medidas de proteção de desempenho estão listados na [página de descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

Você também precisa estar ciente das [Medidas de proteção aos dados de perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=pt-BR){target="_blank"} antes de iniciar.


>[!NOTE]
>
>Em raras circunstâncias, interrupções temporárias em uma região específica podem resultar na exclusão de perfis válidos das jornadas ou em emails marcados incorretamente como rejeições. Depois que os serviços forem restaurados, verifique novamente os logs do jornada, verifique os campos do perfil de consentimento e republique a jornada, se necessário. No caso de uma interrupção de ISP, saiba como remover perfis da lista de supressão em [esta seção](../configuration/manage-suppression-list.md#remove-from-suppression-list).
>

## Navegadores compatíveis {#browsers}

A interface do Adobe [!DNL Journey Optimizer] foi projetada para funcionar de maneira ideal na versão mais recente do Google Chrome. Você pode ter problemas ao usar determinados recursos em versões mais antigas ou outros navegadores.

## Medidas de proteção de mensagens {#message-guardrails}

* Não é possível adicionar anexos a um email com [!DNL Journey Optimizer].
* Você não pode usar o mesmo domínio de envio para enviar mensagens do [!DNL Adobe Journey Optimizer] e de outro produto, como o [!DNL Adobe Campaign] ou o [!DNL Adobe Marketo Engage] por exemplo.

## Medidas de proteção de conjuntos de dados {#datasets-guardrails}

A partir de fevereiro de 2025, uma garantia de TTL (time-to-live) será implantada nos conjuntos de dados gerados pelo sistema da Journey Optimizer em **novas sandboxes e novas organizações** da seguinte maneira:

* 90 dias para dados na loja de perfis
* 13 meses para dados no data lake

Explore a [seção de Perguntas Frequentes](../data/datasets-ttl.md#ttl) para obter mais detalhes sobre essas medidas de proteção.

## Medidas de proteção das páginas de destino {#lp-guardrails}

* Somente um componente de **Formulário** pode ser usado em uma única página principal.
* O componente de **Formulário** não pode ser usado em subpáginas.
* Não é possível adicionar um pré-cabeçalho a uma página de destino.
* Não é possível selecionar a opção **Codifique você mesmo** ao criar uma página de destino principal.

## Medidas de proteção de SMS {#sms-guardrails}

* Os arquivos de mídia para MMS podem ser incluídos por meio de um URL compatível. Verifique se o arquivo de mídia foi enviado separadamente.
* A sincronização de feedback da mensagem não está disponível no momento para MMS.
* O gerenciamento de consentimento opera no nível do canal SMS para MMS.

### Medidas de proteção do canal da Web {#web-guardrails}

As campanhas da Web do [!DNL Journey Optimizer] direcionam novos perfis que não foram engajados anteriormente em outros canais. Isso aumentará a contagem total de perfis engajáveis, o que pode ter implicações de custo se o número contratual de perfis engajáveis que você adquiriu for excedido. As métricas de licença para cada pacote estão listadas na página [Descrição do produto Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

## Medidas de proteção de subdomínios {#subdomain-guardrails}

Por padrão, o [!DNL Journey Optimizer] permite delegar até 10 subdomínios no total (englobando canais de email e da web).

No entanto, dependendo do contrato de licença, talvez você possa delegar até 100 subdomínios. Fale com seu contato na Adobe para saber mais sobre o número de subdomínios aos quais você tem direito.

## Medidas de proteção de fragmentos {#fragments-guardrails}

* Os fragmentos visuais só estão disponíveis para o canal de email.
* Os fragmentos de expressão não estão disponíveis para o canal interno do aplicativo.

## Medidas de proteção de jornada {#journeys-guardrails}

### Medidas de proteção gerais da jornada {#journeys-guardrails-journeys}

* O limite de número de atividades em uma jornada é de 50. O número de atividades é exibido na seção superior esquerda da tela da jornada. Isso ajudará na legibilidade, controle de qualidade e solução de problemas.
* À medida que você publica jornadas, dimensionaremos e ajustaremos automaticamente para garantir uma máxima taxa de transferência e estabilidade. Ao se aproximar do marco de 100 jornadas ativas de uma só vez, você verá uma notificação aparecer na interface sobre essa conquista. Se vir esta notificação e precisar aumentar o número de jornadas para acima de 100 jornadas ativas por vez, crie um tíquete para o Atendimento ao cliente e ajudaremos a atingir suas metas.
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* Ao usar uma qualificação de público-alvo em uma jornada, essa atividade de qualificação de público-alvo pode levar até 10 minutos para ficar ativa e ouvir os perfis que entram ou saem do público-alvo.
* Uma instância de jornada para um perfil tem tamanho máximo de 1 MB. Todos os dados coletados como parte da execução da jornada são armazenados nessa instância da jornada. Portanto, dados de um evento de entrada, informações de perfil recuperadas da Adobe Experience Platform, respostas de ações personalizadas etc. são armazenados nessa instância da jornada e afetam o tamanho da jornada. É aconselhável, quando uma jornada inicia com um evento, limitar o tamanho máximo desse conteúdo do evento (por exemplo: até 800 KB) para evitar atingir esse limite após algumas atividades, na execução da jornada. Quando esse limite é atingido, o perfil fica com status de erro e será excluído da jornada.
* Além do tempo limite usado em atividades de jornada, também há um tempo limite de jornada global que não aparece na interface e não pode ser alterado. Esse tempo limite global interrompe o progresso das pessoas na jornada 91 dias após a sua entrada. [Leia mais](../building-journeys/journey-properties.md#global_timeout)


### Ações gerais {#general-actions-g}

* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida. Novas tentativas são executadas para todos os erros HTTP, exceto para HTTP 401, 403 e 404.
* O evento **Reação** integrado permite que você reaja a ações predefinidas. Saiba mais [nesta página](../building-journeys/reaction-events.md). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.
* Um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá entrar novamente em uma jornada, mas não até que tenha saído totalmente da instância anterior da jornada. [Leia mais](../building-journeys/end-journey.md)

### Versões de jornada {#journey-versions-g}

* Uma jornada que começa com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com um evento de **Qualificação de público-alvo**.
* Uma jornada que começa com uma atividade de **Qualificação de público-alvo** em v1 deve sempre começar com uma **Qualificação de público-alvo** em outras versões.
* O público-alvo e o namespace escolhidos na **Qualificação de público-alvo** (primeiro nó) não podem ser alterados em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões da jornada.
* Uma jornada que começa com um **Público-alvo de leitura** não pode começar com outro evento nas próximas versões.
* Não é possível criar uma nova versão de uma jornada de público-alvo de leitura com leitura incremental. Você precisa duplicar a jornada.

### Ações personalizadas {#custom-actions-g}

* Um limite máximo de 300.000 chamadas em um minuto é definido para todas as ações personalizadas, por host e por sandbox. Consulte [esta página](../action/about-custom-action-configuration.md). Esse limite foi definido com base no uso pelos clientes, para proteger pontos de acesso externos direcionados por ações personalizadas. É necessário considerar isso em jornadas baseadas em público-alvo, definindo uma taxa de leitura apropriada (5.000 perfis por segundo ao utilizar ações personalizadas). Se necessário, é possível substituir essa configuração aumentando o limite máximo por meio das APIs de limite e limitação. Consulte [esta página](../configuration/external-systems.md).
* O URL de ação personalizada não aceita parâmetros dinâmicos.
* Os métodos de chamada POST, PUT e GET são compatíveis
* O nome do parâmetro de consulta ou cabeçalho não deve começar com “.” ou “$”
* Endereços IP não são permitidos
* Endereços internos da Adobe (`.adobe.*`) não são permitidos em URLs e APIs.
* As ações personalizadas incorporadas não podem ser removidas.
* As ações personalizadas são compatíveis com o formato JSON somente ao usar conteúdos de solicitação ou resposta. Consulte [esta página](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Ao escolher um ponto de acesso para destino usando uma ação personalizada, verifique se:

   * Esse ponto de acesso pode suportar a taxa de transferência da jornada, usando configurações da [API de limitação](../configuration/throttling.md) ou da [API de limite](../configuration/capping.md) para limitá-la. Tenha cuidado, pois uma configuração de limitação não pode ficar abaixo de 200 TPS. Qualquer ponto de acesso como direcionado precisará oferecer suporte a pelo menos 200 TPS.
   * Esse ponto de acesso precisa ter um tempo de resposta o mais baixo possível. Dependendo da taxa de transferência esperada, ter um tempo de resposta alto pode afetar a taxa de transferência real.

### Eventos {#events-g}

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada ao conteúdo de transmissão que entra na Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.
* Os eventos comerciais não podem ser usados junto com eventos unitários ou atividades de qualificação de público-alvo.
* As jornadas unitárias (começando com um evento ou uma qualificação de público-alvo) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. Por padrão, a reentrada do perfil é temporariamente bloqueada por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12h01 para um perfil específico e outra chegar às 12h03 (quer seja o mesmo evento ou outro que acione a mesma jornada), essa jornada não será reiniciada para esse perfil.
* O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço principal de coleção de dados (DCCS) para acionar uma jornada. Eventos assimilados em lote ou eventos de conjuntos de dados internos da Journey Optimizer (Feedback de mensagem, Rastreamento de email etc.) não podem ser usados para acionar uma jornada. Para casos de uso nos quais não é possível obter os eventos transmitidos, é necessário criar um público-alvo com base nesses eventos e usar a atividade **Público-alvo de leitura**. Tecnicamente, a qualificação de público-alvo pode ser usada, mas não é recomendada, pois pode causar desafios no downstream com base nas ações usadas.


### Fontes de dados {#data-sources-g}

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e poder lidar com o volume de solicitações.
* Endereços internos da Adobe (`.adobe.*`) não são permitidos em URLs e APIs.

>[!NOTE]
>
>Como as respostas agora são compatíveis, você deve usar ações personalizadas em vez de fontes de dados para casos de uso de fontes de dados externas.

### Criação de jornadas e perfis {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API na Adobe Experience Platform. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a ingestão até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera depois do primeiro evento para conceder à Adobe Experience Platform o tempo necessário para executar a ingestão no Serviço de Perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento da experiência pode conter informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc.).

### Atualizar perfil {#update-profile-g}

Medidas de proteção específicas se aplicam à atividade **[!UICONTROL Atualizar perfil]**. Elas são listadas [nesta página](../building-journeys/update-profiles.md).


### Público-alvo de leitura {#read-segment-g}

As seguintes medidas de proteção se aplicam à atividade **[!UICONTROL Público-alvo de leitura]**:

* Os públicos-alvo transmitidos estão sempre atualizados, mas os públicos-alvo em lote não serão calculados no momento da recuperação. Eles só são avaliados diariamente no momento da avaliação diária do lote.
* Para jornadas que usam uma atividade de **público-alvo de leitura**, há um número máximo de jornadas que podem ser iniciadas ao mesmo tempo. O sistema ainda realizará novas tentativas, mas você deve evitar ter mais de cinco jornadas (com **Público-alvo de leitura**, agendadas ou iniciando “o mais rápido possível”) que se iniciem ao mesmo tempo, espalhando-as ao longo do tempo, por exemplo, em intervalos de 5 a 10 minutos.
* A atividade de **público-alvo de leitura** não pode ser usada com atividades do Adobe Campaign.
* A atividade de **público-alvo de leitura** só pode ser usada como a primeira atividade de uma jornada ou após uma atividade de evento de negócios.
* Uma jornada só pode ter uma atividade de **público-alvo de leitura**.
* Consulte também as recomendações de como usar a atividade de **público-alvo de leitura** descritas [nesta página](../building-journeys/read-audience.md).
* As novas tentativas são aplicadas por padrão em jornadas acionadas por público-alvo (começando com um **público-alvo de leitura** ou um **evento de negócios**) ao recuperar o trabalho de exportação. Se ocorrer um erro durante a criação do trabalho de exportação, as novas tentativas serão realizadas a cada 10 minutos por, no máximo, 1 hora. Depois disso, vamos considerá-la como uma falha. Esses tipos de jornada podem, portanto, ser executados até 1 hora após o horário agendado.


### Qualificação de público-alvo {#audience-qualif-g}

A medida de proteção a seguir se aplica à atividade **[!UICONTROL Qualificação de público-alvo]**:

* A atividade Qualificação de público-alvo não pode ser usada com atividades do Adobe Campaign.


### Editor de expressão {#expression-editor}

* Os grupos de campos de evento de experiência não podem ser usados em jornadas que comecem com atividades de Público-alvo de leitura, de Qualificação de público-alvo ou de evento comercial. É necessário criar um novo público-alvo e usar uma condição de público-alvo na jornada.


### Atividade No aplicativo {#in-app-activity-limitations}

* No momento, esse recurso não está disponível para clientes do Healthcare.

* A personalização pode conter apenas atributos de perfil.

* A atividade No aplicativo não pode ser usada com atividades do Adobe Campaign.

* A exibição no aplicativo está vinculada à duração da jornada, o que significa que, quando a jornada terminar para um perfil, todas as mensagens no aplicativo dentro dessa jornada deixarão de ser exibidas para esse perfil.  Consequentemente, não é possível interromper uma mensagem no aplicativo diretamente de uma atividade da jornada. Em vez disso, será necessário encerrar toda a jornada para impedir que as mensagens No aplicativo sejam exibidas no perfil.

* No modo de teste, a exibição no aplicativo depende da duração da jornada. Para evitar que a jornada termine muito cedo durante o teste, ajuste o valor **[!UICONTROL Tempo de espera]** em suas atividades de **[!UICONTROL Espera]**.

* As atividades de **[!UICONTROL Reação]** não podem ser usadas para reagir a uma abertura ou clique no aplicativo.

* Um atraso na ativação pode ocorrer entre o momento em que um perfil de usuário ou usuária alcança uma atividade no aplicativo na tela e o momento em que começa a visualizar essa mensagem no aplicativo.

* O tamanho do conteúdo da mensagem no aplicativo é limitado a 2 Mb. A inclusão de imagens grandes pode prejudicar o processo de publicação.



### Atividade Salto {#jump-g}

Medidas de proteção específicas se aplicam à atividade **[!UICONTROL Salto]**. Elas são listadas [nesta página](../building-journeys/jump.md#jump-limitations).

### Atividades do Campaign {#ac-g}

As seguintes medidas de proteção se aplicam às atividades do **[!UICONTROL Campaign v7/v8]** e **[!UICONTROL Campaign Standard]**:

* As atividades do Adobe Campaign não podem ser usadas com uma atividade Público-alvo de leitura ou Qualificação de público-alvo.
* Essas atividades não podem ser usadas com atividades No aplicativo.

## Medidas de proteção de públicos-alvo {#audience}

Você pode publicar até 10 composições de público-alvo em uma determinada sandbox. Se tiver atingido esse limite, será necessário excluir uma composição para liberar espaço e publicar uma nova.

## Medidas de proteção da gestão de decisões {#decision-management}

### Medidas de proteção de desempenho {#performance-guardrails}

A taxa de transferência de entrega corresponde ao número de respostas de decisão que podem ser entregues pelo serviço do aplicativo de gestão de decisões em um período especificado. O número de decisões por segundo é indicado na tabela abaixo.

| API | Decisões por segundo |
|---------|----------|
| Solicitações da API de decisão | 500 por segundo |
| Solicitações de API de decisão do Edge com a segmentação do Edge | 1.500 por segundo |
| Solicitações de API de decisão do Edge sem a segmentação do Edge | 5.000 por segundo |

### Limitações {#offers-limitations}

As limitações da gestão de decisões estão listadas abaixo.

* **Ofertas personalizadas aprovadas + ofertas substitutas** - Até 10.000 ofertas, considerando a combinação de ofertas personalizadas aprovadas e ofertas substitutas aprovadas.
* **Decisões** - Até 10.000 decisões.
* **Decisões em tempo real** - O serviço do aplicativo do Offer Decisioning oferece suporte a até 1.000 decisões em tempo real.
* **Ofertas retornadas por resposta** - O Offer Decisioning oferece suporte a um retorno de até 100 ofertas por solicitação em todos os escopos de decisão.
* **Coleções** - Até 10.000 coleções.
* **Coleções por decisão** - Até 30 coleções por decisão.
* **Regras de decisão + funções de classificação** - Até 10.000, considerando a combinação de regras de decisão e funções de classificação.
* **Posicionamentos** - Até 1.000 posicionamentos.
* **Posicionamentos por decisão** - Até 30 posicionamentos por decisão.
* **Método de classificação por decisão** - O serviço do aplicativo do Offer Decisioning oferece suporte a até 30 funções de classificação por decisão.
* **Modelo de classificação de IA** - O serviço do aplicativo do Offer Decisioning oferece suporte a até 5 modelos de classificação de IA.
* **Qualificador de coleção por oferta ou coleção** - O serviço do aplicativo do Offer Decisioning oferece suporte a até 20 qualificadores de coleção em uma única coleção ou oferta personalizada.
* **Total de qualificadores de coleção** - O serviço do aplicativo do Offer Decisioning oferece suporte a até 1.000 qualificadores de coleção.