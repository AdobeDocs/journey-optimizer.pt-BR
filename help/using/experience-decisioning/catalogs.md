---
title: Catálogo de itens
description: Saiba como trabalhar com o catálogo de itens
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Catálogo de itens {#catalog}

No Decisioning, os catálogos servem como contêineres centrais para organizar itens de decisão. Cada catálogo está vinculado a um esquema do Adobe Experience Platform, abrangendo todos os atributos atribuíveis a um item de decisão.

Por enquanto, todos os itens de decisão criados são consolidados em um único catálogo &quot;Ofertas&quot;, acessível pelo menu **[!UICONTROL Catálogos]**.

![](assets/catalogs-list.png)

## Medidas de proteção e limitações

Para garantir desempenho e consistência ideais, o Decisioning impõe as seguintes medidas de proteção e limitações:

* **Tipos de dados com suporte**

  Por enquanto, a Decisão suporta exclusivamente os seguintes tipos de dados: String, Integer, Boolean, Date, DateTime, Decisioning Asset e Object. Qualquer campo fora desses tipos de dados não estará disponível para uso ao criar um item de decisão ou um catálogo.


* **Limite de atributo personalizado**

  Cada item de decisão pode incluir até 100 atributos personalizados.

* **Aninhando restrições**

  Há suporte para no máximo quatro níveis de aninhamento. Imagens não são compatíveis no último nível.

## Acessar e editar o esquema do catálogo {#access-catalog-schema}

Para acessar o schema do catálogo em que os atributos dos itens de decisão são armazenados, siga estas etapas:

1. Na lista de itens, clique no botão **[!UICONTROL Editar esquema]** localizado ao lado do botão **[!UICONTROL Criar item]**.

1. O schema do catálogo é aberto em uma nova guia, seguindo a estrutura abaixo:

   * O nó **`_experience`** inclui atributos de itens de decisão padrão, como nome, data inicial e final e descrição.
   * O nó **`_<imsOrg>`** hospeda atributos de itens de decisão personalizados. Por padrão, nenhum atributo personalizado é configurado, mas você pode adicionar quantos forem necessários para atender aos seus requisitos. Depois de concluído, os atributos personalizados aparecem na tela de criação do item de decisão ao lado dos atributos padrão.

   ![](assets/catalogs-schema.png)

1. Para adicionar um atributo personalizado ao esquema, expanda o nó **`_<imsOrg>`** e clique no botão &quot;+&quot; no local desejado na estrutura.

   ![](assets/catalogs-add.png)

1. Preencha os campos necessários para o atributo adicionado e clique em **[!UICONTROL Aplicar]**.

   O valor inserido em um atributo com atributo de ativo de decisão é um url público. Na maioria das vezes, isso apontaria para uma imagem.

   Informações detalhadas sobre como trabalhar com esquemas do Adobe Experience Platform estão disponíveis na [documentação do Sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=pt-BR).

1. Depois que os atributos personalizados desejados forem adicionados, salve o esquema. O novo campo agora está disponível na tela de criação do item de decisão, na seção **[!UICONTROL Atributos personalizados]**.


   O exemplo abaixo mostra uma tela de criação de item com atributos personalizados, como objetos definidos no esquema.

   ![](assets/custom-attributes.png)

