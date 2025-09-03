---
solution: Journey Optimizer
product: journey optimizer
title: Usar dados da Adobe Experience Platform
description: Saiba como usar conjuntos de dados do Adobe Experience Platform no [!DNL Journey Optimizer] Recursos de decisão e personalização.
badge: label="Disponibilidade limitada" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expressão, editor
mini-toc-levels: 1
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 42f231a9b0b34a63d1601dcae653462f6321caed
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 6%

---

# Usar dados da Adobe Experience Platform {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="Habilitar para pesquisa"
>abstract="Habilitar para pesquisa"

>[!AVAILABILITY]
>
>No momento, esse recurso está disponível para todos os clientes como uma versão de disponibilidade limitada.

O Journey Optimizer permite aproveitar os dados do Adobe Experience Platform com recursos de personalização e decisão. Para fazer isso, os conjuntos de dados baseados em registros necessários para a personalização da pesquisa devem primeiro ser habilitados para o serviço de pesquisa, conforme descrito abaixo.

## Leitura obrigatória

### Medidas de proteção e diretrizes {#guidelines}

Antes de começar, reveja as seguintes restrições e diretrizes:

* Os conjuntos de dados habilitados para pesquisa não devem conter Informações pessoais identificáveis (PII).
* Os conjuntos de dados habilitados para pesquisa e usados na personalização não estão protegidos contra exclusão. Cabe a você acompanhar quais conjuntos de dados estão sendo usados para personalização para garantir que eles não sejam excluídos ou removidos.
* Os conjuntos de dados devem ser associados a um esquema que NÃO seja do tipo Perfil ou Evento.
* Os esquemas devem ter uma identidade primária. Somente uma única chave primária pode ser usada para pesquisas.

### Direito ao serviço de pesquisa

| Componente de recurso | Limite da sandbox de produção | Notas |
| ------- | ------- | ------- |
| Conjuntos de dados de pesquisa habilitados | Máximo de 10 por organização | Número máximo de conjuntos de dados que podem ser configurados para pesquisa em um determinado momento. Esse limite se aplica ao número total combinado de conjuntos de dados de pesquisa em sandboxes de produção e desenvolvimento na instância do cliente. |
| Contagem de registros do conjunto de dados | Até 2 milhões de registros por conjunto de dados | Número máximo de registros permitidos em um único conjunto de dados, calculado como a contagem total em todos os lotes nesse conjunto de dados. |
| Tamanho do registro | Até 2 KB por registro | Tamanho máximo de registro padrão aceito. |
| Tamanho do conjunto de dados | Até 4 GB | Tamanho máximo de um conjunto de dados individual, não o tamanho combinado em todos os conjuntos de dados em uma sandbox. A contagem de registros e os limites de tamanho do conjunto de dados são medidas de proteção independentes — ambas devem ser atendidas. |
| Atualizações de frequência do conjunto de dados | Até 5 atualizações por dia por conjunto de dados | Frequência máxima de operações de atualização permitida para um único conjunto de dados por dia. |

>[!NOTE]
>
>Se forem necessários volumes adicionais além das medidas de proteção listadas acima, entre em contato com o representante da Adobe.

### Considerações adicionais sobre desempenho

As recomendações abaixo são orientações para evitar atrasos no delivery:

| Consideração | Limite recomendado | Descrição |
| ------- | ------- | ------- |
| Atributos por pesquisa | Até 20 | Número de campos de dados recuperados por registro em uma única atividade de pesquisa. |
| Atividades de pesquisa | Até 5 por jornada | Cada jornada pode conter até 5 atividades de pesquisa separadas. Cada pesquisa pode direcionar a um conjunto de dados diferente. |

## Ativar um conjunto de dados para pesquisa de dados {#enable}

Para aproveitar os dados do seu conjunto de dados para personalização, é necessário habilitar o conjunto de dados para pesquisa.

### Pré-requisitos {#prerequisites-enable}

O esquema associado ao conjunto de dados que você deseja habilitar para pesquisa deve ser do tipo registro. O esquema NÃO deve ser de perfil ou classe de evento.

+++Exemplo

![](assets/data-lookup-schema.png)

+++

O esquema deve ter uma identidade primária definida.

+++Exemplo

![](assets/data-lookup-primary.png)

+++

Se um namespace personalizado ainda não tiver sido definido, verifique se a identidade é um identificador que não seja de pessoa.

+++Exemplo

![](assets/aep-data-namespace.png)

+++

### Habilitar o conjunto de dados para pesquisa na interface de gerenciamento do conjunto de dados

Na interface do usuário de gerenciamento de conjunto de dados, use o botão para ativar o conjunto de dados para pesquisa.

![](assets/aep-data-enable.png)

>[!NOTE]
>
>Recomenda-se que o conjunto de dados TAMBÉM NÃO esteja habilitado para o perfil, pois isso pode levar a um aumento na riqueza do perfil e não é necessário para executar as pesquisas.

### Método da API

Siga as instruções detalhadas em [esta documentação](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) para configurar seu ambiente para enviar comandos de API.

#### Pré-requisitos

* O projeto do desenvolvedor deve ter as APIs do Adobe Journey Optimizer e do Adobe Experience Platform adicionadas ao projeto.

  ![](assets/aep-data-api.png)

* Você deve ter permissão de gerenciamento de conjuntos de dados como parte de sua função.

* O esquema no qual o conjunto de dados se baseia deve conter uma identidade primária que possa atuar como a chave de pesquisa.

#### Estrutura de chamada da API

```shell
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}" 
```

Em que:

* A URL é `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* A ID do conjunto de dados é o conjunto de dados para o qual você deseja habilitar.
* A ação é ativar OU desativar.
* O token de acesso pode ser recuperado do console do desenvolvedor.
* A chave de API pode ser recuperada do console do desenvolvedor.
* A ID da organização IMS é sua organização da Adobe.
* Nome da sandbox é o nome da sandbox do conjunto de dados (ou seja, prod, dev etc.).

>[!NOTE]
>
>Se você encontrar o erro abaixo ao tentar fazer uma chamada de API para habilitar conjuntos de dados, tente remover as APIs do Adobe Journey Optimizer do projeto do console do desenvolvedor e adicioná-las novamente:
>
>`"error_code": "403003",`
>`"message": "Api Key is invalid"`

## Monitoramento do conjunto de dados

Depois que um conjunto de dados for habilitado para pesquisa, você poderá revisar o status de assimilação no serviço de pesquisa acessando o menu **[!UICONTROL Monitoramento]** e selecionando a guia **[!UICONTROL Journey Optimizer]**.

Esse indicador de processo ajuda a entender quando novos lotes de dados estão disponíveis no serviço de pesquisa.

![](assets/aep-data-monitoring.png)

<!--Ivan Mironchuk
Note - we have a bug here currently. Will need to update screenshot once the lookup service will accurately reflect the progress.-->

## Próximas etapas

Depois que um conjunto de dados for habilitado para pesquisa usando uma chamada de API, você poderá usar os dados com os recursos de personalização e Decisão do [!DNL Journey Optimizer]. Para obter mais informações, consulte estas seções:

* [Usar dados da Adobe Experience Platform para personalização](../personalization/aep-data-perso.md)
* [Usar dados da Adobe Experience Platform para decisão](../experience-decisioning/aep-data-exd.md)
