---
solution: Journey Optimizer
product: journey optimizer
title: Converter imagens em modelos HTML
description: Saiba como usar o conversor de imagem alimentada por IA para HTML para converter designs de imagem em modelos de email editáveis do HTML
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
badge: label="Disponibilidade limitada" type="Informative"
keywords: email, modelo, imagem, HTML, AI, design, conversor
exl-id: d13467b7-2f3c-4707-a7e0-9b46cb6cafb1
source-git-commit: e5b02fe84f00dec189d4002280e9a69b782cd91f
workflow-type: tm+mt
source-wordcount: '1659'
ht-degree: 4%

---

# Converter imagens em modelos HTML {#image-to-html}

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

O [!DNL Journey Optimizer] ajuda você a acelerar bastante a criação de emails, convertendo designs de imagens estáticas em modelos de conteúdo de email modulares e totalmente personalizáveis do HTML.

Ao utilizar a tecnologia de IA gerativa, uma ferramenta integrada analisa o layout, a tipografia, as cores e os elementos visuais da imagem e gera um código de HTML limpo e modular que mantém a fidelidade do design e, ao mesmo tempo, garante total capacidade de edição com o [Designer de email](../email/get-started-email-design.md).

Esse recurso sem código permite que os profissionais de marketing transformem ativos visuais de designers gráficos ou ferramentas de design em modelos de email responsivos e editáveis que podem ser salvos e reutilizados em várias jornadas e campanhas, sem a necessidade de conhecimento técnico.

Os principais benefícios são os seguintes:

* **Mais rápido que a codificação manual** - O conversor transforma imagens em HTML editável em minutos, para que você possa pular o fluxo de trabalho manual demorado de modelagem para HTML.
* **Nenhuma habilidade técnica necessária** - Os profissionais de marketing podem produzir e ajustar modelos sem suporte a design ou desenvolvimento.
* **Reutilizável em campanhas** - Salve modelos na biblioteca e use-os em qualquer jornada ou campanha.
* **Permanece fiel ao design** - A saída corresponde ao seu layout e estilo, sendo totalmente compatível com o Designer de email.

<!--* **Design fidelity**: Maintain visual consistency with your original design while creating fully editable content
* **Email compatibility**: Generate HTML that works seamlessly with the Email Designer and across email clients-->

+++ Casos de uso comuns

O conversor de imagem para HTML é ideal para:

* **Migração de plataforma**: migrando de outra plataforma de marketing por email? Converta seus designs de email existentes em modelos do HTML prontos para [!DNL Journey Optimizer] sem recriar do zero.
* **Conversão do modelo de design**: transforme modelos de design de ferramentas como o Photoshop, o Figma ou outro software de design em modelos de email funcionais.
* **Criação rápida de modelo**: gere modelos de email rapidamente para campanhas sensíveis ao tempo sem esperar pelos recursos do desenvolvedor.
* **Criando bibliotecas de modelos**: crie uma biblioteca abrangente de modelos consistentes com a marca que os membros da equipe não técnica possam personalizar e implantar.
* **Redução das dependências técnicas**: permitir que os profissionais de marketing criem e repitam modelos de email de maneira independente, acelerando a execução da campanha.

+++

## Medidas de proteção e recomendações {#limitations}

Esteja ciente das seguintes limitações ao converter imagens em modelos de conteúdo do HTML.

* **Interpretação de IA**: a IA gera o HTML com base na interpretação visual da sua imagem. Designs complexos ou incomuns podem exigir ajustes manuais após a conversão.

* **Precisão do texto**: enquanto a IA tenta reconhecer e reproduzir o texto com precisão, sempre verifique o conteúdo do texto e faça as correções necessárias.

* **Conteúdo dinâmico**: o processo de conversão cria um HTML estático com base na sua imagem. Você precisará adicionar personalização, conteúdo dinâmico e rastreamento manualmente após a conversão.

* **Layouts complexos**: projetos altamente complexos com camadas complexas, formas incomuns ou elementos não padrão podem não ser perfeitamente convertidos. Designs mais simples geralmente produzem melhores resultados.

* **Tempo de processamento**: o processo de conversão pode levar até 5 minutos, dependendo da complexidade e do tamanho da sua imagem. O processamento da IA acontece em segundo plano, permitindo que você trabalhe em outras tarefas sem manter a tela aberta. O modelo é salvo automaticamente como rascunho após a conclusão da conversão.

* **Disponibilidade limitada**: como um recurso de Disponibilidade limitada, a imagem para o conversor HTML está sendo aprimorada continuamente. A funcionalidade e a precisão podem variar, e seus comentários ajudam a aprimorar o recurso.

>[!NOTE]
>
>O conversor de imagem para HTML foi projetado para fornecer um forte ponto de partida para a criação de emails. O HTML gerado deve ser revisado e refinado usando o Designer de email para garantir que ele atenda aos seus requisitos exatos.

## Conversão de uma imagem em um modelo do HTML {#convert-image}

Para converter um design de imagem em um modelo de email do HTML totalmente personalizável, siga as etapas abaixo.

1. Verifique se você tem um arquivo de imagem no formato JPEG ou PNG contendo seu design de email.

   >[!NOTE]
   >
   >Para obter melhores resultados, use imagens de alta qualidade com elementos visuais claros e texto legível. Idealmente, as imagens devem ter entre 600 e 800 pixels de largura para corresponder às dimensões de email padrão.

1. Acesse a lista de modelos de conteúdo selecionando **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** no menu esquerdo.

1. Clique em **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do modelo, selecione **[!UICONTROL Email]** como canal e clique em **[!UICONTROL Criar]**.

1. Na seção **[!UICONTROL Converter imagem em modelo]**, execute as seguintes etapas:

   * (Opcional) Se sua organização tiver temas de marca definidos no Journey Optimizer, você poderá selecionar um tema como entrada para que o HTML gerado seja estilizado de acordo com os parâmetros do tema da marca. [Saiba mais sobre temas](../email/apply-email-themes.md)

     Estilos como cor de fundo, cor do botão, fontes, espaçamento entre linhas, margens e preenchimento serão aplicados ao modelo gerado, reduzindo o trabalho adicional de design e produzindo um modelo pronto para uso com edições mínimas.

   * Para fazer upload de uma imagem, verifique se ela não contém informações de identificação pessoal (PII) ou outros dados confidenciais e marque a opção correspondente para confirmar que você analisou o arquivo.

   * Clique no botão **[!UICONTROL Carregar imagem]** para selecionar seu arquivo de imagem.

     ![](../email/assets/email_designer_convert_img.png)

     >[!CAUTION]
     >
     >Ao fazer upload de uma imagem para conversão, todo o conteúdo adicionado no momento no email será excluído e substituído pelo modelo gerado.


1. Depois de selecionar a imagem, clique em **[!UICONTROL Abrir]** para iniciar o processo de conversão baseado em IA.

   >[!NOTE]
   >
   >O processo de geração pode levar até 5 minutos, dependendo da complexidade e do tamanho do design de imagem. Você pode sair desta tela e trabalhar em outras tarefas enquanto a conversão está em andamento.

1. Quando a conversão for concluída, seu modelo de conteúdo será salvo automaticamente como rascunho.

   ![](../email/assets/email_designer_converted_img.png)

1. Clique em **[!UICONTROL Editar corpo do email]**. O modelo convertido abre na [Designer de email](../email/get-started-email-design.md) com recursos de edição completos. Agora você pode:

   * Revisar, editar conteúdo de texto e aplicar personalização
   * Modificar imagens e adicionar links
   * Ajustar cores, fontes e estilo
   * Adicionar, remover ou reorganizar componentes de conteúdo
   * Aproveite todos os recursos do Email Designer como com qualquer outro modelo

   ![](../email/assets/email_designer_html_components.png)

1. Faça os ajustes necessários para refinar o modelo e corresponder às diretrizes da marca.

1. Depois de satisfeito com seu modelo, clique em **[!UICONTROL Salvar]**.

Seu template agora está disponível na biblioteca de template de conteúdo e pode ser usado ao criar emails em jornadas ou campanhas. [Saiba como usar modelos de conteúdo](../email/use-email-templates.md)

## Práticas recomendadas {#best-practices}

Para alcançar os melhores resultados ao converter imagens em modelos de conteúdo do HTML, siga estas recomendações.

+++Antes de começar

* **Salvar conteúdo existente**: a conversão de uma imagem em HTML substituirá todo o conteúdo existente no seu email. Sempre salve o trabalho atual antes de usar este recurso.
* **Planeje seu fluxo de trabalho**: use o conversor de imagem para HTML no início do processo de criação de email ou verifique se você está pronto para substituir todo o conteúdo atual.

+++

+++Preparação da imagem

* **Solução**: use imagens de alta resolução (no mínimo 1200px de largura) para melhor reconhecimento de texto e detecção de elementos
* **Clareza**: verifique se o texto é claramente legível e se os elementos visuais estão bem definidos
* **Largura**: crie imagens nas larguras de email padrão (600-800px) para corresponder aos requisitos típicos do cliente de email
* **Formato de arquivo**: usar o formato JPEG ou PNG - evitar imagens compactadas ou de baixa qualidade
* **Design completo**: incluir o design de email completo em uma única imagem, do cabeçalho ao rodapé

+++

+++Considerações de design

* **Layouts simples**: layouts mais simples e bem estruturados são convertidos com maior precisão do que designs altamente complexos
* **Elementos padrão**: usar padrões comuns de design de email (cabeçalho, seções de corpo, CTAs, rodapé)
* **Legibilidade do texto**: garanta contraste suficiente entre o texto e os planos de fundo
* **Fontes seguras para a Web**: os designs que usam fontes comuns seguras para a Web terão melhor fidelidade
* **Evitar elementos sobrepostos**: mantenha os elementos de design claramente separados para obter um melhor reconhecimento de estrutura

+++

+++Após a conversão

* **Analisar rascunho**: depois que a conversão for concluída, o modelo será salvo automaticamente como rascunho. Reserve tempo para analisar cuidadosamente a precisão do HTML gerado
* **Testar completamente**: testar o email em diferentes clientes e dispositivos de email
* **Refinar manualmente**: faça os ajustes necessários usando os recursos de edição completos do Designer de email
* **Alinhamento da marca**: verifique se as cores, fontes e estilos correspondem às diretrizes da sua marca
* **Personalization**: adicionar conteúdo dinâmico e tokens de personalização conforme necessário
* **Acessibilidade**: revisar e aprimorar recursos de acessibilidade, se necessário

+++

## Perguntas frequentes {#faq}

+++O que acontece com meu conteúdo de email existente quando uso o conversor de imagem para HTML?

Todo o conteúdo existente no seu email será excluído e substituído pelo modelo recém-gerado ao fazer upload de uma imagem para conversão. Salve qualquer conteúdo importante antes de usar este recurso. É melhor usar o conversor de imagem para HTML no início do processo de criação de email.

+++

+++Quais formatos de arquivo são compatíveis?

O conversor de imagem para HTML é compatível com os formatos de imagem JPEG (.jpg, .jpeg) e PNG (.png).

+++

+++Quanto tempo leva o processo de conversão?

A conversão pode levar até 5 minutos, dependendo da complexidade e do tamanho do design de imagem. O processamento da IA acontece em segundo plano, para que você possa sair e trabalhar em outras tarefas; não é necessário manter a tela aberta. Quando a conversão estiver concluída, o arquivo será salvo automaticamente como rascunho para que você o revise e edite.

+++

+++Posso editar o modelo gerado?

Sim! O modelo de HTML gerado é aberto no Designer de email com recursos de edição completos. É possível modificar todos os aspectos do modelo, incluindo texto, imagens, estilo, layout e estrutura.

+++

+++O que acontece se a conversão não corresponder exatamente ao meu design?

A IA faz o melhor para interpretar com precisão o design, mas pode ser necessário refinar manualmente. Use o Designer de email para ajustar todos os elementos que precisam de ajuste.

+++

+++Posso usar esse recurso para páginas de aterrissagem ou outros tipos de conteúdo?

Atualmente, o conversor de imagem para HTML é projetado especificamente para modelos de email. Para outros tipos de conteúdo, use as opções padrão de design e importação disponíveis no Designer de email.

+++

+++Preciso de permissões especiais para usar este recurso?

A imagem para o conversor HTML está disponível com disponibilidade limitada. Você precisa de acesso de Disponibilidade limitada (entre em contato com o representante da Adobe para obter acesso) e de permissões padrão de Designer de email para usar esse recurso.

+++

+++Posso reutilizar modelos convertidos em várias campanhas?

Sim! Os modelos criados com o conversor de imagem para HTML são salvos automaticamente na biblioteca de Modelos de conteúdo. Você pode acessá-los e reutilizá-los em qualquer email nas suas jornadas e campanhas. [Saiba mais](content-templates.md)

+++

+++Posso usar isso para migração de plataforma?

Sim! O conversor de imagem para HTML é ideal para migrar de outras plataformas de marketing por email. Basta exportar ou capturar a tela de seus designs de email existentes da plataforma anterior e convertê-los em modelos do HTML prontos para AJO sem precisar recriá-los do zero.

+++

## Tópicos relacionados {#related-topics}

* [Introdução aos modelos de conteúdo](content-templates.md)
* [Criar modelos de conteúdo](create-content-templates.md)
* [Usar modelos de email](../email/use-email-templates.md)
* [Utilizar temas de email](../email/apply-email-themes.md)
* [Introdução ao design de email](../email/get-started-email-design.md)
* [Importar o conteúdo do email](../email/existing-content.md)
* [Crie um conteúdo do zero](../email/content-from-scratch.md)
