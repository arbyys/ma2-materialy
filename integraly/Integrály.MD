# Integrály

## Integrace na trojúhelníku

Integrujte funkci _f(x,y)_ = _x_ + _y_ + (1 + _x_ + _y_)<sup>-3</sup> přes oblast tvořenou trojúhelníkem s vrcholy [0; 0], [1; -1], [2; 0].

### Zjistit hranice integrálů

* Trojúhelník si nakreslíme
* Někdy je potřeba rozdělit si trojúhelník na několik dílů a integrovat zvlášť
* Ideální je, pokud je nějaká strana trojúhelníku rovnoběžná s jednou z os

&nbsp;

* V našem případě je hrana ([0; 0]; [2; 0]) na ose _y_, nejdříve si tedy vytvoříme hranice podle _y_ od -1 do 0 (-1 kvůli bodu [1; -1], 0 kvůli [0; 0] a [2; 0])
* Nyní jsme trojúhelník jakoby ohraničili dvěma přímkami _y_=-1 a _y_=0
* Zbývá trojúhelník ohraničit zleva a zprava, to budou meze integrace podle _x_
  * Zleva se jedná o přímku _x_=-_y_
  * Zprava se jedná o přímku _x_=_y_+2
  * Vyjadřujeme pro tu proměnnou, podle které budeme integrovat, někdy je potřeba vypočítat obecnou rovnici přímky
* Integrál tedy vypadá takto:

<!-- $$
\int_{-1}^0 \! \int_{-y}^{y+2} \! \bigg(x+y+\frac{1}{(1+x+y)^3}\bigg) \, \mathrm{d}x \, \mathrm{d}y
$$ -->

<br><div align="left"><img style="" src="svg\RD4OdVI4Qy.svg"></div><br>

* Písmenka v hranicích by se měla objevovat pouze u vnitřního integrálu, vnitřním integrálem je tedy ten podle _x_
* Pokud je vnitřní integrál podle _x_, v hranicích by se mělo objevovat pouze písmenko _y_ (hranice jsou vyjádřeny pro _x_) a obráceně
* Na konci máme d<i>x</i>d<i>y</i> – nejdřív integrujeme podle _x_ a pak podle _y_

### Spočítat integrál

* Spočteme vnitřní integrál

<!-- $$
\int_{-y}^{y+2} \! \bigg(x+y+\frac{1}{(1+x+y)^3}\bigg) \, \mathrm{d}x =\bigg[ \frac{x^2}{2}+xy+\frac{1}{-2(1+x+y)^2} \bigg]_{-y}^{y+2}
$$ -->

<br><div align="left"><img style="" src="svg\YDH5SGFoXf.svg"></div><br>

* Dosadíme hranice, spočteme vrchní minus spodní

<!-- $$
\begin{align*}
&=\frac{(y+2)^2}{2}+y^2+2y-\frac{1}{2(2y+3)^2}-\bigg( \frac{y^2}{2}-y^2-\frac{1}{2} \bigg)=
\\
&=\frac{y^2}{2}+\frac{4y}{2}+\frac{4}{2}+\frac{2y^2}{2}+\frac{4y}{2}-\frac{1}{2(2y+3)^2}-\frac{y^2}{2}+\frac{2y^2}{2}+\frac{1}{2}=
\\
&=2y^2+4y+\frac{5}{2}-\frac{1}{2(2y+3)^2}
\end{align*}
$$ -->

<br><div align="left"><img style="" src="svg\ZI9cQYOoyG.svg"></div><br>

* Spočteme vnější integrál

<!-- $$
\int_{-1}^0 \! \bigg( 2y^2+4y+\frac{5}{2}-\underbrace{\frac{1}{2(2y+3)^2}}_{t=2y+3; \mathrm{d}y=\mathrm{d}t/2}  \bigg) \, \mathrm{d}y=\bigg[ \frac{2y^3}{3}+2y^2+\frac{5y}{2}+\frac{1}{4(2y+3)}\bigg]_{-1}^0
$$ -->

<br><div align="left"><img style="" src="svg\oZvAqaYa2L.svg"></div><br>

* Dosadíme hranice, spočteme vrchní minus spodní

<!-- $$
\frac{1}{12}-\bigg( -\frac{2}{3}+2-\frac{5}{2}+\frac{1}{4} \bigg)=\frac{1}{12}+\frac{8}{12}-\frac{24}{12}+\frac{30}{12}-\frac{3}{12}=\frac{12}{12}=1
$$ -->

<br><div align="left"><img style="" src="svg\0IgWPOfk8J.svg"></div><br>

## Obecná rovnice přímky

<img src="svg\ObecnaPrimka.PNG" width="534" />
