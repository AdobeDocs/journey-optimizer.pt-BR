---
solution: Journey Optimizer
product: journey optimizer
title: Gerenciar recusa
description: Saiba como gerenciar opções de rejeição e privacidade
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: f5390bbb3bab435b21ace4d1842de0048132bc8c
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 1%

---

# Implementar consentimento para opção de não participação para personalização {#cpes-opt-out}


## Editor de expressão

Editor de expressões ao personalizar imagens, texto, linha de assunto ( Segmento em campanhas) - interface e headless

O editor de personalização em si não executa verificações de consentimento ou imposição, pois não está envolvido na entrega de ações de mensagem. O editor de personalização segue os rótulos de controle de acesso com base em direitos fornecidos pelo serviço de perfil unificado para permitir/proibir que diferentes campos sejam usados para personalização. O serviço de visualização e renderização de mensagens mascarará os campos identificados com informações confidenciais.

Em Campanhas do AJO, a aplicação da política de consentimento pode ocorrer em dois lugares. Os clientes podem incluir definições de política de consentimento como parte da criação do público ou segmento para garantir que o público selecionado para a campanha já tenha filtrado os perfis que não correspondem aos critérios de consentimento. Além disso, o serviço de tempo de execução da mensagem executará uma verificação de consentimento geral no nível do canal para garantir que os perfis tenham aceitado receber comunicações de marketing no canal específico. O objeto da campanha do AJO em si não executa verificações adicionais de aplicação de política de consentimento no momento.

Etapas de campanha e personalização do AJO para impor o consentimento manualmente:

O status de aceitação e as preferências de personalização de um usuário devem fazer parte das regras e da definição de público-alvo antes da ativação em uma campanha do Journey Optimizer. Um usuário de marketing no Adobe Experience Platform pode adicionar uma verificação de consentimento ao público-alvo criando uma nova composição de público-alvo ou definindo um novo segmento usando o construtor de regras.

Se estiver usando o Audience Composer, você pode dividir o público usando atributos de perfil. Depois de fazer as seleções nos atributos de consentimento apropriados que deseja verificar, você pode salvar os públicos resultantes para ativação em uma campanha. Lembre-se de que, se você criar um público-alvo que não consentiu com a personalização e depois selecionar esse público para ativação em uma campanha, as ferramentas de personalização permanecerão disponíveis. Cabe ao usuário de marketing entender que, se estiver trabalhando com um público-alvo que não deve receber personalização, ele não deve usar ferramentas de personalização.

Para criar um público-alvo dividido na composição do público-alvo, siga estas etapas:

1. Selecione o público inicial.

1. Clique no ícone de adição para criar um público-alvo dividido.

1. Nas propriedades de Divisão, escolha &quot;divisão de atributo&quot; como tipo.

1. No campo de atributo, clique no ícone de lápis para abrir a janela de seleção de atributo.

1. Digite no valor Opção para pesquisar o atributo de consentimento de personalização (observe que esse será o caminho do atributo profile.consentients.personalize.content.val

1. Selecione este atributo.

1. No Caminho 1 - escolha um rótulo para ajudar a definir o público-alvo não personalizado.

1. Escolha o valor apropriado na lista: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=en#choice-values

   Nesse caso, usaremos um &quot;n&quot; para indicar NÃO como recusa da personalização

   Você pode criar um caminho separado para outros valores de opção ou optar por excluir caminhos restantes e ativar &quot;outros perfis&quot;, o que incluiria todos os outros perfis que não tinham um valor de opção de &quot;n&quot;.

1. Depois de concluir, clique na caixa onde está escrito &quot;Salvar público-alvo&quot;. Uma nova janela de propriedades será aberta, permitindo escolher qual nome deseja usar para os públicos derivados.

1. Depois de concluído, publique a composição do público-alvo.

Se estiver usando o construtor de regras de segmento para criar seu público-alvo, você poderá selecionar opções de valor de personalização e consentimento como parâmetros de exclusão na definição do público-alvo. Ao adicionar os parâmetros de exclusão, é possível criar um único segmento de público-alvo de perfis onde os indivíduos que não consentiram são filtrados.

