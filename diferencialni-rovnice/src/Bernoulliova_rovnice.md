# Bernoulliova rovnice

- pozná se tak, že má v zápisu $y^n, \quad n\in\mathbb{R} \setminus \{0,1\}$
- tvar

$$
y' + a(x)y + b(x)y^n=0
$$

## Výpočet
- úkolem je transformovat rovnici na lineární, kterou už poté dokážeme vyřešit klasicky
- pokud u výrazu $y^n$ je $n>0$, automaticky můžeme přidat $y=0$ jako řešení příkladu

$$
y' + xy = xy^3
$$

- **vždy děláme substituci** $t = y^{-n+1}$
- v tomto případě $\underline{\underline{\underline{t = y^{-2}}}}$
- poté zderivujeme danou subtituce a vyjádříme z ní člen $y'$
$$
\begin{aligned}
t' &= -2y^{-3} * y'\\
{t' \over -2y^{-3}} &= y'\\
y' &= \underline{\underline{\underline{-{t'y^3 \over 2}}}}
\end{aligned}
$$
- 3krát jsou podrtženy výrazy, které nyní budeme potřebovat pro substituci
- rovnici vydělíme členem $y^n$
$$
\begin{aligned}
y' + xy &= xy^3\\
{y' \over y^3} + {x \over y^2} &= x 
\end{aligned}
$$

- vidíme, že v rovnici je ${1 \over y^2}$, což jde přepsat jako $y^{-2}$, tudíž našli jsme člen pro substituci - provedeme substituci a upravíme
$$
\begin{aligned}
{-{t'y^3 \over 2 } \over y^3} + xt &= x\\
-{t'y^3 \over 2y^3} + xt &= x\\
\underline{\underline{-{t' \over 2} + xt - x}} &= 0
\end{aligned}
$$

- výsledek už je klasická lineární rovnice, kterou můžeme řešit integračním faktorem / variací konstant
- na konci nezapomenout vrátit substituci
- nezapomenout přidat $y=0$ jako řešení příkladu - jelikož u výrazu $y^n$ je $n>0$ 