# Zona Genialidade — Guia de Instalação

**Versão:** 1.0.0
**Data:** 2026-03-05
**Status:** ✅ Instalado

---

## ✅ O Que Foi Instalado

### 1. **Agents (8 Elite Minds)**
- `@zona-genialidade-chief` — Orquestrador principal
- `@gay-hendricks` — Zone of Genius diagnostician
- `@don-clifton` — CliftonStrengths analyst
- `@dan-sullivan` — Unique Ability strategist
- `@roger-hamilton` — Wealth Dynamics expert
- `@alex-hormozi` — Monetization specialist
- `@kathy-kolbe` — Execution style analyst
- `@sally-hogshead` — Positioning & fascination expert

**Localização:** `.aios-core/development/zona-genialidade/agents/`

### 2. **Skill: `/ZonaGenialidade`**
- Nome: `zona-genialidade`
- Descrição: Discover your Genius Zone through integrated assessment
- Modelo: Claude Opus
- Ativação: `/ZonaGenialidade` ou `*start`

**Localização:** `.aios-core/development/zona-genialidade/skills/zona-genialidade.md`

### 3. **Tasks (5)**
- `start` — Pipeline completo (assessment → analysis → matching → blueprint)
- `run-assessment` — Assessment integrado de 30 min
- `analyze-genius-profile` — Análise multi-framework
- `recommend-squad` — Recomendação de squad
- `generate-blueprint` — Blueprint final

### 4. **Knowledge Base**
- Frameworks de 7 elite minds
- Assessment templates
- Example blueprints

---

## 🎯 Como Usar

### **Opção 1: Via Skill (Recomendado)**

```
/ZonaGenialidade
```

O skill será ativado automaticamente quando você mencionar:
- "genius zone"
- "zona de genialidade"
- "discover my strengths"
- "descubra meu potencial"
- "qual squad criar"
- "monetization"

### **Opção 2: Via Agent Command**

```
@zona-genialidade-chief *start
```

### **Opção 3: Via Master Agent**

```
@aios-master *workflow zona-genialidade-discovery
```

---

## 📋 Fluxo Completo (30 minutos)

### **Etapa 1: Assessment Integrado (5-8 min)**
Responda ~43 perguntas que alimentam TODOS os 7 frameworks simultaneamente:
- Contexto pessoal
- Atividades e energia
- Talentos e padrões
- Estilo de negócios
- Visão e ambição

### **Etapa 2: Análise Multi-Framework (5-10 min - Automática)**
7 agentes analisam seus dados em paralelo:
```
Dados do Assessment
    ├── Gay Hendricks    → Zona atual + Upper Limit Problem
    ├── Don Clifton      → Top 5 talentos + domínio
    ├── Dan Sullivan     → Unique Ability + delegação
    ├── Roger Hamilton   → Wealth Profile + squad match
    ├── Alex Hormozi     → Value Equation + monetização
    ├── Kathy Kolbe      → Action Modes + execução
    └── Sally Hogshead   → Arquétipo + posicionamento
```

### **Etapa 3: Matching (2-3 min - Automático)**
Algoritmo de matching recomenda:
- Squad ideal para criar/operar
- Modelos de monetização
- Próximos passos

### **Etapa 4: Blueprint (Entrega)**
Documento com 10 seções:
1. Perfil em 30 Segundos
2. Diagnóstico de Zona
3. Mapa de Talentos
4. Habilidade Única
5. Perfil de Riqueza
6. Squad Recomendado
7. Plano de Monetização
8. Estilo de Execução
9. Posicionamento
10. Próximos Passos

---

## ⚡ Comandos Disponíveis

| Comando | Descrição |
|---------|-----------|
| `/ZonaGenialidade` | Ativar skill completo |
| `/ZG:start` | Pipeline completo (alias curto) |
| `/ZG:hendricks` | Gay Hendricks specialist |
| `/ZG:clifton` | Don Clifton specialist |
| `/ZG:sullivan` | Dan Sullivan specialist |
| `/ZG:hamilton` | Roger Hamilton specialist |
| `/ZG:hormozi` | Alex Hormozi specialist |
| `/ZG:kolbe` | Kathy Kolbe specialist |
| `/ZG:hogshead` | Sally Hogshead specialist |

---

### Via Agent
```
@zona-genialidade-chief *start
@zona-genialidade-chief *assess
@zona-genialidade-chief *analyze
@zona-genialidade-chief *recommend-squad
@zona-genialidade-chief *blueprint
@zona-genialidade-chief *help
```

---

## 📊 Estrutura de Diretórios

```
.aios-core/development/zona-genialidade/
├── agents/                          # 8 Agentes especialistas
│   ├── zona-genialidade-chief.md    # Orquestrador
│   ├── gay-hendricks.md             # Zone of Genius
│   ├── don-clifton.md               # CliftonStrengths
│   ├── dan-sullivan.md              # Unique Ability
│   ├── roger-hamilton.md            # Wealth Dynamics
│   ├── alex-hormozi.md              # Monetization
│   ├── kathy-kolbe.md               # Action Modes
│   └── sally-hogshead.md            # Fascination
├── skills/
│   └── zona-genialidade.md          # Skill ativável
├── tasks/                           # 5 Tasks executáveis
│   ├── start.md
│   ├── run-assessment.md
│   ├── analyze-genius-profile.md
│   ├── recommend-squad.md
│   └── generate-blueprint.md
├── workflows/                       # Workflows YAML
├── checklists/                      # Quality gates
├── data/                            # Knowledge base
│   ├── zona-genialidade-kb.md
│   └── examples/
├── config.yaml                      # Configuração
├── README.md                        # Documentação
└── INSTALL.md                       # Este arquivo
```

---

## 🔧 Configuração dos Slashes

### Para Claude Code

Os slashes `/ZonaGenialidade` e `/ZG:*` estão registrados em `.claude/skills-registry.json`:

```json
{
  "skills": {
    "zona-genialidade": {
      "slashCommands": [
        "/ZonaGenialidade",
        "/ZG:start",
        "/ZG:hendricks",
        "/ZG:clifton",
        "/ZG:sullivan",
        "/ZG:hamilton",
        "/ZG:hormozi",
        "/ZG:kolbe",
        "/ZG:hogshead"
      ]
    }
  }
}
```

---

## ✨ Frameworks Inclusos

| Framework | Expert | Aplicação |
|-----------|--------|-----------|
| **Zone of Genius** | Gay Hendricks | Identificar zona de excelência |
| **CliftonStrengths 34** | Don Clifton | Mapear talentos |
| **Unique Ability** | Dan Sullivan | Encontrar habilidade única |
| **Wealth Dynamics** | Roger Hamilton | Perfil empreendedor → Squad match |
| **Value Equation** | Alex Hormozi | Monetização e pricing |
| **Kolbe Action Modes** | Kathy Kolbe | Estilo de execução |
| **Fascination Advantage** | Sally Hogshead | Posicionamento pessoal |

---

## 🎯 Use Cases

### **UC1: Diagnóstico Comportamental**
Descubra seu perfil integrado (DISC, Enneagram, CliftonStrengths, Big Five)

**Comando:**
```
@zona-genialidade-chief *run-assessment
```

### **UC2: Mapeamento Zona de Genialidade**
Cruzar perfil com habilidades, paixões e oportunidades de mercado

**Comando:**
```
@zona-genialidade-chief *analyze-genius-profile
```

### **UC3: Recomendação de Squad**
Qual squad criar/operar baseado no seu perfil

**Comando:**
```
@zona-genialidade-chief *recommend-squad
```

### **UC4: Plano de Monetização**
Como transformar sua zona de genialidade em receita

**Comando:**
```
@zona-genialidade-chief *generate-blueprint
```

---

## 🔄 Próximos Passos

1. **Executar Pipeline Completo**
   ```
   /ZonaGenialidade
   ```

2. **Integrar com Squad Creator**
   - Use o squad recomendado como input para `@squad-chief`
   - Crie o squad da sua zona de genialidade

3. **Implementar Plano**
   - Use o blueprint para guiar seus próximos 90 dias
   - Agende mentorias com especialistas (se aplicável)

4. **Monitorar Progresso**
   - Re-execute assessment em 6 meses
   - Compare mudanças no seu perfil
   - Ajuste squad e monetização conforme necessário

---

## 🆘 Troubleshooting

**Problema:** Skill não aparece com `/ZonaGenialidade`

**Solução:**
1. Verifique se `skills/zona-genialidade.md` existe
2. Reinicie Claude Code
3. Use `@zona-genialidade-chief` como alternativa

---

**Problema:** Assessment incompleto

**Solução:**
1. Responda todas as ~43 perguntas
2. Use `*resume` para continuar
3. Verifique conexão com internet (para buscar dados)

---

**Problema:** Análise não converge

**Solução:**
1. Aguarde análise dos 7 agentes (5-10 min)
2. Verifique logs em `.aios/logs/zona-genialidade.log`
3. Re-execute com `@zona-genialidade-chief *analyze-genius-profile`

---

## 📞 Suporte

- **Documentação:** `.aios-core/development/zona-genialidade/` folder
- **Exemplos:** `data/examples/` para blueprints de referência
- **Issues:** Consulte `README.md` para troubleshooting detalhado

---

## 🎁 Bônus: Integração com Squad Creator

Após descobrir sua zona de genialidade, use o squad recomendado com `@squad-chief`:

```
@squad-chief *create-squad {domain-from-blueprint}
```

Seu squad de genialidade será criado automaticamente com base no seu perfil!

---

**Instalação completa! Você está pronto para descobrir sua zona de genialidade.** 🧠

Próximo comando:
```
/ZonaGenialidade
```
