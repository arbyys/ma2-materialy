# Exaktní rovnice

- pozná se tak, že má v zápisu $\mathrm{d}x$ a $\mathrm{d}y$
- tvar

$$
M(x,y)\mathrm{d}x + N(x,y)\mathrm{d}y = 0
$$

- (funkce, která je násobena $\mathrm{d}x$ je $M$, druhá, násobená $\mathrm{d}y$ je $N$)

## Výpočet

$$
\underbrace{\bigg({1 \over y} + x\bigg)}_{\text{M}}*\mathrm{d}x \underbrace{\ - \ \bigg({x \over y^2}\bigg)}_{\text{N}}*\mathrm{d}y = 0
$$

- ověřit, zda se opravdu jedná o exaktní rovnici
  - parciální derivace se musí rovnat

$$
{\partial M \over \partial y} = {\partial N \over \partial x}
$$

- pokud vztah neplatí, musíme rovnici pronásobit integračním faktorem, poté dostaneme exaktní rovnici
- jakmile vztah platí, můžeme začít počítat:
- chceme nalézt **kmenovou funkci** $F(x,y)$
- zintegrujeme buď funkci $M$ podle $x$, nebo funkci $N$ podle $y$ (můžeme si vybrat)
- nezapomenut přidat $c(x)$ pokud integrujeme podle $y$, nebo $c(y)$ pokud integrujeme podle $x$

$$
F(x,y) = \int \! N \, \mathrm{d}y =\\ = \int \! -{x \over y^2} \, \mathrm{d}y =\\ ...\\ ...\\ = \underline{\underline{{x \over y} + c(x)}}
$$

- výsledek dosadíme do následujícího vztahu a potřebujeme **vyjádřit**  $c(x)$
- funkci vždy derivujeme podle **opačné proměnné**, než podle které jsme ji integrovali
- na pravou stranu rovnice vždy dosazujeme **tu druhou funkci** ($M$ nebo $N$), než jsme integrovali

$$
\begin{aligned}
{\mathrm{d} \over \mathrm{d}x}F(x,y) &= M \\
{\mathrm{d} \over \mathrm{d}x}\bigg({x \over y} + c(x)\bigg) &= {1 \over y} + x \\
... \\
c(x) &= \underline{\underline{{x^2 \over 2} + c}} & c \in \mathbb{R}
\end{aligned}
$$

- nalezenou funkci $c(x)$ dosadíme do vypočtené funkce $F(x,y)$ z předchozího kroku a máme výsledek

$$
\begin{aligned}
F(x,y) &= {x \over y} + c(x) \\
F(x,y) &= \underline{\underline{{x \over y} + {x^2 \over 2} + c}} & c \in \mathbb{R}
\end{aligned}
$$
