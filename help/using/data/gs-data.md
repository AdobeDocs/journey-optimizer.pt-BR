---
solution: Journey Optimizer
product: journey optimizer
title: Introdução aos dados em [!DNL Journey Optimizer]
description: Saiba como trabalhar com dados no [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: f418570a82d7b56dfb4c83df22b8109f506ec73a
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# Introdução ao gerenciamento de dados no [!DNL Journey Optimizer] {#about-data}

A riqueza e a cobertura dos dados do cliente final são as definições da força e do sucesso de qualquer solução de experiência do cliente; e esses dados são armazenados e de maior valor para qualquer cliente específico. A seleção de tecnologia agora é incorporada inerentemente com uma avaliação rigorosa dos recursos de gerenciamento de dados.

Com o Adobe Journey Optimizer, você pode gerenciar, manter e exportar facilmente esses dados para plataformas ou sistemas que fazem parte de sua pilha de tecnologia.

**Meus dados, Minhas regras** - O Journey Optimizer cria continuamente (e em tempo real) um conjunto avançado de dados de perfil do cliente, além de todos os dados de jornada e dados de oferta inerentes às suas operações. As versões Strawman dos dados do usuário assimilados de seus bancos de dados são enriquecidas e transformadas em dados de alto valor com cobertura e profundidade. Você quer que esses dados sejam seguros e, ao mesmo tempo, onipresentes, para que você possa aproveitar seu valor em todo o ecossistema de TI.

Em geral, a flexibilidade que você deseja de seus dados é três vezes:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinos" src="assets/do-not-localize/dest.png" /> 
    <br>Disponível em outros destinos - embora a Journey Optimizer sinalize e integre dados para uma experiência hiper-personalizada do cliente, você deseja que esses dados sejam usados em outros sistemas em seu cenário tecnológico geral, enquanto procura outras maneiras de aproveitar esses dados.
    <div>
     <a href="../start/ajo-integrations.md">Saiba mais</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="retenção" src="assets/do-not-localize/retention.png" />  
    <br>Rastreados por uma duração estipulada - Regulamentos do setor ou regionais (como GDPR ou CCPA) ou políticas internas de governança de dados estipulam por quanto tempo ou por quanto tempo, os dados precisam ser mantidos ou arquivados no Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Saiba mais</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="política" src="assets/do-not-localize/policy.png" /> 
    <br>Baseada excluída em um cronograma acordado ou em sua política - A exclusão de dados é um aspecto essencial da proteção de dados e é uma etapa fundamental em todos os processos de governança de dados. O Journey Optimizer pode produzir mais dados do que o necessário. Além disso, você deseja tomar o máximo cuidado com o que acontece após a duração necessária para um conjunto de dados, seja por causa do utilitário ou da regulamentação. O controle necessário é excluir dados em qualquer momento. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Saiba mais sobre higiene de dados na documentação do Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

O Adobe Experience Platform, no qual o Journey Optimizer é criado, fornece os níveis mais altos de controle dos dados para você - durante o engajamento também no final do engajamento. No Journey Optimizer, você tem controle total sobre os dados (que são trazidos ou gerados pelo Journey Optimizer), a governança sobreposta a esses dados e os destinos para os quais esses dados são enviados.

Todos os dados são considerados propriedade dos Clientes e só podem ser mantidos, criptografados, distribuídos ou destruídos a sua solicitação. O Adobe atua como fiduciário, sem direitos aos seus dados.

Você pode usar a flexibilidade de dados da Journey Optimizer para atender aos seus requisitos específicos relacionados à retenção, arquivamento ou exclusão de dados:

* **Extração/exportação de dados**: Você pode iniciar a extração dos dados de origem a qualquer momento por meio da API de acesso aos dados, sem penalidades ou atrasos. O [API de acesso a dados](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;} fornece aos usuários uma interface RESTful focada na capacidade de descoberta e acessibilidade de conjuntos de dados assimilados no Experience Platform. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Observe que o conteúdo usado em jornadas ou campanhas não pode ser extraído por meio da API ou dos métodos de Destino mencionados acima.

* **Retenção de dados do serviço de perfil**: Para dados de séries comportamentais e de tempo adicionados a qualquer Perfil, você pode optar por usar a configuração padrão da Journey Optimizer de manter esses dados por até 30 dias a partir da data de adição a um Perfil ou até um período de tempo alternativo selecionado por você. O tempo que o Adobe mantém esses dados varia de contrato para contrato e é descrito na política de retenção de dados de uma organização.

   Saiba mais sobre as expirações do evento de experiência em [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target=&quot;_blank&quot;}.

* **Mecanismos de limpeza e arquivamento**: A limpeza de dados e arquivamento pode ser definida e automatizada livremente no Journey Optimizer para automatizar as políticas de retenção de dados. É possível definir diferentes estratégias de envelhecimento para as diferentes entidades de dados. Os mecanismos de exportação também podem ser definidos para exportar automaticamente os dados antigos antes que sejam limpos ou arquivados.

   A área de trabalho Higiene de dados na interface do usuário do Adobe Experience Platform permite criar e monitorar várias tarefas de higiene de dados, incluindo a exclusão das identidades do consumidor e o agendamento das expirações do conjunto de dados. Saiba mais em [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

* **Data Lake e Exclusões**: Os dados do cliente armazenados no Data Lake podem ser retidos pela Journey Optimizer:

   * por sete dias para facilitar a integração dos dados do cliente nos serviços de perfil, após o que poderão ser permanentemente excluídos, ou
   * até que tenha escolhido ser excluído por você


* **Extração de Dados na Encerramento do Envolvimento/Saída**: Quando o contrato for rescindido, seus dados serão completamente removidos do espaço de armazenamento Adobe. Além disso, você pode extrair as extrações completas de perfil antes de encerrar um contrato. Não há custo adicional para esse recurso. Isso pode ser feito a qualquer momento e não apenas após o término.

Os métodos acima são definidos por contrato e detalhados no DPA (Data Processing Agreement, contrato de processamento de dados) que a Adobe concorda mutuamente com você no início de um contrato. Os aplicativos Adobe, incluindo a Journey Optimizer, são projetados em torno do princípio de que os dados de cada cliente sejam tratados como o ativo de dados proprietário desse cliente.
