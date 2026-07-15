---
title: Configurar um canal personalizado - visão geral
description: Saiba mais sobre as etapas que um administrador precisa concluir para configurar um canal personalizado no Adobe Journey Optimizer, desde a criação do canal até a definição de uma configuração de canal.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilidade limitada" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# Configurar um canal personalizado {#custom-channel-configuration}

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

Configurar um canal personalizado é uma tarefa de administrador que ocorre uma vez por canal. Após a configuração do canal, os profissionais de marketing podem selecioná-lo imediatamente em campanhas, jornadas e campanhas orquestradas, como em qualquer canal [!DNL Journey Optimizer] nativo.

O processo de configuração abrange quatro etapas: definir o próprio canal (endpoint, autenticação, carga), gerenciar as credenciais de API usadas para autenticar solicitações, delegar opcionalmente um subdomínio para rastreamento de link e, finalmente, criar uma configuração de canal que os profissionais de marketing selecionarão no momento da criação.

>[!NOTE]
>
>Antes de começar, revise os pré-requisitos e as medidas de proteção para canais personalizados, incluindo as permissões necessárias e os métodos de autenticação compatíveis.

## Etapas de configuração {#steps}

O processo de configuração de um canal personalizado consiste em quatro etapas. Cada etapa é descrita em detalhes nos artigos vinculados abaixo.

| Etapa | O que você faz | Por que isso importa | Link |
| --- | --- | --- | --- |
| **1. Criar o canal personalizado** | Defina o URL do endpoint, os cabeçalhos, a política de limitação, o tipo de autenticação e a estrutura de payload da mensagem no Channel Builder. | Essa é a definição principal do seu canal. Informa ao [!DNL Journey Optimizer] como enviar uma mensagem e qual é a aparência dela. | [Saiba mais](create-custom-channel.md) |
| **2. Gerenciar credenciais de API** | Crie e gerencie os conjuntos de credenciais usadas para autenticar solicitações no seu ponto de extremidade. | Vários conjuntos de credenciais permitem reutilizar a mesma definição de canal em diferentes marcas ou ambientes sem duplicar o canal. | [Saiba mais](custom-channel-api-credentials.md) |
| **3. Delegar um subdomínio** *(opcional)* | Delegar um subdomínio especificamente para o canal personalizado. | Obrigatório somente se a carga da mensagem contiver links rastreáveis. Sem um subdomínio delegado, o rastreamento de link não está disponível para este canal. | [Saiba mais](custom-channel-subdomains.md) |
| **4. Criar uma configuração de canal** | Crie uma predefinição nomeada que vincula o canal personalizado a um conjunto específico de credenciais, um subdomínio e padrões opcionais de carga. | Ao criar campanhas ou jornadas, os profissionais de marketing selecionam um canal personalizado e uma configuração de canal associada. É possível criar várias configurações para o mesmo canal (por exemplo, uma por marca ou região). | [Saiba mais](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->