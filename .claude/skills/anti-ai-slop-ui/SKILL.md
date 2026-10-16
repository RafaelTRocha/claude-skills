---
name: anti-ai-slop-ui
description: Checklist estrito e diretrizes para eliminar 100% do visual genérico gerado por IA (AI Design Slop). Use ao criar, refatorar ou auditar interfaces web/mobile para garantir acabamento profissional e humano.
license: MIT
---

# Anti-AI Slop UI — Diretrizes de Design Humano & Distintivo

Esta skill existe para erradicar o **"AI Visual Slop"** — o conjunto previsível de vícios visuais que modelos de linguagem utilizam por padrão quando geram interfaces sem direcionamento rigoroso.

---

## 1. O que é Proibido (Lista Negra do "AI Slop")

Se a interface contiver qualquer um dos itens abaixo sem justificativa contratual expressa, ela falha na revisão de acabamento:

| Vício Visual de IA (Slop) | Por que acontece | O que fazer no lugar |
|---|---|---|
| **Eyebrows em Caixa Alta** (`UPPERCASE TRACKING-WIDEST` acima do H1/H2) | Modelo tenta imitar landing pages do Twitter/X | Remova o eyebrow. Deixe o título falar por si mesmo ou use hierarquia editorial direta. |
| **Paleta "Creme + Terracota"** (`#F4F1EA` + `#D97757`) ou "Dark Neon" (`#0A0A0A` + `#00FF99`) | Confluência de prompts comuns e defaults da Anthropic | Escolha paleta de 3-4 cores inspirada no nicho real (ex: azul marinho técnico, ardósia, bronze, papel de arquivo). |
| **SaaS Card Trap** (tudo fatiado em cartões idênticos com `rounded-xl` e sombra suave) | O modelo não sabe organizar fluxo de leitura sem caixas | Use linhas divisórias sutis (`border-t`), contraste de fundo de seção, alinhamentos tipográficos ou tabelas compactas. |
| **Título com 1 Palavra Colorida/Gradiente** ("Construa o *Futuro* dos Dados") | Clichê publicitário raso de geradores de landing page | Título monocromático sóbrio com peso e tamanho bem calibrados. Destaque por contraste de peso, não por cor/gradiente. |
| **Glow Blobs & Gradientes Radiais nos Cantos** (`radial-gradient` borrado no fundo) | Tentativa preguiçosa de preencher espaço em branco | Use textura sutil real, espaço negativo intencional ou grid técnico funcional. |
| **Botões com Seta Obrigatória** (`Começar Agora →`) | O modelo replica CTAs de templates Bootstrap/Tailwind genéricos | Botão limpo com verbo de ação direto no infinitivo ou imperativo: "Criar relatório", "Exportar dados", "Acessar painel". |
| **Animações de Scroll em Cascata** (cada card dando fade-in-up) | O modelo acha que movimento = qualidade | Zero animação automática desnecessária. Use transições rápidas (<150ms) apenas em interações do usuário (hover, clique, expansão). |
| **Fonte Padrão Única (Inter/Roboto)** sem escala calculada | Ausência de personalidade tipográfica | Combine duas famílias com propósito (ex: uma Serif técnica ou Display angular para títulos + Sans geométrica limpa para dados). |

---

## 2. Matriz de Decisão Estética Baseada em Contexto

O design deve ser uma consequência direta do problema e do usuário, nunca uma escolha arbitrária de moda. O agente mapeia o domínio para o arquétipo visual correto:

| Contexto / Domínio do Produto | Estilo Visual Recomendado | Tratamento de Superfície | Tipografia & Detalhes | O que NUNCA fazer aqui |
|---|---|---|---|---|
| **Industrial, Offshore, Regulatório & Segurança (ex: FACIU)** | **Minimalismo Técnico / Precisão Suíça** | Superfícies sólidas e opacas, divisores sutis de 1px (`border`), contraste alto | Sans funcional neutra, numerais tabulares (`tabular-nums`), badges de status operacionais sóbrias | Proibido Glassmorphism, proibido sombras difusas e cantos arredondados gigantes (`rounded-3xl`). |
| **Fintech, Bancos & B2B Analítico** | **Refined Functional Minimalism** | Superfícies planas com elevação discreta (1-2 níveis), fundo sóbrio (slate/ardósia) | Números tabulares, rótulos compactos em sentence case, paleta monocromática com acentos semânticos | Proibido gradientes coloridos aleatórios e botões gigantes estilo brinquedo. |
| **Modais, Sticky Navbars & Camadas Flutuantes** | **Glassmorphism / Frosted Glass Tátil** | `backdrop-filter: blur(16px)` com fundo translúcido `rgba(..., 0.7)` e borda sutil `1px solid rgba(255,255,255,0.08)` | Tipografia nítida sobre o vidro, contraste garantido contra o fundo subjacente | Proibido aplicar vidro no corpo da página, tabelas ou formulários inteiros (destrói a legibilidade). |
| **Developer Tools, Terminais & CLI Dashboards** | **Technical Monochrome / Dark Terminal** | Superfícies carvão profundo (`#12161f`), grids técnicos, zero gradiente | Monospace de alta qualidade para comandos/dados, contraste por peso | Proibido fontes cursivas, sombras suaves ou paletas pastéis infantis. |
| **Documentação Técnica, Manuais & Relatórios (Docs)** | **Editorial Clássico / Swiss Grid** | Papel digital limpo, respiração em espaço negativo, leitura confortável | Serif técnica para títulos + Sans limpa para corpo, largura máxima de 68-75ch, entrelinha generosa | Proibido layouts cheios de cards pequenos flutuantes que quebram o fluxo de leitura contínua. |
| **Ferramentas Ágeis & Produtos Jovens / Criativos** | **Neobrutalismo Disciplinado** | Bordas escuras marcadas (1.5px a 2px), sombras sólidas com deslocamento seco sem blur (`3px 3px 0 #000`) | Tipografia expressiva e angular, contrastes altos de blocos | Proibido excesso de firulas decorativas que distraiam da tarefa principal. |

---

## 3. Princípios de Acabamento & Autenticidade

### A. Ancoragem no Domínio Real
- **Software Industrial / Técnico / Regulatório:** Densidade alta, tabelas ricas, fontes tabulares (`font-feature-settings: "tnum"`), cores funcionais para status (Neutro, Alerta, Sucesso), sem frufrus.
- **Ferramentas de Produtividade / Dashboards:** Foco em velocidade de leitura, teclado em primeiro lugar (`:focus-visible` impecável), estados vazios (empty states) instrucionais.
- **Editorial / Conteúdo:** Ritmo de leitura agradável, largura de linha máxima de 70-80 caracteres, entrelinha confortável.

### B. Sistema de Tokens Semânticos em `:root`
Evite cores soltas no CSS/Tailwind. Defina tokens funcionais claros:
```css
:root {
  --bg-app: #0f141c;
  --bg-surface: #161d27;
  --bg-surface-elevated: #1e2735;
  --border-subtle: #273344;
  --border-strong: #3b4d66;
  --text-main: #f0f4f8;
  --text-muted: #8a99ad;
  --brand-primary: #2563eb;
  --brand-accent: #38bdf8;
  --status-warning: #eab308;
  --status-danger: #ef4444;
  --status-success: #10b981;
}
```

### C. Tipografia com Intenção
- Hierarquia estrita com escala modular (ex: 12px, 14px, 16px, 20px, 28px, 40px).
- Numerais tabulares para tabelas financeiras ou de engenharia (`font-variant-numeric: tabular-nums`).
- Linhas de texto nunca devem atravessar telas largas (`max-w-prose` ou `max-width: 68ch`).

### D. Densidade & Espaçamento
- Diferencie áreas densas (tabelas, formulários operacionais) de áreas de respiração (cabeçalhos, resumos).
- Um bom layout é reconhecido pela elegância do espaço negativo, não pela quantidade de bordas e cartões coloridos.

---

## 3. Checklist de Autoavaliação (O Teste do Espelho)

Antes de aprovar qualquer tela ou componente, responda:
1. [ ] Há algum "eyebrow" desnecessário em caixa alta? Se sim, **remova**.
2. [ ] Tudo está dentro de um "card" com borda redonda e sombra cinza? Se sim, **transforme em layout de fluxo**.
3. [ ] Há palavras isoladas coloridas no meio do título? Se sim, **unifique a cor**.
4. [ ] Há gradientes borrados ou efeitos neon nos cantos? Se sim, **remova**.
5. [ ] O texto e os contrastes passam no WCAG AA (mínimo 4.5:1)?
6. [ ] A tipografia transmite a seriedade e o contexto do produto ou parece template baixado da internet?
