---
solution: Journey Optimizer
product: journey optimizer
title: Verificação e envio de uma mensagem de correspondência direta
description: Saiba como verificar e enviar uma mensagem de correspondência direta no Journey Optimizer
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
TQID: https://experienceleague.adobe.com/4GZKFKOx-D-RT1mssiV5vpmZQSJGVbGMro8Q-suhtPE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 114f184e73298bf79d666ef7b17755498c93df83
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 15%

---

# Verificação e envio de uma mensagem de correspondência direta {#direct-mail-test-send}

Saiba como visualizar o arquivo de extração, validar e ativar a campanha ou jornada de correspondência direta e gerenciar o consentimento de correspondência postal no Journey Optimizer.

## Antes de começar {#before-you-start}

Antes de testar e enviar uma mensagem de correspondência direta, [crie a mensagem e configure o arquivo de extração](create-direct-mail.md). Verifique se você também concluiu a [configuração do canal de correspondência direta](direct-mail-configuration.md).

## Visualizar o arquivo de extração {#preview-dm}

Depois que o conteúdo do arquivo de extração for definido, você poderá usar perfis de teste para visualizá-lo. Se você inseriu conteúdo personalizado, é possível verificar como esse conteúdo é exibido na mensagem, usando os dados do perfil de teste.

Para fazer isso, clique em **[!UICONTROL Simular conteúdo]** e adicione um perfil de teste para verificar como é a renderização do arquivo de extração usando os dados do perfil de teste.

![Simular visualização de conteúdo para um arquivo de extração de correspondência direta](assets/direct-mail-simulate.png){width="800" align="center"}

Informações detalhadas sobre como selecionar perfis de teste e pré-visualizar seu conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

Depois que o conteúdo do arquivo estiver pronto para ser enviado, feche a tela de simulação e clique no botão **[!UICONTROL Revisar para ativar]**.

## Validar e ativar a campanha de correspondência direta {#dm-validate}

>[!IMPORTANT]
>
> Se a campanha estiver sujeita a uma política de aprovação, será necessário solicitar aprovação para enviar a campanha de correspondência direta. [Saiba mais](../test-approve/gs-approval.md)

Antes de ativar a campanha de correspondência direta, verifique se a campanha ou jornada e o arquivo de extração estão configurados corretamente. Para fazer isso, verifique os alertas na seção superior do editor. Alguns deles são avisos simples, mas outros podem impedir que você envie a mensagem. Dois tipos de alertas podem ocorrer: avisos e erros.

* **Os avisos** referem-se às recomendações e práticas recomendadas. Por exemplo, uma mensagem de aviso será exibida se a mensagem SMS estiver vazia.

* **Erros** impedem que você publique a campanha, desde que não sejam resolvidos. Por exemplo, uma mensagem de erro avisa quando a linha de assunto está ausente.

![Revisar e ativar tela mostrando alertas de validação da campanha de correspondência direta](assets/direct-mail-review.png){width="800" align="center"}

Quando a campanha de correspondência direta estiver pronta, conclua a configuração da [jornada](../building-journeys/journey-gs.md) ou da [campanha](../campaigns/create-campaign.md) para enviá-la.

>[!NOTE]
>
>O arquivo exportado por padrão termina com uma nova linha. Isso garante a compatibilidade com as ferramentas padrão de processamento de dados.

Depois de enviado, você pode medir o impacto da campanha ou jornada de correspondência direta nos relatórios. Para obter mais informações sobre a geração de relatórios de correspondência direta, consulte estas seções:
* [Relatório de campanha de correspondência direta](../reports/campaign-global-report-cja-direct.md)
* [Relatório de jornada de correspondência direta](../reports/journey-global-report-cja-direct.md)

## Gerenciar o consentimento para correspondência direta {#dm-consent-management}

No [!DNL Journey Optimizer], o consentimento é gerenciado pelo [esquema de consentimento](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=pt-BR){target="_blank"} da Experience Platform. Por padrão, o valor do campo de consentimento fica vazio e é tratado como consentimento para receber suas comunicações.

Se um perfil optou por não receber correspondência direta, nos atributos de perfil correspondentes do Experience Platform, o valor de `consents.marketing.postalMail.val` será `n` e o perfil correspondente será excluído das entregas subsequentes.

Para habilitá-lo novamente, o atributo de perfil deve ser alterado de volta para `consents.marketing.postalMail.val` : `y`.

Para gerenciar os atributos de um perfil, acesse o Experience Platform e o perfil selecionando um namespace de identidade e um valor de identidade correspondente. Saiba mais na [documentação da Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=pt-BR#getting-started){target="_blank"}.

Saiba mais sobre como gerenciar a opção de não participação no Journey Optimizer em [esta seção](../privacy/opt-out.md).

## Tópicos relacionados {#related-topics}

* [Introdução à correspondência direta](get-started-direct-mail.md)
* [Criar uma mensagem de correspondência direta](create-direct-mail.md)
* [Configurar canal de correspondência direta](direct-mail-configuration.md)
* [Pré-visualizar e testar conteúdo](../content-management/preview-test.md)

Para perguntas comuns sobre correspondência direta, consulte [Introdução à correspondência direta](get-started-direct-mail.md).
