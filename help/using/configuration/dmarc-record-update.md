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
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Atualização importante do registro DMARC{#dmarc-record}


>[!CAUTION]
>
>Seguindo os anúncios recentes do Gmail e do Yahoo para remetentes em massa, a Journey Optimizer agora é compatível com a tecnologia de autenticação DMARC.

Como parte da aplicação de práticas recomendadas do setor, a Google e o Yahoo exigirão que você tenha um registro DMARC para qualquer domínio usado para enviar emails para eles. Este novo requisito começa em **1 de fevereiro de 2024**.

Saiba mais sobre os requisitos do Google e do Yahoo para registro DMARC em [nesta seção](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Saiba mais sobre as alterações anunciadas no Google e no Yahoo em [esta página](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Em seguida, você terá uma ação ou as próximas etapas da seção que indicará:

Você precisa configurá-la para todos os seus subdomínios
* Se tiver delegado totalmente o domínio a nós, você terá duas opções
   * Configurar DMARC no domínio pai do domínio delegado na solução de hospedagem OU
   * Configure o DMARC no domínio delegado usando nosso próximo recurso na interface do administrador sem trabalho extra na solução de hospedagem
* Se você tiver configurado o CNAME para os domínios de envio, terá duas opções
   * Configurar DMARC no subdomínio OU no domínio principal do subdomínio na solução de hospedagem OU
   * Configure o DMARC usando nosso recurso futuro na interface do administrador. No entanto, isso exigirá não apenas nossa interface do usuário, mas também a entrada na solução de hospedagem.

Mais detalhes sobre nosso próximo recurso serão divulgados em breve.

Além disso, você pode incluir o impacto, se não estiver definido copiando a seção relevante para o DMARC da seção abaixo (copiada do link acima). Ou extraímos apenas coisas relacionadas ao DMARC. Ou aqui você pode informar que o anúncio é para DMARC e um clique unsub e aqui está a mais recente sobre linhas do tempo para ambos os recursos.

As atualizações das linhas do tempo estão disponíveis desde o anúncio original de outubro.

As linhas do tempo mais recentes se parecem com:

Gmail:

* Fevereiro de 2024 - As rejeições temporárias projetadas para fornecer aviso de não conformidade serão iniciadas. Os e-mails ainda serão entregues normalmente após um pequeno atraso se você ainda não estiver em conformidade. Se você estiver em total conformidade, não haverá rejeições temporárias e você não perceberá nada.
* Abril de 2024 - Os blocos começarão para remetentes que não estiverem em conformidade com tudo, exceto List-Unsubscribe 1-Click. Somente uma parte do email incompatível será bloqueada no início, com a % de bloqueio aumentando com o tempo.
* 1º de junho de 2024 - Qualquer remetente que não estiver em total conformidade, incluindo o List-Unsubscribe 1-Click, receberá bloqueio.

Yahoo:

Não forneceu datas exatas, mas disse que &quot;a implantação da fiscalização terá início em fevereiro de 2024. A execução será gradualmente implementada&quot;.
