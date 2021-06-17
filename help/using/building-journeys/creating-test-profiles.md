---
title: Criar um perfil de teste
description: Saiba como criar um perfil de teste
feature: Jornadas
topic: Gerenciamento de conteúdo
role: User
level: Intermediate
source-git-commit: 8f77802fcaa23790f9de4e8f15e593643b13fb1e
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 1%

---

# Criar perfis de teste {#create-test-profiles}

Perfis de teste são necessários ao usar o modo de teste Para saber como usar o [modo de teste](../building-journeys/testing-the-journey.md) em uma jornada, e para [visualizar e testar suas mensagens](../preview.md).

Os métodos disponíveis para criar perfis de teste são detalhados abaixo:

* Você pode transformar um [perfil existente](#turning-profile-into-test) em um perfil de teste

* Você pode criar um perfil de teste carregando um [arquivo csv](#create-test-profiles-csv) ou usando [chamadas de API](#create-test-profiles-api). Além desses dois métodos, o Adobe Journey Optimizer vem com um [caso de uso no produto](#use-case-1) específico para facilitar a criação do perfil de teste.

* Você também pode fazer upload de um arquivo json em um conjunto de dados. Para obter mais informações, consulte a [Documentação de assimilação de dados](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset).

Observe que criar um perfil de teste é semelhante à criação de perfis regulares no Adobe Experience Platform. Para obter mais informações, consulte a [documentação do Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

## Pré-requisitos {#test-profile-prerequisites}

Para criar perfis, primeiro é necessário criar um esquema e um conjunto de dados no Adobe [!DNL Journey Optimizer].

Primeiro, você precisa **criar um schema**. Siga estas etapas:

1. Na seção do menu GESTÃO DE DADOS , clique em **[!UICONTROL Schemas]**.
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
1. No painel direito **[!UICONTROL Field properties]**, marque as opções **[!UICONTROL Identity]** e **[!UICONTROL Primary Identity]** e selecione um namespace. Se quiser que a identidade primária seja um endereço de email, escolha o namespace **[!UICONTROL Email]**. Clique em **[!UICONTROL Apply]**.
   ![](../assets/test-profiles-4bis.png)
1. Selecione o schema e habilite a opção **[!UICONTROL Profile]** no painel **[!UICONTROL Schema properties]**.
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

## Caso de uso no produto{#use-case-1}

Na página inicial do Adobe Journey Optimizer, você pode aproveitar os perfis de teste no caso de uso do produto. Esse caso de uso facilita a criação de perfis de teste usados para testar jornadas antes da publicação.

![](../assets/use-cases-home.png)

Clique no botão **[!UICONTROL Begin]** para iniciar o caso de uso.

As seguintes informações são obrigatórias:

1. **Namespace** de identidade: O namespace  [de identidade ](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html) usado para identificar exclusivamente os perfis de teste. Por exemplo, se o email for usado para identificar os perfis de teste, o namespace de identidade **Email** deverá ser selecionado. Se o identificador exclusivo for o número de telefone, então o namespace de identidade **Phone** deverá ser selecionado.

2. **Arquivo** CSV: Um arquivo separado por vírgulas contendo a lista de perfis de teste a serem criados. O caso de uso espera um formato predefinido para o arquivo CSV que contenha a lista de perfis de teste a serem criados. Cada linha no arquivo deve incluir os seguintes campos na ordem correta, da seguinte maneira:

   1. **Id** da pessoa: Identificador exclusivo do perfil de teste. Os valores desse campo devem refletir o namespace de identidade selecionado. (Como exemplo, se **Phone** for selecionado para o namespace de identidade, os valores desse campo deverão ser números de telefone. Da mesma forma, se **Email** for selecionado, os valores desse campo deverão ser emails)
   1. **Email**: Endereço de email do perfil de teste. (O campo **ID de pessoa** e o campo **Email** poderiam conter os mesmos valores se **Email** for selecionado como o namespace de identidade)
   1. **Nome**: Nome do perfil de teste.
   1. **Sobrenome**: Sobrenome do perfil de teste.
   1. **Cidade**: Perfil de teste da cidade de residência
   1. **País**: País de residência do perfil de teste
   1. **Gênero**: Gênero do perfil de teste. Os valores disponíveis são **macho**, **fêmeas** e **não_especificado**

Depois de selecionar o namespace de identidade e fornecer o arquivo CSV com base no formato acima, clique no botão **[!UICONTROL Run]** no canto superior direito. O caso de uso pode levar alguns minutos para ser concluído. Quando o caso de uso concluir o processamento e criar os perfis de teste, uma notificação será enviada para notificar o usuário.

>[!NOTE]
>
>Os perfis de teste podem substituir perfis existentes. Antes de executar o caso de uso, verifique se o CSV contém somente perfis de teste e se é executado na sandbox correta.

## Transformar um perfil em um perfil de teste{#turning-profile-into-test}

Você pode transformar um perfil existente em um perfil de teste: é possível atualizar os atributos de perfil da mesma maneira que criar um perfil.

Uma maneira simples de fazer isso é usando uma atividade de ação **[!UICONTROL Update Profile]** em uma jornada e alterar o campo booleano testProfile de false para true.

Sua jornada será composta de uma atividade **[!UICONTROL Read Segment]** e uma atividade **[!UICONTROL Update Profile]** . Primeiro, é necessário criar um segmento direcionado aos perfis que você deseja transformar em perfis de teste.

>[!NOTE]
>
> Como você atualizará o campo **testProfile**, os perfis escolhidos devem incluir este campo. O schema relacionado deve ter o grupo de campos **Detalhes do teste de perfil**. Consulte [esta seção](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Navegue até **Segmentos** e **Criar segmento**, no canto superior direito.
   ![](../assets/test-profiles-22.png)
1. Defina um nome para o segmento e crie o segmento: escolha os campos e os valores para direcionar os perfis desejados.
   ![](../assets/test-profiles-23.png)
1. Clique em **Save** e verifique se os perfis são direcionados corretamente pelo segmento.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > O cálculo de segmentos pode levar algum tempo. Saiba mais sobre segmentos em [esta seção](../segment/about-segments.md).

1. Agora crie uma nova jornada e comece com uma atividade de orquestração **[!UICONTROL Read Segment]** .
1. Escolha o segmento criado anteriormente e o namespace que seus perfis usam.
   ![](../assets/test-profiles-25.png)
1. Adicione uma atividade de ação **[!UICONTROL Update Profile]** .
1. Selecione o schema, o campo **testProfiles**, o conjunto de dados e defina o valor como **True**. Para fazer isso, no campo **[!UICONTROL VALUE]**, clique no ícone **Pen** à direita, selecione **[!UICONTROL Advanced mode]** e digite **true**.
   ![](../assets/test-profiles-26.png)
1. Adicione uma atividade **End** e clique em **[!UICONTROL Publish]**.
1. Na seção **[!UICONTROL Segments]**, verifique se os perfis foram atualizados corretamente.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Para obter mais informações sobre a atividade **[!UICONTROL Update Profile]**, consulte [esta seção](../building-journeys/update-profiles.md).

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

Você deve usar um Esquema de perfil que contenha o grupo de campos &quot;Detalhes do teste de perfil&quot;. O sinalizador testProfile faz parte desse grupo de campos.
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
