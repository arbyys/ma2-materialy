# Základní diferenciální rovnice 1. řádu
___

## Separace proměnných

- todo

___

## Homogenní rovnice

- todo

___

## Lineární rovnice

- jsou ve tvaru:
$$y' + f(x)y + g(x) = 0$$
- nebo občas zapsané také ve tvaru:
$$y' + f(x)y = g(x)$$
- jedna funkce závislá na $x$ násobí proměnnou $y$
- pokud $f(x) = 0$, řešení je pouze integrál z $g(x)$ - "triviální případ"
- pokud $g(x) = 0$, řešení získáme pomocí metody separace proměnných - "triviální případ"
- pokud $g(x) \neq 0$ a $f(x) \neq 0$, musíme použít jednu z uvedených metod

zadaná rovnice:
$$
    y' - 2xy = x
$$

### 1. metoda - **integrační faktor**
- nejdříve **musíme** funkci dostat do tvaru $y' + f(x)y = g(x)$
    - tato funkce v tomto tvaru již je
- spočítáme integrační faktor $i_f = e^{\int f(x) dx}$
    - $f(x)$ je funkce, která v rovnici **násobí $y$**
$$
\begin{aligned}
i_f &= e^{\int f(x) dx}\\
i_f &= e^{\int -2x dx}\\
i_f &= \underline{e^{-x^2}}
\end{aligned}
$$
- po vypočtení integračního faktoru vezmeme původní rovnici a vynásobíme ji integračním faktorem
$$
\begin{aligned}
y' - 2xy &= x &/*i_f\\
\underbrace{y'e^{-x^2}}_{\text{1. člen}} -2xye^{-x^2} &= xe^{-x^2}\\
\end{aligned}
$$
- nyní uděláme obrat šílenců:
    - vezmeme **první člen rovnice** (zvýrazněno), **smažeme derivaci u $y$**, součin dáme do závorky a tu celou zderivujeme
    - zbytek levé strany smažeme, pravou stranu opíšeme
        - obrat funguje díky vzorci na derivaci součinu (pokud výslednou závorku zderivujeme, vyjde nám původní levá strana rovnice)

$$
\begin{aligned}
\underbrace{(y*e^{-x^2})'}_{\text{1. člen po obratu}}&=xe^{-x^2}\\
\end{aligned}
$$

- nyní si lze všimnout, že na levé straně se nachází pouze derivace
- můžeme tedy obě strany zintegrovat a na levé straně se nám to vyruší s derivací
- poté stačí pouze vyjádřit $y$

$$
\begin{aligned}
(y*e^{-x^2})'&=xe^{-x^2} &/\int ... dx\\
y*e^{-x^2} &= -{e^{-x^2} \over 2} + c &/:e^{-x^2}\\
y &= -{1 \over 2} + {c \over e^{-x^2}} \\
y &= \underline{\underline{-{1 \over 2} + c*e^{x^2}}}
\end{aligned}
$$

- toto je výsledek - pokud jsou zadány podmínky, zde je chvíle je dopočítat
- podmínka: $y(0) = 2$
    
$$
\begin{aligned}
y &= -{1 \over 2} + c*e^{x^2}\\
2 &= -{1 \over 2} + c*e^{0^2}\\
c &= {5 \over 2}
\end{aligned}
$$

- po dosazení podmínky máme finální výsledek

$$
\begin{aligned}
y &= -{1 \over 2} + {5 \over 2}*e^{x^2}\\
y &= \underline{\underline{{5e^{x^2} - 1 \over 2}}}
\end{aligned}
$$