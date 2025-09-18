---
solution: Journey Optimizer
product: journey optimizer
title: Geração automática de variantes de conteúdo (Beta)
description: Saiba como gerar variantes de conteúdo automaticamente usando a simulação baseada em IA.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Beta privado" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 53d8fbb28e8516e4ee79f556a335b2d084af42e7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---


# Geração automática de variantes de conteúdo (Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>Este recurso está atualmente no **beta privado** e pode não estar disponível em seu ambiente. Entre em contato com o seu representante da Adobe para obter acesso.

O [!DNL Journey Optimizer] apresenta uma simulação baseada em IA que pode gerar automaticamente várias variantes para testar seu conteúdo. Esse recurso reduz a necessidade de criar variantes manualmente, facilitando a validação da lógica de personalização em modelos complexos.

Ao renderizar conteúdo para simulação ou prova, o sistema analisa seu conteúdo e identifica todos os tokens de personalização e regras de ramificação. Ele substitui tokens de personalização por valores significativos que fornecem uma visualização quase realista do conteúdo final.

Considere um modelo de email de serviços financeiros com lógica de ramificação baseada em **tipo de investidor**, **faixa etária**, **estado civil**, **verificação de ID de imposto** e **localização**. Sem a geração de variantes, seria necessário criar manualmente dezenas de variantes para validar todos os caminhos. Com variantes geradas automaticamente, o sistema produz variantes representativas que cobrem automaticamente essas condições.  Cada variante gerada é renderizada no painel de visualização, mostrando exatamente quais blocos e condições são aplicados.

## Gerar variantes de conteúdo

Para gerar variações para seu conteúdo e visualizá-las, siga estas etapas:

1. Abra o conteúdo e selecione **[!UICONTROL Simular conteúdo]** / **[!UICONTROL Simular variações de conteúdo]**.

   ![](assets/simulate-sample.png)

2. Clique no botão **[!UICONTROL Gerar]**.

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer] gera automaticamente variantes com base em atributos detectados.

4. Revise a lista de variantes geradas no painel esquerdo e selecione uma variante para ver sua renderização personalizada no painel de visualização.

>[!NOTE]
>
>Esse recurso funciona da mesma forma que o recurso Simular variações de conteúdo padrão. Para obter mais informações sobre simulações de variações de conteúdo e as medidas de proteção e limitações associadas, consulte esta seção: [Simular variações de conteúdo](../test-approve/simulate-sample-input.md)
