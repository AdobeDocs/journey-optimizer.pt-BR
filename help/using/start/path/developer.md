---
title: Introdução para desenvolvedores
description: Como desenvolvedor(a), saiba mais sobre como trabalhar com o Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: ht
source-wordcount: '1816'
ht-degree: 100%

---

# Introdução para desenvolvedores {#get-started-developers}

Como **desenvolvedor(a)**, você é responsável pela implementação e integração do [!DNL Adobe Journey Optimizer] nos aplicativos e sistemas. É possível começar a trabalhar com o [!DNL Adobe Journey Optimizer] assim que o(a) [admin de sistema](administrator.md) e o(a) [engenheiro(a) de dados](data-engineer.md) concederem acesso e prepararem o ambiente.

## Sua função no ecossistema do Journey Optimizer

Enquanto outros membros da equipe configuram o Journey Optimizer por meio da interface, você se concentrará em:

* **Implementar SDKs** em aplicativos para dispositivos móveis e web
* **Enviar eventos** a partir dos aplicativos para acionar jornadas
* **Criar pontos de acesso de API** que o Journey Optimizer pode chamar por meio de ações personalizadas
* **Integrar** o Journey Optimizer aos sistemas e infraestrutura existentes
* **Testar e depurar** implementações

O [Engenheiro de dados](data-engineer.md) manipulará esquemas de dados, configurações de eventos e fontes de dados. O [Admin](administrator.md) definirá as permissões e as configurações de canal. [Os profissionais de marketing](marketer.md) criarão as jornadas e o conteúdo que usa as implementações.

Este guia aborda as etapas essenciais de implementação técnica para uma introdução ao Journey Optimizer. Se estiver criando aplicativos para dispositivos móveis, experiências da web ou integrações de API, siga as seções abaixo para configurar a implementação.

## Pré-requisitos {#prerequisites}

Antes de iniciar a implementação, verifique se possui:

| Categoria | Exigências |
|----------|-------------|
| **Competências técnicas** | * Experiência com JavaScript (para SDK da web) ou Swift/Kotlin (SDK para dispositivos móveis)<br>* Noções básicas sobre APIs RESTful e JSON<br>* Familiaridade com programação assíncrona e arquiteturas orientadas por eventos<br>* Conhecimento da arquitetura de aplicativos da organização |
| **Acesso e ferramentas** | * Acesso ao [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para credenciais de API<br>* Ambiente de desenvolvimento com acesso à base do código do aplicativo<br>* Ferramentas de teste como o Postman para teste de API<br>* Ferramentas de desenvolvedor do navegador ou ferramentas de depuração para dispositivos móveis |
| **De outros membros da equipe** | * Concessão de acesso ao ambiente pelos esquemas XDM do [Admin](administrator.md)<br>* e definições de evento do [Engenheiro de dados](data-engineer.md)<br>* Requisitos e casos de uso dos [Profissionais de marketing](marketer.md) |

## Compreender as bases técnicas {#technical-foundation}

Antes de se aprofundar na implementação, familiarize-se com os conceitos técnicos principais:

1. **Integração da Adobe Experience Platform**: o Journey Optimizer foi criado nativamente na Adobe Experience Platform. Compreender a arquitetura subjacente ajudará a criar implementações mais eficazes. Saiba mais sobre [como o Journey Optimizer funciona](../understanding-ajo.md).

1. **Modelos de dados XDM**: o Journey Optimizer usa o Experience Data Model (XDM) para estruturar dados de evento e perfil. Como desenvolvedor(a), será necessário entender como enviar dados que estejam em conformidade com os esquemas configurados pelo [Engenheiro de dados](data-engineer.md). Saiba mais sobre [esquemas XDM](../../data/get-started-schemas.md).

1. **Autenticação e segurança**: todas as implementações exigem autenticação adequada. Entenda como configurar a autenticação para SDKs e APIs. Saiba mais sobre [Autenticação de API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configurar integrações de aplicativos para dispositivos móveis {#mobile-integration}

### Configurar o SDK para dispositivos móveis da Adobe Experience Platform

Para habilitar notificações por push, mensagens no aplicativo e outros recursos móveis, integre o SDK para dispositivos móveis da Adobe Experience Platform nos aplicativos móveis.

1. **Instalar e configurar o SDK para dispositivos móveis**: siga a [documentação do SDK para dispositivos móveis da Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} para ver uma introdução à integração do SDK.

1. **Criar uma propriedade móvel**: configure uma propriedade móvel na [!DNL Adobe Experience Platform Data Collection]. Saiba como [criar e configurar uma propriedade móvel](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurar notificações por push**:
   * Para **aplicativos iOS**: registre o aplicativo com APNs (serviço de notificação por push da Apple). Saiba mais na [documentação da Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Para **aplicativos Android**: configure o Firebase Cloud Messaging para seu aplicativo Android. Saiba mais na [documentação do Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testar a integração móvel**: use o [fluxo de trabalho de início rápido da integração para dispositivos móveis](../../push/mobile-onboarding-wf.md) para definir e testar rapidamente a configuração para dispositivos móveis.

As etapas detalhadas para configurar notificações por push estão disponíveis [nesta página](../../push/push-configuration.md).

### Implementar experiências baseadas em código (SDK para dispositivos móveis)

Para personalização nativa de aplicativos móveis com experiências baseadas em código:

* Siga [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} para a implementação do SDK para dispositivos móveis
* Revise as implementações de exemplo do [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} e do [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementar experiências da web {#web-implementation}

### Configurar o SDK da web da Adobe Experience Platform

Para implementações baseadas na web, o SDK da web é o principal ponto de integração:

1. **Instalar o SDK da web**: siga o [guia de implementação do SDK da web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} para configurar o SDK no site.

1. **Configurar sequências de dados**: crie e configure uma sequência de dados na [!DNL Adobe Experience Platform Data Collection] com o Journey Optimizer habilitado. Saiba mais na [documentação das sequências de dados](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}.

1. **Habilitar notificações por push da web** (opcional): configure a [propriedade pushNotifications](https://experienceleague.adobe.com/pt-br/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} na configuração do SDK da web e use o [comando sendPushSubscription](https://experienceleague.adobe.com/pt-br/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} para registrar assinaturas por push.

### Implementar experiências baseadas em código (SDK da web)

Experiências baseadas em código permitem personalizar qualquer ponto de contato digital:

1. **Escolha o método de implementação**: lado do cliente, lado do servidor ou híbrido. Revise os [exemplos de implementação](../../code-based/code-based-implementation-samples.md) para cada abordagem.

1. **Definir superfícies**: identifique os locais no aplicativo em que deseja fornecer conteúdo personalizado. Saiba mais sobre a [configuração da superfície](../../code-based/code-based-surface.md).

1. **Implementar renderização de conteúdo**: use o SDK da web para buscar e aplicar conteúdo de personalização. Consulte [tutoriais de implementação baseados em código](../../code-based/code-based-decisioning-implementations.md).

1. **Enviar eventos de exibição e interação**: controle quando o conteúdo é exibido e quando os usuários interagem com ele para fins de análise e otimização.

Explore [implementações de exemplo no GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para ver as experiências baseadas em código em ação.

Saiba mais sobre a [introdução a experiências baseadas em código](../../code-based/get-started-code-based.md).

## Implementar a transmissão de eventos {#event-streaming}

### Enviar eventos para acionar jornadas

Como desenvolvedor(a), você implementará o código para enviar eventos que acionam jornadas. O [Engenheiro de dados](data-engineer.md) configurará os esquemas e as definições de eventos no Journey Optimizer.

1. **Entender o conteúdo do evento**: trabalhe com o Engenheiro de dados para obter o esquema do evento e a estrutura de conteúdo necessária. O conteúdo deve estar em conformidade com o esquema XDM configurado. Saiba mais sobre os [requisitos do esquema de evento](../../event/experience-event-schema.md).

1. **Implementar a transmissão de eventos**: envie eventos para a Adobe Experience Platform usando as [APIs de ingestão de transmissão](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=pt-BR){target="_blank"}. Saiba mais sobre as [etapas para enviar eventos](../../event/additional-steps-to-send-events-to-journey.md).

1. **Tipos de evento de processamento**:
   * **Eventos unitários**: implementam o envio de eventos para ações específicas de pessoas (por exemplo: clique de botão, conclusão de compra)
   * **Eventos de negócios**: enviar eventos relacionados a negócios (por exemplo: atualizações de estoque, alterações de preço)

1. **Entrega de evento de teste**: verifica se os eventos são recebidos corretamente e acionam as jornadas conforme o esperado. Saiba mais sobre a [solução de problemas de eventos](../../building-journeys/troubleshooting-inbound.md).

**Exemplo de implementação** para enviar um evento via API:

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

Saiba mais sobre como [trabalhar com eventos de jornada](../../event/about-events.md).

## Desenvolver pontos de acesso de ações personalizadas {#custom-actions}

As ações personalizadas permitem que as jornadas chamem as APIs. Como desenvolvedor(a), você criará os pontos de acesso da API invocados pelas ações personalizadas:

1. **Criar ponto de acesso de API**: crie pontos de acesso da API RESTful que o Journey Optimizer chamará durante a execução da jornada. Seu ponto de acesso deve:
   * Aceitar conteúdos JSON
   * Autenticar solicitações (OAuth, chave de API ou JWT)
   * Processar solicitações dentro dos limites de tempo apropriados
   * Retornar respostas no formato esperado

1. **Entenda os recursos das ações personalizadas**: as ações personalizadas podem se conectar a sistemas de terceiros, como Epsilon, Slack, Firebase ou os seus próprios serviços. Saiba mais sobre [ações personalizadas](../../action/action.md).

1. **Trabalhar com configurações de ação**: o [Admin](administrator.md) ou o [Engenheiro de dados](data-engineer.md) configurará a ação personalizada no Journey Optimizer, definindo a URL do ponto de acesso da API, o método de autenticação e os parâmetros. Você fornecerá a eles a especificação da API. Saiba mais sobre a [configuração da ação personalizada](../../action/about-custom-action-configuration.md).

1. **Retornar dados acionáveis**: crie a API para retornar dados que possam ser usados nas etapas seguintes da jornada. Saiba mais sobre as [respostas de ação](../../action/action-response.md).

1. **Implementar a limitação de taxa**: certifique-se de que os pontos de acesso possam lidar com o volume esperado. O Journey Optimizer aplica um limite de 5000 chamadas/segundo, mas o sistema deve ser resiliente. Saiba mais sobre [limitação e controle](../../configuration/external-systems.md).

**Caso de uso de exemplo**: [gravação de eventos da jornada na Experience Platform](../../building-journeys/custom-action-aep.md) usando ações personalizadas.

## Trabalhar com APIs do Journey Optimizer {#apis}

O Journey Optimizer fornece APIs REST abrangentes para acesso programático:

1. **Entender os recursos da API**: as APIs do Journey Optimizer permitem criar, ler, atualizar e excluir vários recursos de forma programática. Saiba mais sobre as [APIs do Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticação**: siga [este tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para configurar a autenticação de API com o Adobe Developer Console.

1. **Explorar referências de API**: navegue pela documentação completa da API e experimente APIs diretamente na [Referência da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campanhas acionadas por API**: crie mensagens transacionais com campanhas acionadas por API. Para cenários com alto volume (até 5000 TPS), explore o [modo de Alta taxa de transferência](../../campaigns/api-triggered-high-throughput.md) (requer licença complementar).

1. **APIs de Gestão de decisões**: use APIs especializadas para gerenciamento de ofertas e decisioning. Saiba mais no [Guia da API de Gestão de Decisões](../../offers/api-reference/getting-started.md).

## Teste e depuração {#testing}

1. **Depurar implementação do SDK**: use o Adobe Experience Platform Assurance para inspecionar eventos do SDK, validar a coleta de dados e solucionar problemas de integração em tempo real. [Saiba mais sobre o Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=pt-BR){target="_blank"}.

1. **Entrega de evento de teste**: verifica se os eventos do aplicativo são recebidos corretamente pela Adobe Experience Platform e acionam jornadas conforme o esperado. Monitore a ingestão de eventos e valide a estrutura do conteúdo.

1. **Validar integrações de API**: teste os pontos de acesso de ações personalizadas para garantir que eles processem corretamente as solicitações do Journey Optimizer, respondam dentro dos limites de tempo e retornem formatos de dados esperados.

1. **Usar o modo de teste com perfis de teste**: trabalhe com o [Engenheiro de dados](data-engineer.md) para obter acesso aos perfis de teste e validar a implementação com o modo de teste de jornada. Saiba como [testar jornadas](../../building-journeys/testing-the-journey.md).

1. **Monitorar logs do SDK**: habilite os logs de depuração na implementação do SDK para solucionar problemas durante o desenvolvimento:
   * **SDK para dispositivos móveis**: habilite logs para ver eventos do SDK e chamadas de API
   * **SDK da web**: use o console do navegador para monitorar a atividade do SDK

1. **Verificar configuração da sequência de dados**: verifique se a sequência de dados está configurada corretamente para enviar dados ao Journey Optimizer. Verifique se os eventos fluem pela sequência de dados para os destinos corretos.

1. **Consultar dados da jornada para análise**: use consultas SQL no data lake para analisar eventos de etapa da jornada, depurar problemas e monitorar o desempenho da ação personalizada. Explore [exemplos de consulta para análise da jornada](../../reports/query-examples.md) incluindo:
   * Rastreamento de entrada/saída de perfil e motivos de descarte
   * Métricas de desempenho de ação personalizada (latência, taxa de transferência, erros)
   * Entrega de eventos e padrões de erro
   * Estados da instância da jornada

## Tópicos avançados do desenvolvedor {#advanced-topics}

### Trabalho com dados contextuais e enriquecimento

* **Iterar em matrizes**: use a sintaxe de manipuladores para exibir listas dinâmicas de eventos, respostas da ação personalizada e pesquisas de conjuntos de dados em mensagens. Saiba mais sobre a [iteração de dados contextuais](../../personalization/iterate-contextual-data.md).
* **Pesquisa de conjunto de dados**: implemente pesquisas de conjunto de dados para enriquecer os dados da jornada a partir de conjuntos de dados da Adobe Experience Platform. Trabalhe com o(a) engenheiro(a) de dados na configuração. Saiba mais sobre [pesquisa de conjunto de dados](../../building-journeys/dataset-lookup.md).

### Trabalhar com consentimento e governança

Implemente políticas de consentimento e governança de dados nas integrações:

* **Governança de dados**: aplica políticas de uso de dados a ações personalizadas. Saiba mais sobre a [governança de dados](../../action/action-privacy.md).
* **Gerenciamento de consentimento**: lida com as preferências de consentimento do cliente nas implementações. Saiba mais sobre [consentimento](../../action/consent.md).

### Otimização e práticas recomendadas

* **Limite e controle**: entenda os limites de taxa e implemente o controle apropriado. Saiba mais sobre [sistemas externos](../../configuration/external-systems.md).
* **Otimização de jornada**: siga as práticas recomendadas para a [otimização de jornada](../../building-journeys/optimize.md).
* **Gerenciamento de erros**: implemente um gerenciamento de erros robusto. Revise [códigos de erro](../../building-journeys/error-codes-reference.md) e [guias de solução de problemas](../../building-journeys/troubleshooting.md).

## Recursos adicionais {#additional-resources}

* **Developer Console**: acesse o [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para criar integrações e gerenciar credenciais de API.
* **Código de exemplo**: explore [implementações de exemplo no GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Vídeos tutoriais**: aprenda com tutoriais práticos na [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=pt-BR){target="_blank"}.
* **Comunidade de desenvolvedores**: conecte-se com outros desenvolvedores e obtenha suporte nos fóruns da comunidade da Adobe.

## Colaborar entre funções {#next-steps}

O trabalho de implementação cruza com o trabalho de outros membros da equipe:

>[!BEGINTABS]

>[!TAB Trabalhar com Engenheiros de dados]

Colabore com [Engenheiros de dados](data-engineer.md) em configurações de dados e eventos:

* Obter os esquemas XDM e as estruturas de evento necessárias para implementar
* Entenda quais eventos você precisa enviar e o formato de conteúdo necessário
* Alinhe os requisitos de coleta de dados e os padrões de qualidade dos dados
* Teste a entrega de eventos e a ingestão de dados em conjunto

>[!TAB Trabalhar com admins]

Colabore com os [Admins](administrator.md) no acesso e nas configurações:

* Forneça especificações de API para ações personalizadas que serão configuradas
* Solicite as permissões necessárias e as credenciais de API
* Coordene os requisitos de configuração de canais (por exemplo: certificados de push)
* Alinhe os ambientes de teste e a estratégia de sandbox

>[!TAB Trabalhar com profissionais de marketing]

Colabore com os [Profissionais de marketing](marketer.md) nos requisitos e testes da jornada:

* Entenda quais interações do usuário devem acionar eventos
* Implemente o rastreamento para o desempenho do conteúdo e o engajamento do usuário
* Dê suporte a testes de jornadas com os recursos implementados
* Solucione problemas com a entrega ou personalização de mensagens

>[!ENDTABS]

## Comece a implementar

Pronto(a) para começar a criar? Escolha a primeira área de implementação nas seções acima:

1. **Aplicativo móvel?** Iniciar com a [Integração do SDK para dispositivos móveis](#mobile-integration)
2. **Site?** Começar com a [configuração do SDK da web](#web-implementation)
3. **Integração da API?** Ir para [Trabalho com APIs](#apis)
4. **Sistema personalizado?** Confira as [Ações personalizadas](#custom-actions)

Cada seção inclui links para a documentação técnica detalhada, amostras de código e tutoriais para orientar a implementação.
