---
solution: Journey Optimizer
product: journey optimizer
title: Correções de marca alimentadas por IA
description: Saiba como configurar e usar correções de marca alimentadas por IA no Adobe Journey Optimizer.
feature: Brand Guidelines
topic: Content Management
role: User
level: Intermediate
exl-id: a872a3a4-f05b-439d-923e-5191b6e06d34
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 3%

---


# Correções de marca e sugestões editoriais alimentadas por IA {#brand-corrections-ai}

>[!AVAILABILITY]
>
>Esse recurso está disponível para usuários do Adobe Journey Optimizer com as Diretrizes de marca ativas e os direitos do Assistente de IA. Entre em contato com seu representante da Adobe para obter detalhes de acesso.

## Visão geral {#overview}

O Adobe Journey Optimizer estende sua ferramenta de conformidade de marca alimentada pela GenAI em todos os canais de conteúdo compatíveis: SMS, notificações por push, conteúdo da Web e email. Quando o mecanismo de controle de qualidade da marca detecta conteúdo que viola as diretrizes da marca ou falha nos critérios de qualidade editorial, o sistema gera automaticamente alternativas corrigidas que você pode revisar e aplicar diretamente no fluxo de trabalho de criação.

Isso transforma a validação da marca de uma lista de verificação passiva em uma experiência ativa do tipo &quot;corrigir conforme você vai&quot;. Em vez de identificar violações e retornar ao editor para resolver cada problema manualmente, os autores de conteúdo recebem sugestões direcionadas geradas por IA que se alinham às diretrizes de estilo, tom e voz da marca estabelecidas pela organização — tudo sem sair do editor de conteúdo.

Esse recurso foi projetado para profissionais de marketing de conteúdo, redatores e operadores de campanha que precisam mover o conteúdo do rascunho para a ativação rapidamente e, ao mesmo tempo, manter a conformidade da marca em escala.

## Pré-requisitos {#prerequisites}

Antes de usar as correções de marca alimentadas por IA, confirme o seguinte:

- **Diretrizes de marca** estão configuradas no Adobe Journey Optimizer. Sem um perfil de marca ativo, o sistema não pode gerar sugestões de correção alinhadas à marca.
- O recurso **Assistente de IA** está habilitado para a sua organização da Adobe Experience Cloud.
- Você tem as permissões apropriadas para criar e editar conteúdo para o canal relevante (SMS, push, Web ou email).
- Pelo menos um item de conteúdo está disponível para revisão no editor de conteúdo do Journey Optimizer.

>[!NOTE]
>
>As sugestões de correção de marca são geradas usando a infraestrutura de IA gerativa da Adobe e estão sujeitas às políticas de uso do Assistente de IA aplicáveis à sua organização. Sempre revise as sugestões aceitas antes de publicar.

## Como funciona {#how-it-works}

As correções de marca se integram diretamente no fluxo de validação de controle de qualidade da marca no editor de conteúdo do Journey Optimizer. O processo completo funciona da seguinte maneira:

**Etapa 1 — Verificação de controle de qualidade da marca**: quando você executa uma verificação de validação de marca em seu conteúdo — manualmente no painel de revisão ou acionada por uma regra de fluxo de trabalho — o sistema avalia cada bloco de conteúdo em relação às diretrizes de marca configuradas. As verificações abrangem tom de voz, terminologia, idioma proibido, padrões editoriais e requisitos regulatórios.

**Etapa 2 — Detecção e sinalização de violação**: qualquer segmento de conteúdo que não atenda aos critérios de qualidade editorial ou de marca será sinalizado com um indicador de violação. O tipo de violação — por exemplo, incompatibilidade de tom, uso de termo proibido ou não conformidade de diretriz — é exibido ao lado do segmento sinalizado para que os autores entendam exatamente o que precisa ser alterado.

**Etapa 3 — Geração de sugestão de IA**: para cada segmento sinalizado, o Journey Optimizer gera automaticamente uma ou mais alternativas corrigidas usando o Assistente de IA. As sugestões são baseadas nas diretrizes de marca ativas, garantindo que o texto recomendado reflita a voz, a terminologia e o estilo editorial corretos, específicos para sua organização.

**Etapa 4 — visualização e revisão em linha**: as correções sugeridas aparecem em linha, adjacentes ao conteúdo sinalizado no painel lateral de QA da marca. Você pode comparar o texto original com a alternativa gerada pela IA sem sair do editor.

**Etapa 5 — Aceitar ou descartar**: aceite uma sugestão com um único clique para substituir o conteúdo sinalizado pela versão corrigida. Como alternativa, descarte a sugestão e edite o conteúdo manualmente. Aceitar uma sugestão atualiza imediatamente o bloco de conteúdo e marca a violação como resolvida no painel de controle de qualidade.

**Etapa 6 — Revalidação**: após aplicar as correções, execute novamente a verificação de controle de qualidade da marca para confirmar se todas as violações foram resolvidas antes de publicar ou ativar o conteúdo em uma jornada ou campanha.

## Configurar {#configure}

Nenhuma configuração adicional é necessária além dos pré-requisitos padrão. O recurso é ativado automaticamente no painel Controle de qualidade da marca quando um perfil de marca é associado ao seu conteúdo e o Assistente de IA é ativado para sua organização.

Para começar a usar as correções de marca alimentadas por IA:

1. Abra o editor de conteúdo para o canal relevante — SMS, notificação por push, Web ou email.
2. Na barra de ferramentas do editor, selecione **Diretrizes da marca** e escolha o perfil da marca aplicável no menu suspenso.
3. Rascunhe ou abra o conteúdo e selecione **Controle de qualidade da marca** no painel de revisão para iniciar uma verificação.
4. Revise as violações sinalizadas no painel lateral **Controle de qualidade da marca**. Para cada item sinalizado, uma sugestão gerada por IA é exibida automaticamente.
5. Clique em **Aplicar** para aceitar uma sugestão ou **Ignorar** para tratar a correção manualmente.
6. Execute novamente o **Controle de qualidade da marca** para verificar se todas as violações foram resolvidas e, em seguida, prossiga com sua aprovação padrão ou fluxo de trabalho de ativação.

### Canais compatíveis {#supported-channels}

As correções de marca alimentadas por IA estão disponíveis nos seguintes tipos de conteúdo no Adobe Journey Optimizer:

| Canal | Elementos de conteúdo compatíveis |
|---|---|
| **Email** | Linha de assunto, pré-cabeçalho, texto do corpo, rótulos CTA |
| **SMS** | Corpo da mensagem |
| **Notificações por push** | Título, corpo de texto |
| **Web** | Título, cópia do corpo, rótulos de botão |

>[!NOTE]
>
>Os elementos de conteúdo suportados podem variar dependendo da configuração do canal e das diretrizes de marca definidas no perfil da marca. A validação de ativos visuais e de imagens não está no escopo para correções de texto geradas por IA.

## Principais benefícios {#key-benefits}

**Esforço de edição manual reduzido**: os autores de conteúdo não precisam mais fazer referência cruzada das diretrizes da marca manualmente para cada problema sinalizado. As sugestões de IA surgem como alternativas prontas para serem aplicadas, reduzindo drasticamente o tempo gasto no ciclo de correção.

**Conformidade consistente com a marca**: as correções são baseadas nas mesmas diretrizes de marca usadas para validação. As sugestões aceitas mantêm a consistência com a voz da marca aprovada e os padrões editoriais em todos os canais, reduzindo o risco de mensagens inconsistentes em campanhas multicanais.

**Produção de conteúdo mais rápida**: ao transformar o controle de qualidade da marca em um fluxo de trabalho simplificado, as equipes movem o conteúdo pelo ciclo de revisão mais rapidamente, reduzindo o tempo de conclusão entre o rascunho e a ativação. Os operadores de campanha podem resolver um conjunto inteiro de violações em uma única passagem sem alternar entre ferramentas.

**Cobertura entre canais**: ao produzir uma campanha SMS, uma sequência de push para dispositivos móveis ou uma mensagem no aplicativo da Web, as sugestões de correção da marca estarão disponíveis de forma consistente em todas as superfícies de conteúdo com suporte, garantindo que os padrões da marca sejam mantidos em todos os lugares em que a sua marca se comunicar.

## Tópicos relacionados {#related-topics}

- [Introdução às diretrizes de marca](../content-management/brands.md)
- [Usar o Assistente de IA para geração de conteúdo](../content-management/ai-assistant.md)
- [Criar uma mensagem SMS](../sms/create-sms.md)
- [Criar uma notificação por push](../push/create-push.md)
- [Introdução ao canal da web](../web/get-started-web.md)
- [Visualizar e testar o conteúdo](../content-management/preview-test.md)
