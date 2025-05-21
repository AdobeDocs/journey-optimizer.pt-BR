---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos-alvo da Adobe Experience Platform
description: Saiba como trabalhar com públicos-alvo da Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: c52049383bf6a8b60fcb0ab1c2331724c8cdb771
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 22%

---

# Ativação de público em [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Você pode selecionar em campanhas e jornadas qualquer público gerado usando definições de segmento, upload personalizado, fluxos de trabalho de composição ou Composição de público federado.

>[!AVAILABILITY]
>
>O uso de públicos-alvo e atributos da composição de público-alvo está indisponível para uso com o Healthcare Shield ou o Privacy and Security Shield. [Saiba como usar atributos de enriquecimento de públicos no Journey Optimizer](../audience/about-audiences.md#enrichment)

## Atraso de ativação de públicos-alvo {#activation}

Os públicos-alvo estão prontos para uso no Journey Optimizer logo após a conclusão da assimilação. Embora isso normalmente ocorra em uma hora, está sujeito a alguma variabilidade. Os públicos-alvo resultantes de composições devem estar disponíveis 24 horas após a publicação.

Para públicos resultantes de trabalhos de segmentação em lote, a ativação pode ser atrasada devido à variabilidade da assimilação em lote. Para jornadas de leitura de público agendadas diariamente, você pode definir uma janela de tempo nas propriedades da jornada para garantir que dados novos do público-alvo estejam disponíveis antes da execução da jornada. Se o trabalho de segmentação não for concluído dentro da janela de tempo definida, a jornada será ignorada até a próxima ocorrência. [Saiba como agendar uma jornada de leitura de público-alvo](../building-journeys/read-audience.md)

## Composição de upload personalizado e público-alvo federado

Para públicos-alvo de upload personalizado e composição de público-alvo federado, observe as seguintes medidas de proteção:

* **Suporte para visualização e prova:** Atualmente, não há suporte para visualização e prova para públicos-alvo criados por meio de carregamento CSV ou Composição de Público Federado. Lembre-se disso ao planejar suas campanhas.

* **Direcionamento de novos perfis:** Quando uma correspondência não é encontrada entre um registro e um perfil UPS, um novo perfil vazio é criado. Este perfil está vinculado aos atributos de enriquecimento que são armazenados no data lake. Como esse novo perfil está vazio, os campos de direcionamento normalmente usados no Journey Optimizer (por exemplo, personalEmail.address, mobilePhone.number) estão vazios e, portanto, não podem ser usados para direcionamento.

  Para resolver isso, você pode especificar o &quot;campo de execução&quot; (ou o &quot;endereço de execução&quot; dependendo do canal) na configuração do canal como &quot;identityMap&quot;. Isso garantirá que o atributo escolhido como a identidade na criação do público-alvo será aquele usado para o direcionamento no Journey Optimizer.

* **Registros ativados e identificação de identidade:** todos os registros do público-alvo são ativados, incluindo duplicatas. Durante a próxima exportação de perfil da UPS, esses registros passarão pela compilação de identidade. Como resultado, o número de registros ativados pode diferir do número de perfis após a identificação de identidade.

## Públicos-alvo em [!DNL Journey Optimizer]

É possível aproveitar os públicos-alvo no **[!DNL Journey Optimizer]** de maneiras diferentes:

* Escolha um público para uma **campanha**, na qual a mensagem é enviada a todas as pessoas que pertencem ao público-alvo selecionado. [Saiba como definir o público-alvo de uma campanha](../campaigns/create-campaign.md#define-the-audience-audience).

* Use uma atividade de orquestração de **Ler público** em uma jornada para fazer com que todos os indivíduos do público entrem na jornada e recebam as mensagens incluídas na jornada. Digamos que você tenha um público-alvo de “cliente prata”. Com essa atividade, você pode fazer com que todos os clientes prata entrem em uma jornada e enviar-lhes uma série de mensagens personalizadas. [Saiba como configurar uma atividade Ler público-alvo](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  >[!NOTE]
  >
  >Qualquer jornada que utilize um público-alvo da composição de público-alvo ou do upload personalizado na atividade &quot;Ler público-alvo&quot; terá atributos de perfil tão novos quanto a última avaliação em lote. Isso inclui consentimento/supressões na jornada.

* Use a atividade **Condição** em uma jornada para criar condições com base na associação de público-alvo. [Saiba como usar públicos-alvo em condições](../building-journeys/condition-activity.md#using-a-segment).

* Use a atividade de evento **Qualificação de público-alvo** em uma jornada para fazer com que os indivíduos entrem ou avancem na jornada com base nas entradas e saídas do público-alvo da Adobe Experience Platform. Por exemplo, é possível fazer com que todos os novos clientes prata entrem em uma jornada e enviar-lhes mensagens. Para obter mais informações sobre como usar essa atividade, consulte [Saiba como configurar uma atividade de qualificação de público-alvo](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Devido à natureza em lote de públicos-alvo criados usando workflows de composição, upload personalizado ou Composição de público-alvo federado, não é possível direcionar esses públicos-alvo em uma atividade de &quot;Qualificação de público-alvo&quot;. Somente públicos-alvo criados usando definições de segmento podem ser aproveitados nessa atividade.
