---
solution: Journey Optimizer
product: journey optimizer
title: Revisar e ativar uma campanha
description: Saiba como revisar e ativar campanhas no Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campaign, review, validation, ativating, ativating, otimizer
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
TQID: https://experienceleague.adobe.com/Q9UQEnAqQNFD869w4lQOQxcbH82SwDZyT8Q-9RvRD5k
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a5c0537a45acbc708ce62bd05a569630230201ac
workflow-type: tm+mt
source-wordcount: 584
ht-degree: 1%

---

# Executar uma campanha acionada por API {#execute}

>[!BEGINSHADEBOX]

**Nesta página:** recupere a solicitação de cURL gerada e use-a para acionar a campanha acionada pela API em tempo real por meio das APIs, com orientações de solução de problemas para que você possa resolver atrasos de entrega e erros de autenticação.

>[!ENDSHADEBOX]

Depois que sua campanha for ativada, é necessário recuperar a solicitação de cURL de amostra gerada e usá-la na API para criar sua carga e acionar a campanha.

## Leitura obrigatória {#must-read}

* **Datas de início/término da campanha** - Se você tiver configurado uma data de início e/ou término específica ao criar a campanha, ela não será executada fora dessas datas, e as chamadas de API falharão.

* **Tempo limite de chamada** - A chamada para a API REST de Execução de Mensagem Interativa tem um tempo limite de 60 segundos. No entanto, tentativas internas estão em vigor no caso de tempos limite inesperados para garantir o delivery.

## Acionar a campanha {#trigger}

1. Abra a campanha e copie e cole a solicitação de carga da seção **[!UICONTROL cURL request]**. Essa carga inclui todas as variáveis de personalização (perfil e contexto) usadas na mensagem. Ele fica disponível assim que a campanha é ativada.

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >Os pontos de extremidade na seção cURL diferem entre as [campanhas padrão e de alta taxa de transferência](../campaigns/api-triggered-high-throughput.md).

1. Use essa solicitação de cURL nas APIs para criar sua carga e acionar a campanha. Para obter mais informações, consulte a [documentação da API de Execução de Mensagens Interativas](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution), onde todos os pontos de extremidade para campanhas padrão e de Alta Taxa de Transferência são listados.

   Exemplos de chamadas de API também estão disponíveis em [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples).

## Solução de problemas {#troubleshooting}

### Atrasos de entrega de email {#delivery-delays}

Se os tempos de delivery de email excederem as expectativas, investigue possíveis interrupções ou problemas de desempenho com serviços externos, como provedores de infraestrutura em nuvem ou provedores de serviço de email. O Journey Optimizer registra os carimbos de data e hora de partida da mensagem, que podem ajudar a determinar se ocorreram atrasos downstream no pipeline de entrega.

### Erros de autenticação do Azure cosmos DB (erro interno 500 do servidor) {#cosmosdb-auth-errors}

Se você encontrar **500 Erros Internos do Servidor** ao acionar campanhas acionadas por API, e os logs do sistema mostrarem um erro **403 Proibido** do Azure Cosmos DB com uma mensagem como:

_&quot;O acesso à sua conta está revogado no momento porque o serviço Azure Cosmos DB não pode obter o token de autenticação AAD para a identidade padrão da conta&quot;_

Normalmente, esse erro ocorre quando a entidade de serviço do Azure necessária para a autenticação do Cosmos DB foi desabilitada, excluída ou configurada incorretamente.

+++Como resolver esse problema

1. **Verifique a entidade de serviço do Azure** - Verifique se a entidade de serviço ou a identidade gerenciada do Azure está habilitada e não foi desabilitada ou excluída no Azure Ative Diretory.

1. **Verificar permissões** - Confirme se a entidade de serviço tem as permissões necessárias para acessar os recursos do Cofre de Chaves da Azure e do Cosmos DB. A entidade de serviço deve ter atribuições de função apropriadas para autenticar com o Azure Cosmos DB.

1. **Revise a configuração do CMK do Azure Cosmos DB** - Se estiver usando CMK (Chaves gerenciadas pelo cliente), consulte o [guia de solução de problemas do CMK do Azure Cosmos DB](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"} para obter etapas detalhadas sobre como restaurar a aquisição do token AAD.

1. **Reabilitar e testar** - Depois de corrigir a configuração, habilite novamente a entidade de serviço, se ela estiver desabilitada, e teste novamente suas chamadas de API de campanha transacional para confirmar se a autenticação foi bem-sucedida, e se as mensagens foram entregues.

>[!NOTE]
>
>Normalmente, esse problema é causado por uma configuração incorreta ou desabilitação acidental da entidade de serviço do Azure necessária para a autenticação do Cosmos DB. Manter a entidade de serviço habilitada e configurada corretamente evitará esse erro no futuro.

+++
