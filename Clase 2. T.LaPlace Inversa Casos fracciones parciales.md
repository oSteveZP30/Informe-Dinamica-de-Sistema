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

$$2s^2 + 6s + 5 = As^2 + 2As + A + Bs^2 + 3Bs + 2B + Cs + 2C$$


2 = A + B <span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span>A= 2 - B

6 = 2A + 3B + C<span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span>                6 = 2(2 - B) + 3B + C

<span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span>6= 4-2B + 3B + C

5 =A + 2B + 2C<span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;2 =B + C

<span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span> B= 2 - C

A =2-1

A = 1<span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;5= 2 - B + 2(2 - C) + 2C 


<span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span>5 = 2 - B + 4 

C = 2- B <span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;&nbsp;</span><span>&nbsp;&nbsp;B = 2 - 5 + 4

$$C = 2 - 1 B= 1$$

C = 1


$$\frac{2s^2 + 6s + 5}{(s+2)(s+1)^2} = \frac{1}{s+2} + \frac{1}{s+1} + \frac{1}{(s+1)^2}$$

### Transformada Inversa de Laplace

$$L^{-1}\left[\frac{1}{s+2} + \frac{1}{s+1} + \frac{1}{(s+1)^2} \right] = L^{-1}\left\[\frac{1}{s+2}\right\] + L^{-1}\left\[\frac{1}{s+1}\right\] + L^{-1}\left\[\frac{1}{(s+1)^2}\right\]$$

$$= e^{-2t} + e^{-t} + te^{-t}$$

## Caso 3:
Q(s) tiene raìces complejas conjugadas:

$$G(s)=\frac{P(s)}{Q(s)}=\frac{P(s)}{(s^{2}+b_{1}s+c_{1})(s^{2}+b_{2}s+c_{2})....(s+b_{n}s+c_{n})} $$

La descomposiciòn en fracciones parciales es de la forma: 

$$G(s) = \frac{As + B}{(s^2 + b_1s + c_1)} + \frac{Cs + D}{(s^2 + b_2s + c_2)} + \cdots + \frac{Ms + N}{(s^2 + b_ns + c_n)}$$

### Ejercicio 3: Transformada Inversa

$$G(s) = \frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)}$$

$$\frac{s^2 + 2s + 3}{(s^2 + 2s + 2)(s^2 + 2s + 5)} = \frac{As + B}{s^2 + 2s + 2} + \frac{Cs + D}{s^2 + 2s + 5}$$

$$s^2 + 2s + 3 = (As + B)(s^2 + 2s + 5) + (Cs + D)(s^2 + 2s + 2)$$

$$s^2 + 2s + 3 = As^3 + 2As^2 + 5As + Bs^2 + 2Bs + 5B + Cs^3 + 2Cs^2 + 2Cs + Ds^2 + 2Ds + 2D$$


$$\begin{aligned}0= A + C &&&& A = -C \end{aligned}$$

$$\begin{aligned}1= 2A + B + 2C + D\end{aligned}$$

$$\begin{aligned}2= 5A + 2B + 2C + 2D &&&& 1 = -2C + B + 2C + D\end{aligned}$$
$$\begin{aligned}3= 5B + 2D &&&&& 1 &= -2C + B + 2C + D\end{aligned}$$
$$\begin{aligned}&&&& 1 = B + D\end{aligned}$$

$$\begin{aligned}2 = 5(-C) + 2(1 - D) + 2C + 2D &&&&& B &= 1 - D\end{aligned}$$
$$\begin{aligned}2 = -5C +2- 2D + 2C + 2D&&&&&&&&&&&&&\end{aligned}$$ 
$$\begin{aligned}2 = -3C + 2 &&&&& 3 &= 5(1 - D) + 2D &&&&&\end{aligned}$$
$$\begin{aligned}0 = - 3C &&&&& 3= 5 - 5D + 2D&&&&&&&&&&&&&&&&\end{aligned}$$
$$\begin{aligned}C = 0 &&&&& 3 =  5-3D &&&&&&&&&& D= \frac{2}{3}&&&&&&&\end{aligned}$$
$$\begin{aligned}&& -2 = -3D&&&&&&&&&&&&&&&&\end{aligned}$$
$$\begin{aligned}A= 0 &&&&& \frac{-2}{-3}= D&&&&&&&B=1\frac{-2}{3}\end{aligned}$$
$$\begin{aligned}B = \frac{1}{3}\end{aligned}$$
$$\frac{\frac{1}{3}}{s^{2+2s+2}}+\frac{\frac{2}{3}}{s^{2}+2s+5}$$

$$L^{-1}\left\[\frac{\frac{1}{3}}{s^2 + 2s + 2} + \frac{\frac{2}{3}}{s^2 + 2s + 5}\right\] = L^{-1}\left\[\frac{\frac{1}{3}}{s^2 + 2s + 2}\right\] + L^{-1}\left\[\frac{\frac{2}{3}}{s^2 + 2s + 5}\right\]$$


Operamos el denominador para que quede más sencillo de expresar:

$$s^2 + 2s + 2$$

Tomamos primero los 2 primeros términos y le agregamos y restamos 1:

$$s^2 + 2s + 1 - 1 + 2 = (s+1)^2 + 1$$

Juntamos las 2 expresiones y operamos:

$$s^2 + 2s + 5 = s^2 + 2s + 1 - 1 + 5 = (s+1)^2 + 4$$

Ahora para poder operar estas transformadas:

$$L^{-1}\left\[\frac{\frac{1}{3}}{(s+1)^2 + 1}\right\] + L^{-1}\left\[\frac{\frac{2}{3}}{(s+1)^2 + 4}\right\]$$

Sabemos que la transformada inversa de:

$$L^{-1}\left\[\frac{a}{(s+c)^2 + a^2}\right\] = e^{-ct} \sin(at)$$

Para nuestra casa, los términos son \((s+1)^2 + a^2\). Esto nos dice que la transformada de la placa, la cual introducimos es:

$$ L^{-1}\left\[\frac{1}{(s+c)^2 + a^2}\right\] = e^{-ct} \frac{\sin(at)}{a}
$$

Entonces:

$$= \frac{1}{3} e^{-t} \sin(t) + \frac{2}{3} e^{-t} \frac{\sin(2t)}{2}$$

Finalmente:

$$= \frac{1}{3} e^{-t} \sin(t) + \frac{1}{3} e^{-t} \sin(2t)$$

# Ejercicios propios:
## 📚Ejercicio 1: 
Obtenga la \( T \) inversa de

$$G(s) = \frac{5-4}{s^4 - 9s^2} = \frac{5-4}{s^2(s^2 - 9)} = \frac{5-4}{s^2(s-3)(s+3)}$$

$$\frac{5-4}{s^2(s-3)(s+3)} = \frac{A}{s} + \frac{B}{s^2} + \frac{C}{s-3} + \frac{D}{s+3}$$



$$5-4 = A(s)(s-3)(s+3) + B(s-3)(s+3) + C(s^2)(s+3) + D(s^2)(s-3)$$

$$5-4 = As(s^2-9) + B(s^2-9) + Cs^3 + 3Cs^2 + Ds^3 - 3Ds^2$$

$$5-4 = As^3 - 9As + Bs^2 - 9B + Cs^3 + 3Cs^2 + Ds^3 - 3Ds^2$$



$$\begin{aligned} 0 &= A + C + D &&&& D = -A - C\end{aligned}$$

$$\begin{aligned}1= -9A\end{aligned}$$
$$\begin{aligned}A= \frac{-1}{9}&&&&0=\frac{4}{9} + 3C - 3(-A-C)\end{aligned}$$
$$\begin{aligned}-4 =-9B&&&&0=\frac{4}{9} + 3C + 3(\frac{-1}{9})+3C\end{aligned}$$
$$\begin{aligned}B = \frac{4}{9}&&&& 0 = \frac{4}{9} + 6C(\frac{-3}{9})=\frac{4}{9} + 6C (\frac{-1}{3})\end{aligned}$$ 
$$\begin{aligned} 0 &= B + 3C - 3D &&&& 0 = \frac{1}{9} + 6C\end{aligned}$$
$$-9A = 0$$ 
-9B &= -4
\end{aligned}
$$

$$\frac{5-4}{s^2(s-3)(s+3)} = \frac{\frac{1}{9}}{s}+\frac{\frac{4}{9}}{s^2} - \frac{\frac{1}{54}}{s-3} + \frac{\frac{1}{54}}{s+3}$$

$$(\frac{-1}{9})L^{-1}\left\[\frac{1}{s}\right\] + (\frac{4}{9})L^{-1}\left\[\frac{1}{s^2}\right\] + (\frac{1}{54}) L^{-1}\left\[\frac{1}{s-3}\right\] + (\frac{7}{54})[\frac{1}{s+3}]$$

$$= -\frac{1}{9} + \frac{4}{9}t - \frac{1}{54}e^{3t} + \frac{1}{54}e^{-3t}$$

## 📚Ejercicio 2:
Obtenga la transformada inversa de:

$$G(s) = \left(\frac{s+1}{s^2}\right)^2 = \frac{s^2 + 2s + 1}{s^6} = \frac{s^2}{s^6} + \frac{2s}{s^6} + \frac{1}{s^6}$$

$$ \frac{1}{s^4} + \frac{2}{s^5} + \frac{1}{s^6}= L^{-1}\left\[\frac{1}{s^4}\right\] + 2 L^{-1}\left\[\frac{1}{s^5}\right\] + L^{-1}\left\[\frac{1}{s^6}\right\]$$

$$=\frac{1}{3!}\frac{3!}{s^{3+1}}= \frac{1}{6}t^{3}= 2\frac{1}{4!} \frac{4!}{s^{4+1}}=\frac{1}{24}t^{4=\frac{1}{5!}}\frac{5!}{s^{5+1}}-\frac{1}{120}t^{5}$$

$$=\frac{1}{6}t^{3}+\frac{1}{12}t^{4}+\frac{1}{120}t^{5}$$

## 📚Ejercicio 3:

$$G(s) = \frac{2s - 5}{s^2 + 36} = \frac{2s}{s^2 + 36} - \frac{5}{s^2 + 36}$$

$$2 L^{-1}\left\[\frac{2s}{s^2 + 36}\right\] -  5 L^{-1}\left\[\frac{1}{s^2 + 36}\right\]$$

$$2 L^{-1}\left\[\frac{2s}{s^2 + 36}\right\] - (\frac{1}{6}) L^{-1}\left\[\frac{6}{s^2 + 6^2}\right\]$$

$$= 2\cos(6t) - \frac{5}{6}\sin(6t)$$

