---
solution: Journey Optimizer
product: journey optimizer
title: Testar uma ação personalizada
description: Saiba como solucionar problemas de uma ação personalizada
badge: label="Disponibilidade limitada"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, third-party, custom, jornada, API
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 2%

---


# Solução de problemas de ações personalizadas {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Esse recurso só está disponível para algumas organizações (disponibilidade limitada). Para obter acesso, entre em contato com seu representante da Adobe.
>

## Visão geral

O recurso **Enviar Solicitação de Teste** permite que os administradores validem suas configurações de ação personalizadas fazendo chamadas de API reais diretamente do Adobe Journey Optimizer (AJO). Esse recurso garante que a estrutura de solicitação, os cabeçalhos, a autenticação e a carga sejam formatados corretamente antes de serem usados em uma jornada.

![](assets/send-test-request.png){width="70%" align="left"}

## Pré-requisitos

- **Acesso de Administrador Necessário:**
   - Os usuários devem ter a permissão **&quot;Gerenciar eventos, fontes de dados e ações do jornada&quot;**.
   - Esta permissão está incluída na função *Administradores do Jornada*.
   - A permissão **&quot;Exibir eventos do jornada...&quot;** sozinha não é suficiente.
- Uma **Ação Personalizada** deve ser pré-configurada com uma URL, cabeçalhos e configurações de autenticação.

## Como usar o recurso Enviar solicitação de teste

1. Navegue até a tela de configuração **Ações Personalizadas**.
1. Clique no botão **&quot;Enviar Solicitação de Teste&quot;**.
1. Uma janela pop-up é exibida, permitindo especificar os parâmetros de solicitação:
   - Se o método de ação personalizada **for GET**, nenhuma carga será necessária.
   - Se o método de ação personalizado **for POST**, você deverá fornecer uma carga JSON.

     >[!NOTE]
     >
     >O AJO levantará um erro se a estrutura desse JSON estiver incorreta, mas não o fará se houver uma incompatibilidade com um tipo de dados. Por exemplo, não haverá erro se um parâmetro inteiro for usado para o que deve ser uma string.

   - Se a autenticação estiver definida, você será solicitado a inserir detalhes de autenticação.

1. Clique em **Enviar** para executar a solicitação.
1. A resposta da API, incluindo cabeçalhos e códigos de status, será exibida na interface.

## Tratamento de autenticação

Quando uma ação personalizada inclui autenticação, o AJO exige que o usuário insira detalhes de autenticação para cada solicitação de teste:

- **Autenticação Básica**: o usuário deve fornecer a *senha*.
- **Autenticação da Chave de API:** o usuário deve inserir a chave de API *value*.
- **Autenticação Personalizada**: o usuário deve fornecer os parâmetros de autenticação na solicitação *bodyParam*. Duas seções para conclusão foram adicionadas neste caso: **Solicitação de autenticação** e **Resposta de autenticação**.

## Principais diferenças das ferramentas de teste externas (por exemplo, Postman)

- A solicitação de teste é executada por **Jornada AJO**, significando:
   - A estrutura de solicitação exata (incluindo cabeçalhos específicos do AJO) é usada.
   - O IP de origem e os cabeçalhos correspondem àqueles usados nas jornadas ativas.
- Pode ser usado para solucionar problemas de **jornadas ao vivo** em que a ação personalizada já foi implantada.
- Elimina a necessidade de copiar manualmente os detalhes de configuração entre as ferramentas, reduzindo o risco de erros.

## Solução de problemas

- Se a solicitação falhar, verifique:
   - As credenciais de autenticação inseridas no teste.
   - O método de solicitação (GET vs. POST) e a carga útil correspondente.
   - O endpoint da API e os cabeçalhos definidos na ação personalizada.
- Use os dados de resposta para identificar possíveis erros de configuração.

Esse recurso simplifica o processo de teste e validação, garantindo que as ações personalizadas funcionem corretamente nas jornadas ativas do AJO.

