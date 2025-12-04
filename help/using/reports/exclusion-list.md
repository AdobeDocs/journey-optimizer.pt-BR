---
solution: Journey Optimizer
product: journey optimizer
title: Lista de exclusões
description: Saiba mais sobre as exclusões que ocorrem durante o envio
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: ca6f722c93fffe0cebcddb4f730f23d9a720ef9d
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 8%

---

# Motivos de exclusão {#exclusion-list}

## Como as exclusões são contadas nos relatórios do Campaign

Ao exibir relatórios de campanha, observe que a métrica *Exclusões* é calculada da seguinte forma:

**Exclusões = Exclusões Exclusivas + Eventos de Exclusão Duplicados**

Isso significa que se um perfil for excluído várias vezes (por exemplo, devido a vários eventos de exclusão para o mesmo perfil), cada evento será contado no total de Exclusões. Como resultado, a soma de *Entregues* e *Exclusões* pode exceder o tamanho original do público-alvo direcionado. Esse comportamento é esperado e reflete a maneira como os eventos de exclusão são rastreados no sistema.

**Exemplo:**

- Público-alvo: 94.000 perfis
- Entregue: 69.000
- Exclusões: 37.000 (inclui eventos de exclusão duplicados)
- Total (Entregues + Exclusões): 106.000

O total excede o público-alvo direcionado porque os eventos de exclusão duplicados estão incluídos na contagem de Exclusões.

Para obter mais detalhes sobre os motivos específicos de exclusão, consulte a tabela abaixo.

## Lista de motivos de exclusão

| Motivo da exclusão | Código de erro | Canal | Explicação |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Todos os canais | Evento de exclusão genérico para qualquer erro de despacho de Tempo de Execução. |
| RuntimeRenderingError | 050302 | Todos os canais | Evento de exclusão genérico para qualquer erro de renderização de Tempo de Execução. |
| ErroDeNamespaceParaExperimentação | 050017 | Todos os canais | Um evento de exclusão é gerado quando o Namespace no experimento é diferente do namespace do perfil. |
| ExperimentationHoldoutExclusion | 050018 | Todos os canais | Esse evento de exclusão é gerado quando o Tratamento qualificado de um experimento é &quot;Holdout&quot;. |
| ExcludedForControlRules | 050002 | Todos os canais | Esse evento de exclusão é gerado quando a entrega da mensagem atual resulta em violação das regras de controle, por exemplo, o número de emails permitidos em um mês. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Um evento de exclusão é gerado quando a variante de correspondência direta não está definida. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Um evento de exclusão é gerado quando o experimento é habilitado para a mensagem e nenhuma mensagem é encontrada para o tratamento qualificado. |
| EmailSemConsentimento | 050101 | Email | Um evento de exclusão é gerado quando o usuário optou por não receber emails de marketing. |
| Suprimido | 050107 | Email | Exclusão devido a um dos motivos de Supressão. |
| EmailSuprimido | 050102 | Email | Um evento de exclusão é gerado quando o email de destino é suprimido. |
| DomainSuppressed | 050105 | Email | Um evento de exclusão é gerado quando o domínio do email direcionado é suprimido. |
| Não permitido | 050108 | Email | Um evento de exclusão é gerado quando a lista de permissões é ativada e o email direcionado é excluído da lista de permissões. |
| EmailNãoPermitido | 050103 | Email | Um evento de exclusão é gerado quando a lista de permissões é ativada e o email direcionado é excluído da lista de permissões. |
| DomínioNãoPermitido | 050106 | Email | Um evento de exclusão é gerado quando a lista de permissões é ativada e o domínio do email direcionado é excluído da lista de permissões. |
| EmailNoSubscriberIdFoundInProfile | 050025 | Email | Um evento de exclusão é gerado quando o subscriberId não é encontrado no perfil para um email de assinatura. |
| EmailSemEndereçoEncontradoNoPerfil | 050020 | Email | Um evento de exclusão é gerado quando o endereço de email não é encontrado no endereço de execução. |
| EmailSemEndereçoDefinidoNaPredefinição | 050021 | Email | Um evento de exclusão é gerado quando o endereço de execução não é definido na configuração. |
| EmailSemVarianteDefinida | 050026 | Email | Um evento de exclusão é gerado quando nenhuma variante é definida na mensagem de email. |
| EmailNenhumaMensagemEncontradaParaTratamento | 050027 | Email | Um evento de exclusão é gerado quando o experimento é habilitado para a mensagem e nenhuma mensagem é encontrada para o tratamento qualificado. |
| EndereçoMalformadoEmail | 050024 | Email | Um evento de exclusão é gerado quando o email contém um endereço malformado. |
| InAppNoVariantDefined | 050041 | InApp | Um evento de exclusão é gerado quando nenhuma variante é definida para mensagem no aplicativo. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Um evento de exclusão é gerado quando o experimento é habilitado para a mensagem e nenhuma mensagem é encontrada para o tratamento qualificado. |
| PushNoTokenFoundInProfile | 050030 | Push | Um evento de exclusão é gerado quando o perfil não tem tokens de push. |
| PushNoValidTokenFoundForApps | 050031 | Push | Um evento de exclusão é gerado quando nenhum token válido é encontrado para os aplicativos direcionados na configuração. **Importante:** ao usar um certificado de produção, o atributo `pushNotificationDetails.platform` no perfil de usuário deve ser definido como `apns`. Se estiver usando um certificado de sandbox, defina-o como `apnsSandbox`. Uma incompatibilidade entre o atributo de plataforma e o tipo de certificado acionará essa exclusão. |
| PushMalformedProfile | 050034 | Push | Um evento de exclusão é gerado quando pushNotificationDetails no perfil está malformado. |
| PushNoConsent | 050111 | Push | Um evento de exclusão é gerado quando o usuário recusa as notificações por push de marketing. |
| PushNoApplicationDefinedInPreset | 050033 | Push | Um evento de exclusão é gerado quando a configuração não contém nenhum aplicativo para o target. |
| PushNoVariantDefined | 050035 | Push | Um evento de exclusão é gerado quando nenhuma variante é definida. |
| PushNoMessageFoundForTreatment | 050036 | Push | Um evento de exclusão é gerado quando o experimento é habilitado para a mensagem e nenhuma mensagem é encontrada para o tratamento qualificado. |
| SMSNoConsent | 050104 | SMS | Um evento de exclusão é gerado quando o usuário recusa o SMS de marketing. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Um evento de exclusão é gerado quando &quot;FromNumber&quot; não está definido na configuração. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Um evento de exclusão é gerado quando &quot;ToNumber&quot; não está definido na configuração. |
| SMSNoVariantDefined | 050154 | SMS | Um evento de exclusão é gerado quando nenhuma variante é definida. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | Um evento de exclusão é gerado quando o experimento é habilitado para a mensagem e nenhuma mensagem é encontrada para o tratamento qualificado. |
| WebNoVariantDefined | 050041 | Web | Um evento de exclusão é gerado quando nenhuma variante é definida para uma mensagem da Web. |
| WebNenhumaMensagemEncontradaParaTratamento | 050042 | Web | Um evento de exclusão é gerado quando o experimento é habilitado para a mensagem e nenhuma mensagem é encontrada para o tratamento qualificado. |
