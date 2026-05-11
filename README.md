# Pulse Design System

> **Pulse** — *a realidade da operação.*
> Sistema de gestão para operações de trade marketing: controle de promotores, lojas, atividades, leitura de estoque, gestão de shelf e análise de dados.

---

## Sobre

Pulse é uma plataforma B2B para times de trade marketing operarem com velocidade e clareza. O design system reflete isso: **enérgico, direto, baseado em dados, com identidade forte**. O símbolo da marca — um sinal de pulso atravessando um globo vermelho-e-azul — vira o motivo visual recorrente: linhas que cortam, ritmo, batimento.

### Produtos cobertos por este DS
- **Web Dashboard (desktop)** — supervisores, coordenadores e gestores operacionais
- **App Mobile (promotor em campo)** — check-in em loja, leitura de estoque, fotos, atividades
- **Landing/Site institucional** — captação de clientes B2B

### Concorrentes de referência
- [Involves Stage](https://involves.com/pt-br/stage/) — *padrão de mercado, sério/corporativo*
- [WebJasper](https://webjasper.com.br/sistema-de-validade/) — *pragmático, próximo do operacional*

Pulse se diferencia visualmente: mais **enérgico, moderno e respirado** que ambos.

---

## Índice de arquivos

| Arquivo | O que tem |
|---|---|
| `README.md` | Este documento — overview, voice, foundations |
| `SKILL.md` | Frontmatter para Agent Skills (usar este DS como skill no Claude Code) |
| `colors_and_type.css` | Tokens completos (cores, tipo, spacing, radii, motion, sombras) — light + dark |
| `assets/` | Logos (símbolo + completo) em PNG e JPG |
| `preview/` | Cards visuais que populam a aba Design System |
| `ui_kits/web/` | UI kit do dashboard desktop — JSX components + index.html |
| `ui_kits/mobile/` | UI kit do app de promotor — JSX components + index.html |
| `ui_kits/landing/` | UI kit do site institucional |

---

## Fundamentos de conteúdo (Voice & Tone)

**Personalidade:** próximo, descontraído, confiante. Falamos com o operador como um colega que entende o chão da loja — não como um software corporativo distante.

| Faça | Não faça |
|---|---|
| "Olá, Marina! Você tem 4 lojas pra visitar hoje." | "Bem-vindo(a) ao seu painel de operações diárias." |
| "Bateu o ponto? Bora começar." | "Confirme sua presença no estabelecimento." |
| "Estoque abaixo do mínimo em 3 SKUs" | "Foi detectada uma anomalia de inventário" |
| "Pulse no ar" (em loading/empty states) | "Carregando dados, por favor aguarde..." |
| "Sem internet? Sem problema — salvamos aqui." | "Erro de conexão. Tente novamente." |

**Regras práticas:**
- **Você (informal)**, nunca "Senhor(a)" ou tratamentos rígidos.
- **Frases curtas**. Verbo no imperativo nos CTAs: *"Bater ponto"*, *"Conferir estoque"*, *"Abrir mapa"*.
- **Números em destaque**. Quando há um KPI relevante, ele aparece grande, com unidade pequena ao lado.
- **Sem jargão corporativo gratuito**. "Sell-out" sim (termo do setor); "alavancar sinergias" não.
- **Emoji**: evitar no produto. OK em comunicação de marketing ocasional (ex: 📈 em case studies).
- **Erros são humanos**: explique o que aconteceu E o próximo passo. *"Foto não enviou — tenta de novo quando pegar sinal."*

---

## Fundamentos visuais

### Motivos da marca
1. **A linha de pulso** — o batimento cardíaco do logo é o elemento gráfico mais distintivo. Aparece como divisor entre seções, decoração em headers de página, animação sutil em estados de loading.
2. **O gradiente vermelho→azul** — usado em hero sections, ícones de feature destacados e botões grandes de CTA primário em momentos especiais. Nunca em background de tela inteira (vira AI-slop).
3. **O contraste duro vermelho/azul-marinho** — vermelho é ação e urgência; azul-marinho é confiança e dado. Não misturar funções.

### Cores

**Marca:**
- `--red-600 (#C8102E)` — vermelho do logo, CTA primário em light, alertas
- `--navy-700 (#1B2A4E)` — azul do logo, headers/sidebar em light, base de dark mode
- Escalas completas de 50→950 em ambas

**Uso semântico (regra de ouro):**
- **Vermelho = ação**. Botão primário, link ativo, item selecionado, "ao vivo".
- **Navy = estrutura**. Sidebar, headers de tabela, dados densos, autoridade.
- **Cinza/slate** carrega 80% da interface. Cor é tempero.

**Temas:**
- **Light**: fundo `slate-50`, surface branco, texto `slate-900`. Vibe diurna, escritório.
- **Dark**: fundo `navy-950` (nunca preto puro), surface `navy-900`, texto warm-white. Vibe operação noturna, dashboard 24/7.

### Tipografia
- **Display**: Space Grotesk — geométrica com personalidade. Headlines, números grandes, hero.
- **Body / UI**: Manrope — humanista neutra, ótima em UI densa.
- **Mono**: JetBrains Mono — códigos, SKUs, dados tabulares.
- Numerais sempre tabular-nums em métricas. Tracking negativo (-0.02em) em displays grandes.

### Espaçamento e densidade
- Escala 4px-base (4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96).
- **Densidade confortável-espaçada**: cards têm padding generoso (24-32px), gaps de 16-24px em grids.
- Em tabelas: row-height de 48-56px (não 40), pra dar respiro mesmo com muitos dados.

### Cantos, sombras e bordas
- **Radii**: 10px (md) é o default de card/input/botão. 14-20px em elementos maiores. 4-6px só em pílulas pequenas.
- **Sombras**: suaves e baixas-em-cor, tinted com navy (não preto cinza). Cards levam `shadow-sm` ou `shadow-md`. Modais `shadow-xl`.
- **Bordas**: hairline `1px` cor `border-subtle`. Bordas fortes só em estado focus.

### Background
- **Sem gradientes de tela cheia.** Padrão fortemente desencorajado.
- O gradiente da marca aparece em **superfícies pequenas** (ícone hero, badge de "PRO", cantos arredondados de uma card de feature).
- Imagens reais (fotos de PDV, mapas, screenshots de relatório) > ilustrações abstratas.

### Movimento
- **Easing default**: `cubic-bezier(0.22, 1, 0.36, 1)` (ease-out). Saídas mais rápidas que entradas.
- **Duração base**: 220ms. Fast: 140ms (hover/feedback). Slow: 360ms (modais, page transitions).
- **Linha de pulso animada** em loaders globais (a wave do logo correndo). Específica da marca.
- **Sem bounces excessivos** — operação séria, não app de jogo.

### Estados
- **Hover**: surface fica `bg-surface-2`; botão fica um tom mais escuro (red-700, navy-800).
- **Active/Press**: mais um tom escuro + scale(0.98) opcional.
- **Focus**: ring 3px `rgba(red-500, 0.25)` — sempre visível, é acessibilidade.
- **Disabled**: opacity 0.5 + cursor not-allowed. Nunca esconder, só atenuar.

### Layout
- Web: container max-width 1440px, sidebar fixa 240-280px, header fixo 64px.
- Mobile: 16px de gutter, safe-area-insets respeitados, bottom nav 64px.
- Landing: hero 100vh opcional, seções 96px de padding vertical desktop / 64px mobile.

---

## Iconografia

**Sistema escolhido:** [Lucide](https://lucide.dev) — stroke icons, 1.75-2px weight, geométricos, encaixam com Manrope/Space Grotesk. Linkado via CDN nos UI kits.

**Substituição flagada:** Pulse ainda não tem icon set próprio. Lucide é a melhor aproximação até existir um. **Ação para o usuário**: confirmar se Lucide está OK ou se há outro set preferido (Phosphor, Heroicons, custom).

**Regras:**
- Tamanho default 20px em UI, 16px inline com texto, 24-32px em headers/empty states.
- Cor herdada do texto via `currentColor` — nunca cor fixa.
- Ícone do produto (símbolo Pulse) reservado para logo e splash. Não usar como ícone de UI.

**Logos disponíveis:**
- `assets/pulse-symbol.png` — só o símbolo, com transparência (uso em app)
- `assets/pulse-logo-full.jpg` — símbolo + wordmark + slogan
- `assets/pulse-symbol.jpg` — versão JPG do símbolo

⚠️ **Falta:** versões SVG dos logos e variantes monocromáticas (branco sobre escuro, preto sobre claro). Recomendado o usuário fornecer.

---

## Como usar em outro arquivo

```html
<link rel="stylesheet" href="colors_and_type.css">
<body data-theme="light"><!-- ou "dark" -->
  <h1 class="t-h1">Olá, Marina!</h1>
  <button style="background: var(--brand-primary); color: var(--brand-primary-fg);">
    Bater ponto
  </button>
</body>
```

Trocar tema é só mudar o atributo no `<body>` (ou `<html>`).
