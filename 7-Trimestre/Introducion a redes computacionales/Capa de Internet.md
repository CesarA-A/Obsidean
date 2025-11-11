---
Date: 2024-11-11
tags:
---
---

IP publicas -> Todo mundo puede verlas
IP privadas -> Nadamas en un campo se pueden ver.

---

# Marcara de subred  de Longitud Variable

El criterio que vamos a usar es tratando de desperdiciar la menor cantidad de IPs.

Suponga que se tienen la siguiente direccion de red:

148.206.0.0

y que se tiene 2550 host  para dos posibles escenarios:

a(Se planea contar con red con 750 hostd.
b) Se requiere de 16 subredes o redes cada una de al menos 200 host.rft5g3NN

>[!note] 
>La ultima se usa como puerta de enlace para los demas hosts

**Este es el caso a)**
La primera los indica la red y el ultimo el broadcast.

1 red - 750 -> Vamos a necesitar 10 bits
16 redes - 200  

Entonces son 17 redes por lo que vamos a necesitar 5 bits (2^5=32)

A # Max_redes

5 bits de 16 = 16 +5 = 21 bits para hosts

(2^5)32 redes 2^11 -2 = 2046

Con esto vamos a desaprovechar muchas direcciones IP por lo que vamos a necesitar 

148.206.0.0/21
148.206.8.0/21
148.206.16.0/21
148.206.24.0/21
...
148.206.248.0/21

La ultima de la dirección de red se hace:

Restando le un 1 a la primera dirección de IP


Host que sobran 
(2^11 -2) - 750 aprox 1300
(2^11 -2) - 200 aprox 18461


**Este es el caso b**

750 10 bits
	2^10 - 2 = 1022

Son  6 que vamos a tomas para la red por lo que se lo sumamos a 16 
148.206.0.0/22

Se avanza de 4 en cuatros por que de nuestro octeto tomamos 6 entonces
<mark style="background: #FF5582A6;">0 0 0 0 0 0</mark> 0 0 :El primer elemento es del primer bit de lo rojo

148 . 206 .0 .0/22
148 . 206 .4 .0/22
148 . 206 .8 .0/22
148 . 206 .12 .0/22



>[!note] Uso
>Casi simpre sera el numero maximo de host



