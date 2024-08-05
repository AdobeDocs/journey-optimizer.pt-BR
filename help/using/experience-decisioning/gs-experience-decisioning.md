---
title: Introdução à Escolha de experiências
description: Saiba mais sobre decisões de experiência
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilidade limitada"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 1d8ea66425b21ec831542bb36bb283c23760e94f
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 32%

---

# Introdução à Escolha de experiências {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>No momento, a Escolha de experiências está disponível apenas para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.
>
>Por enquanto, o recurso não está disponível para clientes que compraram o Adobe Systems **ofertas complementares do Healthcare Shield** e **do Escudo** de Privacidade e Segurança.

## O que é a decisão da experiência {#about}

A Escolha de experiências simplifica a personalização oferecendo um catálogo centralizado de ofertas de marketing conhecidas como “itens de decisão”, além de um mecanismo de decisão sofisticado. Esse mecanismo usa regras e critérios de classificação para selecionar e apresentar os itens de decisão mais relevantes para cada pessoa.

Esses itens de decisão são perfeitamente integrados em uma ampla gama de superfícies de entrada através das [novas experiência canal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based) baseadas em código, agora acessíveis nas campanhas do Journey Optimizer. As políticas de decisão da Escolha de experiências estão disponíveis para uso somente em campanhas de experiência baseadas em código.

## Etapas principais de decisão da experiência {#steps}

As principais etapas para trabalhar com Decisões de experiência são as seguintes:

1. **Atribuir permissões adequadas**. O Experience Decisioning só está disponível para usuários com acesso a uma função relacionadas **[!UICONTROL a Decisões]** de experiência, como Gerentes de decisão. Se não for possível acessar a Decisão da experiência, suas permissões devem ser estendidas.

   ++Saiba mais sobre como atribuir os gerentes de decisão função

   1. Para atribuir um função a um usuário no [!DNL Permissions] produto, navegue até as **[!UICONTROL Funções]** guia e selecione Gestores de decisão.

      ![](assets/decision_permission_1.png)

   1. Na guia **[!UICONTROL Usuários]**, clique em **[!UICONTROL Adicionar usuário]**.

      ![](assets/decision_permission_2.png)

   1. Digite o nome de usuário ou endereço de email ou selecione o usuário na lista e clique em **[!UICONTROL Salvar]**.

      Se o usuário não foi criado anteriormente, consulte a [documentação Adicionar usuários](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   O usuário deve receber um email de redirecionamento para sua instância.

+++

1. **Configure atributos personalizados**: adapte o catálogo de itens a seus requisitos específicos configurando atributos personalizados no schema do catálogo.

1. **Criar itens de decisão que serão exibidos** no público-alvo direcionado.

1. **Organizar com coleções**: use coleções para categorizar itens de decisão com base em regras baseadas em atributos. Incorpore coleções em suas estratégias de seleção para determinar quais coleção de itens de decisão devem ser consideradas.

1. **Criar regras** de decisão: as regras de decisão são usadas em itens de decisão e/ou estratégias de seleção para determinar para quem um item de decisão pode ser exibido.

1. **Implemente métodos** classificação: Criar classificação métodos e aplicá-los dentro de estratégias de decisão para determinar a prioridade solicitar para a seleção de itens de decisão.

1. **Criar estratégias** de seleção: crie estratégias de seleção que usar coleções, regras de decisão e métodos classificação para identificar os itens de decisão adequados para exibição em perfis.

1. **Incorpore uma decisão política em seu campanha** baseado em código: as políticas de decisão combinam várias estratégias de seleção para determinar os itens de decisão elegíveis a serem exibidos para o público-alvo pretendido.
