---
solution: Journey Optimizer
product: journey optimizer
title: Converter imagens em modelos do HTML com o Acelerador de modelo
description: Saiba como usar o Acelerador de modelo habilitado por IA para converter designs de imagem em modelos de email editáveis do HTML
feature: Email Design
topic: Content Management
role: User
level: Beginner
keywords: email, modelo, imagem, HTML, IA, design, accelerator
hide: true
hidefromtoc: true
source-git-commit: ddbab603e4ac612a49a3853fcac428950def1d98
workflow-type: tm+mt
source-wordcount: '1563'
ht-degree: 3%

---

# Converter imagens em modelos do HTML com o Acelerador de modelo {#image-to-html}

>[!CONTEXTUALHELP]
>id="ajo_template_accelerator"
>title="Acelerador de modelo"
>abstract="Use o Acelerador de modelo para converter designs de imagem estática (JPEG ou PNG) em modelos de email do HTML totalmente personalizáveis. Esse recurso alimentado por IA ajuda a transformar rapidamente designs visuais em conteúdo de email responsivo e editável. Observação: todo o conteúdo existente em seu email será excluído quando você fizer upload de uma imagem para conversão."

>[!AVAILABILITY]
>
>Este recurso é oferecido com disponibilidade limitada. Entre em contato com o representante da Adobe para obter acesso.

## Visão geral {#overview}

O Acelerador de Modelos é um recurso inovador alimentado por IA, disponível no menu **Modelos de conteúdo**, que acelera consideravelmente a criação de emails, convertendo designs de imagens estáticas em modelos de conteúdo de email do HTML totalmente personalizáveis. Essa ferramenta permite que os profissionais de marketing transformem designs visuais de designers gráficos ou ferramentas de design em modelos de email responsivos e editáveis que podem ser salvos na biblioteca Modelos de conteúdo e reutilizados em várias jornadas e campanhas.

Ao utilizar a tecnologia de IA gerativa, o Acelerador de modelo analisa o layout, a tipografia, as cores e os elementos visuais da imagem e gera um código HTML limpo e estruturado que mantém a fidelidade do design e, ao mesmo tempo, garante total capacidade de edição e compatibilidade com o Designer de email.

**Principais benefícios:**

* **Criação acelerada**: reduza o tempo de criação de email convertendo instantaneamente modelos de design em modelos de conteúdo reutilizáveis
* **Designer-developer bridge**: elimine a necessidade de codificação manual do HTML ao trabalhar com designs visuais
* **Fidelidade de design**: mantenha a integridade do design original ao criar conteúdo editável
* **Reusabilidade**: salvar modelos na biblioteca de Modelos de Conteúdo para uso em várias jornadas e campanhas
* **Compatibilidade de email**: gerar HTML que funcione perfeitamente com o Designer de email e entre clientes de email

## Pré-requisitos {#prerequisites}

Antes de usar o Acelerador de Modelo, verifique se você tem:

* Acesso ao Adobe Journey Optimizer com o Designer de email
* Um arquivo de imagem no formato JPEG ou PNG contendo seu design de email
* Acesso de disponibilidade limitada ao recurso Acelerador de modelo (entre em contato com o representante da Adobe)

>[!NOTE]
>
>Para obter melhores resultados, use imagens de alta qualidade com elementos visuais claros e texto legível. Idealmente, as imagens devem ter entre 600 e 800 pixels de largura para corresponder às dimensões de email padrão.

## Conversão de uma imagem em um modelo HTML {#convert-image}

Para converter um design de imagem em um modelo de email do HTML totalmente personalizável, siga estas etapas:

1. Acesse a lista Modelos de conteúdo selecionando **[!UICONTROL Gerenciamento de conteúdo]** > **[!UICONTROL Modelos de conteúdo]** no menu esquerdo.

1. Clique em **[!UICONTROL Criar modelo]**.

1. Preencha os detalhes do modelo e selecione **[!UICONTROL Email]** como canal.

1. Clique em **[!UICONTROL Criar]** para acessar o Designer de email.

1. Na página inicial do Designer de Email, selecione **[!UICONTROL Importar HTML]**.

   ![](assets/import-html_2.png)

1. Na caixa de diálogo de importação, você verá a seção **[!UICONTROL Converter imagem em HTML]**.

   >[!CAUTION]
   >
   >Ao carregar uma imagem para conversão, **todo o conteúdo adicionado ao email será excluído e substituído** pelo modelo gerado. Se você tiver conteúdo existente em seu email, salve-o antes de prosseguir com a conversão da imagem.

1. Clique no botão **[!UICONTROL Carregar imagem]** para selecionar seu arquivo de imagem.

1. Arraste e solte o arquivo de imagem (JPEG ou PNG) ou clique em para procurar e selecionar o arquivo de imagem.

1. Clique em **[!UICONTROL Gerar]** para iniciar o processo de conversão baseado em IA.

   >[!NOTE]
   >
   >O processo de geração pode levar até 5 minutos, dependendo da complexidade e do tamanho do design de imagem. Seja paciente enquanto a IA analisa e converte sua imagem.

1. Quando a conversão for concluída, seu modelo de conteúdo será salvo automaticamente como rascunho. Em seguida, você pode revisar e editar o modelo HTML gerado na tela Designer de email.

1. O modelo convertido é aberto no Designer de email com recursos de edição completos. Agora você pode:

   * Editar conteúdo de texto e aplicar personalização
   * Modificar imagens e adicionar links
   * Ajustar cores, fontes e estilo
   * Adicionar, remover ou reorganizar componentes de conteúdo
   * Aproveite todos os recursos do Email Designer como com qualquer outro modelo

   ![](assets/email_designer_structure_components.png)

1. Faça os ajustes necessários para refinar o modelo e corresponder às diretrizes da marca.

1. Depois de satisfeito com o modelo, clique em **[!UICONTROL Salvar]** para salvar o modelo de conteúdo.

1. Seu template agora está disponível na biblioteca de Modelos de conteúdo e pode ser usado ao criar emails em jornadas ou campanhas. [Saiba como usar modelos de conteúdo](use-email-templates.md)

## Usar seu modelo convertido em emails {#use-template}

Depois de criar e salvar o modelo de conteúdo usando o Acelerador de modelo, você pode usá-lo ao criar emails em jornadas ou campanhas:

1. Ao criar um email em uma jornada ou campanha, acesse o Designer de email na tela **[!UICONTROL Editar conteúdo]**.

1. Na página inicial do Designer de email, vá para a guia **[!UICONTROL Modelos salvos]**.

1. Selecione o modelo gerado pelo Acelerador de Modelo na lista.

1. Clique em **[!UICONTROL Usar este modelo]** para aplicá-lo ao seu email.

1. Continue editando e personalizando seu conteúdo de email conforme necessário.

Saiba mais sobre [como trabalhar com modelos de email](use-email-templates.md) e [como criar modelos de conteúdo](../content-management/content-templates.md).

## Práticas recomendadas {#best-practices}

Para obter ótimos resultados ao usar o Acelerador de modelo, siga estas recomendações:

**Antes de começar**

* **Salvar conteúdo existente**: a conversão de uma imagem em HTML substituirá todo o conteúdo existente no seu email. Sempre salve o trabalho atual antes de usar este recurso.
* **Planeje seu fluxo de trabalho**: use o Acelerador de Modelo no início do processo de criação de email ou verifique se você está pronto para substituir todo o conteúdo atual.

**Preparação da imagem**

* **Solução**: use imagens de alta resolução (no mínimo 1200px de largura) para melhor reconhecimento de texto e detecção de elementos
* **Clareza**: verifique se o texto é claramente legível e se os elementos visuais estão bem definidos
* **Largura**: crie imagens nas larguras de email padrão (600-800px) para corresponder aos requisitos típicos do cliente de email
* **Formato de arquivo**: usar o formato JPEG ou PNG - evitar imagens compactadas ou de baixa qualidade
* **Design completo**: incluir o design de email completo em uma única imagem, do cabeçalho ao rodapé

**Considerações sobre o design**

* **Layouts simples**: layouts mais simples e bem estruturados são convertidos com maior precisão do que designs altamente complexos
* **Elementos padrão**: usar padrões comuns de design de email (cabeçalho, seções de corpo, CTAs, rodapé)
* **Legibilidade do texto**: garanta contraste suficiente entre o texto e os planos de fundo
* **Fontes seguras para a Web**: os designs que usam fontes comuns seguras para a Web terão melhor fidelidade
* **Evitar elementos sobrepostos**: mantenha os elementos de design claramente separados para obter um melhor reconhecimento de estrutura

**Após a conversão**

* **Analisar rascunho**: depois que a conversão for concluída, o modelo será salvo automaticamente como rascunho. Reserve tempo para analisar cuidadosamente a precisão do HTML gerado
* **Testar completamente**: testar o email em diferentes clientes e dispositivos de email
* **Refinar manualmente**: faça os ajustes necessários usando os recursos de edição completos do Designer de email
* **Alinhamento da marca**: verifique se as cores, fontes e estilos correspondem às diretrizes da sua marca
* **Personalization**: adicionar conteúdo dinâmico e tokens de personalização conforme necessário
* **Acessibilidade**: revisar e aprimorar recursos de acessibilidade, se necessário

## Limitações e considerações {#limitations}

Esteja ciente das seguintes limitações ao usar o Acelerador de modelo:

* **Interpretação de IA**: a IA gera o HTML com base na interpretação visual da sua imagem. Designs complexos ou incomuns podem exigir ajustes manuais após a conversão.

* **Precisão do texto**: enquanto a IA tenta reconhecer e reproduzir o texto com precisão, sempre verifique o conteúdo do texto e faça as correções necessárias.

* **Conteúdo dinâmico**: o processo de conversão cria um HTML estático com base na sua imagem. Você precisará adicionar personalização, conteúdo dinâmico e rastreamento manualmente após a conversão.

* **Layouts complexos**: projetos altamente complexos com camadas complexas, formas incomuns ou elementos não padrão podem não ser perfeitamente convertidos. Designs mais simples geralmente produzem melhores resultados.

* **Tempo de processamento**: o processo de conversão pode levar até 5 minutos, dependendo da complexidade e do tamanho da sua imagem. O modelo é salvo automaticamente como rascunho após a conclusão da conversão.

* **Disponibilidade Limitada**: como um recurso de Disponibilidade Limitada, o Acelerador de Modelo está sendo aprimorado continuamente. A funcionalidade e a precisão podem variar, e seus comentários ajudam a aprimorar o recurso.

>[!NOTE]
>
>O Acelerador de modelo foi projetado para fornecer um ponto de partida sólido para a criação de emails. O HTML gerado deve ser revisado e refinado usando o Designer de email para garantir que ele atenda aos seus requisitos exatos.

## Perguntas frequentes {#faq}

+++O que acontece com meu conteúdo de email existente quando uso o Acelerador de modelo?

Todo o conteúdo existente no seu email será excluído e substituído pelo modelo recém-gerado ao fazer upload de uma imagem para conversão. Salve qualquer conteúdo importante antes de usar este recurso. É melhor usar o Acelerador de modelo no início do processo de criação de email.

+++

+++Quais formatos de arquivo são compatíveis?

O Acelerador de modelo suporta os formatos de imagem JPEG (.jpg, .jpeg) e PNG (.png).

+++

+++Quanto tempo leva o processo de conversão?

A conversão pode levar até 5 minutos, dependendo da complexidade e do tamanho do design de imagem. Quando a conversão estiver concluída, o arquivo será salvo automaticamente como rascunho para que você o revise e edite.

+++

+++Posso editar o modelo gerado?

Sim! O modelo de HTML gerado é aberto no Designer de email com recursos de edição completos. É possível modificar todos os aspectos do modelo, incluindo texto, imagens, estilo, layout e estrutura.

+++

+++O que acontece se a conversão não corresponder exatamente ao meu design?

A IA faz o melhor para interpretar com precisão o design, mas pode ser necessário refinar manualmente. Use o Designer de email para ajustar todos os elementos que precisam de ajuste.

+++

+++Posso usar esse recurso para páginas de aterrissagem ou outros tipos de conteúdo?

O Acelerador de modelos foi criado especificamente para modelos de email. Para outros tipos de conteúdo, use as opções padrão de design e importação disponíveis no Designer de email.

+++

+++Preciso de permissões especiais para usar este recurso?

O Acelerador de Modelo está disponível com disponibilidade limitada. Você precisa de acesso de Disponibilidade limitada (entre em contato com o representante da Adobe para obter acesso) e de permissões padrão de Designer de email para usar esse recurso.

+++

+++Posso reutilizar modelos convertidos em várias campanhas?

Sim! Os modelos criados com o Acelerador de Modelo são salvos automaticamente na biblioteca de Modelos de conteúdo. Você pode acessá-los e reutilizá-los em qualquer email nas suas jornadas e campanhas. [Saiba mais](../content-management/content-templates.md)

+++

## Tópicos relacionados {#related-topics}

* [Introdução aos modelos de conteúdo](../content-management/content-templates.md)
* [Criar modelos de conteúdo](../content-management/create-content-templates.md)
* [Usar modelos de email](use-email-templates.md)
* [Introdução ao design de email](get-started-email-design.md)
* [Importar o conteúdo do email](existing-content.md)
* [Crie um conteúdo do zero](content-from-scratch.md)

