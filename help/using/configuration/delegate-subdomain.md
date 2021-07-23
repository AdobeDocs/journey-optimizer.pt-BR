---
title: Delegar subdomínios
description: Saiba como delegar subdomínios
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Configurações do aplicativo
topic: Administração
role: Admin
level: Intermediate
source-git-commit: 29ebb0d8ba228ee8bf430d29f92cc30a9edac69a
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 9%

---


# Delegar um subdomínio

A delegação de nome de domínio é um método que permite ao proprietário de um nome de domínio (tecnicamente: uma zona DNS) para delegar uma subdivisão dessa zona (tecnicamente: uma zona DNS sob ela, que pode ser chamada de subzona) para outra entidade. Basicamente, se um cliente estiver lidando com a zona &quot;example.com&quot;, ele poderá delegar a subzona &quot;marketing.example.com&quot; ao Adobe.

Ao delegar um subdomínio para uso com [!DNL Journey Optimizer], os clientes podem depender do Adobe para manter a infraestrutura de DNS necessária para atender aos requisitos de deliverability padrão do setor para seus domínios de envio de marketing de email, enquanto continuam a manter e controlar o DNS para seus domínios de email internos.

[!DNL Journey Optimizer] O permite delegar totalmente seus subdomínios ao Adobe diretamente da interface do produto. Com isso, o Adobe poderá enviar mensagens como um serviço gerenciado controlando e mantendo todos os aspectos do DNS necessários para fornecer, renderizar e rastrear campanhas de email.

>[!NOTE]
>
>Por padrão, o [!DNL Journey Optimizer] contrato de licença permite delegar até 10 subdomínios. Entre em contato com o Adobe se quiser aumentar essa limitação.
>
>No momento, o uso de CNAMEs para delegação de subdomínio não é compatível com o Journey Optimizer.

Para delegar um novo subdomínio, siga as etapas abaixo:

1. Acesse o menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** e clique em **[!UICONTROL Delegate subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. Especifique o nome do subdomínio que será delegado.

   ![](../assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Não é permitido delegar um subdomínio inválido para Adobe. Certifique-se de inserir um subdomínio válido que seja de propriedade de sua organização, como marketing.suaempresa.com.
   >
   >Observe que subdomínios de vários níveis, como email.marketing.suaempresa.com, não são suportados no momento.

1. A lista de registros que serão colocados em seus servidores DNS é exibida. Copie esses registros, um por um ou baixando um arquivo CSV, e navegue até a solução de hospedagem de domínio para gerar os registros DNS correspondentes.

   Verifique se todos os registros DNS foram gerados na solução de hospedagem de domínio. Se tudo estiver configurado corretamente, marque a caixa &quot;I confirm...&quot; e clique em **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Você pode criar os registros e enviar a configuração de subdomínio posteriormente usando o botão **[!UICONTROL Save as draft]**. Você poderá retomar a delegação do subdomínio abrindo-a a partir da lista de subdomínios.

1. Depois que a delegação de subdomínio for enviada, o subdomínio será exibido na lista com o status **[!UICONTROL Processing]**. Para obter mais informações sobre os status dos subdomínios, consulte [esta seção](access-subdomains.md).

   As verificações e ações abaixo serão executadas até que o subdomínio seja verificado e possa ser usado para enviar mensagens.

   Essa etapa é executada pelo Adobe e pode levar até 3 horas.

   1. Verifique se o subdomínio foi delegado ao Adobe DNS (registro NS, registro SOA, configuração de zona, registro de propriedade),
   1. Configurar DNS para o domínio,
   1. Criar URLs de rastreamento e espelho,
   1. Provisionar Frente da Nuvem CDN,
   1. Criar, validar e anexar o certificado SSL CDN,
   1. Criar DNS de encaminhamento,
   1. Criar registro PTR.

   ![](../assets/subdomain-processing.png)

1. Depois que as verificações são bem-sucedidas, o subdomínio recebe o status **[!UICONTROL Success]**. Ele está pronto para ser usado para entregar mensagens.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


