---
title: Delegar subdomínios
description: Saiba como delegar subdomínios
internal: n
snippet: y
feature: Configurações do aplicativo
topic: Administração
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 27%

---


# Delegação de subdomínio em [!DNL Journey Optimizer]

A criação de um subdomínio para campanhas de email permite que as marcas isolem vários tipos de tráfego (marketing vs. corporativo, por exemplo) em pools de IP específicos e com domínios específicos, o que agilizará o processo de aquecimento de IP e melhorará a capacidade de entrega em geral. Se você compartilhar um domínio e ele for bloqueado ou adicionado à lista de bloqueios, isso poderá afetar seu delivery de email corporativo. No entanto, problemas ou blocos de reputação em um domínio específico para suas comunicações de marketing por email afetarão apenas esse fluxo de email. Usar seu domínio principal como remetente ou endereço &quot;De&quot; para vários fluxos de email também pode quebrar a autenticação de email, fazendo com que suas mensagens sejam bloqueadas ou colocadas na pasta de spam.

Um subdomínio é uma divisão do seu domínio que pode ser usada para isolar suas marcas ou vários tipos de tráfego, por exemplo, mensagens transacionais e comunicações de marketing.

Vamos ver o exemplo do domínio &quot;mybrand.com&quot;, usado para enviar comunicações transacionais e de marketing. Nessa situação, você pode optar por configurar dois subdomínios:

* subdomínio &quot;info.mybrand.com&quot; para comunicações transacionais (confirmação de compras, redefinição de senha etc.),
* subdomínio &quot;marketing.mybrand.com&quot; para emails de prospecção.

Ao fazer isso, você ajudará a preservar a reputação do seu domínio e de outros subdomínios. Por exemplo, se os subdomínios &quot;marketing.mybrand.com&quot; acabassem sendo incluídos na lista de bloqueios por provedores de serviço de internet devido a uma entrega incorreta, isso evitaria que todo o domínio &quot;mybrand.com&quot; e o subdomínio &quot;info.mybrand.com&quot; fossem incluídos na lista de bloqueios.

Ao implementar uma solução, há requisitos para componentes voltados para o exterior: isso inclui configurar links e páginas da Web a serem rastreadas, exibir mirror pages, etc.

Embora esses requisitos estejam sendo gerenciados por meio de componentes hospedados pelo Adobe e pelo cliente, eles incluem URLs que podem ser vistos pelos recipients dos emails. Para evitar URLs que indicam a solução técnica subjacente ou o provedor de hospedagem, os subdomínios podem ser configurados para tornar isso transparente para os recipients dos emails.

**Saiba mais**

* Saiba como [delegar seus subdomínios](delegate-subdomain.md) diretamente da interface
* Saiba como [adicionar registros TXT do Google](google-txt.md) a seus subdomínios para garantir o delivery bem-sucedido de emails para endereços Gmail
* Saiba como [acessar os registros PTR](ptr-records.md) gerados para seus subdomínios, permitindo que eles sejam verificados pelo envio de servidores de email
