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
source-git-commit: 745474d6232f01ee959db8d706110477ed0220e2
workflow-type: ht
source-wordcount: '561'
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

  >[!IMPORTANT]
  >
  >No entanto, a configuração do CNAME também requer entradas adicionais na solução de hospedagem. Consequentemente, certifique-se de coordenar com seu departamento de TI a realização da atualização detalhada [nesta seção](dmarc-record.md#implement-dmarc).

As linhas do tempo mais recentes compartilhadas pelo Google e Yahoo! são as seguintes:

* Google:

   * **Fevereiro de 2024**: rejeições temporárias projetadas para fornecer aviso de não conformidade serão iniciadas. Os emails ainda serão entregues normalmente após um pequeno atraso se você ainda não estiver em conformidade. Se você estiver em total conformidade, não haverá rejeições temporárias e você não será afetado.

   * **Abril de 2024**: os blocos serão iniciados para remetentes que não estiverem em conformidade com o requisito DMARC. Somente uma parte dos emails que não estiverem em conformidade será bloqueada no início, com a porcentagem aumentando ao longo do tempo.

   * **1º de junho de 2024**: qualquer remetente que não estiver em total conformidade será bloqueado.

* O Yahoo! não forneceu datas exatas, mas informou que: “A implantação da aplicação terá início em fevereiro de 2024. A aplicação será gradualmente implementada&quot;.

>[!NOTE]
>
>Se tiver dúvidas ou precisar de suporte, entre em contato com o consultor de capacidade de entrega da Adobe ou com o seu representante da Adobe.

**Links úteis:**

* Saiba mais sobre o DMARC no [Guia de práticas recomendadas de capacidade de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=pt-BR#about){target="_blank"}
* Leia o [Comunicado do Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Leia o [Comunicado do Yahoo!](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
