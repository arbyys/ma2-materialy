# Exaktní rovnice

- pozná se tak, že má v zápisu $dx$ a $dy$
- tvar 
$$M(x,y)dx + N(x,y)dy = 0$$
- (funkce, která je násobena $dx$ je $M$, druhá, násobená $dy$ je $N$)

## Výpočet

$$ \underbrace{({1 \over y} + x)}_{\text{M}}*dx \underbrace{\ - \ ({x \over y^2})}_{\text{N}}*dy = 0 $$


- ověřit, zda se opravdu jedná o exaktní rovnici
    - parciální derivace se musí rovnat 
    $$ {\partial M \over \partial y} = {\partial N \over \partial x} $$
    - pokud vztah neplatí, musíme rovnici pronásobit integračním faktorem, poté dostaneme exaktní rovnici
- jakmile vztah platí, můžeme začít počítat:
- chceme nalézt **kmenovou funkci** $F(x,y)$
- zintegrujeme buď funkci $M$ podle $x$, nebo funkci $N$ podle $y$ (můžeme si vybrat)
- nezapomenut přidat $c(x)$ pokud integrujeme podle $y$, nebo $c(y)$ pokud integrujeme podle $x$
    $$ F(x,y) = \int{Ndy} =\\= \int{(-{x \over y^2})dy} =\\ ...\\...\\ = \underline{\underline{{x \over y} + c(x)}} $$
- výsledek dosadíme do následujícího vztahu a potřebujeme **vyjádřit**  $c(x)$
- funkci vždy derivujeme podle **opačné proměnné**, než podle které jsme ji integrovali
- na pravou stranu rovnice vždy dosazujeme **tu druhou funkci** ($M$ nebo $N$), než jsme integrovali
    $$
        \begin{aligned}
        {d \over dx}F(x,y) &= M \\
        {d \over dx}({x \over y} + c(x)) &= {1 \over y} + x \\
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

<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" });
</script>