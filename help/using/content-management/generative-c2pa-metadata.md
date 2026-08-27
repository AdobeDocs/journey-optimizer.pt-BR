---
solution: Journey Optimizer
product: journey optimizer
title: Metadados C2PA no conteúdo de Geração
description: Saiba como o Adobe Journey Optimizer aplica automaticamente metadados C2PA a imagens geradas ou editadas com o recurso Gerar conteúdo e o que isso significa para o seu conteúdo.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 5a3b83eb2e92263a5fed39b9b3670cf1fb1e15ae
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Metadados C2PA no conteúdo de Geração {#generative-content-credentials}

>[!BEGINSHADEBOX]

**Nesta página:** Saiba quais ações Gerar conteúdo anexam metadados C2PA, o que isso significa para imagens que combinam várias fontes de IA geradoras e o que é transferido quando o conteúdo se move entre aplicativos.

>[!ENDSHADEBOX]

>[!INFO]
>
>Novas leis estão surgindo em torno da transparência generativa da IA, e a Adobe está trabalhando para atender aos requisitos aplicáveis em todas as jurisdições. Os metadados C2PA são a ferramenta de origem que o Adobe usa para atender aos requisitos dessas leis.

Os metadados C2PA são metadados duráveis e invisíveis que registram como um conteúdo foi criado ou editado. Quando você usa a opção Gerar conteúdo no Adobe Journey Optimizer para gerar ou editar uma imagem com ferramentas de IA gerativas, os metadados C2PA são anexados automaticamente a essa imagem, nenhuma ação é necessária da sua parte.

## Ações que anexam metadados C2PA {#cc-workflows}

A tabela a seguir resume quando os metadados C2PA são anexados, com base na ação de imagem executada em Gerar conteúdo.

| Ação | Descrição | Metadados C2PA anexados? | Exemplo de caso de uso |
| --- | --- | --- | --- |
| **Gerar uma imagem** | Criar uma nova imagem a partir de um prompt de texto, de uma imagem de referência ou gerar uma imagem semelhante | Sempre. A imagem é gerada por IA gerativa, de modo que sempre carrega um metadado C2PA novo. | Uma imagem de banner para uma campanha de email é gerada a partir de um prompt de texto que descreve o visual desejado. |
| **Cortar uma imagem** (recorte central ou inteligente) | Ajustar uma imagem às dimensões solicitadas | Somente se a imagem de origem já tiver metadados C2PA. O recorte recria os pixels da imagem, o que normalmente apagaria esses metadados do C2PA. Portanto, o Generate content lê os pixels da imagem de origem antes do recorte e, em seguida, recria e anexa esses metadados ao resultado recortado. O corte em si não adiciona uma nova ação de IA gerativa, ele preserva a existente. | Uma imagem de banner gerada é cortada para caber em uma página da Web: os metadados C2PA são preservados por meio do corte. </br> Uma foto do stock carregada usada como um plano de fundo de notificação por push é cortada para caber na tela: como a foto do stock não carrega nenhuma ação de IA gerativa, nenhum metadado C2PA é criado. |
| **Adicionar uma sobreposição de texto** | Renderizar texto gerado sobre uma imagem de plano de fundo | Somente se a imagem de fundo já tiver metadados C2PA. A renderização da sobreposição produz uma nova imagem do plano de fundo mais o texto, o que normalmente apagaria esses metadados do C2PA. Portanto, o botão Gerar conteúdo lê-lo da imagem do plano de fundo com antecedência, em seguida, reconstrói e reanexa-o ao resultado. A etapa de sobreposição não adiciona uma nova ação de IA gerativa. | Um título promocional é renderizado como uma sobreposição de texto em uma imagem de fundo gerada para uma landing page: os metadados C2PA da imagem de fundo são preservados. |
| **Sobrepor imagens** | Compor duas ou mais imagens | Se qualquer uma das imagens de origem tiver metadados C2PA, a imagem combinada carregará todas elas, mescladas em um único metadado C2PA. A composição produz uma nova imagem das fontes, o que normalmente apagaria esses metadados C2PA. Portanto, o Generate content lê cada um antes da composição e cria um único metadado C2PA combinado listando cada fonte que contribuiu para uma ação de IA geradora. | Uma imagem de produto gerada é composta por um plano de fundo gerado para um cabeçalho de email: o resultado carrega um metadado C2PA que reflete as duas fontes de IA geradoras. <br> Duas fotos de marca carregadas são compostas em uma única colagem: como nenhuma fonte carrega uma ação de IA gerativa, nenhum metadado C2PA é criado. |

## Tipos de conteúdo e seu escopo {#cc-content-types}

* **Imagens**: Cobertas. Os metadados C2PA são anexados quando as imagens são geradas com IA gerativa e preservados por meio de operações de recorte, sobreposição de texto e sobreposição de imagem executadas pela função Gerar conteúdo.
* **Texto**: não aplicável. Saídas somente texto do conteúdo gerado, como geração de cópia, tradução e sugestões de alinhamento de marca, não exigem metadados C2PA.

## O que acontece quando o conteúdo se move {#cc-content-moves}

Os metadados do C2PA viajam com o arquivo de imagem. Quando uma imagem gerada ou editada com IA gerativa é baixada ou exportada do Adobe Journey Optimizer, seus metadados C2PA são preservados. [Saiba mais sobre metadados C2PA](https://helpx.adobe.com/firefly/using/content-credentials.html){target="_blank"}.

Algumas maneiras de trazer imagens para o seu conteúdo, como extrair uma imagem de um PDF ou de uma fonte incorporada (base64), podem não preservar os metadados C2PA originais. Nesses casos, nenhum metadado C2PA pode ser lido da origem, e nenhum é criado para o resultado.

## Recursos adicionais

* [Diretrizes do usuário da IA gerada da Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html?lang=pt-BR){target="_blank"}
* [Medidas de proteção e limitações](gs-generative.md#generative-guardrails)
* [Transparência do conteúdo de IA gerativa](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency#related-links)