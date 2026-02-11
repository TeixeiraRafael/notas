---
tags:
  - física
  - conceito
---
Um Movimento Harmônico Simples (MHS) é um tipo básico de oscilação, definido como um movimento retilíneo e periódico que ocorre quando uma força restauradora atua sobre um corpo, de forma proporcional ao seu deslocamento em torno de uma posição de equilíbrio mas no sentido oposto.

Como veremos a seguir, a maioria das equações que modelam o comportamento de um MHS envolvem ângulos, fases e frequências angulares. No primeiro momento isso pode não fazer sentido, de onde viria um ângulo e um movimento que é, por definição, retilíneo? Acontece que todo movimento oscilatório pode ser estudado como a "sombra"de um movimento circular uniforme. É dessa relação se surgem os ângulos nas equações que descrevem seu comportamento.

Como a figura mostra, para cada ponto do eixo X existe um ângulo θ correspondente no círculo.

![[MHS como Projeção de um MCU.png]]

A partir dessa projeção, podemos descrever cada posição do corpo no eixo x em função do cosseno do ângulo θ e a amplitude `A` do movimento, da seguinte forma:
$$\cos(\phi) = \frac{x}{A}$$$$x = \cos(\phi) * A$$
Para analisarmos o comportamento do corpo ao longo do tempo, precisamos adicionar mais alguns termos no argumento da função cosseno, um deles é a frequência angular ω, o instante no tempo `t` e a constante de fase φ. Sendo assim, a função que descreve a posição ao longo do tempo é: 
$$x(t) = x_{m}*\cos(\omega t + \varphi)$$
O termo ωt representa a variação do ângulo em função do tempo, é a parte "dinâmica" da definição, que se refere ao movimento em si, a constante de fase serve como uma espécie de correção do cálculo, indica onde o corpo estava no instante `t = 0`, sem esse termo, a equação só seria capaz de descrever movimentos de corpos cuja posição inicial é o deslocamento máximo (xm).

No MHS definimos o Período (T) como o tempo necessário para completar um ciclo de oscilação completo. E a frequência (f) como o inverso do período, representando a quantidade de oscilações por segundo:
$$f = \frac{1}{T} [Hz]$$

Podemos então inferir que uma partícula retorna para a sua posição inicial a cada "Período" de tempo. Aplicando essa relação na função da possição do corpo, podemos definir a frequência angular em termos do período de oscilação: 
$$x(t) = x_{m}\cos(\omega t + \varphi) = x_{m}\cos(\omega(t+T) + \varphi)$$
A função cosseno, que descreve o movimento do corpo, volta a ter o mesmo valor a cada incremento da fase por 2π, portanto podemos definir a igualdade:
$$
\cos(\omega t + \varphi) = \cos(\omega (t+T) + \varphi) = \cos(\omega t+\varphi+2\pi)
$$
Simplificando os cossenos temos:
$$\omega (t+T)+\varphi=\omega t + \varphi + 2\pi$$

Podemos também simplificar os termos da constante de fase φ:
$$\omega (t+T) = \omega t + 2\pi$$

Então:
$$\omega t + \omega T = \omega t + 2\pi$$

$$\omega T = 2\pi$$

$$\omega = \frac{2\pi}{T} = 2\pi f$$

