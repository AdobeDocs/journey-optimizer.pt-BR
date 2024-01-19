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
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
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

Consequentemente, a Adobe recomenda que você garanta que tenha o registro DMARC configurado para todos os subdomínios que você delegou à Adobe no [!DNL Journey Optimizer]. Siga uma das duas opções abaixo:

* Configure o DMARC nos subdomínios ou no domínio principal dos subdomínios, **na sua solução de hospedagem**.

* Configurar DMARC nos subdomínios delegados **usando o novo recurso na [!DNL Journey Optimizer] interface de administração** - sem trabalho extra na solução de hospedagem. [Saiba mais](#implement-dmarc)

  >[!CAUTION]
  >
  >Se você configurou o [Delegação CNAME](delegate-subdomain.md#cname-subdomain-delegation) para os subdomínios de envio, também será necessária alguma entrada na solução de hospedagem. Certifique-se de coordenar com o departamento de TI para que ele possa realizar a atualização assim que a [!DNL Journey Optimizer] O recurso está disponível (em 30 de janeiro de 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>Saiba mais sobre a implementação do DMARC na [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para entender melhor o impacto na capacidade de delivery de emails.

## O que é DMARC?

DMARC, que significa **Autenticação de mensagens baseadas em domínio, relatórios e conformidade** O, é um protocolo de autenticação de email que ajuda a proteger contra falsificação de email, phishing e outras atividades fraudulentas.

* Autenticação de email:

   * SPF (Estrutura de Política do Remetente): o DMARC depende do SPF para autenticar a identidade do servidor de email de envio. O SPF ajuda a verificar se a mensagem de email vem de uma fonte autorizada, verificando o endereço IP do servidor de envio em relação a uma lista de endereços IP autorizados para o domínio.
   * DKIM (DomainKeys Identified Mail): o DMARC também usa o DKIM para adicionar uma assinatura digital às mensagens de email, permitindo que o recipient verifique a integridade e a autenticidade da mensagem.

* O DMARC ajuda a impedir que agentes mal-intencionados enviem emails que parecem vir do seu domínio. Ao configurar o DMARC, você pode especificar como os provedores de email devem lidar com as mensagens que falham nas verificações de autenticação, reduzindo a probabilidade de os emails de phishing chegarem aos destinatários.

* O DMARC ajuda a melhorar a capacidade de entrega de emails, fornecendo uma política clara que os provedores de email devem seguir ao encontrar mensagens que afirmam ser do seu domínio. Isso pode reduzir as chances de emails legítimos serem marcados como spam ou rejeitados.

* Ao implementar o DMARC, você pode proteger a reputação da sua marca, garantindo que partes não autorizadas não possam abusar do seu domínio para phishing ou outras atividades mal-intencionadas. Isso é particularmente importante para empresas e organizações que dependem de comunicação por email com clientes e parceiros.

A configuração de um registro DMARC envolve a adição de um registro TXT de DNS às configurações de DNS do seu domínio. Esse registro especifica sua política DMARC, como colocar em quarentena ou rejeitar mensagens que falham na autenticação. A implementação do DMARC é uma etapa proativa para melhorar a segurança do email e proteger sua organização e seus recipients de ameaças baseadas em email.

## Implementar DMARC {#implement-dmarc}

* Se você não adicionar o DMARC, será colocado em quarentena (pelo menos).

* Certifique-se de que você tem uma caixa de entrada original onde pode receber em seu controle - você gerencia essa caixa de entrada (não deve ser a caixa de entrada Adobe)

A recomendação é 24 porque geralmente é isso que os ISPs têm.
se menos, avalie sua capacidade / verifique o seu > chat GPT

Se um registro DMARC for detectado, você poderá copiar e colar os mesmos valores que os listados ou alterá-los, se necessário.

Se você não colocar nada, os valores padrão serão usados.

### Subdomínios totalmente delegados

### Subdomínios delegados usando CNAME

para CNAME no fluxo de edição, é necessário baixar o arquivo CSV novamente (não para totalmente delegado)





