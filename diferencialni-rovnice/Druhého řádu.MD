# Diferenciální rovnice druhého řádu s konstantními koeficienty

## Homogenní tvar

_y_'' - 4<i>y</i> = 0

* Vytvoříme charakteristický polynom a spočteme kořeny

_λ_<sup>2</sup> - 4 = 0<br>_λ_ = ±2

* Výsledek je tvaru _y(x)_ = _c_<sub>1</sub>_e_<sup>_λ_<sub>1</sub>_x_</sup> + _c_<sub>2</sub>_e_<sup>_λ_<sub>2</sub>_x_</sup>

_y(x)_ =  _c_<sub>1</sub>_e_<sup>-2<i>x</i></sup> + _c_<sub>2</sub>_e_<sup>2<i>x</i></sup>

* Pokud _λ_ je _k_-násobný kořen charakteristického polynomu, pak řešením jsou _e_<sup>_λx_</sup>, _xe_<sup>_λx_</sup>, ..., _x_<sup>_k_-1</sup>_e_<sup>_λx_</sup>
* Pokud _λ_ = _α_ ± _βi_, pak _y(x)_ = _e_<sup>_αx_</sup>(_c_<sub>1</sub>sin(_βx_) + _c_<sub>2</sub>cos(_βx_))

## Nehomogenní tvar

* Řešení je součtem homogenního a partikulárního řešení

### Speciální pravá strana: polynom ⋅ exponenciela

* Obecně _y_'' - _a_<sub>1</sub> <i>y</i>' - _a_<sub>2</sub> <i>y</i> = _P(x)_ ⋅ _e<sup>αx</sup>_

#### Příklad I

Vyřešte rovnici _y_'' - 2<i>y</i>' - 3<i>y</i> = -3<i>x</i> + 1

* Rovnici si můžeme představit jako _y_'' - 2<i>y</i>' - 3<i>y</i> = (-3<i>x</i> + 1) ⋅ _e<sup>0x</sup>_
  * _P(x)_ = (-3<i>x</i> + 1)
  * exp = _e<sup>0x</sup>_ ⇒ _α_ = 0
* Nejprve vyřešíme homogenní část (kořeny charakteristického polynomu)
  * Vyjdou nám kořeny -1 a 3
  * _α_ = 0 je nulanásobným kořenem charakteristického polynomu, _m_ je tedy rovno nule
* Hledáme partikulární řešení ve tvaru _e<sup>αx</sup>_ ⋅ _x<sup>m</sup>_ ⋅ _Q(x)_
  * V našem případě _α_ = 0 a _m_ = 0; _Q(x)_ je vždy stejného řádu jako _P(x)_
  * Partikulární řešení je tedy ve tvaru _e<sup>0x</sup>_ ⋅ _x<sup>0</sup>_ ⋅ (_Ax_ + _B_), musíme spočítat jeho první dvě derivace, abychom ho mohli dosadit do zadání
* Dosazením tvaru _y<sub>p</sub>_ a jeho derivací do zadání dopočítáme _A_ a _B_, to dosadíme do tvaru _y<sub>p</sub>_
* Výsledkem je _y<sub>h</sub>_ + _y<sub>p</sub>_

$$
\begin{align*}
y''-2y'-3y&=(-3x+1)\cdot e^{0x} \\
\\
\lambda^2-2\lambda-3&=0 \\
(\lambda+1)(\lambda-3)&=0 \\
y_h&=c_1e^{-x}+c_2e^{3x} \\
\\
\implies m&=0 \\
\implies y_p&=e^{0x}\cdot x^0\cdot(Ax+B) \\
\\
y_p&=Ax+B \\
y_p'&=A \\
y_p''&=0 \\
\\
0-2A-3(Ax+B)&=-3x+1 \\
-2A-3Ax-3B&=-3x+1 \\
-3Ax+(-2A-3B)&=-3x+1 \\
A&=1 \\
-2A-3B&=1 \\
-3B&=3 \\
B&=-1 \\
\implies y_p&=e^{0x}\cdot x^0\cdot(1x-1) \\
\\
y&=c_1e^{-x}+c_2e^{3x}+e^{0x}\cdot x^0\cdot(1x-1) \\
y&=c_1e^{-x}+c_2e^{3x}+x-1
\end{align*}
$$

#### Příklad II

Vyřešte rovnici _y_'' - 2<i>y</i>' - 3<i>y</i> = 4<i>e<sup>-x</sup></i>

* Rovnici si můžeme představit jako _y_'' - 2<i>y</i>' - 3<i>y</i> = (4) ⋅ <i>e<sup>-1x</sup></i>
  * _P(x)_ = 4
  * exp = _e<sup>-1x</sup>_ ⇒ _α_ = -1
* Nejprve vyřešíme homogenní část (kořeny charakteristického polynomu)
  * Vyjdou nám kořeny -1 a 3
  * _α_ = -1 je jednonásobným kořenem charakteristického polynomu, _m_ je tedy rovno jedné
* Hledáme partikulární řešení ve tvaru _e<sup>αx</sup>_ ⋅ _x<sup>m</sup>_ ⋅ _Q(x)_
  * V našem případě _α_ = -1 a _m_ = 1; _Q(x)_ je vždy stejného řádu jako _P(x)_
  * Partikulární řešení je tedy ve tvaru _e<sup>-1x</sup>_ ⋅ _x<sup>1</sup>_ ⋅ (_A_), musíme spočítat jeho první dvě derivace, abychom ho mohli dosadit do zadání
* Dosazením tvaru _y<sub>p</sub>_ a jeho derivací do zadání dopočítáme _A_, to dosadíme do tvaru _y<sub>p</sub>_
  * Po dosazení do zadání by rovnice měly jít vydělit exponencielou
* Výsledkem je _y<sub>h</sub>_ + _y<sub>p</sub>_

$$
\begin{align*}
y''-2y'-3y&=(4)\cdot e^{-1x} \\
\\
\lambda^2-2\lambda-3&=0 \\
(\lambda+1)(\lambda-3)&=0 \\
y_h&=c_1e^{-x}+c_2e^{3x} \\
\\
\implies m&=1 \\
\implies y_p&=e^{-1x}\cdot x^1\cdot(A) \\
\\
y_p&=e^{-x}\cdot x\cdot A \\
y_p'&=e^{-x}(-1)\cdot xA+e^{-x}\cdot A \\
&= e^{-x}(A-xA) \\
y_p''&=(-1)(e^{-x}(-1)\cdot xA+e^{-x}\cdot A)+Ae^{-x}(-1) \\
&= e^{-x}\cdot xA-e^{-x}\cdot A-e^{-x}\cdot A \\
&= e^{-x}(-2A+xA) \\
\\
e^{-x}(-2A+xA)-2e^{-x}(A-xA)-3e^{-x}xA&=4e^{-x} \\
(-2A+xA)-2(A-xA)-3xA&=4 \\
-2A+\cancel{xA}-2A+\cancel{2xA}-\cancel{3xA}&=4 \\
-4A&=4 \\
A&=-1 \\
\implies y_p&=e^{-1x}\cdot x^1\cdot(-1) \\
\\
y&=c_1e^{-x}+c_2e^{3x}+e^{-1x}\cdot x^1\cdot(-1) \\
y&=c_1e^{-x}+c_2e^{3x}-e^{-x}\cdot x
\end{align*}
$$

### Speciální pravá strana: polynom ⋅ exponenciela ⋅ goniometrická funkce

* Pravá strana obecně _P(x)_ ⋅ _e<sup>αx</sup>_ ⋅ sin,cos(_βx_)
* Řešením homogenní rovnice pro _λ_ = _α_ ± _βi_ je ___y<sub>h</sub>_ = _e_<sup>_αx_</sup>(_c_<sub>1</sub>sin(_βx_) + _c_<sub>2</sub>cos(_βx_))__
* Partikulární řešení hledáme ve tvaru ___e<sup>(α+βi)x</sup>_ ⋅ _x<sup>m</sup>_ ⋅ _Q(x)___, kde _m_ je násobnost kořene _α_ ± _βi_ v charakteristickém polynomu
* Partikulární řešení dosazujeme do zadání, kde na pravé straně exponencielu a goniometrickou funkci nahradíme za _e<sup>(α+βi)x</sup>_
* Po úpravě použijeme na _y<sub>p</sub>_ identitau ___e<sup>βix</sup>_ = cos(_βx_) + _i_ ⋅ sin(_βx_)__
* Opecné řešení je pak součet homogenního a
  * imaginární části partikulárního řešení pro rovnice se sinem
  * reálné části partikulárního řešení pro rovnice s kosinem

#### Příklad III

Vyřešte rovnici _y_'' + _y_ = 5<i>e<sup>x</sup></i>sin(_x_).

* Rovnici si můžeme představit jako _y_'' + _y_ = (5) _e_<sup>1<i>x</i></sup></i> sin(1<i>x</i>)
  * _P(x)_ = 5
  * exp = _e_<sup>1<i>x</i></sup></i> ⇒ _α_ = 1
  * gon = sin(1<i>x</i>) ⇒ _β_ = 1
* Nejprve vyřešíme homogenní část (kořeny charakteristického polynomu)
  * Vyjdou nám kořeny ±<i>i</i>
  * _α_ ± _βi_ = 1 ± 1<i>i</i> je nulanásobným kořenem charakteristického polynomu, _m_ je tedy rovno nule
* Hledáme partikulární řešení ve tvaru _e<sup>(α+βi)x</sup>_ ⋅ _x<sup>m</sup>_ ⋅ _Q(x)_
  * V našem případě _α_ = 1 a _m_ = 0; _Q(x)_ je vždy stejného řádu jako _P(x)_
  * Partikulární řešení je tedy ve tvaru _e<sup>(1+1i)x</sup>_ ⋅ _x<sup>0</sup>_ ⋅ _Q(x)_, musíme spočítat jeho druhou derivaci, abychom ho mohli dosadit do zadání
* Tvar _y<sub>p</sub>_ a jeho derivace dosadíme do rovnice, kde levá strana je stejná jako zadání a pravá strana = _P(x)_ ⋅ _e<sup>(α+βi)x</sup>_ (exponenciela a goniometrická funkce nahrazeny _e<sup>(α+βi)x</sup>_), dopočítáme _A_
  * Po dosazení do zadání by rovnice měly jít vydělit exponencielou
  * _y<sub>p</sub>_ můžeme přepsat pomocí identity _e<sup>βix</sup>_ = cos(_βx_) + _i_ ⋅ sin(_βx_)
* Partikulární řešení rovnice se sinem je pouze imaginární část _y<sub>p</sub>_
* Výsledkem je _y<sub>h</sub>_ + ℑ(_y<sub>p</sub>_)

$$
\begin{align*}
y''+y&=5e^x\sin(x) \\
\\
\lambda^2+1&=0 \\
\lambda&=0\pm i \\
\\
\implies m&=0 \\
\implies y_p&=e^{(1+1i)x}\cdot x^0\cdot A \\
\\
y_p&=e^{(1+i)x}\cdot A \\
y_p'&=e^{(1+i)x}\cdot (1+i)\cdot A \\
y_p''&=e^{(1+i)x}\cdot (1+i)(1+i)\cdot A \\
&=e^{(1+i)x}\cdot 2i\cdot A \\
\\
e^{(1+i)x}\cdot 2i\cdot A+e^{(1+i)x}\cdot A&=5e^{(1+i)x} \\
2i\cdot A+ A&=5 \\
A(1+2i)&=5 \\
A&=\frac{5}{1+2i} \\
A&=\frac{5}{1+2i}\frac{1-2i}{1-2i}=\frac{5(1-2i)}{5} \\
A&=1-2i \\
\implies y_p&=e^{(1+i)x}\cdot (1-2i)=e^x\cdot(\cos(x)+i\sin(x))\cdot (1-2i) \\
\\
y&=(c_1\sin(x)+c_2\cos(x))+ℑ(y_p) \\
y&=(c_1\sin(x)+c_2\cos(x))+e^x(\sin(x)-2\cos(x)) \\
\end{align*}
$$

#### Příklad IV

Vyřešte rovnici _y_'' + _y_ = 2cos(_x_).

* Rovnici si můžeme představit jako _y_'' + _y_ = (2) _e_<sup>0<i>x</i></sup></i> cos(1<i>x</i>)
  * _P(x)_ = 2
  * exp = _e_<sup>0<i>x</i></sup></i> ⇒ _α_ = 0
  * gon = cos(1<i>x</i>) ⇒ _β_ = 1
* Nejprve vyřešíme homogenní část (kořeny charakteristického polynomu)
  * Vyjdou nám kořeny ±<i>i</i>
  * _α_ ± _βi_ = 0 ± 1<i>i</i> je jednanásobným kořenem charakteristického polynomu, _m_ je tedy rovno jedné
* Hledáme partikulární řešení ve tvaru _e<sup>(α+βi)x</sup>_ ⋅ _x<sup>m</sup>_ ⋅ _Q(x)_
  * V našem případě _α_ = 0 a _m_ = 1; _Q(x)_ je vždy stejného řádu jako _P(x)_
  * Partikulární řešení je tedy ve tvaru _e<sup>(0+1i)x</sup>_ ⋅ _x<sup>1</sup>_ ⋅ _Q(x)_, musíme spočítat jeho druhou derivaci, abychom ho mohli dosadit do zadání
* Tvar _y<sub>p</sub>_ a jeho derivace dosadíme do rovnice, kde levá strana je stejná jako zadání a pravá strana = _P(x)_ ⋅ _e<sup>(α+βi)x</sup>_ (exponenciela a goniometrická funkce nahrazeny _e<sup>(α+βi)x</sup>_), dopočítáme _A_
  * Po dosazení do zadání by rovnice měly jít vydělit exponencielou
  * _y<sub>p</sub>_ můžeme přepsat pomocí identity _e<sup>βix</sup>_ = cos(_βx_) + _i_ ⋅ sin(_βx_)
* Partikulární řešení rovnice s kosinem je pouze reálná část _y<sub>p</sub>_
* Výsledkem je _y<sub>h</sub>_ + ℜ(_y<sub>p</sub>_)

$$
\begin{align*}
y''+y&=2\cos(x) \\
\\
\lambda^2+1&=0 \\
\lambda&=0\pm i
\\
\implies m&=1 \\
\implies y_p&=e^{(0+1i)x}\cdot x^1\cdot A \\
\\
y_p&=e^{ix}\cdot x\cdot A \\
y_p'&=A(e^{ix}\cdot i\cdot x+e^{ix}) \\
&=Ae^{ix}ix+Ae^{ix} \\
y_p''&=Ai(e^{ix}\cdot i\cdot x+e^{ix})+Aie^{ix} \\
&=Ae^{ix}\cdot (-1)\cdot x+Aie^{ix}+Aie^{ix} \\
&=Ae^{ix}(2i-x) \\
\\
Ae^{ix}(2i-x)+e^{ix}xA&=2e^{ix} \\
A(2i-x)+xA&=2 \\
2iA&=2 \\
A&=-i \\
\implies y_p&=e^{ix}\cdot x \cdot (-i) \\
&=(\cos(x)+i\sin(x))\cdot x\cdot (-i) = (\sin(x)-i\cos(x))\cdot x\\
\\
y&=(c_1\sin(x)+c_2\cos(x))+ℜ(y_p) \\
y&=(c_1\sin(x)+c_2\cos(x))+\sin(x)\cdot x \\
\end{align*}
$$
