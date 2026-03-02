---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Funções compatíveis com o editor de expressão
description: Saiba quais funções do editor de personalização são compatíveis com a Gestão de decisões (Offer Decisioning).
badge: label="Legado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
source-git-commit: 8dcac6e63f6a38874b3aff4996fc317e3606cb9b
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 16%

---

# Funções compatíveis com o editor de expressão {#personalization-editor-supported-functions}

Na Gestão de decisões, você cria expressões usando o editor de personalização. Você usa esse editor especificamente quando:

* **Definindo o conteúdo da oferta** - quando você [adicionar representações](offer-library/add-representations.md) e personalizar o conteúdo da oferta (imagens, texto, links)
* **Criando regras de decisão** - quando você [define a qualificação](offer-library/creating-decision-rules.md) para ofertas
* **Criando fórmulas de classificação** - quando você [cria fórmulas de classificação](ranking/create-ranking-formulas.md) para solicitar ofertas

O back-end do Offer Decisioning dá suporte apenas a **subconjunto** das funções disponíveis no editor de personalização. Esta página lista todas as funções que você pode usar com segurança. Expanda cada seção para ver os operadores, auxiliares e funções compatíveis.

## Lista de funções suportadas {#supported-functions-list}

+++ Operadores

* `+` `-` `*` `/` `%` (aritmética)
* `and` `or` `!` (lógico)
* `=` `!=` `>` `>=` `<` `<=` (comparação)

+++

+++ Auxiliares

* Each
* Com
* Se
* A menos que
* Let
* Valor de fallback padrão
* fragmento
* datasetLookup
* externalDataLookup (Alpha)
* Em linha
* URL
* Metadados de execução
* valueAtPath

+++

+++ Funções de strings

| Nome de exibição | Nome interno |
|--------------|---------------|
| Minúsculas | lowerCase |
| Maiúscula | upperCase |
| Camel case | camelCase |
| Caixa do título | titleCase |
| Aparar | trim |
| Cortar à esquerda | leftTrim |
| Cortar à direita | rightTrim |
| Está vazio | isEmpty |
| Ignorar maiúsculas e minúsculas é igual a | equalsIgnoreCase |
| Diferente de Ignorar Maiúsculas e Minúsculas | notEqualWithIgnoreCase |
| Substituir | replace |
| Substituir tudo | replaceAll |
| Concat | concat |
| Divisão | split |
| Encode64 | encode64 |
| Length | comprimento |
| MD5 | md5 |
| SHA256 | sha256 |
| É como | semelhante |
| Começa com | startsWith |
| Não inicia com | doesNotStartWith |
| Termina com | endsWith |
| Não termina com | doesNotEndWith |
| Contains | contém |
| Não contém | doesNotContain |
| Igual | igual a |
| Não é igual a | notEqualTo |
| Corresponde | matches |
| Grupo de expressão regular | regexGroup |
| Sequência de caracteres para número | stringToNumber |
| Sequência de caracteres para data | stringToDate |
| Para data hora | toDateTime |
| Somente para data e hora | toDateTimeOnly |
| Extrair domínio de email | extractEmailDomain |
| Extrair nome de usuário de email | extractEmailUsername |
| Não Está Vazio | isNotEmpty |
| Índice de | indexOf |
| Último índice de | lastIndexOf |
| Substring | substr |
| Para booleano | toBool |
| Sequência de caracteres para inteiro | string_to_integer |
| Máscara | máscara |
| Obter formato de moeda | formatCurrency |
| Obter valor unicode de caractere | charCodeAt |
| Obter código Qr para qualquer texto | qrCode |

+++

+++ Funções de matriz, lista e definição

| Nome de exibição | Nome interno |
|--------------|---------------|
| Distinto | distinct |
| Entrada | no |
| Não está em | notIn |
| Interseta | cruzamentos |
| Subconjunto de | subsetOf |
| Superconjunto de | supersetOf |
| Inclui | inclui |
| Classificar e obter o primeiro N na matriz | topN |
| Classificar e obter o último N na matriz | bottomN |
| Primeiro item | head |
| Count | contagem |
| Sum | sum |
| Média | média |
| Mínimo | min |
| Máximo | max |

+++

+++ Funções do mapa

| Nome de exibição | Nome interno |
|--------------|---------------|
| Obter | get |
| Chaves | chaves |
| Valores | valores |

+++

+++ Funções do objeto

| Nome de exibição | Nome interno |
|--------------|---------------|
| É nulo | isNull |
| Não é nulo | isNotNull |

+++

+++ Funções matemáticas

| Nome de exibição | Nome interno |
|--------------|---------------|
| Para porcentagem | toPercentage |
| Arredondar para cima | roundUp |
| Arredondar para baixo | roundDown |
| Para precisão | toPrecision |
| Absoluto    | absoluto |
| Aleatória | random |
| Para hexadecimal | toHexString |
| Obter número para localidade | formatNumber |
| Para string | toString |
| Para Int | toInt |
| Para Longo | toLong |

+++

+++ Funções de data e hora

| Nome de exibição | Nome interno |
|--------------|---------------|
| Agora | now |
| Obter CurrentZonedDateTime | getCurrentZonedDateTime |
| Data - Até | toDate |
| Até o horário | toTime |
| Para data hora | toDateTime |
| Somente para data e hora | toDateTimeOnly |
| Somente Até a Data | toDateOnly |
| Somente para horário | toTimeOnly |
| Para Fuso Horário | toTimeZone |
| Formatar data | formatDate |
| Formatar data e hora | formatDateTime |
| Formatar hora | formatTime |
| Data da análise | parseDate |
| Data e hora da análise | parseDateTime |
| Tempo de análise | parseTime |
| Adicionar dias | addDays |
| Adicionar meses | addMonths |
| Adicionar anos | addYears |
| Adicionar Horas | addHours |
| Adicionar Minutos | addMinutes |
| Adicionar segundos | addSeconds |
| Subtrair dias | subtractDays |
| Subtrair meses | subtractMonths |
| Subtrair anos | subtractYears |
| Subtrair Horas | subtractHours |
| Subtrair Minutos | subtractMinutes |
| Subtrair segundos | subtractSeconds |
| Diferença em Dias | diffDays |
| Diferença em meses | diffMonths |
| Diferença em Anos | diffYears |
| Diferença em Horas | diffHours |
| Diferença em Minutos | diffMinutes |
| Diferença em segundos | diffSeconds |
| Início do dia | startOfDay |
| Fim do dia | endOfDay |
| É antes | isBefore |
| É após | isAfter |

+++

+++ Funções de URL

| Nome de exibição | Nome interno |
|--------------|---------------|
| Codificar URL | encodeUrl |
| Decodificar URL | decodeUrl |
| Obter parâmetro de consulta de URL | getUrlQueryParam |
| Obter protocolo de URL | getUrlProtocol |
| Obter host de URL | getUrlHost |

+++

>[!NOTE]
>
>Se você usar uma função que não esteja na lista acima, a expressão poderá falhar no tempo de execução ou produzir resultados inesperados. Para obter o conjunto completo de funções disponíveis na personalização [!DNL Journey Optimizer], consulte [Lista de funções auxiliares](../personalization/functions/functions.md). Somente o subconjunto documentado nesta página é compatível com o Offer Decisioning.
