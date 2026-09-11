---
solution: Journey Optimizer
product: journey optimizer
title: Personalizar o plano de fundo do email
description: Saiba como personalizar o plano de fundo do email
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: plano de fundo, email, cor, editor
exl-id: 09a2e892-8c6f-460d-8b12-5026582c6ed0
TQID: https://experienceleague.adobe.com/8kFppIm3Q-zHDqalE0Vt0CK5Z1ts9fGspVu476TapSk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebbid: c41e8697-e629-4c38-96b3-564faaa17acf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 7047a27a870c50f7a093ec7d98d8398948b78edb
workflow-type: tm+mt
source-wordcount: 887
ht-degree: 12%

---

# Personalizar o plano de fundo do email {#backgrounds}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como definir cores e imagens de plano de fundo nos níveis de corpo, visor, estrutura e coluna do seu email no Designer de email.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="Configurações de fundo"
>abstract="Você pode personalizar a cor ou a imagem do fundo para o seu conteúdo. Observe que a imagem do fundo não é aceita por todos os clientes de email."

Os planos de fundo ajudam a reforçar a identidade da marca e chamar a atenção para as principais áreas do seu email. No Designer de email, você pode definir uma cor ou imagem de fundo em diferentes níveis de seu conteúdo — do corpo geral às estruturas e colunas individuais —, fornecendo controle preciso sobre como os planos de fundo são renderizados no email.

Lembre-se das seguintes práticas recomendadas ao definir planos de fundo no Designer de email:

* Aplique uma cor de plano de fundo ao corpo somente se o design exigir.
* Prefira definir as cores de fundo no nível da coluna sempre que possível.
* Evite usar as cores do plano de fundo em componentes de imagem ou texto, pois elas são mais difíceis de gerenciar.
* Teste imagens de fundo em clientes de email reais antes do envio, pois a renderização pode diferir da pré-visualização do Designer de email.

As configurações a seguir permitem aplicar uma cor ou imagem de fundo em qualquer nível do conteúdo do email, desde o corpo até estruturas e colunas individuais.

>[!TIP]
>
>Se um tema for aplicado ao seu email, não será possível substituir diretamente a cor de fundo definida pelo tema para um determinado componente. Você deve primeiro desbloquear esse estilo usando o ícone dedicado na guia **[!UICONTROL Estilos]**. [Saiba como](apply-email-themes.md#unlocking-styles)

## Definir uma cor de plano de fundo {#background-color}

1. **Cor do plano de fundo do corpo** - Defina uma **[!UICONTROL Cor do plano de fundo]** para o email inteiro. Selecione **[!UICONTROL Corpo]** na **[!UICONTROL árvore de navegação]** acessível na paleta esquerda e use a opção dedicada da guia **[!UICONTROL Estilos]** à direita.

   ![Envie um email ao Designer com o Corpo selecionado na árvore de navegação e a opção Cor do plano de fundo realçada no painel Estilos](assets/background_1.png)

1. **Cor do plano de fundo da janela** - Defina uma **[!UICONTROL Cor da janela]** para aplicar a mesma cor de plano de fundo a todos os componentes da estrutura, independentemente da cor do plano de fundo do corpo.

   ![Painel Estilos de Designer de email com a opção de cor Viewport realçada e um seletor de cores aberto para escolher a cor de plano de fundo aplicada a todas as estruturas](assets/background_2.png)

1. **Cor do plano de fundo da estrutura** - Para aplicar uma cor de plano de fundo a um único componente de estrutura, selecione-o diretamente na tela de desenho ou na paleta esquerda e defina uma cor específica para essa estrutura.

   ![Painel Estilos de email do Designer para uma estrutura selecionada, com a opção Cor do plano de fundo realçada](assets/background_3.png)

   >[!TIP]
   >
   >Nesse caso, não defina uma cor de fundo de visor, pois ela pode ocultar as cores de fundo da estrutura.

1. **Cor de plano de fundo da coluna** - Defina uma cor de plano de fundo no nível da coluna. Novamente, selecione a coluna desejada na paleta esquerda e defina uma cor específica para essa coluna.

   ![Painel Estilos de email do Designer para uma coluna selecionada, com a opção Cor do plano de fundo realçada](assets/background_5.png)

   >[!TIP]
   >
   >Esse é o caso de uso mais comum e uma prática recomendada, pois oferece mais flexibilidade ao editar o restante do conteúdo de email.

## Definir uma imagem de plano de fundo {#background-image}

Você também pode definir uma **[!UICONTROL Imagem de plano de fundo]** para o conteúdo de uma estrutura ou componente de coluna. Isso é usado com mais frequência no nível da estrutura; é possível definir um no nível da coluna, mas raramente é usado.

>[!NOTE]
>
>Alguns programas de email não são compatíveis com imagens de fundo. Quando não houver compatibilidade, a cor de fundo da linha será usada. Certifique-se de selecionar uma cor de fundo sobressalente apropriada caso a imagem não possa ser exibida.

![Painel Estilos de email do Designer com imagem de plano de fundo habilitada e posicionamento de Imagem definido como Altura Total - Direita, mostrando a imagem preenchendo uma coluna](assets/background_4.png)

>[!TIP]
>
>Pré-visualize a imagem de fundo nos clientes de email reais antes de enviar, não apenas na pré-visualização do Designer de email. A mesma imagem e posicionamento podem ser renderizados corretamente no editor, mas são exibidos esticados ou cortados de forma diferente em alguns clientes, como o Outlook no iOS.

Depois que uma imagem de plano de fundo é definida, use a lista suspensa **[!UICONTROL Posicionamento da imagem]** para controlar como a imagem preenche a estrutura ou a coluna. As opções abaixo estão disponíveis para seleção:

![Painel Estilos de email do Designer mostrando a lista suspensa Posicionamento da imagem com várias opções](assets/background_6.png){width=80%}

**Escala para preenchimento, centralizada:**

* **[!UICONTROL Ajustar]** - Estica a imagem para preencher o contêiner em ambos os eixos, sem preservar sua taxa de proporção.
* **[!UICONTROL Largura Total]** - Dimensiona a imagem proporcionalmente à largura do contêiner e a centraliza verticalmente.
* **[!UICONTROL Altura total]** - Dimensiona a imagem proporcionalmente à altura do contêiner e a centraliza horizontalmente.

**Escala de preenchimento, ancorada em uma borda:**

* **[!UICONTROL Largura Total - Superior]** - Igual à **[!UICONTROL Largura Total]**, ancorada na parte superior do contêiner. O estouro é cortado na parte inferior.
* **[!UICONTROL Largura Total - Inferior]** - Igual à **[!UICONTROL Largura Total]**, ancorada na parte inferior do contêiner. O estouro é cortado na parte superior.
* **[!UICONTROL Altura Completa - Esquerda]** - Igual a **[!UICONTROL Altura Completa]**, ancorado à esquerda do contêiner. O estouro é cortado à direita.
* **[!UICONTROL Altura Completa - Direita]** - Igual à **[!UICONTROL Altura Completa]**, ancorada à direita do contêiner. O estouro é cortado à esquerda.

**Bloco:**

* **[!UICONTROL Repetir]** - Organiza lado a lado a imagem em seu tamanho original para preencher o contêiner.

**Posição sem dimensionamento:**

* **[!UICONTROL Esquerda]**, **[!UICONTROL Direita]**, **[!UICONTROL Centro]**, **[!UICONTROL Superior]**, **[!UICONTROL Inferior]** - Posiciona a imagem em seu tamanho original, ancorada na borda ou no centro correspondente do contêiner.

>[!NOTE]
>
>As opções de borda ancorada oferecem mais controle sobre qual parte da imagem permanece na exibição quando não corresponde às proporções da estrutura, em comparação às opções centralizadas acima.

{{$include /help/_includes/do-not-localize/email/ai-augmented-backgrounds.md}}
