---
solution: Journey Optimizer
product: journey optimizer
title: Introdução aos dados no Journey Optimizer
description: Saiba como trabalhar com dados no Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dados, gerenciamento, plataforma
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# Introdução ao gerenciamento de dados no [!DNL Journey Optimizer] {#about-data}

A riqueza e a cobertura dos dados do cliente final são as definições da força e do sucesso de qualquer solução de experiência do cliente; e esses dados são armazenados e de maior valor para qualquer cliente específico. A seleção de tecnologia agora é incorporada inerentemente com uma avaliação rigorosa dos recursos de gerenciamento de dados.

Com [!DNL Adobe Journey Optimizer], você pode gerenciar, manter e exportar facilmente esses dados para plataformas ou sistemas que fazem parte da sua pilha de tecnologia.

**Meus dados, Minhas regras** - [!DNL Adobe Journey Optimizer] O continuamente (e em tempo real) cria um conjunto avançado de dados de perfil do cliente, além de todos os dados de jornada e dados de oferta inerentes às suas operações. As versões Strawman dos dados do usuário assimilados de seus bancos de dados são enriquecidas e transformadas em dados de alto valor com cobertura e profundidade. Você quer que esses dados sejam seguros e, ao mesmo tempo, onipresentes, para que você possa aproveitar seu valor em todo o ecossistema de TI.

Em geral, a flexibilidade que você deseja de seus dados é:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinos" src="assets/do-not-localize/dest.png" /> 
    <br>Disponível em outros destinos - While [!DNL Adobe Journey Optimizer] sinaliza e integra dados para uma experiência hiper-personalizada do cliente, você quer esses dados em outros sistemas em seu panorama técnico geral, enquanto procura outras maneiras de aproveitar esses dados.
    <div>
     <a href="../start/ajo-integrations.md">Saiba mais</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="política" src="assets/do-not-localize/policy.png" /> 
    <br>Baseada excluída em um cronograma acordado ou em sua política - A exclusão de dados é um aspecto essencial da proteção de dados e é uma etapa fundamental em todos os processos de governança de dados. [!DNL Adobe Journey Optimizer] pode produzir mais dados do que o necessário. Além disso, você deseja tomar o máximo cuidado com o que acontece após a duração necessária para um conjunto de dados, seja por causa do utilitário ou da regulamentação. O controle necessário é excluir dados em qualquer momento. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Saiba mais</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], em que [!DNL Adobe Journey Optimizer] O é criado, fornece os níveis mais altos de controle dos dados para você, durante o engajamento e também no final do engajamento. Within [!DNL Journey Optimizer], você tem controle total sobre os dados (que são trazidos para ou gerados por, [!DNL Journey Optimizer]), a governança sobreposta a esses dados e os destinos para os quais esses dados são enviados.

Todos os dados são considerados propriedade dos Clientes e só podem ser mantidos, criptografados, distribuídos ou destruídos a sua solicitação. O Adobe atua como fiduciário, sem direitos aos seus dados.

Você pode usar o [!DNL Journey Optimizer]A flexibilidade dos dados do para atender aos requisitos específicos relacionados à retenção, arquivamento ou exclusão de dados:

* **Extração/exportação de dados**: Você pode iniciar a extração dos dados de origem a qualquer momento por meio da API de acesso aos dados, sem penalidades ou atrasos. O [API de acesso a dados](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} fornece aos usuários uma interface RESTful focada na capacidade de descoberta e acessibilidade de conjuntos de dados assimilados dentro do [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Observe que o conteúdo usado em jornadas ou campanhas não pode ser extraído por meio da API ou dos métodos de Destino mencionados acima.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Mecanismos de limpeza e arquivamento**: A limpeza de dados e arquivamento pode ser definida e automatizada livremente no [!DNL Adobe Journey Optimizer] para automatizar as políticas de retenção de dados. É possível definir diferentes estratégias de envelhecimento para as diferentes entidades de dados. Os mecanismos de exportação também podem ser definidos para exportar automaticamente os dados antigos antes que sejam limpos ou arquivados.

   O espaço de trabalho Higiene de dados permite criar e monitorar várias tarefas de higiene de dados, incluindo a exclusão de identidades de consumidores e o agendamento de expirações do conjunto de dados. Este espaço de trabalho está disponível com o Security &amp; Privacy Shield e com o Healthcare Shield. Saiba mais [nesta página](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Extração de Dados na Encerramento do Envolvimento/Saída**: Quando o contrato for rescindido, seus dados serão completamente removidos do espaço de armazenamento Adobe. Além disso, você pode extrair as extrações completas de perfil antes de encerrar um contrato. Não há custo adicional para esse recurso. Isso pode ser feito a qualquer momento e não apenas após o término.

Os métodos acima são definidos por contrato e detalhados no DPA (Data Processing Agreement, contrato de processamento de dados) que a Adobe concorda mutuamente com você no início de um contrato. aplicativos de Adobe, incluindo [!DNL Journey Optimizer], são criados em torno do princípio de que os dados de cada cliente sejam tratados como ativos de dados proprietários desse cliente.
