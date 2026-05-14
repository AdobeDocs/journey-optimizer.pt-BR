---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos-alvo da Adobe Experience Platform
description: Saiba como trabalhar com públicos-alvo da Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 10%

---

# Upload personalizado {#custom-upload}

O Adobe Experience Platform Audience Portal permite importar um público usando um arquivo CSV.

Durante o processo de upload personalizado, especifique o atributo CSV a ser usado como a identidade e a identidade do perfil para o qual ele é mapeado. Isso estabelece um link entre os dados do público-alvo e o perfil. Se o arquivo CSV contiver um valor de identidade não encontrado no perfil, um novo perfil será criado com esse valor de identidade.

>[!NOTE]
>
>Para públicos-alvo de upload personalizados, se a &quot;Leitura incremental&quot; estiver ativada em uma jornada recorrente, os perfis serão recuperados somente na primeira recorrência, pois esses públicos-alvo são corrigidos.

![](assets/import-audience.png)

Informações detalhadas sobre como importar públicos estão disponíveis na [documentação do Serviço de segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} do Adobe Experience Platform.

Saiba como fazer upload de públicos-alvo no formato CSV em vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3423361?captions=por_br&quality=12)
