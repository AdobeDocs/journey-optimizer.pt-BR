---
solution: Journey Optimizer
product: journey optimizer
title: Criptografar parâmetros de URL
description: Saiba como criptografar parâmetros de consulta de URL confidenciais para que o PII não seja exposto em texto sem formatação em links de rastreamento e páginas de aterrissagem do Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="Disponibilidade limitada" type="Informative"
keywords: criptografia, URL, rastreamento, página de aterrissagem, registro de chaves, personalização, segurança, privacidade, sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 3%

---

# Criptografar parâmetros de URL {#url-parameter-encryption}

>[!AVAILABILITY]
>
>Esse recurso está disponível em Disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.
>
>No momento, esse recurso só está disponível para o canal de email.

## Por que usar a criptografia de parâmetro de URL? {#why-url-parameter-encryption}

Os links de rastreamento personalizados e os URLs de página de aterrissagem geralmente incluem atributos de perfil, identificadores, tokens ou outros valores na sequência de consulta. Normalmente, esses parâmetros são visíveis como texto sem formatação no email ou SMS e permanecem legíveis se alguém copiar, compartilhar ou marcar o link. Isso pode ser um risco à segurança e à privacidade quando os valores puderem incluir informações de identificação pessoal (PII) ou outros dados confidenciais que eles precisam proteger.

[!DNL Journey Optimizer] fornece um auxiliar de criptografia no editor de personalização para que você possa criptografar qualquer valor de expressão no momento da renderização (por exemplo, um atributo de perfil, um token ou uma cadeia de caracteres criada a partir de vários campos). A criptografia sempre requer uma chave do registro de sua organização.

Você criptografa somente os parâmetros de consulta escolhidos, usando chaves que os administradores gerenciam em um registro em nível de sandbox, de modo que os valores confidenciais não sejam deixados expostos em texto não criptografado quando o link for compartilhado ou inspecionado.

### Como funciona {#how-it-works}

* **Administradores** usam o Registro de chaves para [criar chaves](#create-keys) e [gerenciar chaves](#manage-keys) de acordo com as políticas de segurança de sua organização.
* **Os profissionais de marketing** inserem o auxiliar `Encrypt` no editor de personalização e passam o valor a ser protegido, além de um identificador de chave ativo do Registro. Para obter sintaxe e opções, consulte [esta seção](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>A descriptografia é responsabilidade de sua organização. [!DNL Journey Optimizer] criptografa valores quando a mensagem é renderizada. Seu site, aplicativo ou API deve descriptografar parâmetros usando o mesmo material e processos criptográficos definidos por você, consistente com seu modelo de segurança.

### Exemplo

Uma URL de página de aterrissagem pode usar um parâmetro de consulta, como `token`, cujo valor é um token de cadeia de caracteres (por exemplo, uma carga JSON com identificadores de oferta ou perfil). Sem criptografia, esse token de string fica visível como texto simples no link. Quebrar esse valor com o auxiliar de criptografia substitui a carga confidencial por texto cifrado no URL, deixando o restante do link inalterado.

## Criar chaves {#create-keys}

Antes de poder usar o auxiliar de criptografia de parâmetro de URL, é necessário criar uma chave. Para isso, siga as etapas abaixo.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)
-->

1. Vá para **[!UICONTROL Administração]** > **[!UICONTROL Configurações]**.

1. Clique no botão **[!UICONTROL Gerenciar]** para abrir o **[!UICONTROL Registro de chave]**.

   ![Seção de Registro de chave no menu Administração](assets/encryption-key-registry.png){width="80%"}

1. Usando o botão dedicado, crie as chaves conforme necessário para sua organização.

   ![Botão Criar chave na seção Registro de chave](assets/encryption-create-key.png){width="80%"}

1. Atribua a eles um rótulo ou identificador claro que suas equipes possam fazer referência no editor de personalização.

   ![Detalhes da chave na seção Registro da chave](assets/encryption-key-details.png){width="80%"}

1. Clique em **[!UICONTROL Enviar]** para confirmar as alterações.

Depois que uma chave é criada, os profissionais de marketing podem usar o auxiliar [criptografia de parâmetros de URL](functions/helpers.md#url-parameter-encryption-helper) no editor de personalização para criptografar valores específicos que colocam nos parâmetros de consulta de URL.

## Gerenciar chaves {#manage-keys}

Para gerenciar chaves, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Registro de chave]**. Você pode ver todas as chaves criadas para a sandbox atual em uma exibição de lista.

   ![Exibição da lista de chaves do Registro](assets/encryption-key-registry-list.png){width="100%"}

1. Clique em uma chave com o status **[!UICONTROL Ativo]** para abrir os detalhes da chave.

   ![Detalhes da chave ativa](assets/encryption-key-active-details.png){width="80%"}

1. Clique no botão **[!UICONTROL Revogar]** para desabilitar permanentemente a chave para nova criptografia.

   Quando uma chave é revogada, as tentativas de usá-la no auxiliar devem falhar no momento da renderização. As entradas revogadas permanecem visíveis para auditoria; talvez suas equipes ainda precisem do material correspondente para descriptografar cargas úteis mais antigas em seus próprios sistemas.

1. Clique no botão **[!UICONTROL Girar]** para fornecer novo material importante, mantendo um identificador de chave estável no qual suas jornadas e campanhas já fazem referência.

   O material anterior é mantido no registro com um status revogado e um motivo apropriado (por exemplo, um carimbo de data e hora de rotação), e uma nova linha ou versão reflete a chave ativa.

   >[!NOTE]
   >
   >Somente chaves ativas devem ser selecionadas para criptografar novos valores no editor de personalização. Não use chaves revogadas para o novo conteúdo.
