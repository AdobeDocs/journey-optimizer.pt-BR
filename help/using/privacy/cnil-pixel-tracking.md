---
solution: Journey Optimizer
product: journey optimizer
title: Orientação da CNIL sobre pixels de rastreamento de email
description: Saiba mais sobre as orientações atualizadas da CNIL sobre pixels de rastreamento de email e os controles do Adobe Journey Optimizer que podem apoiar seus esforços de conformidade.
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL, rastreamento, pixel, email, consentimento, recusa, privacidade
source-git-commit: dc428295d1916580c1b15eacce987696f178668b
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 1%

---


# Noções básicas sobre a orientação atualizada da CNIL sobre pixels de rastreamento de email {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**Nesta página:** saiba mais sobre a recomendação da CNIL de abril de 2026 sobre pixels de rastreamento de email e descubra os controles do Adobe Journey Optimizer — opções de rastreamento aberto, rastreamento em nível de link, gerenciamento de consentimento, mecanismos de recusa e supressão — que podem apoiar seus esforços de conformidade.

>[!ENDSHADEBOX]

Esta página é apenas para fins informativos. Não é um aconselhamento jurídico e não garante a sua conformidade com a legislação aplicável. Os recursos do produto Adobe Journey Optimizer descritos abaixo são componentes básicos que, configurados e operados adequadamente, podem oferecer suporte a uma implementação em conformidade. Cada cliente é responsável por determinar e cumprir suas obrigações conforme a legislação aplicável.

## Visão geral {#overview}

Em 14 de abril de 2026, a *Commission Nationale de l&#39;Informatique et des Libertés* (CNIL), autoridade de proteção de dados da França, publicou uma [recomendação sobre o uso de pixels de rastreamento em emails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). As orientações esclarecem quando o consentimento é necessário e destacam a importância de práticas de consentimento adequadas para o rastreamento de pixels de email. Essa política pode afetar as práticas de envio para qualquer entidade que entregue emails a assinantes com sede na França.

A CNIL forneceu um período de três meses a partir da data da recomendação para que as empresas informassem seus destinatários de email (&quot;usuários&quot;) sobre a presença dos pixels de rastreamento, sua finalidade e o direito dos usuários de recusarem. Durante esse período de transição, espera-se que os clientes notifiquem os usuários sobre o rastreamento de pixels e forneçam uma opção de não participação, se necessário. A **CNIL deve iniciar as atividades de imposição após 14 de julho de 2026.**

À medida que a CNIL e outros reguladores esclarecem orientações sobre rastreamento de pixels e problemas relacionados, a Adobe continuará a monitorar atualizações e informar os clientes sobre os recursos técnicos dos produtos da Adobe que oferecem suporte ao marketing por email, incluindo o Adobe Journey Optimizer.

O Adobe Journey Optimizer fornece controles que podem ajudar os clientes a gerenciar o rastreamento aberto no nível do delivery. Os clientes são responsáveis por determinar suas próprias obrigações de conformidade de acordo com as orientações da CNIL e outras leis aplicáveis, mas esses recursos podem apoiar os esforços de conformidade do cliente.

### O que é um pixel de rastreamento de email {#tracking-pixel}

Um pixel de rastreamento de email é uma imagem transparente 1x1 inserida na HTML de um email. Quando o cliente de email do recipient carrega essa imagem, o pixel faz o ping em um servidor que registra dados, como carimbo de data e hora, tipo de dispositivo, cliente de email e, às vezes, um endereço IP para localização aproximada. Esse log é vinculado ao registro de um recipient, permitindo que os profissionais de marketing vejam se um email está aberto.

### Suporte ao cliente {#support}

Os clientes que buscam assistência para implementar as alterações descritas acima podem interagir com o ecossistema existente do Adobe. Para perguntas técnicas sobre os recursos da Adobe mencionados, entre em contato com o Gerente de sucesso do cliente ou gerente de conta técnica.

## Funcionalidade do Adobe Journey Optimizer relacionada ao rastreamento de email {#ajo-functionality}

A Adobe Journey Optimizer fornece vários controles nativos para ajudar os clientes a lidar com elementos da orientação da CNIL. As seções abaixo descrevem os recursos relevantes do produto.

### Classificação do tipo de email {#email-type}

No Adobe Journey Optimizer, cada configuração de canal de email é classificada como Marketing ou Transacional. Essa classificação determina se o consentimento do assinante é necessário antes do envio.

* **Emails de marketing**: comunicações promocionais enviadas aos assinantes aceitos. O consentimento do usuário é necessário. Esses emails respeitam as preferências de supressão e recusa automaticamente.
* **Emails transacionais**: comunicações não comerciais (por exemplo, confirmações de pedidos, redefinições de senha). Eles podem ser enviados para perfis que cancelaram a assinatura de comunicações de marketing, sujeito à legislação aplicável.

O tipo de email está definido no nível de [configuração de canal](../email/email-settings.md#email-type). Ao criar um email em uma jornada ou campanha, os autores devem selecionar uma configuração de canal cujo tipo de email corresponda à natureza da comunicação. Essa classificação informa quais verificações de consentimento são aplicadas antes do delivery.

### Abrir controles de rastreamento {#open-tracking}

O Adobe Journey Optimizer permite que os profissionais de marketing controlem o rastreamento aberto (ou seja, o pixel 1x1) no nível da mensagem individual. Ao criar um email em uma jornada ou campanha, duas opções de rastreamento estão disponíveis no painel de propriedades da mensagem:

* **[!UICONTROL Aberturas de email]**: controla se o pixel de rastreamento aberto está incluído no email. Essa opção está habilitada por padrão.
* **[!UICONTROL Clique no email]**: controla se os cliques em links são rastreados. Essa opção também está ativada por padrão.

Para desabilitar o rastreamento de aberturas para um email específico, desmarque a opção **[!UICONTROL Aberturas de email]** ao criar sua mensagem. Quando desativada, a opção impede que dados de rastreamento abertos sejam coletados para esse delivery. Para organizações dentro do escopo, analise as configurações de rastreamento aberto para todas as jornadas e campanhas ativas antes da data de imposição.

<!--
Unclear whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral as engineering wasn't able to clarify.
-->

[Saiba como rastrear suas mensagens](../email/message-tracking.md)

### Gerenciamento de rastreamento de nível de link {#link-tracking}

Além da opção de rastreamento aberto por mensagem, o Designer de email da Adobe Journey Optimizer fornece controle granular sobre quais URLs são rastreados. Usando o painel **[!UICONTROL Links]** no Designer de email, os autores podem exibir todas as URLs rastreadas em uma mensagem e definir o modo de rastreamento para cada link individualmente.

Os modos de rastreamento disponíveis para cada link incluem:

* **Rastrear**: ativa o rastreamento nesse URL.
* **Recusar**: designa esta URL como recusa ou cancelamento de assinatura.
* **Mirror page**: designa esta URL como um link de mirror page.
* **Nunca**: o rastreamento nunca é ativado para esta URL, independentemente das configurações de nível de mensagem.

Definir links específicos para **Nunca** pode ajudar a garantir que determinadas URLs não sejam rastreadas mesmo quando o rastreamento em nível de mensagem estiver habilitado.

[Saiba como gerenciar o rastreamento no Designer de email](../email/message-tracking.md#manage-tracking)

### Captura e gerenciamento de consentimento {#consent-management}

O Adobe Journey Optimizer lida com o consentimento por meio do [esquema de Consentimento e Preferências](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=pt-BR){target="_blank"} do Adobe Experience Platform (AEP). As preferências de consentimento são armazenadas no nível do perfil e aplicadas automaticamente durante a execução da jornada e da campanha.

Os principais atributos de consentimento relevantes para o rastreamento de email incluem:

* **`consents.marketing.email.val`**: o campo principal de consentimento de marketing por email. Um valor de `y` indica aceitação; `n` indica recusa. Um valor vazio é tratado como consentimento por padrão (esse padrão pode ser alterado na integração).

### Mecanismos de recusa e retirada {#opt-out}

O Adobe Journey Optimizer oferece vários mecanismos para que os assinantes optem por não participar de comunicações e gerenciem suas preferências, e todos eles atualizam os atributos de consentimento do perfil no Adobe Experience Platform.

**Cancelar inscrição com um clique (cabeçalho do email)**

Quando a opção **[!UICONTROL Habilitar List-Unsubscribe]** está ativada na configuração do canal de email, uma URL de cancelamento de inscrição com um clique e o endereço mailto são adicionados automaticamente ao cabeçalho do email. Os recipients podem recusar diretamente do cliente de email sem clicar no corpo do email. Essa opção é ativada por padrão para novas configurações de canal.

[Saiba como configurar o List-Unsubscribe](../email/list-unsubscribe.md)

**Recusa em um clique (corpo do email)**

Os autores podem inserir um link para opção de não participação com um clique diretamente no conteúdo do email usando o Designer de email. Quando um recipient clica nesse link, sua preferência é atualizada imediatamente. O escopo da recusa pode ser:

* **Nível de canal**: exclui o perfil de todas as futuras comunicações por email no canal.
* **Nível de identidade**: recusa o endereço de email específico usado somente na mensagem atual.

[Saiba como adicionar um link para opção de não participação com um clique](../email/email-opt-out.md#one-click-opt-out)

**Central de preferências por meio de páginas de aterrissagem**

O recurso de página de aterrissagem nativa da Adobe Journey Optimizer permite que as organizações criem centros de preferências onde os assinantes podem gerenciar suas preferências de comunicação e rastreamento. Quando um assinante envia um formulário de centro de preferências, suas escolhas são gravadas de volta em seus atributos de perfil do AEP no grupo de campos Consentimento e Preferências.

Para cenários de conformidade com a CNIL, uma landing page do centro de preferências pode ser vinculada ao rodapé do email (distinta do link de cancelamento de inscrição) para que os recipients possam gerenciar suas preferências de rastreamento independentemente do status da assinatura.

[Saiba como gerenciar as preferências dos clientes](../action/preference-center.md)

### Processamento e aplicação do consentimento {#consent-enforcement}

Quando um recipient recusa por meio de qualquer um dos mecanismos acima, ocorre o seguinte:

* O atributo de consentimento do perfil (`consents.marketing.email.val`) é atualizado para `n` no Adobe Experience Platform.
* O perfil é imediatamente excluído dos envios futuros de email de marketing em jornadas e campanhas.
* As informações de recusa são armazenadas no Conjunto de dados do Serviço de consentimento da AEP.
* O Journey Optimizer executa uma verificação de consentimento no nível do canal antes de cada envio, garantindo que os perfis de recusa não recebam comunicações de marketing.

[Saiba mais sobre o gerenciamento de recusa](opt-out.md)

### Políticas de consentimento {#consent-policies}

As organizações podem criar e aplicar políticas de consentimento no Adobe Journey Optimizer para garantir que somente perfis que atendem a critérios de consentimento específicos recebam comunicações. As políticas de consentimento podem ser associadas às configurações de canal por meio de ações de marketing.

[Saiba como trabalhar com políticas de consentimento](../action/consent.md)

### Lista de supressão e nova solicitação {#suppression}

O Adobe Journey Optimizer gerencia automaticamente uma lista de supressão que inclui endereços de email, resultando em devoluções permanentes, devoluções temporárias ou reclamações de spam. Os perfis na lista de supressão são excluídos de envios de marketing futuros.

A API REST de supressão do Journey Optimizer fornece controle programático adicional sobre mensagens de saída, permitindo que as organizações gerenciem a supressão e incluam na lista de permissões o comportamento por meio da API.

[Saiba como gerenciar a lista de supressão](../configuration/manage-suppression-list.md)

<!--
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys.
-->

### Relatório {#reporting}

O relatório de email do Adobe Journey Optimizer fornece métricas de abertura e clique por meio de [Relatórios ao vivo](../reports/live-report.md) e [Relatórios do Customer Journey Analytics](../reports/report-gs-cja.md). Quando o rastreamento de **[!UICONTROL Aberturas de email]** é desabilitado para uma mensagem, os dados abertos não são coletados para essa entrega; os relatórios refletirão apenas cliques e outros sinais de envolvimento.
