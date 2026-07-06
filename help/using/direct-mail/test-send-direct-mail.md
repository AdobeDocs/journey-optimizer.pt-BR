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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 2f3a44b2366119c84e52861db09054f22d55623d
workflow-type: tm+mt
source-wordcount: 829
ht-degree: 11%

---

# Verificação e envio de uma mensagem de correspondência direta {#direct-mail-test-send}

>[!BEGINSHADEBOX]

**Nesta página:** visualize o arquivo de extração, valide e ative sua campanha ou jornada e gerencie o consentimento postal para que a correspondência direta chegue com precisão aos destinatários certos.

>[!ENDSHADEBOX]

Saiba como visualizar o arquivo de extração, validar e ativar a campanha ou jornada de correspondência direta e gerenciar o consentimento de correspondência postal no Journey Optimizer.

## Antes de começar {#before-you-start}

Antes de testar e enviar uma mensagem de correspondência direta, [crie a mensagem e configure o arquivo de extração](create-direct-mail.md). Verifique se você também concluiu a [configuração do canal de correspondência direta](direct-mail-configuration.md).

## Visualizar o arquivo de extração {#preview-dm}

Depois que o conteúdo do arquivo de extração tiver sido definido, visualize-o usando um dos métodos de simulação:

* Clique em **[!UICONTROL Simular conteúdo]** para testar as variações de conteúdo com dados de entrada de exemplo ou geração automática de IA. [Saiba como simular variações de conteúdo](../test-approve/simulate-sample-input.md)
* Clique em **[!UICONTROL Simular conteúdo]**, selecione **[!UICONTROL Simular conteúdo (perfis do AEP)]** na lista suspensa e adicione um perfil de teste para verificar como o arquivo de extração é renderizado.

Informações detalhadas sobre como visualizar e testar o conteúdo estão disponíveis na seção [Gerenciamento de conteúdo](../content-management/preview-test.md).

![Simular visualização de conteúdo para um arquivo de extração de correspondência direta](assets/direct-mail-simulate.png){width="800" align="center"}

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

## Entender o tempo de exportação e a geração de arquivos {#dm-export-timing}

Exportações de correspondência direta são executadas em ciclos UTC fixos de 4 horas em **02:01**, **06:01**, **10:01**, **14:01**, **18:01** e **22:01**.

Os perfis são incluídos no ciclo de exportação *próximo* depois que atingem a atividade de correspondência direta. Isso significa que a criação do arquivo se baseia em quando os perfis chegam ao nó Correspondência direta, não quando a campanha ou jornada foi ativada pela primeira vez.

* **Por que você pode receber vários arquivos em um dia** - Se os perfis atingirem a atividade de correspondência direta em janelas de 4 horas diferentes, o Journey Optimizer gerará arquivos de exportação separados para cada janela. Esse é o comportamento esperado.

  Por exemplo:

   * Os perfis que chegam antes de **14:01** são exportados em **14:01**.
   * Os perfis que chegam de **14:02** a **18:01** são exportados em **18:01**.

  Isso não duplica perfis, pois os agrupa por janela de chegada.

* **Tempo de atividade de Atualização do Perfil** - No jornada, a atividade **[!UICONTROL Atualizar perfil]** é executada imediatamente no tempo de execução da jornada quando um perfil atinge essa atividade. Ele não espera pelo ciclo de exportação de correspondência direta.

* **Recomendações para cenários de um arquivo por dia** - Se você precisar de um arquivo por dia, considere as seguintes opções:

   * **Frequência de roteamento de 24 horas**: garante um arquivo por dia, mas introduz a latência de entrega.
   * **Aguardar até a hora do dia**: pode alinhar perfis na mesma janela de exportação, mas os resultados dependem do tempo da jornada.
   * **Frequência de roteamento de 4 horas**: fornece a latência mais baixa, mas pode gerar vários arquivos por dia.

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
