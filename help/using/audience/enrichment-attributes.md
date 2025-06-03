---
solution: Journey Optimizer
product: journey optimizer
title: Sobre públicos-alvo da Adobe Experience Platform
description: Saiba como trabalhar com públicos-alvo da Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3ec496ba-7555-49e2-992c-403c33302a90
source-git-commit: b6fe3fec0c64983fc2317027a5748a0d44c18469
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 3%

---

# Usar atributos de enriquecimento de públicos-alvo {#enrichment}

Ao direcionar um público-alvo gerado por meio de workflows de composição, público-alvo personalizado (arquivo CSV) ou Composição de público federado, você pode usar atributos de enriquecimento desses públicos-alvo para criar sua jornada e personalizar suas mensagens.

>[!NOTE]
>
>Os públicos-alvo criados por meio do upload personalizado de arquivo CSV antes de 1° de outubro de 2024 não estão qualificados para personalização. Para usar atributos desses públicos-alvo e utilizar totalmente esse recurso, recrie e faça upload de qualquer público CSV externo importado antes dessa data.
>
>As políticas de consentimento não oferecem suporte a atributos de enriquecimento. Portanto, quaisquer regras de política de consentimento devem ser baseadas apenas nos atributos encontrados no perfil.

Estas são as ações que você pode executar usando os atributos de enriquecimento dos públicos-alvo:

* **Crie vários caminhos em uma jornada** com base em regras que usam os atributos de enriquecimento do público-alvo. Para fazer isso, direcione o público usando uma atividade [Ler público-alvo](../building-journeys/read-audience.md) e, em seguida, crie regras em uma atividade [Condição](../building-journeys/condition-activity.md) com base nos atributos de enriquecimento do público-alvo.

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* **Personalize suas mensagens** em jornadas ou campanhas adicionando atributos de enriquecimento do público-alvo direcionado no editor de personalização. [Saiba como trabalhar com o editor de personalização](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!IMPORTANT]
>
>Para usar atributos de enriquecimento de públicos-alvo criados usando workflows de composição, verifique se eles foram adicionados a um Grupo de campos no Data Source da &quot;ExperiencePlatform&quot;.
>
+++ Saiba como adicionar atributos de enriquecimento a um Grupo de campos>
>
1. Navegue até &quot;Administração&quot; > &quot;Configuração&quot; > &quot;Fontes de dados&quot;.
1. Selecione &quot;Experience Platform&quot; e crie ou edite um Grupo de campos.
1. No seletor de schema, selecione o schema apropriado. O nome do esquema seguirá este formato: &quot;Esquema para audienceId:&quot; + a ID do público-alvo. Você pode encontrar a ID do público-alvo na tela de detalhes do público-alvo no inventário de público-alvo.
1. Abra o seletor de campos, localize os atributos de enriquecimento que deseja adicionar e marque a caixa de seleção ao lado deles.
1. Salve as alterações.
1. Depois que os atributos de enriquecimento forem adicionados a um Grupo de campos, você poderá usá-los no Journey Optimizer nos locais listados acima.
>
Informações detalhadas sobre fontes de dados estão disponíveis nestas seções:
>
* [Trabalhar com a fonte de dados do Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
* [Configurar uma fonte de dados](../datasource/configure-data-sources.md)
>
+++







+++ O que são atributos de enriquecimento?

Os atributos de enriquecimento são atributos adicionais que são contextuais e específicos a um público-alvo. Eles não estão associados ao perfil e são normalmente usados para fins de personalização.

Os atributos de enriquecimento são vinculados a um público-alvo por meio de uma atividade Enrich na composição do público-alvo ou no processo de upload personalizado.

+++

+++ Onde posso usar atributos de enriquecimento no Journey Optimizer?

Os atributos de enriquecimento da composição de público-alvo podem ser aproveitados nas seguintes áreas. [Saiba como usar atributos de enriquecimento de públicos-alvo](#enrichment)

* Atividade de condição (Jornada)
* Atributos de ação personalizados (Jornada)
* Personalização de mensagens (Jornadas e campanhas)

+++

+++ Como ativar atributos de enriquecimento no Jornada?

Para usar atributos de enriquecimento de públicos-alvo criados usando workflows de composição, verifique se eles foram adicionados a um Grupo de campos no Data Source da &quot;ExperiencePlatform&quot;. Informações sobre como adicionar atributos de enriquecimento a um Grupo de Campos estão disponíveis em [esta seção](#enrichment)

+++

+++ Os valores do atributo de enriquecimento são atualizados após o início de uma jornada?

Atualmente, não. Mesmo depois dos nós de espera ou evento, os valores do atributo de enriquecimento permanecem os mesmos de quando a jornada foi iniciada.

+++
