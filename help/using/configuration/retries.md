---
solution: Journey Optimizer
product: journey optimizer
title: Tentativas
description: Saiba como as tentativas são executadas antes de enviar um endereço para a lista de supressão
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: tentativas, rejeição, software, otimizador, erro
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 0db7f514a2604ad09fbd9863a51d3c86d69eac41
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 8%

---

# Tentativas {#retries}

Quando um email falha devido a um erro temporário **Soft bounce** para um determinado endereço, várias tentativas são executadas. Cada erro incrementa um contador de erros. Quando esse contador atinge o limite, o endereço de email é adicionado à lista de supressão.

>[!NOTE]
>
>Saiba mais sobre os tipos de erros na seção [Tipos de falha de entrega](../reports/suppression-list.md#delivery-failures).

Na configuração padrão, o limite é definido como 5 erros.

* Para a mesma entrega, no quinto erro encontrado no [período de nova tentativa](#retry-duration), o endereço é suprimido.

* Se houver diferentes deliveries e dois erros ocorrerem com pelo menos 24 horas de intervalo, o contador de erros será incrementado em cada erro e o endereço também será suprimido na quinta tentativa. Os erros são cumulativos para cada endereço.

Se um delivery for bem-sucedido após uma tentativa, o contador de erros do endereço será reinicializado.

Por exemplo:

* Você envia um email na segunda-feira com um período de nova tentativa definido como 24 horas. Falha na entrega do endereço `emma.jones@mail.com`. O email é repetido até três vezes e o interrompe ao atingir o período de 24 horas de nova tentativa.

* Você envia outro email na quarta-feira. O `emma.jones@mail.com`, que já tem uma contagem de três erros, também é direcionado e novamente não é entregue - duas vezes. Dois outros erros são contabilizados.

Desde que nenhuma outra entrega tenha sido tentada e bem-sucedida entre esses dois emails, o endereço `emma.jones@mail.com` será adicionado à lista de supressão devido ao impacto cumulativo de erros 3 + 2.

## Edição do limite de novas tentativas {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="Atualizar limite de novas tentativas"
>abstract="Se o valor padrão não atender às suas necessidades, você poderá modificar o número permitido de rejeições temporárias consecutivas. Quando o contador de tentativas atinge o limite de erro de um endereço de email específico, esse endereço é adicionado à lista de supressão."
<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html?lang=pt-BR" text="Understand the suppresion list"-->

Caso o valor padrão de 5 não atenda às suas necessidades, você poderá modificar o limite de erro seguindo as etapas abaixo.

1. Vá para **[!UICONTROL Canais]** > **[!UICONTROL Configurações de email]** > **[!UICONTROL Lista de supressão]**.

1. Selecione o botão **[!UICONTROL Editar regras de supressão]**.

   ![](assets/suppression-list-edit-retries.png)

1. Edite o número permitido de rejeições temporárias consecutivas de acordo com suas necessidades.

   ![](assets/suppression-list-edit-soft-bounces.png)

   Você deve inserir um valor inteiro entre 1 e 20, o que significa que o número mínimo de tentativas é 1 e o número máximo é 20.

   >[!CAUTION]
   >
   >Qualquer valor maior que 10 pode causar problemas de reputação da capacidade de entrega, bem como limitação de IP ou incluir na lista de bloqueios por ISPs. [Saiba mais sobre a capacidade de entrega](../reports/deliverability.md)

## Período de nova tentativa {#retry-duration}

O **período de nova tentativa** é o período no qual qualquer mensagem de email da entrega que encontrou um erro temporário ou uma rejeição temporária será repetida.

Por padrão, as tentativas serão executadas por **3.5 dias** (ou **84 horas**) a partir do momento em que a mensagem for adicionada à fila de emails.

No entanto, para garantir que as tentativas de repetição não sejam mais executadas quando não forem mais necessárias, você pode alterar essa configuração de acordo com suas necessidades ao criar ou editar uma [configuração de canal](channel-surfaces.md) aplicável ao canal de email.

Por exemplo, você pode definir o período de nova tentativa para 24 horas para um email transacional relacionado à redefinição de senha e que contém um link válido por apenas um dia. Da mesma forma, para uma venda à meia-noite, é possível definir um período de nova tentativa de 6 horas.

>[!NOTE]
>
>O período de nova tentativa não pode exceder 84 horas. O período mínimo de nova tentativa é de 6 horas para emails de marketing e 10 minutos para emails transacionais.

Saiba como ajustar os parâmetros de nova tentativa de email ao criar uma configuração de canal no [esta seção](../email/email-settings.md#email-retry).

