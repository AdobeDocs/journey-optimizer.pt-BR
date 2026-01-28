---
solution: Journey Optimizer
product: journey optimizer
title: Exportação de mensagens no Journey Optimizer
description: Saiba como exportar mensagens
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportação, mensagens, HIPAA, emails, SMS, configuração
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: ab0f100d53cb987919eb134442bf05e64c30719a
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 3%

---

# Exportar conteúdo da mensagem {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Reter e exportar o conteúdo enviado"
>abstract="Selecionar essa opção permite gravar o conteúdo do email ou das mensagens SMS enviadas usando essa configuração em um conjunto de dados [!DNL Experience Platform]. Os registros são retidos por 7 dias a partir da assimilação, durante os quais você pode exportá-los para seu próprio armazenamento."

>[!AVAILABILITY]
>
>Esse recurso só está disponível para o canal de email e SMS, para organizações que compraram a oferta complementar Exportação de mensagens. Para obter mais informações, entre em contato com o seu representante da Adobe.

A **Exportação de Mensagens** permite transferir o conteúdo de mensagens de email e SMS enviadas do [!DNL Journey Optimizer] para seu próprio armazenamento por meio de destinos do [!DNL Adobe Experience Platform], que permitem que você forneça dados do [!DNL Experience Platform] para endpoints externos. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/home){target="_blank"}

Com este recurso, o conteúdo de mensagens de email e SMS enviadas por [!DNL Journey Optimizer] que foram marcadas para exportação são gravadas no [!DNL Experience Platform] **Conjunto de Dados de Exportação de Mensagens do AJO**. [Saiba mais sobre conjuntos de dados](../data/get-started-datasets.md)

Os registros são retidos no conjunto de dados por sete dias a partir da assimilação, durante os quais você pode exportá-los para o sistema externo de sua escolha.

## Medidas de proteção

* Este recurso só oferece suporte aos canais de **Email** e **SMS**.
* Os registros no Conjunto de dados de exportação de mensagens do AJO são retidos **por sete dias a partir da assimilação**.
* O preenchimento retroativo não é compatível com mensagens enviadas antes de ativar a Exportação de mensagens, conforme descrito abaixo.

## Ativar exportação de mensagens {#enable-message-export}

O processo de integração do recurso Exportação de mensagens consiste em duas etapas:

1. [Configurar o fluxo de dados de exportação](#set-up-export-dataflow) em [!DNL Experience Platform];
1. [Habilitar Exportação de Mensagem](#config-message-export) na configuração de canal em [!DNL Journey Optimizer].

>[!WARNING]
>
>Somente novos registros após a ativação de exportações e o envio de mensagens serão exibidos. Não há suporte para preenchimentos retroativos de conteúdo antes de configurar o processo de exportação e ativar a opção Exportar mensagem.

### Configurar o fluxo de dados de exportação {#set-up-export-dataflow}

Antes de poder exportar seus dados, você deve configurar o processo de exportação definindo o destino [!DNL Experience Platform] e o conjunto de dados que será usado. Siga as etapas abaixo.

>[!NOTE]
>
>Essa configuração deve ser definida para cada sandbox.

1. Escolha um [tipo de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types){target="_blank"} do Experience Platform. Uma lista de plataformas de destino disponíveis que estão prontas para receber dados está disponível em [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. No [!DNL Experience Platform], configure seu destino definindo credenciais, bucket/container, prefixo de caminho e opções de segurança. [Saiba como](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Crie um fluxo de exportação do conjunto de dados usando os seguintes dados:

   * Conjunto de dados do Source: selecione **Conjunto de dados de exportação de mensagens do AJO**.
   * Formato de arquivo: selecione JSON ou Parquet (escolha um com base nas ferramentas downstream).
   * Programar: verifique se ele é executado dentro da janela de retenção de 7 dias.

### Ativar Exportação de mensagens na configuração do canal {#config-message-export}

Para aplicar a Exportação de mensagens às suas campanhas e jornadas, é necessário habilitar a opção dedicada no nível de configuração do canal. Siga as etapas abaixo.

1. Em [!DNL Journey Optimizer], edite ou crie a [configuração de canal](channel-surfaces.md#create-channel-surface) de email ou SMS desejada.

1. Selecione a opção **[!UICONTROL Habilitar Exportação de Mensagem]**.

   ![](assets/config-message-export.png)

1. Salve as alterações e envie a configuração do canal.

Depois de enviar mensagens por meio de campanhas ou jornadas usando esta configuração de canal, as mensagens de email e SMS serão gravadas no **Conjunto de Dados de Exportação de Mensagens do AJO**. Em seguida, você pode [acessar os registros](#access-exported-data) no conjunto de dados e exportá-los para o destino de armazenamento selecionado com base no fluxo de dados de exportação definido.

>[!NOTE]
>
>A desabilitação da opção **[!UICONTROL Habilitar Exportação de Mensagem]** impede que novos registros desta configuração de canal sejam assimilados no conjunto de dados. Os registros existentes permanecem até que a retenção expire.

## Acessar dados de mensagem exportados {#access-exported-data}

Depois que as mensagens forem enviadas usando uma configuração de canal com a Exportação de Mensagens habilitada, você poderá acessar e revisar os dados exportados no **Conjunto de Dados de Exportação de Mensagens do AJO**.

Para exibir os dados de mensagem exportados:

1. Em [!DNL Journey Optimizer], navegue até **[!UICONTROL Gerenciamento de dados]** > **[!UICONTROL Conjuntos de dados]** na navegação à esquerda. [Saiba mais sobre conjuntos de dados](../data/get-started-datasets.md)

1. Certifique-se de exibir conjuntos de dados gerados pelo sistema.

1. Selecione o **Conjunto de dados de exportação de mensagens do AJO** na lista.

   ![](assets/datasets-list.png)

1. Na página de detalhes do conjunto de dados, clique em **[!UICONTROL Visualizar conjunto de dados]** para exibir os registros mais recentes.

   ![](assets/ajo-message-export-dataset.png)

O conjunto de dados contém informações abrangentes para cada mensagem enviada pela configuração de canal com a Exportação de mensagens ativada, incluindo: linha de assunto, corpo da mensagem, endereço de email ou número de telefone do recipient, endereço ou número de telefone do remetente, data e hora do envio, dados de personalização e muito mais.

Todos os registros no conjunto de dados são retidos por **sete dias a partir da assimilação**. Durante esse período de retenção, você pode acessar os dados para auditorias de conformidade, consultas legais ou exportá-los para o seu próprio sistema de armazenamento por meio do destino Experience Platform configurado.

