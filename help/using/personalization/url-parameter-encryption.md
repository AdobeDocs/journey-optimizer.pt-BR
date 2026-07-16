---
solution: Journey Optimizer
product: journey optimizer
title: Criptografar parâmetros de URL
description: Saiba como criptografar parâmetros de consulta de URL confidenciais para que o PII não seja exposto em texto sem formatação em links de rastreamento e páginas de aterrissagem do Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
keywords: criptografia, URL, rastreamento, página de aterrissagem, registro de chaves, personalização, segurança, privacidade, sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 1%

---

# Criptografar parâmetros de URL {#url-parameter-encryption}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como criptografar parâmetros de consulta de URL confidenciais para que informações de identificação pessoal não sejam expostas em texto sem formatação, incluindo como os administradores criam, giram e revogam chaves no registro de chave da sandbox do Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
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

>[!IMPORTANT]
>
>Para acessar e gerenciar chaves, você deve ter as permissões **Exibir Registro de Chave** e **Gerenciar Registro de Chave** concedidas. [Saiba mais](../administration/high-low-permissions.md#administration-permissions)

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

## Referência rápida {#quick-reference}

Esta seção contém conhecimento estruturado destinado a oferecer suporte à interpretação, recuperação e resposta a perguntas relacionadas a este tópico.

Para uma compreensão completa, essas informações devem ser combinadas com a documentação desta página. Nenhuma das origens deve ser independente; a página descreve o recurso, enquanto esta seção fornece um contexto adicional que ajuda a desfazer a ambiguidade da terminologia, intenção, aplicabilidade e restrições.

>[!BEGINTABS]

>[!TAB Visão geral]

**TL;DR**

Esta página explica como os administradores criam, giram e revogam chaves de criptografia no registro de chaves em nível de sandbox da Journey Optimizer, permitindo que os profissionais de marketing criptografem parâmetros de consulta de URL confidenciais para que as PII não sejam expostas em texto simples em links de rastreamento e páginas de aterrissagem.

**Intenções**

* Entenda por que a criptografia de parâmetro de URL é necessária (dados confidenciais e PII visíveis em sequências de consulta de texto sem formatação)
* Criar chaves de criptografia no registro de chaves da sandbox (tarefa do administrador que requer permissões específicas)
* Revogar uma chave para desabilitá-la permanentemente para nova criptografia
* Girar uma chave para fornecer novo material criptográfico, mantendo o mesmo identificador
* Use o auxiliar `Encrypt` no editor de personalização para proteger valores de parâmetro de consulta específicos

>[!TAB Glossário]

* **Registro de chave**: um repositório em nível de sandbox no Journey Optimizer (Administração > Configurações), onde os administradores criam e gerenciam chaves de criptografia usadas pelo auxiliar de criptografia do parâmetro de URL. *(específico do produto)*
* **Auxiliar de criptografia (`Encrypt`)**: uma função auxiliar no editor de personalização que criptografa um valor de expressão no momento da renderização, substituindo o PII por texto cifrado em parâmetros de consulta de URL. *(específico do produto)*
* **Revogar (chave)**: o ato de desabilitar permanentemente uma chave para nova criptografia; a entrada de chave permanece visível no Registro para auditoria e cargas mais antigas ainda podem exigi-la para descriptografia nos sistemas da organização.
* **Girar (chave)**: o ato de fornecer novo material criptográfico para uma chave, mantendo seu identificador estável; portanto, campanhas e jornadas que já fazem referência a essa chave não precisam ser atualizadas.
* **PII (Informações de identificação pessoal)**: dados que podem identificar um indivíduo — como atributos de perfil, tokens ou identificadores de oferta — que deve ser protegido quando incluído nos parâmetros de consulta de URL.

>[!TAB Terminologia]

* **Nome canônico:** Criptografia de parâmetro de URL — variantes: criptografia de URL, criptografia de parâmetro de consulta, ofuscação de parâmetro de URL
* **Sinônimos:** &quot;registro de chave&quot; = &quot;Registro de chave&quot; (rótulo da interface do usuário em Administração > Configurações)
* **Não confundir:** Revogar (desabilita permanentemente a chave para nova criptografia; a entrada permanece para auditoria) ≠ Girar (substitui material criptográfico, mas mantém o mesmo identificador de chave ativo para nova criptografia)

>[!TAB Medidas de proteção e limitações]

* No momento, a criptografia de parâmetros de URL está disponível apenas para o canal de email.
* Exige permissões **Exibir Registro de Chave** e **Gerenciar Registro de Chave** para acessar e gerenciar chaves.
* A descriptografia é responsabilidade da organização. O Journey Optimizer criptografa valores no momento da renderização; o site, aplicativo ou API deve descriptografar parâmetros usando o mesmo material e processos criptográficos definidos pela organização.
* Somente chaves ativas devem ser usadas para criptografar novos valores no editor de personalização; chaves revogadas não devem ser usadas para novo conteúdo.
* As chaves revogadas permanecem visíveis no registro para fins de auditoria; elas ainda podem ser necessárias para que os sistemas da organização descriptografem cargas mais antigas.

>[!TAB Perguntas frequentes]

**P: Quem é responsável pela descriptografia?**

A descriptografia é responsabilidade da organização. O Journey Optimizer criptografa valores quando a mensagem é renderizada. O site, aplicativo ou API deve descriptografar parâmetros de consulta usando o mesmo material e processos criptográficos que a organização definiu.

**P: Qual é a diferença entre Revogar e Girar?**

Revogar desativa permanentemente uma chave para nova criptografia enquanto mantém a entrada visível no registro para auditoria (cargas mais antigas ainda podem precisar da chave para descriptografar nos sistemas da organização). A Rotate fornece novo material criptográfico para uma chave, mantendo o mesmo identificador de chave, de modo que as campanhas e jornadas que fazem referência a ele continuem a funcionar sem atualizações.

**P: Quais permissões são necessárias para gerenciar chaves?**

**Exibir Registro de Chave** e **Gerenciar Registro de Chave** permissões.

**P: Quais canais oferecem suporte à criptografia de parâmetro de URL?**

Atualmente, apenas o canal de email.

**P: Uma chave revogada pode ser usada para a nova criptografia?**

Não. Quando uma chave é revogada, as tentativas de usá-la no assistente de criptografia devem falhar no momento da renderização. Não use chaves revogadas para o novo conteúdo.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: c594ce24 -->
