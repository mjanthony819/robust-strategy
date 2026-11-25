# Robust Strategy

Parameter sweep heatmap plus walk-forward testing, in the browser. Part of a set of four quant
projects; this one answers: is the best parameter setting real, or curve-fit?

Live: https://mjanthony819.github.io/robust-strategy/

## What it does

- Sweeps an 8x8 grid of fast/slow moving-average pairs on real S&P 500 data and draws the Sharpe heatmap
- Picks the centre of a stable plateau (best average of a cell and its neighbours), not the single hottest pixel
- Walk-forward validation: chooses parameters on a rolling 4-year train window, then applies them to the
  following unseen 1-year test window, chained across 12 years
- Out-of-sample equity curve vs buy and hold over the same stitched test windows
- Load your own Date,Close CSV

## Stack

Single `index.html`. No frameworks, no build step, no API keys. Charts are hand-drawn on canvas.

## Honest note

The out-of-sample result is weaker than the in-sample one. That gap is exactly what the project is about.

Built with AI assistance (Claude).
