---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 2%

---
O arquivo não existe no repositório de pipeline — é um arquivo de documentação fornecido como contexto. Escreverei a marcação atualizada completa diretamente conforme instruído (apenas o arquivo é exibido, sem explicações).

&#x200B;---

solução: Journey Optimizer
produto: otimizador de jornada
title: Ativar o modo de alta taxa de transferência para campanhas acionadas por API
description: Saiba como ativar o modo Alta taxa de transferência para campanhas acionadas por API.
recurso: Campanhas, API
tópico: Gestão de conteúdo
função: desenvolvedor
level: Experiente
palavras-chave: campanhas, acionadas por API, REST, otimizer, mensagens
exl-id: 2b3e87dc-097a-4d05-873c-f421d11338c3
TQID: https://experienceleague.adobe.com/SwmK1epuhZUf4EWnaLRHTBH-eE1hEV02Z8nqXGtMb6U
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
rótulo interno: Journey Optimizer
feature_v2:
- id: d556b755-390a-43f0-be32-a08cf6236126
internal-label: Configuração
- id: a653cc2e-bc85-4353-a306-399e5b247978
rótulo interno: campanhas do Journey Optimizer
subfeature_v2:
- id: f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label: campanhas acionadas por API
- id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label: Gerenciamento de campanha
role_v2:
- id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Desenvolvedor
topic_v2:
- id: e0eb8757-182f-49f3-94a4-1587d16f5094
rótulo interno: Personalization
---
# Ativar modo de taxa de transferência alta para campanhas acionadas por API {#high-throughput}

>[!BEGINSHADEBOX]

**Nesta página:** ative o modo de alta taxa de transferência para campanhas acionadas pela API para que você possa enviar mensagens transacionais em tempo real em grande escala em até 5.000 transações por segundo (email) ou até 1.500 transações por segundo (push) sem depender de perfis.

>[!ENDSHADEBOX]

O modo Alta Taxa de Transferência foi projetado para organizações que precisam de **mensagens transacionais em tempo real e em grande escala**. Diferentemente das campanhas acionadas pela API comum, as campanhas de alta taxa de transferência operam independentemente dos Perfis do Adobe e exigem um modelo de configuração diferente.

Esta página explica como as campanhas com alta taxa de transferência diferem das campanhas acionadas pela API padrão, dos requisitos de configuração e de quando escolher cada modo.

## Medidas de proteção e limitações

&#x200B;* **Acesso** - Disponível somente na região dos EUA para organizações licenciadas com o complemento de mensagens transacionais de Alta Taxa de Transferência.

&#x200B;* **Canais**: disponíveis para notificações por email e por push.

&#x200B;* **Taxa de transferência**:

   &#x200B;* **Email** - Até 5.000 transações por segundo.
   &#x200B;* **Push** - Até 1500 transações por segundo. Os seguintes níveis de taxa de transferência em camadas estão disponíveis: 500 TPS (base), 1000 TPS e 1500 TPS. Níveis mais altos exigem o direito complementar apropriado.

&#x200B;* **Personalization**:

   &#x200B;* Toda a personalização deve ser incluída na carga da API como **dados contextuais**. [Saiba como personalizar o conteúdo usando dados contextuais](../campaigns/api-triggered-campaign-content.md#contextual)
   &#x200B;* A personalização baseada em perfil não é compatível. Se as variáveis de perfil forem usadas, ocorrerão erros de validação.

&#x200B;* **Configurações de canal personalizadas** - As configurações de canal que usam [personalização baseada em perfil](../email/surface-personalization.md) não podem ser usadas com campanhas de alta taxa de transferência. Somente superfícies sem personalização de perfil podem ser usadas.

&#x200B;* **Ponto de extremidade de API** - As campanhas com Alta Taxa de Transferência usam um ponto de extremidade diferente das campanhas acionadas pela API padrão. Para obter detalhes, consulte [Executar uma campanha acionada por API](../campaigns/trigger-campaigns.md#trigger).

&#x200B;* **Exclusividade da campanha** - Campanhas de alta taxa de transferência não usam Perfis do Adobe. As mensagens são entregues independentemente de um perfil existir ou não.

  Além disso, uma campanha não pode ser usada para casos de uso habilitados para perfil e não perfis. Se precisar de ambos, crie duas campanhas separadas e verifique se o sistema de chamada decide qual delas acionar com base no contexto.

&#x200B;* **Conjuntos de dados para feedback e rastreamento** - Os dados de feedback e rastreamento para campanhas de alta taxa de transferência são armazenados em conjuntos de dados dedicados que não estão habilitados para perfis. Como resultado, esses eventos não são compilados em perfis, mesmo se um perfil correspondente existir.

  Os conjuntos de dados usados são:

   &#x200B;* **Conjunto de Dados de Evento de Feedback de Mensagens do AJO - Não Perfil**
   &#x200B;* **Conjunto De Dados De Evento De Experiência De Acompanhamento De Email Do AJO - Não Perfil**

&#x200B;* **Alocação de taxa de transferência** - A taxa de transferência provisionada no complemento Alta Taxa de Transferência é reservada exclusivamente para campanhas de alta taxa de transferência. Não há compartilhamento de taxa de transferência entre campanhas padrão e campanhas acionadas pela API de alta taxa de transferência.

## Escolha entre campanhas com taxa de transferência padrão vs. alta

Use esta tabela para decidir qual tipo de campanha acionada por API se adapta ao seu caso de uso:

| Recurso/Requisito | Campanha acionada por API padrão | Campanha de alto rendimento |
|------------------------|---------------------------------|---------------------------|
| **Disponibilidade** | Incluído na oferta base | Requer complemento de mensagens transacionais de alta taxa de transferência. |
| **Taxa de transferência** | Até 500 transações por segundo | Até 5.000 TPS (email); até 1.500 TPS (push) |
| **Canais** | Email, SMS, Push | Email, Push |
| **Personalização** | Perfil + contextual na carga da API | Contextual somente na carga da API |
| **Compilação e perfil** | Existe ou é criado com eventos compilados no perfil | Nenhum perfil |
| **Volume da mensagem** | Pacotes de mensagens e direitos padrão | Separar volumes de mensagens em camadas |
| **Infraestrutura** | Standard | Aprimorado |
| **Tempo de atividade** | 99,9% | 99,99% |
| **API de verificação de integridade** | Sim | Sim |

Em outras palavras:

&#x200B;* Escolha **Campanhas de API padrão acionadas** se:
   &#x200B;* Você não tem contrato de alto throughput.
   &#x200B;* Suas necessidades de taxa de transferência são ≤ 500 TPS.
   &#x200B;* Você precisa de personalização com base nos perfis do Adobe.
   &#x200B;* Você deseja que os dados da campanha sejam compilados com perfis para direcionamento futuro.
   &#x200B;* Você precisa de mensagens SMS.

&#x200B;* Escolha campanhas de **Alta taxa de transferência** se:
   &#x200B;* Você precisa de throughput >500 TPS.
   &#x200B;* Você não precisa de compilação de perfil.
   &#x200B;* Você pode transmitir toda a personalização na carga da API.
   &#x200B;* Você deseja usar o canal de email ou push.

## Configurar diretrizes

Para configurar campanhas de Alta Taxa de Transferência corretamente, siga estas diretrizes:

1. **Somente para alta taxa de transferência de email** - Crie um novo pool de IPs. [Saiba como criar pools de IP](../configuration/ip-pools.md)
1. Crie uma nova configuração de canal. [Saiba como definir configurações de canal](../configuration/channel-surfaces.md)
1. Entre em contato com o Atendimento ao cliente da Adobe para solicitar que a superfície ativada seja mapeada para o recurso de Alta taxa de transferência. Forneça a configuração do canal e os detalhes do Pool de IPs (para email) junto com a ID da organização.

>[!IMPORTANT]
>
>As configurações de canal designadas para mensagens transacionais de alta taxa de transferência devem ser usadas exclusivamente para essa finalidade, e não devem ser usadas com mensagens transacionais padrão usando campanhas ou jornadas acionadas por API. Para alta taxa de transferência de e-mail, o pool de IP designado para essa finalidade também deve ser usado exclusivamente para envio de alta taxa de transferência.