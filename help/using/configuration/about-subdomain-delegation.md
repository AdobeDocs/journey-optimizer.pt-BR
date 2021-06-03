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
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# Introdução à delegação de subdomínio

## Isole suas marcas para proteger sua reputação

Um subdomínio é uma divisão do seu domínio que pode ser usada para isolar suas marcas ou vários tipos de tráfego (mensagens transacionais, informações de marketing etc.).
Vamos ver o exemplo do domínio &quot;mybrand.com&quot;, usado para enviar comunicações transacionais e de marketing. Nessa situação, você pode optar por configurar dois subdomínios:

* subdomínio &quot;info.mybrand.com&quot; para comunicações transacionais (confirmação de compras, redefinição de senha etc.),
* subdomínio &quot;marketing.mybrand.com&quot; para emails de prospecção.

Ao fazer isso, você ajudará a preservar a reputação do seu domínio e de outros subdomínios. Por exemplo, se os subdomínios &quot;marketing.mybrand.com&quot; acabassem sendo incluídos na lista de bloqueios por provedores de serviço de internet devido a uma entrega incorreta, isso evitaria que todo o domínio &quot;mybrand.com&quot; e o subdomínio &quot;info.mybrand.com&quot; fossem incluídos na lista de bloqueios.

## Mantenha seus URLs de recursos transparentes para os clientes

Ao implementar uma solução, há requisitos para componentes voltados para o exterior: isso inclui configurar links e páginas da Web a serem rastreadas, exibir mirror pages, etc.

Embora esses requisitos estejam sendo gerenciados por meio de componentes hospedados pelo Adobe e pelo cliente, eles incluem URLs que podem ser vistos pelos recipients dos emails. Para evitar URLs que indicam a solução técnica subjacente ou o provedor de hospedagem, os subdomínios podem ser configurados para tornar isso transparente para os recipients dos emails. [Saiba mais sobre Delegação](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=pt-BR) de domínio.

## Delegação de subdomínio no Journey Optimizer

O Journey Optimizer fornece vários recursos para ajudar você a gerenciar subdomínios:

* [Delegar seus ](delegate-subdomain.md) subdomínios diretamente da interface,
* [Adicione ](google-txt.md) registros TXT do Google a seus subdomínios para garantir o delivery bem-sucedido de emails para endereços Gmail,
* [Acesse os ](ptr-records.md) registros PTR gerados para seus subdomínios, permitindo que eles sejam verificados pelo envio de servidores de email.
