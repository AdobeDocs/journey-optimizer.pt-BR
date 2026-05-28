---
solution: Journey Optimizer
product: journey optimizer
title: Ações de auditoria em recursos do Journey Optimizer
description: Saiba como rastrear ações executadas em recursos do Journey Optimizer.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2: id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56id: f365ec33-2b99-4b7f-b4ee-c743dd7f615fid: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 100%

---

# Ações de auditoria em recursos do Journey Optimizer {#track-changes}

## Sobre logs de auditoria {#audit-logs}

>[!IMPORTANT]
>
>Para exibir e exportar o log de auditoria, você deve ter a permissão **[!DNL View User Activity Log]** concedida. [Saiba mais](../administration/ootb-product-profiles.md)

Com o Journey Optimizer, você pode identificar as ações executadas pelos usuários no sistema em vários serviços e recursos como jornadas, mensagens, páginas de destino etc.

Isso permite aumentar a visibilidade das atividades realizadas no sistema, solucionar problemas e ajudar seu negócio a cumprir os regulamentos e as políticas corporativas de gerenciamento de dados.

Cada ação é registrada com metadados em “logs de auditoria”, que são acessíveis na Adobe Experience Platform. Para obter mais informações sobre logs de auditoria, incluindo como visualizá-los e gerenciá-los na interface ou na API, consulte a [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=pt-BR).

![](assets/audit-logs.png)

## Tipos de evento capturados por logs de auditoria {#events}

A tabela a seguir descreve quais ações de recursos do Journey Optimizer são registradas por logs de auditoria. A lista completa de ações capturadas nos logs de auditoria está disponível na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=pt-BR#category).

>[!NOTE]
>
>Logs de auditoria relacionados à **gestão de decisões** são visíveis apenas no arquivo CSV que pode ser baixado usando o botão **[!UICONTROL Baixar log]**.

| Recurso | Ação |
|-----------|------------------|
| Campanha do AJO | Criar / Excluir / Atualizar / Ativar / Interromper |
| Configuração geral do canal do AJO | Criar / Excluir / Atualizar |
| Pool de IP do AJO | Criar / Excluir / Atualizar |
| Páginas de destino do AJO | Criar / Excluir / Atualizar / Publicar / Desfazer a publicação |
| Modelo HTML da página de destino do AJO | Criar / Excluir / Atualizar |
| Predefinição da página de destino do AJO | Criar / Excluir / Atualizar |
| Subdomínio da página de destino do AJO | Criar / Excluir / Atualizar |
| Predefinição de mensagem do AJO | Criar / Excluir / Atualizar |
| Registro PTR do AJO | Criar / Excluir / Atualizar |
| Modelo de expressão salva do AJO | Criar / Excluir / Atualizar |
| Credenciais da API de SMS do AJO | Criar / Excluir / Atualizar |
| Subdomínio do AJO | Criar / Excluir / Atualizar |
| Lista de supressão do AJO | Criar / Excluir / Baixar CSV |
| Grupo de campos | Criar / Excluir / Atualizar |
| Jornada | Criar / Excluir / Atualizar / Interromper / Publicar |
| Ação personalizada da jornada | Criar / Excluir / Atualizar |
| Fonte de dados da jornada | Criar / Excluir / Atualizar |
| Evento da jornada | Criar / Excluir / Atualizar |
| Regra de frequência de mensagens | Criar / Excluir / Atualizar |
| Estratégia de classificação | Criar / Excluir / Atualizar |
