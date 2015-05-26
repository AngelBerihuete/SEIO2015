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

<style>#forkongithub a{background:#c11;color:#fff;text-decoration:none;font-family:arial,sans-serif;text-align:center;font-weight:bold;padding:5px 40px;font-size:1rem;line-height:2rem;position:relative;transition:0.5s;}#forkongithub a:hover{background:#c11;color:#fff;}#forkongithub a::before,#forkongithub a::after{content:"";width:100%;display:block;position:absolute;top:1px;left:0;height:1px;background:#fff;}#forkongithub a::after{bottom:1px;top:auto;}@media screen and (min-width:800px){#forkongithub{position:fixed;display:block;top:0;right:0;width:200px;overflow:hidden;height:200px;z-index:9999;}#forkongithub a{width:200px;position:absolute;top:60px;right:-60px;transform:rotate(45deg);-webkit-transform:rotate(45deg);-ms-transform:rotate(45deg);-moz-transform:rotate(45deg);-o-transform:rotate(45deg);box-shadow:4px 4px 10px rgba(0,0,0,0.8);}}</style><span id="forkongithub"><a href="https://github.com/AngelBerihuete/SEIO2015">Fork me on GitHub</a></span>

<br>

<br>

<br>

## Estimación de parámetros 

## físicos en estrellas de baja masa

<br>

bajo el marco de la misión espacial GAIA

<br>

<small> <a href= "mailto:angel.berihuete@uca.es" >A. Berihuete,</a> L. M. Sarro, A. Suárez, D. Barrado, C. Carrión, M. Sánchez
<br>
<br>

Universidad de Cádiz
<br>
Universidad Nacional de Educación a Distancia
<br>
Centro de Astrobiología

</small>

---


## Esquema de la presentación

1. Contexto: ¿qué es la misión espacial GAIA?
2. Los datos: ¿qué son las estrellas de baja masa?
3. Estimación parámetrica. Principales  resultados.
4. Trabajo actual y futuro.


--- &twocol

## La misión espacial GAIA

*** =left

<figure>
<div style='text-align: center;'>
    <img src='Hipparchus_by_Raphael.jpg' />
</div>
<figcaption><small>
Fuente Wikipedia
<br>
Hiparco de Nicea
</small></figcaption>
</figure>

*** =right

<figure>
<div style='text-align: center;'>
    <img src='hipparcos1.jpg' />
</div>
<figcaption><small>
Fuente ESA. Satelite Hipparcos 
<br>
(The High Precision Parallax Collecting Satellite)
</small></figcaption>
</figure>

--- &twocol

## La misión espacial GAIA

<figure>
<div style='text-align: center;'>
<video width="512" data-autoplay controls src="Gaialaunch.mp4" type="video/mp4"></video>
</div>
</figure>

*** =left

<font color = "red" underline> Reto tecnológico </font>

<p class="fragment" data-fragment-index="1" style="text-align: left;">
106 CCDs con 8 millones de pixels cada uno.
</p>

<p class="fragment" data-fragment-index="2" style="text-align: left;">
Transmitirá, durante 5 años, 50 Gb diarios. Al final de la misión el archivo de datos excederá el Petabyte.
</p>

*** =right

<font color = "red"> Reto científico </font>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
Se registrarán un total de 70 mil millones de observaciones, cada una de ellas compuesta a su vez de varios conjuntos de medidas.
</p>

<p class="fragment" data-fragment-index="4" style="text-align: left;">
La astrometría será la mejor conseguida hasta ahora.
</p>


--- &twocol

## La misión espacial GAIA
<br>

<font size="12"> El reto:  un censo de 
<font color = "red"> mil millones de estrellas 
</font>
</font>

<br>

*** =left

<figure>
<div style='text-align: center;'>
<img src='gaiaSatellite.png' />
</div>
<figcaption><small>
Fuente ESA
</small></figcaption>
</figure>

*** =right

<br>
<br>

<p style="text-align: left;">
La <font color = "red"> Astroestadística </font> 
se ha convertido en eslabón fundamental para el análisis y 
contraste de modelos en las grandes bases de la Astronomía actual.
</p>

--- &twocol

## La misión espacial GAIA

<br>

Consorcio para el procesado de datos (DPAC)

<br>

*** =left

<figure>
<div style='text-align: center;'>
<img src='DPAC1.png' />
</div>
<figcaption><small>
Fuente ESA
</small></figcaption>
</figure>

*** =right
<figure>
<div style='text-align: center;'>
<img src='DPAC2.png' />
</div>
<figcaption><small>
Fuente ESA
</small></figcaption>
</figure>


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

## El módulo UCD

### estrellas enanas ultra frías

<br>

***=left

<figure>
<div style='text-align: center;'>
    <img src='BrownDwarfs.png' />
</div>
<figcaption><small>
Fuente Wikipedia
</small></figcaption>
</figure>

***=right

<p class="fragment" data-fragment-index="3" style="text-align: left;">
<font color="red">Contexto:</font>  GAIA contendrá un vasto número de objetos, incluyendo estrellas enanas ultrafrías (temperatura por debajo de 2500 K)
</p>

<p class="fragment" data-fragment-index="3" style="text-align: left;">
<font color="red">Objetivo:</font> Abordar la precisión de las estimaciones de la temperatura y gravedad obtenidas a partir de modelos y observaciones actuales.
</p>

--- &twocol

## El módulo UCD

### estrellas enanas ultra frías

<br>

***=left

<figure>
<div style='text-align: center;'>
    <img src='BrownDwarfs.png' />
</div>
<figcaption><small>
Fuente Wikipedia
</small></figcaption>
</figure>

***=right

### 

<figure>
<div style='text-align: center;'>
    <img src='EvolutionaryTracks.png' />
</div>
<figcaption><small>
Tracks evolutivos
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

---

## Datos para el módulo UCD

### ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

<br>

Bibliotecas de modelos estelares y los espectros sintéticos asociados
ofrecen un conjunto homogéneo que cubren uniformemente el espacio de
parámetros.

---

## Datos para el módulo UCD

### ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

<br>

Estas bibliotecas parametrizan los modelos con magnitudes físicas (temperatura efectiva, gravedades, y metalicidades)

.fragment Son imperfectas, ya que no pueden reproducir exactamente todas las características de un espectro real UCD.

---

## Datos para el módulo UCD

### ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a></small></figcaption>
</figure>

Los tipos espectrales pueden inferirse sin el uso de modelos sintéticos, pero el camino de espectro a los parámetros físicos necesitan de éstas para su correcta interpretación.

.fragment Dado el espectro de baja resolución de GAIA, la mayoría de las características utilizadas para decidir el tipo espectral permanecen no resueltas o innobservadas, i.e., cuidado con las interpretaciones.

---

## Datos para el módulo UCD

### ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

<br>

Los modelos sintéticos definen la relación entre los espcetros observados por GAIA y los parámetros que queremos estimar $T_{eff}$ y $\log (g)$,  temperatura y gravedad. Esta relación es capturada por un modelo de regresión mediante una red neuronal artificial (perceptron multicapa).

---

## Datos para el módulo UCD

### ¿qué vemos realmente?

<figure>
<div style='text-align: center;'>
<img src='NormalisedSampleSpectra.png' />
</div>
<figcaption><small>
Espectros normalizados a partir de la biblioteca de modelos BT-Settl
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
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
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

---

## Estimación paramétrica

<strong> Recordemos <font color= "red"> objetivo </font> </strong>: Abordar la precisión de las estimaciones de la temperatura
y gravedad obtenidas a partir de modelos y observaciones actuales.

<br> 

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />


---

## Estimación paramétrica

### KNN

<figure>
<div style='text-align: center;'>
<img height='412' style="float: center" src="knnPredictions.png">
</div>
<figcaption><small>
Resultados utilizando KNN
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

---

## Estimación paramétrica

### Procesos Gausianos

<figure>
<div style='text-align: center;'>
<img height='412' style="float: center" src="GPPredictions.png">
</div>
<figcaption><small>
Resultados utilizando PG
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>

</small></figcaption>
</figure>

---

## Estimación paramétrica

### Bayes

<figure>
<div style='text-align: center;'>
<img height='412' src="BayesPredictions.png" />
</div>
<figcaption><small>
Resultados para Nested Sampling con $\theta \sim \mathcal{U} (400, 4000) \times (3.5, 5.5)$
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

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
<figcaption>
<small>
Fuente <a href="http://www.inference.phy.cam.ac.uk/bayesys/Valencia.pdf">John Skilling (Proc. Valencia / ISBA)</a>
</small>
</figcaption>
</figure>

*** =right

Además $p_i = \frac{p(s | \theta_i) \cdot w_i}{\widehat{m(s)}}$,

con $w_i = 0.5 ( X_{i-1} - X_i ) $. ADemás

$$ \widehat{T}_{eff} = \sum_{i = 1}^n T_{eff, i} \cdot p_i $$

--- &twocol

## Inferencia Bayesiana

*** =left

<figure>
<div style='text-align: center;'>
<img src="figura14b.png" />
</div>
<figcaption><small>
$\log p(s| \theta)$ para modelo BT-Settl 1500K
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

*** =right

<figure>
<div style='text-align: center;'>
<img src="figura14a.png" />
</div>
<figcaption><small>
$\log p(s| \theta)$ para spectro con ruido SDSS0107 (G=20)
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
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
<br>
Fuente <a href="http://www.aanda.org/articles/aa/abs/2013/02/aa19867-12/aa19867-12.html">Sarro et al.</a>
</small></figcaption>
</figure>

--- &twocol

## Distribución previa mediante cópula

Ampliar las distribuciones previas a copulas, simulando la relación
entre la temperatura y gravedad. Primera aproximación en TFG de Marta Sánchez, obteniendo mejores resultados (densidades unimodales).

*** =left

<figure>
<div style='text-align: center;'>
<img src="fdDtefflogg.png" />
</div>
<figcaption><small>
Relación temperatura gravedad
<br>
Fuente TFG Marta Sánchez

</small></figcaption>
</figure>

*** =right

<figure>
<div style='text-align: center;'>
<img src="CopulafdDtefflogg.png" />
</div>
<figcaption><small>
mixtura de distribuciones uniformes y cópula normal
<br>
Fuente TFG Marta Sánchez
</small></figcaption>
</figure>


--- &twocol

## Distribución previa mediante cópula

Ampliar las distribuciones previas a copulas, simulando la relación
entre la temperatura y gravedad. Primera aproximación en TFG de Marta Sánchez, obteniendo mejores resultados (menor error de estimación).

*** =left

<figure>
<div style='text-align: center;'>
<img src="valor_prop_logpost_unif.png" />
</div>
<figcaption><small>
Relación temperatura gravedad
<br>
Fuente TFG Marta Sánchez

</small></figcaption>
</figure>

*** =right

<figure>
<div style='text-align: center;'>
<img src="valor_prop_logpost_copula.png" />
</div>
<figcaption><small>
log posterior con previa cópula
<br>
Fuente TFG Marta Sánchez
</small></figcaption>
</figure>



--- 

## Distribución posterior 

### temperatura y gravedad

<small>
Fuente TFG Marta Sánchez
</small>

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

<ul>
<li> Jerarquizar el modelo. </li>
<li> Paralelización del algoritmo, High Perfomance Computing para emcee, y/o HMC (programación en Python y R)</li>
<li>Paralelización de la verosimilitud

$$ \log p(s | \theta) = \sum_{i=1}^n \log  p(s_i | \theta), \quad n>> $$

Hemos utilizado colas Condor, Slrum, y estamos con las primeras pruebas en arquitectura Spark. ¿Es la arquitectura correcta?
</li>
</ul>

---

## Gracias

¡No olviden descargarse al app!

<img height='480' style="float: center" src="GaiaMissionAPP.png">
