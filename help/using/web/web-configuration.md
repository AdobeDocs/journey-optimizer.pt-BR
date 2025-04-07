---
title: Configuração do canal da Web
description: Criar configuração do canal da Web
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 2161baf0-38b7-4397-bffe-083929e8033a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 11%

---

# Configurar suas experiências na Web {#web-configuration}

## Criar uma configuração de canal da Web {#create-web-configuration}

Uma configuração da Web é uma propriedade da Web identificada por um URL em que o conteúdo será entregue. Ele pode corresponder a um único URL de página ou a várias páginas, permitindo que você faça modificações em uma ou várias páginas da Web.

Para criar uma configuração de canal da Web, siga as etapas abaixo.

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/web_config_1.png)

1. Insira um nome e uma descrição (opcional) para a configuração.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar os caracteres de sublinhado `_`, ponto `.` e hífen `-`.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre o OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md)

1. Selecione o canal **Web**.

   ![](assets/web_config_2.png)

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

1. Na seção **[!UICONTROL Configurações da Web]**, selecione uma das seguintes opções:

   * **[!UICONTROL Página única]** - Se quiser aplicar as alterações a uma única página, insira uma **[!UICONTROL URL da página]**.

   * **[!UICONTROL Regra de correspondência de páginas]** - Para direcionar várias URLs correspondentes à mesma regra, crie uma regra de correspondência de páginas e insira uma **[!UICONTROL URL de criação e visualização padrão]**. [Saiba mais](#web-page-matching-rule)

1. Clique em **[!UICONTROL Enviar]** para salvar suas alterações.

Agora é possível selecionar essa configuração ao usar o canal da Web em suas campanhas ou jornadas.

## Criar uma regra de correspondência de páginas {#web-page-matching-rule}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Criar uma regra de correspondência de páginas"
>abstract="Para gerenciar e direcionar com eficiência um grupo de URLs que compartilham os mesmos critérios, crie uma regra de correspondência de páginas. Essa regra permite consolidar vários URLs em uma única diretriz, simplificando a aplicação de configurações e ações consistentes nessas páginas."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="Definir um URL para criação e visualização de conteúdo"
>abstract="Este campo garante que as páginas geradas ou encontradas pela regra tenham um URL designado, o que é essencial para criar e visualizar conteúdo com eficiência."

Ao criar uma configuração da Web ou da [experiência baseada em código](../code-based/get-started-code-based.md), você pode criar uma **[!UICONTROL regra de correspondência de páginas]** para direcionar várias URLs correspondentes à mesma regra. Portanto, é possível aplicar as mesmas alterações de conteúdo em várias páginas de uma só vez.

Por exemplo, talvez você queira aplicar as alterações em um banner principal em todo o site ou adicionar uma imagem superior que seja exibida em todas as páginas de produtos de um site.

1. Ao configurar sua [Web](#web-configuration) ou [experiência baseada em código](../code-based/code-based-configuration.md), selecione **[!UICONTROL Páginas que correspondem à regra]**.

1. Defina seus critérios para os campos **[!UICONTROL Domínio]** e **[!UICONTROL Página]**.

   >[!NOTE]
   >
   >Verifique os operadores disponíveis em [esta seção](#available-operators).

   Por exemplo, se você deseja editar elementos que são exibidos em todas as páginas de produtos femininas do seu site Luma, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Começa com]** > `luma` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `women`.

   ![](assets/web_config_3.png)

1. Se o caso de uso não puder ser modelado usando uma regra, você terá a opção de adicionar várias regras. Clique em **[!UICONTROL Adicionar outra regra de página]** e repita a etapa acima.

   >[!NOTE]
   >
   >Você pode adicionar até 10 regras.

1. Você pode usar os operadores **[!UICONTROL Or]** ou **[!UICONTROL Exclude]** entre as diferentes regras.

   **[!UICONTROL Excluir]** é útil quando uma das páginas que correspondem à regra definida não deve ser direcionada. Por exemplo, você pode direcionar todas as `luma.com` páginas que contenham `product`, excluindo a seguinte página: `https://luma.com/blogs/productinfo`.

   ![](assets/web_config_4.png)

1. Insira a **[!UICONTROL URL padrão de criação e visualização]**. Essa etapa garante que as páginas geradas ou correspondidas pela regra tenham um URL designado para fins de criação de conteúdo e pré-visualização.

### Operadores disponíveis para criar regras de correspondência de página {#available-operators}

Ao criar uma regra [que corresponda a várias páginas](#web-page-matching-rule), você pode usar operadores diferentes nas seções **[!UICONTROL Domínio]** e **[!UICONTROL Caminho]** para criar a regra desejada. Os operadores disponíveis estão listados abaixo.

* **Domínio**

  | Operador  | Descrição  | Exemplos  |
  |---|---|---|
  | Igual a  | Correspondência exata do domínio.  |
  | Começa com  | Corresponde a todos os domínios (incluindo subdomínios) que começam com a cadeia de caracteres inserida.  | Exemplo: &quot;Começa com: dev&quot; -> corresponde a todos os domínios e subdomínios que começam com &quot;dev&quot;, como: dev.example.com, dev.products.example.com, developer.example.com  |
  | Termina com  | Corresponde a todos os domínios (incluindo subdomínios) que terminam com a cadeia de caracteres inserida.  | Ex: &quot;Termina com: exemplo.com&quot; -> corresponde a todos os domínios e subdomínios que terminam com &quot;exemplo.com&quot;, como: stage.example.com, prod.example.com, myexample.com  |
  | Correspondência de curinga  | O operador &quot;Correspondência de curinga&quot; permite que o usuário defina uma correspondência de curinga no meio da cadeia de caracteres, como &quot;dev.*.example.com&quot;. As regras de validação indicam que o valor deve conter apenas um curinga (asterisco) quando o operador for &quot;correspondente a um curinga&quot;.  | Exemplo: &quot;Correspondência curinga: dev.*.example.com&quot; -> corresponde a domínios como: dev.products.example.com, dev.mytest.products.example.com, dev.blog.example.com  |
  | Qualquer  | Corresponde a todos os domínios; útil ao testar um caminho específico entre domínios  |


* **Caminho**

<table>
    <thead>
    <tr>
        <th><strong>Operador</th>
        <th><strong>Descrição</th>
        <th><strong>Exemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>Igual a</td>
        <td>Correspondência exata do caminho. </td>
        <td></td>
    </tr>
    <tr>
        <td>Inicia com</td>
        <td>Corresponde a todos os caminhos (incluindo subcaminhos) que começam com a cadeia de caracteres inserida.</td>
        <td></td>
    </tr>
    <tr>
        <td>Termina com</td>
        <td>Corresponde a todos os caminhos (incluindo subcaminhos) que terminam com a cadeia de caracteres inserida.</td>
        <td></td>
    </tr>
    <tr>
        <td>Qualquer uma</td>
        <td>Corresponde a todos os caminhos, útil ao direcionar todos os caminhos em um ou vários domínios.</td>
        <td></td>
    </tr>
    <tr>
        <td>Correspondência de curinga</td>
        <td>O operador "Wildcard matching" permite que o usuário defina um curinga interno dentro do caminho, como "/products/*/detail".  O caractere curinga * no componente Caminho ** corresponde a qualquer sequência de caracteres até que o primeiro caractere / seja encontrado.  /*/ corresponde a qualquer sequência de caracteres (incluindo subcaminhos)</td>
        <td>Ex: "Correspondência curinga: /products/*/detail", corresponde a todos os caminhos como: <ul><li>example.com/products/yoga/detail</li><li>example.com/products/surf/detail</li><li>example.com/products/tennis/detail</li><li>example.com/products/yoga/pants/detail</li></ul>Ex: "Corresponde: /prod*/detail, corresponde a todos os caminhos como: <ul><li>example.com/products/detail</li><li>example.com/production/detail</li></ul>não corresponde a caminhos como: <ul><li>example.com/products/yoga/detail</li></ul></td>
    </tr>
    <tr>
        <td>Contains</td>
        <td>"contains" é traduzido para um curinga como "mystring" e corresponde a todos os caminhos que contêm essa sequência de caracteres.</td>
        <td>Por exemplo: "Contains: product" corresponde a todos os caminhos que contêm a cadeia de caracteres product, como: <ul><li>example.com/products</li><li>example.com/yoga/perfproduct</li><li>example.com/surf/productdescription</li><li>example.com/home/product/page</li></ul></td>
    </tr>
    </tbody>
</table>
