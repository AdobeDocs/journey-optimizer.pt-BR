---
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 1%

---
# PRD atualizado para o Agente de gerenciamento de página (Agente de estrutura)

## URL da página wikihttps://wiki.corp.adobe.com/display/~simonetn/%3CUC-12%3E+Structure+Agent

&#x200B;---

&#x200B;# &#x200B;1. Resumo

O **Agente de Gerenciamento de Página** (antigo &quot;Agente de Estrutura&quot;) ajuda os autores a reorganizar a documentação com segurança, movendo, excluindo ou renomeando páginas enquanto gerencia automaticamente todos os impactos em todo o repositório.

**Status:** ✅ **IMPLEMENTADO** (v1.5.0 - Lançado em novembro de 2025)

**Meta:** elimine a refatoração manual e propensa a erros da documentação, fornecendo análise de impacto automatizada, execução transparente e verificação abrangente para movimentações, exclusões e renomeações.

JIRA > DOCAC-13695

&#x200B;---

&#x200B;# &#x200B;2. Declaração de problemas

Os repositórios de documentação exigem alterações estruturais frequentes. Estas operações são atualmente **manuais e extremamente propensas a erros**, resultando em:

- **Links internos corrompidos** — mover uma página interrompe todas as referências a ela
- **Links de âncora inválidos** — Os deep links (`page.md#section`) param de funcionar
- **Entradas do sumário desatualizadas** — O sumário se torna inconsistente
- **Redirecionamentos ausentes** — SEO sofre com URLs inválidas
- **Caminhos de imagem quebrados** — Os caminhos de imagem relativos quebram quando as páginas movem pastas
- **Front matter obsoleto** — As referências de página relacionadas ficam desatualizadas
- **Horas de trabalho manual** — Os autores devem preencher, localizar e atualizar os links manualmente

**Exemplo Real:** Mover uma página da pasta `campaigns/` para a pasta `email/` requer atualizar mais de 20 arquivos, levar de 2 a 3 horas e os problemas que estão faltando com frequência.

O **Agente de Gerenciamento de Página** automatiza todo esse processo, concluindo em menos de 1 minuto com 100% de precisão.

&#x200B;---

&#x200B;# &#x200B;3. Objetivos e principais resultados (OKR)

| **Objetivo** | **Resultados principais** | **Status** |
|---------------|-----------------|-----------|
| Automatizar fluxo de trabalho de refatoração completo | 100% dos impactos detectados e atualizados | ✅ **OBTIDO** |
| Eliminar links quebrados | 0 links quebrados após operações | ✅ **OBTIDO** |
| Manter integridade da documentação | Consistência de 100% no índice/redirecionamento | ✅ **OBTIDO** |
| Reduzir o tempo de criação | 95% de redução (3h → 1min) | ✅ **OBTIDO** |
| Operações transparentes | Pré-execução com 100% de visibilidade | ✅ **OBTIDO** |

&#x200B;---

&#x200B;# &#x200B;4. Operações de três núcleos

## 📦 Mover uma página

Realocar página para outra pasta ao atualizar todas as referências:
- Atualiza links internos (absoluto, relativo, relativo à raiz)
- Recalcula os caminhos da imagem para a nova estrutura de pastas
- Atualiza o TOC.md com a nova localização
- Adiciona redirecionamento em redirects.csv
- Atualiza as referências principais
- Valida todos os links âncora

## 🗑️ Excluir uma página

Remova a página com gerenciamento de impacto abrangente:
- Identifica todas as páginas vinculadas à página excluída
- Opcionalmente, configura o redirecionamento para a página de substituição
- Remove a entrada do TOC.md
- Avisa sobre links com falha se nenhum redirecionamento for fornecido
- Limpa as referências da matéria inicial

## ✏️ Renomear uma página

Alterar nome de arquivo ao manter na mesma pasta:
- Atualiza todas as referências para usar o novo nome de arquivo
- Atualiza a entrada TOC.md
- Adiciona redirecionamento para continuidade de SEO
- Mantém todos os links âncora
- Atualiza referências de página relacionadas

&#x200B;---

&#x200B;# &#x200B;5. Fluxo de trabalho (16 etapas)

| **Etapa** | **Ação** | **Detalhes** |
|----------|-----------|-------------|
| &#x200B;1. Invocação | Tipos de usuário `@page-management` | Carregamento instantâneo do agente |
| &#x200B;2. Verificação do repositório | Analisar estrutura | Contar arquivos, localizar sumário/redirecionamentos, criar gráfico de links |
| &#x200B;3. Seleção da operação | Escolher mover/excluir/renomear | Menu interativo |
| &#x200B;4. Coleta de caminhos | Obter origem e destino | Validar caminhos |
| &#x200B;5. Análise de impacto | Verificação abrangente | grep + pesquisa semântica para todas as referências |
| &#x200B;6. Relatório de impacto | Detalhado antes/depois | Caminhos de arquivo, números de linha, alterações |
| &#x200B;7. Confirmação do usuário | Aprovação explícita necessária | Sim/Não/Modificar |
| &#x200B;8. Operação de arquivo | Mover/excluir/renomear arquivo | Operação do sistema de arquivos |
| &#x200B;9. Atualizações de link | Atualizar todos os links | Links internos e de âncora |
| &#x200B;10. Atualização do sumário | Atualizar sumário | Preservar hierarquia |
| &#x200B;11. Gerenciamento de redirecionamento | Adicionar a redirects.csv | Para SEO |
| &#x200B;12. Atualização do caminho da imagem | Recalcular caminhos (apenas movimentações) | Manter resolução da imagem |
| &#x200B;13. Atualização do Front Matter | Atualizar referências YAML | Páginas relacionadas, pré-requisitos |
| &#x200B;14. Verificação | Validar todas as alterações | Verificar se há links desfeitos |
| &#x200B;15. Preparação da Confirmação | Gerar mensagem de confirmação | Resumo detalhado com estatísticas |
| &#x200B;16. Estágios opcionais | Adição de Git, se solicitado | Recurso de conveniência |

&#x200B;---

&#x200B;# &#x200B;6. Requisitos funcionais

| **ID** | **Requisito** | **Prioridade** | **Status** |
|--------|----------------|-------------|-----------|
| FR-1 | Suporte a operações de Mover, Excluir e Renomear | P1 | ✅ Implementado |
| FR-2 | Detectar todos os links internos (absoluto, relativo, relativo à raiz) | P1 | ✅ Implementado |
| FR-3 | Validar e atualizar links de âncora | P1 | ✅ Implementado |
| FR-4 | Atualizar o TOC.md automaticamente | P1 | ✅ Implementado |
| FR-5 | Gerenciar redirects.csv para SEO | P1 | ✅ Implementado |
| FR-6 | Recalcular caminhos de imagem ao mover páginas | P1 | ✅ Implementado |
| FR-7 | Atualizar referências de front matter | P1 | ✅ Implementado |
| FR-8 | Gerar relatório de impacto abrangente | P1 | ✅ Implementado |
| FR-9 | Fornecer antes/depois da visualização | P1 | ✅ Implementado |
| FR-10 | Exigir confirmação explícita do usuário | P1 | ✅ Implementado |
| FR-11 | Mostrar progresso transparente | P1 | ✅ Implementado |
| FR-12 | Verificar todas as alterações | P1 | ✅ Implementado |

&#x200B;---

&#x200B;# &#x200B;7. Execução Técnica

## Algoritmo de detecção de link

Abordagem multiestratégia:
- **Padrão Regex:** `\[([^\]]+)\]\(([^)]+\.md(?:#[^)]*)?)\)`
- **Identificadores:** caminhos absolutos, relativos, relativos à raiz + âncoras
- **Ferramentas:** grep (correspondência exata) + codebase_search (semântica)

## Resolução do caminho

Algoritmo inteligente:
1. Obter diretório de arquivo de link
2. Resolver em relação ao caminho absoluto
3. Normalizar caminhos (remover `./`, resolver `..`)
4. Comparar com caminho de destino
5. Calcular novo caminho relativo para destino

## Recálculo do caminho da imagem

Ao mover páginas entre pastas, recalcula os caminhos relativos para manter a resolução de imagem correta.

**Exemplo:**

```
Original:  help/using/campaigns/page.md
Image:     ![](assets/image.png)
Resolves:  help/using/campaigns/assets/image.png

Moving to: help/using/email/page.md
New image: ![](../campaigns/assets/image.png)
Resolves:  help/using/campaigns/assets/image.png ✅
```

&#x200B;---

&#x200B;# &#x200B;8. Formato do relatório de impacto

Relatório abrangente que mostra:

1. **Resumo da Operação** — Source, destino, tipo
2. **Tabela de Resumo de Impacto** — Contagem de cada tipo de impacto
3. **Links Internos** — Arquivo, linha, antes/depois de cada link
4. **Links de Âncora** — Links profundos com referências de seção
5. **Atualizações do índice** — Alterações no índice
6. **Redirecionamentos** — Novas entradas de redirecionamento
7. **Caminhos de imagem** — Referências de imagem atualizadas (para movimentações)
8. **Front Matter** — Atualizações de referência de metadados
9. **Problemas em potencial** — Avisos
10. **Plano de Execução** — visualização passo a passo

**Exemplo de Relatório de Impacto:**
- 23 links internos atualizados em 15 arquivos
- 5 links de âncora atualizados
- 1 entrada do índice atualizada
- 1 redirecionamento adicionado
- 4 caminhos de imagem recalculados
- 2 referências principais atualizadas
- **Total: 18 arquivos modificados em ~30 segundos**

&#x200B;---

&#x200B;# &#x200B;9. Requisitos não funcionais

| **Categoria** | **Requisito** | **Atingido** |
|--------------|----------------|-------------|
| **Desempenho** | Conclua em 60 segundos | ✅ 30-45 segundos |
| **Precisão** | 100% de detecção | ✅ 100% |
| **Escalabilidade** | Lidar com milhares de páginas | Mais de ✅ 500 testados |
| **Transparência** | Mostrar todas as alterações | ✅ Concluir visualização |
| **Segurança** | Nenhuma perda de dados | ✅ Confirmação explícita |
| **Verificação** | Validar alterações | ✅ Verificações automatizadas |
| **Auditabilidade** | Concluir log de alterações | ✅ Confirmações detalhadas |

&#x200B;---

&#x200B;# &#x200B;10. Métricas de sucesso

## Quantitativo- **Economia de tempo:** redução de 95% (2 a 3 horas → &lt;1 minuto)- **Precisão:** 100% das referências detectadas e atualizadas- **Confiabilidade:** 0 links desfeitos após a refatoração- **Desempenho:** 30-45 segundos para operações típicas- **Cobertura:** 7 tipos de impacto analisados

## Qualitative- ✅ Autores podem refatorar com confiança- ✅ Transparência completa- ✅ Controle de segurança explícito- ✅ Nenhuma limpeza manual necessária- ✅ Auditabilidade completa

&#x200B;---

&#x200B;# &#x200B;11. Riscos e atenuações

| **Risco** | **Impacto** | **Mitigação** |
|----------|-----------|---------------|
| Cálculos de caminho incorretos | Links quebrados | ✅ Algoritmo abrangente + verificação |
| Referências perdidas | Links quebrados em casos de borda | ✅ Pesquisa multiestratégia (grep + semântica) |
| Execução sem revisão | Alterações não intencionais | ✅ Confirmação obrigatória necessária |
| Conflitos de arquivo | Perda ou substituição de dados | ✅ Verificações de conflitos antes da migração |
| Alterações não confirmadas | Trabalho em andamento perdido | ✅ aviso de árvore de trabalho suja |
| Caminhos relativos complexos | Referências de imagem corrompidas | ✅ Resolução de caminho testada |
| Operações em larga escala | Atualizações incompletas | ✅ Algoritmos eficientes |

&#x200B;---

&#x200B;# &#x200B;12. Instruções de utilização

## Início rápido

```
@page-management
```

## Comandos de linguagem natural

```
move a page
delete a page
rename a page
refactor documentation
```

## Exemplo de sessão

```
User: @page-management

Agent: 🔧 Page Management Agent
       [Scans repository...]
       ✅ Found 487 Markdown files
       
       What would you like to do?
       1. Move a page
       2. Delete a page
       3. Rename a page

User: 1

Agent: Which page do you want to move?

User: help/using/campaigns/setup.md

Agent: Where should it go?

User: help/using/email/setup.md

Agent: [Analyzes impacts...]
       📊 Impact Report:
       - 23 internal links → update needed
       - 5 anchor links → update needed
       - 1 TOC entry → update needed
       - 4 image paths → update needed
       Total: 18 files will be modified
       
       Proceed? (Yes/No)

User: Yes

Agent: ✅ Complete! All changes verified.
       Ready to commit.
```

&#x200B;---

&#x200B;# &#x200B;13. Melhorias futuras

**Recursos Planejados:**
- Operações em lote (mover/renomear várias páginas)
- Modo de simulação (mostrar impactos sem execução)
- Recurso de desfazer/reverter
- Sugestões de mesclagem inteligente ao excluir
- Vincular atualizações de texto quando o título for alterado
- Movimentação de ativos (mover imagens com a página)
- Tratamento de links entre repositórios
- Opção de confirmação automática
- Visualização do Diff
- Exportar relatórios de impacto

&#x200B;---

&#x200B;# &#x200B;14. Documentação e recursos

- **Arquivo do Agente:** `.cursor-agents/agents/page-management-agent.md`
- **Referência rápida:** `.cursor-agents/AGENTS.md`
- **Versão:** 1.5.0 (novembro de 2025)
- **Repositório:** `git@git.corp.adobe.com:AdobeDocs/CursorAgents.git`

**Documentação adicional:**
- Guia de Instalação: `INSTALL.md`
- Solução de problemas: `TROUBLESHOOTING.md`
- Todos os Agentes: `AGENTS.md`

&#x200B;---

&#x200B;# &#x200B;15. Notas de versão

## v1.5.0 (novembro de 2025) — Versão inicial- ✅ Concluir a implementação das operações Mover/Excluir/Renomear- ✅ Análise de impacto abrangente (7 tipos de referência)- ✅ Execução transparente com acompanhamento de progresso- ✅ Verificação e validação automatizadas- ✅ Geração detalhada da mensagem de confirmação- ✅ Verificação de versão silenciosa- ✅ Política de novo início (sem sangria de contexto)

## Limitações conhecidas- Somente operações de página única (lote em breve)- Exige árvore de trabalho limpa para segurança (aviso fornecido)- Confirmação manual necessária (confirmação automática em breve)

&#x200B;---

*Última atualização: 6 de novembro de 2025*

