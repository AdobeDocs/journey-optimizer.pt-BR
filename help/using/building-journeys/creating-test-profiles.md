---
title: Criar um perfil de teste
description: Saiba como criar um perfil de teste
source-git-commit: 4464ea7169424c1ec6212394b8bda79a9bec1913
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 2%

---

# Criar perfis de teste {#create-test-profiles}

![](../assets/do-not-localize/badge.png)

Os perfis de teste são necessários ao usar o modo de teste em uma jornada. Você pode transformar um [perfil existente](../building-journeys/creating-test-profiles.md#turning-profile-into-test) em um perfil de teste ou [criar um perfil de teste](../building-journeys/creating-test-profiles.md#create-test-profiles-csv). Para saber como usar o modo de teste, consulte [esta seção](../building-journeys/testing-the-journey.md).

Há diferentes maneiras de criar um perfil de teste no Adobe Experience Platform. Nesta documentação, nos concentramos em dois métodos: carregar um arquivo [csv](../building-journeys/creating-test-profiles.md#create-test-profiles-csv) e usar [chamadas de API](../building-journeys/creating-test-profiles.md#create-test-profiles-api). Você também pode fazer upload de um arquivo json em um conjunto de dados, consulte a [Documentação de assimilação de dados](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset).

Criar um perfil de teste é semelhante à criação de perfis regulares no Adobe Experience Platform. Para obter mais informações, consulte a [documentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

## Pré-requisitos{#test-profile-prerequisites}

Para criar perfis, primeiro é necessário criar um esquema e um conjunto de dados no Adobe [!DNL Journey Optimizer].

Primeiro, você precisa **criar um schema**. Siga estas etapas:

1. Na seção ADMINISTRATION , clique em **[!UICONTROL Schemas]**.
   ![](../assets/test-profiles-0.png)
1. Clique em **[!UICONTROL Create schema]**, na parte superior direita, e selecione um tipo de esquema, por exemplo **Perfil individual XDM**.
   ![](../assets/test-profiles-1.png)
1. Selecione os grupos de campos apropriados. Certifique-se de adicionar o grupo de campos **Detalhes do teste de perfil**.
   ![](../assets/test-profiles-1-ter.png)
Depois de concluído, clique em  **[!UICONTROL Add field groups]**: a lista de grupos de campos é exibida na tela de visão geral do schema.
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* Clique no nome do schema para alterá-lo e atualizar suas propriedades.
      >
      >
   * Clique no botão **[!UICONTROL Add]** na seção Grupos de campos para selecionar outros grupos de campos a serem adicionados no esquema


1. Na lista de campos, clique no campo que deseja definir como a identidade primária.
   ![](../assets/test-profiles-3.png)
1. No painel direito **[!UICONTROL Field properties]**, marque as opções ****[!UICONTROL Identity]** e ****[!UICONTROL Primary Identity]** e selecione um namespace. Se desejar que a identidade primária seja um endereço de email, escolha o namespace **Email**. Clique em **Aplicar**.
   ![](../assets/test-profiles-4.png)
1. Selecione o schema e habilite a opção **[!UICONTROL Profile]** no **[!UICONTROL Schema properties]**.
   ![](../assets/test-profiles-5.png)
1. Clique em **Salvar**.

>[!NOTE]
>
>Para obter mais informações sobre a criação do schema, consulte a [documentação XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites).

Em seguida, é necessário **criar o conjunto de dados** no qual os perfis serão importados. Siga estas etapas:

1. Navegue até **[!UICONTROL Datasets]** e clique em **[!UICONTROL Create dataset]**.
   ![](../assets/test-profiles-6.png)
1. Escolha **[!UICONTROL Create dataset from schema]**.
   ![](../assets/test-profiles-7.png)
1. Selecione o schema criado anteriormente e clique em **[!UICONTROL Next]**.
   ![](../assets/test-profiles-8.png)
1. Escolha um nome e clique em **[!UICONTROL Finish]**.
   ![](../assets/test-profiles-9.png)
1. Habilite a opção **[!UICONTROL Profile]**.
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> Para obter mais informações sobre a criação do conjunto de dados, consulte a [Documentação do Serviço de Catálogo](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started).

## Transformar um perfil em um perfil de teste{#turning-profile-into-test}

Você pode transformar um perfil existente em um perfil de teste: é possível atualizar os atributos de perfil da mesma maneira que criar um perfil.

Uma maneira simples de fazer isso é usando uma atividade de ação **[!UICONTROL Update profile]** em uma jornada e alterar o campo booleano testProfile de false para true.

Sua jornada será composta de uma atividade **[!UICONTROL Read segment]** e uma atividade **[!UICONTROL Update profile]** . Primeiro, é necessário criar um segmento direcionado aos perfis que você deseja transformar em perfis de teste.

>[!NOTE]
>
> Como você atualizará o campo **testProfile**, os perfis escolhidos devem incluir este campo. O schema relacionado deve ter a combinação **Profile test details**. Consulte [esta seção](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Navegue até **Segmentos** e **Criar segmento**, no canto superior direito.
   ![](../assets/test-profiles-22.png)
1. Defina um nome para o segmento e crie o segmento: escolha os campos e os valores para direcionar os perfis desejados.
   ![](../assets/test-profiles-23.png)
1. Clique em **Save** e verifique se os perfis são direcionados corretamente pelo segmento.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > O cálculo de segmentos pode levar algum tempo. Saiba mais sobre segmentos em [esta seção](../segment/about-segments.md).

1. Agora crie uma nova jornada e comece com uma atividade de orquestração **[!UICONTROL Read segment]** .
1. Escolha o segmento criado anteriormente e o namespace que seus perfis usam.
   ![](../assets/test-profiles-25.png)
1. Adicione uma atividade de ação **[!UICONTROL Update profile]** .
1. Selecione o schema, o campo **testProfiles**, o conjunto de dados e defina o valor como **True**. Para fazer isso, no campo **[!UICONTROL VALUE]**, clique no ícone **Pen** à direita, selecione **[!UICONTROL Advanced mode]** e digite **true**.
   ![](../assets/test-profiles-26.png)
1. Adicione uma atividade **End** e clique em **[!UICONTROL Publish]**.
1. Na seção **[!UICONTROL Segments]**, verifique se os perfis foram atualizados corretamente.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Para obter mais informações sobre a atividade **[!UICONTROL Update profile]**, consulte [esta seção](../building-journeys/update-profiles.md).

## Criar um perfil de teste usando um arquivo csv{#create-test-profiles-csv}

No Adobe Experience Platform, é possível criar perfis carregando um arquivo csv contendo os diferentes campos de perfil no conjunto de dados. Este é o método mais fácil.

1. Crie um arquivo csv simples usando um software de planilha.
1. Adicione uma coluna para cada campo necessário. Certifique-se de adicionar o campo de identidade primário (&quot;personID&quot; no nosso exemplo acima) e o campo &quot;testProfile&quot; definidos como &quot;true&quot;.
   ![](../assets/test-profiles-11.png)
1. Adicione uma linha por perfil e preencha os valores de cada campo.
   ![](../assets/test-profiles-12.png)
1. Salve a planilha como um arquivo csv. Verifique se as vírgulas são usadas como separadores.
1. Navegue até Adobe Experience Platform **Workflows**.
   ![](../assets/test-profiles-14.png)
1. Escolha **Mapear CSV para esquema XDM** e clique em **Iniciar**.
   ![](../assets/test-profiles-16.png)
1. Selecione o conjunto de dados para o qual deseja importar os perfis. Clique em **Próximo**.
   ![](../assets/test-profiles-17.png)
1. Clique em **Escolha os arquivos** e selecione o arquivo csv. Quando o arquivo for carregado, clique em **Next**.
   ![](../assets/test-profiles-18.png)
1. Mapeie os campos csv de origem para os campos de esquema e clique em **Finish**.
   ![](../assets/test-profiles-19.png)
1. A importação de dados é iniciada. O status será movido de **Processando** para **Sucesso**. Clique em **Visualizar conjunto de dados**, na parte superior direita.
   ![](../assets/test-profiles-20.png)
1. Verifique se os perfis de teste foram adicionados corretamente.
   ![](../assets/test-profiles-21.png)

Seus perfis de teste são adicionados e agora podem ser usados ao testar uma jornada. Consulte [esta seção](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Para obter mais informações sobre importações de csv, consulte a [documentação sobre assimilação de dados](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials).

## Criar perfis de teste usando chamadas de API{#create-test-profiles-api}

Também é possível criar perfis de teste por meio de chamadas de API. Saiba mais nesta [página](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

Você deve usar um Esquema de perfil que contenha a combinação &quot;Detalhes do teste de perfil&quot;. O sinalizador testProfile faz parte dessa mistura.

Ao criar um perfil, transmita o valor: testProfile = true.

Observe que você também pode atualizar um perfil existente para alterar seu sinalizador testProfile para &quot;true&quot;.

Este é um exemplo de uma chamada de API para criar um perfil de teste:

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```
