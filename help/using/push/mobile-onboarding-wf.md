---
solution: Journey Optimizer
product: journey optimizer
title: Fluxo de trabalho de início rápido de integração para dispositivos móveis
description: Saiba como usar o fluxo de trabalho de início rápido de integração para dispositivos móveis
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 9%

---

# Fluxo de trabalho de início rápido de integração para dispositivos móveis {#mobile-wf}

O novo **fluxo de trabalho de início rápido de integração móvel** é um novo recurso do produto para configurar rapidamente o Adobe Experience Platform Mobile SDK, começar a coletar e validar dados de eventos móveis e enviar notificações por push com [!DNL Journey Optimizer].

Esse recurso pode ser acessado por meio da página inicial do **[!DNL Adobe Experience Platform Data Collection]** para todos os clientes como um Beta público.

## Introdução{#gs-mobile-wf}

Esse novo fluxo de trabalho automatiza a configuração da Coleção de dados, reduzindo o total de cliques e acelerando a configuração móvel do Journey Optimizer. Este fluxo de trabalho de início rápido orienta você em quatro etapas fáceis para [configurar](##setup-mobile-wf), [implementar](#implement-mobile-wf), [validar](#valid-mobile-wf) e [revisar](#review-mobile-wf) sua configuração móvel.

Para acessar o novo fluxo de trabalho de início rápido da integração móvel, navegue até **[!DNL Data Collection]** no alternador de soluções. Em seguida, selecione o cartão **[!DNL Start Collecting Mobile Data]** na home page.

![](assets/mobile-wf-home.png)

Abaixo estão alguns recursos adicionais:

* Fácil fluxo de trabalho de quatro etapas e interface do usuário.
* Fornece uma configuração básica para iniciar a coleta de dados de eventos móveis por meio da [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} em minutos.
* Capacidade de testar e validar um evento básico de push móvel aproveitando o [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=pt-BR){target="_blank"}.
* Cria e configura automaticamente todos os ativos necessários de Coleção de dados e Journey Optimizer.
* Em Orientação do produto e dicas de ferramentas.
* Fornece uma transição natural para uma implementação mais avançada, se necessário.

## Configuração {#setup-mobile-wf}

A primeira etapa desse fluxo de trabalho cria e configura automaticamente toda a Coleção de dados necessária e ativos do Journey Optimizer, como Propriedades móveis, Extensões móveis, Extensão do Journey Optimizer, Regras, Elementos de dados etc.

Depois de aceitar os Termos e Condições do Beta, digite o nome do aplicativo móvel e clique em **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Forneça informações para plataformas iOS e Android, incluindo a ID do aplicativo e as chaves de autenticação ou o arquivo de chave.

## Implementação{#implement-mobile-wf}

A próxima etapa fornece orientação passo a passo para instalar o código no aplicativo móvel.

![](assets/mobile-wf-add-code.png)


## Validar{#valid-mobile-wf}

Revise e verifique a implementação para validá-la. Você pode enviar uma notificação por push de teste.

![](assets/mobile-wf-valid.png)


## Revisar {#review-mobile-wf}

A configuração automatizada está concluída. Agora você pode visitar sua propriedade móvel de tag, configurar suas regras ou elementos de dados e começar a enviar notificações por push com o Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Tópicos relacionados**

* [Introdução à notificação por push](get-started-push.md)
* [Fluxo de dados e componentes da notificação por push](push-gs.md)
* [Configurar o canal de push](push-configuration.md)
* [Relatório de notificação por push](../reports/journey-global-report-cja-push.md#push-global)
* [Criar uma notificação por push](create-push.md)
