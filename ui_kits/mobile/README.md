# Pulse · Mobile UI Kit

App nativo para o promotor de campo. Três telas representativas lado a lado.

## Telas
1. **Home / Rota do dia** — saudação, "próxima loja" como hero card com gradiente Pulse + linha de batimento, stats, lista de visitas (concluída · ativa · agendada), bottom tab bar com FAB de scan.
2. **Leitura de estoque (scan)** — câmera mock identificando SKU, contador grande, lista de já contados.
3. **Home em dark theme** — mesma tela trocando `data-theme="dark"`.

## Design notes
- Hero card sempre vermelho-navy gradient — é o "momento Pulse" da tela.
- Tabs estão escondidas no design mas FAB central destacado (scan = ação primária do promotor).
- Tipos grandes (24-26px títulos) — usuário usa o app rápido, em pé, na loja.
- Tudo via tokens semânticos; dark theme funciona trocando o atributo.
