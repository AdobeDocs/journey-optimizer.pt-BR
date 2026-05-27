---
solution: Journey Optimizer
product: journey optimizer
title: Verificar e testar suas mensagens do WhatsApp
description: Saiba como verificar e enviar suas mensagens do WhatsApp no Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 1ed76bda056ea59a11a6133e83934bfc47ccb4e9
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 2%

---

# Verificar e enviar mensagens do WhatsApp {#send-whatsapp}

## Pré-visualizar sua mensagem do WhatsApp {#preview-whatsapp}

Depois que o conteúdo da mensagem for definido, você poderá usar perfis de teste ou dados de entrada de amostra carregados de um arquivo CSV/JSON ou adicionados manualmente para visualizar seu conteúdo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** e verifique sua mensagem usando os dados do perfil de teste.

Informações detalhadas sobre como visualizar e testar o conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

## Validar seu conteúdo {#whatsapp-validate}

Você deve verificar os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem ocorrer: avisos e erros.

* **Os avisos** referem-se às recomendações e práticas recomendadas. Por exemplo, uma mensagem de aviso será exibida se a mensagem de texto estiver vazia.

* **Erros** impedem que você teste ou ative a jornada, ou publique a campanha, desde que não sejam resolvidos. Por exemplo, uma mensagem de erro avisa quando a linha de assunto está ausente.

## Envie suas mensagens do WhatsApp {#whatsapp-send}

>[!IMPORTANT]
>
> Se sua campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para poder enviar suas mensagens de texto. [Saiba mais](../test-approve/gs-approval.md)

Quando a mensagem do WhatsApp estiver pronta, conclua a configuração da [jornada](../building-journeys/publish-journey.md) ou da [campanha](../campaigns/review-activate-campaign.md) para enviá-la.

## Analisar interações do WhatsApp {#whatsapp-channel-context}

O Journey Optimizer captura dados adicionais de interação retornados do canal do WhatsApp e os armazena no **Conjunto de Dados de Relatórios - Evento de Experiência de Rastreamento de Email** no grupo de campos `whatsAppChannelContext`. Use estes campos para compilar [públicos-alvo](../audience/about-audiences.md), executar [consultas](../data/get-started-queries.md) e analisar o engajamento no WhatsApp. [Saiba mais sobre conjuntos de dados do sistema](../data/get-started-datasets.md#system-datasets).

Os seguintes campos são capturados:

| Campo | Descrição |
|-|-|
| `messageType` | Tipo de mensagem do WhatsApp (por exemplo, `templateBased`, `response`). |
| `inboundMessage` | Conteúdo de resposta de entrada (por exemplo, `stop`, `start`, `subscribe`). |
| `inboundNumber` | ID do remetente em que a mensagem de entrada foi recebida. |
| `channelType` | Categoria de canal (`Utility`, `Marketing` ou `Promotional`). |
| `profileNumber` | Número de telefone do qual a mensagem de entrada foi recebida. |
| `origTimestamp` | Carimbo de data e hora original do Meta/WhatsApp. |
| `status` | Status da entrega incluindo feedback de provedor padronizado (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` ou `unknown`) e a mensagem de status de provedor bruto. |
| `reactionEvent` | Conteúdo da resposta do usuário: emoji para reações ou texto da mensagem para respostas a uma mensagem específica. |
| `reactionMessageID` | ID da mensagem original que está sendo respondida. |
| `reactionActionName` | Tipo de ação de resposta (`react`, `unreact` ou `reply`). |
| `interactiveSelectedTitle` | Título selecionado pelo usuário em uma mensagem interativa do WhatsApp. |
| `interactiveType` | Tipo de mensagem interativa (`list reply`, `button reply` ou `button`). |
| `interactiveSelectedDescription` | Descrição da opção interativa do WhatsApp selecionada. |
| `interactiveSelectedID` | ID da opção selecionada no WhatsApp. |

Para consultar esse conjunto de dados, use a tabela `ajo_email_tracking_experience_event_dataset` no Serviço de consulta. Para padrões de consulta e casos de uso relacionados, consulte [exemplos de consulta de conjunto de dados](../data/datasets-query-examples.md).
