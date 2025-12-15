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
source-git-commit: a5d8f10c8751d6be47f5423aea576e16590b86d6
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 1%

---


# Executar uma campanha acionada por API {#execute}

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

1. Use essa solicitação de cURL nas APIs para criar sua carga e acionar a campanha. Para obter mais informações, consulte a [documentação da API de Execução de Mensagens Interativas](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution), onde todos os pontos de extremidade para campanhas padrão e de Alta Taxa de Transferência são listados.

   Exemplos de chamadas de API também estão disponíveis em [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

## Solução de problemas {#troubleshooting}

### Atrasos de entrega de email {#delivery-delays}

Se os tempos de delivery de email excederem as expectativas, investigue possíveis interrupções ou problemas de desempenho com serviços externos, como provedores de infraestrutura em nuvem ou provedores de serviço de email. O Journey Optimizer registra os carimbos de data e hora de partida da mensagem, que podem ajudar a determinar se ocorreram atrasos downstream no pipeline de entrega.

### Erros de autenticação do Azure Cosmos DB (Erro interno 500 do servidor) {#cosmosdb-auth-errors}

Se você encontrar **500 Erros Internos do Servidor** ao acionar campanhas acionadas por API, e os logs do sistema mostrarem um erro **403 Proibido** do BD do Azure Cosmos com uma mensagem como:

_&quot;O acesso à sua conta está revogado no momento porque o serviço Azure Cosmos DB não pode obter o token de autenticação AAD para a identidade padrão da conta&quot;_

Normalmente, esse erro ocorre quando a entidade de serviço do Azure necessária para a autenticação do Cosmos DB foi desabilitada, excluída ou configurada incorretamente.

+++Como resolver esse problema

1. **Verifique a entidade de serviço do Azure** - Verifique se a entidade de serviço do Azure ou a identidade gerenciada está habilitada e não foi desabilitada ou excluída no Azure Ative Diretory.

1. **Verificar permissões** - Confirme se a entidade de serviço tem as permissões necessárias para acessar os recursos do Cofre de Chaves do Azure e do Cosmos DB. A entidade de serviço deve ter atribuições de função apropriadas para autenticar com o Azure Cosmos DB.

1. **Revise a configuração do CMK do Azure Cosmos DB** - Se estiver usando as Chaves Gerenciadas pelo Cliente (CMK), consulte o [guia de solução de problemas do CMK do Azure Cosmos DB](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"} para obter etapas detalhadas sobre como restaurar a aquisição do token AAD.

1. **Reabilitar e testar** - Depois de corrigir a configuração, habilite novamente a entidade de serviço, se ela estiver desabilitada, e teste novamente suas chamadas de API de campanha transacional para confirmar se a autenticação foi bem-sucedida, e se as mensagens foram entregues.

>[!NOTE]
>
>Normalmente, esse problema é causado por uma configuração incorreta ou desabilitação acidental da entidade de serviço do Azure necessária para a autenticação do Cosmos DB. Manter a entidade de serviço habilitada e configurada corretamente evitará esse erro no futuro.

+++
