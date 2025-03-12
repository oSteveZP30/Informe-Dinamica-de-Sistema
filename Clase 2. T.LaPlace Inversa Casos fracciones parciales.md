# Descomposicion en fracciones parciales:

La descomposición en fracciones parciales es un método que consiste en expresar una fracción racional (el cociente de dos polinomios) como la suma de fracciones más simples, cuyos denominadores son factores del denominador original. Esto facilita operaciones como la integración y la transformada inversa de Laplace.

## La descomposicion en fracciones parciales se divide en 4 casos:

## Caso 1:

Q(s) tiene raíces reales distintas (Denominador con factores lineales).

$$ G(s)=\frac{P(s)}{Q(s)}=\frac{P(s)}{(s+p_{1})(s+p_{2})....(s+p_{n})} $$

Cada factor lineal $(s+p_{n})$ en el denominador tiene una fraccion parcial correspondiente de la forma:

$$ G(s)=\frac{P(s)}{Q(s)}=\frac{A}{(s+p_{1})}+\frac{B}{(s+p_{2})}+....+\frac{N}{(s+p_{n})} $$

### Ejercicio 1: Obtenga la transformada inversa de:

$$ G(s)=\frac{2s^2-4}{(s+1)(s-2)(s-3)} $$
$$ \frac{2s^2-4}{(s+1)(s-2)(s-3)}=\frac{A}{s+1}+\frac{B}{s-2}+\frac{C}{s-3} $$

$$ 2s^2=A(s-2)(s-3)+B(s+1)(s-3)+C(s+1)(s-2)$$
$$ s=2 $$
$$ 2(2)^2=A((2)-2)((2)-3)+B((2)+1)((2)-3)+C((2)+1)((2)-2) $$
$$ 4=-3B$$
$$ B=-\frac{4}{3} $$


$$ s=-1 $$
$$ 2(-1)^2=A((-1)-2)((-1)-3)+B((-1)+1)((-1)-3)+C((-1)+1)((-1)-2)$$
$$ -2=A(-3)(-4) $$
$$ -2=12A$$
$$ A=-\frac{2}{12} $$
$$ A=-\frac{1}{6} $$


$$ s=3 $$
$$ 2(3)^2=A((3)-2)((3)-3)+B((3)+1)((3)-3)+C((3)+1)((3)-2)$$
$$ 14=4C $$
$$ C=\frac{14}{4} $$
$$ A=\frac{7}{2} $$


$$ \frac{2s^2-4}{(s+1)(s-2)(s-3)}=-\frac{\frac{1}{6}}{s+1}-\frac{\frac{4}{3}}{s-2}+\frac{\frac{7}{2}}{s-3} $$

Ahora aplicamos la transformada de laplace inversa:

$$ =-L^{-1}\left[ \frac{\frac{1}{6}}{s+1} \right] - L^{-1}\left[ \frac{\frac{4}{3}}{s-2} \right] + L^{-1}\left[ \frac{\frac{7}{2}}{s-3} \right] $$

$$ =-\frac{1}{6}e^{-t}-\frac{4}{3}e^{2t}+\frac{7}{2}e^{3t} $$


## Caso 2:

Q(s) tiene n raíces reales repetidas (Denominador con un factor repetido).

$$ G(s)=\frac{P(s)}{Q(s)}=\frac{P(S)}{(s+p)^n} $$

La descomposición en fracciones parciales es de la forma:

$$ G(s)=\frac{A}{(s+p)}+\frac{B}{(s+p)^2}+....+\frac{N}{(s+p)^n} $$


### Ejercicio 2: Obtenga la transformada inversa de:

$$ G(s)=\frac{2s^2+6s+5}{(s+2)(s+1)^2} $$
$$ \frac{2s^2+6s+5}{(s+2)(s+1)^2}=\frac{A}{s+2}+\frac{B}{s+1}+\frac{C}{(s+1)^2} $$

$$ 2s^2+6s+5= A(s+1)^2+B(s+2)(s+1)+C(s+2) $$

















