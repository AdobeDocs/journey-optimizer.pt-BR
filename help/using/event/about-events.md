---
title: Sobre eventos
description: Saiba mais sobre eventos
feature: Eventos
topic: Administração
role: Administrator
level: Intermediate
source-git-commit: 6e2526bd3c80ad2bff59502c6537a3e2213f7bf7
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 31%

---

# Sobre eventos{#concept_gfj_fqt_52b}

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Sobre eventos"
>abstract="Um evento está vinculado a uma pessoa. Relaciona-se com o comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site, etc.) ou com algo que acontece ligado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos no programa de fidelidade). É o que o [!DNL Journey Optimizer] escutará nas jornadas para orquestrar as melhores ações futuras."

A configuração do evento permite definir as informações que o [!DNL Journey Optimizer] receberá como eventos. É possível usar vários eventos (em etapas diferentes de uma jornada) e várias jornadas podem usar o mesmo evento.

>[!CAUTION]
>
>A configuração do evento é **mandatory** e deve ser executada por um **usuário técnico**.

Você pode configurar dois tipos de eventos:

* **** Unitaryevents: esses eventos estão vinculados a uma pessoa. Elas estão relacionadas ao comportamento de uma pessoa (por exemplo, uma pessoa comprou um produto, visitou uma loja, saiu de um site etc.) ou com algo que acontece ligado a uma pessoa (por exemplo, uma pessoa atingiu 10.000 pontos no programa de fidelidade). É o que o [!DNL Journey Optimizer] escutará nas jornadas para orquestrar as melhores ações futuras. Eventos unários podem ser baseados em regras ou gerados pelo sistema. Para saber como criar um evento unitário, consulte esta [página](../event/about-creating.md).

* **** Eventos de negócios: um evento comercial é um evento que, ao contrário de um evento unitário, não está vinculado a um perfil específico. Por exemplo, pode ser um alerta de notícias, uma atualização de esportes, uma alteração ou cancelamento de voo, uma atualização de inventário, eventos climáticos etc. Embora esses eventos não sejam específicos de um perfil, eles podem ser de interesse para qualquer número de perfis: pessoas subscritas em determinados tópicos noticiosos, passageiros de um voo, compradores interessados em um produto esgotado, etc. Os eventos comerciais sempre se baseiam em regras. Quando você solta um evento comercial em uma jornada, ele adiciona automaticamente uma atividade **Read segment** logo em seguida. Para saber como criar um evento comercial, consulte esta [página](../event/about-creating-business.md).


>[!NOTE]
>
>Se você editar um evento usado em um rascunho ou em uma jornada ao vivo, será possível apenas alterar o nome, a descrição ou adicionar campos de carga útil. Limitamos rigorosamente a edição de rascunho ou jornadas ao vivo para evitar a quebra de jornadas.

## Tipo de ID de evento{#event-id-type}

Para eventos comerciais, o tipo de ID de evento sempre se baseia em regras.

Para eventos unitários, há dois tipos de ID de evento:

* **Baseados** em regras: esse tipo de evento não gera uma eventID. Usando o editor de expressões simples, basta definir uma regra que será usada pelo sistema para identificar os eventos relevantes que acionarão suas jornadas. Essa regra pode ser baseada em qualquer campo disponível no payload do evento, por exemplo, o local do perfil ou o número de itens adicionados ao carrinho do perfil.

   >[!CAUTION]
   >
   >Uma regra de limitação é definida para eventos com base em regras. Limita o número de eventos qualificados que uma jornada pode processar para 5000 por segundo em uma determinada organização (ORG). Corresponde aos SLAs do Journey Optimizer. Consulte esta [página](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **Eventos** gerados pelo sistema: esses eventos exigem uma eventID. Esse campo eventID é gerado automaticamente ao criar o evento. O sistema que envia o evento não deve gerar uma ID, mas sim passar a disponível na pré-visualização de carga.

O Journey Optimizer requer que os eventos sejam transmitidos ou armazenados em lote no Adobe Experience Platform. Esses dados não precisam necessariamente acessar o Perfil em tempo real. Se você quiser usar os eventos para segmentação ou pesquisa em uma jornada separada, recomendamos ativar o conjunto de dados para perfil.

## Ciclo de dados {#section_r1f_xqt_pgb}

Eventos são chamadas POST API. Os eventos são enviados para a Adobe Experience Platform por meio de APIs de assimilação de fluxo. O destino do URL de eventos enviados por meio de APIs de mensagens transacionais é chamado de &quot;inlet&quot;. A carga útil de eventos segue a formatação XDM.

A carga útil contém informações necessárias para que as APIs de assimilação de fluxo funcionem (no cabeçalho) e as informações necessárias para que [!DNL Journey Optimizer] funcione e as informações que serão usadas nas jornadas (no corpo, por exemplo, a quantidade de um carrinho abandonado). Há dois modos para a assimilação de fluxo, autenticados e não autenticados. Para obter detalhes sobre as APIs de assimilação de fluxo, consulte [este link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=pt-BR).

Após chegar pelas APIs de assimilação de fluxo contínuo, os eventos fluem para um serviço interno chamado Pipeline e, em seguida, para o Adobe Experience Platform. Se o schema do evento tiver o sinalizador de Serviço de perfil do cliente em tempo real ativado e uma ID de conjunto de dados que também tenha o sinalizador de Perfil do cliente em tempo real, ele fluirá para o Serviço de perfil do cliente em tempo real.

Para eventos gerados pelo sistema, o Pipeline filtra eventos que têm uma carga útil contendo [!DNL Journey Optimizer] eventIDs (consulte o processo de criação de eventos abaixo) fornecidas por [!DNL Journey Optimizer] e contidas na carga útil do evento. Para eventos com base em regras, o sistema identifica o evento usando a condição eventID. Esses eventos são acompanhados pelo [!DNL Journey Optimizer] e a jornada correspondente é acionada.
