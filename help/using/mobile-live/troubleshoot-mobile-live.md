---
solution: Journey Optimizer
product: journey optimizer
title: Solução de problemas de atividades em tempo real
description: Saiba como solucionar problemas de atividades ativas no Journey Optimizer para casos de uso unitários e de transmissão, incluindo problemas de token de perfil, configuração de campanha e falhas de delivery
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
source-git-commit: 016d905840a3ccc05ca1d2a934130b53c1108e7c
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---

# Solução de problemas de atividades em tempo real {#troubleshoot-mobile-live}

As atividades online no Adobe Journey Optimizer permitem atualizações dinâmicas e em tempo real nas telas bloqueadas do iOS e nas Ilhas dinâmicas. Eles só podem ser acionados e gerenciados por meio de Campanhas acionadas por API.

**Tipos de caso de uso:**

* **Unitário**: direcionado individualmente, transacional (campanhas transacionais acionadas por API)
* **Transmissão**: entrega em massa direcionada por público-alvo (campanhas de marketing acionadas por API)

Um desafio frequente com atividades Live é quando a chamada da API para acionar ou atualizar uma atividade Live retorna uma **resposta bem-sucedida (200 OK)**, mas a atividade Live não é exibida ou atualizada no dispositivo do usuário. Essa desconexão entre a confirmação da API e o comportamento real do dispositivo pode ocorrer em vários pontos do pipeline de entrega. Este guia fornece uma abordagem sistemática de solução de problemas para identificar onde o delivery está falhando, examinando cada estágio da validação da solicitação de API à renderização do dispositivo.

## Pré-requisitos

Antes de solucionar problemas, verifique se você tem:

* &#x200B;
  +++ Configurar uma sessão do Assurance

  Configure uma **sessão do Assurance** para capturar eventos do SDK e inspecionar o pipeline de entrega. O Assurance oferece visibilidade sobre:

   * Solicitações e respostas do Edge Network
   * Eventos de qualificação de perfil
   * Registro do token de push
   * Eventos de ciclo de vida de atividade ao vivo

  Saiba como configurar o Assurance na [documentação do Adobe Experience Platform Assurance](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance).

  **Observação**: para a atividade do iOS Live, verifique se seu aplicativo está sendo executado em um dispositivo físico iOS (iOS 16.1 ou posterior) ou no Xcode Simulator (iOS 16.1 ou posterior).

  +++

* &#x200B;
  +++ Coletar detalhes da campanha acionada pela API

  Navegue até a Campanha acionada pela API no Journey Optimizer e recupere:

   * Nome da campanha
   * ID da campanha encontrada nas propriedades URL ou campaign
   * Versão do Campaign, se aplicável
   * Configuração de superfície, superfície de aplicativo do iOS usada para atividade online

  +++

* &#x200B;
  +++ Coletar informações de solicitação da API

  Ao fazer a chamada de API para acionar a atividade Live, salve:

   * Carga de solicitação de API, incluindo identificadores de perfil e dados de atividade em tempo real
   * Resposta da API, incluindo código de status, ID da mensagem, ID da solicitação
   * Carimbo de data e hora de quando a API foi chamada
   * Ponto de extremidade usado, por exemplo, `/campaign/{CAMPAIGN_ID}/execute`

  +++

* &#x200B;
  +++ Identificar o perfil de teste

  Na solicitação da API, recupere:

   * Namespace de perfil, por exemplo, ECID, email, ID do cliente
   * ID de perfil usada na chamada de API

  Verifique se você pode pesquisar esse perfil no Adobe Experience Platform. Saiba como [pesquisar um perfil na documentação do Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html).

  +++

* &#x200B;
  +++ Informações do dispositivo e do aplicativo

  Colete o seguinte do seu dispositivo de teste:

   * Modelo do dispositivo, por exemplo, iPhone 14 Pro
   * Versão do iOS
   * Identificador do conjunto de aplicativos
   * Token de push de APNs
   * Status de conectividade de rede no momento do teste

  +++

## Cenários comuns

### Problemas de perfil ou token de push {#profile-issue}

[!BADGE Aplica-se a casos de uso unitários e de difusão]{type=Positive}

A API retorna HTTP 200, mas a atividade Live não é exibida. Causas comuns:

* O perfil não existe no Adobe Experience Platform.
* O token de push da atividade online não foi sincronizado com o perfil.
* Os detalhes de push da atividade ao vivo estão sincronizados, mas contêm configurações incorretas, por exemplo, `appId` ou `attributeType` incorretos.

**Observação para casos de uso de difusão**: se alguns perfis no seu público-alvo não tiverem tokens, somente eles não receberão a atividade Live. Obtenha amostras de vários perfis do seu público-alvo para diagnosticar problemas de token. Isso se aplica somente a eventos de início remoto, não a eventos de atualização ou término.

#### Pré-verificações

* Requisitos do aplicativo iOS:
   * iOS 16.1+
   * `NSSupportsLiveActivities` definido como `YES` em `Info.plist`
   * `ActivityAttributes` implementado corretamente.
* Integração do Mobile SDK:
   * Adobe Experience Platform Mobile SDK (mensagens do SDK 5.11.0+)
   * `Messaging.registerLiveActivities` implementado e chamado com token de push de atividade online.

#### Etapas de depuração

1. &#x200B;
   +++ Verificar se o perfil existe no Adobe Experience Platform

   1. No Journey Optimizer, navegue até **Cliente** `>` **Perfis**.
   1. Pesquisar usando o namespace e o valor de identidade da solicitação de API.
   1. Se o perfil não for encontrado, ele não existe ou a assimilação não foi concluída. Crie o perfil ou aguarde a assimilação antes de acionar a atividade Live.
   1. Se o perfil for encontrado, vá para a etapa 2 abaixo para verificar se o token de push está sincronizado.

      +++

1. &#x200B;
   +++ Verificar se o token de push da atividade online está sincronizado

   Você pode usar o Assurance para verificar o registro do token:

   1. No Assurance, na lista **Eventos**, filtre ou pesquise eventos `eventType = "liveActivity.pushToStart"`.
   1. Selecione o **Evento** e inspecione a carga.
   1. Verifique se os valores de token, appId e attributeType estão presentes.
   1. Confirme se o evento foi enviado com êxito.

   Também é possível fazer check-in do perfil do Adobe Experience Platform.

   1. No Adobe Experience Platform, em seu **Perfil**, acesse a guia **Eventos**.
   1. Pesquisar `liveActivity.pushToStart` eventos.
   1. Verifique o carimbo de data e hora e a carga do evento.

   Se nenhum evento for encontrado, o aplicativo móvel não está chamando `Messaging.registerLiveActivity` corretamente. Você precisa corrigir a integração do SDK.

   +++

1. &#x200B;
   +++ Validar detalhes do token no perfil

   1. Em seu **Perfil**, acesse a guia **Atributos**.
   1. Localizar `liveActivityPushNotificationDetails`.
   1. Verifique a configuração do token:

      ```json
      {
        "liveActivityPushNotificationDetails": [
          {
            "appId": "com.example.myapp",
            "token": "abc123def456...",
            "platform": "apns",
            "denylisted": false,
            "attributeType": "OrderTrackingAttributes",
            "identity": {}
          }
        ]
      }
      ```

   **Validar cada campo:**

   | Campo | Requisito | Problema comum |
   |-|-|-|
   | `appId` | Deve corresponder exatamente ao identificador de conjunto do iOS | Incompatibilidade entre IDs do pacote dev/prod |
   | `attributeType` | Deve corresponder exatamente ao nome de estrutura Swift `ActivityAttributes` (diferencia maiúsculas de minúsculas) | Erro de digitação ou nome de estrutura incorreto |
   | `platform` | Deve ser `"apns"` ou `"apnsSandbox"` | Valor de plataforma incorreto |
   | `denylisted` | Deve ser `false` | Token marcado como inválido ou usuário recusado |
   | `token` | Token de push de APNs válido | Token expirado ou aplicativo reinstalado |

   Se algum campo estiver incorreto: atualize o aplicativo móvel, registre-se novamente usando `Messaging.registerLiveActivities`, aguarde de 5-10 minutos e verifique novamente.

   Se `liveActivityPushNotificationDetails` estiver ausente: o token ainda não foi sincronizado. Aguarde de 5 a 10 minutos após ver o evento `liveActivity.pushToStart` no Assurance.

   +++

### Problemas de configuração de campanha e de carga {#payload-issues}

[!BADGE Aplica-se a casos de uso unitários e de difusão]{type=Positive}

O perfil existe com tokens válidos, mas a atividade Live não é exibida. Isso pode ser causado por:

* Configuração de superfície ou canal incorreta.
* Estrutura de carga de API incorreta.
* `content-state` e `attributes` não correspondem à implementação do iOS `ActivityAttributes`.
* Obsoleto `timestamp` (crítico para atualização/fim).

**Observação para casos de uso de difusão**: a campanha deve ser **Marketing acionado por API** (não Transacional). A carga usa `audience` em vez de `profile` individual. Consulte [esta seção](#broadcast-config) para obter a estrutura de conteúdo específica para difusão e a [documentação do Adobe Developer](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution) para obter as especificações completas da API.

#### Pré-verificações

* A campanha é **Transacional acionada por API** (unitária) ou a opção **Marketing acionado por API** (difusão) e **Alta Taxa de Transferência** deve ser **não** habilitada, pois é incompatível com a atividade online.
* Verifique se o perfil existe e se os tokens estão sincronizados corretamente usando o [cenário acima](#profile-issue).

#### Etapas de depuração

1. &#x200B;
   +++ Verificar a configuração da superfície de campanha

   1. No Journey Optimizer, abra a **Campanha** e navegue até o menu **Ações**.
   1. Verifique sua **configuração de atividade do Live**. A superfície deve ser configurada para o aplicativo iOS com um identificador de conjunto que corresponda a `appId` no `liveActivityPushNotificationDetails` do seu perfil. Por exemplo, se o seu perfil tem `"appId": "com.example.myapp"`, a superfície deve ter como alvo o mesmo aplicativo.
   1. Verifique se o **Tipo de atividade** na configuração da campanha corresponde exatamente ao `attributeType` no `liveActivityPushNotificationDetails` do seu perfil. Por exemplo, se o seu perfil tiver `"attributeType": "FoodDeliveryLiveActivityAttributes"`, a campanha deverá especificar esse mesmo tipo de Atividade.

      +++

1. &#x200B;
   +++Validar estrutura de carga da API

   Ao executar a campanha via API, verifique se a carga segue a estrutura correta.

   **Carga unitária:**

   ```json
   {
     "campaignId": "your-campaign-id",
     "recipients": [{
       "type": "aep",
       "userId": "user@example.com",
       "namespace": "email",
       "context": {
         "requestPayload": {
           "aps": {
             "content-available": 1,
             "timestamp": 1756984054,
             "event": "start",
             "attributes-type": "FoodDeliveryLiveActivityAttributes",
             "content-state": { ... },
             "attributes": { ... }
           }
         }
       }
     }]
   }
   ```

   **Problemas comuns de carga:**

   | Campo | Requisito | Problema comum |
   |-|-|-|
   | `attributes-type` | Deve corresponder ao tipo de Atividade de campanha e ao perfil `attributeType` | Incompatibilidade ou erro de digitação |
   | `campaignId` | Deve corresponder à ID da campanha ativada | ID de campanha incorreta ou ausente |
   | `content-available` | Deve ser `1` | Valor ausente ou incorreto |
   | `event` | Deve ser `"start"`, `"update"` ou `"end"` | Tipo de evento inválido |
   | `timestamp` | Deve ser sempre o horário atual/mais recente da época do Unix em segundos | Uso do carimbo de data e hora antigo/em cache |
   | `userId` / `namespace` | Deve corresponder a um perfil existente no AEP | Incompatibilidade do identificador de perfil |

   **Crítico: sempre usar o carimbo de data/hora mais recente**

   * O campo `timestamp` deve **sempre** ser o **horário atual da época Unix** (em segundos) no momento em que cada chamada de API é feita.
   * Isso se aplica a **todos os tipos de evento**: `start`, `update` e **especialmente`end`**.
   * **Impacto nas solicitações de atualizações/término**: o uso de um carimbo de data/hora obsoleto ou antigo fará com que as solicitações de atualização e término falhem ou sejam ignoradas pelo dispositivo.
   * **NÃO** reutilize carimbos de data/hora de solicitações anteriores ou use valores em cache.
   * Gere um carimbo de data e hora novo para cada chamada de API.

   **Campos opcionais (todos os tipos de evento):**

   * `requestId`: Identificador exclusivo para rastreamento (recomendado).
   * `alert`: Objeto com `title` e `body` para notificação (útil para chamar atenção para atualizações).

   **Sobre `dismissal-date`:**

   * Campo opcional que contém o tempo da época Unix (segundos).
   * **Relevante somente quando`event: "end"`**.
   * Especifica quando a atividade Live deve ser removida automaticamente do dispositivo.
   * Se não for fornecido no evento final, a atividade online permanecerá visível até que o usuário a ignore.
   * Deve ser um carimbo de data/hora futuro (posterior a `timestamp`).

     +++

1. &#x200B;
   +++ Alinhar a carga com a implementação do iOS

   Verifique se a carga da API corresponde à implementação `ActivityAttributes` do aplicativo iOS. O protocolo `LiveActivityAttributes` do Adobe SDK estende o iOS `ActivityAttributes` e requer uma propriedade `liveActivityData`.

   **Validar o mapeamento:**

   1. Seu `ActivityAttributes` deve implementar o protocolo `LiveActivityAttributes` da Adobe. Exemplo:

      ```swift
      struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
       public struct ContentState: Codable, Hashable {
           var orderStatus: String
           var estimatedDeliveryTime: String
       }
      
       // Adobe SDK requirement
       var liveActivityData: LiveActivityData
      
       // Your custom attributes
       var restaurantName: String
      }
      ```

      **Observe** que o campo `liveActivityData` é exigido pelo Adobe SDK e deve ser incluído em todas as implementações.

   1. A carga da API deve refletir a estrutura do iOS:

      ```json
      {
        "aps": {
           "event": "start",
           "timestamp": 1756984054,
           "attributes-type": "FoodDeliveryLiveActivityAttributes",
           "content-state": {
           "orderStatus": "Preparing",
           "estimatedDeliveryTime": "20 mins"
        },
        "attributes": {
          "liveActivityData": {
            "liveActivityID": "order-12345"
          },
          "restaurantName": "Pizza Palace"
        }
        }
      }
      ```

   **Lista de verificação de validação:**

   * Incluir todos os campos `ContentState` em `content-state` (obrigatório para todos os tipos de evento).
   * Incluir todos os campos `LiveActivityAttributes` em `attributes` (somente eventos iniciais), incluindo:
      * `liveActivityData` (obrigatório; geralmente contém `liveActivityID` ou identificador semelhante)
      * Todos os campos personalizados da estrutura
   * Corresponder nomes de campo exatamente (diferencia maiúsculas de minúsculas).
   * Corresponder tipos de dados (String, Int, Bool, objetos aninhados).
   * Preserva a estrutura do objeto aninhado.

   **Erros comuns:**

   | Problema | Impacto | Correção |
   |-------|--------|-----|
   | `liveActivityData` ausente nos atributos | A atividade online não iniciará | Sempre incluir objeto `liveActivityData` no evento inicial |
   | Campo obrigatório ausente no evento de início | A atividade online não iniciará | Adicionar todos os campos da estrutura do iOS |
   | Nome de campo incorreto (erro de digitação/uso de maiúsculas e minúsculas) | Campo ignorado ou erro de análise | Corresponder exatamente aos nomes de campo do iOS |
   | Tipo de dados incorreto | Erro de análise | Corresponder tipos de dados do iOS |
   | Objeto aninhado ausente | Dados incompletos | Incluir todas as estruturas aninhadas |
   | Incluindo `attributes` em atualização/fim | Desnecessário, mas geralmente ignorado | Incluir apenas `attributes` no evento inicial |
   | Carimbo de data/hora obsoleto na atualização/término | Atualização/fim ignorado pelo dispositivo | Sempre gerar carimbo de data/hora novo |

   Para obter mais exemplos, consulte [Criar página de atividade ao vivo](create-mobile-live.md).

   +++

1. &#x200B;
   +++ Testar com o Assurance

   Verifique a execução da API e o delivery de carga usando o Assurance:

   1. Abra sua sessão do Assurance.
   1. Execute a chamada de API para acionar a atividade Live.
   1. Na **Lista de Eventos**, verifique se:
      * Eventos de execução de campanha.
      * Eventos de entrega de atividades online.
      * Eventos de erro de validação de carga.
   1. Revise as cargas do evento para verificar:
      * A carga foi processada corretamente.
      * Não ocorreram erros de validação.
      * A atividade online foi enviada para APNs.

      +++

### Falhas de entrega e análise de erros

[!BADGE Aplica-se a casos de uso unitários e de difusão]{type=Positive}

Nesse cenário, todas as verificações anteriores foram aprovadas:

* O perfil existe com [tokens de push de atividades online válidos](#profile-issue)
* A campanha está [configurada corretamente com a carga adequada](#payload-issues)
* [Os tokens de atualização estão sincronizados](#token-not-synced) (somente para eventos de atualização/término, caso de uso unitário)

Mas a atividade Live ainda não é exibida, atualizada ou encerrada conforme esperado. O problema pode estar no nível do sistema de entrega da Adobe ou com o provedor de serviços de notificação por push (APNs).

**Observação para casos de uso de difusão**: os relatórios mostram as métricas de todos os membros do público-alvo. Alguns perfis podem ter sucesso, enquanto outros falham.

**Pré-verificações**

* **Cenários Anteriores Validados:**
   * O perfil existe com o `liveActivityPushNotificationDetails` correto
   * A superfície de campanha e o tipo de atividade estão corretos
   * A carga da API é válida com o carimbo de data e hora atual
   * Os tokens de atualização são sincronizados (para eventos de atualização/término)

* **Chamada de API Confirmada:**

   * A chamada de API retornou HTTP 200 (sucesso)
   * A ID da campanha e os detalhes do recipient estão corretos

#### Etapas de depuração

1. &#x200B;
   +++ Verificar relatórios de campanha

   1. Navegue até a **Campanha de atividade ao vivo**.
   1. Clique no botão **Relatórios**.
   1. Selecione **Exibir relatório de todos os tempos**.
   1. Analise as seguintes seções:

      1. Verifique as métricas **Estatísticas de envio** para entender o sucesso da entrega:

         | Métrica | O que significa | O que procurar |
         |-|-|-|
         | Direcionado | Número de perfis qualificados para o público | Deve incluir seu perfil de teste |
         | Envios | Total de tentativas de notificações por push | Deve corresponder às chamadas de API |
         | Entregues | Entregue com sucesso a dispositivos | Compare com Envios para ver a taxa de sucesso |
         | Enviar erros | Notificações por push que não foram enviadas | Números altos |
         | Enviar exclusões | Perfis excluídos pelo Adobe Journey Optimizer | Verifique se o seu perfil foi excluído |

      1. Se Enviar erros > 0, verifique a tabela **Motivos de Erro** para obter códigos de erro e mensagens específicas:

         | Erro comum | Significado | Resolução |
         |-|-|-|
         | Token inválido | O token de push é inválido ou expirou | Registrar novamente os tokens de atividade ao vivo do dispositivo |
         | Token não encontrado | Nenhum token válido associado ao perfil | Verificar se `liveActivityPushNotificationDetails` existe |
         | APNs rejeitadas | O serviço de Notificação por push do Apple rejeitou o push | Verificar certificado APNs, ID do pacote, ambiente |
         | Tempo limite de rede | Não é possível acessar APNs | Problema transitório; repetir a chamada da API |

      1. Se **Enviar exclusões** > 0, verifique a tabela **Motivos excluídos**:

         | Exclusão comum | Significado | Resolução |
         |-|-|-|
         | Perfil recusado | O usuário recusou as notificações | Verificar status de consentimento do perfil |
         | Token alterado | Token marcado como inválido | Registre o token novamente ou verifique o status do incluo na lista de bloqueios |
         | Perfil não qualificado | O perfil não atende aos critérios da campanha | Revisar regras de público-alvo da campanha |

   Saiba mais na [página de relatório de campanha de atividades ao vivo](../reports/campaign-global-report-cja-activity.md).

   +++

1. &#x200B;
   +++ Verificar eventos de feedback da mensagem no perfil

   1. Navegue até **Cliente** > **Perfis** na Journey Optimizer.
   1. Procure e abra o perfil.
   1. Selecione a guia **Eventos**.
   1. Filtrar ou pesquisar eventos com `eventType = "message.feedback"`.
   1. Procure eventos de feedback que correspondam aos tipos `liveActivityID` e `event` da atividade Ativa.
   1. Revise os seguintes campos principais:

      | Campo | Valores possíveis | O que significa |
      |-|-|-|
      | `feedbackStatus` | `sent`, `error`, `denylist` | Resultado da entrega do provedor de serviços |
      | `serviceProvider` | `apns/apnsSandbox` | Deve ser APNs para atividades do iOS Live |
      | `errorCode` | Código numérico ou `null` | Código de erro específico de APNs em caso de falha |
      | `errorMessage` | Descrição de erro ou `null` | Mensagem de erro legível |

   1. **Se `feedbackStatus: "error"`:**
      * Verifique o `errorCode` e o `errorMessage` quanto a erros de APNs específicos
      * Erros comuns de APNs incluem token expirado, certificado inválido, ID de pacote incorreta

   1. **Se nenhum evento de feedback for encontrado:**
      * A notificação por push pode não ter sido tentada
      * Verifique se o perfil foi excluído nos Relatórios de campanha, conforme detalhado na Etapa 1 acima.

      +++

1. &#x200B;
   +++ Verificar a entrega de atividade em tempo real para APNs no Assurance

   1. Abra a sessão do Assurance. Ela deve estar ativa durante a chamada de API.
   1. Execute a chamada de API (start, update ou end).
   1. Na **Lista de Eventos**, procure por eventos de entrega de atividades online.
   1. Procure eventos relacionados à entrega por push de APNs.
   1. Verifique os seguintes indicadores:
      * **Solicitação de push para APNs**: confirma que a Adobe enviou o push para os servidores da Apple
      * **Resposta APNs**: mostra se APNs aceitaram ou rejeitaram o push
      * **Status da entrega**: indicação de êxito ou falha
   1. Se forem encontrados problemas, consulte os seguintes problemas comuns de delivery de APNs:

      | Problema | Sintoma no Assurance | Resolução |
      |-|-|-|
      | Certificado APNs expirado | Erro de autenticação | Renovar e carregar novo certificado APNs |
      | Ambiente errado (desenvolvimento vs. produção) | Erro de incompatibilidade de token | Verifique se o certificado corresponde ao tipo de build do aplicativo |
      | Incompatibilidade de ID do pacote | Identificador de conjunto inválido | Verificar se a ID do conjunto de certificados corresponde ao aplicativo |
      | Token expirado | Erro InvalidToken de APNs | Registrar tokens de atividade ao vivo novamente |
      | Limitação de taxa | Solicitações demais | Reduzir a frequência de chamada da API |

      +++

1. &#x200B;
   +++ Prosseguir com verificações de diagnóstico adicionais

   1. Verifique as métricas de ciclo de vida de atividade Ativo no Relatório de campanha.

      No relatório de campanha, revise a seção **Ciclo de vida da atividade em tempo real**:

      | Métrica | O que verificar |
      |-|-|
      | Início remoto | Deve mostrar a contagem de inicializações acionadas por API |
      | Atualizações | Deve mostrar a contagem de eventos de atualização |
      | Término | Deve mostrar a contagem de eventos finais |
      | Contagem total | Volume geral do evento de atividade Ativa |

      Se essas métricas forem zero ou não corresponderem às chamadas da API, há um problema de delivery entre o Adobe e os APNs.

   1. Se o Adobe mostrar entrega bem-sucedida, mas o dispositivo não mostrar a atividade Live:

      * Verifique se há erros de atividade ao vivo nos logs de dispositivos do iOS.
      * Verifique se o aplicativo está em primeiro ou segundo plano (não finalizado).
      * Confirme se o dispositivo tem conectividade de rede.
      * Teste em vários dispositivos para descartar problemas específicos do dispositivo.
      * Verifique se a versão do iOS é 16.1 ou posterior.

      +++

1. &#x200B;
   +++ Escalonamento para o suporte da Adobe

   Se você concluiu todas as etapas e o problema permanece não resolvido, entre em contato com o Atendimento ao cliente da Adobe com:

   **Informações necessárias:**

   * ID e nome da campanha
   * Namespace e ID do perfil
      * `liveActivityID` da carga da API
   * Carimbos de data e hora de chamadas de API
   * Capturas de tela de:
      * Relatórios De Campanha (Estatísticas De Envio, Motivos De Erro, Motivos Excluídos)
      * Eventos de Perfil (`liveActivity.updateToken`, `message.feedback`)
      * Sessão do Assurance mostrando eventos de entrega
   * Carga de solicitação de API concluída
   * Detalhes do certificado APNs (expiração, ambiente, ID do pacote)

     +++

## Cenários específicos unitários

### Token de atualização de atividade online não sincronizado{#token-not-synced}

A atividade Live é iniciada com êxito no dispositivo, mas as chamadas de API `update` ou `end` subsequentes (retornando HTTP 200) não atualizam ou descartam a atividade Live. Isso ocorre quando o **token de atualização de atividade em tempo real** não é sincronizado corretamente com o sistema da Adobe.

**Noções básicas sobre tokens de atualização**

Quando uma atividade Live é iniciada em um dispositivo, o iOS gera um token de atualização exclusivo para essa instância de atividade Live específica. Este token é necessário para:

* Envio de atualizações para a atividade Live
* Encerrando a atividade Live remotamente

Cada instância da atividade Live tem seu próprio token de atualização exclusivo. O Adobe precisa desse token para fornecer eventos de atualização e término.

**Comportamento esperado**

Para que os eventos de atualização e término funcionem, o seguinte deve ocorrer:

1. A atividade online é iniciada com sucesso no dispositivo.
1. O dispositivo gera um token de atualização para a instância da atividade Live.
1. O Mobile SDK captura e envia o token de atualização para a Adobe.
1. O token de atualização é sincronizado e armazenado no sistema do Adobe.
1. As chamadas de API subsequentes para atualização/fim usam esse token para entrega.

**Pré-verificações:**

* **Permissão de usuário**: na primeira vez que uma atividade ao vivo é iniciada em um dispositivo, o iOS exibe um prompt do sistema: &quot;Permitir que o [Nome do aplicativo] forneça atualizações de atividade ao vivo?&quot; O usuário **deve tocar em &quot;Permitir&quot;** para que os tokens de atualização sejam gerados e sincronizados. Se o usuário tocar em &quot;Não permitir&quot;, nenhum token de atualização será criado e as solicitações de atualização/encerramento falharão. Esta é uma permissão única por aplicativo.
* **Validação de Perfil e Campanha**: Conclua as verificações do [Cenário 1](#profile-issue) e do [Cenário 2](#payload-issues) para garantir que o perfil, os tokens e a configuração da campanha estejam corretos.

#### Etapas de depuração

1. &#x200B;
   +++ Verificar sincronização do token de atualização no Assurance

   1. Abra sua sessão do Assurance.
   1. Verifique se a sessão estava ativa quando a atividade Live foi iniciada no dispositivo.
   1. Filtrar ou pesquisar eventos com `eventType = "liveActivity.updateToken"`.
   1. Selecione o evento e inspecione a carga:

      * Verifique se o campo `token` contém uma cadeia de token de atualização válida.
      * Verifique se o `liveActivityID` corresponde à sua instância de atividade do Live.
      * Confirme se o `activityType` corresponde ao seu `attributes-type`.

   1. Se o evento não for encontrado:

      * O token de atualização não foi gerado ou capturado pela SDK.
      * Verifique se o usuário recebeu permissões de atividade em tempo real.
      * Verifique se a atividade Live foi iniciada com êxito no dispositivo.
      * Confirme se o SDK para dispositivos móveis está integrado corretamente para capturar tokens de atualização.

   1. Se o evento for encontrado, prossiga para a Etapa 2.

      +++

2. &#x200B;
   +++ Verificar token de atualização em eventos de perfil

   1. Navegue até **Cliente** > **Perfis** na Journey Optimizer.
   1. Procure e abra o perfil.
   1. Selecione a guia **Eventos**.
   1. Procurar `liveActivity.updateToken` eventos.
   1. Verifique os detalhes do evento:

      * Verifique se o carimbo de data e hora é recente (corresponde ao início da atividade online).
      * Confirme se `token` e `liveActivityID` estão presentes.
      * Verifique se `activityType` está correto.

   1. Se o evento não for encontrado no perfil:

      * O evento de token de atualização pode não ter sido assimilado no perfil ainda.
      * Aguarde de 5 a 10 minutos e verifique novamente.
      * Se ainda estiver ausente após 15 minutos, pode haver um problema de assimilação de evento.

   1. Se um evento for encontrado, o token de atualização foi sincronizado. Você pode prosseguir para a Etapa 3.

      +++

3. &#x200B;
   +++ Verificar eventos de entrega de atividade em tempo real no Assurance

   1. Na sessão do Assurance, execute uma chamada de API de atualização ou fim.
   1. Na **Lista de Eventos**, procure por eventos de entrega de atividade (eventos de push APNs).
   1. Verificar se há eventos que indicam:
      * Notificação por push enviada para APNs.
      * Resposta de APNs (sucesso ou erro).
      * Confirmação de entrega.
   1. Se um evento de delivery APNs estiver presente: a notificação por push foi enviada. Se o dispositivo ainda não for atualizado, o problema pode estar no lado do dispositivo (aplicativo que não lida com push, problemas de rede etc.).
   1. Se o evento de entrega APNs estiver ausente: o token de atualização pode não estar armazenado ou associado corretamente ao perfil no sistema do Adobe.
   1. Se houver eventos de erro: inspecione os detalhes do erro em busca de motivos específicos de falha (token inválido, APNs rejeitados etc.).

      +++

## Cenários específicos de transmissão

### Problemas de configuração da campanha de transmissão e de carga{#broadcast-config}

Esta seção aborda cenários de solução de problemas específicos para atividades de transmissão ao vivo, que exigem abordagens de depuração diferentes das campanhas unitárias.

Quando os perfis têm tokens válidos, mas a atividade Ao vivo não é exibida, atualizada ou se comporta conforme esperado para membros do público-alvo, o problema normalmente resulta de um dos seguintes:

* A campanha não está configurada como Marketing acionado por API.
* A carga da API usa uma estrutura de difusão incorreta (ausente `audience` ou `input-push-channel`).
* Os campos `content-state` e `attributes` não correspondem à implementação do iOS `ActivityAttributes`.
* O `input-push-channel` não foi criado corretamente no Portal do Desenvolvedor do Apple.

Este cenário de solução de problemas se aplica a todos os eventos de atividade Live em campanhas de difusão: `start`, `update` e `end`.

**Pré-verificações:**

* **Tipo de campanha**:
   * Verifique se a campanha foi criada como Marketing acionado por API (necessário para campanhas com base em transmissão/público-alvo).
   * Confirme se um público-alvo está definido na configuração da campanha.
* **Validação de Perfil e Token**: exemplifique vários perfis do público-alvo para verificar se eles têm um `liveActivityPushNotificationDetails` válido. Para obter etapas de validação detalhadas, siga o [Cenário 1](#profile-issue).

#### Etapas de depuração

1. &#x200B;
   +++ Verificar a configuração do público-alvo da campanha

   1. Abra sua **Campanha de Marketing Acionado pela API** na Journey Optimizer.
   1. Navegue até a seção **Público-alvo** e verifique:
      * Um público é selecionado para a campanha.
      * A ID de público-alvo corresponde à ID usada na carga da API.
      * O público-alvo contém os perfis esperados.
   1. Navegue até a seção **Ações**.
   1. Verifique a **configuração da atividade online**:
      * A configuração deve ser definida para o aplicativo iOS com o identificador de pacote correto.
      * O tipo de atividade deve corresponder ao `attributes-type` na carga da API. Por exemplo, se sua carga contém `"attributes-type": "AirplaneTrackingAttributes"`, a campanha deve especificar esse mesmo tipo de Atividade.

      +++

1. &#x200B;
   +++ Validar a estrutura de carga da API de transmissão

   A estrutura de carga da transmissão é diferente das campanhas unitárias. Verifique se a carga segue o formato de transmissão correto.

   **Campos obrigatórios para difusão:**

   ```json
   {
     "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
     "audience": {
       "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
     },
     "context": {
       "requestPayload": {
         "aps": {
           "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
           "content-available": 1,
           "timestamp": 1771829292,
           "event": "update",
           "attributes-type": "AirplaneTrackingAttributes",
           "content-state": { ... },
           "attributes": { ... }
         }
       }
     }
   }
   ```

   **Problemas comuns de carga:**

   | Campo | Requisito | Problema comum |
   |-|-|-|
   | `campaignId` | Deve corresponder à ID de campanha de marketing ativada | ID de campanha incorreta ou uso da campanha transacional |
   | `audience.id` | Deve corresponder a um público-alvo existente no AEP | ID de público-alvo ou público-alvo incorreto não existe |
   | `input-push-channel` | Obrigatório para transmissão - Identificador exclusivo para esta instância de transmissão | Ausente ou não corresponde a `channelID` em `liveActivityData` |
   | `timestamp` | Deve ser sempre o horário atual/mais recente da época do Unix em segundos | Uso do carimbo de data e hora antigo/em cache |
   | `event` | Deve ser `"start"`, `"update"` ou `"end"` | Tipo de evento inválido |
   | `attributes-type` | Deve corresponder ao tipo de Atividade da campanha | Incompatibilidade ou erro de digitação |
   | `content-available` | Deve ser `1` | Valor ausente ou incorreto |

   **Campos críticos específicos da difusão:**

   * **`input-push-channel`**
      * Obrigatório para todas as atividades de transmissão ao vivo.
      * Atua como um identificador exclusivo para essa instância de transmissão específica.
      * Todos os perfis no público-alvo recebem atividades ao vivo vinculadas a este canal.
      * Deve corresponder a `channelID` em `liveActivityData.channelID` (consulte a Etapa 3).
      * Deve ser criado para `appID` no Portal do Desenvolvedor do Apple pelo cliente.
      * Somente os canais criados para o `appID` específico podem ser usados para transmitir a atividade em tempo real nesse aplicativo.

   * **`audience.id`**
      * Deve fazer referência a um segmento de público-alvo válido criado no Adobe Experience Platform.
      * Todos os perfis neste público-alvo são direcionados para a atividade Live.
      * O público deve ser ativado e conter perfis com `liveActivityPushNotificationDetails` válido.

   **Sempre usar o carimbo de data/hora mais recente:**

   * O campo `timestamp` deve ser sempre o tempo da época Unix atual (em segundos) para cada chamada de API.
   * Este requisito se aplica a todos os tipos de evento: `start`, `update` e `end`.
   * **Crítico para atualizações/fim**: usar carimbos de data/hora obsoletos faz com que as solicitações de atualização e término falhem.
   * Gere um carimbo de data e hora novo para cada chamada de API de transmissão.

   **Campos opcionais:**

   * `dismissal-date`: Tempo de época Unix para descarte automático (relevante somente para `end` eventos)
   * `alert`: Objeto com `title` e `body` para notificação

   Consulte a [documentação da API de Mensagens do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/messaging) para obter as especificações completas da API.

   +++

1. &#x200B;
   +++ Alinhar o estado do conteúdo, os atributos e o canal de push de entrada com a implementação do iOS

   Verifique se os campos de carga correspondem à implementação `ActivityAttributes` do aplicativo iOS e se `input-push-channel` corresponde a `channelID` em `liveActivityData`.

   1. Revise sua definição de Atributos da atividade do iOS.

   Sua estrutura `ActivityAttributes` personalizada deve implementar o protocolo `LiveActivityAttributes` da Adobe:

   ```swift
   struct AirplaneTrackingAttributes: LiveActivityAttributes {
    public struct ContentState: Codable, Hashable {
        var journeyProgress: Int
    }
   
    // Adobe SDK requirement
    var liveActivityData: LiveActivityData
   
    // Your custom attributes
    var arrivalAirport: String
    var departureAirport: String
    var arrivalTerminal: String
   }
   ```

   1. Mapeie os campos do iOS para a carga da API de transmissão.

   Para todos os eventos, inclua `attributes` e `content-state`:

   ```json
         {
         "aps": {
          "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
          "event": "start",
          "timestamp": 1771829292,
          "attributes-type": "AirplaneTrackingAttributes",
          "content-state": {
            "journeyProgress": 0
          },
          "attributes": {
            "arrivalAirport": "DEL",
            "departureAirport": "MUM",
            "arrivalTerminal": "T1",
            "liveActivityData": {
              "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
            }
          }
         }
         }
   ```

   **Crítico: `input-push-channel` deve corresponder a`channelID`**

   * O valor `input-push-channel` na raiz de `aps` deve corresponder exatamente a `channelID` em `liveActivityData`.
   * No exemplo acima, ambos os valores são `"FEt0NgvLEfEAAOqA6AXdIQ=="`.
   * Isso vincula a instância de transmissão aos dados de atividade Live.
   * Uma incompatibilidade causa falhas de delivery.

   **Pontos principais de validação:**

   * Incluir todos os campos `ContentState` em `content-state` para todos os tipos de evento.
   * Incluir todos os campos personalizados `LiveActivityAttributes` em `attributes` somente para eventos iniciais.
   * Para eventos de início, `liveActivityData.channelID` deve corresponder a `input-push-channel`.
   * Os nomes de campos diferenciam maiúsculas de minúsculas e devem corresponder exatamente.
   * Os tipos de dados devem corresponder (String, Int, Bool, objetos aninhados etc.).
   * Para eventos de atualização/encerramento, use o mesmo `input-push-channel` que o evento inicial original.

   **Erros comuns:**

   | Problema | Impacto | Correção |
   |-|-|-|
   | `input-push-channel` ausente | A transmissão não funcionará | Adicionar ID de canal exclusiva para cada transmissão |
   | `input-push-channel` não corresponde a `channelID` | A atividade online não iniciará | Certifique-se de que ambos os valores sejam idênticos |
   | Diferente de `input-push-channel` para atualização/fim | Atualizar/encerrar não atingirá as atividades Live | Usar a mesma ID de canal no ciclo de vida |
   | `liveActivityData.channelID` ausente | A atividade ao vivo não será vinculada à transmissão | Incluir `channelID` em atributos para iniciar evento |
   | Campo obrigatório ausente no evento de início | A atividade online não iniciará | Adicionar todos os campos da estrutura do iOS |
   | Nome de campo incorreto (erro de digitação/uso de maiúsculas e minúsculas) | Campo ignorado ou erro de análise | Corresponder exatamente aos nomes de campo do iOS |
   | Carimbo de data/hora obsoleto na atualização/término | Atualização/fim ignorado pelos dispositivos | Sempre gerar carimbo de data/hora novo |

   +++

1. &#x200B;
   +++ Testar com o Assurance

   Verifique a execução da API e o delivery de carga usando o Assurance:

   1. Abra a sessão do Assurance em um dispositivo de teste que faça parte do público-alvo.
   1. Execute a chamada de API de transmissão.
   1. Na **Lista de Eventos**, procure:
      * Eventos de execução de campanha.
      * Eventos de entrega de atividades online.
      * Eventos de erro que indicam falhas de validação de carga.
   1. Inspecione as cargas do evento para confirmar:
      * A carga foi processada corretamente.
      * O `input-push-channel` está presente.
      * Não ocorreram erros de validação.
      * As atividades ativas foram enviadas para APNs para membros do público-alvo.

      +++

### O perfil não está no público-alvo ou no instantâneo de público-alvo obsoleto

Nesse cenário, a campanha e a carga são configuradas corretamente, mas perfis específicos não recebem a atividade Live. Isso normalmente ocorre quando:

* O perfil não é um membro do público vinculado à campanha.
* O público-alvo é um público-alvo em lote e contém um instantâneo desatualizado dos dados do perfil.
* Os tokens de atividade do perfil do Live foram adicionados recentemente, mas ainda não foram refletidos no instantâneo do público-alvo.

Esse cenário de solução de problemas se aplica especificamente a campanhas de transmissão que usam direcionamento baseado em público-alvo.

**Noções básicas sobre a avaliação de público-alvo**

O Adobe Experience Platform usa diferentes métodos de avaliação de público-alvo que determinam quando as atualizações de perfil são refletidas no público-alvo:

| Método | Frequência de avaliação | Atualização de dados | Melhor para |
|-|-|-|--|
| Lote | Uma vez por dia (agendado) | Pode estar obsoleto por até 24 horas | Grandes públicos-alvo, sem distinção de tempo |
| Transmissão | Tempo real (em alterações de perfil) | Quase em tempo real para perfis atualizados | Requer atualizações de perfil, diferencia tempo |

**Pré-verificações:**

* **Validação de campanha e carga**:
   * Conclua as verificações em [este cenário](#broadcast-config) para garantir que a campanha e a carga estejam corretas.
   * Verifique se o `audience.id` na carga da API corresponde à configuração da campanha.
* **Perfil Existe**: confirme se o perfil existe no AEP com um `liveActivityPushNotificationDetails` válido.

#### Etapas de depuração

1. &#x200B;
   +++ Verificar se o perfil está no público

   Primeiro, confirme se o perfil que deve receber a atividade Live faz parte do público-alvo.

   1. Navegue até **Públicos-alvo** no Adobe Experience Platform.
   1. Procure e abra o público-alvo usando o `audience.id` da sua campanha.
   1. Clique em **Procurar** ou **Perfis de amostra** para exibir membros do público-alvo.
   1. Procure pelo perfil de teste usando o valor de namespace e identidade.
   1. **Se o perfil não for encontrado na audiência:**
      * O perfil não atende aos critérios de público-alvo ou às regras de segmento.
      * Revise a definição de público-alvo para entender os requisitos de associação.
      * Atualize os dados do perfil ou a definição do público-alvo para incluir o perfil.
      * Aguarde a conclusão da avaliação do público-alvo (consulte Etapa 2).
   1. **Se o perfil for encontrado no público-alvo:** Vá para a Etapa 2 para verificar a atualização dos dados.

      +++

2. &#x200B;
   +++ Verificar o tipo e a programação da avaliação do público-alvo

   Identifique se o público-alvo usa avaliação em lote ou por transmissão, pois isso determina a atualização dos dados.

   1. Na página **Detalhes do público-alvo**, verifique o **Método de avaliação**:
      * **Lote**: avaliado uma vez por dia de acordo com um agendamento.
      * **Streaming**: avaliado em tempo real quando ocorrem atualizações de perfil.
      * **Edge**: avaliado em locais de borda em tempo real.

   Siga as etapas apropriadas de solução de problemas com base no método de avaliação:

   **Se o público-alvo usar a Avaliação em lote:**

   1. **Compreender as limitações de público-alvo em lotes:**
      * Os públicos-alvo em lote são avaliados uma vez por dia (normalmente durante a noite).
      * O instantâneo do público-alvo pode ter até 24 horas.
      * Se um perfil registrou tokens de atividade ao vivo recentemente, esses tokens podem não estar no instantâneo atual.
      * As atualizações para perfis não serão refletidas até a próxima avaliação do lote.

   1. **Verificar quando ocorreu a última avaliação:**
      * Nos detalhes do público, procure pelo carimbo de data e hora **Última avaliação**.
      * Se o `liveActivityPushNotificationDetails` do perfil foi atualizado após esse carimbo de data/hora, o público-alvo tem dados obsoletos.

   1. **Resolver dados obsoletos:**
      1. **Opção 1: Aguardar a avaliação agendada do lote**
         * A próxima avaliação do lote incluirá os dados atualizados do perfil.
         * Isso acontece automaticamente uma vez por dia.
         * Melhor para cenários não urgentes.

      1. **Opção 2: acionar avaliação de público-alvo sob demanda**
         1. Navegue até **Públicos-alvo** no AEP.
         1. Selecione o público-alvo.
         1. Clique em **Avaliar agora** ou **Ativar sob demanda**.
         1. Aguarde a conclusão da avaliação (isso pode levar de alguns minutos a horas, dependendo do tamanho do público).
         1. Verifique se o perfil agora atualizou os dados no instantâneo do público-alvo.
         1. Tente novamente a chamada da API de transmissão.

   **Se o público-alvo usar a avaliação de Streaming:**

   1. **Entender o comportamento de transmissão de público:**
      * Os públicos-alvo de transmissão são avaliados em tempo real quando ocorrem atualizações de perfil.
      * **Novos perfis**: qualifique-se logo após a criação se eles atenderem aos critérios de segmento.
      * **Perfis atualizados**: qualifique ou desqualifique logo após ser atualizado.
      * **Perfis inalterados existentes**: não serão reavaliados, a menos que ocorra uma atualização.

   1. **Identificar o problema:**
      * Se um perfil já existir e atender aos critérios de segmento, mas nenhuma atualização ocorrer nesse perfil, ele não poderá ser adicionado a um público de transmissão recém-criado.
      * O perfil deve receber uma atualização (qualquer alteração de atributo) para acionar a reavaliação.

   1. **Resolver o problema:**
      * **Para novos perfis**: eles se qualificam automaticamente se os critérios forem atendidos. Nenhuma ação necessária.
      * **Para perfis existentes sem atualizações recentes:**
         * Fazer uma atualização secundária no perfil (por exemplo, atualizar um campo de carimbo de data e hora).
         * Isso aciona a avaliação de transmissão e adiciona o perfil ao público-alvo.
         * Alternativa: use um público-alvo em lote ou público-alvo de borda para perfis existentes.

      +++
