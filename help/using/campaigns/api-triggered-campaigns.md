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
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 3%

---

# Acione campanhas usando APIs {#trigger-campaigns}

## Sobre campanhas acionadas por API {#about}

Com [!DNL Journey Optimizer], você pode criar campanhas e depois invocá-las de um sistema externo com base no acionador do usuário usando a [API REST de Execução de Mensagens Interativas](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Isso permite cobrir várias necessidades de mensagens operacionais e transacionais, como redefinições de senha, token OTP, entre outras.

Para fazer isso, primeiro crie uma campanha acionada por API no Journey Optimizer e, em seguida, inicie a execução por meio de uma chamada de API.

Os canais disponíveis para campanhas acionadas por API são mensagens de email, SMS e push.

## Criar uma campanha acionada por API {#create}

### Configurar e ativar a campanha {#create-activate}

O processo para criar campanhas acionadas por API permanece o mesmo que as campanhas programadas, exceto pela seleção de público-alvo que é executada na carga da API. Informações detalhadas sobre como criar uma campanha estão disponíveis em [esta seção](create-campaign.md).

Para criar uma campanha acionada por API, siga estas etapas:

1. Crie uma nova campanha com a **[!UICONTROL Acionado por API]** tipo .

1. Escolha o canal e a superfície do canal a serem usados para enviar a mensagem e clique em **[!UICONTROL Criar]**.

   ![](assets/api-triggered-type.png)

1. Especifique um título e uma descrição para a campanha, em seguida, clique em **[!UICONTROL Editar conteúdo]** para configurar a mensagem a ser enviada.

   >[!NOTE]
   >
   >Você pode transmitir dados adicionais para a carga da API que pode ser usada para personalizar a mensagem. [Saiba mais](#contextual)
   >
   >Usar um grande número ou dados contextuais pesados em seu conteúdo pode afetar o desempenho.

1. No **[!UICONTROL Público]** , especifique o namespace a ser usado para identificar os indivíduos do segmento.

   O **[!UICONTROL Criar novos perfis]** permite criar automaticamente perfis que não existem no banco de dados. [Saiba mais sobre a criação de perfil na execução da campanha](#profile-creation)

1. Configure as datas de início e término da campanha.

   Se você configurar uma data de início e/ou término específica para uma campanha, ela não será executada fora dessas datas, e as chamadas de API falharão se a campanha for acionada pelas APIs.

1. Clique em **[!UICONTROL Revisar para ativar]** para verificar se a campanha está configurada corretamente, ative-a.

Agora você está pronto para executar a campanha a partir das APIs. [Saiba mais](#execute)

### Executar a campanha {#execute}

Depois que a campanha tiver sido ativada, é necessário recuperar a solicitação de cURL de amostra gerada e usá-la na API para criar a carga útil e acionar a campanha.

1. Abra a campanha e copie e cole a solicitação de amostra do **[!UICONTROL Solicitação cURL]** seção.

   ![](assets/api-triggered-curl.png)

1. Use essa solicitação de cURL nas APIs para criar sua carga e acionar a campanha. Para obter mais informações, consulte [Documentação da API de execução de mensagem interativa](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   >[!NOTE]
   >
   >Se você configurou uma data de início e/ou término específica ao criar a campanha, ela não será executada fora dessas datas, e as chamadas de API falharão.

## Usar atributos contextuais em campanhas acionadas por API {#contextual}

Com campanhas acionadas por API, você pode passar dados adicionais na carga da API e usá-los dentro da campanha para personalizar sua mensagem.

Vejamos este exemplo, onde os clientes desejam redefinir a senha e você deseja enviar a eles um URL de redefinição de senha gerado em uma ferramenta de terceiros. Com campanhas acionadas por API, você pode passar esse URL gerado para a carga da API e aproveitá-lo para a campanha para adicioná-lo à mensagem.

>[!NOTE]
>
>Diferentemente dos eventos ativados por perfil, os dados contextuais transmitidos na API REST são usados para comunicação pontual e não armazenados em relação ao perfil. No máximo, o perfil é criado com os detalhes do namespace, caso ele tenha sido encontrado ausente.

Para usar esses dados em suas campanhas, é necessário passá-los para a carga da API e adicioná-los em sua mensagem usando o editor de expressão. Para fazer isso, use o `{{context.<contextualAttribute>}}` sintaxe, em que `<contextualAttribute>` deve corresponder ao nome da variável no payload da API que contém os dados que você deseja transmitir.

O `{{context.<contextualAttribute>}}` A sintaxe é mapeada somente para um tipo de dados String .

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>Os atributos contextuais transmitidos para a solicitação não podem exceder 50 kb.
>
>O `context.system` A sintaxe é restrita somente ao uso interno do Adobe e não deve ser usada para transmitir atributos contextuais.

Observe que, por enquanto, nenhum atributo contextual está disponível para uso no menu do painel à esquerda. Os atributos devem ser digitados diretamente na expressão de personalização, sem que nenhuma verificação seja executada por [!DNL Journey Optimizer].

## Criação de perfil na execução da campanha {#profile-creation}

Em alguns casos, pode ser necessário enviar mensagens transacionais para perfis que não existem no sistema. Por exemplo, se um usuário desconhecido tentar redefinir a senha em seu site.

Quando um perfil não existe no banco de dados, o Journey Optimizer permite que você o crie automaticamente ao executar a campanha para permitir o envio da mensagem para esse perfil.

>[!IMPORTANT]
>
>Este recurso é fornecido para **criação de perfil de volume muito pequeno** em um caso de uso de envio transacional de grande volume, com a maior parte dos perfis já existentes na plataforma.

Para ativar a criação de perfil na execução da campanha, alterne a **[!UICONTROL Criar novos perfis]** na opção **[!UICONTROL Público]** seção.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Os perfis desconhecidos são criados na **Conjunto de dados do perfil de mensagens interativas AJO** conjunto de dados, em três namespace padrão (email, telefone e ECID), respectivamente, para cada canal de saída (Email, SMS e Push).
