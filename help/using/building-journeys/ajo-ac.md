---
solution: Journey Optimizer
product: journey optimizer
title: Enviar uma mensagem usando o Campaign v7/v8
description: Saiba como enviar uma mensagem usando o Campaign v7/v8
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Developer, User
level: Intermediate, Experienced
keywords: jornada, mensagem, campanha, integração
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/btOUMO8tgvwLD7kjVdgpj6I6QXRrj1iTD3P8AUrqJFM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1025
ht-degree: 0%

---

# Enviar uma mensagem com o Campaign v7/v8 {#campaign-v7-v8-use-case}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como enviar um email de uma jornada usando a integração com o Adobe Campaign v7 e v8, incluindo a criação de modelo transacional, evento e ação.

>[!ENDSHADEBOX]

Este caso de uso explica todas as etapas necessárias para enviar um email usando a integração com o [!DNL Adobe Campaign] v7 e o [!DNL Adobe Campaign] v8.

>[!NOTE]
>
>Para usar essa integração, você deve ter o Campaign v7/v8 build 9125 ou superior.

Primeiro, crie um template de email transacional no Campaign. Em seguida, no Journey Optimizer, crie o evento, a ação e crie a jornada.

Para saber mais sobre a integração do Campaign, consulte estas páginas:

* [Criar uma ação de campanha](../action/acc-action.md)
* [Usando a ação em uma jornada](../building-journeys/using-adobe-campaign-v7-v8.md).

**[!DNL Adobe Campaign]**

A instância do Campaign deve ser provisionada para essa integração. O recurso de mensagens transacionais deve ser configurado.

1. Faça logon na instância de controle do Campaign.

1. Em **Administração** > **Plataforma** > **Enumerações**, selecione a enumeração **Tipo de evento** (eventType). Crie um novo tipo de evento (&quot;jornada-evento&quot;, em nosso exemplo). Use o nome interno do tipo de evento ao gravar o arquivo JSON posteriormente.

   ![Configurar um evento em [!DNL Adobe Journey Optimizer] com seleção de esquema e campo](assets/accintegration-uc-1.png)

1. Desconecte e reconecte à instância para que a criação entre em vigor.

1. Em **Centro de Mensagens** > **Modelos de mensagens transacionais**, crie um novo modelo de email com base no tipo de evento criado anteriormente.

   ![Configuração de evento mostrando as configurações de identificador de perfil e namespace](assets/accintegration-uc-2.png)

1. Projete seu modelo. Neste exemplo, a personalização é aplicada ao nome do perfil e ao número do pedido. O nome está na fonte de dados [!DNL Adobe Experience Platform] e o número do pedido é um campo do evento Journey Optimizer. Use os nomes de campo corretos no Campaign.

   ![Visualização da carga do evento mostrando a estrutura JSON com dados de perfil e evento](assets/accintegration-uc-3.png)

1. Publique seu template transacional.

   ![Botão de cópia de evento para copiar a ID da carga para integração com a API](assets/accintegration-uc-4.png)

1. Escreva a carga JSON correspondente ao modelo.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Para o canal, é necessário digitar &quot;email&quot;.
* Para eventType, use o nome interno do tipo de evento criado anteriormente.
* O endereço de email será uma variável, para que você possa digitar qualquer rótulo.
* No ctx, os campos de personalização também são variáveis.

**Journey Optimizer**

1. Criar um evento. Inclua o campo &quot;purchaseOrderNumber&quot;.

   ![Tela de configuração de ação personalizada para a integração Clássica [!DNL Adobe Campaign]](assets/accintegration-uc-5.png)

1. Crie uma ação no Journey Optimizer correspondente ao seu template de Campanha. No menu suspenso **Tipo de ação**, selecione **[!DNL Adobe Campaign]Clássico**.

   ![Seleção de tipo de ação mostrando a opção [!DNL Adobe Campaign] Clássica](assets/accintegration-uc-6.png)

1. Clique no **campo de carga** e cole o JSON criado anteriormente.

   ![Lista suspensa de seleção de conta de campanha para integração de ações](assets/accintegration-uc-7.png)

1. Para o endereço de email e os dois campos de personalização, altere **Constante** para **Variável**.

   ![Configuração de carga de ação com mapeamento de campo para integração com o Campaign](assets/accintegration-uc-8.png)

1. Agora crie uma nova jornada e comece com o evento criado anteriormente.

   ![Jornada tela com evento e ação de campanha configurados](assets/accintegration-uc-9.png)

1. Adicione a ação e mapeie cada campo para o campo correto no Journey Optimizer.

   ![Mapeamento de parâmetro de ação com o editor de expressão para valores dinâmicos](assets/accintegration-uc-10.png)

1. Teste a jornada.

   ![Concluir o fluxo de jornadas com o disparador de eventos e a execução da ação de Campanha](assets/accintegration-uc-11.png)

1. Agora você pode publicar sua jornada.

+++ Referência de conhecimento de IA

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

* **TL;DR:** esta página fornece um caso de uso passo a passo para enviar um email transacional do Adobe Journey Optimizer usando a integração com o Adobe Campaign v7/v8, abordando a criação de modelo de campanha, configuração de evento e ação e design de jornada.

**Intenções:**
* Configurar um template de email transacional no Adobe Campaign v7/v8 para uso com o Journey Optimizer
* Crie um evento no Journey Optimizer que inclua campos personalizados, como um número de ordem de compra
* Criar e configurar uma ação do Campaign Classic no Journey Optimizer com uma carga JSON
* Mapear campos de evento de jornada para variáveis de personalização de Campanha na configuração da ação
* Criar e publicar uma jornada que aciona um email transacional do Campaign

**Glossário:**
* **Mensagens transacionais**: um recurso do Campaign que envia emails acionados em tempo real com base em eventos; deve ser configurado antes que essa integração possa ser usada *(específico do produto)*
* **Tipo de evento (eventType)**: um valor de enumeração definido no Campaign que identifica o tipo de evento transacional; seu nome interno é referenciado na carga JSON *(específico do produto)*
* **Ação do Campaign Classic**: um tipo de ação do Journey Optimizer que se conecta ao Adobe Campaign v7/v8 para enviar mensagens transacionais *(específico do produto)*
* **Campo de carga**: a estrutura JSON colada em uma ação do Journey Optimizer que define os campos de dados enviados para a Campanha *(específico do produto)*

**Medidas de Proteção:**
* A build 9125 ou superior do Campaign v7/v8 é necessária para essa integração
* O recurso Mensagens transacionais deve ser configurado na instância do Campaign antes do uso
* Depois de criar um novo tipo de evento no Campaign, você deve se desconectar e reconectar à instância para que ela entre em vigor
* Os valores de campo do Personalization definidos como &quot;Constante&quot; na ação devem ser alterados para &quot;Variável&quot; para permitir a população dinâmica no tempo de execução

**Terminologia:**
* Nome canônico: Adobe Campaign v7/v8 — Acrônimo: ACC — variantes: Campaign Classic, Campaign v7, Campaign v8
* Sinônimos: &quot;eventType&quot; = &quot;nome interno do tipo de evento&quot;
* Não confunda: &quot;Campaign Classic action&quot; ≠ &quot;custom action&quot; (a ação do Campaign Classic é um tipo de ação incorporada específico para integração com o ACC)

**Perguntas frequentes:**
* **P: Qual versão do Campaign é necessária para essa integração?** — O Campaign v7/v8 build 9125 ou superior é necessário.
* **P: O que deve ser configurado no Campaign antes de iniciar?** — O recurso de mensagens transacionais deve ser configurado e um template de email transacional deve ser criado com base no tipo de evento.
* **P: Como faço para tornar os campos de personalização dinâmicos na ação do Journey Optimizer?** — Na configuração da carga de ação, altere a configuração do campo de &quot;Constante&quot; para &quot;Variável&quot; para campos que serão preenchidos no tempo de execução.
* **P: De onde vêm os dados de personalização de nome neste caso de uso?** — O nome vem da fonte de dados do Adobe Experience Platform, enquanto o número do pedido vem da carga útil do evento do Journey Optimizer.
* **P: Como conectar a ação do Journey Optimizer ao modelo de campanha?** — Selecione &quot;Adobe Campaign Classic&quot; como o Tipo de ação e cole a carga JSON que corresponde à estrutura do modelo de mensagem transacional.

+++
