---
solution: Journey Optimizer
product: journey optimizer
title: Delegação de subdomínio em  [!DNL Journey Optimizer]
description: Saiba como delegar subdomínios
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, otimizador, delegação
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 7854de133ebcd3b29ca59b747aa89fae242f2ea5
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 32%

---

# Delegação de subdomínio no [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="Os subdomínios delegados são exibidos aqui."
>abstract="Delegue seu primeiro subdomínio. Após a conclusão da delegação, os registros PTR são criados e os canais de email são habilitados."

A criação de um subdomínio para campanhas de email permite que as marcas isolem vários tipos de tráfego (marketing versus corporativo, por exemplo) em pools de IP específicos e com domínios específicos, o que agilizará o processo de aquecimento de IP e melhorará a capacidade de entrega em geral.

Se você compartilhar um domínio e ele for bloqueado ou adicionado à lista de bloqueios, isso poderá afetar seu delivery de email corporativo. No entanto, problemas de reputação ou bloqueios em um domínio específico para suas comunicações de marketing por email afetarão apenas esse fluxo de email. Usar seu domínio principal como remetente ou endereço &quot;De&quot; para vários fluxos de email também pode interromper a autenticação de email, fazendo com que suas mensagens sejam bloqueadas ou colocadas na pasta de spam.

>[!CAUTION]
>
>Você não pode usar o mesmo domínio de envio para enviar mensagens de [!DNL Adobe Journey Optimizer] e de outro produto, como [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage].

## Por que configurar subdomínios? {#why-set-up-subdomains}

Um subdomínio é uma divisão do seu domínio que pode ser usada para isolar suas marcas ou vários tipos de tráfego; por exemplo, mensagens transacionais e comunicações de marketing.

Vamos ver o exemplo do domínio &quot;mybrand.com&quot;, usado para enviar comunicações transacionais e de marketing. Nessa situação, você pode optar por configurar dois subdomínios:

* subdomínio &quot;info.mybrand.com&quot; para comunicações transacionais (confirmação de compras, redefinição de senha etc.),
* subdomínio &quot;marketing.mybrand.com&quot; para emails de prospecção.

Ao fazer isso, você ajudará a preservar a reputação do seu domínio e de outros subdomínios. Por exemplo, se os subdomínios &quot;marketing.mybrand.com&quot; acabassem sendo incluídos na lista de bloqueios por provedores de serviço de internet devido a uma entrega incorreta, isso evitaria que todo o domínio &quot;mybrand.com&quot; e o subdomínio &quot;info.mybrand.com&quot; fossem incluídos na lista de bloqueios.

Ao implementar uma solução, há requisitos para componentes voltados para o exterior: eles incluem a configuração de links e páginas da Web a serem rastreadas, a exibição de mirror pages etc.

Embora esses requisitos estejam sendo gerenciados por meio de componentes hospedados pelo Adobe e pelo cliente, eles incluem URLs que podem ser vistos pelos recipients dos emails. Para evitar ter URLs que indicam a solução técnica subjacente ou o provedor de hospedagem, os subdomínios podem ser configurados para tornar isso transparente para os recipients dos emails.

**Saiba mais**

* Saiba como [delegar subdomínios](delegate-subdomain.md) diretamente da interface
* Saiba como [adicionar registros TXT do Google](google-txt.md) aos seus subdomínios para garantir a entrega bem-sucedida de emails para endereços Gmail
* Saiba como [acessar os registros PTR](ptr-records.md) gerados para seus subdomínios, permitindo que eles sejam verificados pelo envio de servidores de email

## Métodos de configuração de subdomínio {#subdomain-delegation-methods}

A configuração de subdomínio permite configurar uma subseção do seu domínio (tecnicamente uma &quot;zona DNS&quot;) para usar com o Adobe Campaign.

Os métodos de configuração disponíveis são os seguintes.

### Delegar totalmente um subdomínio à Adobe (recomendado) {#full-subdomain-delegation}

O [!DNL Journey Optimizer] permite delegar totalmente os subdomínios à Adobe diretamente da interface do produto. Ao fazer isso, o Adobe poderá enviar mensagens como um serviço gerenciado, controlando e mantendo todos os aspectos do DNS necessários para fornecer, renderizar e rastrear campanhas de email.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Você pode confiar no Adobe para manter a infraestrutura de DNS necessária para atender aos requisitos de capacidade de entrega padrão do setor para seus domínios de envio de marketing por email, enquanto continua mantendo e controlando DNS para seus domínios de email internos.

>[!IMPORTANT]
>
>A delegação de subdomínio completa é o método preferido.

Saiba como delegar completamente um subdomínio ao Adobe nesta [seção](delegate-subdomain.md#set-up-subdomain).

### Configurar um subdomínio com CNAMEs {#cname-subdomain-setup}

Se você tiver políticas de restrição específicas de domínio e quiser que o Adobe tenha controle parcial sobre o DNS, poderá optar por realizar todas as atividades relacionadas ao DNS da sua parte.

A configuração do subdomínio CNAME permite criar um subdomínio e usar CNAMEs para apontar para registros específicos do Adobe. Com essa configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS para configurar o ambiente para enviar, renderizar e rastrear emails.

>[!CAUTION]
>
>O método CNAME é recomendado se as políticas de sua organização restringirem o método completo de delegação de subdomínio. Essa abordagem exige que você mantenha e gerencie registros DNS por conta própria.
>
>O Adobe não poderá ajudar na alteração, manutenção ou gerenciamento de DNS em um subdomínio configurado por meio do método CNAME.

Saiba como criar um subdomínio usando CNAMEs para apontar para registros específicos do Adobe em [esta seção](delegate-subdomain.md#cname-subdomain-setup).

## Comparação dos métodos de configuração

A tabela abaixo apresenta um resumo de como esses métodos funcionam, bem como o nível de esforço necessário:

| Método de configuração | Como funciona | Nível de esforço |
|---|---|---|
| **Delegação completa** | Crie o subdomínio e o registro de namespace. A Adobe irá configurar todos os registros DNS necessários para o Adobe Campaign.<br/><br/>Nesta configuração, a Adobe é totalmente responsável pelo gerenciamento do subdomínio e de todos os registros DNS. | Baixo |
| **método CNAME** | Crie o subdomínio e o registro de namespace. A Adobe fornecerá os registros que serão colocados em seus servidores DNS e configurará os valores correspondentes em servidores DNS do Adobe Campaign.<br/><br/>Nessa configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS. | Alto |

<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Campaign.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Campaign DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |
| **Custom delegation method** |  Create the subdomain and namespace record - Adobe will then provide the records to be placed in your DNS servers. Upload the SSL Certificate obtained from the Certificate Authority and complete the Feedback Loop steps by verifying domain ownership and reporting email address.<br/><br/>In this setup, you have full responsibility for maintaining DNS. | Very high |-->

Outras informações sobre a delegação de domínios estão disponíveis [nesta documentação](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=pt-BR){target="_blank"}.

Se você tiver qualquer pergunta relacionada aos métodos de configuração de subdomínio, entre em contato com a Adobe ou com o Atendimento ao cliente para solicitar a consultoria de capacidade de entrega.


