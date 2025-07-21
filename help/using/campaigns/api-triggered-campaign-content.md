---
solution: Journey Optimizer
product: journey optimizer
title: Editar o conteúdo da campanha acionada pela API
description: Saiba como editar o conteúdo de campanha acionada pela API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campanhas, acionadas por API, REST, otimizador, mensagens
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 2%

---


# Editar o conteúdo da campanha acionada pela API {#api-content}

Para configurar o conteúdo da mensagem, navegue até a guia **[!UICONTROL Conteúdo]** ou clique no botão **[!UICONTROL Editar conteúdo]**.

![](assets/campaign-content.png)

## Projetar o conteúdo {#design}

O processo de criação de conteúdo depende do canal selecionado. Saiba mais sobre as etapas detalhadas para criar o conteúdo da mensagem nas seguintes páginas:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="email" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>Email</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Notificação por push</strong></a></div></td>
</tr></table>

## Personalizar conteúdo usando dados contextuais {#contextual}

Você pode transmitir dados adicionais para a carga da API que você pode usar para personalizar sua mensagem.

Vejamos este exemplo, em que os clientes desejam redefinir suas senhas e você deseja enviar a eles um URL de redefinição de senha gerado em uma ferramenta de terceiros. Com campanhas acionadas por API, é possível passar esse URL gerado para a carga da API e aproveitá-lo na campanha para adicioná-lo à mensagem.

Para fazer isso, você precisa passá-los para a carga da API e adicioná-los em sua mensagem usando o editor de personalização. Use a sintaxe `{{context.<contextualAttribute>}}`, em que `<contextualAttribute>` deve corresponder ao nome da variável na carga da API que contém os dados que você deseja passar.

Observe que, por enquanto, nenhum atributo contextual está disponível para uso no menu do painel esquerdo. Os atributos devem ser digitados diretamente na sua expressão de personalização, sem que nenhuma verificação seja executada por [!DNL Journey Optimizer].

![](assets/api-triggered-context.png)

**Precisa ler**

* Os atributos contextuais passados para a solicitação não podem exceder 200 kb e são sempre considerados do tipo string.
* A sintaxe `context.system` está restrita somente ao uso interno da Adobe e não deve ser usada para transmitir atributos contextuais.
* Diferentemente dos eventos habilitados para perfis, os dados contextuais transmitidos na API REST são usados para comunicação única e não são armazenados em relação ao perfil. No máximo, o perfil é criado com os detalhes do namespace, se ele estiver ausente.
* O uso de um grande número ou de dados contextuais pesados em seu conteúdo pode afetar o desempenho.

## Testar e verificar seu conteúdo

Depois que o conteúdo for definido, use o botão **[!UICONTROL Simular conteúdo]** para visualizar e testar o conteúdo com perfis de teste ou dados de entrada de amostra carregados de um arquivo CSV/JSON ou adicionados manualmente. [Saiba como visualizar e testar o conteúdo](../content-management/preview-test.md). Para voltar para a tela de criação da campanha, clique na seta para a esquerda.

![](assets/create-campaign-design.png)

## Próximas etapas {#next}

Quando a configuração e o conteúdo da campanha estiverem prontos, você poderá definir o público da campanha. [Saiba mais](api-triggered-campaign-audience.md)
