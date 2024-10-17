---
solution: Journey Optimizer
product: journey optimizer
title: Configurar dispositivos móveis e a web
description: Saiba como configurar e monitorar canais móveis e da web
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, superfície, técnico, parâmetros, otimizador
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: ht
source-wordcount: '770'
ht-degree: 100%

---

# Introdução à configuração de canal guiada {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nome da configuração móvel e da web"
>abstract="Insira o nome da sua configuração móvel ou da Web. Esse nome será usado para cada recurso criado automaticamente na configuração de canal guiada."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Validar com o Assurance"
>abstract="O Adobe Experience Platform Assurance está incorporado a este fluxo de trabalho para ajudar você a inspecionar a implementação do SDK, bem como simular e validar eventos de aplicativo."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-platform/assurance/home" text="Visão geral do Adobe Experience Platform Assurance"

Essa definição facilita a configuração rápida de canais de marketing, garantindo que todos os recursos necessários estejam prontamente disponíveis na Experience Platform, no Journey Optimizer e na Coleção de dados. Isso permite que sua equipe de marketing comece a criar campanhas e jornadas.

A configuração de canal guiada é compatível com as seguintes plataformas e canais.

* Plataformas e SDKs:

   * Swift para Apple, iOS

   * Kotlin, Android

   * Javascript, Web

* Canais:

   * Aplicativo móvel

   * Mensagem de push para dispositivos móveis

   * Básico para a web


Observe que é necessário criar uma configuração separada para cada plataforma que você deseja configurar. Isso se deve ao fato de que cada aplicativo exige uma configuração de canais exclusiva e garante flexibilidade para determinar quais canais você gostaria de usar em cada plataforma.

## Pré-requisitos {#prereq}

* Para implementar isso de maneira eficaz, é essencial que um membro da organização com autoridade e capacidade técnica para modificar o site ou o código móvel supervisione a configuração.

  Veja abaixo as permissões necessárias para executar a configuração de canal guiada.

+++ Permissões necessárias

  <table>
    <thead>
      <tr>
        <th><strong>Solução</strong></th>
        <th><strong>Permissões</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>Coleção de dados</p>
        </td>
        <td>
          <ul>
            <li>Direitos da empresa &gt; Propriedades</li>
            <li>Direitos de propriedade: desenvolver, publicar e gerenciar extensões e ambientes</li>
            <li>Superfícies do aplicativo: gerenciar a configuração do aplicativo</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>Coleção de dados: gerenciar sequências de dados</li>
           <li>Sandbox: conceder acesso a sandboxes</li>
            <li>Gerenciar segmentos: ler, criar, editar e excluir definições de segmentos</li>
            <li>Gerenciar perfis: ler, criar, editar e excluir perfis</li>
            <li>Conjuntos de dados de leitura: acesso somente leitura a conjuntos de dados</li>
            <li>Esquemas de leitura: acesso somente leitura a esquemas</li>
            <li>Namespace de identidade de leitura: acesso somente leitura ao namespace de identidade</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>Campanhas: gerenciar e publicar campanhas</p>
        </td>
      </tr>
    </tbody>
  </table>

+++

* Se você estiver usando a opção de configuração “Existente”, verifique se está utilizando as seguintes versões de extensão do SDK móvel da Adobe Experience Platform. Para obter mais detalhes sobre a configuração do SDK, incluindo as dependências e o código de inicialização necessários, consulte a [documentação a seguir](https://experienceleague.adobe.com/pt-br/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=pt-BR).

  Para Android

   * Mobile Core v3.1.0 ou posterior
   * Adobe Journey Optimizer v3.1.0 ou posterior

  Para iOS

   * Mobile Core v5.2.0 ou posterior
   * Adobe Journey Optimizer v5.1.1 ou posterior

## Recursos criados automaticamente {#auto-create-resources}

A configuração de canal guiada agiliza a configuração de canais de marketing, disponibilizando prontamente todos os recursos essenciais nos aplicativos da Experience Platform, do Journey Optimizer e da Coleção de dados. Isso permite que sua equipe de marketing comece rapidamente a criar campanhas e jornadas. Veja abaixo uma lista dos recursos que são gerados e configurados automaticamente como parte da configuração de canal guiada.

Navegue pelas guias abaixo para acessar as listas abrangentes de todos os recursos gerados automaticamente:

>[!BEGINTABS]

>[!TAB iOS]

Para a **configuração inicial**, veja abaixo uma lista abrangente de todos os recursos criados na tela **Detalhes da configuração** após clicar em **Criar recursos automaticamente**.

<table>
  <thead>
  <tr>
  <th><strong>Solução</strong></th>
  <th><strong>Recursos criados automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Propriedade de tag móvel</li>
  <li>Regras</li>
  <li>Elementos de dados</li>
  <li>Biblioteca</li>
  <li>Ambientes (preparo, produção, desenvolvimento)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensões de tags</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimento (com políticas de consentimento padrão habilitadas)</li>
  <li>Identidade (com ECID padrão e regras de compilação padrão)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sessão do Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Sequência de dados</p>
  </td>
  <td>
  <p>Sequência de dados com serviços</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Conjunto de dados</li>
  <li>Esquema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Para a **configuração de canal**, veja abaixo uma lista abrangente de todos os recursos criados na tela **Adicionar canais**.

<table>
  <thead>
  <tr>
  <th><strong>Solução</strong></th>
  <th><strong>Recursos criados automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configuração de canais</li>
  <li>Fazer upload da credencial de push (somente mensagem de push para dispositivos móveis)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Para a **configuração inicial**, veja abaixo uma lista abrangente de todos os recursos criados na tela **Detalhes da configuração** após clicar em **Criar recursos automaticamente**.

<table>
  <thead>
  <tr>
  <th><strong>Solução</strong></th>
  <th><strong>Recursos criados automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Propriedade de tag móvel</li>
  <li>Regras</li>
  <li>Elementos de dados</li>
  <li>Biblioteca</li>
  <li>Ambientes (preparo, produção, desenvolvimento)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensões de tags</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimento (com políticas de consentimento padrão habilitadas)</li>
  <li>Identidade (com ECID padrão e regras de compilação padrão)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sessão do Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Sequência de dados</p>
  </td>
  <td>
  <p>Sequência de dados com serviços</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Conjunto de dados</li>
  <li>Esquema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Para a **configuração de canal**, veja abaixo uma lista abrangente de todos os recursos criados na tela **Adicionar canais**.

<table>
  <thead>
  <tr>
  <th><strong>Solução</strong></th>
  <th><strong>Recursos criados automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configuração de canais</li>
  <li>Fazer upload da credencial de push (somente mensagem de push para dispositivos móveis)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Para a **configuração inicial**, veja abaixo uma lista abrangente de todos os recursos criados na tela **Detalhes da configuração** após clicar em **Criar recursos automaticamente**.

<table>
  <thead>
  <tr>
  <th><strong>Solução</strong></th>
  <th><strong>Recursos criados automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Propriedade de tag móvel</li>
  <li>Regras</li>
  <li>Elementos de dados</li>
  <li>Biblioteca</li>
  <li>Ambientes (preparo, produção, desenvolvimento)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensões de tags</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimento (com políticas de consentimento padrão habilitadas)</li>
  <li>Identidade (com ECID padrão e regras de compilação padrão)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sessão do Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Sequência de dados</p>
  </td>
  <td>
  <p>Sequência de dados com serviços</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Conjunto de dados</li>
  <li>Esquema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

