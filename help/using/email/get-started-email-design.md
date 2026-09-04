---
solution: Journey Optimizer
product: journey optimizer
title: Design de emails
description: Saiba como criar o design dos emails
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: email, design, Stock, Assets
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
TQID: https://experienceleague.adobe.com/fyUHQD4jpIUI2KdyrGbgktEhNNc4OWYRJ8AkgZhrIoQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: f550d0f2-143d-4093-9463-467fbec95fcc
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 6edb8a6f2724d2776dc595b48332e064eb04e2a0
workflow-type: tm+mt
source-wordcount: 1325
ht-degree: 100%

---

# Introdução ao design de email {#get-started-content-design}

>[!BEGINSHADEBOX]

**Nesta página:** saiba como projetar seu conteúdo de email no Designer de email, as principais etapas para criá-lo do zero, codificar ou importar o HTML e as práticas recomendadas que mantêm seus emails renderizados entre clientes.

>[!ENDSHADEBOX]

Para acessar o Designer de email e começar a criar o conteúdo do email, primeiro [crie um email](create-email.md) em uma jornada ou campanha.

É possível então usar os **recursos de design de email** do [!DNL Journey Optimizer] para importar conteúdo existente ou começar a criar emails responsivos do zero. [Saiba mais](content-from-scratch.md)

O Designer de email também permite:

* Aproveitar o **Adobe Experience Manager Assets Essentials** para enriquecer seus emails e criar e gerenciar seu próprio banco de dados de ativos. [Saiba mais](../integrations/assets.md)

* Encontrar **fotos do Adobe Stock** para criar seu conteúdo e melhorar o design de emails. [Saiba mais](../integrations/stock.md)

* Melhore a experiência dos clientes criando mensagens personalizadas e dinâmicas com base em seus atributos de perfil. Saiba mais sobre [personalização](../personalization/personalize.md) e [conteúdo dinâmico](../personalization/get-started-dynamic-content.md).

➡️ [Conheça este recurso no vídeo](#video)

## Etapas principais para criar conteúdo de email {#key-steps}

Após criar um email, é possível começar a projetar o conteúdo de email.

1. Na tela de configuração da jornada ou campanha, vá até a tela **[!UICONTROL Editar conteúdo]** para acessar o Designer de email. [Saiba mais](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. Na página inicial do Designer de email, escolha uma das seguintes opções para criar o design do email:

   * **Projete seu email do zero** através da interface do Designer de email e aproveite as imagens do [Adobe Experience Manager Assets](../integrations/assets.md). Saiba como criar o design do conteúdo de email [nesta seção](content-from-scratch.md).

   * **Codifique ou cole um HTML bruto** diretamente no Designer de email. Saiba como codificar seu próprio conteúdo [nesta seção](code-content.md).

     >[!NOTE]
     >
     >Em uma campanha, você também pode selecionar o botão **[!UICONTROL Editor de código]** da tela **[!UICONTROL Editar conteúdo]**. [Saiba mais](create-email.md#define-email-content)

   * **Importar conteúdo HTML existente** de um arquivo ou uma pasta .zip. Saiba como importar um conteúdo de email [nesta seção](existing-content.md).

   * **Converter designs de imagem em modelos HTML** usando o conversor de imagem para HTML viabilizado por IA. Saiba como transformar imagens estáticas em modelos de email editáveis [nesta seção](../content-management/image-to-html.md).

   * **Selecionar um conteúdo existente** de uma lista de modelos integrados ou personalizados. Saiba como trabalhar com modelos de email [nesta seção](../email/use-email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Depois que o conteúdo de email é definido e personalizado, você pode verificar seu conteúdo de email com as **verificações automatizadas de conteúdo** para capturar problemas de HTML e CSS — como tags não compatíveis, divs vazias e violações de limite de tamanho — diretamente no painel de criação, antes de enviar. [Saiba mais](content-check.md)

   >[!NOTE]
   >
   >O sistema também verifica configurações importantes durante o processo de criação e exibe alertas para avisos (recomendações e práticas recomendadas) e erros (problemas impeditivos que inviabilizam testes ou a ativação). [Saiba mais sobre alertas por email](create-email.md#check-email-alerts)

   ![Painel de verificação de conteúdo no Designer de email com problemas](assets/content-check.png)

1. Você também pode validar a qualidade do conteúdo para identificar possíveis problemas de legibilidade, coesão do conteúdo e eficácia. [Saiba mais sobre validação da qualidade do conteúdo](../content-management/brands-score.md#validate-quality)

   ![](../content-management/assets/brand-score-7.png)

1. Finalmente, você pode exportar seu conteúdo para validação ou uso posterior. Clique em **[!UICONTROL Exportar HTML]** para salvar em seu computador um arquivo zip que contém o HTML e os ativos.

   ![](assets/email_designer_export.png)

## Práticas recomendadas de design de email {#best-practices}

Ao enviar emails, é importante levar em consideração que os destinatários podem encaminhá-los, o que às vezes pode causar problemas na renderização do email. Isso acontece especialmente ao usar classes CSS que podem não ser compatíveis com o provedor de email usado para encaminhamento. Por exemplo, se estiver usando a classe CSS “is-desktop-hidden” para ocultar uma imagem em dispositivos móveis.

Para minimizar esses problemas de renderização, é recomendado manter a estrutura do design de emails o mais simples possível. Tente usar um único design que funcione bem tanto para desktops quanto para dispositivos móveis e evite usar classes CSS complexas ou outros elementos de design que possam não ser totalmente compatíveis com todos os clientes de email.

>[!NOTE]
>
>O mesmo se aplica quando os emails são abertos no Gmail ou no Outlook por meio de um navegador móvel da Web, em que o tratamento de CSS difere significativamente dos aplicativos nativos — layouts simples baseados em tabela com estilos totalmente incorporados são a escolha mais segura. [Saiba mais](#mobile-web-limitations)

Ao seguir essas práticas recomendadas, você ajuda a garantir que seus emails sejam renderizados corretamente de forma consistente, independentemente de como sejam visualizados ou encaminhados pelos destinatários.

Consulte na tabela abaixo as práticas recomendadas de design de emails:

| Recomendado | Use com cuidado | Não recomendado |
|-|-|-|
| <ul><li><b>Layouts estáticos baseados em tabela</b> para a estrutura</li> <li><b>Tabelas em HTML e tabelas aninhadas</b> para consistência do layout</li> <li><b>Larguras do modelo</b> entre 600 px e 800 px </li> <li><b>CSS simples e em linha</b> para o estilo </li> <li><b>Fontes seguras para a web</b> para compatibilidade universal</li> | <ul><li><b>Imagens de fundo</b> podem não aparecer em certas plataformas de email.</li><li><b>Fontes da web personalizadas</b> não têm compatibilidade universal.</li><li><b>Layouts largos</b> podem ser exibidos incorretamente em telas menores.</li><li>Os <b>mapas de imagem</b> oferecem funcionalidade limitada.</li><li>O <b>CSS incorporado</b> às vezes é removido durante a entrega do email.</li> | <ul><li>Geralmente, o <b>JavaScript</b> não é compatível com ambientes de email.</li> <li> Tags <b>`<iframe>`</b> estão bloqueadas na maioria das plataformas. </li> <li>O <b>Flash</b> está obsoleto e não é mais compatível.</li> <li><b>Áudios integrados</b> muitas vezes não podem ser reproduzidos.</li> <li><b>Vídeos integrados</b> são incompatíveis com várias plataformas de email.</li> <li> <b>Formulários</b> não funcionam nos emails.</li> <li> A disposição em camadas de `<div>` pode causar problemas de renderização.</li> |

>[!NOTE]
>
>A [Lei Europeia de Acessibilidade](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} declara que todas as comunicações digitais devem ser acessíveis. Além das práticas recomendadas de design de email listadas nesta seção, certifique-se de seguir também as diretrizes listadas [nesta página](accessible-content.md) que são específicas para criar conteúdo acessível com o Designer de email.

## Medidas de proteção e limitações específicas {#email-guardrails}

Mesmo emails bem estruturados podem ser renderizados de forma diferente dependendo do cliente ou do ambiente em que são abertos. As seções abaixo documentam as limitações conhecidas e os comportamentos específicos do cliente que devem ser considerados ao criar seus emails.

### Limitações do navegador web para dispositivos móveis {#mobile-web-limitations}

A renderização de email pode ser diferente quando os destinatários abrem o Gmail ou o Outlook **por meio de um navegador da web móvel** (por exemplo, Chrome em um telefone), em vez de usar um aplicativo móvel nativo ou cliente de desktop. Essa é uma limitação conhecida dos ambientes de webmail móvel e não é específica do Journey Optimizer.

Essa diferença de renderização vem de como os clientes de webmail se comportam dentro de um navegador móvel. O navegador renderiza a interface do webmail de desktop completa primeiro, colocando o email em duas camadas, além do alcance de qualquer CSS responsivo ou consulta de mídia. O Gmail Web também desmonta blocos CSS `<style>` e envolve conteúdo de email em seu próprio `<div>`, o que pode substituir seus estilos e criar conflitos de alinhamento.

Os sintomas típicos incluem deslocamento de alinhamento de texto (texto alinhado à esquerda que aparece centralizado), linhas separadoras brancas extras entre seções de conteúdo e um layout geral que difere do design do modelo.

Esses problemas só ocorrem no Gmail Web e no Outlook Web quando acessados por um navegador móvel. Os aplicativos móveis nativos do Outlook e do Gmail, bem como todos os clientes de desktop, não são afetados.

>[!TIP]
>
>Para minimizar o impacto:
>
>* Use layouts simples baseados em tabela com CSS totalmente incorporado.
>
>* Evite depender de consultas de mídia ou blocos `<style>` para propriedades críticas de layout, como alinhamento de texto.

### Considerações de renderização do Outlook {#outlook-tips}

O Outlook apresenta várias peculiaridades de renderização que podem afetar o layout do email se não forem levadas em conta durante o design. Para ajudar a garantir que seus emails sejam renderizados corretamente no Outlook, siga estas práticas recomendadas:

* Use números pares para preenchimento, tamanhos de fonte e larguras. O Outlook converte pixels em pontos internamente, o que pode introduzir espaçamento desigual e linhas brancas indesejadas quando números ímpares são usados.
* Defina as larguras da tabela em pixels, não em porcentagens. Larguras baseadas em porcentagem podem quebrar o layout no Outlook. Aplique valores de largura diretamente no atributo de estilo de cada tabela.
* Sempre defina larguras de imagem usando o atributo `width`. O Outlook ignora as propriedades de CSS `width` e `height` nas imagens e retorna às dimensões nativas do arquivo se nenhum atributo HTML estiver presente.
* Incluir texto alternativo em todas as imagens. Isso evita problemas de exibição e segurança quando imagens são bloqueadas.
* Aplique bordas às células da tabela, não ao próprio elemento da tabela. Se uma borda não estiver renderizando como esperado, mova-a de `<table>` para `<td>`.
* Evite cantos arredondados. O CSS `border-radius` não tem suporte confiável no Outlook: cantos quadrados são o padrão seguro.

Para considerações sobre design no modo escuro, incluindo como usar consultas de mídia e técnicas de troca de imagem específicas do Outlook.com, consulte [esta página](dark-mode.md).

## Vídeos tutoriais {#video}

Saiba como criar conteúdo de email com o editor de mensagens.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)

Saiba como configurar experimentos de conteúdo para testes A/B e explorar o conteúdo de email que melhor impulsiona seus objetivos de negócios.

>[!VIDEO](https://video.tv.adobe.com/v/3419893)

{{$include /help/_includes/do-not-localize/email/ai-augmented-get-started-email-design.md}}
