---
solution: Journey Optimizer
product: journey optimizer
title: Atualização DMARC obrigatória
description: Saiba por que e quando você deve definir o registro DMARC no Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: subdomínio, domínio, correio, dmarc, registro
source-git-commit: 7cbd6a9e80a8d6b87b3c3011db80549a3b5f6e73
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Atualização DMARC obrigatória {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Saiba mais sobre a atualização DMARC obrigatória"
>abstract="Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigirão uma **Registro DMARC** para qualquer domínio que você usar para enviar emails para eles. Este novo requisito começa em **1 de fevereiro de 2024**. <br>Consequentemente, o Adobe recomenda que você garanta que tenha o registro DMARC configurado para todos os subdomínios que você delegou ao Adobe no Journey Optimizer."

Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigirão uma **Registro DMARC** para qualquer domínio que você usar para enviar emails para eles. Este novo requisito começa em **1 de fevereiro de 2024**.

Saiba mais sobre os requisitos do Google e do Yahoo em [nesta seção](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>O não cumprimento desse novo requisito por parte do Gmail e do Yahoo deve resultar no bloqueio dos emails que chegam à pasta de spam.

Consequentemente, a Adobe recomenda que você garanta que tenha o registro DMARC configurado para todos os subdomínios que você delegou à Adobe no [!DNL Journey Optimizer]. Siga uma das duas opções abaixo:

* Configure o DMARC nos subdomínios ou no domínio principal dos subdomínios, **na sua solução de hospedagem**.

* Configurar DMARC nos subdomínios delegados **usar o recurso futuro no [!DNL Journey Optimizer] interface de administração** - sem trabalho extra na solução de hospedagem.

  >[!CAUTION]
  >
  >Se você configurou o [Delegação CNAME](delegate-subdomain.md#cname-subdomain-delegation) para os subdomínios de envio, também será necessária alguma entrada na solução de hospedagem. Certifique-se de coordenar com o departamento de TI para que ele possa realizar a atualização assim que a [!DNL Journey Optimizer] O recurso está disponível (em 30 de janeiro de 2024). <!--and be ready on February 1st, 2024-->

  Mais detalhes sobre o [!DNL Journey Optimizer] O próximo recurso DMARC será lançado em breve.

<!--
* If you have [fully delegated](delegate-subdomain.md#full-subdomain-delegation) your sending subdomains to Adobe, follow either one of the two options below:

    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution.

* If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, follow either one of the two options below:
    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.
    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI**. However, it will also require entry in your hosting solution. Consequently, make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January, 30) - and be ready on February 1st, 2024.
    
-->

>[!NOTE]
>
>Se tiver dúvidas ou precisar de suporte, entre em contato com seu consultor de capacidade de entrega da Adobe ou com seu representante da Adobe.

As linhas do tempo mais recentes compartilhadas pela Google e pelo Yahoo são as seguintes:

* Google:

   * **Fevereiro de 2024** - As rejeições temporárias projetadas para fornecer aviso de não conformidade serão iniciadas. Os e-mails ainda serão entregues normalmente após um pequeno atraso se você ainda não estiver em conformidade. Se você estiver em total conformidade, não haverá rejeições temporárias e você não será afetado.

   * **Abril de 2024** - Os blocos serão iniciados para remetentes que não estão em conformidade com o requisito DMARC. Somente uma parte do e-mail incompatível será bloqueada no início, com a porcentagem bloqueada aumentando com o tempo.

   * **1º de junho de 2024** - Qualquer remetente que não estiver em total conformidade terá bloqueio.

* O Yahoo não forneceu datas exatas, mas disse que &quot;a implantação da fiscalização terá início em fevereiro de 2024. A execução será gradualmente implementada&quot;.

>[!NOTE]
>
>Saiba mais sobre a implementação do DMARC na [Guia de práticas recomendadas de capacidade de delivery](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} para entender melhor o impacto na capacidade de delivery de emails.
