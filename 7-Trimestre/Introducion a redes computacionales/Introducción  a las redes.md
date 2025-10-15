3 de Octubre 2025

# Modelo de Sharon
**Fuente**:Crea datos o ya los tiene.
**Transmisor**:Convierte los datos (información) en algo para poderlo transmitir.
**Medio de transmisión**:En este caso es el aire.
**Receptor**:Toma la información para convertirlo y que llegue al destino.
**Destino**:Le llega la información pero esta también puede regresarla. 

Fuente-Transmisor-Medio de transmisión-Receptor-Destino 

## Señales (Digitales/Analógicas)
[[Señales]]

- Señales Digitales: Se representa con dígitos finitos.(Toma valores en un intervalo) 
- Señales Analógicas: Se representan con dígitos infinitos. (Puede tomar cualquier valor) 

Las señales se pueden representar con funciones $f(x)$, continuos o discontinuas son los valores que se puede tomar según el tiempo.

Función continua.
```chart
type: line
title: Función continua f(x) = x²
xTitle: tiempo
yTitle: f(x)
labels: [-3, -2, -1, 0, 1, 2, 3]
series:
  - title: f(x)=x²
    data: [9, 4, 1, 0, 1, 4, 9]
```

Función discontinua 

```plotly
{
  "data": [
    {
      "x": [-3,-2.5,-2,-1.5,-1,-0.5,-0.2],
      "y": [-0.33,-0.4,-0.5,-0.67,-1,-2,-5],
      "type": "scatter",
      "mode": "lines",
      "name": "x < 0",
      "line": {"color": "blue"}
    },
    {
      "x": [0.2,0.5,1,1.5,2,2.5,3],
      "y": [5,2,1,0.67,0.5,0.4,0.33],
      "type": "scatter",
      "mode": "lines",
      "name": "x > 0",
      "line": {"color": "red"}
    }
  ],
  "layout": {
    "title": "Función discontinua f(x) = 1/x",
    "xaxis": {"title": "x", "zeroline": true},
    "yaxis": {"title": "f(x)", "zeroline": true},
    "showlegend": true
  }
}
```


# Amplitud, Fase, Frecuencia y anchos de banda

## Serie de Furrier

Cualquier señal se puede representar con una suma infinita de funciones senoidales.

$f(t)=\sum_{i}^{\infty} a_i(sen(w_it))$

**Espectro**:Es la representación de la energía de una señal es decir es la forma de la señal en donde cada punto de esa grafica se le conoce como <mark style="background: #FF5582A6;">componente</mark>.

> [!NOTE] Información de unidades 
> La intensidad y el voltaje se espera que tenga la misma forma.
> Al hablar de volts y elevarlo nos sale la energía.
> $f(t)=volts,a_i=voltaje,a_i^2=energia$ 
> Si integramos la función de la señal obtendríamos su energía. 
>En términos **prácticos** podemos decir que nada mas recibimos la mitad de la energía.

**Amplitud**:Es el valor máximo que llega a tener la señal con respecto a su punto de equilibrio (Normalmente es 0).

**Fase**:Desplazamiento de las señales.

**Frecuencia**:Ciclos que se completa en un segundo, se mide en Hertz.

**Ancho de banda**:Es el radio de frecuencia en donde se encuentra la mayor cantidad de energía .Es la mitad de la energía ya que en esa parte esta la mayor cantidad de energía por ende de información.

# Velocidad de transmisión vs ancho de banda


- **Ancho de banda** = número de carriles.
-  **Velocidad de transmisión** = cuántos autos pasan por segundo.

#  Atenuación, distorsión y ruido
>[!NOTE] Información
>- Medio de transmisión 
>1.Puede tener anchos de banda.
>2.Puede general un desfasamiento. Cuando sucede esto se le llama <mark style="background: #FFF3A3A6;">distorsión</mark>.
>3.Añade ruido 
>

**Atenuación**:Que pierde energía y si sucede el receptor puede llegar a no detectarlo.
La atenuación disminuye la amplitud de la señal y la distorsión (desfasa)

# Medio de transmisión 


Existe un estándar para la creación de las arquitectas de redes las cuales se llaman [[Modelos de referencia]]

Ademas de eso cada una de esas debe tener