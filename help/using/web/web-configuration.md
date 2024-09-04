---
title: Configuração do canal da Web
description: Criar configuração do canal da Web
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 2161baf0-38b7-4397-bffe-083929e8033a
source-git-commit: 37e60e5d7c0ad164cde67015b72341e1f4eda6a9
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 3%

---

# Criar configuração do canal da Web {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Regra de correspondência de páginas"
>abstract="Para gerenciar e direcionar com eficiência um grupo de URLs que compartilham os mesmos critérios, crie uma regra de Correspondência de páginas. Essa regra permite consolidar vários URLs em uma única diretriz, simplificando a aplicação de configurações e ações consistentes nessas páginas."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="URL padrão de criação e visualização"
>abstract="Esse campo garante que as páginas geradas ou correspondidas pela regra tenham um URL designado, essencial para a criação e a visualização eficaz do conteúdo."

Uma configuração da Web é uma propriedade da Web identificada por um URL em que o conteúdo será entregue. Ele pode corresponder a um único URL de página ou a várias páginas, permitindo que você faça modificações em uma ou várias páginas da Web.

1. Acesse o menu **[!UICONTROL Canais]** > **[!UICONTROL Configurações gerais]** > **[!UICONTROL Configurações de canal]** e clique em **[!UICONTROL Criar configuração de canal]**.

   ![](assets/web_config_1.png)

1. Insira um nome e uma descrição (opcional) para a configuração.

   >[!NOTE]
   >
   > Os nomes devem começar com uma letra (A-Z). Ele só pode conter caracteres alfanuméricos. Também é possível usar sublinhado `_`, ponto`.` e hífen `-` caracteres.

1. Para atribuir rótulos de uso de dados personalizados ou de núcleo à configuração, você pode selecionar **[!UICONTROL Gerenciar acesso]**. [Saiba mais sobre OLAC (Controle de Acesso em Nível de Objeto)](../administration/object-based-access.md).

1. Selecione o canal **Web**.

   ![](assets/web_config_2.png)

1. Selecione **[!UICONTROL Ação de marketing]**(s) para associar políticas de consentimento às mensagens que usam essa configuração. Todas as políticas de consentimento associadas à ação de marketing são utilizadas para respeitar as preferências dos clientes. [Saiba mais](../action/consent.md#surface-marketing-actions)

1. Você pode digitar uma **[!UICONTROL URL da página]** se quiser aplicar as alterações a uma única página.

1. Ou você pode criar uma **[!UICONTROL regra de correspondência de páginas]** para direcionar várias URLs que correspondam à mesma regra; por exemplo, se você deseja aplicar as alterações a um banner principal em todo o site ou adicionar uma imagem superior que seja exibida em todas as páginas de produto de um site.

   Para fazer isso, selecione **[!UICONTROL Páginas que correspondem à regra]**.

1. Defina seus critérios para os campos **[!UICONTROL Domínio]** e **[!UICONTROL Página]**.

   Por exemplo, se você deseja editar elementos que são exibidos em todas as páginas de produtos femininas do seu site Luma, selecione **[!UICONTROL Domínio]** > **[!UICONTROL Começa com]** > `luma` e **[!UICONTROL Página]** > **[!UICONTROL Contém]** > `women`.

   ![](assets/web_config_3.png)

1. Se você criou uma **[!UICONTROL regra de correspondência de páginas]**, é necessário inserir a URL de criação e visualização **Padrão**. Essa etapa garante que as páginas geradas ou correspondidas pela regra tenham um URL designado para fins de criação de conteúdo e pré-visualização. Saiba mais sobre a regra de correspondência de páginas na [seção abaixo](#web-page-matching-rule).

1. Salve as alterações.

Agora você pode selecionar sua configuração ao usar o canal da Web em campanhas ou jornadas.

## Regra de correspondência de páginas {#web-page-matching-rule}

Ao criar uma regra que corresponda a várias páginas para que você possa aplicar as mesmas alterações de conteúdo em várias páginas de uma só vez, é possível usar operadores diferentes nas seções **Domínio** e **Caminho** para criar a regra desejada. Verifique os operadores disponíveis abaixo.

Operadores disponíveis para criar regras de correspondência de página:

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

Se o caso de uso não puder ser modelado usando uma regra, você terá a opção de adicionar várias regras de página e poderá usar operadores &quot;Ou&quot; ou &quot;Excluir&quot; entre elas. &quot;Excluir&quot; é útil quando uma das páginas que correspondem à regra definida não deve ser direcionada: por exemplo, todas as páginas &quot;example.com&quot; que contêm &quot;product&quot;, excluindo a seguinte página: `https://example.com/blogs/productinfo`.
