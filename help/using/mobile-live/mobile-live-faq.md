---
solution: Journey Optimizer
product: journey optimizer
title: Perguntas frequentes
description: Perguntas frequentes sobre atividades ao vivo
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e7e994ca-aa0c-4e86-8710-c87430b74188
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Perguntas frequentes {#mobile-live-faq}

## Perguntas gerais

+++Qual é a diferença entre uma atividade Live e uma notificação por push?

A atividade Live fornece atualizações persistentes e em tempo real na Tela de bloqueio e na Dynamic Island, sem exigir que os usuários desbloqueiem seus dispositivos. As notificações por push são alertas temporários que desaparecem depois de descartadas. A atividade online permanece visível e pode ser atualizada várias vezes até ser explicitamente encerrada.

+++

+++Quantas instâncias de atividade Live podem estar ativas de uma vez?

Um aplicativo iOS pode executar várias instâncias de atividades Live simultaneamente, incluindo várias que usam o mesmo tipo `ActivityAttributes`.

Não há limite rígido imposto pelos desenvolvedores em quantas instâncias de atividade do Live de um determinado tipo de atributo podem existir. Você pode iniciar quantos forem necessários para a lógica do aplicativo, por exemplo, um por delivery ou ride em andamento. No entanto, o iOS impõe um limite no nível do sistema em quantas instâncias de atividades Live podem estar ativas ou visíveis ao mesmo tempo.

Na prática:

* O iOS geralmente oferece suporte a até cinco instâncias simultâneas de atividades online por aplicativo.

* Se esse número for excedido, o sistema poderá interromper a exibição de algumas instâncias de atividade ou encerrar as mais antigas para conservar recursos.

* Cada instância da atividade Live tem um `Activity.id` exclusivo, que permite atualizá-lo ou encerrá-lo individualmente.

+++

+++Os usuários precisam ter o aplicativo aberto para receber atualizações de atividades em tempo real?

Não. A atividade online pode ser iniciada, atualizada e encerrada remotamente mesmo quando o aplicativo está completamente fechado, um dos principais benefícios do recurso.

+++

+++Quais versões do iOS oferecem suporte à atividade online?

* iOS 16.1+: suporte básico a atividades online
* iOS 17.2+: funcionalidade push-to-start (iniciar remotamente sem abrir o aplicativo)
* iOS 18+: Suporte ao canal de transmissão para atividade ao vivo baseada em público
+++

+++Por quanto tempo uma atividade Live pode permanecer ativa?

O Apple limita a atividade Live a **8 horas de atualizações ativas**. Depois disso, o sistema encerra automaticamente a atividade, embora possa permanecer visível em um estado estático por até **12 horas adicionais** antes da remoção. Você também pode encerrar uma atividade do Live mais cedo definindo um `dismissalDate` ou chamando explicitamente o `activity.end()` no seu aplicativo.

+++

### Perguntas do desenvolvedor

+++Preciso criar uma extensão de widget separada para a atividade do Live?

Sim. A atividade online é exibida por meio do WidgetKit, portanto, é necessário criar uma extensão de widget no projeto Xcode e implementar o `ActivityConfiguration`.
[Saiba mais sobre a configuração do widget](mobile-live-configuration-sdk.md)

+++

+++Posso usar a mesma classe `LiveActivityAttributes` para atividades Live locais e remotas?

Sim. A mesma classe de atributos funciona para atividades Live iniciadas localmente e remotamente (push-to-start). Você precisa se certificar de registrá-lo com `Messaging.registerLiveActivity()`.

+++

+++O que acontece se eu enviar uma atualização para uma atividade Live que não existe?

Se você enviar um evento de atualização ou término para um `liveActivityID` ou `channelID` inexistente, a solicitação falhará silenciosamente no dispositivo. Sempre verifique se você está rastreando quais instâncias de atividade do Live estão ativas para cada usuário.

+++

+++Posso testar a atividade do Live no iOS Simulator?

Sim, você pode testar a atividade online iniciada localmente e remotamente no iOS Simulator.

* **Local**: inclui criar, atualizar e encerrar atividade do Live diretamente do seu aplicativo usando **APIs ActivityKit**.

* **Remoto**: para testar a funcionalidade de atividade do Live remotamente, integre nosso SDK de Mensagens ao seu aplicativo e use as APIs de execução fornecidas para enviar início, atualização e encerramento remotos ao seu dispositivo de teste ou ao iOS Simulator. Semelhante a como as notificações por push podem ser testadas atualmente com a integração dos SDKs da Adobe.

+++

+++Como faço para lidar com atualizações quando o aplicativo está em segundo plano?

O SDK trata isso automaticamente. Depois de registrada, a atividade online recebe atualizações mesmo quando o aplicativo é encerrado. Não são necessários modos de segundo plano adicionais.
+++

+++Qual é a diferença entre `liveActivityID` e `channelID`?

* `liveActivityID`: usado para atividade Live individual (unitária) direcionada a usuários específicos. Cada ID representa uma instância exclusiva da atividade Live.
* `channelID`: usado para atividade de difusão ao vivo enviada aos públicos. Todos os usuários no público-alvo recebem as mesmas atualizações no mesmo canal.
+++

+++Posso personalizar a aparência de Dynamic Island separadamente da Tela de bloqueio?

Sim. O `ActivityConfiguration` tem fechamentos separados para conteúdo de Tela de Bloqueio e conteúdo de Ilha Dinâmica (estados expandido, compacto e mínimo), cada design de maneira independente.
+++

+++Preciso armazenar tokens de push manualmente?

Não. Quando você registra um tipo de Atividade ao vivo com o `Messaging.registerLiveActivity()`, a SDK coleta e gerencia automaticamente tokens de push para você.
+++

+++Há limites para inicializações remotas de atividades Ativas?

Sim. As inicializações remotas via `ActivityKit` estão sujeitas a limites impostos pelo sistema. Se você tentar várias solicitações de início em rápida sucessão, o iOS poderá rejeitar outros inícios devido a cotas de atividade ativas ou restrições de orçamento. Após cerca de 5 tentativas de início consecutivas, as solicitações subsequentes começam a falhar até que um breve período de resfriamento passe.

+++

+++Qual é o orçamento para atualizações de alta prioridade?

A Apple não especifica um limite numérico exato para atualizações de atividade ao vivo de alta prioridade `(priority: 10)`. O sistema mantém um orçamento interno dinâmico que limita a frequência com que essas atualizações podem ser enviadas. Se muitas atualizações de alta prioridade forem emitidas em um curto período, a iOS poderá limitar ou atrasar as subsequentes.

Para minimizar a limitação:

* **Níveis de prioridade de equilíbrio**: combine as atualizações padrão `(priority: 5)` e alta `(priority: 10)` dependendo da importância.
* **Use a alta prioridade com moderação**: reserve a alta prioridade para atualizações críticas ao tempo, como progresso da entrega, status de pedido ou pontuações esportivas ao vivo.
* **Suporte a atualizações frequentes**: inclua `NSSupportsLiveActivitiesFrequentUpdates` no `Info.plist` do seu aplicativo e defina-o como **SIM** se precisar de atualizações frequentes.

+++

### Perguntas do profissional de marketing

+++Posso personalizar o conteúdo de atividade ao vivo para cada usuário em uma campanha de transmissão?

As campanhas de transmissão enviam o mesmo conteúdo para todos os usuários no público-alvo. Para conteúdo personalizado, use campanhas unitárias (transacionais) direcionadas a usuários individuais.
+++

+++Como faço para saber se minha atividade online foi entregue com êxito?

[Monitore suas análises de campanha](../reports/campaign-global-report-cja-activity.md) no Adobe Journey Optimizer. Você pode rastrear taxas de entrega, falhas e métricas de envolvimento. Considere também implementar eventos de análise personalizados em seu aplicativo.
+++

+++Posso programar uma atividade ao vivo com antecedência?

A chamada de API aciona a atividade Live imediatamente. No entanto, você pode agendar suas chamadas de API por meio dos sistemas de back-end ou usar os recursos de orquestração da Journey Optimizer para cronometrá-las adequadamente.
+++

+++O que acontece se eu enviar um evento de &quot;início&quot; para uma atividade Live que já existe?

Ao iniciar remotamente a atividade ativa por meio das APIs de execução do Adobe:

* Você pode incluir um cabeçalho `x-request-id` em sua solicitação. Idealmente, deve haver uma relação um para um entre cada `liveActivityID` e seu `x-request-id` correspondente. Isso garante que, se várias solicitações forem feitas com a mesma combinação de `x-request-id` e `liveActivityID`, somente uma instância de atividade Live será iniciada no dispositivo, e solicitações duplicadas serão ignoradas.

* Se o cabeçalho `x-request-id` for omitido, cada solicitação será tratada independentemente, o que pode resultar na criação de várias instâncias de atividade Live com o mesmo `liveActivityID`. Nesses casos, atualizações futuras podem falhar ou se aplicar a apenas uma das instâncias ativas.

* O valor `x-request-id` não deve ser reutilizado entre `liveActivityIDs` diferentes em solicitações de API separadas.

+++

+++Posso testar A/B diferentes experiências de atividade ao vivo?

Sim. Crie várias campanhas com diferentes estruturas de conteúdo e use os recursos de experimentação do Adobe Journey Optimizer para testar qual tem melhor desempenho. Verifique se o aplicativo é compatível com todas as variações de estado do conteúdo.

+++

+++Com que frequência devo atualizar uma atividade Live?

Atualize somente quando houver alterações significativas nas informações, pois atualizações muito frequentes podem consumir bateria e reduzir a qualidade da experiência do usuário. Para cenários em tempo real, como rastreamento de delivery, normalmente é aceitável a cada 30-60 segundos. Para conteúdo de alteração mais lenta, como pontuações esportivas, atualize somente eventos significativos.

+++

+++Posso definir usuários como alvo com base no fato de eles terem a atividade online ativada?

Você precisará trabalhar com sua equipe de desenvolvimento para rastrear e transmitir essa preferência para o Adobe Experience Platform como um atributo do usuário e, em seguida, segmentar com base nesse atributo.

+++

### Perguntas sobre API

+++Qual é a diferença entre `timestamp` e `dismissal-date`?

* `timestamp`: A hora atual da época em que o evento ocorre, necessária para todos os eventos.
* `dismissal-date`: Uma época futura em que a atividade Live deve ser descartada automaticamente, necessária somente para eventos &quot;finais&quot;.

+++

+++Preciso enviar todos os `attributes` campos em cada chamada de atualização?

Sim, com base na sua classe `LiveActivityAttribute`.

* Todos os campos do objeto de atributos, incluindo `liveActivityData`, devem ser incluídos em cada chamada, para início, atualizações ou fim.
* Somente os campos `content-state` representam o que realmente muda dinamicamente em uma atividade ativa em execução.
* Incluir um objeto de alerta também garante que o push seja tratado como uma notificação visível ao usuário, não como uma notificação em segundo plano silenciosa. Obrigatório somente para casos de &quot;início&quot; e opcional.

+++

+++Em que formato devem estar os carimbos de data e hora da época?

Use o tempo de época Unix em **segundos** e não em milissegundos. Por exemplo: `1759937682`

+++

+++Posso usar o mesmo `requestId` para múltiplas chamadas de API?

Não. Cada solicitação de API deve ter um `requestId` exclusivo para garantir idempotência e rastreamento adequado. Usar UUIDs ou identificadores exclusivos semelhantes.

+++

+++Que autenticação é necessária para a API headless?

Consulte a [Documentação de Campanhas acionadas por API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) para obter os requisitos de autenticação, incluindo tokens OAuth e chaves de API.

+++

+++O que acontece se minha chamada de API falhar?

Implementar lógica de repetição com retirada exponencial. Verifique a resposta da API em busca de códigos de erro e mensagens para diagnosticar problemas. Falhas comuns incluem IDs de campanha inválidas, cargas mal formadas ou problemas de autenticação.

+++

+++Posso enviar atualizações de atividades em tempo real de meus próprios servidores de back-end?

Sim, esse é o comportamento pretendido. Seu back-end chama a API headless do Adobe Journey Optimizer para acionar eventos de atividade ao vivo quando a lógica comercial o exigir.

+++

+++Preciso de uma campanha diferente para iniciar, atualizar e encerrar eventos?

Não. Você pode usar a mesma campanha e alterar o campo `event` na carga. No entanto, algumas organizações preferem campanhas separadas para melhorar o rastreamento de análises.

+++

### Perguntas de solução de problemas

+++Minha atividade Live é iniciada, mas não é atualizada. Qual poderia ser o problema?

Causas comuns:

* Incompatível `liveActivityID` ou `channelID` entre as chamadas de início e atualização.
* `content-state` campos não correspondem à estrutura `ContentState`.
* A atividade Live já terminou.
* Problemas de conectividade de rede no dispositivo.
* O tempo de época usado como carimbo de data e hora não está atualizado.

+++

+++O campo `attributes-type` não está sendo reconhecido. O que devo verificar?

* Verifique se o nome da classe corresponde a **exatamente** (diferencia maiúsculas de minúsculas) com o nome da estrutura Swift
* Verifique se a estrutura está definida e registrada corretamente
* Verificar erros de digitação na carga JSON
* Confirmar se a versão do aplicativo instalada tem a implementação Atividade ativa

+++

+++Os usuários só veem a atualização da atividade Live e não a notificação de alerta. Esse é um problema conhecido?

Não. O campo `alert` é opcional e pode ser suprimido pelo iOS em determinadas condições, por exemplo, no modo Não Incomodar. A atividade online pode ser atualizada silenciosamente, o que geralmente é o comportamento pretendido. O campo de alerta é obrigatório para enviar inícios remotos, caso contrário, a apple o tratará como uma notificação em segundo plano silenciosa.

+++

+++Posso excluir ou limpar todas as instâncias de atividades Ativas para um usuário?

Você precisa enviar um evento &quot;end&quot; para cada instância de atividade ativa do Live. Rastreie quais instâncias de atividade do Live estão ativas para cada usuário em seus sistemas para que você possa limpá-las corretamente.

+++

+++Meu widget mostra &quot;Nenhum dado&quot; mesmo quando enviei uma atualização. Qual poderia ser o problema?

* Verifique se a implementação do widget acessa corretamente `context.state` e `context.attributes`.
* Verifique se os valores padrão ou estados de erro são manipulados na interface do widget.
* Use o protocolo `LiveActivityAssuranceDebuggable` para depurar o esquema.
* Teste com o Adobe Assurance para ver se os dados estão sendo recebidos.
+++
