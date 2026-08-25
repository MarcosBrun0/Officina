---
created: 2026-08-10
modified: 2026-08-24
tags:
  - UENF
  - math
  - computação
---
# Metodologia 
- [[Linguagem Julia]] para resolver problemas 



### Aula 17/08/26
 $$\sqrt(x) - 5e^{-x})$$
 A professora usou derivada para calcular se a função é crescente ou descresente
#### Analise gráfica	$$x^3 -9x +3 = 0$$
$$g(x) = x^3 \newline h(x) = 9x -3$$


bom, tem métodos para achar a raiz:
- método da bissecção
- método da falsa posição

## Aula 24/08/26
### Ordem de convergencia
#### Definição:
 Sejam ${x_k}$ o resultado da aplicação de um método numérico na iteração k e $e_k = |x_k - \bar{x}|$ seu erro. e existirem um número p >= 1 e uma cˆ(te) c>0 tais que 
$$\lim_{k\to\infty}{\frac{|e_{k+1}|}{|e_k|^p}}$$
então p é chamado de ordem de convergência do método.

#### Teorema
O método do ponto fixo tem ordem de convergência linear(p = 1)

obs:
1. O teste $|Q'(x_0)| < 1$ pode levar a um engano se $x_0$ não estiver suficientemente próximo da raiz.
2. A convergência do MPF será mais rápida q menor for o valor de $|Q'(\varepsilon)$

### Metodo de Newton
$$x_{k+1}= x_k - \frac{f(x_r)}{f'(x_k)}$$
==Interpretação gráfica

![[Pasted image 20260824144410.png]]

	A ideia central do método de Newton é: partindo de um ponto inicial x0x_0 x0​, traça-se a reta tangente à curva f(x)f(x) f(x) nesse ponto. Como a tangente é uma boa aproximação local da função, o ponto onde ela cruza o eixo xx x vira a próxima estimativa x1x_1 x1​ — geralmente mais próxima da raiz do que x0x_0 x0​. Repetindo o processo em x1x_1 x1​, obtém-se x2x_2 x2​, e assim por diante, até a sequência convergir para a raiz de f(x)=0f(x) = 0 f(x)=0.


Dado $x_0$ , queremos calcular x , em função de $x_0$ sabendo que x1 srá p ponto no eixo x interceptado pela reta tangente à curva, originad por $x_0$ .
A equação da reta tangente ao gráfico no ponto ($x_0, f(x_0)$) tem inclinação $m = f'(x_0)$

# TO-DO
Comparação entre os métodos 
- f(x) = 0 , f(x) = eˆ(-ax)+xˆ2 -10
- tolerância : E <= 10ˆ(-5)
- intervalo(raiz positiva) : I = [2.4 ,3.5]
- intervalo(raiz negativa): I/2 = [a,b]= ?

Bisseção, Falsa posição, Ponto fixo, Newton e Secante

==Aproveite para criar um programa com todos os metodos 
