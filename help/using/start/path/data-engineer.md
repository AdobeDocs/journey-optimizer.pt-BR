---
solution: Journey Optimizer
product: journey optimizer
title: Introdução do Journey Optimizer ao engenheiro de dados
description: Como engenheiro de dados, saiba mais sobre como trabalhar com o Journey Optimizer
feature: Get Started
role: Data Engineer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: c2f32533027e374a1df26943e7c5acd4e1d13869
workflow-type: ht
source-wordcount: '573'
ht-degree: 100%

---

# Introdução ao engenheiro de dados {#data-engineer}

Como um **Engenheiro de dados do Adobe Journey Optimizer**, prepare e mantenha os dados do perfil do cliente para potencializar as experiências orquestradas por [!DNL Journey Optimizer], modele dados de clientes e negócios em esquemas e configure conectores de origem para assimilar dados. Você pode começar a trabalhar com o [!DNL Adobe Journey Optimizer] assim que o [Administrador do sistema](administrator.md) conceder acesso e preparar seu ambiente.


Saiba como **identificar dados e criar esquemas e conjuntos de dados** para enviar dados à Adobe Experience Platform nesta página.

>[!NOTE]
>
>Saiba mais sobre a **ingestão de dados** na [documentação da Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=pt-BR){target="_blank"}.

As etapas para criar um namespace de identidade e um conjunto de dados habilitado para perfis e perfis de teste são detalhadas nas seções abaixo:

1. **Criar um namespace de identidade**. Na Adobe [!DNL Journey Optimizer], as **Identidades** vinculam consumidores em dispositivos e canais, e o resultado é um gráfico de identidade. O gráfico de identidade vinculado é usado para personalizar experiências com base em interações em todos os pontos de contato comerciais.  Saiba mais sobre identidades e namespaces de identidade [nesta página](../../audience/get-started-identity.md).

1. **Crie um esquema** e ative-o para perfis. Um esquema é um conjunto de regras que representam e validam a estrutura e o formato dos dados. Em um alto nível, os esquemas fornecem uma definição abstrata de um objeto do mundo real (como uma pessoa) e destacam quais dados devem ser incluídos em cada instância desse objeto (como nome, sobrenome, aniversário e assim por diante).  Saiba mais sobre esquemas [nesta página](../../data/get-started-schemas.md).

1. **Crie conjuntos de dados** e ative-os para perfis. Um conjunto de dados é uma construção de armazenamento e gerenciamento para uma coleção de dados, normalmente uma tabela, que contém um esquema (colunas) e campos (linhas). Os conjuntos de dados também contêm metadados que descrevem vários aspectos dos dados armazenados. Depois que um conjunto de dados é criado, é possível mapeá-lo para um esquema existente e adicionar dados a ele. Saiba mais sobre conjuntos de dados [nesta página](../../data/get-started-datasets.md).

1. **Configurar conectores de fontes**. O Adobe Journey Optimizer permite que os dados sejam assimilados de fontes externas e, ao mesmo tempo, fornece a capacidade de estruturar, rotular e aprimorar os dados recebidos usando os serviços da plataforma. Você pode assimilar dados de várias fontes, como aplicativos Adobe, armazenamentos baseados em nuvem, bancos de dados e muitas outras. Saiba mais sobre conectores de origem [nesta página](../get-started-sources.md).

1. **Criar perfis de teste**. Os perfis de teste são necessários ao usar o [modo de teste](../../building-journeys/testing-the-journey.md) em uma jornada, e para [visualizar e testar suas mensagens](../../content-management/preview-test.md) antes de enviar. As etapas para criar perfis de teste são detalhadas [nesta página](../../audience/creating-test-profiles.md).


Além disso, para poder enviar mensagens em jornadas, você deve configurar as **[!UICONTROL Fontes de dados]**, os **[!UICONTROL Eventos]** e as **[!UICONTROL Ações]**. Saiba mais [nesta seção](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* A configuração da **fonte de dados** permite definir uma conexão com um sistema para recuperar informações adicionais que serão usadas em suas jornadas. Saiba mais sobre Fontes de dados [nesta seção](../../datasource/about-data-sources.md).

* Os **Eventos** permitem acionar as jornadas de forma unitária para enviar mensagens, em tempo real, ao indivíduo que flui para a jornada. Na configuração do evento, configure os eventos esperados nas jornadas. Os dados de entrada dos eventos são padronizados de acordo com o Adobe Experience Data Model (XDM). Os eventos vêm das APIs de ingestão de streaming para eventos autenticados e não autenticados (como eventos do SDK móvel da Adobe). Saiba mais sobre eventos [nesta seção](../../event/about-events.md).

* O [!DNL Journey Optimizer] vem com recursos de mensagem integrados: você pode criar suas mensagens em uma jornada e projetar o conteúdo. Se você estiver usando um sistema de terceiros para enviar mensagens, por exemplo, Adobe Campaign, crie uma **ação personalizada**. Saiba mais sobre ações [nesta seção](../../action/action.md).
