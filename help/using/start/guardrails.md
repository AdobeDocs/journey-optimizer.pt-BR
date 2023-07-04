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
source-git-commit: 4c29bb1fbbf2c67d04fcd73076be456323eddc7d
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 93%

---

# Medidas de proteção e limitações {#limitations}

Os direitos, as limitações de produto e as medidas de proteção de desempenho estão listados na [página de descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

Você também precisa estar ciente das [Medidas de proteção aos dados de perfil do cliente em tempo real antes de iniciar](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=pt-BR){target="_blank"}.

Abaixo você encontrará medidas de proteção e limitações adicionais para o uso do [!DNL Adobe Journey Optimizer].

## Navegadores compatíveis {#browsers}

A interface do Adobe [!DNL Journey Optimizer] foi projetada para funcionar de maneira ideal na versão mais recente do Google Chrome. Você pode ter problemas ao usar determinados recursos em versões mais antigas ou outros navegadores.

## Medidas de proteção de mensagens {#message-guardrails}

* Não é possível adicionar anexos a um email com [!DNL Journey Optimizer].
* Você não pode usar o mesmo domínio de envio para enviar mensagens do [!DNL Adobe Journey Optimizer] e de outro produto, como o [!DNL Adobe Campaign] ou o [!DNL Adobe Marketo Engage] por exemplo.


## Medidas de proteção das páginas de destino {#lp-guardrails}

* Somente um componente de **Formulário** pode ser usado em uma única página principal.
* O componente de **Formulário** não pode ser usado em subpáginas.
* Não é possível adicionar um pré-cabeçalho a uma página de destino.
* Não é possível selecionar a opção **Codifique você mesmo** ao criar uma página de destino principal.

## Medidas de proteção de jornada {#journeys-guardrails}

### Medidas de proteção gerais da jornada {#journeys-guardrails-journeys}

* O limite de número de atividades em uma jornada é de 50. O número de atividades é exibido na seção superior esquerda da tela da jornada. Isso ajudará na legibilidade, controle de qualidade e solução de problemas.
* À medida que você publica jornadas, dimensionamos e ajustamos automaticamente para garantir a taxa de transferência e a estabilidade máximas. Ao se aproximar do marco de 100 jornadas ativas de uma só vez, você verá uma notificação aparecer na interface do usuário sobre essa conquista. Se você vir esta notificação e precisar estender suas jornadas além de 100 jornadas ao vivo de cada vez, crie um tíquete para o Atendimento ao cliente e ajudaremos você a atingir suas metas.

### Ações gerais {#general-actions-g}

* Não há limitação de envio.
* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida.
* O evento **Reação** integrado permite que você reaja a ações predefinidas. Saiba mais [nesta página](../building-journeys/reaction-events.md). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.
* Um perfil não pode estar presente várias vezes na mesma jornada ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá inserir uma jornada novamente, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada. [Leia mais](../building-journeys/end-journey.md)

### Versões de jornada {#journey-versions-g}

* Uma jornada que começa com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com um evento de **Qualificação do segmento**.
* Uma jornada que começa com uma atividade de **Qualificação de segmento** em v1 deve sempre começar com uma **Qualificação de segmento** em outras versões.
* O segmento e o namespace escolhidos na **Qualificação de segmento** (primeiro nó) não podem ser alterados em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões da jornada.
* Uma jornada que começa com um **Segmento de leitura** não pode começar com outro evento nas próximas versões.
* Não é possível criar uma nova versão de uma jornada de segmento de leitura com leitura incremental. Você precisa duplicar a jornada.

### Ações personalizadas {#custom-actions-g}

* O URL de ação personalizada não aceita parâmetros dinâmicos.
* Somente os métodos de chamada POST e PUT são compatíveis
* O nome do parâmetro de consulta ou cabeçalho não deve começar com “.” ou “$”
* Endereços IP não são permitidos
* Endereços internos da Adobe (`.adobe.*`) não são permitidos em URLs e APIs.
* As ações personalizadas incorporadas não podem ser removidas.

### Eventos {#events-g}

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada ao conteúdo de transmissão que entra na Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.
* Os eventos comerciais não podem ser usados junto com eventos unitários ou atividades de qualificação de segmento.
* As jornadas unitárias (começando com um evento ou uma qualificação de segmento) incluem uma medida de proteção que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12h01 para um perfil específico e outra chegar às 12h03 (se for o mesmo evento ou outro acionando a mesma jornada), essa jornada não será reiniciada para esse perfil.
* O Journey Optimizer requer que os eventos sejam transmitidos para o Serviço principal de coleção de dados (DCCS) para acionar uma jornada. Eventos assimilados em lote ou eventos de conjuntos de dados internos do Journey Optimizer (feedback de mensagem, rastreamento de email etc.) não podem ser usados para acionar uma jornada. Para casos de uso nos quais não é possível obter eventos transmitidos, crie um segmento com base nesses eventos e use a atividade **Ler segmento** em vez disso. Tecnicamente, a qualificação de segmentos pode ser usada, mas ela pode causar desafios posteriores com base nas ações usadas.

### Fontes de dados {#data-sources-g}

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e poder lidar com o volume de solicitações.
* Endereços internos da Adobe (`.adobe.*`) não são permitidos em URLs e APIs.

### Criação de jornadas e perfis {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API na Adobe Experience Platform. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a ingestão até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera depois do primeiro evento para conceder à Adobe Experience Platform o tempo necessário para executar a ingestão no Serviço de Perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento da experiência pode conter informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc.).

### Ler segmento {#read-segment-g}

* Os segmentos exibidos estão sempre atualizados, mas os segmentos em lote não serão calculados no momento da recuperação. Só são avaliados diariamente no momento da avaliação diária do lote.
* Para jornadas que usam uma atividade Segmento de Leitura, há um número máximo de jornadas que podem ser iniciadas exatamente ao mesmo tempo. As tentativas serão executadas pelo sistema, mas evite ter mais do que cinco jornadas (com Segmento de Leitura, programado ou iniciando &quot;o mais rápido possível&quot;), iniciando exatamente ao mesmo tempo, espalhando-as ao longo do tempo, por exemplo, com intervalos de 5 a 10 minutos.

### Editor de expressão {#expression-editor}

* Grupos de campos de evento de experiência não podem ser usados em jornadas que começam com um segmento de leitura, uma qualificação de segmento ou uma atividade de evento comercial. É necessário criar um novo segmento e usar uma condição de segmento na jornada.


