---
solution: Journey Optimizer
product: journey optimizer
title: Upload personalizado (CSV) e composição de público federado
description: Saiba mais sobre as principais informações e práticas recomendadas ao trabalhar com uploads personalizados (CSV) e públicos-alvo de composição de público federado.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 6%

---

# Upload personalizado (CSV) e composição de público federado {#csv-fac}

## Sobre upload personalizado e composição de público federado {#about}

Além das definições de segmento e composição de público-alvo, o [!DNL Journey Optimizer] permite gerar e direcionar públicos-alvo importando-os de um arquivo CSV ou aproveitando os dados do data warehouse.

* **Upload personalizado**: importe um público usando um arquivo CSV. Saiba como importar públicos na [documentação do Serviço de segmentação](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} do Adobe Experience Platform.

* **Composição de Público-Alvo Federado**: federe conjuntos de dados diretamente do data warehouse existente para compilar e enriquecer públicos-alvo e atributos da Adobe Experience Platform, tudo em um único sistema. Leia o guia em [Composição de Público-Alvo Federado](https://experienceleague.adobe.com/pt-br/docs/federated-audience-composition/using/home).

  >[!AVAILABILITY]
  >
  >No momento, a Composição de público-alvo federado está disponível apenas para um conjunto de organizações (Disponibilidade limitada). Para obter mais informações, entre em contato com o(a) representante da Adobe.

Você pode direcionar esses públicos-alvo no Journey Optimizer ou ativá-los para qualquer destino compatível com o Adobe Experience Platform

➡️ [Descubra estes recursos no vídeo](#video)

## Leitura obrigatória {#must-read}

Esta seção fornece informações principais para ter em mente ao trabalhar com o Upload personalizado (arquivos CSV) e públicos-alvo de composição de público-alvo federado.

* **Suporte para visualização e prova:** Atualmente, não há suporte para visualização e prova para públicos-alvo criados por meio de carregamento CSV ou Composição de Público Federado. Lembre-se disso ao planejar suas campanhas.

* **Atraso de ativação:** os públicos-alvo estão prontos para uso no Journey Optimizer logo após a conclusão da assimilação. Embora isso normalmente ocorra em uma hora, está sujeito a alguma variabilidade.

* **Registros ativados e identificação de identidade:** todos os registros do público-alvo são ativados, incluindo duplicatas. Durante a próxima exportação de perfil da UPS, esses registros passarão pela compilação de identidade. Como resultado, o número de registros ativados pode diferir do número de perfis após a identificação de identidade.

* **Direcionamento de novos perfis:** Quando uma correspondência não é encontrada entre um registro e um perfil UPS, um novo perfil vazio é criado. Este perfil está vinculado aos atributos de enriquecimento que são armazenados no data lake. Como esse novo perfil está vazio, os campos de direcionamento normalmente usados no Journey Optimizer (por exemplo, personalEmail.address, mobilePhone.number) estão vazios e, portanto, não podem ser usados para direcionamento.

  Para resolver isso, você pode especificar o &quot;campo de execução&quot; (ou o &quot;endereço de execução&quot; dependendo do canal) na configuração do canal como &quot;identityMap&quot;. Isso garantirá que o atributo escolhido como a identidade na criação do público-alvo será aquele usado para o direcionamento no Journey Optimizer.

## Vídeos tutoriais {#video}

Saiba como fazer upload de públicos-alvo no formato CSV na Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

Saiba mais sobre Composição de público-alvo federado.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
