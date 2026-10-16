# Claude Code — Catálogo Oficial de Skills & Agentes (5S Organizado)

Estrutura de governança e inventário das skills e agentes ativos no diretório `~/.claude/skills/` e `~/.claude/agents/`.

---

## 1. 🚀 Vibe Coding, Arquitetura & Design
Skills focadas na concepção e ancoragem de novos produtos:
- **`modular-sfa-architect`**: Arquitetura, migração e build de Single-File Applications (SFA) separando Monólito Modular em desenvolvimento de artefato único de distribuição.
- **`vibe-docs-scaffold`**: Cria a pasta `docs/` com os 6 arquivos de contexto mestre (PRD, ARCHITECTURE, RULES, DESIGN, TASKS, MEMORY).
- **`frontend-design`**: Criação de interfaces ricas, humanas e anti-genéricas com tipografia intencional e identidade única.
- **`anti-ai-slop-ui`**: Checklist estrito e diretrizes para eliminar 100% do visual genérico gerado por IA (AI Design Slop) com matriz de decisão por contexto.
- **`brainstorming`**: Exploração de hipóteses e requisitos antes de codificar.
- **`writing-plans`**: Elaboração de especificações e planos atômicos.
- **`executing-plans`**: Execução disciplinada passo a passo de planos aprovados.

---

## 2. 🛠️ Engenharia, TDD & Resolução de Problemas
Skills cirúrgicas para desenvolvimento estável sem quebrar código:
- **`test-driven-development`**: Ciclo RED-GREEN-REFACTOR (testes antes do código).
- **`systematic-debugging`**: Investigação de causa raiz em 4 fases antes de alterar código.
- **`verification-before-completion`**: Prova real de funcionamento antes de declarar pronto.
- **`cascade-impact-analysis`**: Análise de impacto colateral antes de renomear campos/tabelas.
- **`finishing-a-development-branch`**: Checklist de merge e encerramento de features.
- **`using-git-worktrees`**: Trabalho isolado em múltiplas branches simultâneas.

---

## 3. 🔍 Code Review, Auditoria & Fable Method
Skills para validação rigorosa e adversarial:
- **`audit-regras-investigacao`**: Auditoria normativa e de conformidade lógica entre manuais (PG-015, FORM-087, ANP 882/2022) e a implementação de código (FACIU/monólito).
- **`requesting-code-review`**: Autoavaliação e preparação de código antes do commit.
- **`receiving-code-review`**: Aplicação cirúrgica de feedbacks recebidos.
- **`fable-method`**: Metodologia formal de resolução de problemas complexos.
- **`fable-domain`**: Análise e modelagem profunda de regras de negócio.
- **`fable-judge`**: Verificação adversarial estrita de entregas.
- **`fable-loop`**: Loop end-to-end com prova de execução.

---

## 4. 🤖 Orquestração de Agentes & Superpowers
Coordenação de múltiplos agentes e otimização de contexto:
- **`using-superpowers`**: Inicialização de fluxos avançados de trabalho.
- **`diagnosing-superpowers`**: Diagnóstico e recuperação de sessões corrompidas.
- **`dispatching-parallel-agents`**: Divisão de tarefas em subagentes paralelos.
- **`subagent-driven-development`**: Execução de planos usando agentes autônomos.
- **`writing-skills`**: Criação padronizada de novas skills no ecossistema.
- **`jev-systemone-optimization`**: Compactação de contexto e economia de tokens.

---

## 5. 📦 Bento Stacks & Operação de Infraestrutura
Operação Day-2 das ferramentas rodando na VPS:
- **`bento-hermes`**: Operação da API e CLI do Hermes Agent Gateway.
- **`bento-n8n`**: Automação de nós do n8n com validação via MCP.
- **`bento-evolution-api`**: Gestão do WhatsApp (QR Code, instâncias, webhooks).
- **`bento-paperclip`**: Orquestração de squads e agentes autônomos.
- **`bento-metamcp`**: Agrupamento de ferramentas MCP em endpoints unificados.
- **`bento-typebot`**: Gestão e manutenção de bots de atendimento.
- **`bento-chatwoot`**: CRM e atendimento multicanal.
- **`ffmpeg-skill`**: Processamento e manipulação de vídeo/áudio via terminal.

---

## 6. 🦾 Subagentes Especialistas Registrados (`.claude/agents/`)
Subagentes focados para tarefas de alto acabamento e auditoria:
- **`ux-ui-specialist`**: Especialista sênior em UX/UI, Design Systems e Engenharia Frontend. Orquestra as principais skills de design (`impeccable`, `frontend-design`, `dataviz`, `anti-ai-slop-ui`) e elimina 100% do visual padrão genérico de IA com matriz de decisão estética.
- **`impeccable-finish-reviewer`**: Auditoria final adversarial de acabamento de builds contra contratos de direção, fidelidade de comps e piso de craft.
- **`impeccable-asset-producer`**: Produção limpa de assets rasterizados a partir de referências aprovadas sem desviar da direção artística.
- **`impeccable-manual-edit-applier`**: Aplicação de lotes de edições manuais em código fonte.
- **`impeccable-documenter`**: Registro e geração de documentação de Design System (`DESIGN.md`).
