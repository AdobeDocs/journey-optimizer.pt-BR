---
solution: Journey Optimizer
product: journey optimizer
title: Limitações do Jornada
description: Saiba mais sobre as limitações do Jornada
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: jornadas, limitação
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1276
ht-degree: 20%

---

# Limitações {#journey-limitations}

>[!BEGINSHADEBOX]

**Nesta página:** Revise as limitações e medidas de proteção que se aplicam às jornadas, incluindo ações, versões, ações personalizadas, eventos e fontes de dados.

>[!ENDSHADEBOX]

Estas são as limitações relacionadas ao uso de jornadas do.

## Limitações gerais de ações {#action-limitations}

* Não há limitação de envio.
* Três tentativas são executadas sistematicamente em caso de erro. Não é possível ajustar o número de tentativas de acordo com a mensagem de erro recebida.
* O evento **Reação** interno permite que você reaja a ações predefinidas (consulte esta [página](../building-journeys/reaction-events.md)). Se quiser reagir a uma mensagem enviada por meio de uma ação personalizada, será necessário configurar um evento dedicado.
* Não é possível colocar duas ações em paralelo, é necessário adicioná-las uma após a outra.


## Limitações de versões do Jornada {#journey-versions-limitations}

* Uma jornada que começa com uma atividade de evento em v1 não pode começar com algo diferente de um evento em outras versões. Não é possível iniciar uma jornada com um evento de **Qualificação de público-alvo**.
* Uma jornada que começa com uma atividade **Qualificação de público-alvo** em v1 deve sempre começar com uma **Qualificação de público-alvo** em outras versões.
* O público-alvo e o namespace escolhidos em **Qualificação de Público-Alvo** (primeiro nó) não podem ser alterados em novas versões.
* A regra de reentrada deve ser a mesma em todas as versões da jornada.
* Uma jornada que começa com um **Público-alvo de leitura** não pode começar com outro evento nas próximas versões.

## Limitações de ações personalizadas {#custom-actions-limitations}

* O URL de ação personalizada não aceita parâmetros dinâmicos. 
* Somente os métodos de chamada POST e PUT são compatíveis. 
* O nome do parâmetro de consulta ou cabeçalho não deve começar com &quot;.&quot; ou &quot;$&quot;. 
* Endereços IP não são permitidos. 
* Endereços Adobe internos (.adobe.) não são permitidos.

## Limitações de eventos {#events-limitations}

* Para eventos gerados pelo sistema, os dados de transmissão usados para iniciar uma jornada do cliente devem ser configurados no Journey Optimizer primeiro para obter uma ID de orquestração exclusiva. Essa ID de orquestração deve ser anexada à carga de streaming recebida em [!DNL Adobe Experience Platform]. Essa limitação não se aplica a eventos com base em regras.

## Limitações de eventos de reação {#reaction-limitations}

* As atividades de **[!UICONTROL Reação]** devem ser colocadas imediatamente após uma [atividade de ação de canal](../building-journeys/journey-action.md) na tela de jornada. Não há suporte para a colocação de uma atividade **[!UICONTROL Wait]** ou qualquer outra atividade entre a ação de canal e a atividade **[!UICONTROL Reaction]** e pode fazer com que a Reação não funcione conforme esperado. Saiba mais [nesta seção](../building-journeys/reaction-events.md).

## Limitações das fontes de dados {#data-sources-limitations}

* As fontes de dados externas podem ser aproveitadas em uma jornada do cliente para pesquisar dados externos em tempo real. Essas fontes devem ser utilizáveis por meio da API REST, devem ser compatíveis com JSON e poder lidar com o volume de solicitações.

## Jornadas que começam ao mesmo tempo que a criação de um perfil {#journeys-limitation-profile-creation}

Há um atraso associado à criação/atualização de perfil com base em API em [!DNL Adobe Experience Platform]. O Service Level Target (SLT) em termos de latência é &lt; 1 min desde a ingestão até o Perfil unificado, por 95% das solicitações, em um volume de 20 mil solicitações por segundo (RPS).

Se uma Jornada for acionada simultaneamente à criação de um perfil e verificar/recuperar imediatamente as informações do Serviço de perfil, ela pode não funcionar corretamente.

Você pode escolher uma dessas duas soluções:

* Adicione uma atividade de espera após o primeiro evento, para dar a [!DNL Adobe Experience Platform] o tempo necessário para executar a assimilação no Serviço de Perfil.

* Configure uma jornada que não use o perfil imediatamente. Por exemplo, se a jornada for projetada para confirmar a criação de uma conta, o evento da experiência pode conter informações necessárias para enviar a primeira mensagem de confirmação (nome, sobrenome, endereço de email etc).

## Ler limitações de público {#read-audiences-limitations}

* Os públicos-alvo transmitidos estão sempre atualizados, mas os públicos-alvo em lote não serão calculados no momento da recuperação. Eles só são avaliados diariamente no momento da avaliação diária do lote.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página lista as limitações técnicas graves que se aplicam às ações de jornada, versões de jornada, ações personalizadas, eventos, eventos de reação, fontes de dados e leitura de público-alvo no Adobe Journey Optimizer.

**Intenções:**

* Entender os limites de envio e repetição para ações de jornada
* Saiba quais transições de versão do jornada são permitidas ou bloqueadas
* Identificar restrições na URL de ação personalizada, no método e na configuração do cabeçalho
* Entender os requisitos da fonte de dados para integração com o sistema externo
* Evite problemas de tempo ao iniciar uma jornada no mesmo momento que a criação do perfil

**Glossário:**

* **Evento de reação**: uma atividade de jornada que escuta a interação de um perfil com uma ação de canal (por exemplo, email aberto ou clique); deve ser colocada imediatamente após a atividade de ação de canal. *(específico do produto)*
* **Evento baseado em regras**: um tipo de evento em que o gatilho é definido por uma condição lógica em vez de uma ID de orquestração gerada pelo sistema. *(específico do produto)*
* **SLT (Service Level Target)**: o referencial de latência para criação/atualização de perfil com base em API no Adobe Experience Platform — menos de 1 minuto desde a assimilação até o Perfil Unificado no 95º percentil para 20K RPS.

**Medidas de Proteção:**

* Nenhuma limitação de envio é aplicada; três tentativas são executadas automaticamente em caso de erro e não podem ser ajustadas
* Duas ações não podem ser executadas em paralelo; elas devem ser adicionadas sequencialmente
* Uma jornada que começa com uma atividade de evento em v1 não pode começar com uma atividade que não seja de evento em versões posteriores
* Uma jornada que começa com uma Qualificação de público-alvo em v1 deve sempre começar com a Qualificação de público-alvo em todas as versões subsequentes; o público-alvo e o namespace não podem ser alterados
* Uma jornada que começa com Read Audience não pode começar com um evento diferente nas próximas versões
* O URL de ação personalizada não suporta parâmetros dinâmicos; somente os métodos de chamada POST e PUT são suportados
* O parâmetro de consulta de ação personalizada e os nomes de cabeçalho não devem começar com &quot;.&quot; ou &quot;$&quot;; endereços IP e endereços Adobe internos (.adobe.) não são permitidos
* As atividades de reação devem ser colocadas imediatamente após uma atividade de ação de canal; não há suporte para a inserção de uma atividade Wait ou outra entre elas
* As fontes de dados externas devem ser acessíveis por meio da API REST, ter suporte para JSON e manipular o volume de solicitações
* Os públicos-alvo em lote são avaliados apenas uma vez por dia no momento da avaliação diária do lote — eles não são recalculados no momento da recuperação
* Quando uma jornada é acionada simultaneamente com uma criação de perfil, os dados de perfil podem ainda não estar disponíveis devido à latência de assimilação da plataforma

**Terminologia:**

* Nome canônico: Limitações de Jornada — Acrônimo: none — variantes: medidas de proteção de jornada, restrições de jornada
* Não confunda: &quot;Limitação do evento de reação&quot; ≠ &quot;limitação de ação geral&quot; — O evento de reação deve ser colocado diretamente após uma ação de canal; a limitação de ação geral abrange tentativas, paralelismo e limitação

**Perguntas frequentes:**

* **P: Quantas vezes o Journey Optimizer repete uma ação com falha?** — Três tentativas são executadas automaticamente; o número de tentativas não pode ser configurado.
* **P: Posso colocar uma atividade de espera entre uma ação de canal e um evento de Reação?** — Não; o evento Reaction deve ser colocado imediatamente após a atividade channel action. A adição de qualquer atividade intermediária não é suportada e pode fazer com que o evento Reação não funcione como esperado.
* **P: Posso alterar o primeiro tipo de evento ao criar uma nova versão do jornada?** — Não; o mecanismo de entrada definido em v1 deve ser preservado em todas as versões subsequentes. Uma jornada que começa com um evento deve continuar a começar com um evento, e uma jornada que começa com Qualificação de público-alvo deve sempre começar com Qualificação de público-alvo.
* **P: Por que minha jornada pode não funcionar quando acionada ao mesmo tempo que um perfil é criado?** — a criação de perfis por meio da API tem uma latência antes que os dados estejam disponíveis no Perfil unificado (SLT &lt; 1 minuto no percentil 95). Adicionar uma atividade Wait após o primeiro evento dá à Platform tempo para concluir a assimilação.
* **P: Os públicos de streaming são sempre atuais no jornada?** — Sim; os públicos-alvo de transmissão estão sempre atualizados. No entanto, os públicos-alvo em lote são avaliados apenas uma vez por dia no momento da avaliação diária do lote, não no momento da recuperação.

+++
