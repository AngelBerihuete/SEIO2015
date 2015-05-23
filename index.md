---
framework   : revealjs
revealjs    : {theme: night, transition: none, center: "false"} 
highlighter : highlight.js
hitheme     : github
widgets     : [mathjax]
mode        : selfcontained
url         : {lib: ./libraries}
knit        : slidify::knit2slides
assets      :
  js        :
    - "http://ajax.googleapis.com/ajax/libs/jqueryui/1.10.3/jquery-ui.min.js"
    - "http://bartaz.github.io/sandbox.js/jquery.highlight.js"
github      :
  repo      : SEIO2015
  user      : AngelBerihuete

---

<a href="http://github.com/AngelBerihuete/SEIO2015"><img style="position: absolute; top: 0; right: 0; border: 0;" src="https://camo.githubusercontent.com/365986a132ccd6a44c23a9169022c0b5c890c387/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f7265645f6161303030302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_right_red_aa0000.png"></a>

## Estimación de parámetros físicos en estrellas de baja masa

<br>

en el marco de la misión espacial GAIA

<br>

<small> [A. Berihuete](http://github.com/AngelBerihuete/SEIO2015), L. M. Sarro, A. Suárez, D. Barrado, C. Carrión, M. Sánchez </small>

---

## Esquema de la presentación

1. Contexto: ¿qué es la misión espacial GAIA?
2. Los datos: ¿qué son las estrellas de baja masa?
3. Estimación parámetrica. Principales  resultados.
4. Trabajo actual y futuro.

---

## La misión espacial GAIA

<font size="6">
<div class="fragment grow">
El reto: un censo de mil millones de estrellas
</div>
</font>

<br>

<ol>
    <li><font color = "red"> Reto tecnológico: </font></li>
    <ul>
    <li> Gaia trazará un mapa de las estrellas desde el punto de  Lagrange L2, a una distancia de unos 1.5 millones de kilómetros de la Tierra.
    </li>
    <li>
    106 CCDs con 8 millones de pixels cada uno.
    </li>
    <li>
    Transmitirá, durante 5 años, 50 Gb diarios. Al final de la misión, el archivo de datos excederá el Petabyte.
    </li>
    </ul>
    <li><font color = "red"> Reto científico: </font></li>
    <ul>
    <li>
    Se registrarán un total de 70 mil millones de observaciones, cada una de ellas compuesta a su vez de varios conjuntos de medidas.
    </li>
    <li>
    La astrometría será la mejor conseguida hasta ahora.
    </li>
    <li>
    La astroestadística, se ha convertido en eslabón fundamental para el estudio de esta ingente cantidad de datos.
    </li>
    </ul>
</ol>

--- &twocol

## La misión espacial GAIA

*** =left

<img src='DPAC1.png' />

*** =right

<img src='DPAC2.png' />

*** =fullwidth

<br>

Consorcio para el procesado de datos (DPAC)

--- &twocol

## La misión espacial GAIA

CU8 está encargada de la determinación de parámetros astrofísicos. Dichos parámetros se determinan a partir de varios módulos en un  pipeline llamado [Apsis](http://www.aanda.org/articles/aa/abs/2013/11/aa22344-13/aa22344-13.html)

<br>

*** =left

<div>
    <img src='cu8.png' />
</div>

*** =right

.fragment El módulo [Apsis](http://www.aanda.org/articles/aa/abs/2013/11/aa22344-13/aa22344-13.html) incluye una clasificación inicial de los objetos en grandes categorías, e integra módulos para estimar parámetros astrofísicos dentro de cada una de esas categorías.

--- &twocol

## El módulo UCD: estrellas enanas ultra frías

<br>

***=left

<figure>
<div style='text-align: center;'>
    <img src='BrownDwarfs.png' />
</div>
<figcaption><small>
Wikipedia
</small></figcaption>
</figure>

***=right

.fragment <font color="red">Contexto:</font>  GAIA contendrá un vasto número de objetos, incluyendoestrellas enanas ultrafrías (temperatura por debajo de 2500 K)

.fragment <font color="red">Objetivo:</font> Abordar la precisión de las estimaciones de la temperatura y gravedad obtenidas a partir de modelos y observaciones actuales.

--- &twocol

## El módulo UCD: estrellas enanas ultra frías

***=left

<figure>
<div style='text-align: center;'>
    <img height='320' src='BrownDwarfs.png' />
</div>
<figcaption><small>
Wikipedia
</small></figcaption>
</figure>

***=right

### 

<figure>
<div style='text-align: center;'>
    <img height='320' src='EvolutionaryTracks.png' />
</div>
<figcaption><small>
Tracks evolutivos. DOI: 10.1051/0004-6361/201219867
</small></figcaption>
</figure>

---

## Datos para el módulo UCD, ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl.
</small></figcaption>
</figure>

<br>

Bibliotecas de modelos estelares y los espectros sintéticos asociados
ofrecen un conjunto homogéneo que cubren uniformemente el espacio de
parámetros.

---

## Datos para el módulo UCD, ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl.
</small></figcaption>
</figure>

<br>

Estas bibliotecas parametrizan los modelos con magnitudes físicas (temperatura efectiva, gravedades, y metalicidades)

.fragment Son imperfectas, ya que no pueden reproducir exactamente todas las características de un espectro real UCD.

---

## Datos para el módulo UCD, ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl.
</small></figcaption>
</figure>

<br>

Los tipos espectrales pueden inferirse sin el uso de modelos sintéticos, pero el camino de espectro a los parámetros físicos necesitan de éstas para su correcta interpretación.

.fragment Dado el espectro de baja resolución de GAIA, la mayoría de las características utilizadas para decidir el tipo espectral permanecen no resueltas o innobservadas. Hay que tener cuidado con las interpretaciones.

---

## Datos para el módulo UCD, ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl.
</small></figcaption>
</figure>

<br>

Los modelos sintéticos definen la relación entre los espcetros observados por GAIA y los parámetros que queremos estimar $T_{eff}$ y $\log (g)$,  temperatura y gravedad. Esta relación es capturada por un modelo de regresión mediante una red neuronal artificial (perceptron multicapa).

---

## Datos para el módulo UCD, ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl.
</small></figcaption>
</figure>

<br>

El conjunto de entrenamiento se construye utilizando las bibliotecas sintéticas ($T_{eff} < 4000K$) y transformando el espectro sintético mediante el Gaia Object Generator (GOG).

---

## Estimación paramétrica

  * Bibliotecas sintéticas de espectros vistas por GAIA: modelos.
  * Bibliotecas sintéticas y espectros obtenidos en tierra vistas por GAIA: observaciones.

<br>

<figure>
<div style='text-align: center;'>
<img height='380' src='fitSpectralLines.png' />
</div>
<figcaption><small>
Comparación de espectros vistos por GAIA
</small></figcaption>
</figure>

---

## Estimación paramétrica

<strong> Recordemos <font color= "red"> objetivo </font> </strong>: Abordar la precisión de las estimaciones de la temperatura
y gravedad obtenidas a partir de modelos y observaciones actuales.

<br> 

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />

---

## Inferencia Bayesiana

* <font color="red"> Ventajas :</font> No solo da una estimación de los parámetros, sino una 
distribución de probabilidad para los mismos.
* <font color="red"> Desventajas:</font> Complejidad del modelo, consumo computacional elevado.

$$p (\theta | s) = \frac{p(s|\theta)
p(\theta)}{\int p(s|\theta) p(\theta) \, d \theta}
\propto p(s|\theta) p(\theta),
$$

donde $\theta = (T_{eff}, \log (g))$. En realidad la verosimilitud es 

$$s|\theta = s|(s_{model}, \Sigma) \sim \mathcal{N} (s_{model},\Sigma),$$

con $s_{model}$ el espectro obtenido mediante la RNA para $\theta$.


--- &twocol

## Inferencia Bayesiana

Para caracterizar a $p(\theta|s)$ utilizamos el algoritmo
<font color="green"> Nested Sampling </font>: exploramos la relación entre $p(s|\theta)$ y el *volumen de distribución previa* definido por $X (\lambda) = \int_{p(s|\theta) > \lambda} p(\theta) \, d \theta$, el volumen de distribución previa contenido en la región paramétrica contenida dentro del iso-contorno $p(s|\theta) > \lambda$

*** =left

<figure>
<div style='text-align: center;'>
<img src='nestedSampling.png' />
</div>
<figcaption></figcaption>
</figure>
<small>
Imagen propiedad de [John Skilling](http://www.inference.phy.cam.ac.uk/bayesys/Valencia.pdf)
</small>

*** =right

Además $p_i = \frac{p(s | \theta_i) \cdot w_i}{\hat{m(s)}}$,

con $w_i = 0.5(X_{i-1}-X_i)$ y
$\hat{T}_{eff}= \sum_{i = 1}^n T_{eff, i} \cdot p_i$

--- &twocol

## Inferencia Bayesiana

*** =left

<figure>
<div style='text-align: center;'>
<img src="figura14b.png" />
</div>
<figcaption><small>
$\log p(s| \theta)$ para modelo BT-Settl 1500K
</small></figcaption>
</figure>

*** =right

<figure>
<div style='text-align: center;'>
<img src="figura14a.png" />
</div>
<figcaption><small>
$\log p(s| \theta)$ para spectro con ruido SDSS0107 (G=20)
</small></figcaption>
</figure>

---

## Inferencia Bayesiana

<figure>
<div style='text-align: center;'>
<img src="BayesPredictions.png" />
</div>
<figcaption><small>
Resultados para Nested Sampling  con $\theta \sim \mathcal{U} (400, 4000) \times (3.5, 5.5)$
</small></figcaption>
</figure>

--- &twocol

## Distribución previa mediante cópula

Ampliar las distribuciones previas a copulas, simulando la relación
entre la temperatura y gravedad. Primera aproximación en TFG de Marta Sánchez, obteniendo mejores resultado (menor error de estimación).

*** =left

<figure>
<div style='text-align: center;'>
<img src="valor_prop_logpost_unif.png" />
</div>
<figcaption><small>
log posterior con previa uniforme
</small></figcaption>
</figure>

*** =right

<figure>
<div style='text-align: center;'>
<img src="valor_prop_logpost_copula.png" />
</div>
<figcaption><small>
log posterior con previa copula
</small></figcaption>
</figure>

--- 

## Distribución previa mediante cópula

Distribución posterior de $T_{eff}$ y $\log (g)$ 

<div style='text-align: center;'>
    <img height='220' width= '220' src='marginal_teff_uniforme.png' />
    <img height='220' width= '220' src='marginal_teff_copula.png' />
</div>

<div style='text-align: center;'>
    <img height='220' width= '220' src='marginal_logg_uniforme.png' />
    <img height='220' width= '220' src='marginal_logg_copula.png' />
</div>

---

## Trabajo en curso

<br>

<ol>

<li> Jerarquizar el modelo. </li>
<li> Paralelizar la verosimilitud: programación en Python y/o R, primeras prebas con arquitectura Spark. ¿Es la arquitectura correcta? Profiling. </li>

</ol>

---

## Gracias

¡No olviden descargarse al app!

<img height='412' style="float: center" src="GaiaMissionAPP.png">

---
## Extra. Resultados utilizando KNN

Obtiene los parámetros como la media ponderada de los elementos
en el cojunto de entrenamiento que están más cercas del espectro 
de entrada para una métrica dada. Dicha métrica es la distancia
euclídea y los pesos son la inversa de dicha distancia.

> Desventaja, todo el cojunto de datos debe se accesible en todo 
momento. Y la técnica está afectada de la maldición de la dimensionalidad,
es decir, cuando crezca el espacio parámetrico el número de observaciones
debe aumentar exponencialmente para mantener una densidad adecuadad de 
vecinos próximos.

<img height='412' style="float: center" src="knnPredictions.png">

---

## Extra. Resultados utilizando procesos gausianos

Se define como una distribución de probabilida sobre las funciones
de forma que la probabilidad conjunta de las variables aleatorias
definidas por sus evaluaciones en cierto conjunto de vectores (
el training set) es Gaussiano.

<img height='412' style="float: center" src="GPPredictions.png">

```
<video data-autoplay src="http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4"></video>
```
