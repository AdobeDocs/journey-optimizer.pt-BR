---
solution: Journey Optimizer
product: journey optimizer
title: Importar o conteúdo do email
description: Saiba como importar conteúdo de email
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: email, importação, conteúdo, html, zip, css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
TQID: https://experienceleague.adobe.com/R0Csd9gbvY-iyW81G-clHoXozEBYWBfjb0y9PWq4zZA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 30%

---

# Importar o conteúdo do email {#existing-content}

O [!DNL Journey Optimizer] permite importar conteúdo existente do HTML para criar seus emails. Esse conteúdo pode ser:

* Um **arquivo HTML** com uma folha de estilos incorporada;
* Uma pasta **.zip** incluindo um arquivo HTML, a folha de estilos (.css) e as imagens.

  >[!NOTE]
  >
  >Não há restrições na estrutura do arquivo .zip. No entanto, as referências devem ser relativas e se encaixar na estrutura de árvore da pasta .zip.


>[!TIP]
>
>Se você tiver designs de imagem (JPEG ou PNG) em vez de arquivos HTML, poderá usar o [conversor de imagem para HTML](../content-management/image-to-html.md) para convertê-los automaticamente em modelos de email editáveis do HTML usando IA.

Para importar um arquivo contendo conteúdo HTML, siga as etapas abaixo:

1. Na página inicial do Designer de Email, selecione **[!UICONTROL Importar HTML]**.

   ![](assets/import-html_2.png)

1. Arraste e solte o HTML ou arquivo .zip contendo seu conteúdo HTML e clique em **[!UICONTROL Importar]**.

   ![](assets/html-imported_2.png)

1. Depois que o conteúdo do HTML for carregado, ele estará no **[!UICONTROL Modo de compatibilidade]**.

   Nesse modo, você só pode personalizar seu texto, adicionar links ou incluir ativos ao seu conteúdo.

1. Para aproveitar os componentes de conteúdo do Email Designer, acesse a guia **[!UICONTROL Conversor de HTML]** e clique em **[!UICONTROL Converter]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > Usar uma marca `<table>` como a primeira camada em um arquivo do HTML pode causar perda de estilo, incluindo configurações de plano de fundo e largura na marca de camada superior.

1. Agora você pode personalizar o arquivo importado, conforme necessário, com as funcionalidades de Designer de email. [Saiba mais](content-from-scratch.md)

## Vídeo tutorial {#video}

Saiba como importar conteúdo HTML existente, ajustar o design, adicionar mirror page e links para cancelar a inscrição e como codificar seu conteúdo.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
