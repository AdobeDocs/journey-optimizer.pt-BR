---
solution: Journey Optimizer
product: journey optimizer
title: Ativar o modo de alta taxa de transferência para campanhas acionadas por API
description: Saiba como ativar o modo Alta taxa de transferência para campanhas acionadas por API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
source-git-commit: 4521990a02092365f996a81299ada55433639fb7
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 2%

---


# Ativar o modo de alta taxa de transferência para campanhas acionadas por API {#high-throughput}

O modo Alta Taxa de Transferência foi projetado para organizações que precisam de **mensagens transacionais em tempo real de grande escala** (até 5.000 transações por segundo). Diferentemente das campanhas acionadas pela API comum, as campanhas de alta taxa de transferência operam independentemente dos Perfis do Adobe e exigem um modelo de configuração diferente.

Esta página explica como as campanhas com alta taxa de transferência diferem das campanhas acionadas pela API padrão, dos requisitos de configuração e de quando escolher cada modo.

## Medidas de proteção e limitações

* **Acesso** - Disponível somente na região dos EUA para organizações licenciadas com o complemento de mensagens transacionais de Alta Taxa de Transferência.

* **Canais**: atualmente disponíveis apenas para email.

* **Personalization**:

   * Toda a personalização deve ser incluída na carga da API como **dados contextuais**. [Saiba como personalizar o conteúdo usando dados contextuais](../campaigns/api-triggered-campaign-action.md#contextual)
   * A personalização baseada em perfil não é compatível. Se as variáveis de perfil forem usadas, ocorrerão erros de validação.

* **Configurações de canal personalizadas** - As configurações de canal que usam [personalização baseada em perfil](../email/surface-personalization.md) não podem ser usadas com campanhas de alta taxa de transferência. Somente superfícies sem personalização de perfil podem ser usadas.

* **Ponto de extremidade de API** - As campanhas com Alta Taxa de Transferência usam um ponto de extremidade diferente das campanhas acionadas pela API padrão. Para obter detalhes, consulte [Executar uma campanha acionada por API](../campaigns/trigger-campaigns.md#trigger).

* **Exclusividade da campanha** - Campanhas de alta taxa de transferência não usam Perfis do Adobe. As mensagens são entregues independentemente de um perfil existir ou não.

  Além disso, uma campanha não pode ser usada para casos de uso habilitados para perfil e não perfis. Se precisar de ambos, crie duas campanhas separadas e verifique se o sistema de chamada decide qual delas acionar com base no contexto.

* **Conjuntos de dados para feedback e rastreamento** - Os dados de feedback e rastreamento para campanhas de alta taxa de transferência são armazenados em conjuntos de dados dedicados que não estão habilitados para perfis. Como resultado, esses eventos não são compilados em perfis, mesmo se um perfil correspondente existir.

  Os conjuntos de dados usados são:

   * **Conjunto de Dados de Evento de Feedback de Mensagens do AJO - Não Perfil**
   * **Conjunto De Dados De Evento De Experiência De Acompanhamento De Email Do AJO - Não Perfil**

* **Alocação de taxa de transferência** - A taxa de transferência provisionada no complemento Alta Taxa de Transferência é reservada exclusivamente para campanhas de alta taxa de transferência. Não há compartilhamento de taxa de transferência entre campanhas padrão e campanhas acionadas pela API de alta taxa de transferência.

## Escolha entre campanhas com taxa de transferência padrão vs. alta

Use esta tabela para decidir qual tipo de campanha acionada por API se adapta ao seu caso de uso:

| Recurso/Requisito | Campanha acionada por API padrão | Campanha de alto rendimento |
|------------------------|---------------------------------|---------------------------|
| **Disponibilidade** | Incluído na oferta base | Requer complemento de mensagens transacionais de alta taxa de transferência. |
| **Taxa de transferência** | Até 500 transações por segundo | Até 5.000 transações por segundo |
| **Canais** | Email, SMS, Push | Email |
| **Personalização** | Perfil + contextual na carga da API | Contextual somente na carga da API |
| **Compilação e perfil** | Existe ou é criado com eventos compilados no perfil | Nenhum perfil |
| **Volume da mensagem** | Pacotes de mensagens e direitos padrão | Separar volumes de mensagens em camadas |
| **Infraestrutura** | Standard | Aprimorado |
| **Tempo de atividade** | 99,9 % | 99,99 % |
| **API de verificação de integridade** | Sim | Sim |

Em outras palavras:

* Escolha **Campanhas de API padrão acionadas** se:
   * Você não tem contrato de alto throughput.
   * Suas necessidades de throughput são &lt;500 TPS.
   * Você precisa de personalização com base nos perfis do Adobe.
   * Você deseja que os dados da campanha sejam compilados com perfis para direcionamento futuro.
   * Você deseja usar outro canal diferente de Email.

* Escolha campanhas de **Alta taxa de transferência** se:
   * Você precisa de throughput >500 TPS.
   * Você não exige a compilação de perfil.
   * Você pode transmitir toda a personalização na carga da API.
   * Você deseja usar o canal de email.

## Configurar diretrizes

Para configurar campanhas de Alta Taxa de Transferência corretamente, siga estas diretrizes:

1. Crie um novo pool de IPs. [Saiba como criar pools de IP](../configuration/ip-pools.md)
1. Crie uma nova configuração de canal. [Saiba como definir configurações de canal](../configuration/channel-surfaces.md)
1. Entre em contato com o Atendimento ao cliente da Adobe para solicitar que a superfície ativada seja mapeada para o recurso de Alta taxa de transferência. Forneça a configuração do canal e os detalhes do Pool de IP junto com a ID da organização.

>[!IMPORTANT]
>
>O pool de IP e as configurações de canal designadas para mensagens transacionais de alta taxa de transferência devem ser usados exclusivamente para essa finalidade e não devem ser usados com mensagens transacionais padrão usando campanhas ou jornadas acionadas por API.
