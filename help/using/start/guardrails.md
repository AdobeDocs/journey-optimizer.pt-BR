---
title: Medidas de proteção e limitações da Journey Optimizer
description: Saiba mais sobre as medidas de proteção da Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 4%

---

# Medidas de proteção e limitações {#limitations}

Os direitos, as limitações de produtos e as medidas de proteção do desempenho estão listados em [Página de descrição do produto Adobe Journey Optimizer](https://helpx.adobe.com/br/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target=&quot;_blank&quot;}.

Abaixo você encontrará medidas de proteção e limitações adicionais para uso do [!DNL Adobe Journey Optimizer].

## Medidas de proteção de mensagens {#message-guardrails}

* Não é possível adicionar anexos a um email com [!DNL Journey Optimizer].
* Você não pode usar o mesmo domínio de envio para enviar mensagens de [!DNL Adobe Journey Optimizer] e de outro produto, como [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage] por exemplo.


## Medidas de proteção de gestão de decisões {#offer-guardrails}

As medidas de proteção de desempenho e os limites estáticos para a gestão de decisões estão listados no [Página de descrição do produto Serviço de Aplicativo do Adobe Offer Decisioning](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Medidas de proteção das páginas de aterrissagem {#lp-guardrails}

* Somente um **Formulário** pode ser usado em uma única página primária.
* O **Formulário** não pode ser usado em subpáginas.
* Não é possível adicionar um precabeçalho a uma página de aterrissagem.
* Não é possível selecionar a variável **Codifique seu próprio** ao criar uma página primária de aterrissagem.

## Medidas de proteção de jornada {#journeys-guardrails}

### Ações gerais {#general-actions-g}

* Não há limitação de envio.
* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida.
* O **Reação** permite que você reaja a ações predefinidas. Saiba mais [nesta página](../building-journeys/reaction-events.md). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.
* Há uma limitação técnica no jornada hoje que impede que um perfil seja apresentado várias vezes na mesma jornada, ao mesmo tempo. Um perfil ainda pode inserir novamente uma jornada (com base em uma configuração), mas não poderá fazer isso até que ele tenha saído totalmente dessa instância anterior da jornada.
* Na maioria dos casos, um perfil não pode estar presente várias vezes na mesma jornada, ao mesmo tempo. Se a reentrada estiver ativada, um perfil poderá inserir uma jornada novamente, mas não poderá fazer isso até que ele tenha saído totalmente da instância anterior da jornada. [Leia mais](../building-journeys/journey-end.md)

### Versões de jornada {#journey-versions-g}

* Uma jornada que começa com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com uma **Qualificação do segmento** evento.
* Uma jornada que começa com uma **Qualificação do segmento** atividade em v1 deve sempre começar com um **Qualificação do segmento** em outras versões.
* O segmento e o namespace escolhidos em **Qualificação do segmento** (primeiro nó) não pode ser alterado em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões do jornada.
* Uma jornada que começa com uma **Ler segmento** O não pode começar com outro evento nas próximas versões.

### Ações personalizadas {#custom-actions-g}

* O URL de ação personalizada não suporta parâmetros dinâmicos.
* Somente os métodos de chamada de POST e PUT são compatíveis
* O nome do parâmetro de consulta ou cabeçalho não deve começar com &quot;.&quot; ou &quot;$&quot;
* Endereços IP não são permitidos
* Endereços Adobe internos (.adobe.) não são permitidas.

### Eventos {#events-g}

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada à carga de transmissão que entra no Adobe Experience Platform. Essa limitação não se aplica a eventos com base em regras.
* Os eventos comerciais não podem ser usados junto com eventos unitários ou atividades de qualificação de segmento.

### Fontes de dados {#data-sources-g}

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e podem lidar com o volume de solicitações.

### Jornadas e criação de perfis {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API no Adobe Experience Platform. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a assimilação até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera após o primeiro evento para conceder ao Adobe Experience Platform o tempo necessário para executar a assimilação no Serviço de perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento de experiência poderá conter as informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc.).

### Ler segmento {#read-segment-g}

* Os segmentos continuados estão sempre atualizados, mas os segmentos em lote não serão calculados no momento da recuperação. Só são avaliados todos os dias no momento da avaliação diária do lote.
