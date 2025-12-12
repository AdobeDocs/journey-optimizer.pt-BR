---
title: Introdução para desenvolvedores
description: Como desenvolvedor(a), saiba mais sobre como trabalhar com o Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1891'
ht-degree: 2%

---

# Introdução para desenvolvedores {#get-started-developers}

Como **Desenvolvedor**, você é responsável pela implementação e integração do [!DNL Adobe Journey Optimizer] em seus aplicativos e sistemas. Você pode começar a trabalhar com [!DNL Adobe Journey Optimizer] assim que o [Administrador do Sistema](administrator.md) e o [Engenheiro de Dados](data-engineer.md) concederem acesso e prepararem seu ambiente.

## Sua função no ecossistema do Journey Optimizer

Enquanto outros membros da equipe configuram o Journey Optimizer por meio da interface do usuário, você se concentrará em:

* **Implementando SDKs** em aplicativos para dispositivos móveis e Web
* **Enviando eventos** de seus aplicativos para acionar jornadas
* **Criando pontos de extremidade de API** que o Journey Optimizer pode chamar por meio de ações personalizadas
* **Integrando** o Journey Optimizer aos seus sistemas e infraestrutura existentes
* **Testando e depurando** suas implementações

O [Engenheiro de Dados](data-engineer.md) manipulará esquemas de dados, configurações de eventos e fontes de dados. O [Administrador](administrator.md) definirá as permissões e as configurações de canal. [Os profissionais de marketing](marketer.md) criarão as jornadas e o conteúdo que usam suas implementações.

Este guia aborda as etapas essenciais de implementação técnica para ajudar você a começar a usar o Journey Optimizer. Se você estiver criando aplicativos para dispositivos móveis, experiências da Web ou integrações de API, siga as seções abaixo para configurar sua implementação.

## Pré-requisitos {#prerequisites}

Antes de iniciar a implementação, verifique se você tem:

**Habilidades técnicas:**

* Experiência com o JavaScript (para Web SDK) ou Swift/Kotlin (para SDK móvel)
* Noções básicas sobre RESTful APIs e JSON
* Familiaridade com programação assíncrona e arquiteturas orientadas por eventos
* Conhecimento da arquitetura de aplicativos de sua organização

**Acesso e ferramentas:**

* Acesso ao [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para credenciais de API
* Ambiente de desenvolvimento com acesso à base de código do seu aplicativo
* Ferramentas de teste como o Postman para teste de API
* Ferramentas de desenvolvedor do navegador ou ferramentas de depuração móvel

**De outros membros da equipe:**

* Acesso ao ambiente concedido pelo seu [Administrador](administrator.md)
* Esquemas XDM e definições de evento do seu [Engenheiro de dados](data-engineer.md)
* Requisitos e casos de uso de seus [Profissionais de marketing](marketer.md)

## Entender a base técnica {#technical-foundation}

Antes de mergulhar na implementação, familiarize-se com os conceitos técnicos principais:

1. **Integração do Adobe Experience Platform**: o Journey Optimizer foi criado nativamente no Adobe Experience Platform. Compreender a arquitetura subjacente ajudará você a criar implementações mais eficazes. Saiba mais sobre [como o Journey Optimizer funciona](../understanding-ajo.md).

1. **Modelos de dados XDM**: o Journey Optimizer usa o Experience Data Model (XDM) para estruturar dados de evento e perfil. Como desenvolvedor, você precisará entender como enviar dados que estejam em conformidade com os esquemas configurados pelo seu [Engenheiro de dados](data-engineer.md). Saiba mais sobre [esquemas XDM](../../data/get-started-schemas.md).

1. **Autenticação e segurança**: todas as implementações exigem autenticação adequada. Entenda como configurar a autenticação para SDKs e APIs. Saiba mais sobre [Autenticação de API](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Configurar integrações do aplicativo móvel {#mobile-integration}

### Configurar o Adobe Experience Platform Mobile SDK

Para ativar notificações por push, mensagens no aplicativo e outros recursos móveis, integre o Adobe Experience Platform Mobile SDK em seus aplicativos móveis.

1. **Instalar e configurar o Mobile SDK**: siga a [documentação do Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"} para começar a integração com o SDK.

1. **Criar uma propriedade móvel**: configure uma propriedade móvel em [!DNL Adobe Experience Platform Data Collection]. Saiba como [criar e configurar uma propriedade móvel](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}.

1. **Configurar notificações por push**:
   * Para **aplicativos iOS**: registre seu aplicativo com APNs (serviço de notificação por push da Apple). Saiba mais na [documentação da Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Para **aplicativos Android**: configure o Firebase Cloud Messaging para seu aplicativo Android. Saiba mais na [documentação da Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testar a integração móvel**: use o [fluxo de trabalho de início rápido da integração móvel](../../push/mobile-onboarding-wf.md) para configurar e testar rapidamente a configuração móvel.

As etapas detalhadas para configurar notificações por push estão disponíveis em [esta página](../../push/push-configuration.md).

### Implementar experiências baseadas em código (Mobile SDK)

Para personalização nativa de aplicativos móveis usando experiências baseadas em código:

* Siga [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} para implementação do Mobile SDK
* Examine as implementações de exemplo do [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} e do [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementar experiências da Web {#web-implementation}

### Configurar o Adobe Experience Platform Web SDK

Para implementações baseadas na Web, o Web SDK é o seu principal ponto de integração:

1. **Instalar o Web SDK**: siga o [guia de implementação do Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} para configurar o SDK no seu site.

1. **Configurar sequências de dados**: crie e configure uma sequência de dados em [!DNL Adobe Experience Platform Data Collection] com o Journey Optimizer habilitado. Saiba mais na [documentação de sequências de dados](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}.

1. **Habilitar notificações por push da Web** (opcional): configure a [propriedade pushNotifications](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"} na configuração do Web SDK e use o [comando sendPushSubscription](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"} para registrar assinaturas por push.

### Implementar experiências baseadas em código (Web SDK)

Experiências baseadas em código permitem personalizar qualquer ponto de contato digital:

1. **Escolha seu método de implementação**: cliente, servidor ou híbrido. Revise [amostras de implementação](../../code-based/code-based-implementation-samples.md) para cada abordagem.

1. **Definir superfícies**: identifique os locais em seu aplicativo onde você deseja fornecer conteúdo personalizado. Saiba mais sobre a [configuração da superfície](../../code-based/code-based-surface.md).

1. **Implementar renderização de conteúdo**: use o Web SDK para buscar e aplicar conteúdo de personalização. Consulte [tutoriais de implementação baseados em código](../../code-based/code-based-decisioning-implementations.md).

1. **Enviar eventos de exibição e interação**: controle quando o conteúdo é exibido e quando os usuários interagem com ele para fins de análise e otimização.

Explore [implementações de amostra no GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para ver as experiências de código em ação.

Saiba mais sobre a [introdução a experiências baseadas em código](../../code-based/get-started-code-based.md).

## Implementar a transmissão de eventos {#event-streaming}

### Enviar eventos para acionar jornadas

Como desenvolvedor, você implementará o código para enviar eventos que acionam jornadas. O [Engenheiro de dados](data-engineer.md) configurará os esquemas e as definições de eventos no Journey Optimizer.

1. **Entender a carga do evento**: trabalhe com seu Engenheiro de Dados para obter o esquema do evento e a estrutura de carga necessária. A carga deve estar em conformidade com o esquema XDM configurado. Saiba mais sobre [requisitos de esquema de evento](../../event/experience-event-schema.md).

1. **Implementar a transmissão de eventos**: envie eventos para a Adobe Experience Platform usando as [APIs de assimilação de transmissão](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=pt-BR){target="_blank"}. Saiba mais sobre as [etapas para enviar eventos](../../event/additional-steps-to-send-events-to-journey.md).

1. **Manipular tipos de evento**:
   * **Eventos unitários**: implementam o envio de eventos para ações específicas de pessoas (por exemplo, clique de botão, conclusão de compra)
   * **Eventos comerciais**: enviar eventos comerciais (por exemplo, atualizações de estoque, alterações de preço)

1. **Entrega de evento de teste**: verifique se os eventos foram recebidos corretamente e acione jornadas conforme esperado. Saiba mais sobre a [solução de problemas do evento](../../building-journeys/troubleshooting-inbound.md).

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

Saiba mais sobre [como trabalhar com eventos do jornada](../../event/about-events.md).

## Desenvolver endpoints de ação personalizados {#custom-actions}

As ações personalizadas permitem que o jornada chame suas APIs. Como desenvolvedor, você criará os endpoints de API invocados pelas ações personalizadas:

1. **Criar seu ponto de extremidade de API**: crie pontos de extremidade de API RESTful que o Journey Optimizer chamará durante a execução da jornada. Seu terminal deve:
   * Aceitar cargas JSON
   * Autenticar solicitações (OAuth, chave de API ou JWT)
   * Processar solicitações dentro de limites de tempo apropriados
   * Retornar respostas no formato esperado

1. **Entenda os recursos de ação personalizados**: as ações personalizadas podem se conectar a sistemas de terceiros, como Epsilon, Slack, Firebase ou seus próprios serviços. Saiba mais sobre [Ações personalizadas](../../action/action.md).

1. **Trabalhar com configurações de ação**: o [Administrador](administrator.md) ou o [Engenheiro de Dados](data-engineer.md) configurará a ação personalizada no Journey Optimizer, definindo a URL do ponto de extremidade de API, o método de autenticação e os parâmetros. Você fornecerá a eles a especificação da API. Saiba mais sobre a [configuração de ação personalizada](../../action/about-custom-action-configuration.md).

1. **Retornar dados acionáveis**: crie sua API para retornar dados que possam ser usados nas etapas de jornada subsequentes. Saiba mais sobre [respostas de ação](../../action/action-response.md).

1. **Implemente a limitação de taxa**: certifique-se de que seus pontos de extremidade possam manipular o volume esperado. O Journey Optimizer aplica um limite de 5000 chamadas/segundo, mas o sistema deve ser resiliente. Saiba mais sobre [limitação e limitação](../../configuration/external-systems.md).

**Exemplo de caso de uso**: [Gravando eventos de jornada no Experience Platform](../../building-journeys/custom-action-aep.md) usando ações personalizadas.

## Trabalhar com APIs do Journey Optimizer {#apis}

O Journey Optimizer fornece APIs REST abrangentes para acesso programático:

1. **Entender os recursos da API**: as APIs do Journey Optimizer permitem criar, ler, atualizar e excluir vários recursos de forma programática. Saiba mais sobre [APIs do Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticação**: siga [este tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} para configurar a autenticação de API usando o Adobe Developer Console.

1. **Explorar referências de API**: procure a documentação completa da API e tente APIs diretamente na [Referência da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

1. **Campanhas acionadas por API**: crie mensagens transacionais com campanhas acionadas por API. Para cenários de alto volume (até 5000 TPS), explore o [modo Alta Taxa de Transferência](../../campaigns/api-triggered-high-throughput.md) (requer licença complementar).

1. **APIs de Gerenciamento de Decisão**: use APIs especializadas para gerenciamento de ofertas e decisões. Saiba mais no [Guia da API de Gestão de Decisões](../../offers/api-reference/getting-started.md).

## Teste e depuração {#testing}

1. **Depurar implementação do SDK**: use o Adobe Experience Platform Assurance para inspecionar eventos do SDK, validar a coleta de dados e solucionar problemas de integração em tempo real. [Saiba mais sobre o Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=pt-BR){target="_blank"}.

1. **Entrega de evento de teste**: verifique se os eventos do seu aplicativo são recebidos corretamente pela Adobe Experience Platform e acione jornadas conforme esperado. Monitore a assimilação de eventos e valide a estrutura de carga.

1. **Validar integrações de API**: teste seus pontos de extremidade de ação personalizados para garantir que eles lidem corretamente com as solicitações do Journey Optimizer, respondam dentro dos limites de tempo e retornem os formatos de dados esperados.

1. **Usar o modo de teste com perfis de teste**: trabalhe com seu [Engenheiro de dados](data-engineer.md) para obter acesso aos perfis de teste e, em seguida, validar sua implementação usando o modo de teste de jornada. Saiba como [testar jornadas](../../building-journeys/testing-the-journey.md).

1. **Monitorar logs do SDK**: habilite o log de depuração na implementação do SDK para solucionar problemas durante o desenvolvimento:
   * **SDK Móvel**: habilitar o log para ver eventos SDK e chamadas de API
   * **Web SDK**: use o console do navegador para monitorar a atividade do SDK

1. **Verificar configuração da sequência de dados**: verifique se a sequência de dados está configurada corretamente para enviar dados à Journey Optimizer. Verifique se os eventos fluem pelo fluxo de dados para os destinos corretos.

1. **Consultar dados de jornada para análise**: use consultas SQL no Data Lake para analisar eventos de etapa de jornada, depurar problemas e monitorar o desempenho da ação personalizada. Explore [exemplos de consulta para análise de jornada](../../reports/query-examples.md) incluindo:
   * Motivos de rastreamento de entrada/saída de perfil e descarte
   * Métricas de desempenho de ação personalizada (latência, taxa de transferência, erros)
   * Entrega de eventos e padrões de erro
   * Jornada estados de instância

## Tópicos avançados do desenvolvedor {#advanced-topics}

### Trabalho com dados contextuais e enriquecimento

* **Iterar em matrizes**: use a sintaxe Handlebars para exibir listas dinâmicas de eventos, respostas de ação personalizadas e pesquisas de conjuntos de dados em mensagens. Saiba mais sobre [iteração de dados contextuais](../../personalization/iterate-contextual-data.md).
* **Pesquisa de conjunto de dados**: implemente pesquisas de conjunto de dados para enriquecer dados de jornada de conjuntos de dados do Adobe Experience Platform. Trabalhe com seu engenheiro de dados na configuração do. Saiba mais sobre [pesquisa de conjunto de dados](../../building-journeys/dataset-lookup.md).

### Trabalhar com consentimento e governança

Implemente políticas de consentimento e governança de dados em suas integrações:

* **Governança de dados**: aplique políticas de uso de dados a ações personalizadas. Saiba mais sobre [governança de dados](../../action/action-privacy.md).
* **Gerenciamento de consentimento**: lida com as preferências de consentimento do cliente em suas implementações. Saiba mais sobre [consentimento](../../action/consent.md).

### Otimização e práticas recomendadas

* **Limite e limitação**: entenda os limites de taxa e implemente a limitação apropriada. Saiba mais sobre [sistemas externos](../../configuration/external-systems.md).
* **Otimização de Jornada**: siga as práticas recomendadas para [Otimização de jornada](../../building-journeys/optimize.md).
* **Manipulação de erros**: implemente uma manipulação de erros robusta. Revise [códigos de erro](../../building-journeys/error-codes-reference.md) e [guias de solução de problemas](../../building-journeys/troubleshooting.md).

## Recursos adicionais {#additional-resources}

* **Developer Console**: acesse o [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para criar integrações e gerenciar credenciais de API.
* **Código de exemplo**: Explore [implementações de exemplo no GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Vídeos tutoriais**: Aprenda com tutoriais práticos no [Experience League](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}.
* **Comunidade de desenvolvedores**: conecte-se com outros desenvolvedores e obtenha suporte nos fóruns da comunidade do Adobe.

## Colaborar entre funções {#next-steps}

Seu trabalho de implementação cruza com outros membros da equipe:

**Trabalhar com [Engenheiros de Dados](data-engineer.md):**

* Obter os esquemas XDM e as estruturas de evento necessárias para implementar
* Entenda quais eventos você precisa enviar e o formato de carga necessário
* Alinhe os requisitos de coleta de dados e os padrões de qualidade dos dados
* Teste a entrega de eventos e a assimilação de dados juntas

**Trabalhar com [Administradores](administrator.md):**

* Fornecer especificações de API para ações personalizadas que serão configuradas
* Solicite as permissões necessárias e as credenciais da API
* Coordenar os requisitos de configuração de canal (por exemplo, certificados de push)
* Alinhar ambientes de teste e estratégia de sandbox

**Trabalhar com [Profissionais de marketing](marketer.md):**

* Entender quais interações de usuário devem acionar eventos
* Implementar o rastreamento para desempenho do conteúdo e envolvimento do usuário
* Suporte a testes de jornadas com os recursos implementados
* Solucionar problemas com entrega de mensagens ou personalização

## Permanecer atualizado

Acompanhe os recursos e as alterações técnicas mais recentes do Journey Optimizer:

* **[Notas de versão](../../rn/release-notes.md)**: Revise novos recursos, alterações de API, atualizações de SDK e correções de erros lançadas a cada mês
* **[Atualizações da documentação](../../rn/documentation-updates.md)**: controle alterações recentes na documentação técnica, incluindo novos guias de implementação e exemplos de código
* **Notificações do Produto**: Habilite as notificações no seu [perfil do Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} para receber alertas sobre:
   * Novas versões do SDK e atualizações da API
   * Quebra de alterações e descontinuações
   * Janelas de manutenção que afetam integrações
   * Atualizações críticas de segurança

  Para habilitar notificações, clique no ícone de perfil na parte superior direita do Adobe Experience Cloud, vá para **Preferências > Notificações** e configure suas preferências de notificação do Journey Optimizer.

## Começar a implementar o

Pronto para começar a criar? Escolha sua primeira área de implementação nas seções acima:

1. **Aplicativo móvel?** Iniciar com [Integração com o Mobile SDK](#mobile-integration)
2. **Site?** Iniciar com [configuração do Web SDK](#web-implementation)
3. **Integração de API?** Ir para [Trabalho com APIs](#apis)
4. **Sistema personalizado?** Confira [Ações personalizadas](#custom-actions)

Cada seção inclui links para documentação técnica detalhada, amostras de código e tutoriais para orientar sua implementação do.
