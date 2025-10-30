---
source-git-commit: 505810d58d7db1682cc434b0df6d1ec5f5edd23e
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

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
3. O agente irá automaticamente:
   - Testar acesso SSH e HTTPS
   - Usar o método de trabalho
   - Orientar você durante a configuração, se necessário
4. Concluído! ✨

**Observação:** o agente detecta automaticamente se você tem acesso SSH ou HTTPS a `git.corp.adobe.com` e usa o método apropriado. Se nenhum funcionar, ele fornece uma configuração guiada.

### Opção 2: usar o terminal

1. Abra o terminal na raiz do repositório
2. Executar:

   ```bash
   ./setup-agents.sh
   ```

   O script irá automaticamente:
   - Testar acesso SSH e HTTPS
   - Usar o método de trabalho
   - Mostrar instruções de configuração, se necessário

   Ou manualmente (se você souber que o Git está configurado):

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

Consulte [AGENTS.md](AGENTS.md) para obter uma lista completa dos agentes disponíveis.

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
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

O submódulo aponta para:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Isso garante que todos usem os mesmos agentes atualizados.

## Para mantenedores

### Adicionar a um novo repositório

1. Adicione o submódulo:

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. Copiar arquivos de configuração:
   - `setup-agents.sh`
   - `setup-agent.md` (colocar na raiz, não no submódulo)
   - `INSTALL.md`

3. Confirmar:

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### Atualização do repositório central

As alterações nos agentes devem ser feitas em:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Todos os repositórios receberão atualizações via `git submodule update --remote`.

---

**Precisa de ajuda?** Contate o líder da sua equipe de documentação ou verifique a wiki interna.
