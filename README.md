# Claude Skills & Agents — Suite UX/UI & Anti-AI Slop

Coleção personalizada de agentes e skills para **Claude Code**, focada em eliminação do visual padrão genérico de IA (*AI Design Slop*), engenharia de Design Systems e direção de arte contextualizada.

---

## 📦 Conteúdo do Repositório

### 1. 🤖 Agente: `ux-ui-specialist`
- **Arquivo:** `agents/ux-ui-specialist.md` (e `.claude/agents/ux-ui-specialist.md`)
- **Descrição:** Especialista sênior em UX/UI, Design Systems e Engenharia Frontend. Orquestra as principais skills de design (`impeccable`, `frontend-design`, `dataviz`, `anti-ai-slop-ui`) com protocolo de 5 etapas para erradicar o visual genérico gerado por IA.
- **Ferramentas:** `Read`, `Write`, `Edit`, `Bash`, `Glob`, `Grep`

### 2. 🎯 Skill: `anti-ai-slop-ui`
- **Arquivo:** `skills/anti-ai-slop-ui/SKILL.md` (e `.claude/skills/anti-ai-slop-ui/SKILL.md`)
- **Descrição:** Diretrizes estritas e checklist de auditoria visual:
  - **Lista Negra do "AI Slop":** Banimento de eyebrows em caixa alta desnecessários, paletas clichês ("creme + terracota" ou "dark neon"), "SaaS card trap", títulos com palavras isoladas em gradiente, glow blobs nos cantos e botões com setas obrigatórias `→`.
  - **Matriz de Decisão Estética:** Mapeamento do domínio do produto (Industrial/Regulatório, Fintech/B2B, Overlays/Modais, DevTools/CLI, Editorial/Docs, Neobrutalismo) para o arquétipo visual adequado.
  - **Padrões Técnicos:** Tokens semânticos em `:root`, tipografia com escala modular e numerais tabulares (`tabular-nums`), e conformidade de contraste WCAG AA (4.5:1).

---

## 🚀 Como Instalar em Qualquer Workspace do Claude Code

Para usar esta suite em qualquer projeto:

```bash
# Clone ou copie os diretórios para a pasta .claude do seu projeto ou ambiente global (~/.claude)
mkdir -p ~/.claude/skills ~/.claude/agents

# Copiar a skill
cp -r skills/anti-ai-slop-ui ~/.claude/skills/

# Copiar o agente
cp agents/ux-ui-specialist.md ~/.claude/agents/
```

---

## 💡 Como Invocar

### Invocar o Agente Especialista:
> *"Use o agente `ux-ui-specialist` para refatorar a interface de [arquivo/tela] eliminando o visual padrão de IA."*

### Invocar a Skill Diretamente:
> `Skill({ skill: "anti-ai-slop-ui" })` ou `/anti-ai-slop-ui`
