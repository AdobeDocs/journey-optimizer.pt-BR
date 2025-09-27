---
solution: Journey Optimizer
product: journey optimizer
title: Introdução ao conteúdo multilíngue
description: Saiba mais sobre o conteúdo multilíngue no Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introdução, iniciar, conteúdo, experimento
exl-id: b57683b4-6dcc-4f6c-a8b2-4ba371d78d21
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 32%

---

# Introdução ao conteúdo multilíngue {#multilingual-gs}

>[!CONTEXTUALHELP]
>id="ajo_multi_translation_homepage"
>title="Traduções"
>abstract="O recurso multilíngue permite que você crie facilmente conteúdo em vários idiomas em uma única campanha ou jornada. Na página Traduções, é possível configurar projetos, selecionar provedores de tradução ou gerenciar dicionários específicos da localidade"

O recurso multilíngue permite criar conteúdo em vários idiomas facilmente em uma única campanha ou jornada. Com esse recurso, você pode alternar entre idiomas ao editar sua campanha, simplificando todo o processo de edição e melhorando sua capacidade de gerenciar com eficiência o conteúdo multilíngue.

Com o Journey Optimizer, você tem a possibilidade de criar conteúdo multilíngue por meio de dois métodos distintos:

* **Tradução manual**: traduza seu conteúdo diretamente no Designer de email ou importe conteúdo multilíngue existente. [Saiba mais](multilingual-manual.md)

* **Tradução automática**: envie conteúdo para o seu provedor de idioma preferido para tradução automática. [Saiba mais](multilingual-automated.md)

</br>

![](assets/translation_schema.png)

## Pré-requisitos {#prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_multi_translation_error"
>title="Erro de tradução"
>abstract="Caso não seja possível acessar a página Tradução, é provável que o recurso Tradução não esteja habilitado. Para resolver esse problema, verifique se o recurso Tradução foi ativado pelo(a) admin da organização e da sandbox."

Atualmente, o Adobe Journey Optimizer integra-se com provedores de tradução, que oferecem serviços de tradução de terceiros (tradução automática ou tradução humana) independentes do Adobe Journey Optimizer.

Antes de adicionar o Provedor de tradução selecionado, você deve criar uma conta com esse provedor aplicável.

O uso dos serviços de tradução de um Provedor de tradução está sujeito a termos e condições adicionais desse provedor aplicável.  Como soluções de terceiros, os serviços de tradução estão disponíveis para usuários do Adobe Journey Optimizer por meio de uma integração.  A Adobe não controla e não se responsabiliza por produtos de terceiros.

Para problemas ou solicitações de assistência relacionados às suas traduções, entre em contato com o Provedor de tradução aplicável.

Para o conteúdo multilíngue, as seguintes configurações devem ser definidas:

* Para usar o recurso de Tradução no Journey Optimizer, é necessário atribuir a API à função correspondente. [Saiba mais](https://experienceleague.adobe.com/pt-br/docs/experience-platform/landing/platform-apis/api-authentication#assign-api-to-a-role)

* Para começar a criar conteúdo multilíngue, os usuários precisam ter a permissão **[!UICONTROL Gerenciar configurações de idioma]**. Para o fluxo automatizado, os usuários também precisarão de permissões relacionadas aos recursos do **[!UICONTROL Serviço de Tradução]**. [Saiba mais sobre permissões](../administration/permissions.md)

  +++ Saiba como atribuir permissões relacionadas multilíngues

   1. No produto **Permissões**, abra a guia **Funções** e selecione a **função** desejada.

   1. Clique em **Editar** para modificar as permissões.

   1. Adicione o recurso **Serviço de tradução** e selecione as permissões multilíngues apropriadas no menu suspenso.

      ![](assets/multilingual-permission.png){zoomable="yes"}

   1. Clique em **Salvar** para aplicar as alterações.

      As permissões de todos os usuários já atribuídos a essa função serão atualizadas automaticamente.

   1. Para atribuir essa função a novos usuários, navegue até a guia **Usuários** no painel **Funções** e clique em **Adicionar usuário**.

   1. Insira o nome do usuário, seu endereço de email ou escolha na lista e clique em **Salvar**.

   1. Se o usuário não tiver sido criado anteriormente, consulte [esta documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/access-control/abac/permissions-ui/users).

  +++

* Se você não conseguir acessar a página Tradução, será necessário habilitar o recurso Tradução e receber **[!UICONTROL Permissões relacionadas ao serviço de Tradução]**. [Saiba mais](../administration/ootb-permissions.md)

  +++ Saiba como habilitar o recurso de Tradução

   1. Se você estiver vendo a seguinte página de erro, isso indica que o recurso **[!UICONTROL Tradução]** ainda não foi habilitado. Entre em contato com o administrador da organização e da sandbox para solicitar acesso.

  ![](assets/multi-troubleshoot.png)

   1. O administrador precisará navegar até o menu **[!UICONTROL Tradução]** na barra lateral esquerda.

      O sistema habilitará automaticamente o recurso Tradução.

   1. Depois que o recurso for habilitado com êxito, você poderá acessar a página **[!UICONTROL Tradução]**, juntamente com as guias **[!UICONTROL Projetos]**, **[!UICONTROL Provedores]** e **[!UICONTROL Localidade]**.

   1. Se esse procedimento falhar, você ainda verá a mesma página de erro. Nesse caso, entre em contato com o representante da Adobe para obter mais assistência.

  +++

## Vídeo tutorial {#video}

Saiba como criar conteúdo em vários idiomas em uma única campanha ou jornada.

>[!VIDEO](https://video.tv.adobe.com/v/3430921/)
