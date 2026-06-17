---
solution: Journey Optimizer
product: journey optimizer
title: Correções de marca alimentadas por IA
description: Saiba como configurar e usar correções de marca alimentadas por IA no Adobe Journey Optimizer.
feature: Brand Validation
topic: Content Management
role: User
level: Intermediate
exl-id: dd4fde0e-86c8-4a57-86ba-202e3be2c41f
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 1%

---


# Correções de marca alimentadas por IA {#brand-corrections}

>[!AVAILABILITY]
>
>Esse recurso está disponível para o Adobe Journey Optimizer e se aplica a canais de conteúdo de push, SMS e Web.

## Visão geral {#overview}

Quando o conteúdo é sinalizado durante o controle de qualidade da marca, o Adobe Journey Optimizer pode gerar automaticamente alternativas de texto corrigidas ou aprimoradas usando IA gerativa. Em vez de reescrever manualmente a cópia sinalizada, você recebe sugestões em linha que se alinham às diretrizes da sua marca, as quais podem ser revisadas, visualizadas e aplicadas com um único clique.

Isso transforma a etapa de controle de qualidade da marca de um portal de revisão de bloqueio em uma **experiência de correção por uso**, reduzindo o tempo gasto em correções manuais e acelerando a produção de conteúdo em todos os canais.

Esse recurso foi projetado para profissionais de marketing de conteúdo, redatores e operadores de campanha que precisam manter a conformidade com a marca em campanhas de vários canais e alto volume, sem retardar os fluxos de trabalho de produção.

## Como funciona {#how-it-works}

O controle de qualidade da marca no Adobe Journey Optimizer avalia o conteúdo em relação às diretrizes da marca da sua organização, incluindo tom de voz, terminologia, padrões de mensagem e regras editoriais. Quando um problema de violação ou qualidade é detectado, o sistema sinaliza o elemento de conteúdo afetado e, quando suportado, gera automaticamente uma substituição recomendada usando o mecanismo de IA geradora do Adobe.

O fluxo de ponta a ponta é o seguinte:

1. **Verificação de qualidade da marca** — Quando você executa uma verificação da marca no seu conteúdo (corpo da notificação por push, texto da mensagem SMS ou bloco de conteúdo da Web), o sistema avalia cada elemento em relação às regras da marca ativa.
2. **Detecção de violação** — Os elementos que falharem em um ou mais critérios de marca serão sinalizados com um indicador de gravidade (por exemplo, crítico, aviso ou sugestão).
3. **Geração de sugestão de IA** — Para cada elemento sinalizado, o sistema gera automaticamente uma ou mais alternativas de texto corrigidas. As sugestões são produzidas pelo mecanismo de IA gerativa da Adobe, que está ciente do motivo da violação e do contexto das diretrizes da sua marca.
4. **Visualização em linha** — o texto de substituição sugerido aparece em linha, diretamente ao lado do original sinalizado. Você pode comparar as versões original e sugerida lado a lado antes de fazer qualquer alteração.
5. **Aplicar com um clique** — Se a sugestão atender às suas necessidades, selecione **Aplicar** para substituir o texto sinalizado pela versão gerada pela IA. O editor de conteúdo é atualizado imediatamente e o sinalizador da marca é limpo.
6. **Substituição manual** — Você nunca fica bloqueado para a sugestão de IA. Você pode editar a sugestão antes de aplicá-la, descartá-la e escrever sua própria correção, ou ignorar o sinalizador totalmente se o contexto justificar uma exceção.

>[!NOTE]
>
>As sugestões geradas pela IA são somente recomendações. Sua equipe mantém controle editorial total. Sempre revise as sugestões no contexto de sua campanha antes de aplicá-las.

## Pré-requisitos {#prerequisites}

Antes de usar as correções de marca alimentadas por IA, verifique se as seguintes condições são atendidas:

- **Diretrizes de marca configuradas** — sua organização deve ter pelo menos um perfil de marca ativo configurado no Adobe Journey Optimizer. Os perfis de marca definem as regras com base nas quais o conteúdo é avaliado. Entre em contato com o administrador do Adobe ou gerente de marca para verificar se os perfis de marca foram publicados e associados às sandboxes.
- **Recursos de IA de conteúdo habilitados** — A assistência de conteúdo habilitada por IA deve ser habilitada para sua organização e sandbox. Isso é gerenciado no nível do perfil do produto no Adobe Admin Console. Se as sugestões de IA não forem exibidas após uma verificação da marca, confirme com o administrador que o direito de geração de conteúdo de IA está ativo.
- **Tipo de conteúdo com suporte** — As correções de marca com sugestões de IA são compatíveis com os seguintes tipos de conteúdo: título e corpo da notificação por push, texto da mensagem SMS e blocos de conteúdo da Web editados por meio do Journey Optimizer Web Designer. Os ativos de mídia avançada (imagens, vídeo) são avaliados separadamente quanto à conformidade da marca e não estão no escopo para correções de IA no nível do texto.
- **Permissões de edição** — Você deve ter acesso de edição à jornada, campanha ou modelo de conteúdo no qual reside o conteúdo sinalizado.

## Configurar {#configure}

Nenhuma configuração adicional é necessária para ativar as correções de marca alimentadas por IA se sua organização já usar o controle de qualidade da marca. A camada de sugestão de IA é ativada automaticamente quando violações de marca são detectadas em tipos de conteúdo compatíveis.

Para executar uma verificação de marca e acessar sugestões de IA:

1. Abra a campanha ou jornada no Adobe Journey Optimizer.
2. Navegue até a etapa de conteúdo do canal relevante (Push, SMS ou Web).
3. Selecione **Verificar alinhamento da marca** (ou abra o painel **Controle de qualidade da marca** na barra de ferramentas do editor de conteúdo).
4. Aguarde a verificação ser concluída. Os elementos sinalizados são realçados na tela e listados no painel **Problemas de marca** à direita.
5. Para cada item sinalizado, expanda a linha de ocorrência para visualizar o motivo da violação e a sugestão gerada pela IA.
6. Use a **Visualização** para ver o texto sugerido renderizado na tela de conteúdo.
7. Selecione **Aplicar sugestão** para substituir o texto sinalizado ou **Editar** para modificar a sugestão antes de aplicá-la.
8. Depois que todos os problemas forem resolvidos ou reconhecidos, execute novamente a verificação da marca para confirmar a conformidade.

>[!NOTE]
>
>Aplicar uma sugestão atualiza o conteúdo ao vivo no editor, mas não publica ou ativa a campanha automaticamente. Você deve concluir as etapas restantes de configuração e ativação da campanha como de costume.

### Trabalhar com várias sugestões {#multiple-suggestions}

Para algumas violações, o mecanismo de IA pode gerar mais de uma alternativa. Nesses casos, o painel **Problemas de marca** exibe uma lista numerada de opções. Use as setas para frente e para trás para percorrer as alternativas antes de selecionar aquela que melhor se adapta à sua intenção. Cada alternativa é gerada com uma abordagem estilística diferente — por exemplo, uma pode priorizar a concisão enquanto outra enfatiza o alinhamento do tom.

### Correções em massa {#bulk-corrections}

Se vários elementos no mesmo conteúdo forem sinalizados, você poderá aplicar sugestões individualmente ou usar a ação **Aplicar todas as sugestões** na parte superior do painel **Problemas de marca** para aceitar todas as substituições geradas por IA em uma única etapa. Revise a lista com cuidado antes de usar a aplicação em massa, pois essa ação substitui todo o texto sinalizado simultaneamente.

>[!NOTE]
>
>A aplicação em massa está disponível somente quando todos os itens sinalizados têm uma sugestão de IA associada. Itens sem sugestões disponíveis (por exemplo, sinalizadores de conformidade de imagem) são ignorados e permanecem sinalizados para revisão manual.

## Tópicos relacionados {#related-topics}

- [Visão geral das diretrizes da marca](../content-management/brands.md)
- [Executar uma verificação da marca no seu conteúdo](../content-management/brand-score.md)
- [Assistente de IA para geração de conteúdo](../content-management/gs-generative.md)
- [Criar uma notificação por push](create-push.md)
- [Criar uma mensagem SMS](../sms/create-sms.md)
- [Editar conteúdo da Web com o Journey Optimizer](../web/edit-web-content.md)
