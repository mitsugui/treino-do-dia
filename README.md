# Treino do Dia

App web (PWA) de séries fixas de exercícios sem equipamentos, com timers de
exercício e descanso. Funciona offline e pode ser instalado na tela inicial.

## Como funciona

- **Séries fixas por dia da semana** (Segunda = Série 1 … Domingo = Série 7).
- Cada série: 2 aquecimentos + força intercalando **pernas / postura (core) / braços**
  + 2 alongamentos no fim.
- Timers: **40 s** de exercício, **15 s** de descanso curto e **30 s** de descanso
  longo no meio da série.
- Ícone de posição do corpo em cada exercício, beeps de contagem, tela mantida
  ligada durante o treino, contador de sequência de dias e "Parabéns" no fim.

## Uso

Abra o `index.html` no navegador (ou a versão publicada). No celular, use o menu
do navegador → **Adicionar à tela inicial** para instalar como app.

## Personalizar

Tudo fica no topo do `<script>` em `index.html`:

- `WORK`, `SHORT`, `LONG` — tempos.
- `EX` — exercícios (nome, instrução, posição do corpo, grupo). `sides:true`
  transforma o exercício em dois (lado direito / esquerdo).
- `SERIES` — a lista fixa de cada dia.

Ao alterar arquivos, suba a versão do cache em `sw.js` (`treino-vN`) para forçar
a atualização nos aparelhos já instalados.
