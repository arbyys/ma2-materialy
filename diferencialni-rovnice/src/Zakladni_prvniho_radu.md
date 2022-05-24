# Základní diferenciální rovnice 1. řádu
___

## Separace proměnných
- občas trošku sussy
- pro rovnice ve tvaru
$$
y' = f(x)*g(y)
$$
### Výpočet
První příklad:
$$
y' = 3 * \sqrt{x}
$$
- pokud $f(x) = c$, vyřešíme jednoduchým zintegrováním obou stran rovnou
$$
\begin{aligned}
y' &= 3*\sqrt{x} &/\int...dx\\
y &= \underline{\underline{2*\sqrt{x^3}}}
\end{aligned}
$$

Druhý příklad:
$$
y' = {1 \over x^4} * 6y
$$
- pokud $f(x)\neq c$, musíme použít trošku složitější postup
- $y'$ přepíšeme na ${dy \over dx}$, každou proměnnou poté dostaneme na jednu stranu 
$$
\begin{aligned}
y' &= {1 \over x^4} * 6y\\
{dy \over dx} &= {6y \over x^4} &/*dx\\
dy &= {6y \over x^4}*dx &/:y\\
{dy \over y} &= {6 \over x^4}*dx
\end{aligned}
$$

- jakmile máme proměnné rozdělené na opačné strany rovnice, můžeme už integrovat (každou stranu podle příslušné proměnné - máme tam dx a dy)
- po integrování vyjádřit $y$ a hotovo
$$
\begin{aligned}
{dy \over y} &= {6 \over x^4}*dx &/\int...\\
\int{1 \over y} dy &= \int{6 \over x^4} dx\\
ln|y| &= -{2 \over x^3} + c &/e^n\\
e^{ln|y|} &= e^{-{2 \over x^3}+c}\\
|y| &= e^{-{2 \over x^3}}*\underbrace{e^c}_\text{K}\\ 
y &= \underline{\underline{\pm K + e^{-{2 \over x^3}}}}
\end{aligned}
$$
- toho $\pm$ by se ještě šlo zbavit pomocí podmínek a polemizování, který člen je kladný a který záporný (asi)
___

## Homogenní rovnice

- dost sussy mrdka
- ve tvaru
$$
y' = f({y \over x})
$$

- úkolem je převést rovnici na separované proměnné pomocí substituce

### Výpočet
$$
    y' = {x^2 + y^2 \over xy}
$$

- použijeme substituci $y = x*z(x)$
$$
\begin{aligned}
    y' &= {x^2 + y^2 \over xy} \\
    z+xz' &= {x^2 + x^2z^2 \over x^2z}\\
    z+xz' &= {x^2(1 + z^2) \over x^2z}\\
    z' &= {1 \over xz}
\end{aligned}
$$

- teď už můžeme postupovat pomocí separovaných proměnných, poté vrátit substituci
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

### 2. metoda - **variace konstant**
- rovnici **nemusíme** převést na tvar $y' + f(x)y = g(x)$ jako u integračního faktoru, ale hodí se to udělat
    - tato funkce v tomto tvaru již je
- vyřešíme homogenní tvar (levá strana rovnice je rovna nule - pokud ji máme ve správném tvaru viz. výše)
- 