---
solution: Journey Optimizer
product: journey optimizer
title: Registro DMARC
description: Saiba como definir um registro DMARC no Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, domínio, email, dmarc, registro
source-git-commit: cdc3e0ffaddb2ad83ad1703c1858773d09557859
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 12%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Definir o registro DMARC"
>abstract="DMARC é um método de autenticação de email que permite aos proprietários de domínio proteger seus domínios contra uso não autorizado e evitar problemas de capacidade de entrega com provedores de caixa de correio.<br>Como parte da aplicação de práticas recomendadas do setor, o Google e o Yahoo! exigirão um registro DMARC para qualquer domínio que você usar para enviar emails a eles."

## O que é DMARC? {#what-is-dmarc}

O DMARC (Domain-based Message Authentication, Reporting, and Conformance) é um método de autenticação de email que permite que os proprietários do domínio o protejam contra o uso não autorizado. Ao oferecer uma política clara para provedores de email/ISPs, ajuda a impedir que atores mal-intencionados enviem emails que alegam ser do seu domínio. A implementação do DMARC reduz o risco de emails legítimos serem marcados como spam ou rejeitados e melhora a capacidade de entrega de emails.

O DMARC também oferece relatórios sobre mensagens que falham na autenticação, juntamente com controle sobre o tratamento de emails que não passam na validação do DMARC. Dependendo do tipo de [Política DMARC](#dmarc-policies), esses emails podem ser monitorados, colocados em quarentena ou rejeitados. Esses recursos capacitam você a tomar medidas para mitigar e resolver possíveis erros.

<!--To help you prevent deliverability issues by allowing ISPs to authenticate your sending domains - while gaining visibility and control over mail that fail this authentication, [!DNL Journey Optimizer] will soon be supporting the DMARC technology directly in its administration interface.-->

Para ajudar você a evitar problemas de entrega e, ao mesmo tempo, obter controle sobre emails com falha de autenticação, [!DNL Journey Optimizer] O agora oferece suporte à tecnologia DMARC diretamente em sua interface de administração. [Saiba mais](#implement-dmarc)

### Como o DMARC funciona? {#how-dmarc-works}

O SPF e o DKIM são usados para associar um email a um domínio e trabalhar juntos para autenticar o email. O DMARC leva isso um passo além e ajuda a evitar falsificações, correspondendo ao domínio verificado pelo DKIM e pelo SPF.

>[!NOTE]
>
>No Journey Optimizer, o SPF e o DKIM são configurados para você.

Para passar DMARC, uma mensagem deve passar SPF ou DKIM:

* O SPF (Sender Policy Framework) ajuda a verificar se a mensagem de email vem de uma fonte autorizada, verificando o endereço IP do servidor de envio em relação a uma lista de endereços IP autorizados para o domínio.
* O DKIM (DomainKeys Identified Mail) adiciona uma assinatura digital às mensagens de email, permitindo que o recipient verifique a integridade e a autenticidade da mensagem.

Se ambas ou qualquer uma dessas opções falhar na autenticação, o DMARC falhará e o email será entregue de acordo com a política DMARC selecionada.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Políticas DMARC {#dmarc-policies}

Se um email falhar na autenticação DMARC, você poderá decidir qual ação será aplicada a essa mensagem. O DMARC tem três opções de política:

* Monitor (p=none): instrui o provedor da caixa de correio/ISP a fazer o que normalmente faria com a mensagem.
* Quarentena (p=quarantine): instrui o provedor de caixa de correio/ISP a entregar e-mails que não transmitem o DMARC para a pasta de spam ou lixo eletrônico do recipient.
* Reject (p=reject): Instrui o provedor/ISP de caixa de correio a bloquear o email que não passa DMARC, resultando em uma rejeição.

>[!NOTE]
>
>Saiba como definir a política DMARC com [!DNL Journey Optimizer] in [nesta seção](#set-up-dmarc).

## Atualização de requisito DMARC {#dmarc-update}

Como parte da aplicação de práticas recomendadas do setor, o Google e o Yahoo! ambos exigem que você tenha uma **Registro DMARC** para qualquer domínio que você usar para enviar emails para eles. Este novo requisito aplica-se a partir de **1 de fevereiro de 2024**.

Saiba mais sobre o Google e o Yahoo!&#39;requisito s em [nesta seção](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=pt-BR#dmarc){target="_blank"}.

>[!CAUTION]
>
>Espera-se que o não cumprimento deste novo requisito do Gmail e do Yahoo! O deve resultar no bloqueio dos emails para a pasta de spam. [Saiba mais](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#how-will-this-impact-me-as-a-marketer%3F){target="_blank"}

Consequentemente, a Adobe recomenda que você execute as seguintes ações:

* Verifique se **Registro DMARC** configurar para **todos os subdomínios já delegados por você** para Adobe em [!DNL Journey Optimizer]. [Saiba como](#check-subdomains-for-dmarc)

* Quando **delegar qualquer novo subdomínio** para Adobe, é possível **configurar DMARC** diretamente **no [!DNL Journey Optimizer] interface de administração**. [Saiba como](#implement-dmarc)

## Implementar o DMARC no [!DNL Journey Optimizer] {#implement-dmarc}

A variável [!DNL Journey Optimizer] A interface de administração do permite configurar o registro DMARC para todos os subdomínios que você já delegou ou está delegando ao Adobe. As etapas detalhadas estão descritas abaixo.

### Verifique se há DMARC nos subdomínios existentes {#check-subdomains-for-dmarc}

Para garantir que você tenha o registro DMARC configurado para todos os subdomínios que você delegou em [!DNL Journey Optimizer], siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Subdomínios]** e clique em **[!UICONTROL Configurar subdomínio]**.

1. Para cada subdomínio delegado, verifique o **[!UICONTROL Registro DMARC]** coluna. Se nenhum registro for encontrado para um determinado subdomínio, um alerta será exibido.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Para estar em conformidade com o novo requisito do Gmail e do Yahoo! e evitar problemas de capacidade de entrega com os principais ISPs, é recomendável configurar um registro DMARC para todos os subdomínios delegados. [Saiba mais](dmarc-record-update.md)

1. Selecione um subdomínio sem registro DMARC associado e preencha o **[!UICONTROL Registro DMARC]** de acordo com as necessidades de sua organização. As etapas para preencher os campos de registro DMARC estão detalhadas em [nesta seção](#implement-dmarc).

1. Considere as duas opções abaixo:

   * Se você estiver editando um subdomínio configurado com o [CNAME](delegate-subdomain.md#cname-subdomain-delegation), você deve copiar o registro DNS para o DMARC na solução de hospedagem para gerar os registros DNS correspondentes.

     ![](assets/dmarc-record-edit-cname.png)

     Verifique se o registro DNS foi gerado na solução de hospedagem de domínio e marque a caixa &quot;Confirmo...&quot;.

   * Se você estiver editando um subdomínio [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) para Adobe, basta preencher o **[!UICONTROL Registro DMARC]** campos detalhados em [nesta seção](#implement-dmarc). Nenhuma outra ação é necessária.

     ![](assets/dmarc-record-edit-full.png)

1. Salve as alterações.

### Configurar DMARC para novos subdomínios {#set-up-dmarc}

Ao delegar novos subdomínios para o Adobe em [!DNL Journey Optimizer], um registro DMARC será criado no DNS para o seu domínio. Siga as etapas abaixo para implementar o DMARC.

>[!CAUTION]
>
>Para estar em conformidade com o novo requisito do Gmail e do Yahoo! e evitar problemas de capacidade de entrega com os principais ISPs, é recomendável configurar um registro DMARC para todos os subdomínios delegados. [Saiba mais](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Configure um novo subdomínio. [Saiba como](delegate-subdomain.md)

1. Vá para a **[!UICONTROL Registro DMARC]** seção.

   Se o subdomínio tiver um registro DMARC existente e se for buscado por [!DNL Journey Optimizer], você poderá usar os mesmos valores que estão destacados na interface ou alterá-los conforme necessário.

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >Se você não adicionar nenhum valor, os valores padrão pré-preenchidos serão usados.

1. Defina a ação que o servidor do recipient executará se o DMARC falhar. Dependendo do [Política DMARC](#dmarc-policies) que deseja aplicar, selecione uma das três opções:

   * **[!UICONTROL Nenhum]** (valor padrão): instrui o destinatário a não executar nenhuma ação em relação às mensagens que falham na autenticação DMARC, mas ainda enviam relatórios de email ao remetente.
   * **[!UICONTROL Quarentena]**: instrui o servidor de email de recebimento a colocar em quarentena emails que falham na autenticação DMARC - isso geralmente significa colocar essas mensagens na pasta de spam ou lixo eletrônico do destinatário.
   * **[!UICONTROL Rejeitar]**: instrui o destinatário a negar completamente (rejeição) qualquer email do domínio que apresentar falha de autenticação. Com essa política ativada, somente os emails verificados como 100% autenticados pelo seu domínio terão uma chance de inserção na caixa de entrada.

   >[!NOTE]
   >
   >Como prática recomendada, é recomendável implantar lentamente a implementação DMARC, escalando sua política DMARC de **Nenhum**, para **Quarentena**, para **Rejeitar** à medida que você entende o impacto potencial do DMARC.

1. Opcionalmente, adicione um ou mais endereços de email de sua escolha para indicar onde **Relatórios DMARC** em emails que [falha na autenticação](#how-dmarc-works) deve entrar em sua organização. Você pode adicionar até cinco endereços para cada relatório.

   >[!NOTE]
   >
   >Certifique-se de ter uma caixa de entrada original (não o Adobe) em seu controle, onde você pode receber esses relatórios.

   Há dois relatórios diferentes gerados por ISPs que os remetentes podem receber por meio das tags RUA/RUF na política DMARC:

   * **Relatórios agregados** (RUA): eles não contêm nenhuma PII (Informações de identificação pessoal) que possa ser sensível ao GDPR.
   * **Relatórios de falha forense** (RUF): eles contêm endereços de email sensíveis ao GDPR. Antes de usar o, verifique internamente como lidar com informações que precisam ser compatíveis com o GDPR.

   >[!NOTE]
   >
   >Esses relatórios altamente técnicos fornecem uma visão geral dos emails que são tentados de falsificação. Eles são melhor assimilados por meio de uma ferramenta de terceiros.

1. Selecione o **porcentagem aplicável** de emails para DMARC.

   Essa porcentagem depende da confiança na infraestrutura de email e da tolerância a falsos positivos (emails legítimos marcados como fraudulentos). É comum que as organizações comecem com a política DMARC definida como **Nenhum**, aumente gradualmente a porcentagem de política DMARC e monitore de perto o impacto no delivery de email legítimo.

   >[!NOTE]
   >
   >Trabalhe com os administradores de email e a equipe de TI para aumentar gradualmente a porcentagem à medida que você ganhar confiança nas práticas de autenticação de email.

   Como prática recomendada, procure uma alta taxa de conformidade DMARC, idealmente próxima a 100%, para maximizar os benefícios de segurança e, ao mesmo tempo, minimizar o risco de falsos positivos.

1. Selecione um **intervalo de relatórios** entre 24 e 168 horas. Ele permite que os proprietários de domínio recebam atualizações regulares sobre os resultados de autenticação de email e tomem as medidas necessárias para melhorar a segurança do email.

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->







