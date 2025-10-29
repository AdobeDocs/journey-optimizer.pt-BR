---
source-git-commit: d7bb3424bc6dfb837b47d15c448a2d46bf4b6c3c
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---
# 🚀 Instalando Agentes de Cursor

Os agentes de cursor são ferramentas compartilhadas que ajudam você a criar e manter a documentação com mais eficiência.

## Configuração pela primeira vez

Você só precisa fazer isso **uma vez** por repositório.

### Opção 1: Usando Cursor (Recomendado ⭐)

1. Abrir Chat do Cursor (`Cmd+L` ou `Ctrl+L`)
2. Tipo:

   ```
   @setup-agents
   ```
3. Siga as instruções
4. Concluído! ✨

### Opção 2: usar o terminal

1. Abra o terminal na raiz do repositório
2. Executar:

   ```bash
   ./setup-agents.sh
   ```
   Ou manualmente:

   ```bash
   git submodule update --init --recursive
   ```
3. Concluído! ✨

## Verificação

Após a instalação, verifique a instalação:

```bash
ls .cursor-agents/agents/
```

Você deve ver:
- `draft-page-generator.md`
- `fix-grammar.md`
- etc.

## Uso

Depois de instalado, você pode usar agentes no Cursor:

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

Consulte `.cursor-agents/AGENTS.md` para obter uma lista completa dos agentes disponíveis.

## Atualizando agentes

Para obter a versão mais recente de todos os agentes:

### Opção 1: Uso do Cursor

```
@update-agents
```

### Opção 2: usar o terminal

```bash
git submodule update --remote
```

## Resolução de problemas

### Erro &quot;Agente não encontrado&quot;

Se você vir esse erro, os agentes ainda não estão instalados. Executar:

```
@setup-agents
```

### O submódulo está vazio

Se `.cursor-agents/` existe mas está vazio:

```bash
git submodule update --init --recursive --remote
```

### Permissão negada

Verifique se o script de configuração é executável:

```bash
chmod +x setup-agents.sh
```

### Problemas de rede/VPN

- Verifique se você está conectado à Adobe VPN
- Verificar conectividade de rede
- Verificar acesso ao Git:

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## Como funciona

Os Agentes de Cursor são distribuídos como um **submódulo Git**:

```
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

O submódulo aponta para:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Isso garante que todos usem os mesmos agentes atualizados.

---

**Precisa de ajuda?** Contate o líder da sua equipe de documentação ou verifique a wiki interna.

