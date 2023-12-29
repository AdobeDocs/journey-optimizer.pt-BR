---
solution: Journey Optimizer
product: journey optimizer
title: Criar um perfil de teste
description: Saiba como criar um perfil de teste
feature: Test Profiles, Profiles
topic: Content Management
role: User, Data Engineer
level: Intermediate
keywords: perfis de teste, teste, teste, jornada
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 2%

---

# Criar perfis de teste {#create-test-profiles}

Perfis de teste são necessários ao usar o [modo de teste](../building-journeys/testing-the-journey.md) em uma jornada, e para [visualizar e testar o conteúdo](../content-management/preview-test.md).

Há várias maneiras de criar perfis de teste. Você pode encontrar nesta página detalhes para:

* Girar um [perfil existente](#turning-profile-into-test) em um perfil de teste

* Criar perfis de teste fazendo upload de um [arquivo csv](#create-test-profiles-csv) ou usando [Chamadas de API](#create-test-profiles-api).

  Além desses dois métodos, a Adobe Journey Optimizer vem com uma interface [caso de uso no produto](#use-case-1) para facilitar a criação do perfil de teste.

Você também pode fazer upload de um arquivo json em um conjunto de dados existente. Para obter mais informações, consulte [Documentação de assimilação de dados](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset){target="_blank"}.

Observe que a criação de um perfil de teste é semelhante à criação de perfis comuns no Adobe Experience Platform. Para obter mais informações, consulte [Documentação de Perfil do cliente em tempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.

➡️ [Saiba como criar perfis de teste neste vídeo](#video)

## Pré-requisitos {#test-profile-prerequisites}

Para criar perfis, primeiro é necessário criar um esquema e um conjunto de dados no Adobe [!DNL Journey Optimizer].

Para **criar um esquema**, siga estas etapas:

1. Na seção de menu DATA MANAGEMENT, clique em **[!UICONTROL Esquemas]**.
   ![](assets/test-profiles-0.png)
1. Clique em **[!UICONTROL Criar esquema]**, na parte superior direita, selecione um tipo de esquema, por exemplo **Perfil individual** e clique em **Próxima**.
   ![](assets/test-profiles-1.png)
1. Insira um nome para o esquema e clique em **Concluir**.
   ![](assets/test-profiles-1-bis.png)
1. No **Grupos de campos** , à esquerda, clique em **Adicionar$$ e selecione os grupos de campos apropriados. Certifique-se de adicionar o **Detalhes de teste do perfil** grupo de campos.
   ![](assets/test-profiles-1-ter.png)
Depois de concluído, clique em **[!UICONTROL Adicionar grupos de campos]**: a lista de grupos de campos é exibida na tela de visão geral do schema.
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >Clique no nome do schema para atualizar suas propriedades.

1. Na lista de campos, clique no campo que você deseja definir como a identidade principal.
   ![](assets/test-profiles-3.png)
1. No **[!UICONTROL Propriedades do campo]** painel direito, marque a opção **[!UICONTROL Identidade]** e **[!UICONTROL Identidade principal]** e selecione um namespace. Se quiser que a identidade principal seja um endereço de email, escolha a **[!UICONTROL E-mail]** namespace. Clique em **[!UICONTROL Aplicar]**.
   ![](assets/test-profiles-4bis.png)
1. Selecione o esquema e ative a variável **[!UICONTROL Perfil]** opção no **[!UICONTROL Propriedades do esquema]** painel.
   ![](assets/test-profiles-5.png)
1. Clique em **Salvar**.

>[!NOTE]
>
>Para obter mais informações sobre criação de schema, consulte [Documentação XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites){target="_blank"}.

Então você precisa **criar o conjunto de dados** na qual os perfis serão importados. Siga estas etapas:

1. Navegue até **[!UICONTROL Conjuntos de dados]** e, em seguida, clique em **[!UICONTROL Criar conjunto de dados]**.
   ![](assets/test-profiles-6.png)
1. Escolher **[!UICONTROL Criar conjunto de dados a partir do esquema]**.
   ![](assets/test-profiles-7.png)
1. Selecione o schema criado anteriormente e clique em **[!UICONTROL Próxima]**.
   ![](assets/test-profiles-8.png)
1. Escolha um nome e clique em **[!UICONTROL Concluir]**.
   ![](assets/test-profiles-9.png)
1. Ativar o **[!UICONTROL Perfil]** opção.
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> Para obter mais informações sobre a criação de conjuntos de dados, consulte a [Documentação do Serviço de catálogo](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started){target="_blank"}.

## Caso de uso no produto{#use-case-1}

Na página inicial do Adobe Journey Optimizer, você pode aproveitar o caso de uso de perfis de teste no produto. Esse caso de uso facilita a criação de perfis de teste usados para jornadas de teste antes da publicação.

![](assets/use-cases-home.png)

Clique no botão **[!UICONTROL Começar]** para iniciar o caso de uso.

As seguintes informações são obrigatórias:

1. **Namespace de identidade**: A variável [namespace de identidade](../audience/get-started-identity.md) usado para identificar exclusivamente os perfis de teste. Por exemplo, se o email for usado para identificar os perfis de teste, o namespace de identidade **E-mail** deve ser selecionado. Se o identificador exclusivo for o número de telefone, o namespace de identidade **Telefone** deve ser selecionado.

2. **Arquivo CSV**: um arquivo separado por vírgulas contendo a lista de perfis de teste a serem criados. O caso de uso espera um formato predefinido para o arquivo CSV que contém a lista de perfis de teste a serem criados. Cada linha no arquivo deve incluir os seguintes campos na ordem correta, como a seguir:

   1. **ID da pessoa**: Identificador exclusivo do perfil de teste. Os valores desse campo devem refletir o namespace de identidade que foi selecionado. (Por exemplo, se **Telefone** for selecionada para o namespace de identidade e os valores desse campo deverão ser números de telefone. Da mesma forma, se **E-mail** for selecionada, os valores desse campo deverão ser emails)
   1. **Endereço de e-mail**: Testar o endereço de email do perfil. (O **ID da pessoa** e o campo **Endereço de e-mail** O campo pode conter os mesmos valores se **E-mail** está selecionado como o namespace de identidade)
   1. **Nome**: Nome do perfil de teste.
   1. **Sobrenome**: Sobrenome do perfil de teste.
   1. **Cidade**: Cidade de residência do perfil de teste
   1. **País**: País de residência com perfil de ensaio
   1. **Sexo**: Sexo do perfil de teste. Os valores disponíveis são **masculino**, **feminino** e **não_especificado**

Depois de selecionar o namespace de identidade e fornecer o arquivo CSV com base no formato acima, clique em **[!UICONTROL Executar]** no canto superior direito. O caso de uso pode levar alguns minutos para ser concluído. Quando o caso de uso concluir o processamento e a criação dos perfis de teste, uma notificação será enviada ao usuário.

>[!NOTE]
>
>Os perfis de teste podem substituir os perfis existentes. Antes de executar o caso de uso, verifique se o CSV contém apenas perfis de teste e se ele é executado na sandbox correta.

## Transformar um perfil em um perfil de teste{#turning-profile-into-test}

É possível transformar um perfil existente em um perfil de teste: você pode atualizar atributos de perfil da mesma forma que ao criar um perfil.

Uma maneira simples de fazer isso é usando um **[!UICONTROL Atualizar perfil]** atividade de ação em uma jornada e alterar o **testProfile** campo booleano de falso para verdadeiro.

Sua jornada será composta por um **[!UICONTROL Ler público-alvo]** e uma **[!UICONTROL Atualizar perfil]** atividade. Primeiro, é necessário criar um público-alvo direcionado aos perfis que você deseja transformar em perfis de teste.

>[!NOTE]
>
> Como você atualizará o **testProfile** , os perfis escolhidos deverão incluir esse campo. O schema relacionado deve ter o **Detalhes de teste do perfil** grupo de campos. Consulte [esta seção](../audience/creating-test-profiles.md#test-profiles-prerequisites).

1. Navegue até **Públicos-alvo**, depois **Criar público**, no canto superior direito.
   ![](assets/test-profiles-22.png)
1. Defina um nome para o público-alvo e crie o público-alvo: escolha os campos e os valores para direcionar os perfis desejados.
   ![](assets/test-profiles-23.png)
1. Clique em **Salvar** e verifique se os perfis foram direcionados corretamente pelo público-alvo.
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > O cálculo do público pode levar algum tempo. Saiba mais sobre públicos-alvo na [nesta seção](../audience/about-audiences.md).

1. Agora crie uma nova jornada e comece com um **[!UICONTROL Ler público-alvo]** atividade de orquestração.
1. Escolha o público-alvo criado anteriormente e o namespace que seus perfis usam.
   ![](assets/test-profiles-25.png)
1. Adicionar um **[!UICONTROL Atualizar perfil]** atividade de ação.
1. Selecione o esquema e a caixa de diálogo **testProfiles** , o conjunto de dados e defina o valor como **True**. Para fazer isso, na guia **[!UICONTROL VALOR]** clique no botão **Caneta** ícone à direita, selecione **[!UICONTROL Modo avançado]** e insira **true**.
   ![](assets/test-profiles-26.png)
1. Clique em **[!UICONTROL Publicar]**.
1. No **[!UICONTROL Públicos-alvo]** verifique se os perfis foram atualizados corretamente.
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Para obter mais informações sobre o **[!UICONTROL Atualizar perfil]** atividade, consulte [nesta seção](../building-journeys/update-profiles.md).

## Criar um perfil de teste usando um arquivo csv{#create-test-profiles-csv}

No Adobe Experience Platform, é possível criar perfis carregando um arquivo csv contendo os diferentes campos de perfil no conjunto de dados. Esse é o método mais fácil.

1. Crie um arquivo csv simples usando um software de planilha.
1. Adicione uma coluna para cada campo necessário. Adicione o campo de identidade principal (&quot;personID&quot; no exemplo acima) e o campo &quot;testProfile&quot; definido como &quot;true&quot;.
   ![](assets/test-profiles-11.png)
1. Adicione uma linha por perfil e preencha os valores para cada campo.
   ![](assets/test-profiles-12.png)
1. Salve a planilha como um arquivo csv. Verifique se as vírgulas são usadas como separadores.
1. Navegar até o Adobe Experience Platform **Fluxos de trabalho**.
   ![](assets/test-profiles-14.png)
1. Escolher **Mapear CSV para esquema XDM** e, em seguida, clique em **Launch**.
   ![](assets/test-profiles-16.png)
1. Selecione o conjunto de dados para o qual você deseja importar os perfis. Clique em **Avançar**.
   ![](assets/test-profiles-17.png)
1. Clique em **Escolher arquivos** e selecione o arquivo csv. Quando o arquivo for carregado, clique em **Próxima**.
   ![](assets/test-profiles-18.png)
1. Mapeie os campos do csv de origem para os campos de esquema e clique em **Concluir**.
   ![](assets/test-profiles-19.png)
1. A importação de dados é iniciada. O status será movido de **Processando** para **Sucesso**. Clique em **Visualizar conjunto de dados**, no canto superior direito.
   ![](assets/test-profiles-20.png)
1. Verifique se os perfis de teste foram adicionados corretamente.
   ![](assets/test-profiles-21.png)

Seus perfis de teste são adicionados e agora podem ser usados ao testar uma jornada. Consulte [esta seção](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Para obter mais informações sobre importações de csv, consulte [Documentação de assimilação de dados](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials){target="_blank"}.

## Criar perfis de teste usando chamadas de API{#create-test-profiles-api}

Você também pode criar perfis de teste por meio de chamadas de API. Saiba mais em [Documentação do Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=pt-BR){target="_blank"}.

Você deve usar um esquema de Perfil que contenha o grupo de campos &quot;Detalhes do teste de perfil&quot;. O sinalizador testProfile faz parte deste grupo de campos.
Ao criar um perfil, passe o valor: testProfile = true.

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

## Vídeo explicativo {#video}

Saiba como criar perfis de teste.

>[!VIDEO](https://video.tv.adobe.com/v/334236?quality=12)
