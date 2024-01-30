---
solution: Journey Optimizer
product: journey optimizer
title: Conformidade com o novo requisito DMARC
description: Saiba por que e quando você deve definir o registro DMARC no Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, domínio, correio, dmarc, registro
source-git-commit: 11d42198436319cebb67446527e9fd8d0f80cfbc
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 6%

---

# Conformidade com o novo requisito DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Saiba mais sobre a atualização do DMARC obrigatória"
>abstract="Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigirão uma **Registro DMARC** para qualquer domínio que você usar para enviar emails a eles, começando em **1 de fevereiro de 2024**.<br>Consequentemente, você deve configurar o registro DMARC em todos os subdomínios que você delegou ao Adobe no Journey Optimizer."

O DMARC (Domain-based Message Authentication, Reporting, and Conformance) é um método de autenticação de email que permite aos proprietários do domínio proteger seu domínio contra o uso não autorizado. Ao oferecer uma política clara para provedores de email/ISPs, ajuda a impedir que intervenientes mal-intencionados enviem emails que alegam ser do seu domínio. A implementação do DMARC reduz o risco de emails legítimos serem marcados como spam ou rejeitados e melhora a capacidade de entrega de emails.


Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo! ambos exigem que uma **Registro DMARC** para qualquer domínio que você usar para enviar emails para eles. Este novo requisito aplica-se a partir de **1 de fevereiro de 2024**. [Saiba mais](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}

>[!CAUTION]
>
>Não cumprimento deste novo requisito por parte do Gmail e do Yahoo! O deve resultar no bloqueio dos emails para a pasta de spam.

Consequentemente, a Adobe recomenda que você garanta que tenha o registro DMARC configurado para todos os subdomínios que você delegou à Adobe no [!DNL Journey Optimizer]. Siga as etapas abaixo que se aplicam ao seu caso:

* Se você tiver [totalmente delegado](delegate-subdomain.md#full-subdomain-delegation) Para enviar subdomínios para o Adobe, siga uma das opções abaixo:

   * Configurar o DMARC no domínio principal dos subdomínios delegados **na sua solução de hospedagem**.
ou
   * Configurar DMARC nos subdomínios delegados **no[!DNL Journey Optimizer]** interface do usuário de configuração do - sem trabalho extra na solução de hospedagem. [Saiba como](dmarc-record.md#implement-dmarc)

* Se você configurou os subdomínios de envio com [CNAME](delegate-subdomain.md#cname-subdomain-delegation), siga uma das opções abaixo:

   * Configure o DMARC nos subdomínios ou no domínio principal dos subdomínios **na sua solução de hospedagem**.
ou
   * Configurar DMARC nos subdomínios delegados **no[!DNL Journey Optimizer]** interface do usuário de configuração do. [Saiba como](dmarc-record.md#implement-dmarc)

     No entanto, com a delegação CNAME, também será necessária a entrada na solução de hospedagem. Consequentemente, certifique-se de coordenar com seu departamento de TI para que ele possa realizar a atualização assim que a [!DNL Journey Optimizer] O recurso está disponível (em 30 de janeiro). [Saiba mais](dmarc-record.md#implement-dmarc)

**Uma interface de autoatendimento para implementação do DMARC estará disponível a partir de 30 de janeiro. Saiba mais em [nesta seção](dmarc-record.md#implement-dmarc).**

As linhas do tempo mais recentes compartilhadas pela Google e pelo Yahoo são as seguintes:

* Google:

   * **Fevereiro de 2024** - As rejeições temporárias projetadas para fornecer aviso de não conformidade serão iniciadas. Os e-mails ainda serão entregues normalmente após um pequeno atraso se você ainda não estiver em conformidade. Se você estiver em total conformidade, não haverá rejeições temporárias e você não será afetado.

   * **Abril de 2024** - Os blocos serão iniciados para remetentes que não estão em conformidade com o requisito DMARC. Somente uma parte do e-mail incompatível será bloqueada no início, com a porcentagem bloqueada aumentando com o tempo.

   * **1º de junho de 2024** - Qualquer remetente que não estiver em total conformidade terá bloqueio.

* O Yahoo não forneceu datas exatas, mas disse que &quot;a implantação da fiscalização terá início em fevereiro de 2024. A execução será gradualmente implementada&quot;.

>[!NOTE]
>
>Se tiver dúvidas ou precisar de suporte, entre em contato com seu consultor de capacidade de entrega da Adobe ou com seu representante da Adobe.

**Links úteis**

* Saiba mais sobre o DMARC na [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Encontre mais orientações sobre essas alterações na [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Ler [Anúncio do Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Ler [Yahoo! comunicado](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
