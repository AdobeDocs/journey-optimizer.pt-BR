---
title: Introdução para desenvolvedores
description: Como desenvolvedor(a), saiba mais sobre como trabalhar com o Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2fid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: e9001ce2-5245-4a8e-8601-dd958009072fid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: cf815079d67f4a41c3647c6a6e381ef5f1c44e51
workflow-type: tm+mt
source-wordcount: 3490
ht-degree: 53%

---

# Introdução para desenvolvedores {#get-started-developers}

>[!BEGINSHADEBOX]

**Nesta página:** Implemente os SDKs, a transmissão de eventos, os pontos de extremidade de ação personalizados e as APIs que conectam seus aplicativos à Adobe Journey Optimizer para que suas jornadas possam ser executadas em dados dinâmicos.

>[!ENDSHADEBOX]

Como **desenvolvedor(a)**, você é responsável pela implementação e integração do [!DNL Adobe Journey Optimizer] nos aplicativos e sistemas. É possível começar a trabalhar com o [!DNL Adobe Journey Optimizer] assim que o(a) [admin de sistema](administrator.md) e o(a) [engenheiro(a) de dados](data-engineer.md) concederem acesso e prepararem o ambiente.

>[!NOTE]
>
>**Ordem de implementação:** [Administrador](administrator.md) → [Engenheiro de dados](data-engineer.md) → Você está aqui: **Desenvolvedor** → [Profissional de marketing](marketer.md)
>
>Verifique se [esquemas de dados e eventos](data-engineer.md) estão configurados antes de implementar suas integrações móveis e da Web.

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

1. **Autenticação e segurança**: todas as implementações exigem autenticação adequada. Entenda como configurar a autenticação para SDKs e APIs. Saiba mais sobre [Autenticação de API](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Configurar integrações de aplicativos para dispositivos móveis {#mobile-integration}

### Configurar o SDK para dispositivos móveis da Adobe Experience Platform

O Mobile SDK é uma coleção de bibliotecas incorporadas diretamente no seu aplicativo iOS ou Android. Ele age como a camada de comunicação entre o aplicativo e o Adobe Experience Platform: identifica usuários, coleta eventos comportamentais e fornece instruções do Journey Optimizer, incluindo notificações por push, mensagens no aplicativo e conteúdo personalizado. Sem ele, o Journey Optimizer não tem visibilidade do que os usuários do aplicativo estão fazendo nem como acessá-los.

1. **Instalar e configurar o SDK para dispositivos móveis**: siga a [documentação do SDK para dispositivos móveis da Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"} para ver uma introdução à integração do SDK.

1. **Criar uma propriedade móvel**: configure uma propriedade móvel na [!DNL Adobe Experience Platform Data Collection]. Saiba como [criar e configurar uma propriedade móvel](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}.

1. **Configurar notificações por push**:
   * Para **aplicativos iOS**: registre o aplicativo com APNs (serviço de notificação por push da Apple). Saiba mais na [documentação da Apple](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}.
   * Para **aplicativos Android**: configure o Firebase Cloud Messaging para seu aplicativo Android. Saiba mais na [documentação do Google](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}.

1. **Testar a integração móvel**: use o [fluxo de trabalho de início rápido da integração para dispositivos móveis](../../push/mobile-onboarding-wf.md) para definir e testar rapidamente a configuração para dispositivos móveis.

As etapas detalhadas para configurar notificações por push estão disponíveis [nesta página](../../push/push-configuration.md).

### Implementar experiências baseadas em código (SDK para dispositivos móveis)

Experiências baseadas em código permitem fornecer conteúdo personalizado a qualquer superfície em seu aplicativo móvel nativo, desde telas de integração e páginas de detalhes do produto até banners no aplicativo e sinalizadores de recursos, sem exigir uma nova versão do aplicativo. Use o Mobile SDK para buscar e renderizar conteúdo personalizado no tempo de execução, dando à sua equipe controle total sobre a disposição e a apresentação:

* Siga [este tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"} para a implementação do SDK para dispositivos móveis
* Revise as implementações de exemplo do [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} e do [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}

## Implementar experiências da web {#web-implementation}

### Configurar o SDK da web da Adobe Experience Platform

O Web SDK (`alloy.js`) é uma única biblioteca JavaScript que substitui a manta de retalhos de tags Adobe separadas que o site poderia precisar. Ele coleta dados comportamentais, transmite-os para o Adobe Experience Platform por meio de uma sequência de dados configurada por você e recebe instruções de personalização de volta — tudo isso em uma rede de ida e volta. Uma vez implementado, o Journey Optimizer pode identificar visitantes, acionar jornadas de suas ações e fornecer conteúdo personalizado para suas páginas imediatamente.

1. **Instalar o SDK da web**: siga o [guia de implementação do SDK da web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=pt-BR){target="_blank"} para configurar o SDK no site.

1. **Configurar sequências de dados**: crie e configure uma sequência de dados na [!DNL Adobe Experience Platform Data Collection] com o Journey Optimizer habilitado. Saiba mais na [documentação das sequências de dados](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=pt-BR){target="_blank"}.

1. **Habilitar notificações por push da Web** (opcional): as notificações por push da Web agora estão disponíveis. Configure a [propriedade pushNotifications](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/pushnotifications){target="_blank"} na configuração do SDK da Web e use o [comando sendPushSubscription](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/sendpushsubscription){target="_blank"} para registrar assinaturas por push. [Saiba mais sobre a configuração de push da Web](../../push/push-configuration-web.md).

### Implementar experiências baseadas em código (SDK da web)

Diferentemente dos canais visuais, em que os profissionais de marketing controlam totalmente o layout, as experiências baseadas em código fornecem total propriedade sobre como o conteúdo personalizado é renderizado na página. O Journey Optimizer retorna uma carga JSON com os dados de personalização; seu código decide onde e como exibi-la. Esse modelo funciona para qualquer superfície da Web — banners ilustrados, carrosséis de recomendação, classificações de resultados de pesquisa, variantes de teste A/B — sem precisar de um editor visual ou fluxo de trabalho de publicação de página.

1. **Escolha o método de implementação**: lado do cliente, lado do servidor ou híbrido. Revise os [exemplos de implementação](../../code-based/code-based-implementation-samples.md) para cada abordagem.

1. **Definir superfícies**: identifique os locais no aplicativo em que deseja fornecer conteúdo personalizado. Saiba mais sobre a [configuração da superfície](../../code-based/code-based-surface.md).

1. **Implementar renderização de conteúdo**: use o SDK da web para buscar e aplicar conteúdo de personalização. Consulte [tutoriais de implementação baseados em código](../../code-based/code-based-decisioning-implementations.md).

1. **Enviar eventos de exibição e interação**: controle quando o conteúdo é exibido e quando os usuários interagem com ele para fins de análise e otimização.

Explore [implementações de exemplo no GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} para ver as experiências baseadas em código em ação.

Saiba mais sobre a [introdução a experiências baseadas em código](../../code-based/get-started-code-based.md).

## Implementar a transmissão de eventos {#event-streaming}

### Enviar eventos para acionar jornadas

Jornadas executadas em eventos — um usuário faz logon, adiciona um item ao carrinho, conclui uma compra, abandona um formulário. Seu trabalho é emitir esses eventos do seu aplicativo no momento exato. Cada evento é uma carga JSON estruturada em XDM enviada para a API de assimilação de streaming do Experience Platform; o Journey Optimizer a seleciona em milissegundos e direciona o perfil para qualquer jornada correspondente. O esquema de evento e a estrutura de carga são definidos pelo seu [Engenheiro de Dados](data-engineer.md) — coordene com eles antes de começar a codificar.

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

Quando uma jornada atinge uma etapa de ação personalizada, o Journey Optimizer faz uma chamada HTTP de saída para um URL que você fornece — seu back-end, um CRM, uma plataforma de fidelidade, qualquer endpoint REST. Seu trabalho é criar e expor esse endpoint: definir o contrato de solicitação (forma de carga, método de autenticação, formato de resposta), implementar a lógica de negócios por trás dele e garantir que ele possa lidar com o volume de chamadas gerado pelo Journey Optimizer. O [Administrador](administrator.md) registra o ponto de extremidade no Journey Optimizer para que os profissionais de marketing possam usá-lo como uma etapa em suas jornadas.

1. **Criar ponto de acesso de API**: crie pontos de acesso da API RESTful que o Journey Optimizer chamará durante a execução da jornada. Seu ponto de acesso deve:
   * Aceitar conteúdos JSON
   * Autenticar solicitações (OAuth, chave de API ou JWT)
   * Processar solicitações dentro dos limites de tempo apropriados
   * Retornar respostas no formato esperado

1. **Entenda os recursos das ações personalizadas**: as ações personalizadas podem se conectar a sistemas de terceiros, como Epsilon, Slack, Firebase ou os seus próprios serviços. Saiba mais sobre [ações personalizadas](../../action/action.md).

1. **Trabalhar com configurações de ação**: o [Admin](administrator.md) ou o [Engenheiro de dados](data-engineer.md) configurará a ação personalizada no Journey Optimizer, definindo a URL do ponto de acesso da API, o método de autenticação e os parâmetros. Você fornecerá a eles a especificação da API. Saiba mais sobre a [configuração da ação personalizada](../../action/about-custom-action-configuration.md). Você pode definir um **conteúdo de resposta a erros** opcional para uma lógica de fallback mais avançada em ramificações de tempo limite/erro.

1. **Retornar dados acionáveis**: crie a API para retornar dados que possam ser usados nas etapas seguintes da jornada. Saiba mais sobre as [respostas de ação](../../action/action-response.md).

1. **Monitorar a integridade da ação personalizada**: use o painel de monitoramento da ação personalizada para rastrear chamadas bem-sucedidas, erros, taxa de transferência, tempos de resposta e tempos de espera em fila. Saiba mais sobre [relatórios de ações personalizadas](../../action/reporting.md).

1. **Implementar a limitação de taxa**: certifique-se de que os pontos de acesso possam lidar com o volume esperado. O Journey Optimizer aplica um limite de 5000 chamadas/segundo, mas o sistema deve ser resiliente. Saiba mais sobre [limitação e controle](../../configuration/external-systems.md).

**Caso de uso de exemplo**: [gravação de eventos da jornada na Experience Platform](../../building-journeys/custom-action-aep.md) usando ações personalizadas.

## Trabalhar com APIs do Journey Optimizer {#apis}

Nem tudo precisa acontecer por meio da interface do usuário do Journey Optimizer. Às vezes, você precisa acionar uma campanha do seu próprio back-end, suprimir um endereço de email após uma solicitação de privacidade ou sincronizar modelos de conteúdo de um CMS externo. As REST APIs do Journey Optimizer fornecem acesso programático aos principais recursos da plataforma. Todas as chamadas usam a autenticação de servidor para servidor OAuth — o método JWT mais antigo foi descontinuado.

1. **Entender os recursos da API**: as APIs do Journey Optimizer permitem criar, ler, atualizar e excluir vários recursos de forma programática. Saiba mais sobre as [APIs do Journey Optimizer](../../configuration/ajo-apis.md).

1. **Autenticação**: siga [este tutorial](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} para configurar a autenticação de API com o Adobe Developer Console.

1. **Explorar referências de API**: navegue pela documentação completa da API e experimente APIs diretamente na [Referência da API do Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

1. **Campanhas acionadas por API**: crie mensagens transacionais com campanhas acionadas por API. Para cenários com alto volume (até 5000 TPS), explore o [modo de Alta taxa de transferência](../../campaigns/api-triggered-high-throughput.md) (requer licença complementar).

1. **APIs de Gestão de decisões**: use APIs especializadas para gerenciamento de ofertas e decisioning. Saiba mais no [Guia da API de Gestão de Decisões](../../offers/api-reference/getting-started.md).

1. **APIs de migração de decisão**: migre programaticamente entidades de Gestão de decisões para a Decisão com escopos flexíveis, validação automatizada e suporte de reversão. Saiba mais no [Guia da API de migração de decisão](../../experience-decisioning/decisioning-migration-api.md).

1. **Webhooks de SMS**: configure webhooks de entrada para capturar mensagens de entrada e webhooks de feedback para receber confirmações de entrega e atualizações de status. [Saiba mais](../../mobile/mobile-webhook.md).

## Teste e depuração {#testing}

Antes da implementação entrar em vigor, você precisa ter certeza de que os eventos serão acionados no momento certo, as jornadas serão acionadas conforme esperado, as ações personalizadas se comportarão sob carga realista e o conteúdo personalizado será renderizado corretamente. Esta seção aborda as ferramentas e técnicas para capturar problemas antecipadamente — desde o registro de baixo nível do SDK até a execução completa de testes de jornada com perfis reais.

1. **Depurar implementação do SDK**: use o Adobe Experience Platform Assurance para inspecionar eventos do SDK, validar a coleta de dados e solucionar problemas de integração à medida que eles ocorrem. [Saiba mais sobre o Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=pt-BR){target="_blank"}.

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

Quando seus SDKs, eventos e APIs principais estiverem em vigor, esses tópicos ajudarão você a ir além: enriquecer dados do jornada no tempo de execução sem sobrecarregar o perfil, manipular sinais de consentimento para que as recusas se propaguem por todas as integrações e ajustar a implementação para a taxa de transferência e a confiabilidade que a escala de produção exige.

### Trabalho com dados contextuais e enriquecimento

As jornadas geralmente precisam de mais dados do que o que chega no evento de acionamento — um nome de produto, um nível de fidelidade, uma lista de itens de linha de pedido. Em vez de pré-carregar tudo isso em cada perfil, o enriquecimento contextual permite que a jornada o procure no tempo de execução dos conjuntos de dados do AEP ou o carregue a partir de uma resposta de ação personalizada. Suas mensagens e condições de ramificação podem fazer referência a esses dados sem que eles sejam armazenados permanentemente no perfil.

* **Iterar em matrizes**: use a sintaxe de manipuladores para exibir listas dinâmicas de eventos, respostas da ação personalizada e pesquisas de conjuntos de dados em mensagens. Saiba mais sobre a [iteração de dados contextuais](../../personalization/iterate-contextual-data.md).
* **Pesquisa de conjunto de dados**: implemente pesquisas de conjunto de dados para enriquecer os dados da jornada a partir de conjuntos de dados da Adobe Experience Platform. Trabalhe com o(a) engenheiro(a) de dados na configuração. Saiba mais sobre [pesquisa de conjunto de dados](../../building-journeys/dataset-lookup.md).

### Trabalhar com consentimento e governança

O Journey Optimizer aplica políticas de consentimento e governança de dados no nível da plataforma, mas a integração também precisa respeitá-las. Quando um cliente recusa comunicações de marketing ou quando um rótulo de uso de dados restringe como um campo pode ser usado, essas regras precisam se propagar por meio de ações personalizadas e pesquisas de conjunto de dados, não apenas ações de bloco na interface do usuário.

* **Governança de dados**: aplica políticas de uso de dados a ações personalizadas. Saiba mais sobre a [governança de dados](../../action/action-privacy.md).
* **Gerenciamento de consentimento**: lida com as preferências de consentimento do cliente nas implementações. Saiba mais sobre [consentimento](../../action/consent.md).

### Otimização e práticas recomendadas

As implementações de produção do Journey Optimizer lidam regularmente com milhões de eventos e milhares de execuções de jornadas por segundo. Esses recursos ajudam a ajustar a integração para essa escala: compreender limites de taxa antes de atingi-los, evitar armadilhas comuns do design de jornada que silenciosamente descartam perfis e criar um tratamento de erros que degrada normalmente em vez de falhar opaquamente.

* **Limite e controle**: entenda os limites de taxa e implemente o controle apropriado. Saiba mais sobre [sistemas externos](../../configuration/external-systems.md).
* **Otimização de jornada**: siga as práticas recomendadas para a [otimização de jornada](../../building-journeys/optimize.md).
* **Gerenciamento de erros**: implemente um gerenciamento de erros robusto. Revise [códigos de erro](../../building-journeys/error-codes-reference.md) e [guias de solução de problemas](../../building-journeys/troubleshooting.md).

## Chamar APIs REST do Journey Optimizer {#rest-apis}

Além de implementar SDKs e transmissão de eventos, você também pode impulsionar o Journey Optimizer de forma programática a partir de seus próprios sistemas. A referência completa da API, as especificações da OpenAPI e as amostras de código estão no [portal do desenvolvedor do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

>[!NOTE]
>
>Todas as integrações devem usar a autenticação de servidor para servidor do OAuth — o método JWT foi descontinuado. [Configurar autenticação](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### Executar campanhas acionadas por API {#api-triggered}

Acione mensagens transacionais ou de marketing de um sistema externo usando a API REST de execução de mensagem interativa. Antes de chamar o ponto de extremidade:

* A campanha deve ser **ativada** antes que o ponto de extremidade aceite chamadas.
* As chamadas têm um **tempo limite de 60 segundos**; as tentativas internas lidam com tempos limite inesperados.
* Se as datas de início/término da campanha forem configuradas, as chamadas da API fora dessas datas falharão.
* Para criar sua carga, recupere a solicitação de cURL de amostra gerada na seção **cURL request** da sua campanha em tempo real na interface do usuário do Journey Optimizer — ela inclui todas as variáveis de personalização dessa campanha.
* As [campanhas padrão e de alta taxa de transferência](../../campaigns/api-triggered-high-throughput.md) usam pontos de extremidade diferentes.

[Referência de API](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [Amostras de código](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [Trabalhar com campanhas acionadas por API](../../campaigns/api-triggered-campaigns.md)

### Limite e limitação para endpoints externos {#capping-throttling}

Quando o jornada chama sistemas externos por meio de ações personalizadas ou fontes de dados, as APIs de limitação e limitação protegem esses sistemas contra sobrecarga. O limite rejeita chamadas que excedem o limite configurado; a limitação as enfileira por até 6 horas (sandboxes de produção, somente ações personalizadas).

[Referência da API de Limite](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [Trabalhar com a API de Limite](../../configuration/capping.md) · [Trabalhar com a API de Limitação](../../configuration/throttling.md)

### Mais REST APIs {#more-rest-apis}

Além das mensagens e do limite, o Journey Optimizer expõe os endpoints REST para gerenciamento de supressão, modelos de conteúdo, recuperação de campanha, provas e execução de campanha orquestrada. Use-os quando precisar automatizar operações que, de outra forma, exigiriam etapas manuais na interface do usuário — por exemplo, suprimir endereços em massa após um pull de dados ou sincronizar modelos de um pipeline de conteúdo externo.

| O que você precisa fazer | Referência da API |
| ------------------- | ------------- |
| Excluir programaticamente endereços de email ou domínios do envio | [API de supressão](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [Gerenciar a lista de supressão](../../configuration/manage-suppression-list.md) |
| Recuperar metadados de jornada para auditoria ou sincronização externa | [API do Jornada](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| Criar e gerenciar modelos e fragmentos de conteúdo de um pipeline externo | [API de conteúdo](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [Modelos](../../content-management/content-templates.md) · [Fragmentos](../../content-management/fragments.md) |
| Recuperar e filtrar Campanhas de ação | [API de campanhas](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| Pré-visualizar campanhas e enviar provas de forma programática | [API de simulações](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |

>[!NOTE]
>
>A API de simulações está disponível para campanhas acionadas por API e de Ação (programadas). Não há suporte para **campanhas orquestradas**: em vez disso, use o fluxo de trabalho de visualização e prova na interface do usuário Campanhas orquestradas.

| Validar conjuntos de dados e acionar a execução de campanha orquestrada | [Validação do conjunto de dados](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [Acionador](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [Habilitar conjuntos de dados](../../orchestrated/manual-schema.md) |

## Recursos adicionais {#additional-resources}

* **Developer Console**: acesse o [Adobe Developer Console](https://developer.adobe.com){target="_blank"} para criar integrações e gerenciar credenciais de API.
* **Código de exemplo**: explore [implementações de exemplo no GitHub](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}.
* **Vídeos tutoriais**: aprenda com tutoriais práticos na [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=pt-BR){target="_blank"}.
* **Comunidade de desenvolvedores**: conecte-se com outros desenvolvedores e obtenha suporte nos fóruns da comunidade da Adobe.

## Colaborar entre funções {#next-steps}

O trabalho de implementação cruza com o trabalho de outros membros da equipe:

>[!BEGINTABS]

>[!TAB Trabalhar com Engenheiros de dados]

Colabore com [engenheiros de dados](data-engineer.md) em configurações de dados e eventos. Cada jornada que reage ao comportamento do usuário depende dos eventos enviados — o Engenheiro de dados define os esquemas e implementa o código que os produz.

* Obtenha os [esquemas XDM](../../data/get-started-schemas.md) e as estruturas de evento necessárias para implementar
* Entenda quais eventos você precisa enviar e o formato de conteúdo necessário — consulte [trabalho com eventos de jornada](../../event/about-events.md)
* Confirme quais campos são obrigatórios vs. opcionais em cada carga do evento e o que acontece no jornada quando os campos esperados estão ausentes ou malformados — consulte [requisitos de esquema](../../event/experience-event-schema.md#schema-requirements)
* Teste a entrega de eventos e a assimilação de dados em conjunto usando o [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=pt-BR){target="_blank"}

>[!TAB Trabalhar com admins]

Colabore com [Administradores](administrator.md) em configurações de acesso e canal. O Jornada só pode alcançar os usuários por meio de canais configurados pelo administrador — coordene antecipadamente para que o SDK funcione e a configuração permaneça sincronizada.

* Fornecer especificações de API para [ações personalizadas](../../action/about-custom-action-configuration.md) que serão configuradas no Journey Optimizer
* Solicite as permissões necessárias e as credenciais de API via [Adobe Developer Console](https://developer.adobe.com){target="_blank"}
* Coordenar nos requisitos de configuração de canal — enviar certificados para o [iOS](../../push/push-configuration.md) e o Android, [enviar pela Web](../../push/push-configuration-web.md) configurações, [webhook de SMS](../../mobile/mobile-webhook.md) pontos de extremidade
* Alinhe a estratégia de sandbox e os ambientes de teste antes de executar o [modo de teste de jornada](../../building-journeys/testing-the-journey.md)

>[!TAB Trabalhar com profissionais de marketing]

Colabore com [profissionais de marketing](marketer.md) no design e teste do jornada. Os profissionais de marketing criam as jornadas e o conteúdo que dependem totalmente dos eventos enviados e das superfícies expostas — quanto mais perto você se alinha, mais rapidamente as jornadas são ativadas.

* Revise os designs de jornada em [Journey Optimizer](../../building-journeys/journey.md) em conjunto para entender quais interações de usuário devem disparar eventos e quais superfícies precisam de personalização
* Implemente o rastreamento para que os profissionais de marketing possam medir [o desempenho do conteúdo e o engajamento do usuário](../../reports/report-gs-cja.md)
* Execute o [modo de teste de jornada](../../building-journeys/testing-the-journey.md) juntos usando perfis de teste para validar o fluxo completo de ponta a ponta
* Solucione problemas com a entrega de mensagens, renderização de personalização ou respostas de [ação personalizada](../../action/action.md)

>[!ENDTABS]

## Comece a implementar

Pronto(a) para começar a criar? Escolha a primeira área de implementação nas seções acima:

1. **Aplicativo móvel?** Inicie com a [integração do SDK móvel](#mobile-integration)
2. **Site?** Comece com a [configuração do SDK da Web](#web-implementation)
3. **Integração da API?** Ir para a seção [Trabalho com APIs](#apis)
4. **Sistema personalizado?** Confira as [Ações personalizadas](#custom-actions)

Cada seção inclui links para a documentação técnica detalhada, amostras de código e tutoriais para orientar a implementação.

## Outros guias de função {#other-role-guides}

| Função | Guia |
|------|-------|
| Administrador | [Introdução para administradores](administrator.md) |
| Engenheiro de dados | [Introdução para engenheiros de dados](data-engineer.md) |
| Desenvolvedor | [Introdução para desenvolvedores](developer.md) |
| Profissional de marketing | [Introdução para profissionais de marketing](marketer.md) |

Voltar à [Visão geral de funções e responsabilidades](../quick-start.md) · Voltar à [Introdução](../../../rp_landing_pages/get-started-landing-page.md)
