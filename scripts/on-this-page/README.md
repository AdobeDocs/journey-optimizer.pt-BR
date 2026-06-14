---
source-git-commit: f59dc265b0de732b52e9d26b6ee510733d0d760e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---
# Ferramenta de caixa &quot;Nesta página&quot;

Ferramenta para adicionar e verificar o padrão **&quot;Nesta página&quot;** caixa sombreada na parte superior de
Páginas de documentação do AJO. Consulte a especificação em `.cursor/rules/on-this-page-box.mdc`.
A implantação é acompanhada em epic **DOCAC-14936** (uma tarefa por pasta de nível superior).

## Como a caixa se parece

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## Fluxo de trabalho recomendado (por pasta/tarefa Jira)

Executar da raiz do repositório (`journey-optimizer.en/`).

1. **Inserir caixas** (propagando uma frase de primeiro rascunho do primeiro assunto de cada página
   `description`). Mecânico, idempotente, nunca toca na matéria dianteira:

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   Visualizar primeiro com `--dry-run`.

2. **Refine a redação.** A semente é um ponto de partida — edite cada frase para que ela
O é lido como uma declaração de finalidade (uma frase, texto simples, inglês americano). **Lead
com o por quê**: declare o resultado/benefício do leitor (&quot;...para que você possa &lt;outcome>&quot;), não
apenas uma lista do que a página cobre. Combinar nomes de recursos de estilo doméstico (por exemplo,
&quot;Campanha orquestrada&quot;, &quot;No aplicativo&quot;). Consulte `.cursor/rules/on-this-page-box.mdc`. Se você
ignorar `--seed-from-description`, um espaço reservado de `{{TODO...}}` é inserido e
o validador sinalizará qualquer item restante.

3. **Validar** antes de abrir a PR:

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   O código de saída é diferente de zero em qualquer falha, portanto, pode comportar o CI.

## Escopo/exclusões

Páginas de referência e sintaxe são excluídas por padrão (partes do caminho `api-reference`,
`expression`, `functions`). Substituir por `--exclude ...`, se necessário.

## Verificação de progresso em todo o repositório

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

Sem o `--require`, as páginas com uma caixa faltando são reportadas como `pending` (não como
falha), para que você possa acompanhar o progresso da implantação no guia.
