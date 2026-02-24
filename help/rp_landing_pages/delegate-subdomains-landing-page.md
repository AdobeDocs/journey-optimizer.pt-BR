---
solution: Journey Optimizer
product: Journey Optimizer
title: Delegar subdomínios de email
description: Delegar subdomínios de email
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# Delegar subdomínios de email{#section-overview}

A delegação de subdomínios de email é uma etapa principal na [configuração de canal](../using/configuration/get-started-configuration.md), necessária antes do envio de emails do Journey Optimizer. Os subdomínios permitem isolar tipos de tráfego (por exemplo, marketing ou transacional), proteger a reputação do seu domínio principal e acelerar o [aquecimento de IP](../using/configuration/ip-warmup-gs.md). Eles trabalham junto com a [configuração do canal de email](../using/email/get-started-email-config.md) e o [monitoramento da capacidade de entrega](../using/reports/deliverability.md) para garantir que as mensagens cheguem às caixas de entrada.

Você pode escolher entre vários métodos de configuração: **delegação completa** (o Adobe gerencia DNS), **configuração de CNAME** ou **delegação personalizada** (você tem certificados e DNS). Se você começar com CNAME, poderá mais tarde [migrar para a delegação personalizada](../using/configuration/custom-subdomain-migration.md) para obter segurança mais estrita. Esta seção também abrange registros DMARC e PTR, registros Google TXT para Gmail e pools de IP. Para obter orientações mais amplas sobre a capacidade de entrega, consulte [Introdução à capacidade de entrega](../using/reports/deliverability.md) e [Monitorar endereços de email](monitor-reputation-landing-page.md).

## Delegar subdomínios de email

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=pt-BR)

Introdução à delegação de subdomínios

Saiba mais sobre os benefícios, os métodos de configuração e as considerações para delegar subdomínios no Adobe Journey Optimizer.

[Iniciar delegação de subdomínios](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=pt-BR)

Delegar um subdomínio

Orientações passo a passo para delegar subdomínios à Adobe, incluindo delegação completa e configuração de CNAME.

[Saiba como delegar](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg?lang=pt-BR)

Configurar um subdomínio personalizado

Assuma a propriedade total de seus subdomínios com delegação personalizada — faça upload de seus próprios certificados SSL e mantenha o controle total sobre a configuração do domínio.

[Configurar um subdomínio personalizado](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=pt-BR)

Migrar de CNAME para Delegação personalizada

Migre subdomínios existentes configurados para CNAME para uma delegação personalizada para atender às políticas de segurança e obter controle total sobre os certificados.

[Migrar o subdomínio](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=pt-BR)

Configurar os registros de DMARC

Configure registros de DMARC para aprimorar a segurança e a capacidade de entrega de emails para subdomínios delegados.

[Configurar DMARC agora](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=pt-BR)

Adicionar um registro TXT do Google

Verifique a capacidade de entrega do Gmail dos subdomínios, adicionando registros de TXT do Google, no Adobe Journey Optimizer.

[Adicionar registros de TXT do Google](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=pt-BR)

Acessar e editar registros de PTR

Gerencie registros de PTR para os subdomínios delegados, incluindo edição e noções básicas sobre os status de atualização.

[Editar registros de PTR](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=pt-BR)

Criar pools de IP

Agrupe endereços IP para melhorar a capacidade de entrega de email e gerenciar a reputação do subdomínio de maneira eficaz.

[Criar pools de IP](../using/configuration/ip-pools.md)
:::

::::

## Recursos adicionais

- **[Configurar subdomínios de página de aterrissagem](../using/landing-pages/lp-subdomains.md)** - Configure subdomínios para páginas de aterrissagem e formulários de assinatura.
- **[Configurar subdomínios da Web](../using/web/web-delegated-subdomains.md)** - Delegar subdomínios para experiências e rastreamento da Web.
- **[Introdução à configuração de canais](../using/configuration/get-started-configuration.md)** - Visão geral de todas as etapas de configuração de canal, incluindo a delegação de subdomínio.
