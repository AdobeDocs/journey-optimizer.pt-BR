---
solution: Journey Optimizer
product: journey optimizer
title: Content Credentials no assistente de IA
description: Saiba como o Adobe Journey Optimizer aplica automaticamente o Content Credentials a imagens geradas ou editadas com o AI Assistant e o que isso significa para o seu conteúdo.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: 556502a5c45ad920827785a9950bc5f7bbc4ca8f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Content Credentials no assistente de IA {#generative-content-credentials}

>[!BEGINSHADEBOX]

**Nesta página:** saiba quais ações do Assistente de IA anexam o Content Credentials, o que isso significa para imagens que combinam várias fontes de IA geradoras e o que é transferido quando o conteúdo é transferido entre aplicativos.

>[!ENDSHADEBOX]

>[!INFO]
>
>Novas leis estão surgindo em torno da transparência generativa da IA, e a Adobe está trabalhando para atender aos requisitos aplicáveis em todas as jurisdições. Content Credentials são a ferramenta de origem que o Adobe usa para atender aos requisitos dessas leis.

Content Credentials são metadados invisíveis e duráveis que registram como um conteúdo foi criado ou editado. Quando você usa o Assistente de IA no Adobe Journey Optimizer para gerar ou editar uma imagem com ferramentas de IA gerativas, o Content Credentials é anexado automaticamente a essa imagem. Nenhuma ação é necessária da sua parte.

## Ações que anexam o Content Credentials {#cc-workflows}

A tabela a seguir resume quando as Content Credentials são anexadas, com base na ação de imagem executada no Assistente de IA.

| Ação | Descrição | Content Credentials conectado? | Exemplo de caso de uso |
| --- | --- | --- | --- |
| **Gerar uma imagem** | Criar uma nova imagem a partir de um prompt de texto, de uma imagem de referência ou gerar uma imagem semelhante | Sempre. A imagem é gerada por IA gerativa, de modo que sempre carrega um Content Credential novo. | Uma imagem de banner para uma campanha de email é gerada a partir de um prompt de texto que descreve o visual desejado. |
| **Cortar uma imagem** (recorte central ou inteligente) | Ajustar uma imagem às dimensões solicitadas | Somente se a imagem de origem já tiver uma Content Credential. O corte recria os pixels da imagem, o que normalmente apagaria essa Content Credential. Assim, o Assistente de IA lê os pixels da imagem de origem antes de cortar e, em seguida, recria e anexa novamente ao resultado cortado. O corte em si não adiciona uma nova ação de IA gerativa, ele preserva a existente. | Uma imagem de banner gerada é cortada para se ajustar a uma página da Web: a Content Credential é preservada durante o recorte. </br> Uma foto do stock carregada usada como um plano de fundo de notificação por push é cortada para caber na tela: como a foto do stock não carrega nenhuma ação de IA geradora, nenhum Content Credential é criado. |
| **Adicionar uma sobreposição de texto** | Renderizar texto gerado sobre uma imagem de plano de fundo | Somente se a imagem de fundo já tiver uma Content Credential. A renderização da sobreposição produz uma nova imagem do plano de fundo mais o texto, o que normalmente apagaria essa Content Credential. Portanto, o AI Assistant a lê da imagem do plano de fundo com antecedência e, em seguida, a reconstrói e a anexa ao resultado. A etapa de sobreposição não adiciona uma nova ação de IA gerativa. | Um título promocional é renderizado como uma sobreposição de texto em uma imagem de fundo gerada para uma página de aterrissagem: a Content Credential da imagem de fundo é preservada. |
| **Sobrepor imagens** | Compor duas ou mais imagens | Se qualquer uma das imagens de origem tiver uma Content Credential, a imagem combinada carregará todas elas, mescladas em uma única Content Credential. A composição produz uma nova imagem das fontes, o que normalmente apagaria essas Content Credentials. Portanto, o Assistente de IA lê cada uma antes da composição e cria uma única Content Credential combinada listando cada fonte que contribuiu para uma ação de IA geradora. | Uma imagem de produto gerada é composta por um plano de fundo gerado para um cabeçalho de email: o resultado carrega um Content Credential que reflete as duas fontes de IA geradoras. <br> Duas fotos de marca carregadas são compostas em uma única colagem: como nenhuma fonte carrega uma ação gerativa de IA, nenhum Content Credential é criado. |

## Tipos de conteúdo e seu escopo {#cc-content-types}

* **Imagens**: Cobertas. Os Content Credentials são anexados quando as imagens são geradas com IA gerativa e preservadas por meio de operações de recorte, sobreposição de texto e sobreposição de imagem realizadas pelo Assistente de IA.
* **Texto**: não aplicável. Saídas somente texto do Assistente de IA, como geração de cópia, tradução e sugestões de alinhamento de marca, não exigem o Content Credentials.

## O que acontece quando o conteúdo se move {#cc-content-moves}

O Content Credentials viaja com o arquivo de imagem. Quando uma imagem gerada ou editada com IA gerativa é baixada ou exportada do Adobe Journey Optimizer, sua Content Credentials é preservada. [Saiba mais sobre o Content Credentials](https://helpx.adobe.com/firefly/using/content-credentials.html){target="_blank"}.

Algumas maneiras de trazer imagens para o seu conteúdo, como extrair uma imagem de um PDF ou de uma fonte incorporada (base64), podem não preservar o Content Credential original. Nesses casos, nenhuma Content Credential pode ser lida a partir da origem e nenhuma é criada para o resultado.

## Recursos adicionais

* [Adobe Content Credentials](https://helpx.adobe.com/firefly/using/content-credentials.html){target="_blank"}: saiba mais sobre como o Content Credentials funciona em produtos Adobe.
* [Diretrizes do usuário da IA gerada da Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html?lang=pt-BR){target="_blank"}
* [Medidas de proteção e limitações](gs-generative.md#generative-guardrails)
