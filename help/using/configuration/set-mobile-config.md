---
solution: Journey Optimizer
product: journey optimizer
title: Configurar dispositivos móveis e Web
description: Saiba como configurar e monitorar canais móveis e da Web
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, superfície, técnico, parâmetros, otimizador
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 13%

---

# Introdução à configuração de canal guiado {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nome da configuração móvel e da web"
>abstract="Insira o nome da sua configuração móvel ou da Web. Esse nome será usado para cada recurso criado automaticamente com a Configuração de canal guiada."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Validar com garantia"
>abstract="O Adobe Experience Platform Assurance está incorporado a este fluxo de trabalho para ajudá-lo a inspecionar a implementação do SDK, bem como simular e validar eventos de aplicativo."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Visão geral do Adobe Experience Platform Assurance"

Essa definição facilita a configuração rápida de canais de marketing, garantindo que todos os recursos necessários estejam prontamente disponíveis na Experience Platform, Journey Optimizer e Coleção de dados. Isso permite que sua equipe de marketing comece com a criação de campanhas e jornadas.

A configuração Canal guiado é compatível com as seguintes plataformas e canais.

* Plataformas e SDKs:

   * Swift para Apple, iOS

   * Kotlin, Android

   * Javascript, Web

* Canais:

   * Mobile In-App

   * Mensagem por push para dispositivo móvel

   * Web Basic


Observe que, para cada plataforma que você deseja configurar, é necessário criar uma configuração separada. Isso ocorre porque cada aplicativo requer uma Configuração de canal exclusiva e oferece flexibilidade para determinar quais canais você gostaria de usar em cada plataforma.

## Pré-requisitos {#prereq}

* Para implementar isso de maneira eficaz, é essencial que um membro da organização com autoridade e capacidade técnica para modificar o site ou o código móvel supervisione a configuração.

  Abaixo estão as permissões necessárias para executar a Configuração de canal guiada.

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
            <li>Direitos de propriedade: desenvolver, publicar, gerenciar extensões e ambientes</li>
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
            <li>Coleção de dados: gerenciar fluxos de dados</li>
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

* Se você estiver usando a opção Configuração existente, verifique se está usando as seguintes versões de extensão do SDK do Adobe Experience Platform Mobile. Para obter mais detalhes sobre a configuração do SDK, incluindo as dependências e o código de inicialização necessários, consulte a [documentação a seguir](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en).

  Para Android

   * Mobile Core v3.1.0 ou posterior
   * Adobe Journey Optimizer v3.1.0 ou posterior

  Para iOS

   * Mobile Core v5.2.0 ou posterior
   * Adobe Journey Optimizer v5.1.1 ou posterior

## Recursos criados automaticamente {#auto-create-resources}

A Configuração de canal guiada simplifica a configuração rápida de canais de marketing, disponibilizando prontamente todos os recursos essenciais nos aplicativos Experience Platform, Journey Optimizer e Coleção de dados. Isso permite que sua equipe de marketing comece rapidamente a criar campanhas e jornadas. Veja abaixo uma lista dos recursos que são gerados e configurados automaticamente como parte da Configuração de canal guiada.

Navegue pelas guias abaixo para acessar as listas abrangentes de todos os recursos gerados automaticamente:

>[!BEGINTABS]

>[!TAB iOS]

Para a **Configuração inicial**, abaixo há uma lista abrangente de todos os recursos criados na tela **Detalhes da Configuração** quando você clica em **Criar Recursos Automaticamente**.

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
  <li>Propriedade da tag móvel</li>
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
  <li>Edge Network Adobe Experience Platform</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimento (com políticas de consentimento padrão ativadas)</li>
  <li>Identidade (com ECID padrão, com regras de compilação padrão)</li>
  <li>Núcleo móvel</li>
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
  <p>Sequências de dados</p>
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

Para a **Configuração de canal**, abaixo há uma lista abrangente de todos os recursos criados na tela **Adicionar Canais**.

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
  <li>Configuração de canal</li>
  <li>Fazer upload da credencial de push (somente mensagem de push para dispositivos móveis)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Para a **Configuração inicial**, abaixo há uma lista abrangente de todos os recursos criados na tela **Detalhes da Configuração** quando você clica em **Criar Recursos Automaticamente**.

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
  <li>Propriedade da tag móvel</li>
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
  <li>Edge Network Adobe Experience Platform</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimento (com políticas de consentimento padrão ativadas)</li>
  <li>Identidade (com ECID padrão, com regras de compilação padrão)</li>
  <li>Núcleo móvel</li>
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
  <p>Sequências de dados</p>
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

Para a **Configuração de canal**, abaixo há uma lista abrangente de todos os recursos criados na tela **Adicionar Canais**.

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
  <li>Configuração de canal</li>
  <li>Fazer upload da credencial de push (somente mensagem de push para dispositivos móveis)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Para a **Configuração inicial**, abaixo há uma lista abrangente de todos os recursos criados na tela **Detalhes da Configuração** quando você clica em **Criar Recursos Automaticamente**.

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
  <li>Propriedade da tag móvel</li>
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
  <li>Edge Network Adobe Experience Platform</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consentimento (com políticas de consentimento padrão ativadas)</li>
  <li>Identidade (com ECID padrão, com regras de compilação padrão)</li>
  <li>Núcleo móvel</li>
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
  <p>Sequências de dados</p>
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

