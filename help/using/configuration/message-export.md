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
TQID: https://experienceleague.adobe.com/4i6dFByqNizhrMeQrr32twEPVrg4Jz8J-rgA-sR70Ho
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 1431
ht-degree: 6%

---

# Exportar conteúdo da mensagem {#message-export}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba como habilitar a Exportação de Mensagens nas configurações de canal de email e SMS para gravar conteúdo de mensagens enviadas em um conjunto de dados do Adobe Experience Platform e transferi-lo para seu próprio armazenamento.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Reter e exportar o conteúdo enviado"
>abstract="Selecionar essa opção permite gravar o conteúdo do email ou das mensagens SMS enviadas usando essa configuração em um conjunto de dados da [!DNL Experience Platform]. Os registros são retidos por sete dias corridos a partir da ingestão, durante os quais você pode exportá-los para o seu armazenamento."

>[!AVAILABILITY]
>
>Esse recurso está disponível apenas para os canais de email e SMS, para organizações que adquiriram o complemento de Exportação de mensagem. Para obter mais informações, entre em contato com o(a) representante da Adobe.

A **Exportação de Mensagens** permite transferir o conteúdo de mensagens de email e SMS enviadas de [!DNL Journey Optimizer] para seu próprio armazenamento por meio de [[!DNL Adobe Experience Platform] destinos](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/home){target="_blank"}, que permitem entregar dados do [!DNL Experience Platform] para pontos de extremidade externos.

Com este recurso, o conteúdo de mensagens de email e SMS enviadas por [!DNL Journey Optimizer] que foram marcadas para exportação são gravadas no [!DNL Experience Platform] [Conjunto de Dados de Exportação de Mensagens do AJO](message-export-schema.md).

Os registros são retidos no conjunto de dados por sete dias a partir da assimilação, durante os quais você pode exportá-los para o sistema externo de sua escolha.

➡️ Para perguntas e respostas comuns, consulte as [Perguntas frequentes sobre Exportação de Mensagens](#message-export-faq).

## Medidas de proteção

* Este recurso só oferece suporte aos canais de **Email** e **SMS**.
* Os registros no Conjunto de dados de exportação de mensagens do AJO são retidos **por sete dias** a partir da assimilação.
* O preenchimento retroativo não é compatível com mensagens enviadas antes de ativar a Exportação de mensagens, conforme descrito abaixo.

## Ativar exportação de mensagens {#enable-message-export}

O processo de integração do recurso Exportação de mensagens consiste em duas etapas:

1. [Configurar o fluxo de dados de exportação](#set-up-export-dataflow) em [!DNL Experience Platform];
1. [Habilitar Exportação de Mensagem](#config-message-export) na configuração de canal em [!DNL Journey Optimizer].

>[!WARNING]
>
>Somente novos registros após a ativação de exportações e o envio de mensagens serão exibidos. Não há suporte para preenchimentos retroativos de conteúdo antes de configurar o processo de exportação e ativar a opção Exportar mensagem.

### Configurar o fluxo de dados de exportação {#set-up-export-dataflow}

Antes de poder exportar seus dados, configure o processo de exportação definindo o destino [!DNL Experience Platform] e o fluxo de exportação do conjunto de dados.

Para obter etapas detalhadas, destinos na nuvem com suporte, permissões necessárias e mais informações, consulte [esta seção](../data/export-datasets.md#export-datasets).

>[!NOTE]
>
>Essa configuração deve ser definida para cada sandbox.

1. Escolha um [tipo de destino](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/destination-types){target="_blank"} do Experience Platform. Uma lista de plataformas de destino disponíveis que estão prontas para receber dados está disponível em [esta página](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. No [!DNL Experience Platform], configure seu destino definindo credenciais, bucket/container, prefixo de caminho e opções de segurança. [Saiba como](https://experienceleague.adobe.com/pt-br/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Crie um fluxo de exportação do conjunto de dados usando os seguintes dados:

   * Conjunto de dados do Source: selecione **Conjunto de dados de exportação de mensagens do AJO**.
   * Formato de arquivo: selecione JSON ou Parquet (escolha um com base nas ferramentas downstream).
   * Programar: verifique se ele é executado dentro da janela de retenção de 7 dias.

### Ativar exportação de mensagens na configuração do canal {#config-message-export}

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

➡️ Para obter uma visão completa da estrutura do conjunto de dados e de todos os campos disponíveis, consulte o [esquema de Exportação de Mensagens do AJO](message-export-schema.md).

Todos os registros no conjunto de dados são retidos por **sete dias** a partir da assimilação. Durante esse período de retenção, você pode acessar os dados para auditorias de conformidade, consultas legais ou exportá-los para o seu próprio sistema de armazenamento por meio do destino Experience Platform configurado.

## Amostra do JSON exportado {#sample-exported-json}

Os exemplos abaixo mostram a forma geral dos registros gravados no Conjunto de dados de exportação de mensagens do AJO para SMS e email. Valores como identificadores, referências de esquema, carimbos de data e hora e conteúdo são ilustrativos; suas exportações refletem sua sandbox, esquema e mensagens enviadas.

Expanda cada seção para visualizar a amostra completa JSON.

+++ Exemplo de exportação de SMS

```json
{
  "header": {
    "msgId": "f06d2a6d-65c3-472b-9ca7-cc4224af2df4",
    "xactionId": "9ccd6e76-9ee5-4a12-bff3-fea240228121",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "906E3A095DC834230A495FD6@AdobeOrg",
    "sandboxId": "db3adc95-dcf6-49c3-badc-95dcf639c345",
    "sandboxName": "ajo-e2e",
    "createdAt": 1773591102107,
    "datasetId": "689653509dd3432b92f6323f",
    "schemaRef": {
      "id": "https://ns.adobe.com/aemonacpprodcampaign/schemas/64cb5d9d26c2aae6b08bdc9b7882deb90202439ec53836e7",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1773591102107,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "CSM-09561055",
            "messageID": "15fe77c8-ab73-49e4-abbb-c25b859162ff-0",
            "messageType": "marketing",
            "campaignID": "5638ce57-5264-4a96-995f-5ae34eddafd7",
            "campaignVersionID": "f9019155-3d6a-44a1-9b6f-5f9cd49e7cf5",
            "campaignActionID": "dfa7f59f-477c-42ec-9db2-831d294b5779",
            "batchInstanceID": "5e23a286fb72411f1cdf1443a81ad2eb",
            "messagePublicationID": "15fe77c8-ab73-49e4-abbb-c25b859162ff",
            "audience": {
              "id": "4c339f63-b66e-4e72-8d56-db624b5277f2",
              "type": "targeted"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/sms",
              "_type": "https://ns.adobe.com/xdm/channel-types/sms"
            },
            "messageProfileID": "7ff5aefb-7583-38c4-8c32-b63cced94aa7",
            "variant": "5c1092da-5ba2-4bcc-b591-713ee7999f7d"
          },
          "messageRenderedContent": {
            "smsContent": {
              "message": "AJO Campaigns - Prod - E2E Test Text VA7"
            }
          },
          "messageDeliveryMetadata": {
            "smsMetadata": {
              "recipient": {
                "number": "+19256260201"
              },
              "sender": {
                "numbers": [
                  "12345678"
                ]
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "rlyajoqa+messageExport1@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "b0001846-cafa-379a-be96-1d8ee973e047",
      "timestamp": "2026-03-15T16:11:42.184Z"
    }
  }
}
```

+++

+++ Exemplo de exportação de email

```json
{
  "header": {
    "msgId": "1e64d2c4-7887-4f80-8b28-5c20d3da8baf",
    "xactionId": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "745F37C35E4B776E0A49421B@AdobeOrg",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "sandboxName": "prod",
    "createdAt": 1754489661211,
    "datasetId": "68912b8881572a2b267380c1",
    "schemaRef": {
      "id": "https://ns.adobe.com/cjmstage/schemas/1684477c0160376b8bb6975a80b5e5bd384696329faa1c42",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1754489659000,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "HUMA-62208933",
            "messageID": "d0d02f68-afea-42fc-b898-6819cee643e6-0",
            "messageType": "transactional",
            "campaignID": "ce2331c2-c259-47ff-a1dd-f6d1eae08801",
            "campaignVersionID": "4272bb9f-e154-44e9-89f1-6548c77d1455",
            "batchInstanceID": "03587190-72cf-11f0-938b-31e7c9f96d89",
            "messagePublicationID": "d0d02f68-afea-42fc-b898-6819cee643e6",
            "audience": {
              "type": "all"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/email",
              "_type": "https://ns.adobe.com/xdm/channel-types/email"
            },
            "messageProfileID": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
            "variant": "11cc5796-8017-4738-aa66-ca5db967dfcc"
          },
          "messageRenderedContent": {
            "emailContent": {
              "subject": "test",
              "html": "xxx"
            }
          },
          "messageDeliveryMetadata": {
            "emailMetadata": {
              "recipient": {
                "email": "himanshig@adobe.com"
              },
              "sender": {
                "email": "cjm-team@e2e-personalisation.test.cjmadobe.com",
                "name": "CJM team",
                "replyToEmail": "replyto@marketing.adobecjm.com",
                "replyToName": "replyto",
                "errorEmail": "replyto@e2e-personalisation.test.cjmadobe.com"
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "chijain@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "ea48ce1b-80c9-3c6a-b05f-d1c998989e02",
      "timestamp": "2025-08-06T14:14:22.814Z"
    }
  }
}
```

+++

## Perguntas frequentes sobre exportação de mensagens {#message-export-faq}

+++ O que é Exportação de mensagens?

A Exportação de mensagens permite que os clientes exportem mensagens totalmente renderizadas (Email e SMS) que foram enviadas para usuários finais. Os dados exportados podem ser entregues a destinos externos usando recursos de exportação padrão do [!DNL Adobe Experience Platform] (AEP) e usados para fins como arquivamento, revisão de conformidade, análise ou integrações downstream.

+++

+++ Quais canais são compatíveis?

A Exportação de mensagens oferece suporte a:

* Email
* SMS

+++

+++ Quais dados são gerados pela Exportação de Mensagens?

A Exportação de Mensagem cria um conjunto de dados gerado pelo sistema em [!DNL Adobe Experience Platform] que contém um instantâneo da mensagem no momento do envio. Esse conjunto de dados pode ser exportado para destinos compatíveis (por exemplo, armazenamento em nuvem ou sistemas de terceiros).

A exportação de mensagens foi projetada como um mecanismo de habilitação para que os clientes retirem os dados de mensagens dos sistemas Adobe — os clientes são responsáveis por transformar, armazenar e gerenciar os dados em suas próprias soluções de arquivamento ou de conformidade.

+++

+++ A Exportação de mensagens captura mensagens totalmente personalizadas?

Sim. A exportação de mensagens captura a mensagem totalmente renderizada que foi enviada para cada recipient, incluindo personalização e conteúdo dinâmico como renderizado no momento do envio.

+++

+++ A Exportação de mensagens pode ser usada para reproduzir a mensagem original?

Sim. O HTML exportado pode ser usado para reproduzir a mensagem enviada original em um navegador.

No entanto, a reprodução depende da disponibilidade de ativos hospedados externamente (como imagens). A Exportação de mensagem não incorpora arquivos de mídia diretamente na exportação.

+++

+++ As imagens e a mídia estão incluídas na exportação?

A Exportação de mensagens inclui conteúdo do HTML com referências (URLs) a imagens e outras mídias. Os ativos de mídia não estão incorporados à exportação.

Se um URL de imagem ou ativo se tornar inválido, restrito ou não publicado após o tempo de envio, a Exportação de mensagem não poderá recuperar esse ativo.

+++

+++ Como os links são tratados na Exportação de mensagens?

As mensagens exportadas contêm links rastreados criptografados, consistentes com a maneira como os links são tratados no momento do envio. Esses links criptografados são preservados na exportação e podem ser resolvidos conforme projetado pela plataforma.

+++

+++ Como os dados de PII e personalização são tratados?

Os dados são armazenados exatamente como aparecem na mensagem renderizada:

* Os valores de Personalization renderizados na mensagem (por exemplo, nome) são exibidos como texto.
* Os elementos criptografados (como links rastreados) permanecem criptografados.
* A Exportação de mensagens não anonimiza ou redige automaticamente o conteúdo de mensagens renderizadas.

+++

+++ Qual é o período de retenção dos dados de Exportação de mensagens?

Os dados de Exportação de Mensagem seguem uma janela de retenção de 7 dias em [!DNL Adobe Experience Platform].

Os clientes devem exportar os dados dentro desse período e armazená-los em seus próprios sistemas se for necessária uma retenção mais longa.

+++

+++ Os clientes podem testar a Exportação de mensagens antes de comprar?

Não há uma avaliação ou opção de &quot;experimentar antes de comprar&quot; para a Exportação de mensagens.

Os clientes podem validar seus sistemas downstream usando arquivos de exportação de amostra, já que a Exportação de mensagens depende do conjunto de dados padrão da AEP e da funcionalidade de destino.

+++

+++ O esquema Exportação de mensagens está disponível antes da compra?

Não. O conjunto de dados e o esquema Exportação de mensagens ficam disponíveis no produto somente após o complemento Exportação de mensagens ser comprado e habilitado.

+++

+++ A Exportação de mensagens é uma solução completa de arquivamento ou conformidade?

Não. A exportação de mensagens é um ativador, não um produto de arquivamento completo ou de conformidade.

Espera-se que os clientes:

* Exportar dados de mensagem do Adobe
* Transformar ou enriquecer conforme necessário
* Armazenar e gerenciar os dados em seus próprios sistemas de arquivamento ou de conformidade

+++

+++ Quais são os casos de uso comuns?

Os clientes normalmente usam a Exportação de mensagens para:

* Revisão regulamentar ou de conformidade
* Arquivamento de mensagens
* Integração com sistemas de terceiros
* Workflows de auditoria interna ou suporte
* Analytics além dos aplicativos da Adobe

+++

+++ O que a exportação de mensagens não faz

A exportação de mensagens não:

* Incorporar imagens externas ou ativos de mídia
* Fornecer retenção de dados ilimitada ou a longo prazo em sistemas Adobe
* Oferecer um ambiente de avaliação
* Arquivar automaticamente mensagens fora do Adobe

+++

