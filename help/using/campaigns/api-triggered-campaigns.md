---
solution: Journey Optimizer
product: journey optimizer
title: Acione campanhas usando APIs
description: Saiba como acionar campanhas usando APIs do Journey Optimizer
topic: Content Management
role: Developer, Admin
level: Intermediate, Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 6999f52a3426aa252f31440189ba9d1a7118dd0a
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 1%

---

# Acione campanhas usando APIs {#trigger-campaigns}

## Sobre campanhas acionadas por API {#about}

Com [!DNL Journey Optimizer], você pode criar campanhas e chamá-las de um sistema externo com base no acionador do usuário usando o [API REST de execução de mensagem interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Isso permite cobrir várias necessidades de mensagens de marketing e transacionais, como redefinições de senha, token OTP, entre outras.

Para fazer isso, primeiro é necessário criar uma campanha acionada por API no Journey Optimizer e, em seguida, iniciar a execução por meio de uma chamada de API.

![](../rn/assets/do-not-localize/api-triggered.gif)

Os canais disponíveis para campanhas acionadas por API são mensagens de email, SMS e push.

>[!NOTE]
>
>Por enquanto, o modo de entrega rápida não é compatível com campanhas acionadas por API de notificação por push.

## Criar uma campanha acionada por API {#create}

### Configurar e ativar a campanha {#create-activate}

Para criar uma campanha acionada por API, siga as etapas abaixo. Informações detalhadas sobre como criar uma campanha estão disponíveis em [nesta seção](create-campaign.md).

1. Crie uma nova campanha com o **[!UICONTROL Acionado pela API]** tipo.

1. Escolha o **[!UICONTROL Marketing]** ou **[!UICONTROL Transacional]** categoria dependendo do tipo de comunicação que você deseja enviar.

1. Escolha um dos canais com suporte e a superfície de canal associada a serem usados para enviar a mensagem. Em seguida, clique em **[!UICONTROL Criar]**.

   ![](assets/api-triggered-type.png)

1. Especifique um título e uma descrição para a campanha e clique em **[!UICONTROL Editar conteúdo]** para configurar a mensagem a ser enviada.

   >[!NOTE]
   >
   >Você pode transmitir dados adicionais para a carga da API que você pode usar para personalizar sua mensagem. [Saiba mais](#contextual)
   >
   >O uso de um grande número ou de dados contextuais pesados em seu conteúdo pode afetar o desempenho.

1. No **[!UICONTROL Público]** especifique o namespace a ser usado para identificar os indivíduos.

   * Se você estiver criando uma **transacional** tipo campanha, os perfis segmentados precisam ser definidos na chamada de API. A variável **[!UICONTROL Criar novos perfis]** permite criar automaticamente perfis que não existem no banco de dados. [Saiba mais sobre a criação de perfil na execução da campanha](#profile-creation)

   * Para **marketing** campanhas do tipo, clique no link **[!UICONTROL Público]** botão para escolher o público-alvo a ser direcionado.

1. Configure as datas de início e término da campanha.

   Se você configurar uma data de início e/ou término específica para uma campanha, ela não será executada fora dessas datas, e as chamadas de API falharão se a campanha for acionada por APIs.

1. Clique em **[!UICONTROL Revisar para ativar]** para verificar se a campanha está configurada corretamente, ative-a.

Agora você está pronto para executar a campanha das APIs. [Saiba mais](#execute)

### Executar a campanha {#execute}

Depois que sua campanha for ativada, é necessário recuperar a solicitação de cURL de amostra gerada e usá-la na API para criar sua carga e acionar a campanha.

1. Abra a campanha e copie e cole a solicitação de amostra do **[!UICONTROL solicitação cURL]** seção.

   ![](assets/api-triggered-curl.png)

1. Use essa solicitação de cURL nas APIs para criar sua carga e acionar a campanha. Para obter mais informações, consulte [Documentação da API de execução de mensagem interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   Exemplos de chamada de API também estão disponíveis em [esta página](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Se você tiver configurado uma data de início e/ou término específica ao criar a campanha, ela não será executada fora dessas datas e as chamadas de API falharão.

## Usar atributos contextuais em campanhas acionadas por API {#contextual}

Com campanhas acionadas por API, você pode transmitir dados adicionais na carga da API e usá-los na campanha para personalizar sua mensagem.

Vejamos este exemplo, em que os clientes desejam redefinir suas senhas e você deseja enviar a eles um URL de redefinição de senha gerado em uma ferramenta de terceiros. Com campanhas acionadas por API, é possível passar esse URL gerado para a carga da API e aproveitá-lo na campanha para adicioná-lo à mensagem.

>[!NOTE]
>
>Diferentemente dos eventos habilitados para perfis, os dados contextuais transmitidos na API REST são usados para comunicação única e não são armazenados em relação ao perfil. No máximo, o perfil é criado com os detalhes do namespace, se ele estiver ausente.

Para usar esses dados em suas campanhas, você precisa passá-los para a carga da API e adicioná-los em sua mensagem usando o editor de expressão. Para fazer isso, use o `{{context.<contextualAttribute>}}` sintaxe, onde `<contextualAttribute>` deve corresponder ao nome da variável na carga da API que contém os dados que você deseja passar.

A variável `{{context.<contextualAttribute>}}` A sintaxe é mapeada somente para um tipo de dados String.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>Os atributos contextuais passados para a solicitação não podem exceder 50 kb e são sempre considerados do tipo string.
>
>A variável `context.system` a sintaxe é restrita somente ao uso interno do Adobe e não deve ser usada para transmitir atributos contextuais.

Observe que, por enquanto, nenhum atributo contextual está disponível para uso no menu do painel esquerdo. Os atributos devem ser digitados diretamente na sua expressão de personalização, sem que nenhuma verificação seja executada por [!DNL Journey Optimizer].

## Criação de perfil na execução da campanha {#profile-creation}

Em alguns casos, pode ser necessário enviar mensagens transacionais para perfis que não existem no sistema. Por exemplo, se um usuário desconhecido tentar redefinir a senha no seu site.

Quando um perfil não existe no banco de dados, o Journey Optimizer permite que você o crie automaticamente ao executar a campanha para permitir o envio da mensagem para esse perfil.

>[!IMPORTANT]
>
>No caso de mensagens transacionais, esse recurso é fornecido para **criação de perfil de volume muito pequeno** em um caso de uso de envio transacional de grande volume, com a maior parte dos perfis já existentes na platform.

Para ativar a criação de perfil na execução da campanha, alterne a variável **[!UICONTROL Criar novos perfis]** opção ativada no **[!UICONTROL Público]** seção. Se essa opção estiver desativada, perfis desconhecidos serão rejeitados para qualquer envio e a chamada à API falhará.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Perfis desconhecidos são criados no **Conjunto de dados do perfil de mensagens interativas do AJO** conjunto de dados, em três namespaces padrão (email, telefone e ECID) respectivamente para cada canal de saída (Email, SMS e Push).
