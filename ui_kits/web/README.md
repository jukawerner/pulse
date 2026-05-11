# Pulse · Web Dashboard UI Kit

Dashboard desktop para supervisores, coordenadores e gestores operacionais.

## Telas/conceitos incluídos
- **Sidebar fixa** com navegação completa (Operação · Trade · Conta)
- **Top bar** com saudação personalizada, busca global, notificações
- **KPI cards** (4 colunas): incluindo o "card assinatura" com gradiente Pulse e linha de batimento animada
- **Gráfico multi-line** de sell-out por categoria (paleta de chart tokens)
- **Activity feed live** com badge piscando
- **Mapa mock** com pins coloridos (status das lojas) e linha de rota tracejada
- **Tasks/atividades** com checkbox toggleable
- **Tabela de lojas** com store cells, progress bars, badges, dados tabulares

## Interações funcionando
- Toggle tema **light ↔ dark** (botão lua/sol no card de usuário, canto inferior esquerdo da sidebar)
- Marcar/desmarcar atividades como concluídas
- Trocar segmented controls (Hoje/7d/30d, etc.)

## Como abrir
`index.html` é standalone — abre em qualquer browser.

## Notas de design
- Tudo consome **apenas tokens semânticos** (`--bg-surface`, `--brand-primary`, etc.). Trocar `data-theme` no body recolore tudo.
- Lucide via CDN para iconografia. Tamanho default 18px em UI, 16px inline com texto.
- Sem gradiente de tela cheia — o gradiente da marca aparece **só** no KPI "Pulse no ar" e na linha de pulso decorativa.
