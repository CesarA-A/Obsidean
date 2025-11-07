---
Date: 2025-10-06
tags:
---
---

Tenemos 16 millones de posibles direcciones, pero es mas recomendable dividirlo.

**Tipos de **

- A: 255.0.0.0
- B: 255.255.0.0
- C: 255.255.255.0

**Marcara**
identificador de red.
Cuantos bits se tiene en el prefijo, para poder estimar o suponer que fue segmentada
Ejemplos


Este es de clase A, por que segmento la red
*108.130.1.1 / 255.192.0.0*

 255.192.0.0

255 tiene 8 ceros
192 lo pasamos a binario por  lo que tiene dos ceros

***Resultado***
108.130.1.1/10 {sale de sumar los unos que tiene}

---
*iP=128.1.1.56/Mascara=255.255.192.0*

255.255.192.0
255: 8 ceros
255: 8 ceros
192: 2  ceros

***Resultado***
128.1.1.56/18

Es de  tipo B con 18 bits de la trama 

---
Que prefijo tiene 
192.16.182.19/24


---
>[!Note] IP
>Las direcciones ip tiene 32 bits

ID de las clases 
A = 0 > 128 host 24
B = 128 >192 host 16
C = 192 >224 host 8
D = 224 > 239
E = 240 > 255

---

*192.16.182.19/255.255.255.192*

Como el primero es 192 y se encuentra en el intervalo de C tiene 24 bits de marcara pero nos damos cuenta que no concuerda con la que nos da

2^8  -2 =254

Entonces nos damos cuenta que tomaron otros dos bits (debería se 24 pero nos salio 26), 2^2 esto nos dice que tenemos 4 **redes o subredes**


---
172.8.4.7/<mark style="background: #FFB86CA6;">22</mark>

Mascara
255.255.252 = <mark style="background: #FFB86CA6;">22</mark> ceros

Es de clase B por lo que su prefijo debería ser 16 entonces (22 - 16) tenemos 2^6 subredes

---

Para saber la <mark style="background: #BBFABBA6;">dirección de la red</mark> aplicamos el and


192.168.20.238(11101110) and 255.255.255.11110000


## Preguntas examen cual es una direccion de red

Para sacar la dirección de ip:

IP and Mascara



-  
 