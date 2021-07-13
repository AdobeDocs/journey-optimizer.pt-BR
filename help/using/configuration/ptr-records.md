---
title: Registros PTR
description: '"Saiba como gerenciar registros ptr"'
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
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---


# Registros PTR

## Sobre registros PTR

Um registro de ponteiro (PTR) é um tipo de registro de Sistema de Nome de Domínio (DNS) que fornece o nome de domínio vinculado a um endereço IP.

Com registros PTR, os servidores de email de recebimento podem verificar a autenticidade do envio dos servidores de email identificando se seus endereços IP correspondem aos nomes com os quais os servidores se conectam.

## Acesse os registros PTR dos subdomínios

Depois que um subdomínio é delegado no Gerenciamento de jornada do cliente, um registro PTR é criado automaticamente e associado a esse subdomínio. Você pode acessá-lo no menu **[!UICONTROL Channels]** `>` **[!UICONTROL PTR records]**.

![](../assets/ptr-records.png)

A lista mostra os registros PTR gerados para cada subdomínio delegado, usando a sintaxe abaixo:

* &quot;r&quot; para registro,
* &quot;xx&quot; para os dois últimos algarismos do endereço IP,
* nome do subdomínio.

Você pode abrir um registro PTR na lista para exibir o nome do subdomínio associado e o endereço IP.

>[!NOTE]
>
>Observe que os registros PTR são somente leitura e que não é possível modificar o subdomínio associado a um endereço IP.
