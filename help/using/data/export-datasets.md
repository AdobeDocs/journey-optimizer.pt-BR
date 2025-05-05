---
solution: Journey Optimizer
product: journey optimizer
title: Exportar conjuntos de dados para locais de armazenamento na nuvem
description: Saiba como exportar seus conjuntos de dados usando destinos de armazenamento na nuvem do Adobe Experience Platform.
feature: Datasets
role: User
level: Beginner
keywords: plataforma, data lake, criar, lake, conjuntos de dados, perfil
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 6%

---

# Exportar conjuntos de dados para locais de armazenamento na nuvem {#export-datasets}

O Journey Optimizer permite estabelecer uma conexão ativa com locais de armazenamento na nuvem para exportar o conteúdo de seus conjuntos de dados.

Ao exportar seus dados periodicamente, você pode garantir um registro completo e atualizado das interações com o cliente, disponibilizando-o prontamente para fins de emissão de relatórios, arquivamento ou análise de dados.

## Destinos de armazenamento na nuvem disponíveis {#destinations}

Você pode exportar conjuntos de dados para 6 destinos de armazenamento na nuvem que podem ser acessados pelo menu **[!UICONTROL Destinos]**, na guia **[!UICONTROL Catálogo]**.

![](assets/dataset-export-setup.png)

Informações detalhadas sobre cada destino estão disponíveis na documentação do Adobe Experience Platform:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html?lang=pt-BR){target="_blank"}
* [Blob do Azure](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html?lang=pt-BR){target="_blank"}
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html?lang=pt-BR){target="_blank"}
* [Zona de aterrissagem de dados](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html?lang=pt-BR){target="_blank"}
* [Armazenamento na nuvem do Google](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html?lang=pt-BR){target="_blank"}
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html?lang=pt-BR){target="_blank"}.


## Pré-requisitos {#prerequisites}

Para exportar conjuntos de dados, você precisa das [permissões de controle de acesso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=pt-BR#permissions){target="_blank"} listadas abaixo. Leia a [visão geral do controle de acesso](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html?lang=pt-BR){target="_blank"} ou contate o administrador do produto para obter as permissões necessárias.

| Categoria | Permissão |
|--|--|
| Destinos | Gerenciar e ativar destinos do conjunto de dados |
| Gerenciamento de dados | Exibir conjuntos de dados |
| Destinos | Exibir destinos |

## Etapas principais para exportar conjuntos de dados {#main-steps}

As principais etapas para exportar um conjunto de dados para um local de armazenamento na nuvem são as seguintes:

![](assets/dataset-export-process.png)

Informações detalhadas sobre cada etapa estão disponíveis na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=pt-BR){target="_blank"}.

1. **Configurar o destino do armazenamento na nuvem**. Se ainda não tiver feito isso, conecte-se a um destino de armazenamento na nuvem no catálogo de destinos. Saiba como criar uma nova conexão de destino na [documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=pt-BR#setup){target="_blank"}.

   <!--![](assets/dataset-export-setup.png)-->

1. **Selecione o destino do armazenamento na nuvem** para o qual deseja exportar seus conjuntos de dados. No catálogo de destinos, clique no botão **[!UICONTROL Exportar conjuntos de dados]** no cartão desejado e selecione a conexão a ser usada.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Se você estiver usando o Adobe Journey Optimizer juntamente com perfis de clientes em tempo real, os cartões de destino exibirão o botão **Ativar**, permitindo exportar conjuntos de dados e ativar públicos para esse destino, dependendo das permissões habilitadas.

1. **Selecione o(s) conjunto(s) de dados** que deseja exportar para o destino selecionado. [Saiba mais sobre os conjuntos de dados do Journey Optimizer disponíveis para exportação](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Agende a exportação** do seu conjunto de dados. Especifique quando a exportação deve começar e em que frequência ela deve ocorrer.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Revise e confirme a exportação** verificando o resumo exibido no final da configuração.

   <!--![](assets/dataset-export-review.png)-->

Quando a exportação for concluída, o conteúdo do conjunto de dados será depositado no local de armazenamento na nuvem de acordo com o agendamento configurado. [Saiba como verificar a exportação bem-sucedida do conjunto de dados](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=pt-BR#verify){target="_blank"}.

## Conjuntos de dados disponíveis para exportação {#datasets}

Entenda na tabela abaixo quais conjuntos de dados do Journey Optimizer você pode exportar.

| Conjunto de dados | Descrição |
| ------- | ------- | 
| Conjunto de dados do evento de feedback CCO do AJO | Conjunto de dados do evento de feedback CCO do AJO |
| Conjunto de dados de classificação do AJO | Conjunto de dados para assimilar eventos de feedback de aplicativos de email e por push do Journey Optimizer. Criado por meio do SDK. |
| Conjunto de dados do serviço de consentimento da AJO | Armazena informações de consentimento de um perfil. |
| Conjunto de dados de evento de experiência de rastreamento de email do AJO | Logs de interação para o canal de email, que é usado para fins de criação de relatórios e público-alvo.  |
| Conjunto de dados da entidade AJO | Conjunto de dados para armazenar metadados de entidade para mensagens enviadas ao usuário final.  |
| Conjunto de dados do evento de atividade de entrada do AJO | Conjunto de dados para canais na Web e no aplicativo do Journey Optimizer para eventos de entrega e interação. |
| Conjunto de dados do perfil de mensagens interativas da AJO | Armazena perfis criados para oferecer suporte a campanhas acionadas por API |
| Conjunto de dados do evento de feedback de mensagem do AJO | Logs de entrega de mensagens. Informações sobre todas as entregas de mensagens do Journey Optimizer para fins de criação de relatórios e de público-alvo. O feedback dos ISPs de email sobre rejeições também é registrado neste conjunto de dados. |
| Extensão Contadores de perfis do AJO | Contém um mapa de objetos contendo counter_value e expiryDate, digitado por counter_id |
| Conjunto de dados do perfil push do AJO | Armazena tokens de push de um perfil. |
| Conjunto de dados de evento de experiência de rastreamento de push do AJO | Logs de interação para canal de push usados para relatórios e criação de público-alvo.  |
| Conjunto de dados do AJO Surfaces | Conjunto de dados vazio relacionado ao esquema de Superfícies de entrada do Journey Optimizer |
| OutputForUPSDataset | Contém todas as associações de público-alvo do AO a serem gravadas no UPS |
| Conjunto de dados do perfil do Audience Orchestration | Gerado por composição de público-alvo para públicos-alvo de composição de público. Contém todos os públicos-alvo de composição de público-alvo, seus atributos e dados de enriquecimento |
| Repositório de objetos de decisão - Atividades | também conhecido como Decisões na interface do usuário do. Mas esses são os objetos que um usuário cria que reúne todos os elementos, incluindo a lógica de decisão. Por exemplo, para uma disposição específica (localização), quais ofertas devem ser consideradas (coleção de ofertas) e qual método de classificação usar nessas ofertas. |
| Repositório de objetos de decisão - Ofertas substitutas | este é o repositório para o outro tipo de oferta que um usuário cria. Especificamente, se não estiverem qualificados para ver uma oferta personalizada e precisarem ver algo, pelo menos verão a oferta substituta. Esse conjunto de dados contém os atributos desse tipo de oferta |
| Repositório de objetos de decisão - Ofertas personalizadas | este é o repositório para um tipo de oferta que um usuário cria. Portanto, esse conjunto de dados contém os atributos sobre esse tipo de oferta |
| Repositório de objetos de decisão - Posicionamentos | este é o repositório de objetos que definem o local onde uma oferta precisa ser exibida. |
| Jornada eventos de etapa | Captura todos os eventos de experiência de etapa de Jornada gerados no Journey Optimizer para serem consumidos por serviços como relatórios. |
| Jornadas | Informações sobre o conjunto de dados de metadados que contém cada etapa de uma jornada |
| ODE DecisionEvents - decisão de produção | Sempre que tomamos uma decisão com base em uma solicitação, contamos isso como um evento de decisão |