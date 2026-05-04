---
solution: Journey Optimizer
product: journey optimizer
title: Integração de fornecedores
description: Use as Integrações do Adobe Journey Optimizer com qualquer plataforma externa que exponha uma API válida, além de padrões de fornecedores testados pela engenharia para obter confiança ao projetar sua configuração.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integração, fornecedor, terceiros
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '10154'
ht-degree: 5%

---

# Exemplos de configurações do fornecedor {#vendor-integration}

>[!BEGINSHADEBOX]

Os clientes são responsáveis por garantir que seu uso do recurso de Integrações da AJO e de quaisquer outros fornecedores ou integrações associados de terceiros esteja em conformidade com todas as leis e normas aplicáveis, como a HIPAA.

>[!ENDSHADEBOX]

## Navegação rápida {#quick-navigation}

Use esses links agrupados para ir rapidamente para o padrão do fornecedor relevante:

* **Sistema de gerenciamento de conteúdo:** [Conteúdo](#contentful), [Sitecore](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fidelidade e recompensas:** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fidelidade do Salesforce](#salesforce-loyalty), [Capilar](#capillary)
* **Modelos, personalização e recomendações:** [Stensul](#stensul), [Marigold](#marigold), [Recomendações do Adobe Target](#adobe-target-recommendations)
* **Dados, clima e operações:** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Revisões, consentimento e redes sociais:** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)

## Conteúdo e CMS {#content-and-cms}

### Conteúdo {#contentful}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido pelo ou formalmente suportado pelo Contentful. Confirme os detalhes da API atual com a Documentação de conteúdo.

>[!BEGINSHADEBOX]

O conteúdo é um CMS headless para entradas e ativos estruturados em REST ou GraphQL, para que o Journey Optimizer possa extrair conteúdo no tempo de envio ou abertura.

Casos de uso típicos incluem blocos herói localizados, texto alternativo e CTAs no email, bem como entradas de produto ou promoção em módulos dinâmicos. Outro padrão comum é recuperar uma entrada específica por ID para mensagens personalizadas.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Conteúdo.

Os seguintes pré-requisitos se aplicam:

* Espaço de conteúdo com acesso à API de entrega e uma chave de API orientada a leitura.
* Limpar tipos de conteúdo e IDs de campo; acesso de administrador no Journey Optimizer para criar integrações.

As seguintes limitações e exclusões se aplicam:

* As APIs de conteúdo paginadas ou de listagem ampla não se encaixam bem nesse padrão; prefira chamadas de recuperação que direcionem uma entrada ou ativo específico.
* A sincronização de write-back ou bidirecional está fora do escopo deste exemplo.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Configure o **GET** com a API de entrega de conteúdo e o token de entrega, cole o JSON de exemplo, mapeie campos, teste e ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o ponto de extremidade usando a URL da API de Entrega de Conteúdo (CDA): `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. Selecione o método HTTP: **GET**.

1. Adicionar autenticação. Defina o parâmetro **`access_token`** **query** para seu token da API de entrega de conteúdo, conforme mostrado nos **Campos de integração de exemplo** abaixo. O conteúdo também aceita o mesmo token em um cabeçalho `Authorization: Bearer`; use o que seus campos de integração aceitarem.

1. Adicione variáveis de caminho, se necessário (por exemplo, ID de entrada, localidade).

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos obrigatórios para personalização.

1. Configure o tempo limite e o cache, conforme necessário.

1. Teste a conexão e ative.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplos de campos de integração (alinhe com a [API de entrega de conteúdo](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"} para seu espaço e ambiente):

| Campo | Valor |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/environments/{{environment_id}}/entries/{{entry_id}}` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **método HTTP** | `GET` |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |
| `entry_id` | `entry_id` | `<YOUR_ENTRY_ID>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | `access_token` | `<YOUR_API_KEY>` | Parâmetro da consulta |

+++

### Sitecore {#sitecore}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido nem formalmente suportado pelo Sitecore. Confirme os detalhes da API atual com a documentação do Sitecore.

>[!BEGINSHADEBOX]

O Sitecore Content Hub e as APIs de nuvem relacionadas são compatíveis com fluxos de download e metadados no estilo do DAM; o padrão de exemplo abaixo se concentra em um pedido de download por ID.

Casos de uso típicos incluem metadados de ativos ou downloads em conteúdo de email e alinhamento com fluxos de trabalho DAM gerenciados no Sitecore.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Sitecore.

Os seguintes pré-requisitos se aplicam:

* URL do locatário e credenciais (portador ou token por superfície da API).
* Acesso de administrador no Journey Optimizer para criar integrações.

As seguintes limitações e exclusões se aplicam:

* Os nomes de host e caminhos variam de acordo com o produto Sitecore. Use apenas endpoints expostos pelo locatário.
* Os tokens de acesso OAuth, a atualização e a duração devem seguir a política de segurança do Sitecore.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Configure o **GET** no caminho do pedido de download, defina cabeçalhos de autorização por Sitecore, mapeie `id` do contexto, cole o JSON de exemplo, mapeie campos e ajuste tempos limite para latência de ativos.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API do Content Hub (exemplo: ordem de download por ID). Exemplo de padrão de URL:

   `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Use os campos a seguir ao configurar essa chamada de amostra no Journey Optimizer. Confirme o nome do host e a versão da API do seu produto (Content Hub, XM Cloud e assim por diante) na [documentação do Sitecore](https://doc.sitecore.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| Autorização | Autorização | Constante | Portador `<token>` | Sim (ativado) |
| Se-Modificado-Desde | Se-Modificado-Desde | Variable | 24/08/2019 T14:15:22Z | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | X-Auth-Token | `<token>` | Header |

+++

### Salsify {#salsify}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido pelo Salsify nem é formalmente apoiado por ele. Confirme os detalhes da API atual com a documentação do Salsify.

>[!BEGINSHADEBOX]

O Salsify é um PIM com APIs para produtos, canais e ativos digitais.

Casos de uso típicos incluem atributos de produto ou URLs de mídia em emails e mensagens alinhadas aos dados de catálogo sindicalizado.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Salsify.

Os seguintes pré-requisitos se aplicam:

* Token de API e contexto de organização; IDs de produto que podem ser resolvidas a partir do perfil ou contexto.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Catálogos muito grandes: evite endpoints de lista em massa se as integrações esperarem uma recuperação por entidade.
* A visibilidade de atributos pode ser limitada pelas permissões de função do Salsify.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Prefira recuperação de produto único a chamadas de catálogo em massa, defina a autenticação do portador, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API do produto Salsify. Exemplo de padrão de URL:

   `https://api.salsify.com/v1/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Algumas referências mais antigas reutilizaram um caminho de estilo de pedido de download para o Salsify; seu locatário pode usar `https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}` ou similar. Confirmar em [Salsificar desenvolvedores](https://developers.salsify.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Content-Type (parâmetro padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| Autorização | Autorização | Constante | `Bearer <YOUR_TOKEN_HERE>` | Sim (ativado) |
| Se-Modificado-Desde | Se-Modificado-Desde | Variable | 24/08/2019 T14:15:22Z | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | `apiKey` | `<your_api_key>` | Header |

+++

### Contentstack {#contentstack}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido nem formalmente suportado pelo Contentstack. Confirme os detalhes da API atual com a documentação Contentstack.

>[!BEGINSHADEBOX]

A pilha de conteúdo é uma CMS headless; a entrega REST é típica do mapeamento de campos JSON no Journey Optimizer.

Um caso de uso típico é o uso de entradas para banners ou promoções com parâmetros que incluem o local.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Contentstack.

Os seguintes pré-requisitos se aplicam:

* Empilhar chave de API, token de entrega, nome do ambiente e UIDs de tipo de conteúdo.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Esse padrão usa REST JSON para mapeamento de campo; a entrega do GraphQL segue um caminho de integração diferente.
* Use tokens de entrega apropriados para produção; os fluxos de visualização e publicação não são intercambiáveis.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Adicione cabeçalhos `api_key` e `access_token` como Contentstack requer, inclua o parâmetro de consulta `environment`, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API de entrega de conteúdo. Exemplo de padrão de URL:

   `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Campos de integração de exemplo. Consulte [API de Entrega de Conteúdo Contentstack](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |
| Cabeçalhos | Não são necessários cabeçalhos extras. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `content_type_uid` | UID do tipo de conteúdo | `<your_content_type_uid>` |
| `entry_uid` | UID de entrada | `<your_entry_uid>` |

**Autenticação**

| Nome da chave | Valor da chave | Adicionar a |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

Contentstack espera **ambas** chaves como cabeçalhos para solicitações de entrega.

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `environment` | Nome do ambiente | Variable | `<your_environment_name>` | Sim (ativado) |

+++

### Akeneo {#akeneo}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente suportado pelo Akeneo. Confirme os detalhes da API atual com a documentação do Akeneo.

>[!BEGINSHADEBOX]

O Akeneo PIM expõe as APIs REST para produtos, atributos e mídia.

Casos de uso típicos incluem dados de produtos controlados em módulos de email e atributos para um determinado canal no jornada.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e as limitações do Akeneo.

Os seguintes pré-requisitos se aplicam:

* URL de base do PIM e cliente OAuth; estratégia de identificador ou UUID do produto.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* As respostas do PIM podem ser grandes. Mapeie somente os atributos necessários para personalização.
* As operações de gravação estão fora do escopo de exemplos típicos de personalização somente leitura.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o **GET** com um token de portador, solicite apenas as opções de atributo necessárias nos sinalizadores de consulta, cole a amostra de JSON, mapeie um conjunto de atributos mínimo, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API REST do Akeneo. Exemplo de padrão de URL:

   `https://{pim-host}/api/rest/v1/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplo de padrão: `https://{pim-host}/api/rest/v1/products-uuid/{uuid}` com `Accept: application/json`. Consulte [API Akeneo](https://api.akeneo.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Autorização | Autorização | Constante | `Bearer <YOUR_TOKEN>` | Sim (ativado) |
| Aceitar | Aceitar | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | Incluir opções de atributo | Variable | falso | Não (desativado) |
| `with_quality_scores` | Incluir pontuações de qualidade | Variable | falso | Não (desativado) |
| `with_completenesses` | Incluir Completenesses | Variable | falso | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | Autorização | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### Magnólia {#magnolia}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente apoiado pela Magnolia. Confirme os detalhes da API atual com a documentação do Magnolia.

>[!BEGINSHADEBOX]

O Magnolia oferece endpoints de entrega headless e REST dependendo da implantação.

Um caso de uso típico é o fornecimento de nós ou fragmentos de conteúdo para módulos de marketing.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e as limitações do Magnolia.

Os seguintes pré-requisitos se aplicam:

* URL da instância e token ou autenticação básica; espaço de trabalho e caminhos para entrega.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Os URLs de entrega REST dependem dos módulos e da configuração do Magnolia instalados.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o padrão de URL de entrega pública que seus módulos expõem, autentique de acordo com a orientação do Magnolia (entrega anônima vs. token para conteúdo protegido), cole a amostra de JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando o Magnolia REST (delivery). Exemplo de padrão de URL:

   `https://{author-or-public}/.rest/delivery/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplo de padrão: `https://{domain}/magnoliaAuthor/.rest/delivery/...` ou URLs de estilo tours de entrega pública. Seus caminhos dependem dos módulos instalados. Consulte a [documentação do Magnolia](https://docs.magnolia-cms.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| Aceitar | Aceitar | Constante | application/json | Sim (ativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | Autorização | `<bearer_token>` | Header |

Observação: a API de entrega é usar a função rest-anonymous para conteúdo que não exija um logon. Para obter acesso seguro a dados protegidos, é preferível um método mais robusto, como tokens de API ou OAuth 2.0.

+++


## Lealdade e recompensas {#loyalty-and-rewards}

### Voucherify {#voucherify}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado pelo Voucherify. Confirme os detalhes da API atual com a documentação do Voucherify.

>[!BEGINSHADEBOX]

O Voucherify fornece promoções e APIs REST de fidelidade (campanhas, vouchers, programas de fidelidade).

Casos de uso típicos incluem leitura de fidelidade ou estado promocional para ofertas no conteúdo e exibição de nível ou saldo, quando apropriado.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e as limitações do Voucherify.

Os seguintes pré-requisitos se aplicam:

* ID do aplicativo e segredo (por região/cluster); clareza sobre quais endpoints de fidelidade ou de campanha você chama.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Evite expor promoções internas ou identificadores de campanha em erros voltados para o cliente ou conteúdo de mensagem.
* Limites de taxa no nível do aplicativo são aplicados. Configurar novas tentativas e armazenamento em cache de acordo com a orientação do Voucherify.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Defina a URL de base para seu cluster, adicione os cabeçalhos necessários (`X-APP-ID`, `X-APP-TOKEN`), restrinja os pontos de extremidade da lista com filtros ou IDs, cole a amostra de JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando as APIs de fidelidade/REST. Por [Voucherify](https://docs.voucherify.io/){target="_blank"}, defina o host **cluster** e os caminhos para sua região. Exemplo de padrão de URL:

   `https://{cluster}.voucherify.io/`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Campos de integração de exemplo. Referência completa: [Voucherify API](https://docs.voucherify.io/reference/introduction){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| X-APP-ID | X-APP-ID | Constante | `<YOUR-APP-ID>` | Sim (ativado) |
| X-Voucherify-Channel | X-Voucherify-Channel | Constante | Voucherify Documentação | Não (desativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | Variable | 10 | Não (desativado) |
| `page` | `page` | Variable | 1 | Não (desativado) |
| `customer` | `customer` | Variable | `<customer_identifier>` | Não (desativado) |
| `created_at` | `created_at` | Variable | `<iso8601_date>` | Não (desativado) |
| `updated_at` | `updated_at` | Variable | `<iso8601_date>` | Não (desativado) |
| `order` | `order` | Variable | `<sort_field>` | Não (desativado) |
| `code` | `code` | Variable | `<loyalty_card_code>` | Não (desativado) |
| `ids` | `ids` | Variable | `<array_of_ids>` | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### Talon.One {#talon-one}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado por Talon.One. Confirme os detalhes da API atual com a documentação do Talon.One.

>[!BEGINSHADEBOX]

Talon.One é um mecanismo de regras de promoção e fidelidade com APIs REST para sessões, efeitos e perfis.

Casos de uso típicos incluem promoções no nível do carrinho ou do perfil em conteúdo personalizado e progresso de fidelidade ou exibição de recompensas.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Talon.One.

Os seguintes pré-requisitos se aplicam:

* Chave da API e URL de base específico da implantação; identificadores para o escopo do aplicativo ou da campanha.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Fluxos de sessão intensa podem exigir mapeamento cuidadoso para o modelo de solicitação de Integrações.
* Observe os limites de taxa de Talon.One e a orientação de idempotência.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o **GET** no perfil ou caminho de conquista necessário, defina `Authorization: ApiKey-v1 <key>` como documentado, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API de integração Talon.One. Exemplo de padrão de URL:

   `https://{your-domain}.talon.one/v1/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **método HTTP** | `GET` |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | Variable | em andamento / concluído / expirado | Não (desativado) |
| `startDate` | `startDate` | Variable | 2024-05-29T15:04:05+07:00 | Não (desativado) |
| `endDate` | `endDate` | Variable | 2024-05-29T15:04:05+07:00 | Não (desativado) |
| `pageSize` | `pageSize` | Variable | `<default_page_size>` | Não (desativado) |
| `skip` | `skip` | Variable | `<items_to_skip>` | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | Autorização | ApiKey-v1 `<YOUR_API_KEY>` | Header |

+++

### Antavo {#antavo}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado por Antavo. Confirme os detalhes da API atual com a documentação do Antavo.

>[!BEGINSHADEBOX]

Antavo é uma plataforma de fidelidade corporativa com APIs REST para membros, recompensas e eventos.

Casos de uso típicos incluem pontos, níveis ou recompensas por email ou push e ofertas orientadas por estado de fidelidade.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Antavo.

Os seguintes pré-requisitos se aplicam:

* Empilhar credenciais de URL e API; identificadores de programa ou loja, conforme necessário.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* As PII do cliente devem ser tratadas em contratos do Antavo e em suas políticas de privacidade.
* Confirme as versões da API e endpoints estáveis com o Antavo para o seu ambiente.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Configure o **GET** com a autenticação do fornecedor (por exemplo, chave de API na consulta), evite expor PII em relação à política, cole a amostra de JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API Antavo Enterprise.

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Campos de integração de exemplo usam o host **staging**; a produção usa seu nome de host da pilha Antavo. Consulte a [documentação do Antavo](https://antavo.com/docs/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| Aceitar | Aceitar | Constante | application/json | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | `api_key` | `<YOUR_API_KEY>` | Parâmetros de consulta |

+++

### Fidelidade Salesforce {#salesforce-loyalty}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido pela Salesforce nem é formalmente compatível com a. Confirme os detalhes da API atual com a documentação do Salesforce.

>[!BEGINSHADEBOX]

O Salesforce Loyalty Management expõe APIs REST na plataforma Salesforce para membros, programas e transações.

Casos de uso típicos incluem camada de superfície, pontos ou benefícios em jornadas e alinhamento de mensagens com dados de CRM e fidelidade.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Salesforce Loyalty.

Os seguintes pré-requisitos se aplicam:

* Instância do Salesforce, aplicativo conectado ou usuário de integração e OAuth apropriados para a sua organização.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Os limites da API do Salesforce e a atualização do token OAuth devem ser projetados na integração.
* As regras de compartilhamento e segurança em nível de campo regulam quais campos aparecem nas respostas da API.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o endpoint de integração de fidelidade que sua equipe aprova, conclua o Salesforce OAuth, cole a amostra de JSON, mapeie campos, respeite os limites da API composta, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando o Salesforce Loyalty Management REST. Exemplo de padrão de URL:

   `https://{instance}.salesforce.com/services/data/vXX.X/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Use a operação do GET **perfil de membro** do Gerenciamento de Fidelidade documentada para a versão da API da sua organização; os caminhos incluem identificadores de membro e programa. Consulte [desenvolvedores do Salesforce](https://developer.salesforce.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| Aceitar | Aceitar | Constante | application/json | Não (desativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | Variable | `<membership_number>` | Não (desativado) * |
| `membershipId` | `membershipId` | Variable | `<membership_id>` | Não (desativado) * |
| `posMemId` | `posMemId` | Variable | `<pos_mem_id>` | Não (desativado) * |

\* Pelo menos um dos três é obrigatório.

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | Autorização | `<access_token>` | Header |

+++

### Capilar {#capillary}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente apoiado pelo Capilar. Confirme os detalhes da API atual com a documentação do Capilary.

>[!BEGINSHADEBOX]

O Capilary fornece APIs de fidelidade e envolvimento comuns em pilhas de varejo.

Casos de uso típicos incluem pontos, camadas ou ofertas dentro de jornadas personalizadas.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Capilary.

Os seguintes pré-requisitos se aplicam:

* Host e autenticação da API (solicitações geralmente assinadas; siga os documentos do Capillary ).
* Identificadores de programa para o endpoint.

As seguintes limitações e exclusões se aplicam:

* Os esquemas de autenticação e hosts regionais variam de acordo com a implantação. Confirme com Capilar para sua pilha.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Configure cabeçalhos como `CAP-API-ACCESS-TOKEN` conforme necessário, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando as APIs Capilares.

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplo: `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}` (o host varia por região). Valide o host e o esquema de autenticação com [Capilar](https://capillarytech.com/){target="_blank"}.


| Campo | Valor |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `reward_id` | ID da recompensa | `<your_reward_id>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| CAP-API-ACCESS-TOKEN | Token de acesso | Constante | `<YOUR_ACCESS_TOKEN>` | Sim (ativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## Modelos e mensagens {#templates-and-messaging}

### Stensul {#stensul}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado pelo Stensul. Confirme os detalhes da API atual com a documentação do Stensul.

>[!BEGINSHADEBOX]

O Stensul é uma plataforma de criação de email para modelos aprovados; o Journey Optimizer pode consumir metadados de modelo e regiões estruturadas por meio de sua API.

Casos de uso típicos incluem a importação de modelos aprovados e o mapeamento de regiões para atributos de perfil, além da reutilização de blocos controlados para builds de campanha escaláveis.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Stensul.

Os seguintes pré-requisitos se aplicam:

* Conta do Stensul com acesso à API e modelos publicados com tokens definidos.
* Acesso de administrador no Journey Optimizer para criar integrações.

As seguintes limitações e exclusões se aplicam:

* A edição no local do WYSIWYG de modelos do Stensul no Journey Optimizer não é abordada aqui.
* HTML grandes ou complexos em cargas úteis do modelo podem exigir análise e limpeza de segurança.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração.

1. Configure o endpoint usando o URL da API de Modelos do Stensul. Exemplo de padrão de URL:

   `https://api.stensul.com/v1/templates/{template_id}`

1. Configure a autenticação (chave de API ou OAuth por documentação da API do Stensul).

1. Definir variáveis de caminho, por exemplo, ID do modelo.

1. Cole uma amostra de resposta JSON para detecção de campo.

1. Mapeie os campos de modelo obrigatórios para campos de personalização do Journey Optimizer.

1. Teste a conexão e ative.

### Marigold {#marigold}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado por Marigold. Confirme os detalhes da API atual com a documentação do Marigold.

>[!BEGINSHADEBOX]

Marigold expõe APIs de fidelidade e envolvimento; os hosts diferem por geografia (nomes de host de módulo UE versus EUA).

Um caso de uso típico é o enriquecimento de mensagens com dados de fidelidade ou preferência de programas Marigold.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e as limitações do Marigold.

Os seguintes pré-requisitos se aplicam:

* URL base e credenciais do seu contrato; usuário da API de privilégio mínimo, quando possível.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Os pontos de acesso variam de acordo com o produto Marigold. Valide com o suporte ao Marigold para sua implantação.
* Os dados pessoais nas respostas do devem estar em conformidade com as políticas de retenção e do DPA.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Aponte para o host Marigold da sua região, defina a autenticação (a amostra abaixo usa `X-Api-Key` com chave e segredo), cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API REST do Marigold.

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

1. Marigold usa 2 endpoints com base na área geográfica para a qual a instância do cliente está ativa:

   * Europa: `https://{{customername}}.module.slgnt.eu`
   * EUA: `https://{{customername}}.module.slgnt.us`

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

O host base depende da região (por exemplo, `https://{{customername}}.module.slgnt.eu` ou `https://{{customername}}.module.slgnt.us`). Confirme os caminhos com o Marigold para sua implantação.

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | X-Api-Key | `<apiKey>:<apiSecret>` | Header |

+++

### Recomendações do Adobe Target {#adobe-target-recommendations}

>[!IMPORTANT]
>
>Essa configuração é um padrão ilustrativo testado pela equipe do Adobe Journey Optimizer. O Adobe Target Recommendations é um produto Adobe separado com seu próprio ciclo de lançamento e versão da API. Sempre confirme os detalhes da API atual com a [documentação para desenvolvedores do Adobe Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview) antes de implantar na produção.

>[!BEGINSHADEBOX]

O Adobe Target inclui Recommendations e APIs de entrega para experiências integradas ou do lado do servidor, sujeitas a direitos.

Casos de uso típicos incluem inserir recomendações nas experiências criadas no Journey Optimizer e alinhar chaves ao perfil ou contexto do Experience Platform.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Adobe Target Recommendations.

Os seguintes pré-requisitos se aplicam:

* Target com Recommendations, organização IMS e autenticação compatível.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* As APIs de recomendação e entrega exigem parâmetros específicos (por exemplo, mbox ou identificadores de produto). Siga a documentação do Adobe Target.
* Ajuste a latência e o cache do volume de envio e do caso de uso.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). As chamadas de entrega geralmente são **POST** com um corpo JSON. Configure o OAuth por [Autenticação de destino](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication){target="_blank"}, cole uma resposta de exemplo, mapeie campos e teste no volume esperado.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando as Recommendations do Target/APIs de entrega.

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **método HTTP** | `POST` |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| cliente | cliente | Variable | `<customer_client_code>` | Sim (ativado) |
| sessionId | sessionId | Variable | ` <session_identifier>` | Sim (ativado) |

**Autenticação**

Consulte [Configuração de autenticação do Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication) e adicione JSON à Carga.

**Solicitar carga**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## Dados, clima e operações {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente suportado pelo AccuWeather. Confirme os detalhes da API atual com a documentação do AccuWeather.

>[!BEGINSHADEBOX]

O AccuWeather expõe as APIs REST de previsão e localização para que as mensagens possam incluir trechos com reconhecimento de clima.

Casos de uso típicos incluem previsões curtas em email ou push e personalização de conteúdo usando valores de previsão vinculados ao perfil ou contexto.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do AccuWeather.

Os seguintes pré-requisitos se aplicam:

* Assinatura da API e chave; chave de localização ou fluxo de pesquisa de cidade.
* Acesso de administrador no Journey Optimizer para criar integrações.

As seguintes limitações e exclusões se aplicam:

* Confirme a forma de resposta JSON para a camada de assinatura AccuWeather. As integrações mapeiam campos a partir de respostas JSON.
* Observe os limites de taxa do AccuWeather e o armazenamento em cache recomendado.
* Resolver `locationKey` geralmente requer uma solicitação separada de geolocalização ou pesquisa de cidade antes das chamadas de previsão.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o **GET**, a menos que sua assinatura exija o contrário, anexe o parâmetro de consulta `apiKey`, mapeie `locationKey` e outras variáveis do perfil/contexto, cole a amostra JSON, mapeie campos e teste.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API de Previsões Diárias. Exemplo de padrão de URL:

   `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++Campos de integração de exemplo

Campos de integração de exemplo. Detalhes e camadas estão descritos em [APIs AccuWeather](https://developer.accuweather.com/apis){target="_blank"}. Você geralmente resolve `locationKey` com uma chamada de pesquisa de locais separados (por exemplo `.../locations/v1/cities/search?q={{cityName}}`).

| Campo | Valor |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `format` | `format` | Variable | json | Não (desativado) |
| `language` | `language` | Variable | pt-BR | Não (desativado) |
| `details` | `details` | Variable | Falso | Não (desativado) |
| `metric` | `metric` | Variable | Falso | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | `apiKey` | `<YOUR_API_KEY>` | Parâmetros de consulta |

+++

### ShipStation {#shipstation}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente suportado pelo ShipStation. Confirme os detalhes da API atual com a documentação do ShipStation.

>[!BEGINSHADEBOX]

O ShipStation oferece APIs de envio e pedido para transportadoras, rótulos e rastreamento.

Os casos de uso típicos incluem status do pedido, links de rastreamento ou ETAs de delivery em mensagens transacionais.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do ShipStation.

Os seguintes pré-requisitos se aplicam:

* Chave de API e segredo (Autenticação básica por documentos do ShipStation).
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Não exponha as chaves de API ShipStation no conteúdo da mensagem; mantenha as credenciais somente na configuração de integração.
* Os endpoints de lista paginados podem ser uma opção ruim para integrações; prefira GETs de recurso único quando possível.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Direcione o recurso que você precisa (pedidos vs. remessas), autentique de acordo com a [API de ShipStation](https://www.shipstation.com/docs/api/){target="_blank"}, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API REST do ShipStation. Exemplo de padrão de URL:

   `https://ssapi.shipstation.com/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

O exemplo **Obter Timer** a seguir ilustra uma chamada de tempo de automação ShipStation. Use o caminho exato e a autenticação do guia de integração do ShipStation ao reproduzi-lo no Journey Optimizer.

| Campo | Valor |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **método HTTP** | `POST` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | apiKey | `<your_api_key>` | Header |

**Carga da solicitação**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### RevenueCat {#revenuecat}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente suportado pelo RevenueCat. Confirme os detalhes da API atual com a documentação do RevenueCat.

>[!BEGINSHADEBOX]

O RevenueCat fornece status de assinatura e APIs de direitos para aplicativos.

Um caso de uso típico está refletindo o estado da assinatura em campanhas de ciclo de vida nas quais a política permite.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do RevenueCat.

Os seguintes pré-requisitos se aplicam:

* Chave da API secreta e identificadores de aplicativo; mapeamento estável entre perfis e IDs do cliente da RevenueCat.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Proteja chaves de API secretas e siga suas políticas de rotação.
* Os dados de assinatura e direito são confidenciais. Atenda aos requisitos de privacidade e consentimento.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Chame o REST **GET** modelado abaixo, autentique com o cabeçalho da chave secreta, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API REST do RevenueCat. Exemplo de padrão de URL:

   `https://api.revenuecat.com/v1/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplo de padrão: usar **Obter um produto** do RevenueCat (ou produto equivalente/GET de direito) de [documentos do RevenueCat](https://docs.revenuecat.com/){target="_blank"} com a URL base e a versão do seu projeto.

| Campo | Valor |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | Não (desativado) |
| `locale` | `locale` | Variable | `<locale_code>` | Não (desativado) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | Autorização | `Bearer <token>` | Header |

+++

### Databricks {#databricks}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido nem formalmente suportado pela Databricks. Confirme os detalhes da API atual com a documentação do Databricks.

>[!BEGINSHADEBOX]

Os databricks fornecem APIs SQL e REST sobre dados de lakehouse; rascunhos anteriores combinavam orientação de execução de instrução com uma amostra **jobs/get**.

Um caso de uso típico é o uso de atributos pequenos e desnormalizados de tabelas controladas para personalização com privilégio mínimo estrito.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Databricks.

Os seguintes pré-requisitos se aplicam:

* Host, token ou OAuth do Workspace por política de organização; entidade de serviço com escopo mínimo.
* Acesso de administrador no Journey Optimizer.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Prefira caminhos de leitura estreitos; se você usar a execução da instrução **POST**, inclua o corpo JSON que a API exige, cole uma amostra de resposta de sucesso para mapeamento, teste a latência cuidadosamente e ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API de Execução de Instrução SQL dos Databricks. Exemplo de padrão de URL:

   `https://{workspace-host}/api/2.0/sql/statements/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++Campos de integração de exemplo

O exemplo de trabalho **GET** abaixo é ilustrativo. Para personalização orientada por SQL, prefira o padrão [API de execução de instrução](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"} compatível com seu espaço de trabalho.

| Campo | Valor |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |
| Autenticação | OAuth |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Aceitar | Aceitar | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | Variable | `12` | Sim |

+++

## Revisões, consentimento e social {#reviews-consent-and-social}

### Bynder {#bynder}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado por Bynder. Confirme os detalhes da API atual com a documentação do Bynder.

>[!BEGINSHADEBOX]

Bynder é um DAM com APIs REST; integrações geralmente usam OAuth 2.0 para metadados somente leitura ou URLs de ativos.

Casos de uso típicos incluem extrair metadados de ativos ou URLs de entrega em mensagens e manter a criação aprovada no Bynder alinhada com as jornadas.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e as limitações do Bynder.

Os seguintes pré-requisitos se aplicam:

* Domínio do portal e cliente OAuth (ou abordagem de token aprovada).
* Escopos para acesso somente leitura; acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* A paginação e a atualização do token OAuth devem seguir as regras de API do Bynder.
* Respostas paginadas grandes: mapeie apenas os campos necessários para personalização.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Configure o **GET** no ponto de extremidade escolhido (um padrão comum é uma lista de usuários), conclua o OAuth por [Bynder](https://developer.bynder.com/){target="_blank"}, evite extrair páginas desnecessárias de dados, mapeie campos, teste e ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API Bynder v4. Exemplo de padrão de URL:

   `https://{your-bynder-domain}/api/v4/users/`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Campos de integração de exemplo. Consulte a [Documentação da API Bynder](https://developer.bynder.com/){target="_blank"} para obter detalhes sobre a carga do OAuth 2.0.

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| Autorização | Autorização | Constante | Portador `<token>` | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | Variable | Falso | Não (desativado) |
| `limit` | `limit` | Variable | 100 | Não (desativado) |
| `page` | `page` | Variable | 1 | Não (desativado) |

**Autenticação**

| Tipo | Conteúdo |
| --- | --- |
| OAuth 2.0 | Carga do OAuth 2.0 (consulte a documentação do Bynder) |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido pela Trustpilot nem é formalmente suportado por ela. Confirme os detalhes da API atual com a documentação do Trustpilot.

>[!BEGINSHADEBOX]

O Trustpilot fornece APIs para negócios e revisa dados de resumo onde seu caso de uso e contrato permitirem.

Um caso de uso típico é a exibição de contagens de análises ou classificações em conteúdo de marketing em conformidade com os termos do Trustpilot.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Trustpilot.

Os seguintes pré-requisitos se aplicam:

* Chave de API e caso de uso aprovado; identificadores de negócios para consultas.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* O uso dos dados do Trustpilot deve estar em conformidade com as políticas de marca e uso de dados do Trustpilot.
* Os limites de taxa se aplicam ao resumo da análise e aos endpoints relacionados.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Configure o **GET** com a autenticação de consulta necessária, mapeie identificadores de perfil ou contexto, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando as APIs Trustpilot. Exemplo de padrão de URL:

   `https://api.trustpilot.com/v1/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Use as categorias que listam a operação de [Trustpilot developers](https://developers.trustpilot.com/){target="_blank"} para o seu padrão de integração; os parâmetros variam de acordo com o recurso.

| Campo | Valor |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | Não (desativado) |
| `locale` | `locale` | Variable | `<locale_code>` | Não (desativado) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | apiKey | `<your_api_key>` | Header |

+++

### Bazaarvoice {#bazaarvoice}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido ou formalmente apoiado pelo Bazaarvoice. Confirme os detalhes da API atual com a documentação do Bazaarvoice.

>[!BEGINSHADEBOX]

O Bazaarvoice fornece classificações, revisões e APIs de UGC.

Um caso de uso típico é a exibição de resumos de revisões ou classificações por email quando a política permitir.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Bazaarvoice.

Os seguintes pré-requisitos se aplicam:

* Chave de acesso da API e identificadores de clientes do seu contrato.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* A exibição de classificações e revisões deve seguir as políticas de conteúdo do Bazaarvoice.
* Limites de taxa e regras de cache se aplicam por chave de API.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o **GET** com `passkey` como parâmetro de consulta na API de Conversas, defina `Accept: application/json`, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API Bazaarvoice Conversations. Exemplo de padrão de URL:

   `https://api.bazaarvoice.com/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplo de ponto de entrada: `https://api.bazaarvoice.com/data/products.json` com parâmetros de consulta de versão e filtro. Consulte [desenvolvedor do Bazaarvoice](https://developer.bazaarvoice.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Aceitar | Aceitar | Constante | application/json | Sim (ativado) |

**Autenticação**

| Tipo | Valor da chave | Localização |
| --- | --- | --- |
| chave de acesso | `<YOUR_ACCESS_TOKEN>` | Parâmetros de consulta |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | Constante | 5.4 | Sim (ativado) |
| `filter` | `filter` | Variable | ID:47950830 | Não (desativado) |
| `stats` | `stats` | Variable | all | Não (desativado) |

+++

### OneTrust {#onetrust}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido pelo OneTrust nem é formalmente suportado por ele. Confirme os detalhes da API atual com a documentação do OneTrust.

>[!BEGINSHADEBOX]

O OneTrust expõe as APIs de privacidade e consentimento (URLs e esquemas específicos do produto).

Um caso de uso típico é a leitura de consentimento ou sinais de preferência para conteúdo condicional, onde a arquitetura e a revisão legal permitem.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do OneTrust.

Os seguintes pré-requisitos se aplicam:

* Credenciais da API e URL de base regional; aprovação legal para campos usados em mensagens.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Os dados de consentimento e preferência são altamente regulamentados. Coordenar com equipes jurídicas e de privacidade.
* Os caminhos e as cargas da API diferem de acordo com o produto OneTrust. Use a documentação da sua assinatura.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use o esquema publicado ou o caminho do centro de preferências em seus documentos de assinatura, conclua o OAuth se necessário, cole a amostra de JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API do OneTrust. Seu locatário, produto e caminho vêm da documentação do [OneTrust](https://developer.onetrust.com/){target="_blank"} para sua assinatura. Exemplo de padrão de URL:

   `https://{tenant}.my.onetrust.com/api/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

| Campo | Valor |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| **Autenticação** | OAuth |

**Parâmetros de caminho**

| Parâmetro | Nome | Valor |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Aceitar | Aceitar | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `state` | `state` | constante | PUBLICADO | Sim |

+++

#### Esquema do centro de preferências (publicado)

Exemplo de padrão (fragmento): `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`. Confirme o caminho exato em [OneTrust Developer](https://developer.onetrust.com/){target="_blank"}.

### Meta {#meta}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Ele não é mantido pela Meta nem é formalmente compatível com a. Confirme os detalhes da API atual com a documentação do Meta.

>[!BEGINSHADEBOX]

As APIs de gráfico e marketing da Meta expõem objetos de catálogo e campanha para integrações de negócios autorizadas.

Um caso de uso típico é o enriquecimento de conteúdo com atributos do Meta, onde tokens e políticas permitem.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Meta.

Os seguintes pré-requisitos se aplicam:

* Token de aplicativo ou usuário do sistema com permissões corretas; alinhamento do Business Manager.
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Os tokens de acesso de curta duração exigem uma estratégia de renovação ou de longa duração adequada às integrações no lado do servidor.
* Esteja em conformidade com os Termos da plataforma Meta; não registre tokens ou outros segredos nas cargas da mensagem.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Frequentemente, as chamadas de gráfico são **GET** com um caminho com controle de versão; manipule a expiração do token, cole a amostra de JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API gráfica do Meta. Exemplo de padrão de URL:

   `https://graph.facebook.com/vXX.X/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Campos de integração de exemplo. Consulte a [API gráfica](https://developers.facebook.com/docs/graph-api){target="_blank"} para obter o controle de versão e os tokens de acesso.

| Campo | Valor |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **método HTTP** | `GET` |
| Carga de resposta | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |
| Política | Configure os detalhes de nível de política de acordo com sua necessidade. |
| Autenticação | OAuth |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Aceitar | Aceitar | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | Variable | id | Não |
| `filter` | `filter` | Variable | — | Não |

+++

### Aprimo {#aprimo}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido nem formalmente apoiado pelo Aprimo. Confirme os detalhes da API atual com a documentação do Aprimo.

>[!BEGINSHADEBOX]

O Aprimo combina operações de marketing e APIs do DAM para registros, ativos e metadados.

Os casos de uso típicos incluem campos de registro ou ativo aprovados em conteúdo dinâmico e fluxos de trabalho controlados do DAM em setores regulamentados.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e as limitações do Aprimo.

Os seguintes pré-requisitos se aplicam:

* URL e credenciais do locatário (OAuth ou chave de API de acordo com a configuração).
* Acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* A segurança em nível de campo Aprimo deve se alinhar aos atributos mapeados no Journey Optimizer.
* Cargas grandes de HAL ou JSON: restrinja os campos mapeados ao conjunto mínimo necessário.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Use **GET** no caminho de registro necessário, envie cabeçalhos obrigatórios como `API-VERSION`, cole a amostra JSON (HAL ou JSON conforme retornado), mapeie um conjunto de campos mínimo, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando o DAM Aprimo/API de registros. Use a URL de base da API e o caminho de registros do seu **locatário** (por Aprimo). Exemplo de padrão de URL:

   `https://{tenant}.dam.aprimo.com/`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

| Campo | Valor |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **método HTTP** | `GET` |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |
| API-VERSION | API-VERSION | Constante | 1 | Sim (ativado) |
| Aceitar | Aceitar | Constante | application/hal+json OR application/json | Não (desativado) |
| select-record | select-record | Variable | `<selection_type>` | Não (desativado) |
| select-record-fields | select-record-fields | Variable | `<field_list>` | Não (desativado) |
| selecionar campo | selecionar campo | Variable | `<field_selection>` | Não (desativado) |

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | Autorização | Portador `<token>` | Header |

+++

### Epsilon (Epsilon3) {#epsilon}

>[!IMPORTANT]
>
>Este exemplo de configuração foi testado independentemente pela Adobe como um padrão de exemplo. Não é mantido ou formalmente apoiado por Epsilon. Confirme os detalhes da API atual com a documentação do Epsilon.

>[!BEGINSHADEBOX]

O Epsilon expõe as APIs por contrato empresarial; os URLs de base e a autenticação vêm da sua equipe de conta (o exemplo da API de eventos abaixo é ilustrativo).

Um caso de uso típico é a exposição de atributos de fidelidade ou oferta por meio de APIs JSON compatíveis.

>[!ENDSHADEBOX]

+++ Saiba mais sobre os pré-requisitos e limitações do Epsilon (Epsilon3).

Os seguintes pré-requisitos se aplicam:

* Credenciais e endpoints do Epsilon; acesso de administrador no Journey Optimizer.

As seguintes limitações e exclusões se aplicam:

* Os terminais e hosts são específicos do cliente. Não implante sem a documentação da sua equipe de conta Epsilon.

+++

Use o procedimento abaixo para configurar essa integração no Journey Optimizer. Consulte **Campos de integração de exemplo** para obter detalhes de solicitação e confirmar esses valores com a documentação do fornecedor para o seu ambiente.

1. Siga [Trabalhar com integrações](integrations.md). Não adivinhe URLs públicos. Use a especificação do Epsilon, cole a amostra JSON, mapeie campos, teste, ative.

1. No Journey Optimizer, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciar]** e selecione **[!UICONTROL Criar Integração]**.

1. Insira um nome de integração sem espaços.

1. Configure o endpoint usando a API Epsilon (de acordo com a especificação de integração). Os caminhos de recurso e URL de base são fornecidos pela equipe de conta do Epsilon. Exemplo de padrão de URL:

   `https://{your-instance}.epsilon3.io/api/...`

1. Selecione o método HTTP mostrado na tabela de configuração, normalmente GET, salvo indicação contrária.

1. Configure a autenticação (cabeçalhos, parâmetros de consulta ou OAuth) exatamente como especificado na tabela e na documentação do fornecedor.

1. Defina parâmetros de caminho, consulta e cabeçalho e mapeie variáveis para dados de perfil ou contextuais onde necessário.

1. Cole uma amostra de resposta JSON para que os campos possam ser detectados e mapeados.

1. Selecione os campos necessários para personalização no mapeamento de carga de resposta.

1. Configure políticas de tempo limite, tentativas e cache com base no volume esperado.

1. Teste a conexão e ative a integração.

A tabela abaixo lista os valores de exemplo para essa solicitação de integração.

+++ Campos de integração de exemplo

Exemplo de padrão: `https://{your-instance}.epsilon3.io/api/v1/planning/events` com `start` e `end` parâmetros de consulta e chave de API baseada em cabeçalho. Confirme com Epsilon antes da produção.

| Campo | Valor |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **método HTTP** | `GET` |
| **Política** | Configure os detalhes de nível de política de acordo com sua necessidade. |
| **Carga de resposta** | Selecione e configure os campos de resposta desejados para uso durante a criação, com base na resposta da API. |

**Parâmetros de caminho**

| Parâmetro de caminho | Nome | Valor padrão |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**Cabeçalhos**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| Tipo de conteúdo (padrão) | Tipo de conteúdo | Constante | application/json | Sim (ativado) |

**Parâmetros de consulta**

| Parâmetro | Nome | Tipo | Valor | Obrigatório |
| --- | --- | --- | --- | --- |
| `start` | `start` | Variable | 24/08/2019 T14:15:22Z | Sim (ativado) * |
| `end` | `end` | Variable | 24/08/2019 T14:15:22Z | Sim (ativado) * |
| `eventType` | `eventType` | Variable | programado/não programado | Não (desativado) |
| `exclude_recurrences` | `exclude_recurrences` | Variable | verdadeiro / falso | Não (desativado) |

\* Opcional para `eventType` = `unscheduled` e para `exclude_recurrences` = `true`.

**Autenticação**

| Tipo | Nome da chave de API | Valor da chave de API | Localização |
| --- | --- | --- | --- |
| Chave de API | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

