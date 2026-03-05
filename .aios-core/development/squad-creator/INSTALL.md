# Squad Creator Premium — Guia de Instalação

**Versão:** 3.0.0
**Data:** 2026-03-05
**Status:** ✅ Instalado

---

## ✅ O Que Foi Instalado

### 1. **Agents (Elite Minds)**
- `@squad-chief` — Orquestrador mestre de squad creation
- `@oalanicolas` — Mind cloning architect (extração de DNA)
- `@pedro-valerio` — Process absolutist (validação de workflows)

**Localização:** `.aios-core/development/squad-creator/agents/`

### 2. **Skill: `/squad`**
- Nome: `squad`
- Descrição: Master orchestrator para criação de squads
- Modelo: Claude Opus
- Ativação: `/squad` ou `*create-squad`

**Localização:** `.aios-core/development/squad-creator/skills/squad.md`

### 3. **Tasks**
- Pesquisa de mentes elite
- Clonagem de mentes (Voice DNA + Thinking DNA)
- Criação de agentes baseados em mentes reais
- Validação de qualidade

### 4. **Workflows**
- `wf-create-squad.yaml` — Master workflow completo
- `wf-clone-mind.yaml` — Pipeline de clonagem de mentes
- `wf-discover-tools.yaml` — Descoberta de ferramentas

---

## 🎯 Como Usar

### **Opção 1: Via Skill (Recomendado)**

```
/squad
```

O skill será ativado automaticamente quando você mencionar:
- "create squad"
- "want a squad"
- "need experts in"
- "squad de"
- "time de especialistas"

### **Opção 2: Via Agent Command**

```
@squad-chief *create-squad {domínio}
```

Exemplo:
```
@squad-chief *create-squad copywriting
```

### **Opção 3: Via Master Agent**

```
@aios-master *workflow squad-creation
```

---

## 📋 Comandos Disponíveis

| Comando | Descrição |
|---------|-----------|
| `/squad` | Ativar o skill Squad Creator |
| `*create-squad {domain}` | Criar squad completo do zero |
| `*clone-mind {name}` | Clonar uma mente individual |
| `*create-agent` | Criar agente a partir de DNA |
| `*validate-squad` | Validar squad contra quality gates |
| `*refresh-registry` | Atualizar estatísticas do ecossistema |
| `*resume` | Continuar workflow interrompido |
| `*status` | Mostrar estado atual |

---

## 🔧 Configuração dos Slashes

### Para Claude Code (Settings)

Para ativar os slashes `/squad`, `/squad:oalanicolas`, `/squad:pedro-valerio`, adicione ao seu `~/.claude.json`:

```json
{
  "skills": {
    "squad": {
      "enabled": true,
      "path": ".aios-core/development/squad-creator/skills/squad.md",
      "aliases": [
        "/squad",
        "/create-squad"
      ],
      "agents": [
        "squad-chief",
        "oalanicolas",
        "pedro-valerio"
      ]
    }
  }
}
```

### Ou via Command (Alternativa)

Você pode ativar diretamente usando:
```
@squad-chief
```

---

## 📚 Documentação

**Guias Principais:**
- `docs/POR-ONDE-COMECAR.md` — Comece aqui!
- `docs/QUICK-START.md` — Primeiro squad em 5 minutos
- `docs/TUTORIAL-COMPLETO.md` — Exemplo real passo a passo
- `docs/CONCEPTS.md` — Entenda DNA, Tiers, Quality Gates
- `docs/COMMANDS.md` — Referência completa de comandos

**Documentação Técnica:**
- `docs/ARCHITECTURE-DIAGRAMS.md` — Diagramas Mermaid
- `docs/HITL-FLOW.md` — Human-in-the-Loop detalhado
- `docs/TROUBLESHOOTING.md` — Problemas comuns e soluções

---

## 🚀 Quick Start (5 minutos)

### Passo 1: Ativar o Squad Creator
```
@squad-chief
```

### Passo 2: Solicitar um Squad
```
Quero um squad de copywriting
```

### Passo 3: Aprovar as Mentes Pesquisadas
O system vai pesquisar as 5 mentes elite de copywriting e pedir aprovação.

### Passo 4: Squad Criado!
```
✅ Squad created!
- Path: squads/copywriting/
- Agents: 5
- Activate with: /copywriting
```

---

## 📊 Estrutura de Diretórios

```
.aios-core/development/squad-creator/
├── agents/                      # Agentes/mentes
│   ├── squad-chief.md          # Orquestrador principal
│   ├── oalanicolas.md          # Mind cloning specialist
│   └── pedro-valerio.md        # Process validation specialist
├── skills/
│   └── squad.md                # Skill ativável com /squad
├── tasks/                      # Tasks de execução
├── workflows/                  # Workflows (YAML)
├── templates/                  # Templates de agentes
├── scripts/                    # Scripts de suporte
├── config.yaml                 # Configuração
├── README.md                   # Documentação principal
├── CHANGELOG.md                # Histórico de versões
└── INSTALL.md                  # Este arquivo

```

---

## ✨ Features Premium (v3.0)

✅ **Mental Model Integration**
- 46 checkpoints de decisão em 10 tasks
- Consulta VALUES/OBSESSIONS/MODELS/PARADOXES antes de cada decisão

✅ **Deep Tool Discovery**
- Pesquisa profunda e paralela de ferramentas
- Análise relativa de tiers (não valores absolutos)
- Recomendações contextualizadas

✅ **Quality Gates Rigorosos**
- SC_AGT_001: Agent Structure (min 300 linhas)
- SC_AGT_002: Content Completeness
- SC_AGT_003: Depth (frameworks com teoria)

✅ **Voice DNA + Thinking DNA**
- Extração automática de padrões de comunicação
- Extração de frameworks mentais
- Heurísticas de decisão documentadas

---

## 🔄 Próximos Passos

1. **Testar o Squad Creator**
   ```
   @squad-chief
   Quero um squad de {seu-dominio}
   ```

2. **Integrar aos Workflows Existentes**
   - Use `@aios-master *workflow` para integrar com workflows AIOS

3. **Customizar Agents**
   - Edite agents em `agents/` conforme necessário
   - Rode validações com `@squad-chief *validate-squad`

4. **Expandir Mentes**
   - Adicione novas mentes em `minds/`
   - Clone mentes com `@oalanicolas *clone-mind {name}`

---

## ⚙️ Configuração Avançada

### Habilitar Logging Detalhado
Edite `config.yaml`:
```yaml
settings:
  logging:
    enabled: true
    level: debug
    path: .aios/logs/squad-creator.log
```

### Customizar Quality Gates
Edite `tasks/validate-squad.md`:
- Ajuste thresholds de score
- Adicione/remova checkpoints
- Configure veto conditions

### Integrar com Ferramentas Externas
Use `wf-discover-tools.yaml` para pesquisar ferramentas:
- GitHub API para estatísticas
- Package managers (npm, PyPI)
- AI model capabilities

---

## 🆘 Troubleshooting

**Problema:** Skill não aparece com `/squad`

**Solução:**
1. Verifique se `skills/squad.md` existe
2. Reinicie Claude Code
3. Use `@squad-chief` como alternativa

---

**Problema:** Erro ao clonar mente

**Solução:**
1. Verifique conexão com internet (para pesquisa web)
2. Use `@oalanicolas *clone-mind` com nome específico
3. Consulte `docs/TROUBLESHOOTING.md`

---

## 📞 Suporte

- **Docs:** `docs/` folder
- **FAQ:** `docs/FAQ.md`
- **Issues:** `CHANGELOG.md` para histórico de bugs e fixes

---

**Instalação completa! Você está pronto para criar squads de elite.** 🚀

Próximo comando:
```
@squad-chief
```
