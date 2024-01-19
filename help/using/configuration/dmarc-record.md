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
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Registro DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Definir o registro DMARC"
>abstract="Definir registro DMARC para evitar problemas de entrega com ISPs"

>[!CAUTION]
>
>Seguindo os anúncios recentes do Gmail e do Yahoo para remetentes em massa, a Journey Optimizer agora é compatível com a tecnologia de autenticação DMARC. //Você deve atualizar todos os subdomínios que já foram criados em sua instância para incluir suporte DMARC.//

É importante fazê-lo até 1º de fevereiro, Doc virá em breve

Começando em

Você tem duas opções:

* Faça isso por conta própria a partir de agora: configure-o com seu departamento de TI - sempre que desejar

* Faça no AJO - mas nesse caso, é necessário aguardar até 30 de janeiro

   * Delegação completa: você pode fazer isso em 30 de janeiro (versão do AJO)

   * O CNAME o planeja com seu departamento de TI para que não seja demorado, mas você precisa planejá-lo

Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigirão que você tenha um registro DMARC para qualquer domínio usado para enviar emails para eles. Este novo requisito começa em **1 de fevereiro de 2024**.

Saiba mais sobre os requisitos do Google e do Yahoo para registro DMARC em [nesta seção](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Saiba mais sobre as alterações anunciadas no Google e no Yahoo em [esta página](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, que significa **Autenticação de mensagens baseadas em domínio, relatórios e conformidade** O, é um protocolo de autenticação de email que ajuda a proteger contra falsificação de email, phishing e outras atividades fraudulentas.

* Autenticação de email:

   * SPF (Estrutura de Política do Remetente): o DMARC depende do SPF para autenticar a identidade do servidor de email de envio. O SPF ajuda a verificar se a mensagem de email vem de uma fonte autorizada, verificando o endereço IP do servidor de envio em relação a uma lista de endereços IP autorizados para o domínio.
   * DKIM (DomainKeys Identified Mail): o DMARC também usa o DKIM para adicionar uma assinatura digital às mensagens de email, permitindo que o recipient verifique a integridade e a autenticidade da mensagem.

* O DMARC ajuda a impedir que agentes mal-intencionados enviem emails que parecem vir do seu domínio. Ao configurar o DMARC, você pode especificar como os provedores de email devem lidar com as mensagens que falham nas verificações de autenticação, reduzindo a probabilidade de os emails de phishing chegarem aos destinatários.

* O DMARC ajuda a melhorar a capacidade de entrega de emails, fornecendo uma política clara que os provedores de email devem seguir ao encontrar mensagens que afirmam ser do seu domínio. Isso pode reduzir as chances de emails legítimos serem marcados como spam ou rejeitados.

* Ao implementar o DMARC, você pode proteger a reputação da sua marca, garantindo que partes não autorizadas não possam abusar do seu domínio para phishing ou outras atividades mal-intencionadas. Isso é particularmente importante para empresas e organizações que dependem de comunicação por email com clientes e parceiros.

A configuração de um registro DMARC envolve a adição de um registro TXT de DNS às configurações de DNS do seu domínio. Esse registro especifica sua política DMARC, como colocar em quarentena ou rejeitar mensagens que falham na autenticação. A implementação do DMARC é uma etapa proativa para melhorar a segurança do email e proteger sua organização e seus recipients de ameaças baseadas em email.

[Saiba mais sobre o DMARC no Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=pt-BR){target="_blank"} para entender melhor o impacto do DMARC na capacidade de entrega de emails.

Se você não adicionar o DMARC, será colocado em quarentena (pelo menos).

certifique-se de que você tenha uma caixa de entrada original onde possa receber em seu controle - você gerencia essa caixa de entrada (não deve ser a caixa de entrada do Adobe)

A recomendação é 24 porque geralmente, se menos, avalie sua capacidade / verifique o seu > chat GPT

Google e Yahoo, e provavelmente todos os outros ISPs principais

para CNAME no fluxo de edição, é necessário Baixar o arquivo CSV novamente (não para totalmente delegado)

novo registro DMARC

Em RN > Coloque em primeiro lugar Todos os subdomínios devem ser atualizados com suporte DMARC



