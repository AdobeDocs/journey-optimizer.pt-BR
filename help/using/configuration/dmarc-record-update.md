---
solution: Journey Optimizer
product: journey optimizer
title: Conformidade com o novo requisito DMARC
description: Saiba por que e quando você deve definir o registro DMARC no Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, domínio, email, dmarc, registro
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: da5b8d6c95e76af98b27ffcff11e75c26b90200a
workflow-type: ht
source-wordcount: '431'
ht-degree: 100%

---

# Conformidade com o novo requisito DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Saiba mais sobre a atualização obrigatória do DMARC"
>abstract="Como parte da aplicação de práticas recomendadas do setor, o Google e o Yahoo exigirão um **Registro DMARC**, para qualquer domínio que você usar para enviar emails a eles, a partir de **1º de fevereiro de 2024**.<br>Consequentemente, você deve configurar o registro DMARC em todos os subdomínios que delegou ao Adobe no Journey Optimizer."

O DMARC (Domain-based Message Authentication, Reporting, and Conformance) é um método de autenticação de email que permite que os proprietários do domínio o protejam contra o uso não autorizado. Ao oferecer uma política clara para provedores de email/ISPs, ajuda a impedir que atores mal-intencionados enviem emails que alegam ser do seu domínio. A implementação do DMARC reduz o risco de emails legítimos serem marcados como spam ou rejeitados e melhora a capacidade de entrega de emails.

Como parte da aplicação de práticas recomendadas do setor, o Google e o Yahoo! estão exigindo um **Registro DMARC** para qualquer domínio que você usar para enviar emails a eles. Este novo requisito se aplica a partir de **1º de fevereiro de 2024**.

>[!CAUTION]
>
>Espera-se que o não cumprimento deste novo requisito do Gmail e do Yahoo! resulte em emails direcionados à pasta de spam ou bloqueados.

Consequentemente, a Adobe recomenda que você se certifique de ter o registro DMARC configurado para todos os subdomínios que delegou à Adobe no [!DNL Journey Optimizer]. Siga as etapas abaixo que se aplicam ao seu caso:

* Se você tiver [delegado por completo](delegate-subdomain.md#full-subdomain-delegation) seus subdomínios de envio para a Adobe, siga uma das opções abaixo:

   * Configure o DMARC no domínio principal dos subdomínios delegados **na sua solução de hospedagem**.
ou
   * Configure o DMARC nos subdomínios delegados **na interface de configuração do[!DNL Journey Optimizer]** – sem trabalho extra na solução de hospedagem. [Saiba como](dmarc-record.md#implement-dmarc)

* Se você configurou os subdomínios de envio com o [CNAME](delegate-subdomain.md#cname-subdomain-delegation), siga uma das opções abaixo:

   * Configure o DMARC nos subdomínios ou no domínio principal dos subdomínios **na sua solução de hospedagem**.
ou
   * Configure o DMARC nos subdomínios delegados **na interface de configuração do[!DNL Journey Optimizer]**. [Saiba como](dmarc-record.md#implement-dmarc)

  No entanto, a configuração do CNAME também requer entradas adicionais na solução de hospedagem. Consequentemente, certifique-se de coordenar com seu departamento de TI a realização da atualização detalhada [nesta seção](dmarc-record.md#implement-dmarc).

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>Se tiver dúvidas ou precisar de suporte, entre em contato com o consultor de capacidade de entrega da Adobe ou com o seu representante da Adobe.

**Links úteis:**

* Saiba mais sobre o DMARC no [Guia de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=pt-BR#about){target="_blank"}
* Leia o [Comunicado do Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Leia o [Comunicado do Yahoo!](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
