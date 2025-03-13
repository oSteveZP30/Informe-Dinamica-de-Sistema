# Fracciones parciales método resumido:
La transformada inversa como ya se había mencionado anteriormente es una técnica que nos permite obtener la función original, es decir de una función de dominio de frecuencia compleja la convierte en una función de dominio del tiempo, lo opuesto a la transformada de Laplace. A continuación se explicará de forma breve la manera de realizar ejercicios por medio de la transformada inversa con diferentes casos.

## 1. Mètodo resumido: 
Se debe factorizar las raíces del polinomio del numerador, de esta manera disminuye el sistema de ecuaciones a solucionar al identificar valores de s y así poder eliminar algunos términos. 
### 1. 1 Caso de raíces reales diferentes:
Es importante buscar los valores del denominador que deben ser lineales diferentes y se cancelen.

$$F(s) = \frac{A(s)}{B(s)} = \frac{a_1}{s+p_1} + \frac{a_2}{s+p_2} + \cdots + \frac{a_n}{s+p_n}$$

Sabiendo que $\( a_k \) (\( k = 1, 2, 3, \ldots \))$ son constantes, $\( a_k \)$ puede hallarse multiplicando ambos lados de la igualdad por $\( (s+p_k) \)$ y haciendo $\( s = -p_k \)$, de lo cual se obtiene:

$$\left[ (s + p_k) \left( \frac{A(s)}{B(s)} \right) \right]_{s = -p_k} = \left[ \frac{a_1}{s + p_1} \right] (s + p_k) + \left[ \frac{a_2}{s + p_2} \right] (s + p_k) + \cdots + \left[ \frac{a_k}{s + p_k} \right] (s + p_k)$$

$$+ \cdots + \left[ \frac{a_k}{s + p_k} \right] (s + p_k) \Big|_{s = p_k} = a_k$$

$$a_k = \left[ (s + p_k) \frac{A(s)}{B(s)} \right]_{s = -p_k}$$

Se cancelan todas menos $$a_k$$

### Transformada inversa caso 1

De la tabla de transformadas
$$f(t) = L^{-1}\{F(s)\} \)$$ $$( F(s) = L\{f(t)\} \)$$

$$2e^{at} \)$$  $$\frac{1}{s-a}$$

$$L^{-1}\left\[\frac{a_k}{s+p_k}\right\] = a_k e^{-p_k t}$$

$$f(t) = L^{-1}[F(s)] = a_1 e^{-p_1 t} + a_2 e^{-p_2 t} + \cdots + a_n e^{-p_n t}$$

### 💡Ejemplo 1:

Obtenga la transformada inversa de:

$$F(s) = \frac{s+3}{(s+1)(s+2)}$$

$$\frac{s+3}{(s+1)(s+2)} = \frac{A}{\frac{s+1}{-1}} + \frac{B}{\frac{s+2}{-2}}$$

$$\left[(s+1) \frac{s+3}{(s+1)(s+2)}\right]_{s=-1} = A = \frac{(-1)+3}{-1+2} = 2$$

Igual para B:

$$\left[(s+2) \frac{s+3}{(s+1)(s+2)}\right]_{s=-2} = B = \frac{(-2)+3}{-2+1} = \frac{-1}{1} = -1$$

$$\frac{2}{s+1} - \frac{1}{s+2}$$

$$= 2L^{-1}\left\[\frac{1}{s+1}\right\] - L^{-1}\left\[\frac{1}{s+2}\right\]$$

$$= 2e^{-t} - e^{-2t}$$

### 1.2 Caso de raíces reales iguales:
Se puede aplicar el mismo principio, pero teniendo en cuenta los exponente. 
### 💡Ejemplo 2:

$$F(s) = \frac{s^2 + 2s + 3}{(s+1)^3}$$

$$F(s) = \frac{A(s)}{B(s)} = \frac{b_3}{(s+1)^3} + \frac{b_2}{(s+1)^2} + \frac{b_1}{s+1}$$

$$(s+1)^3 \frac{A(s)}{B(s)} = b_3 + b_2(s+1) + b_1(s+1)^2$$

tomamos s=-1

$$\frac{(s+1)^3 (s^2 + 2s + 3)}{(s+1)^3} \bigg|_{s=-1} = A = (-1)^2 + 2(1) + 3 = 2=A$$

Para el siguiente tèrmino se deriva u se evalua en s=-1

$$\frac{d}{ds} \left[ (s+1)^3 \frac{A(s)}{B(s)} \right]_{s=-1} \frac{d}{ds} \left[ A + B(s+1) + C(6+1)^2 \right]{s=-1}$$

$$\left[(s+1)^{3} \frac{A(s)}{B(s)}\right]_{s=-1} = 0 +B + 2C(s+1)$$


$$0 = B + 2C(s+1)$$

$$0 = B + 2C(-1+1)$$

$$ B = 0$$

Deerivamos nuevamente: 

$$\frac{d}{ds} \left[ (s+1)^2 \frac{A(s)}{B(s)} \right]{s=-1} = \frac{d}{ds} \left[ B + 2C(s+1) \right]{s=-1} = 2C$$

$$2C = \left[ (s+1)^2 \frac{A(s)}{B(s)} \right]_{s=-1}$$

$$2C = \left[ \frac{s^2 + 2s + 3}{s+1} \right]_{s=-1}$$
$$ c=\frac{2}{2}= 1$$

$$L^{-1}\left[\frac{2}{(s+1)^{3}}\right] + L^{-1}\left[\frac{1}{s+1}\right]$$

$$s+1-> s$$

$$e^{-t}$$

$$\frac{1}{s^{3}}= \frac{n!}{s^{n+1}}= t^{n}$$


$$\frac{1}{2!} \frac{2!}{s^{2+1}}$$

$$2 \frac{1}{2} t^{2}$$


### 1.3 Caso 3: raìces complejas conjugadas
Para este se puede completar el cuadrado

$$F(s) = \frac{2s + 12}{s^2 + 2s + 5}$$

Si las raíces son complejas tal que:

$$s^2 + 2s + 5 = (s+1+j2)(s+1-j2)$$

### 💡Ejemplo 3:

$$F(s) = \frac{2s + 12}{s^2 + 2s + 5} = \frac{2s + 12}{(s+1)^2 + 4}$$

Se saca trinomio cudrado perfecto:

$$s^{2}+2s+1-1+5 = (s+1)^{2}4$$ 

Ahora modificamos el numerador para el seno y coseno amortiguado:

$$F(s) = \frac{10 + 2(s+1)}{(s+1)^2 + 4} = \frac{10}{(s+1)^2 + 4} + \frac{2(s+1)}{(s+1)^2 + 4}$$

$$= 10 \mathcal{L}^{-1}\left\[\frac{1}{(s+1)^2 + 2^2}\right\] + 2 \mathcal{L}^{-1}\left\[\frac{s+1}{(s+1)^2 + 2^2}\right\]$$

$$= 10 e^{-t} \left\[\frac{1}{2} \sin(2t)\right\] + 2 e^{-t} \cos(2t)$$

$$= 5 e^{-t} \sin(2t) + 2 e^{-t} \cos(2t)$$


## 2.Matlab: 
Es un entorno de programación y cálculo desarrollado por MathWorks, tiene un lenguaje de programación propio y permite desarrollar operaciones con matrices y vectores, que facilita cálculos matemáticos complejos, también cuenta con herramientas para crear gráficos en 2D y 3D.

### 2.1 Fracciones parciales de Matlab:
Al conocer los polinomios del numerador y denominador de la función de dominio s puede calcular los términos de las fracciones parciales. 

r => términos del numerador

p => términos del denominador

k => términos independientes










