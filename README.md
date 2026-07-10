# Treino do Dia

App web (PWA) de séries fixas de exercícios sem equipamentos, com timers de
exercício e descanso. Funciona offline e pode ser instalado na tela inicial.

## Como funciona

- **Séries fixas por dia da semana** (Segunda = Série 1 … Domingo = Série 7).
- Cada série: 2 aquecimentos + 11 exercícios de força intercalando
  **pernas / postura (core) / braços** + 2 alongamentos no fim (~14 a 16 min).
- Timers: **40 s** de exercício, **15 s** de descanso curto e **30 s** de descanso
  longo no meio da série.
- Aviso sonoro **"pi-pi-pi-piii"**: três bipes curtos faltando 3 s, 2 s e 1 s, e
  um bipe longo no fim do tempo (agudo = entra exercício, grave = entra descanso).
  Timbre suave (onda triangular). Volume ajustável na tela inicial (fica salvo)
  e botão **Testar som**.
- Botão **🎵 Música** abre uma playlist fixa à sua escolha (o link fica salvo no
  aparelho). O navegador não pode dar play sozinho em outro app: abra a playlist,
  toque em ▶ e volte para o treino.
- Ícone de posição do corpo em cada exercício, descrição do próximo exercício
  durante o descanso, tela mantida ligada durante o treino, contador de sequência
  de dias, histórico exportável (CSV/JSON) e "Parabéns" no fim.

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
