---
solution: Journey Optimizer
product: journey optimizer
title: Referência de códigos de erro
description: Saiba mais sobre códigos de erro comuns no Adobe Journey Optimizer e como solucioná-los
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: error, codes, troubleshooting, jornada, campaign, messages (erro, códigos, solução de problemas, , campanha, mensagens)
source-git-commit: 584d860d0908f354389037be860757dabe1c1e3f
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 1%

---


# Referência de códigos de erro {#error-codes}

O Adobe Journey Optimizer usa códigos de erro padronizados para ajudar você a identificar e resolver problemas rapidamente em jornadas, campanhas e configurações de mensagens. A compreensão desses códigos de erro pode reduzir bastante o tempo de solução de problemas e ajudar você a manter o desempenho ideal da campanha.

## Noções básicas sobre a estrutura do código de erro {#error-code-structure}

Os códigos de erro do Adobe Journey Optimizer seguem um padrão de nomenclatura consistente que ajuda a identificar o componente e o tipo de problema:

* **Prefixo do serviço**: indica qual serviço Adobe Journey Optimizer gerou o erro (por exemplo, CJMPTS para Serviço de Envio/Transporte, CJMRT para Tempo de Execução de Jornada, CJMAS para Serviço de Criação de Mensagens)
* **Número do erro**: identificador exclusivo para a condição de erro específica
* **Código de status HTTP**: código de status HTTP padrão (por exemplo, 400, 403, 422, 500)

Exemplo: `CJMRT-030012-422` indica um erro de Tempo de Execução de Jornada (CJMRT) com o número de erro 030012 e o status HTTP 422 (Entidade Não Processável).

## Onde encontrar códigos de erro {#find-error-codes}

Os códigos de erro aparecem em vários locais no Adobe Journey Optimizer:

* Relatórios e logs de execução de Jornada
* Telas de ativação de campanha
* Avisos de validação de mensagem
* Notificações e alertas do sistema
* Respostas da API (ao usar APIs REST)

Quando ocorrer um erro, anote o código de erro completo e a ID da solicitação que o acompanha, pois eles são essenciais para a solução de problemas e o encaminhamento de suporte.

## Códigos de erro comuns por serviço {#error-codes-by-service}

### CJMPTS: erros do serviço de push e transporte {#cjmpts-errors}

Esses erros ocorrem durante as operações de entrega de notificação por push e transporte de mensagem.

| Código de erro | Descrição | Causa raiz | Resolução |
|------------|-------------|-----------|-----------|
| **CJMPTS-1510-500** | Erro interno do servidor no envio por canal de push | Mau funcionamento de push/transporte de back-end; erro de infraestrutura ou provedor | &#x200B;1. Verifique as configurações de provisionamento do canal<br/>2. Verifique se as credenciais de push são válidas<br/>3. Repita a operação<br/>4. Se for persistente, entre em contato com o Suporte da Adobe com a ID da solicitação <br/><br/>**Documentação relacionada**: [Configuração de push](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Erro interno do servidor durante envio/processo de push (gateways de terceiros) | Mau funcionamento temporário da nuvem ou erro de serviço desconhecido | &#x200B;1. Verifique a configuração de provedor/canal<br/>2. Verifique o status do gateway de terceiros<br/>3. Tente novamente após alguns minutos<br/>4. Examinar logs para contexto adicional <br/><br/>**Documentação relacionada**: [Notificações por push](../push/create-push.md) |
| **CJMPTS-1310-500** | Erro interno do serviço de renderização (pré-visualização ou envio ao vivo) | Falha no renderizador do modelo downstream, geralmente devido a problemas de sintaxe de JSON/modelo | &#x200B;1. Valide a sintaxe e a estrutura do modelo<br/>2. Verifique se todas as variáveis de personalização são válidas<br/>3. Use uma carga de teste para identificar o problema<br/>4. Simplifique a complexidade do modelo, se necessário <br/><br/>**Documentação relacionada**: [Modelos de mensagem](../content-management/content-templates.md), [Sintaxe do Personalization](../personalization/personalization-syntax.md) |

### CJMRT: erros de API e Tempo de execução de Jornada {#cjmrt-errors}

Esses erros ocorrem durante a execução da jornada, o processamento de eventos e as operações da API.

| Código de erro | Descrição | Causa raiz | Resolução |
|------------|-------------|-----------|-----------|
| **CJMRT-030012-422** | Entidade não processável - ação com falha, evento inválido ou carga inválida | Dados de entrada inválidos (por exemplo, público-alvo, evento ou atributo não existente) | &#x200B;1. Verifique novamente a estrutura de carga de entrada/evento<br/>2. Verifique se os objetos referenciados (públicos, conjuntos de dados) existem e estão ativos<br/>3. Validar se todos os campos obrigatórios estão presentes<br/>4. Teste com uma carga em boas condições <br/><br/>**Documentação relacionada**: [Solução de problemas de Jornada](troubleshooting.md), [Configuração de eventos](../event/about-events.md) |
| **CJMRT-130004-400** | Solicitação inválida - entrada malformada no nó do jornada ou na configuração do canal | Jornada referências de carga ou configuração removidas/recurso inválido | &#x200B;1. Revise a configuração do nó de jornada<br/>2. Verifique se todos os recursos referenciados (mensagens, públicos, ações) existem<br/>3. Corrigir ou atualizar referências corrompidas<br/>4. Recrie a configuração da jornada, se necessário <br/><br/>**Documentação relacionada**: [Criação de Jornadas](journey-gs.md), [Ações personalizadas](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Conflito - o recurso já existe | Tentativa de criar recurso com ID ou nome duplicado | &#x200B;1. Use IDs e nomes exclusivos para todos os recursos<br/>2. Verificar recursos existentes com o mesmo identificador<br/>3. Excluir ou renomear objetos conflitantes<br/>4. Revisar convenções de nomenclatura <br/><br/>**Documentação relacionada**: [versões de Jornada](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | Solicitação inválida durante a configuração/visualização do jornada | A carga não tem a dependência necessária ou o link de modelo foi corrompido | &#x200B;1. Verifique se todos os recursos necessários estão ativos<br/>2. Verifique se os modelos e blocos de conteúdo foram publicados<br/>3. Verifique se todas as dependências estão vinculadas corretamente<br/>4. Revise os resultados do modo de teste de jornada <br/><br/>**Documentação relacionada**: [Testando jornadas](testing-the-journey.md), [Dependências de Jornada](journey-gs.md) |
| **CJMRT-080608-400** | Solicitação inválida no domínio/canal/delegação | Registros DNS necessários ou configuração de email/SMS ausente | &#x200B;1. Configuração de DNS concluída para domínios de email<br/>2. Verifique se a delegação de subdomínio foi concluída<br/>3. Execute os assistentes de configuração novamente<br/>4. Tempo de permissão para propagação DNS (até 72 horas)<br/><br/>**Documentação relacionada**: [Superfícies de canal](../configuration/channel-surfaces.md), [Delegação de subdomínio](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Erro interno na carga útil | Dados de back-end/erro de configuração ou configuração não compatível | &#x200B;1. Repita a operação<br/>2. Simplifique a configuração se estiver usando recursos avançados<br/>3. Escalonar para o Suporte da Adobe com ID de solicitação e carga exata<br/>4. Verifique problemas conhecidos nas notas de versão <br/><br/>**Documentação relacionada**: [Solução de problemas de Jornada](troubleshooting.md) |

### CJMAS: Erros do serviço de autoria de mensagens {#cjmmas-errors}

Esses erros ocorrem ao criar, editar ou publicar mensagens, predefinições e conteúdo.

| Código de erro | Descrição | Causa raiz | Resolução |
|------------|-------------|-----------|-----------|
| **CJMAS-1149-400** | Solicitação inválida ao salvar mensagem, predefinição ou variante | Campos obrigatórios ausentes na mensagem ou configuração incorreta | &#x200B;1. Preencha todos os campos obrigatórios (marcados com asterisco)<br/>2. Validar configuração de mensagem/predefinição<br/>3. Verificar formatos e restrições de valor de campo<br/>4. Examine as mensagens de validação na interface <br/><br/>**Documentação relacionada**: [Canal de email](../email/get-started-email.md), [Superfícies de canal](../configuration/channel-surfaces.md) |
| **CJMAS-2073-422** | Entidade não processável na edição de predefinição de mensagem | Erro de validação, campo incompatível ou sintaxe incorreta | &#x200B;1. Corrija os erros de sintaxe/campo conforme indicado<br/>2. Compare com uma configuração em boas condições<br/>3. Use a validação da interface de mensagem antes de salvar<br/>4. Examine os requisitos de campo na documentação <br/><br/>**Documentação relacionada**: [Predefinições de mensagem](../configuration/channel-surfaces.md), [Configurações de email](../email/email-settings.md) |
| **CJMAS-1300-500** | Erro interno da criação de mensagens | Falha no back-end devido a problemas de infraestrutura, grande conteúdo ou tempo de inatividade do serviço | &#x200B;1. Simplifique o modelo/conteúdo (reduza o tamanho/a complexidade)<br/>2. Repita a operação<br/>3. Salve o trabalho incrementalmente<br/>4. Se for persistente, encaminhe para o Suporte da Adobe <br/><br/>**Documentação relacionada**: [Modelos de conteúdo](../content-management/content-templates.md) |
| **CJMAS-2001-200** | Status bem-sucedido, mas banner de erro: link para opção de não participação ausente | Link de cancelamento de inscrição obrigatório ausente na variante de email | &#x200B;1. Adicione o link para opção de não participação/cancelamento de inscrição a todas as variantes de email<br/>2. Verifique se o link está presente em cada versão de idioma<br/>3. Use o auxiliar de personalização para inserir o link para opção de não participação<br/>4. Teste todas as variantes antes de publicar <br/><br/>**Documentação relacionada**: [Gerenciamento de recusa](../privacy/opt-out.md), [Design de email](../email/content-from-scratch.md) |
| **CJMAS-1603-403** | Proibido ao atualizar/publicar modelo ou predefinição | O usuário não tem a permissão/função necessária ou a ação não é permitida no estado atual | &#x200B;1. Verifique se o usuário tem as permissões apropriadas (Gerenciador de mensagens, Autor etc.)<br/>2. Verificar status de predefinição/modelo (rascunho, publicado, arquivado)<br/>3. Solicite acesso ao administrador, se necessário<br/>4. Revisar atribuições de perfil de produto <br/><br/>**Documentação relacionada**: [Permissões](../administration/permissions.md), [Controle de acesso](../administration/permissions-overview.md) |

### CJMCMP: Erros de campanha {#cjmcmp-errors}

Esses erros ocorrem durante a criação, configuração e ativação da campanha.

| Código de erro | Descrição | Causa raiz | Resolução |
|------------|-------------|-----------|-----------|
| **CJMCMP-2050-400** | Solicitação inválida na ativação ou aprovação da campanha | A campanha faz referência a uma política ou segmento inválido/ausente | &#x200B;1. Auditoria de todas as configurações de nó da campanha<br/>2. Verifique se os links de política/segmento são atuais e válidos<br/>3. Atualize com a configuração correta<br/>4. Testar novamente a campanha antes da ativação <br/><br/>**Documentação relacionada**: [Criação de campanha](../campaigns/create-campaign.md), [Aprovação de campanha](../test-approve/gs-approval.md) |

## Abordagem geral de solução de problemas {#troubleshooting-approach}

Ao encontrar um código de erro, siga esta abordagem sistemática:

1. **Identificar o erro**: observe o código de erro completo, o status HTTP e qualquer mensagem ou ID de solicitação que o acompanhe.

2. **Localizar o serviço**: use o prefixo do serviço (CJMPTS, CJMRT, CJMMAS, CJMCMP) para identificar qual componente é afetado.

3. **Verificar o código de status**:
   * **400 (Solicitação inválida)**: revisar dados e configuração de entrada
   * **403 (Proibido)**: verificar permissões e direitos de acesso
   * **409 (Conflito)**: procurar recursos duplicados ou conflitantes
   * **422 (Entidade Não Processável)**: Validar dados em relação aos requisitos do esquema
   * **500 (Erro Interno do Servidor)**: tentar novamente e escalonar para suporte

4. **Revisar alterações recentes**: considere o que foi modificado recentemente (atualizações de jornada, novas campanhas, alterações de configuração etc.).

5. **Consultar documentação**: use os links fornecidos neste guia para acessar a documentação detalhada do recurso afetado.

6. **Repetir quando apropriado**: para erros de 500 séries, uma simples tentativa após alguns minutos geralmente resolve problemas transitórios.

7. **Escalonar quando necessário**: se o erro persistir após as seguintes etapas de resolução, contate o Suporte da Adobe com:
   * Código de erro completo
   * ID da solicitação (se disponível)
   * Etapas a serem reproduzidas
   * Detalhes de configuração relevantes

## Práticas recomendadas para evitar erros comuns {#best-practices}

### Antes da ativação do jornada {#journey-best-practices}

* **Validar todos os recursos**: verifique se todos os públicos referenciados, fontes de dados e ações personalizadas estão ativos
* **Testar completamente**: use o modo de teste para identificar problemas antes de publicar ([Saiba mais](testing-the-journey.md))
* **Verificar permissões**: verifique se você tem os direitos de acesso necessários para todos os componentes
* **Revisar dependências**: verifique se todas as mensagens e conteúdos vinculados foram publicados

### Ao criar mensagens {#message-best-practices}

* **Preencha os campos obrigatórios**: sempre preencha todos os campos obrigatórios antes de salvar
* **Incluir links para opção de não participação**: adicionar links para cancelar inscrição a todas as variantes de email ([Saiba mais](../privacy/opt-out.md))
* **Validar personalização**: testar todo o conteúdo dinâmico com perfis de exemplo ([Saiba mais](../personalization/personalization-build-expressions.md))
* **Manter modelos gerenciáveis**: evite modelos excessivamente complexos que podem causar problemas de renderização

### Para gerenciamento de campanhas {#campaign-best-practices}

* **Verificar dados de público-alvo**: verifique se os públicos-alvo estão configurados e preenchidos corretamente
* **Verificar status da aprovação**: compreenda os requisitos de aprovação antes de tentar ativar ([Saiba mais](../test-approve/gs-approval.md))
* **Monitorar configurações**: revise regularmente as superfícies e predefinições de canais em busca de validade
* **Planejar alterações de DNS**: permitir tempo suficiente para propagação de DNS ao atualizar domínios

## Recursos adicionais {#additional-resources}

* [Solução de problemas do Jornada](troubleshooting.md)
* [Solução de problemas de execução](troubleshooting-execution.md)
* [Solução de problemas de atividades de entrada](troubleshooting-inbound.md)
* [Solução de problemas de ações personalizadas](../action/troubleshoot-custom-action.md)
* [Jornada perguntas frequentes](journey-faq.md)
* [Proteções e limitações](../start/guardrails.md)

## Obter suporte {#getting-support}

Se você encontrar erros persistentes que não podem ser resolvidos usando este guia:

1. **Coletar informações**: coletar o código de erro, a ID da solicitação, os carimbos de data/hora e as etapas para reproduzir
2. **Verificar o status do sistema**: Visite [Status do Adobe](https://status.adobe.com/){target="_blank"} para conhecer problemas de serviço
3. **Pesquisar documentação**: consulte a [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=pt-BR){target="_blank"} para obter soluções
4. **Engajar a comunidade**: postar perguntas na [Comunidade do Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=pt){target="_blank"}
5. **Contate o Suporte da Adobe**: envie um tíquete de suporte com todos os detalhes relevantes

>[!NOTE]
>
>Esta referência de código de erro é atualizada continuamente à medida que novos códigos são identificados e documentados. Para obter as informações mais atuais, verifique os [blogs da Adobe Journey Optimizer Community](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs?profile.language=pt){target="_blank"} regularmente.

**Tópicos relacionados**

* [Códigos de erro de Adobe Journey Optimizer desmistificados: Parte 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884?profile.language=pt){target="_blank"}
* [Códigos de erro de Adobe Journey Optimizer desmistificados: Parte 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661?profile.language=pt){target="_blank"}

