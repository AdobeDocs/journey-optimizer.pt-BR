---
solution: Journey Optimizer
product: journey optimizer
title: Criar um plano de aquecimento de IP
description: Saiba como criar um plano de aquecimento de IP no Journey Optimizer
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupo, subdomínios, capacidade de entrega
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 11%

---

# Criar um plano de aquecimento de IP {#ip-warmup}

>[!BEGINSHADEBOX]

O que há neste guia de documentação:

* [Introdução ao aquecimento de IP](ip-warmup-gs.md)
* [Criar campanhas de aquecimento de IP](ip-warmup-campaign.md)
* **[Criar um plano de aquecimento de IP](ip-warmup-plan.md)**
* [Executar o plano de aquecimento de IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Depois de criar um ou mais [Campanhas de aquecimento de IP](ip-warmup-campaign.md) com uma superfície dedicada e a opção correspondente ativada, você pode começar a criar seu plano de aquecimento de IP.

>[!CAUTION]
>
>Para acessar, criar, editar e excluir os planos de aquecimento de IP, você deve ter a **[!UICONTROL Consultor de avaliação de entrega]** permissão. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## Preparar o arquivo de plano de aquecimento de IP {#prepare-file}

O aquecimento de IP é uma atividade que consiste em aumentar gradualmente o volume de emails que saem de seus IPs e domínios para os principais provedores de serviços de Internet (ISPs), a fim de estabelecer sua reputação como remetente legítimo.

Essa atividade é normalmente realizada com a ajuda de um especialista em capacidade de entrega que ajuda a preparar um plano bem pensado com base nos domínios do setor, casos de uso, regiões, ISPs e vários outros fatores.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Antes de poder criar um plano de aquecimento de IP no [!DNL Journey Optimizer] é necessário preencher um modelo do Excel com todos os dados que alimentarão seu plano.

>[!CAUTION]
>
>Trabalhe com seu consultor de entrega para garantir que seu arquivo de plano de aquecimento de IP esteja configurado corretamente.
>
>Use o formato fornecido no modelo.

Veja abaixo um exemplo de um arquivo contendo um plano de aquecimento de IP.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>Por enquanto, você deve deixar o **Propriedades** e **Valor** células intocadas.

### Guia Plano de aquecimento de IP {#ip-warmup-plan-tab}

* Neste exemplo, um plano foi preparado abrangendo mais de 17 dias (chamado de &quot;**execuções**&quot;) para atingir um volume-alvo de mais de um milhão de perfis.

* Este plano é executado até seis **fases**, cada um deles contendo pelo menos uma execução.

* Você pode ter quantas colunas quiser para os domínios que deseja entregar. Neste exemplo, o plano é dividido em seis colunas:

   * Quatro dos quais correspondem a **grupos de domínio prontos para uso** para usar no seu plano (Gmail, Microsoft, Yahoo e Orange).
   * Um corresponde a um grupo de domínio personalizado (que você precisa adicionar usando o [Grupo de domínio personalizado](#custom-domain-group-tab) guia ).
   * A sexta coluna, **Outros**, contém todos os endereços restantes de outros domínios que não estão explicitamente cobertos no plano. Essa coluna é opcional: se omitida, os emails irão somente para os domínios especificados.
* A variável **Dias de engajamento** mostra que somente os perfis engajados com sua marca no último período inserido são direcionados.

A ideia é aumentar progressivamente o número de endereços direcionados em cada execução, enquanto reduz o número de execuções para cada fase.

Os grupos de domínio principais predefinidos que você pode adicionar ao seu plano estão listados abaixo:

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Laranja
* Softbank
* Docomo
* Internet Unificada
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

<!--
+++ Gmail
gmail.com;gmail.fr;gmail.de;gmail.co.uk;gmail.it
+++

+++ Adobe
adobe.com;adobe.fr;adobe.es
+++

+++WP
+++

+++Comcast
+++

+++Yahoo
+++

+++Bigpond
+++

+++Orange
+++

+++Softbank
+++

+++Docomo
+++

+++United Internet
+++

+++Microsoft
+++

+++KDDI
+++

+++Italia Online
+++

+++La Poste
+++
-->

### Guia Grupo de domínio personalizado {#custom-domain-group-tab}

Você também pode adicionar mais colunas ao seu plano, incluindo grupos de domínio personalizados.

Use o **[!UICONTROL Grupo de domínio personalizado]** para definir um novo grupo de domínio. Para cada domínio, você pode adicionar todos os subdomínios que ele abrange.<!--TBC-->

Por exemplo, se você adicionar o domínio personalizado Luma, desejará que os seguintes subdomínios sejam incluídos: luma.com, luma.co.uk, luma.it, luma.fr, luma.de, etc.

![](assets/ip-warmup-sample-file-custom.png)

### Exemplo {#example}

Digamos que você queira ter dois grupos de domínio personalizados:

* Um somente para domínios do Hotmail.
* Um para todos os outros domínios do grupo de domínio Microsoft (excluindo todos os domínios do Hotmail).

Observe que todos os outros domínios serão coletados na variável **[!UICONTROL Outros]** coluna.

1. No **[!UICONTROL Grupo de domínio personalizado]** , crie a **Hotmail** grupo de domínio.

1. Adicione todos os domínios do Hotmail na mesma linha.

   Você pode [copiar e colar](#copy-paste) todos os domínios do Hotmail listados na variável [Guia Plano de aquecimento de IP](#ip-warmup-plan-tab) seção.

1. Adicione outra linha.

1. Crie o **Microsoft_X** grupo de domínio.

1. Adicione todos os domínios do Microsoft que não são do Hotmail na mesma linha. Da mesma forma, você pode copiá-los e colá-los da lista acima. [Saiba mais](#copy-paste)

1. Volte para o **[!UICONTROL Plano de aquecimento de IP]** guia.

1. Crie três colunas: uma para **Hotmail**, um para **Microsoft_X** e um para **Outros**.

1. Preencha as colunas de acordo com suas necessidades.

>[!NOTE]
>
>Depois que o plano de aquecimento de IP for carregado em [!DNL Journey Optimizer], não será necessário excluir os grupos de domínio do Microsoft.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Copiar e colar domínios padrão {#copy-paste}

Se quiser criar um grupo de domínios personalizado contendo todos os domínios do Hotmail, por exemplo, você pode copiar e colar os domínios da lista padrão fornecida [acima](#ip-warmup-plan-tab).

Em seguida, use a ferramenta de conversão do Excel para converter texto em colunas:

1. Selecionar **[!UICONTROL Dados]** > **[!UICONTROL Texto para colunas...]**, escolha **[!UICONTROL Delimitado]** e selecione **[!UICONTROL Próxima]**.

1. Selecionar **[!UICONTROL Ponto e vírgula]**, clique em **[!UICONTROL Próxima]** e **[!UICONTROL Concluir]**.

Cada domínio agora é exibido em uma coluna diferente na mesma linha.

## Acessar e gerenciar planos de aquecimento de IP {#manage-ip-warmup-plans}

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Planos de aquecimento de IP]** menu. Todos os planos de aquecimento de IP criados até o momento são exibidos.

   ![](assets/ip-warmup-filter-list.png)

1. Você pode filtrar pelo status. Os diferentes status são:

   * **Não iniciado**: nenhuma execução foi ativada ainda. [Saiba mais](ip-warmup-execution.md#define-runs)
   * **Ao vivo**: o plano muda para esse status assim que a primeira execução na primeira fase é ativada com sucesso. [Saiba mais](ip-warmup-execution.md#define-runs)
   * **Concluído**: o plano foi marcado como concluído. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [Saiba mais](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Para excluir um plano de aquecimento de IP, selecione o **[!UICONTROL Excluir]** ícone ao lado do nome de um plano e confirmar a exclusão.

   >[!NOTE]
   >
   >Somente planos com o **Não iniciado** O status pode ser excluído.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >O plano de aquecimento de IP selecionado será excluído permanentemente.

## Criar um plano de aquecimento de IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Especifique o seu plano de aquecimento de IP"
>abstract="Baixe o modelo CSV e preencha-o com os dados das fases de aquecimento de IP e o número de perfis do público-alvo."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Selecione uma superfície de marketing"
>abstract="Você precisa selecionar a mesma superfície que a selecionada na campanha que deseja associar ao plano de aquecimento de IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=pt-BR" text="Configurar superfícies de canais"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=pt-BR" text="Criar campanhas de aquecimento de IP"

Para criar um plano de aquecimento de IP, siga as etapas abaixo.

1. Acesse o **[!UICONTROL Administração]** > **[!UICONTROL Canais]** > **[!UICONTROL Planos de aquecimento de IP]** e clique em **[!UICONTROL Criar plano de aquecimento de IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Preencha os detalhes do plano de aquecimento de IP: dê a ele um nome e uma descrição.

   ![](assets/ip-warmup-plan-details.png)

1. Selecione o [superfície](channel-surfaces.md) que você quer aquecer. Somente as superfícies de marketing estão disponíveis para seleção. [Saiba mais sobre tipo de email](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >As campanhas que você deseja associar ao plano de aquecimento de IP devem usar a mesma superfície. [Saiba como criar uma campanha de aquecimento de IP](ip-warmup-campaign.md)

1. Carregue o arquivo do Excel que contém seu plano de aquecimento de IP. [Saiba mais](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >Caso o upload falhe, verifique se você está usando a formatação e o formato de arquivo corretos (.xls ou .xlsx). Use a amostra fornecida pelo Adobe.

1. Clique em **[!UICONTROL Criar]**. Todas as fases, execuções, colunas e seu conteúdo definido no arquivo que você carregou são automaticamente exibidas na [!DNL Journey Optimizer] interface.

   ![](assets/ip-warmup-plan-uploaded.png)

Agora você está pronto para executar seu plano de aquecimento de IP. [Saiba mais](ip-warmup-execution.md)
