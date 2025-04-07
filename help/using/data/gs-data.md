---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao gerenciamento de dados no Journey Optimizer
description: Saiba como trabalhar com dados no Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dados, gerenciamento, plataforma
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 99%

---

# Introdução ao gerenciamento de dados {#about-data}

A riqueza e a cobertura dos dados do cliente final é o que define a força e o sucesso de qualquer solução de experiência do cliente, e esses dados são pessoais e de maior valor para qualquer cliente. A seleção de tecnologia agora está inerentemente integrada, com avaliação rigorosa dos recursos de gerenciamento de dados.

Com o [!DNL Adobe Journey Optimizer], você pode gerenciar, manter e exportar facilmente esses dados para plataformas ou sistemas que fazem parte de sua pilha de tecnologia. 

**Meus dados, minhas regras**: o [!DNL Adobe Journey Optimizer] cria continuamente (e em tempo real) um conjunto avançado de dados de perfil do cliente, além de todos os dados de jornada e de oferta inerentes às suas operações. As versões Strawman dos dados do usuário assimilados de seus bancos de dados são enriquecidos e transformados em dados de alto valor com cobertura e profundidade. Você quer que esses dados sejam seguros e, ao mesmo tempo, universais, para poder aproveitar seu valor em todo o ecossistema de TI.

Em termos gerais, a flexibilidade que você deseja dos seus dados é:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinos" src="assets/do-not-localize/dest.png" /> 
    <br>Disponível em outros destinos: embora o [!DNL Adobe Journey Optimizer] sincronize e integre dados para obter uma experiência do cliente hiperpersonalizada, você deseja que esses dados estejam em outros sistemas no seu cenário tecnológico geral e, ao mesmo tempo, procura outras maneiras de aproveitar esses dados.
    <div>
     <a href="../integrations/ajo-integrations.md">Saiba mais</a></div>
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
    <br>Excluído com base em uma linha do tempo acordada ou em sua política: a exclusão de dados é um aspecto crítico da proteção de dados e uma etapa essencial em todos os processos de governança de dados. O [!DNL Adobe Journey Optimizer] pode produzir mais dados do que o necessário. Além disso, você deseja ter o máximo cuidado com o que acontece após a duração necessária para um conjunto de dados, seja por causa de utilidade ou regulamentação. O controle necessário é excluir dados em um determinado momento. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Saiba mais</a></div>
    </div>
  </td>
</tr>
</table>

O [!DNL Adobe Experience Platform], em que o [!DNL Adobe Journey Optimizer] é criado, fornece os mais altos níveis de controle de dados para você, durante e após o engajamento. No [!DNL Journey Optimizer], você tem controle total sobre os dados (trazidos ou gerados pelo [!DNL Journey Optimizer]), a governança sobreposta a esses dados e os destinos para os quais esses dados são enviados.

Todos os dados são considerados propriedade dos clientes e só podem ser mantidos, criptografados, distribuídos ou destruídos mediante sua solicitação. A Adobe atua como seu fiduciário, sem absolutamente nenhum direito sobre seus dados.

Você pode usar a flexibilidade de dados do [!DNL Journey Optimizer] para atender aos requisitos específicos relacionados à retenção, ao arquivamento ou à exclusão de dados:

* **Extração/exportação de dados**: é possível iniciar a extração de dados de origem a qualquer momento por meio da API de acesso a dados sem penalidades ou atrasos. A [API de acesso a dados](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=pt-BR){target="_blank"} fornece aos usuários uma interface RESTful focada na capacidade de descoberta e acessibilidade de conjuntos de dados assimilados no [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  Observe que o conteúdo usado em jornadas ou campanhas não pode ser extraído por meio da API ou dos métodos de destino mencionados acima.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Mecanismos de limpeza e arquivamento**: a limpeza de dados e o arquivamento podem ser definidos e automatizados livremente no [!DNL Adobe Journey Optimizer] para automatizar as políticas de retenção de dados. É possível definir diferentes estratégias de envelhecimento para as diferentes entidades de dados. Os mecanismos de exportação também podem ser definidos para exportar automaticamente os dados antigos antes que eles sejam removidos ou arquivados.

  O espaço de trabalho Ciclo de vida de dados permite criar e monitorar várias tarefas de ciclo de vida de dados, incluindo a exclusão de identidades de consumidores e o agendamento de expirações de conjuntos de dados. Esse espaço de trabalho está disponível com o Security &amp; Privacy Shield e com o Healthcare Shield. Saiba mais sobre [esta página](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Extração de dados na recisão/saída do engajamento**: quando o contrato for rescindido, seus dados serão completamente removidos do espaço de armazenamento da Adobe. Além disso, você pode obter extrações completas de perfis antes de rescindir um contrato. Não há custo adicional para este recurso. Isso pode ser feito a qualquer momento e não apenas após a rescisão.

Os métodos acima são definidos e detalhados no contrato de processamento de dados (DPA) que a Adobe concorda mutuamente com você no início de um engajamento. Os aplicativos da Adobe, inclusive o [!DNL Journey Optimizer], são projetados com base no princípio de que os dados de cada cliente são tratados como ativos de dados proprietários desse cliente.
