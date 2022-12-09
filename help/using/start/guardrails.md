---
solution: Journey Optimizer
product: journey optimizer
title: Medidas de proteção e limitações do Journey Otimizer
description: Saiba mais sobre as medidas de proteção do Journey Otimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Medidas de proteção e limitações {#limitations}

Os direitos, as limitações de produtos e as medidas de proteção do desempenho estão listados em [Página de descrição do produto Adobe Journey Otimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Você encontrará abaixo medidas de proteção e limitações adicionais ao usar [!DNL Adobe Journey Optimizer].

## Medidas de proteção de mensagens {#message-guardrails}

* Não é possível adicionar anexos a um email com [!DNL Journey Optimizer].
* Você não pode usar o mesmo domínio de envio para enviar mensagens de [!DNL Adobe Journey Optimizer] e de outro produto, como [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage] por exemplo.


## Medidas de proteção de gestão de decisões {#offer-guardrails}

As medidas de proteção de desempenho e os limites estáticos para a tomada de decisões estão listados na seção [Página de descrição do produto Serviço de aplicativo Adobe Offer Decisioning](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Medidas de proteção das páginas de aterrissagem {#lp-guardrails}

* Somente um **Formulário** pode ser usado em uma única página primária.
* O **Formulário** não pode ser usado em subpáginas.
* Não é possível adicionar um precabeçalho a uma página de aterrissagem.
* Não é possível selecionar a variável **Codifique seu próprio** ao criar uma página primária de aterrissagem.

## Medidas de proteção da viagem {#journeys-guardrails}

### Ações gerais {#general-actions-g}

* Não há limitação de envio.
* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida.
* O **Reação** permite que você reaja a ações predefinidas. Saiba mais em [esta página](../building-journeys/reaction-events.md). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.
* Geralmente, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá entrar novamente em uma jornada, mas não poderá fazê-lo até que ele tenha saído totalmente dessa instância anterior da jornada. [Leia mais](../building-journeys/end-journey.md)

### Versões de jornada {#journey-versions-g}

* Uma jornada que começa com uma atividade de evento na v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com uma **Qualificação do segmento** evento.
* Uma jornada que começa com uma **Qualificação do segmento** atividade em v1 deve sempre começar com um **Qualificação do segmento** em outras versões.
* O segmento e o namespace escolhidos em **Qualificação do segmento** (primeiro nó) não pode ser alterado em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões da jornada.
* Uma jornada que começa com uma **Ler segmento** O não pode começar com outro evento nas próximas versões.

### Ações personalizadas {#custom-actions-g}

* O URL de ação personalizada não suporta parâmetros dinâmicos.
* Somente métodos de chamada POST e PUT são compatíveis
* O nome do parâmetro de consulta ou cabeçalho não deve começar com &quot;.&quot; ou &quot;$&quot;
* Endereços IP não são permitidos
* Endereços internos da Adobe (.adobe.) não são permitidas.

### Eventos {#events-g}

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Otimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada à carga de transmissão que entra na Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.
* Os eventos comerciais não podem ser usados junto com eventos unitários ou atividades de qualificação de segmento.
* As jornadas unitárias (começando com um evento ou uma qualificação de segmento) incluem uma garantia que impede que as jornadas sejam acionadas erroneamente várias vezes para o mesmo evento. A reentrada do perfil é temporariamente bloqueada por padrão por 5 minutos. Por exemplo, se um evento acionar uma jornada às 12:01 para um perfil específico e outra chegar às 12:03 (se for o mesmo evento ou um evento diferente que aciona a mesma jornada), essa jornada não será iniciada novamente para esse perfil.

### Fontes de dados {#data-sources-g}

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e podem lidar com o volume de solicitações.

### Jornadas e criação de perfis {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API na Adobe Experience Platform. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a assimilação até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, talvez não funcione corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera após o primeiro evento para conceder à Adobe Experience Platform o tempo necessário para executar a assimilação no Serviço de perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento de experiência poderá conter as informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc.).

### Ler segmento {#read-segment-g}

* Os segmentos continuados estão sempre atualizados, mas os segmentos em lote não serão calculados no momento da recuperação. Só são avaliados todos os dias no momento da avaliação diária do lote.
* Para jornadas que usam uma atividade Ler segmento , há um número máximo de jornadas que podem começar exatamente ao mesmo tempo. As tentativas serão executadas pelo sistema, mas evite ter mais de cinco jornadas (com Segmento de leitura, programado ou iniciando &quot;o mais rápido possível&quot;), iniciando exatamente ao mesmo tempo, espalhando-as ao longo do tempo, por exemplo, com intervalos de 5 a 10 minutos.

### Editor de expressão {#expression-editor}

* Os grupos de campos de evento de experiência não podem ser usados em jornadas que começam com um segmento Lido, uma qualificação de Segmento ou uma atividade de evento comercial.

