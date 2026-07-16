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
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 22d6cddf35fa26a5fd3f0eddc74ed15faf9d6503
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 8%

---

# Upload personalizado {#custom-upload}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como importar um público-alvo de um arquivo CSV usando o Adobe Experience Platform Audience Portal e mapear seu atributo de identidade para perfis de clientes.

>[!ENDSHADEBOX]

O Adobe Experience Platform Audience Portal permite importar um público usando um arquivo CSV.

Durante o processo de upload personalizado, especifique o atributo CSV a ser usado como a identidade e a identidade do perfil para o qual ele é mapeado. Isso estabelece um link entre os dados do público-alvo e o perfil. Se o arquivo CSV contiver um valor de identidade não encontrado no perfil, um novo perfil será criado com esse valor de identidade.

![](assets/import-audience.png)

Informações detalhadas sobre como importar públicos estão disponíveis na [documentação do Serviço de segmentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} do Adobe Experience Platform.

>[!NOTE]
>
>Atualmente, não há suporte funcional para **[!UICONTROL Leitura incremental]** para carregamentos personalizados (upload de CSV) e outros públicos externos. Em cada recorrência, o **público-alvo inteiro** é recuperado, independentemente da configuração de alternância Leitura incremental.

Saiba como fazer upload de públicos-alvo no formato CSV em vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)
