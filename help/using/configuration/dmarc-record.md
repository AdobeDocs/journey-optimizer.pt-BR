---
solution: Journey Optimizer
product: journey optimizer
title: Registro DMARC
description: Saiba como definir um registro DMARC no Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, domínio, correio, dmarc, registro
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Definir o registro DMARC"
>abstract="Defina o registro DMARC para evitar problemas de entrega com ISPs. Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigem um registro DMARC para qualquer domínio usado para enviar emails para eles."

>[!CAUTION]
>
>Seguindo os anúncios recentes do Gmail e do Yahoo para remetentes em massa, a Journey Optimizer agora é compatível com a tecnologia de autenticação DMARC.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigirão uma **Registro DMARC** para qualquer domínio que você usar para enviar emails para eles. Este novo requisito começa em **1 de fevereiro de 2024**.

Saiba mais sobre os requisitos do Google e do Yahoo em [nesta seção](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>O não cumprimento desse novo requisito por parte do Gmail e do Yahoo deve resultar no bloqueio dos emails que chegam à pasta de spam.

Consequentemente, a Adobe recomenda que você garanta que tenha o registro DMARC configurado para todos os subdomínios que você delegou à Adobe no [!DNL Journey Optimizer]. Siga as etapas abaixo que se aplicam ao seu caso:

* Se você tiver [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) Para enviar subdomínios para o Adobe, siga uma das duas opções abaixo:

   * Configurar o DMARC no domínio principal dos subdomínios delegados **na sua solução de hospedagem**.

   * Configurar DMARC nos subdomínios delegados **usar o recurso futuro no [!DNL Journey Optimizer] interface de administração** - sem trabalho extra na solução de hospedagem.

* Se você configurou o [Delegação CNAME](delegate-subdomain.md#cname-subdomain-delegation) para os subdomínios de envio, siga uma das duas opções abaixo:

   * Configure o DMARC nos subdomínios ou no domínio principal dos subdomínios **na sua solução de hospedagem**.

   * Configurar DMARC nos subdomínios delegados **usar o recurso futuro no [!DNL Journey Optimizer] interface de administração**. No entanto, também exigirá a entrada na sua solução de hospedagem. Consequentemente, certifique-se de coordenar com seu departamento de TI para que ele possa realizar a atualização assim que a [!DNL Journey Optimizer] O recurso está disponível (em 30 de janeiro). <!--and be ready on February 1st, 2024-->

**Mais detalhes sobre o [!DNL Journey Optimizer] O próximo recurso DMARC será lançado em breve.**

>[!NOTE]
>
>Saiba mais sobre a implementação do DMARC na [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para entender melhor o impacto na capacidade de delivery de emails.

## O que é DMARC?

DMARC, que significa **Autenticação de mensagens baseadas em domínio, relatórios e conformidade** O, é um método/protocolo de autenticação de email que permite aos proprietários de domínios proteger seus domínios contra o uso não autorizado.

Oferecendo uma maneira de autenticar o domínio do remetente, ajuda a impedir que agentes mal-intencionados enviem emails que parecem vir do seu domínio.

O DMARC também fornece feedback sobre o status de autenticação do email e permite que os remetentes controlem o que acontece aos emails que falham na autenticação. Isso inclui opções para monitorar, colocar em quarentena ou rejeitar emails, dependendo da política DMARC implementada.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

O DMARC tem três opções de política:

* Monitor (p=none): instrui o provedor da caixa de correio/ISP a fazer o que normalmente faria com a mensagem.
* Quarentena (p=quarantine): instrui o provedor de caixa de correio/ISP a entregar e-mails que não transmitem o DMARC para a pasta de spam ou lixo eletrônico do recipient.
* Reject (p=reject): Instrui o provedor/ISP de caixa de correio a bloquear o email que não passa DMARC, resultando em uma rejeição.

## Como o DMARC funciona?

O SPF e o DKIM são usados para associar um email a um domínio e trabalhar juntos para autenticar o email. O DMARC leva isso um passo além e ajuda a evitar falsificações, correspondendo ao domínio verificado pelo DKIM e pelo SPF. Para passar DMARC, uma mensagem deve passar SPF ou DKIM. Se ambas as opções falharem na autenticação, o DMARC falhará e o email será entregue de acordo com a política DMARC selecionada.

* SPF (Estrutura de Política do Remetente): o DMARC depende do SPF para autenticar a identidade do servidor de email de envio. O SPF ajuda a verificar se a mensagem de email vem de uma fonte autorizada, verificando o endereço IP do servidor de envio em relação a uma lista de endereços IP autorizados para o domínio.
* DKIM (DomainKeys Identified Mail): o DMARC também usa o DKIM para adicionar uma assinatura digital às mensagens de email, permitindo que o recipient verifique a integridade e a autenticidade da mensagem.

>[!NOTE]
>
>O DMARC requer alinhamento entre os endereços &quot;De&quot; e &quot;Caminho de retorno&quot;.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## Implementar DMARC {#implement-dmarc}

Para implementar o DMARC, siga as etapas abaixo que se aplicam ao seu caso.

* Se você não adicionar o DMARC, será colocado em quarentena (pelo menos).

### Subdomínios totalmente delegados

Defina a ação que o servidor do recipient executará se o DMARC falhar.

O DMARC tem três opções de política:

* Monitor (p=none): instrui o provedor da caixa de correio/ISP a fazer o que normalmente faria com a mensagem. Este é o valor padrão.
* Quarentena (p=quarantine): instrui o provedor de caixa de correio/ISP a entregar e-mails que não transmitem o DMARC para a pasta de spam ou lixo eletrônico do recipient.
* Reject (p=reject): Instrui o provedor/ISP de caixa de correio a bloquear o email que não passa DMARC, resultando em uma rejeição.

Emails para receber relatórios DMARC agregados e relatórios de falha DMARC forenses: é possível adicionar até 5 endereços.

* Certifique-se de que você tem uma caixa de entrada original onde pode receber em seu controle - você gerencia essa caixa de entrada (não deve ser a caixa de entrada Adobe)

Porcentagem de emails aplicável para aplicar o DMARC:

Intervalo de relatório: a recomendação é 24 porque geralmente é isso que os ISPs têm.
se menos, avalie sua capacidade / verifique o seu > chat GPT

Se um registro DMARC for detectado, você poderá copiar e colar os mesmos valores que os listados ou alterá-los, se necessário.

Se você não colocar nada, os valores padrão serão usados.

### Subdomínios delegados usando CNAME

para CNAME no fluxo de edição, é necessário baixar o arquivo CSV novamente (não para totalmente delegado)





