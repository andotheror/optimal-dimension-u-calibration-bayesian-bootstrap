# Optimal-Dimension U-Calibration by Bayesian Bootstrap

## Abstract

U-calibration asks one online probability forecaster to have low regret for every bounded proper loss, including losses unknown when the forecasts are made. For nontrivial $K\geq2$, the optimal worst-case rate is $\Theta(\\!\sqrt{\min\\{K,T\\}T}\\,)$, while the smooth-loss class has minimax time rate $\Theta(\log T)$. A recent simultaneous algorithm attains both time rates but leaves a polynomial gap in $K$. We show that the classical Bayesian bootstrap closes this gap. At round $t$, independently assign exponential weights to the past outcomes and predict their normalized weighted histogram. Equivalently, if $c_{t-1}$ is the vector of past outcome counts, sample $P_t\sim\mathrm{Dirichlet}(c_{t-1})$ on the observed face of the simplex. For every outcome sequence with terminal counts $n_1,\ldots,n_K$, observed support size $m$, and every proper loss in $[-1,1]$, the expected regret is at most

$$6\sum_{i=1}^K\sqrt{n_i}\leq6\sqrt{mT}\leq6\sqrt{\min\\\\\\{K,T\\\\\\}T}.$$

For every $\beta$-smooth loss, the same forecasts have regret at most the regret of empirical follow-the-leader plus $(\beta/2)\log T$, and therefore $O(\beta\log T)$ for bounded smooth proper losses. The proof uses three elementary facts: a one-count Dirichlet update has total variation $O(1/\sqrt{c_i})$, size-biasing an exponential weight adds an independent exponential weight, and weighted be-the-leader holds simultaneously for all proper losses. A class-aggregation reduction gives the matching dimension-capped lower bound. The algorithm is loss-agnostic, horizon-free, proper, and minimax-optimal for the worst bounded loss while retaining the minimax-optimal smooth-class time rate.

## Contributions

Our main theorem gives a single horizon-free algorithm with

$$\mathrm{Reg}_\ell\leq6\sum_i\sqrt{n_i}\leq6\sqrt{mT}\leq6\sqrt{\min\\\\\\{K,T\\\\\\}T}$$

for every bounded proper loss $\ell$. The first inequality is support and frequency adaptive, and a class-aggregation corollary proves that the final rate is minimax-optimal in every dimension regime. For every bounded $\beta$-smooth proper loss, the same algorithm has $O(\beta\log T)$ regret, which matches the smooth-class time lower bound. Unlike prior optimal-worst-case algorithms, the perturbation scale is not tuned to $T$. Unlike prediction-space Gaussian noise, every forecast belongs to the simplex.

## Keywords

optimal-dimension, u-calibration, bayesian, bootstrap, asks, online, probability, forecaster, have

## Files

- `main_old_2026-08-13.pdf`, the paper as first published, with its OpenTimestamps proof `main_old_2026-08-13.pdf.ots`.
- `supplement_old_2026-08-13.pdf`, the supplement as first published, with its OpenTimestamps proof `supplement_old_2026-08-13.pdf.ots`.
- source: `aistats2027.sty`, `main.tex`, `references.bib`, `supplement.tex`.
- also: `main.bbl`.
