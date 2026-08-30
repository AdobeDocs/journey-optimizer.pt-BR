---
solution: Journey Optimizer
product: journey optimizer
title: Metadados C2PA no email e na landing page do Designer
description: Saiba o que acontece com os metadados C2PA já anexados a uma imagem à medida que ela se move pelo designer de email e página de aterrissagem no Adobe Journey Optimizer.
feature: Content Management
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 47e95cbc3716e650492e9cda4a4fddbe61f56ffd
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# Metadados C2PA no email e na landing page do Designer {#c2pa-email-landing-page-designer}

>[!BEGINSHADEBOX]

**Nesta página:** saiba o que acontece com os metadados C2PA já anexados a uma imagem à medida que ela se move pelo designer de email e página de aterrissagem no Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!INFO]
>
>Novas leis estão surgindo em torno da transparência generativa da IA, e a Adobe está trabalhando para atender aos requisitos aplicáveis em todas as jurisdições. Os metadados C2PA são a ferramenta de origem que o Adobe usa para atender aos requisitos dessas leis.

O designer de email e página de aterrissagem não gera ou edita imagens sozinho. Ele faz referência a imagens que já foram geradas ou editadas com IA gerativa em outra ferramenta do Adobe, como Gerar conteúdo, Adobe Express ou Firefly, ou em um modelo de parceiro. Os metadados do C2PA já anexados a essas imagens são preservados e inalterados à medida que você cria, publica e envia.

## Os metadados do C2PA são preservados à medida que você cria e envia {#c2pa-preserved}

A tabela a seguir resume o que acontece com os metadados C2PA em cada etapa da criação e envio de conteúdo com o designer de email e de página de aterrissagem.

| Ação | O que acontece | Metadados C2PA preservados? | Exemplo |
| --- | --- | --- | --- |
| **Inserir uma imagem em um modelo** | O designer adiciona uma referência a uma imagem já gerada ou editada com IA gerativa em outro lugar, como Gerar conteúdo, Adobe Express, Firefly ou um modelo de parceiro. O próprio arquivo de imagem não é alterado. | Sim, inalterado | Um banner gerado pela Firefly é inserido em um template de email. |
| **Redimensionar, reposicionar ou adicionar texto alternativo** | Somente as propriedades de exibição no HTML do modelo são alteradas. O arquivo de imagem não é codificado novamente. | Sim, inalterado | Uma imagem é redimensionada para caber em um layout móvel e recebe o texto alternativo. |
| **Publicar** | O email ou a landing page é publicado e a imagem é armazenada para entrega. | Sim, inalterado | Uma campanha é publicada e suas imagens são armazenadas para envio. |
| **Enviar um email ou exibir uma página de aterrissagem** | A imagem é entregue na caixa de entrada do recipient ou exibida na página ao vivo. | Sim, inalterado | Um recipient abre o email e baixa a imagem; a credencial ainda corresponde à original. |

## Tipos de conteúdo e seu escopo {#c2pa-content-types}

* **Imagens**: Cobertas. Os metadados do C2PA já anexados a uma imagem são preservados à medida que são inseridos, ajustados, publicados e entregues, conforme mostrado acima.
* **Vídeo, áudio, texto**: não aplicável. O designer de email e página de aterrissagem não gera nem edita esses tipos de conteúdo com a IA gerativa.

## O que acontece quando o conteúdo se move {#c2pa-content-moves}

Os metadados do C2PA viajam com a imagem pelo email e pelo designer da página de aterrissagem no Adobe Journey Optimizer, do editor ao armazenamento até a caixa de entrada do destinatário ou a página ao vivo. Nenhuma credencial é criada, alterada ou removida em nenhuma dessas etapas.

Se uma imagem não tiver metadados C2PA de IA gerativa, porque não foi gerada ou editada com IA gerativa, nenhuma credencial aparecerá nela aqui. Isso é esperado, não um erro.

## Verificação de uma credencial {#c2pa-checking-credential}

Ainda não há uma maneira de inspecionar um Content Credential diretamente no designer de email ou de página de aterrissagem.

## Recursos adicionais

* [Metadados C2PA no conteúdo de Geração](generative-c2pa-metadata.md)
* [Transparência do conteúdo de IA gerativa](https://experienceleague.adobe.com/pt-br/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency)
