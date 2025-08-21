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
badge: label="Disponibilidade limitada" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: c62653af3c1eacaaf55dcf181d33f2253521e33d
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 12%

---

# Exportar conteúdo da mensagem {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Reter e exportar o conteúdo enviado"
>abstract="Selecionar esta opção permite gravar o conteúdo dos emails ou mensagens SMS enviados, utilizando-se esta configuração, em um conjunto de dados [!DNL Experience Platform]. Os registros são retidos por três dias corridos, durante os quais podem ser exportados para o seu próprio armazenamento."

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível apenas para algumas organizações (disponibilidade limitada). Para obter mais informações, entre em contato com o representante da Adobe.

A **Exportação de Mensagens** permite transferir o conteúdo de mensagens de email e SMS enviadas do [!DNL Journey Optimizer] para seu próprio armazenamento por meio de destinos do [!DNL Adobe Experience Platform], que permitem entregar dados do [!DNL Experience Platform] para pontos de extremidade externos. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/home){target="_blank"}

Com este recurso, o conteúdo de mensagens de email e SMS enviadas por [!DNL Journey Optimizer] que foram marcadas para exportação são gravadas no [!DNL Experience Platform] **Conjunto de Dados de Exportação de Mensagens do AJO**.

Os registros são mantidos no **Conjunto de Dados de Exportação de Mensagens do AJO** por três dias, durante os quais você pode exportá-los para o sistema externo de sua escolha.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## Medidas de proteção

* Esse recurso só é compatível com os canais de email e SMS.
* Os registros no conjunto de dados de exportação de mensagens do AJO são retidos por três dias corridos a partir da assimilação.
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
   * Programar: verifique se ele é executado dentro da janela de retenção de 3 dias.

### Ativar Exportação de mensagens na configuração do canal {#config-message-export}

Para aplicar a Exportação de mensagens às suas campanhas e jornadas, é necessário habilitar a opção dedicada no nível de configuração do canal. Siga as etapas abaixo.

1. Em [!DNL Journey Optimizer], edite ou crie a [configuração de canal](channel-surfaces.md#create-channel-surface) de email ou SMS desejada.

1. Selecione a opção **[!UICONTROL Habilitar Exportação de Mensagem]**.

   ![](assets/config-message-export.png)

1. Salve as alterações e envie a configuração do canal.

Mensagens de email e SMS enviadas por campanhas ou jornadas usando esta configuração de canal são gravadas no **Conjunto de Dados de Exportação de Mensagens do AJO**. Os registros são exportados para o destino de armazenamento selecionado com base no fluxo de dados de exportação definido.

A desabilitação da opção **[!UICONTROL Habilitar Exportação de Mensagem]** impede que novos registros desta configuração de canal sejam assimilados no conjunto de dados. Os registros existentes permanecem até que a retenção expire.
