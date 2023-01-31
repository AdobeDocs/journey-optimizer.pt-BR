---
solution: Journey Optimizer
product: journey optimizer
title: Ações de auditoria em recursos do Journey Optimizer
description: Saiba como rastrear ações executadas em recursos do Journey Optimizer.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 89%

---

# Ações de auditoria em recursos do Journey Optimizer {#track-changes}

## Sobre logs de auditoria {#audit-logs}

>[!IMPORTANT]
>
>Para exibir e exportar o log de auditoria, você deve ter a variável **[!DNL View User Activity Log]** permissão concedida. [Saiba mais](../administration/ootb-product-profiles.md)

Com o Journey Optimizer, você pode identificar as ações executadas pelos usuários no sistema em vários serviços e recursos como jornadas, mensagens, páginas de destino etc.

Isso permite aumentar a visibilidade das atividades realizadas no sistema, solucionar problemas e ajudar sua empresa a cumprir os regulamentos e as políticas corporativas de gerenciamento de dados.

Cada ação é registrada com metadados em “logs de auditoria”, que são acessíveis na Adobe Experience Platform. Para obter mais informações sobre logs de auditoria, incluindo como visualizá-los e gerenciá-los na interface do usuário ou na API, consulte [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=pt-BR).

![](assets/audit-logs.png)

## Tipos de evento capturados por logs de auditoria {#events}

A tabela a seguir descreve quais ações, em quais recursos do Journey Optimizer, são registradas por logs de auditoria.

>[!NOTE]
>
>A lista completa de ações capturadas nos logs de auditoria está disponível na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=pt-BR#category).

| Recurso | Ação |
|-----------|------------------|
| Campanha do AJO | Criar / Excluir / Atualizar / Ativar / Interromper |
| Configuração geral do canal do AJO | Criar / Excluir / Atualizar |
| Pool de IP do AJO | Criar / Excluir / Atualizar |
| Páginas de destino do AJO | Criar / Excluir / Atualizar / Publicar / Desfazer a publicação |
| Modelo HTML da página de destino do AJO | Criar / Excluir / Atualizar |
| Predefinição da página de destino do AJO | Criar / Excluir / Atualizar |
| Subdomínio da página de destino do AJO | Criar / Excluir / Atualizar |
| Mensagens do AJO | Criar / Excluir / Atualizar / Publicar |
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
