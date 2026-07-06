---
solution: Journey Optimizer
product: journey optimizer
title: Usar fragmentos dinâmicos
description: Saiba como usar a resolução de fragmento dinâmico no Adobe Journey Optimizer para selecionar e inserir fragmentos no tempo de execução com base em atributos de perfil, pesquisas de conjunto de dados ou dados de contexto.
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: dynamic, fragmento, expressão, personalização, tempo de execução
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# Usar fragmentos dinâmicos {#dynamic-fragments}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba como usar a resolução de fragmento dinâmico no Adobe Journey Optimizer para selecionar qual fragmento publicado é inserido em uma mensagem no tempo de execução, com base em atributos de perfil, pesquisas de conjunto de dados ou dados de contexto passados no momento do envio.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] dá suporte a **resolução dinâmica de fragmento** em tempo de execução, permitindo que você selecione qual fragmento publicado é inserido em uma mensagem com base em atributos de perfil, pesquisas de conjunto de dados ou dados de contexto passados no momento do envio. Isso permite conteúdo altamente personalizado sem duplicar a lógica de campanha ou jornada.

## Visão geral {#overview}

**Fragmentos estáticos** são inseridos em uma mensagem em tempo de design — o mesmo fragmento é usado para cada destinatário. **Fragmentos dinâmicos** resolvem a ID do fragmento em tempo de execução por destinatário, o que significa que perfis diferentes podem receber blocos de conteúdo totalmente diferentes na mesma campanha ou jornada.

As IDs de fragmento dinâmico podem vir de três fontes:

* Uma **pesquisa de conjunto de dados** — por exemplo, um conjunto de dados de recomendações codificado por estilo ou produto
* Um **atributo de perfil** armazenado no Adobe Experience Platform
* **Dados de contexto** passados diretamente na solicitação de API no momento do envio

>[!NOTE]
>
>O uso da função auxiliar `datasetLookup` nos fragmentos de expressão está atualmente disponível para um conjunto limitado de clientes. Para obter acesso, entre em contato com um representante da Adobe.

## Pré-requisitos {#prerequisites}

Antes de usar fragmentos dinâmicos, verifique se os seguintes itens estão em vigor:

* Você tem as permissões necessárias para criar e publicar fragmentos no [!DNL Journey Optimizer]. [Saiba mais](../administration/ootb-product-profiles.md#content-library-manager)
* O fragmento que você pretende referenciar é **publicado** (status: **Live**). Fragmentos de rascunho não podem ser resolvidos no tempo de execução.
* Se estiver resolvendo a ID do fragmento de um conjunto de dados, o esquema do conjunto de dados incluirá um campo que armazena a ID do fragmento, e o conjunto de dados será [habilitado para pesquisa](../data/lookup-aep-data.md).
* Todos os atributos de perfil que o próprio fragmento dinâmico referencia são incluídos no caminho de exportação da mensagem ou estão disponíveis no perfil no momento do envio.

>[!CAUTION]
>
>Validações relacionadas ao fragmento são ignoradas no fluxo de fragmento dinâmico. Superfície de IDs de fragmento inválidas como falhas de entrega em tempo de execução, em vez de erros de validação iniciais. Sempre verifique se as IDs de fragmento referenciadas são válidas e publicadas antes de ativar uma campanha.

## Etapa 1: criar e publicar o fragmento {#create-fragment}

Antes de fazer referência dinâmica a um fragmento, ele deve ser publicado em [!DNL Journey Optimizer].

1. Em [!DNL Journey Optimizer], navegue até **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Fragmentos]**.

1. Selecione **[!UICONTROL Criar fragmento]** e crie o conteúdo. [Saiba como criar fragmentos](create-fragments.md)

1. Quando o conteúdo estiver pronto, clique em **[!UICONTROL Publicar]**. A publicação é assíncrona e pode levar alguns segundos. Confirme se o status do fragmento muda para **Live** antes de continuar.

1. Anote a **ID do fragmento** na exibição detalhada do fragmento ou na resposta da API de fragmentos. Você referenciará essa ID na mensagem.

>[!NOTE]
>
>Você pode recuperar todas as IDs de fragmento publicadas programaticamente usando a API `GET /fragments`. Consulte a [documentação das APIs do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} para obter mais detalhes.

## Etapa 2: criar a mensagem com uma referência de fragmento dinâmico {#author-message}

No editor de personalização, insira o espaço reservado do fragmento dinâmico usando a seguinte sintaxe:

```handlebars
{{fragment id=dynamic_fragment_id}}
```

O identificador `dynamic_fragment_id` é um nome de variável. Seu valor deve ser resolvido antes que ocorra a pesquisa de fragmento. Você o resolve usando uma expressão de pesquisa do conjunto de dados, um atributo de perfil ou dados de contexto.

### Resolver a partir de uma pesquisa de conjunto de dados {#resolve-from-dataset}

Se a ID do fragmento for armazenada em um conjunto de dados do AEP (por exemplo, uma tabela de mapeamento de estilo para fragmento), use a função auxiliar `datasetLookup` para resolvê-la:

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

Neste exemplo, o conjunto de dados contém linhas com chave de um valor de estilo (como `style1`). Para um determinado perfil, a pesquisa recupera o valor da coluna `fragmentId` correspondente e o atribui a `dynamic_fragment_id`, que é usado para resolver o fragmento.

>[!NOTE]
>
>O uso da função auxiliar `datasetLookup` nos fragmentos de expressão está atualmente disponível para um conjunto limitado de clientes. Para obter acesso, entre em contato com um representante da Adobe. Para obter mais informações sobre pesquisas de conjunto de dados na personalização, consulte [Usar dados do Adobe Experience Platform](../data/lookup-aep-data.md).

### Resolver a partir dos dados de contexto {#resolve-from-context}

Se a ID do fragmento for fornecida no momento do envio como parte do contexto de solicitação de API, referencie-a usando o namespace `context`:

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

O caminho `context.audiencePayload` é o prefixo necessário para todos os atributos originados de um arquivo de público-alvo CSV ou transmitidos pelo contexto de solicitação de API. O nome da coluna do CSV (por exemplo, `fragmentId`) segue o prefixo.

### Resolver a partir de um atributo de perfil {#resolve-from-profile}

Se a ID do fragmento for armazenada como um atributo de perfil no Adobe Experience Platform, faça referência a ela diretamente:

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## Etapa 3: configurar seu conjunto de dados para a abordagem de pesquisa {#configure-dataset}

Se você estiver usando a abordagem de pesquisa do conjunto de dados, atualize o esquema do conjunto de dados e os dados para carregar a ID do fragmento.

1. Nas recomendações ou no conjunto de dados de mapeamento, adicione uma coluna (por exemplo, `fragmentId`) que armazene a ID do fragmento do AJO publicada para cada linha.

1. Para cada estilo ou variante (por exemplo, `style1`, `style2`), preencha a coluna `fragmentId` com a ID de fragmento correspondente.

1. Verifique se o conjunto de dados está assimilado na Adobe Experience Platform e [habilitado para pesquisa](../data/lookup-aep-data.md).

1. Confirme se todos os atributos de perfil referenciados dentro do fragmento dinâmico são capturados na mensagem ou em um fragmento estático para impedir a renderização vazia no momento da exportação.

**Exemplo de estrutura do conjunto de dados:**

| Coluna | Exemplo de valor |
|---|---|
| estilo | style1 |
| fragmentId | &lt;fragment-id-1> |
| estilo | style2 |
| fragmentId | &lt;fragment-id-2> |

## Etapa 4: Transmitir dados de contexto no momento do envio {#pass-context-data}

Se você estiver resolvendo a ID do fragmento a partir dos dados de contexto (por exemplo, de um arquivo de recomendação de público-alvo CSV), transmita a ID do fragmento na solicitação de API sob o prefixo de contexto necessário.

Ao usar a API de prova de campanha, inclua a ID do fragmento no objeto `context`:

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

O prefixo `context.audiencePayload` é obrigatório. Atributos aninhados com esse mapa-chave diretamente para colunas no arquivo de público-alvo CSV ao executar a campanha em tempo real.

## Etapa 5: comprovar e validar {#proof-validate}

Antes de ativar a campanha, use a API de prova de campanha para verificar se o fragmento dinâmico é resolvido corretamente e se a saída de email renderizada é a esperada.

1. Acione um trabalho de prova usando o ponto de extremidade `POST /campaigns/{id}/proofs`. Na solicitação de prova, passe a ID do fragmento que você deseja testar em `context.audiencePayload.fragmentId`.

1. Sonde o status do trabalho de prova usando o ponto de extremidade `GET /campaigns/{id}/proofs/{proofId}` até que o status seja `Submitted` ou `Failed`.

1. Verifique o email entregue para verificar se o conteúdo correto do fragmento é renderizado.

1. Se o conteúdo do fragmento estiver ausente ou incorreto, verifique se a ID do fragmento é válida, se o fragmento está publicado e se todos os atributos de perfil necessários estão presentes.

Para obter mais informações sobre a API de campanha, consulte a [documentação sobre APIs do Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}.

## Medidas de proteção e limitações {#guardrails}

>[!CAUTION]
>
>O OLAC (Object-Level Access Control, Controle de acesso em nível de objeto) não é empregado para fragmentos no modelo de fragmento dinâmico. Verifique se os requisitos de controle de acesso são considerados no nível da campanha e do público-alvo.

As seguintes limitações se aplicam ao usar fragmentos dinâmicos:

* **Cobertura do atributo de perfil no momento da exportação**: o fragmento é escolhido em tempo de execução por perfil. Os atributos de perfil exigidos pelo fragmento dinâmico não são conhecidos antecipadamente. Se o fragmento dinâmico depender de um atributo de perfil que não estava presente na mensagem original ou em qualquer fragmento estático referenciado na mensagem, esse campo poderá ser renderizado vazio no caminho de exportação.

* **Nenhuma validação de fragmento inicial**: validações relacionadas a fragmentos são ignoradas neste fluxo. IDs de fragmento incorretas ou não publicadas surgem como falhas de entrega em tempo de execução, em vez de erros de validação mostrados na interface do usuário.

* **Alteração de esquema necessária para a abordagem do conjunto de dados**: o uso do caminho pesquisa por ID requer a atualização do esquema do conjunto de dados para armazenar e transmitir a ID do fragmento, além da canalização necessária para alimentá-lo no pipeline de mensagens.

* **Captura de atributo para exportação**: certifique-se de que todos os atributos usados dentro do fragmento dinâmico sejam capturados na mensagem ou em fragmentos estáticos para evitar renderização vazia no caminho de exportação.

Mais medidas de proteção aplicáveis aos fragmentos estão disponíveis em [esta seção](../start/guardrails.md#fragments-guardrails).

## Tratamento de erros {#error-handling}

Se um fragmento dinâmico não for resolvido no tempo de execução, um evento de exclusão será gerado para o perfil afetado. Atualmente, todas as falhas de renderização do fragmento são categorizadas como um único tipo de erro geral.

Para depurar falhas de resolução do fragmento:

1. Verifique se há eventos de exclusão nos relatórios do delivery da campanha.
1. Verifique se a ID do fragmento transmitida no tempo de execução corresponde a um fragmento publicado.
1. Confirme se todos os atributos de perfil exigidos pelo fragmento estão presentes no perfil no momento do envio.
1. Use a [API de comprovação](#proof-validate) para testar IDs de fragmento específicas antes de ativar a campanha.
