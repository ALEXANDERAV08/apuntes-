# APUNTES SISTEMAS DE CONTROL 1 PRIMER CORTE 
## NESTOR ALEXANDER AVILA ROJAS 
## JUAN ESTEBAN RINCON BENAVIDES

# Modelamientos de Sistemas 
El modelamientos de sistemas de control es uno de los pasos mas importantes para un b uen analisis y diseño en sistemas de control, pues este nos ayuda a representar por medio de las matematicas yn comportamiento dinamico de algun sistema en especifico meduante ecuaciones, estas asu vez nos ayudan a ver el cambio de sus variables a travez del tiempo.
## Principio General del Modelamiento
Como se dijo anteriomente el modelamiento de un sistema consiste en representarlo mediante un conjunto de ecuaciones o relaciones matematica con el fin de describir su comportamiento atraves del tiempo para si poder analizar y predecir como va a responder ante diferentes condiciones para ello varios de los principos son:
### Conservacion de leyes fundamentales como:
Leyes de Newton (para sistemas mecánicos),
Leyes de Kirchhoff (para circuitos eléctricos),
Leyes de conservación de masa, energía y momento.
### Causalidad 
Esta establece la relacion etre casusa y efecto donde influyen tanto las entradas como las salidas del sistema anlizado esto atraves de unos procesos internos.
### Linialidad o no linialidad 
Esto  nos dira si el sistema se comporta de forma lineal en el tiempo o no ya que pueden haber sistemas los cuales cambien demaciado su estructura durante el transcurso del mismo.
## Como lucen los modelos de ecuaciones diferenciales
Estos son conbinaciones de derivadas de difernte orden su exprecion general esta dada de la siguiente forma:

$$a_{1}\frac{\partial^2 f }{\partial t^2}+a_{2}\frac{\partial f}{\partial t}+a_{3}f=u(t)$$

Donde F es la salida del Sistema,U es la entrada del Sistema,La solución no es un número es una función, gracias a este tipo de funciones podemos ver y analizar los sistemas.

## Sistemas Mecanicos 
Son aquellos sistemas que estan diseñados con utencilios como resortes, amortiguadores, estos a su vez conectados a una masa o superficie, son sistemas los cuales no llevan nada electrico y aparte de eso tambien pueden ser rotativos o combinados su escructura es:

[![Captura-2.png](https://i.postimg.cc/pX1BmMnw/Captura-2.png)](https://postimg.cc/HVXMNKzz)

Para el analizis de estos sistemas nos vasamos en fenomenos fisicos tales como la ley de hooke:

$$F_{R}=K*x$$

La friccion viscosa 

$$F_{f}=b*v_{m}$$

y las leyes de newton 

$$F=m*a$$

Para la solucion de los ejercicios se empesara con el analizis para asi saber como comenzaremos las ecuaciones, para el caso de un sistema de masa resorte amortiguador aplicaremos el diagrama de cuerpo libre para la masa y a si vmermos las fuerzas aplicadas para la ecuacion para la imaguen anterior es como se muestra a continuacion:

[![Captura-de-pantalla-2025-02-16-153035.png](https://i.postimg.cc/4317hpSY/Captura-de-pantalla-2025-02-16-153035.png)](https://postimg.cc/VSdLx01w)

Aqui observamos la sumatoria de furzas igualadas ala masa por su aceleracion, la ley de newton una vez con ella pasaremos a remplazar los valores de las fuerzas aplicadas como u(t), $F_{b}$ y $F_{k}$ para asi obtener la funcion del sistema como lo vemos en la imagen.

## Sistemas Mecanicos mas Complejos 
Los sistemas mecanicos mas complejos son aquellos constituidos por uno o mas sistemas mecanicos juntos su analicis suele ser mas complicado pero no difiere mucho de los calculos para un sistema mecanico simple, para ello veremos un pequeño ejemplo de un sistema mecanico mas complejo.

[![Captura-de-pantalla-2025-02-17-123512.png](https://i.postimg.cc/nLk8bLX8/Captura-de-pantalla-2025-02-17-123512.png)](https://postimg.cc/Ny5CRB8b)

En la imguen podemos ver dos masas conectadas a un resorte entre si y un resorte para la masa 1 y dos amortiguadores para la masa 2.
Para el analizis del ejemplo empesaremos analizando el sistema por medio de un diagrama de cuerpo libre con el fin de ver las fuerzas que actuan en cada mas, una vez con esto veremos que nos queda de la siguiente forma:

[![Captura-de-pantalla-2025-02-17-132632.png](https://i.postimg.cc/7L3n6G46/Captura-de-pantalla-2025-02-17-132632.png)](https://postimg.cc/TyPDNPpM)

Una vez con esto podremos sacar las funciones correspondientes a cada masa empezaremos con la masa numero 1, por medio de la ley de newton veremos la sumatoria de fuerzas la cual luego remplazaremos con las ecuaciones correspondientes como veremos en la siguiente imagen.

[![Captura-de-pantalla-2025-02-17-133053.png](https://i.postimg.cc/xjw3SDBg/Captura-de-pantalla-2025-02-17-133053.png)](https://postimg.cc/9zB7GSmq)

Una vez calculada la masa 1 pasaremos a los calculos de la masa 2 en este caso no varia mucho mas haya de que tenemos en este caso dos amortiguadores agarrados ala pared y el resorte en medio sabiendo esto la funcion que describe las fuerzas de la masa 2 quedaria de esta forma:

[![Captura-de-pantalla-2025-02-17-133734.png](https://i.postimg.cc/Zn6WPgbx/Captura-de-pantalla-2025-02-17-133734.png)](https://postimg.cc/5QN9bsFX)

## Sistemas Rotacionales 
Son otro tipo de sistemas mecanicos solo que en este caso lo que varia es la fuerza aplicada ya que es un movimiento circular que nos genera un torque,estos sistemas se analizan usando las leyes del movimiento rotacional, que son parecidas a las del movimiento traslacional pero en términos angulares.

[![Captura-de-pantalla-2025-02-17-135557.png](https://i.postimg.cc/WzV5wBm2/Captura-de-pantalla-2025-02-17-135557.png)](https://postimg.cc/Q96gXnnP)

Para el anaisis de estos sistemas usaremos leyes comparables al movimiento lineal tales como la fuerza de rosamiento donde el angulo $\varphi$ es el angulo de torcion.

$$F_{r}=k*\varphi$$

Tambien tendremos la fuerza de friccion donde la $\frac{\mathrm{d}\varphi }{\mathrm{d} t}$ es la velocidad angular del sistema

$$F_{f}=b*\frac{\mathrm{d}\varphi }{\mathrm{d} t}$$

y por ultimo el torque donde la constante j es el momento de inercia del sistema 

$$T=j*\frac{\partial \varphi ^2 }{\partial t^2}$$

Deigual forma como se venia trabajando para los demas sistemas este tambien lo anamizaremos por medio de un diagrama de cuerpo libre el cual nos quedara de la siguiente forma ya con las fuerzas dibujadas para asi poder generar la funcion correspondiente.

[![Captura-de-pantalla-2025-02-17-141638.png](https://i.postimg.cc/zvnK03zM/Captura-de-pantalla-2025-02-17-141638.png)](https://postimg.cc/xN1Xdfby)

Una vez con esto podremos hacer la funcion teniendo que $\sum T=J*\alpha$ para ello tendremos que:

$$T-F_{R}-F_{F}=j*\alpha$$

Remplazando tendriamos que la funcion no quedaria de la siguiente forma.

$$T(t)-K\theta (t)-B\frac{\partial \theta(t)}{\partial t}=J\frac{\partial^2\theta (t) }{\partial t^2}$$

## Conversion Movimiento Translacional-Rotacional 
Para estos sistemas veremos el proceso mediante el cual se convierte un desplazamiento lineal en un desplazamiento angular o a la inversa todo esto mediante un sistema mecanico el cual puede ser desglosado en varias partes las mas comunes son:
### Poleas y correas
Transmiten movimiento rotacional a uno lineal o al contrario a través de una banda o varias bandas.
### Cremallera y piñón
Convierte el movimiento rotacional de un engranaje en movimiento lineal.
### Tornillos sin fin 
Convierte la rotación de un tornillo dada ya sea por un motor o un giro manual en movimiento lineal.

Ejemplo: Tenemos el siguiente sistema combinando el cual es un motor enganchado a una polea para a si poder mover la caja.

[![Captura-de-pantalla-2025-02-17-151255.png](https://i.postimg.cc/x18sfD9Z/Captura-de-pantalla-2025-02-17-151255.png)](https://postimg.cc/k2rNsH6N)

Teniendo esto como base pasaremos al diagrama de cuerpo libre obteniendo a si las fuerzas positivas y negativas del sistema.

[![Captura-de-pantalla-2025-02-17-151604.png](https://i.postimg.cc/zfWFvq6x/Captura-de-pantalla-2025-02-17-151604.png)](https://postimg.cc/SXSMtby9)

Con esto pasaremos a resolver la $\sum T=J*\alpha$ teniendo asi:

$$T_{m}-T_{1}-T_{F}=J_{m}*\alpha$$

Donde remplazando las incognitas por sus funciones obtendremos el siguiente resultado, sabiendo que para $T_{1}$ el momento de inercia es $mr^{^2}$.

$$T_{m}-mr^{^2}\frac{\partial^2\theta  }{\partial t^2}-B\frac{\partial \theta }{\partial t}=J_{m}\frac{\partial^2\theta  }{\partial t^2}$$

Teniendo en cuenta que el $\theta = y/r$ remplazamos en la ecuacion

$$T_{m}-mr\frac{\partial^2 y}{\partial t^2}-\frac{B}{r}\frac{\partial y }{\partial t}=\frac{J_{m}}{r}\frac{\partial^2 y}{\partial t^2}$$

## Circuitos RLC
Un circuito RLC es un circuito eléctrico que está formado por resistencias inductancias y capacitancias estas a su vez están conectadas en serie o en paralelo también pueden ser circuitos mixtos son fundamentales para los sistemas de control filtrado de señales y otros circuitos electrónicos.

[![Captura-de-pantalla-2025-02-20-135413.png](https://i.postimg.cc/SRD1vHG4/Captura-de-pantalla-2025-02-20-135413.png)](https://postimg.cc/D44cWjDp)

Estos circuitos se rigen bajo la ley de ohm y otras leyes más como podemos ver en las siguientes ecuaciones tenemos que para cada uno de los elementos tenemos una ecuación característica estas son las siguientes

$$R=\frac{V(t)}{I(t)}$$
$$I=C\frac{\mathrm{d}V(t)}{\mathrm{d} t}$$
$$V=L\frac{\mathrm{d}i(t) }{\mathrm{d} t}$$

Teniendo en cuenta estas ecuaciones y la imagen anterior podemos resolver un ejemplo el cual sería la solución del circuito en serie, para ello utilizaremos la ley de voltajes de kirchhoff para así poder solucionar y encontrar la ecuación que nos describe el sistema.

Iniciaremos haciendo la suma de voltajes e igualando a cero.

$$-U+V_{R}+V_{L}+V_{C}=0$$

Luego reemplazaremos las ecuaciones mostradas anteriormente en la ecuación.

$$-U(t)+i(t)R+L\frac{\mathrm{d}i(t)}{\mathrm{d}t}+V_{C}=0$$

Una vez teniendo esto nos podemos dar cuenta que para que nos quede todo el factor es de voltaje del condensador reemplazaremos en la derivada de $i(t)$ por lo que vale $I$, teniendo la siguiente ecuación.

$$-U(t)+RC\frac{\mathrm{d}V_{C}(t)}{\mathrm{d} t}+LC\frac{\mathrm{d^2}V_{C}(t)}{\mathrm{d}t^2}+V_{C}=0$$

## Aplicación del método de nodos
para este caso el circuito está representado por lo general por 2 o más mayas las cuales a su vez están conectadas por distintos nodos, estos nodos son puntos de entrada y salida de más de 2 conexiones esta es su respuesta conectado ya sea una fuente de corriente o a una fuente de voltaje su representación es la siguiente.

[![Captura-de-pantalla-2025-02-20-145630.png](https://i.postimg.cc/3JYrPqgv/Captura-de-pantalla-2025-02-20-145630.png)](https://postimg.cc/5jKMznK4)

Para el análisis de solución de los ejercicios de nodos usaremos la ley de Corrientes de kirchhoff la cual está por la suma o resta de las Corrientes igualadas a cero, teniendo en cuenta las ecuaciones características de cada elemento así como en los circuitos normales RLC.

Iniciaremos con la suma o resta de las Corrientes teniendo la siguiente ecuación.

$$ i_{u}-i_{1}-i_{c}=0$$

Una vez con esta ecuación pasaremos a identificar el nodo base que es el que está conectado a Tierra en este caso el B, y el nuevo principal que está conectado A, para ello tendremos la siguiente ecuación.

$$ i_u(t) - \frac{V_{AB}}{0.5} - 2 \frac{dy(t)}{dt} = 0 $$

Para la parte del voltaje en el nodo A y B veremos que es igual a la corriente hice que baja por el condensador por 1 mas la salida del condensador, hoy teniendo así la siguiente solución.

$$ V_{AB} = i_c \cdot 1 + y(t) $$
$$V_{AB} = 2 \frac{dy(t)}{dt} + y(t)$$

Hoy una vez con los cambios hechos pasaremos a realizar los diferentes cálculos teniendo así por último la ecuación diferencial que nos describe el circuito

$$ u(t) - 6 \frac{dy(t)}{dt} - 2y(t) = 0 $$

## Ejercicios 
### Numero 1
[![image.png](https://i.postimg.cc/28pLNXyF/image.png)](https://postimg.cc/PN45mymP)

Para la solución del siguiente ejercicio empezaremos analizando las fuerzas que se aplican para cada masa para ello realizaremos el diagrama de cuerpo libre correspondiente para la M1, quedaría el siguiente diagrama.

[![Captura-de-pantalla-2025-02-22-163353.png](https://i.postimg.cc/vmj2YdpZ/Captura-de-pantalla-2025-02-22-163353.png)](https://postimg.cc/5HBSgD4h)

Una vez teniendo el siguiente diagrama pasaremos hacer las ecuaciones correspondientes utilizaremos la sumatoria de fuerzas igualadas a su masa por aceleración teniendo así la primera ecuación.

$$u(t) - F_B - F_{k2} - F_{B2} - F_{k1} - F_{B3} = m a_{m1}$$

Ya con esta ecuación podremos reemplazar correspondientemente quedando por consecuente de la siguiente forma.

$$U(t) - B_1 \frac{dy_1(t)}{dt} - k_2 y_1(t) - B_2 \frac{dy_1(t)}{dt} - k_1 (y_1(t) - y_2(t)) - B_3 \frac{d(y_1(t) - y_2(t))}{dt} = m_1 \frac{d^2 y_1(t)}{dt^2}$$

Una vez con esto podríamos pasar al análisis de la segunda masa para ello realizaremos igual que en el primer paso el diagrama de cuerpo libre correspondiente para M2, teniendo así el siguiente diagrama.

[![Captura-de-pantalla-2025-02-22-164401.png](https://i.postimg.cc/VNybmGKc/Captura-de-pantalla-2025-02-22-164401.png)](https://postimg.cc/nXkL1k8d)

Ya una vez con el diagrama realizado veremos las fuerzas que se aplican para la masa número 2 vemos que ambas masas en este caso se suman teniendo la siguiente ecuación.

$$F_{k1} + F_{B3} = m_2 a_{m2}$$

Con esto pasaremos a reemplazarlas fuerzas para así hallar la ecuación diferencial teniendo como resultado la siguiente ecuación.

$$k_1 (y_1(t) - y_2(t)) + B_3 \frac{d (y_1(t) - y_2(t))}{dt} = m_2 \frac{d^2 y_2(t)}{dt^2}$$

Con esto quedaría el resultado del sistema mecánico mencionado anteriormente teniendo como respuesta las 2 ecuaciones tanto para la masa 1 como para la masa 2.

### Numero 2
[![image.png](https://i.postimg.cc/bJ5PfMRx/image.png)](https://postimg.cc/Kktwn0wj)

A continuación, nos dicen que escribamos las ecuaciones diferenciales que representan el modelo de la siguiente figura para ello vemos que es un sistema mecánico el cual es un carro jalando un remolque que en el medio tiene un resorte y un amortiguador para ello comenzaremos realizando el diagrama de bloques correspondiente.

[![Captura-de-pantalla-2025-02-24-141741.png](https://i.postimg.cc/HxthbZxG/Captura-de-pantalla-2025-02-24-141741.png)](https://postimg.cc/YGhRHxY8)

Una vez teniendo este diagrama de bloques pasaremos a hacer la sumatoria de fuerzas para el vehículo quedando de la siguiente manera.

$$ Fy_1 - Fk_b + FB_b = m_1 a_{m1} $$

Vemos en la sumatoria de fuerzas cómo actúan cada una de ellas a continuación pasaremos a reemplazar cada fuerza con su respectivo valor para poder así hallar la ecuación correspondiente quedando de la siguiente manera.

$$y_1(t) - K_b \left( y_1(t) - y_2(t) \right) - B_b \frac{d \left( y_1(t) - y_2(t) \right)}{dt} = m_1 \frac{d^2 y_1(t)}{dt^2}$$

Con esto tendríamos la ecuación para el primer diagrama de bloques el cual es el vehículo a continuación para terminar el análisis pasaremos a hacer lo mismo en este caso para el remolque teniendo en cuenta que su diagrama de bloques queda de la siguiente manera.

[![Captura-de-pantalla-2025-02-24-142827.png](https://i.postimg.cc/nLKZMfyp/Captura-de-pantalla-2025-02-24-142827.png)](https://postimg.cc/R302byCD)

Listo una vez con esto pasaremos nuevamente a hacer la sumatoria de fuerzas teniendo la siguiente ecuación.

$$ F_{K_b} + F_{B_b} - F_{B_t} = m_2 a_{m_2} $$

Una vez con la sumatoria de fuerzas realizada pasaremos a reemplazar cada una de las fuerzas para así obtener la ecuación característica del sistema esta nos quedaría de la siguiente forma.

$$K_b \left( y_1(t) - y_2(t) \right) + B_b \frac{d \left( y_1(t) - y_2(t) \right)}{dt} - B_t \frac{dy_2(t)}{dt} = m_2 \frac{d^2 y_2(t)}{dt^2}$$

### Numero 3
[![image.png](https://i.postimg.cc/3r1qNxWt/image.png)](https://postimg.cc/23qGXmQW)

Para la solución del siguiente ejercicio empezaremos analizando el circuito para este caso utilizaremos la ley de Corrientes de kirchhoff  garantizando así también el método de nodos para el circuito veremos ubicados 2 modos que a su vez Sera sólo uno para ello empezaremos analizando la ecuación y la sumatoria de Corrientes.

$$ \frac{V_1 - e(t)}{sL} + \frac{V_1 - V_2}{R_2} + \frac{V_1}{R_1} = 0 $$

Sustituyendo los valores correspondientes en el circuito nos queda.

$$\frac{V_1 - e(t)}{2s} + \frac{V_1 - V_2}{200} + \frac{V_1}{50} = 0$$

Con esto nos quedaría las ecuaciones para los primer nodo o el nodo principal también lo podemos dividir con el voltaje de salida teniendo la siguiente ecuación para el nodo 2.

$$ \frac{V_2 - V_1}{R_2} + \frac{V_2}{R_3} + C \frac{dV_2}{dt} = 0 $$

Una vez con esto podemos reemplazar valores en la ecuación.

$$ \frac{V_2 - V_1}{200} + \frac{V_2}{20} + 0.2 \frac{dV_2}{dt} = 0 $$

Ya que el problema nos pide que debemos expresar la ecuación en términos de $i_2(t)$ y sabemos que $i_2(t)$ es igual a:

$$ i_2 = C \frac{dV_2}{dt} = 0.2 \frac{dV_2}{dt} $$

Una vez con esto y después de manipular algebraicamente las ecuaciones hola la ecuación diferencial en términos de $e(t)$ e $i_2(t)$ es :

$$ e(t) = 2 \frac{d^2 i_2}{dt^2} + 270 \frac{d i_2}{dt} + 1500 i_2 $$


# SISTEMAS ELECTRICOS 
Los sitemas electricos en sistema de control permite analizar y diseñar circuitos electricos desde una perspectiva de control automatico usando herramientas como ecuacones diferenciales, funciones
de transferencia
# REDES RLC
Las redes RLC son circuitos eléctricos compuestos por tres elementos básicos:

1. **Resistor (R)**: Limita el flujo de corriente y disipa energía en forma de calor.
2. **Inductor (L)**: Almacena energía en un campo magnético cuando la corriente fluye a través de él y se opone a cambios rápidos de corriente.
3. **Capacitor (C)**: Almacena energía en un campo eléctrico y se opone a cambios rápidos en el voltaje.

![image](https://github.com/user-attachments/assets/78e1e0cf-995e-4515-a7ba-dfd1a2ca000e)

## Tipos de Redes RLC

Las redes RLC pueden ser configuradas en serie o en paralelo, con propiedades diferentes en cada caso:

- **RLC en Serie**: Los componentes R, L y C están conectados uno tras otro. En esta configuración, la corriente que pasa por cada elemento es la misma. La impedancia total se calcula
sumando las impedancias individuales:

![image](https://github.com/user-attachments/assets/d97191da-1149-455a-98dd-fd34090c6585)

tension de escalon aplicada a un circuito en serie:
 
**Al aplicar LVK al circuito se obtiene:**

 $Ri + L \frac{di}{dt} + V_C = 150 \tag{7}\$  **(1)**

**Necesitamos la derivada de la corriente:**

$\frac{di}{dt} = \frac{d(-2000 sen 43.5 t e^{-10t})}{dt}  = -2000 e^{-10t} ((-10) sen 43.5 + 43.5 \cos 43.5t)\$

$\frac{di}{dt} = (20000 sen 43.5 - 87000 cos 43.5t) e^{-10t}\$

**despejando Vs de la ecuacion (1)**

$V_C = 150 - \left( 10i + 0.5 \frac{di}{dt} \right)\$

$10i = 10(-2000 sen 43.5t e^{-10t}) = -20000 sen 43.5t e^{-10t}\$

$0.5 \frac{di}{dt} = 0.5 \left( (20000 sen 43.5 - 87000 cos 43.5t) e^{-10t} \right) = (10000 sen 43.5 - 43500 cos 43.5t) e^{-10t}\$

$10i + 0.5 \frac{di}{dt} = (-10000 sen 43.5t - 43500 cos 43.5t) e^{-10t}$

$V_C = 150 - (-10000 sen 43.5t - 43500 cos 43.5t) e^{-10t}$

**por lo tanto:**

**$V_C = 150 - (-10000 sen 43.5t - 43500 cos 43.5t) e^{-10t}$ U(t)**

## APLICANDO NODOS 
El método de nodos es una técnica basada en la Ley de Kirchhoff de Corrientes (LKC) para analizar circuitos eléctricos. Se utiliza para encontrar los voltajes en los nodos de un circuito en 
función de las fuentes de corriente y los valores de los componentes.
**PASOS:**

Paso 1: Definir el nodo de referencia
El nodo principal es donde se conectan R,L y C, con voltaje V(t).

Paso 2: Expresar cada corriente
Las corrientes que salen del nodo son:

Corriente en la resistencia:  $𝐼𝑅=\frac{V}{R}$

​Corriente en la inductancia:  $IL​=\frac{L}{1}∫Vdt$

Corriente en la capacitancia: $IC=C\frac{dt}{dV}$
​

**Por LKC, la suma de estas corrientes  es igual a la corriente de la fuente:**


$\frac{V}{R} + C\frac{dt}{dV} + \frac{L}{1}∫Vdt=Is(t)$


![image](https://github.com/user-attachments/assets/5f65143e-30ea-47e8-a454-9e27354be3da)


![image](https://github.com/user-attachments/assets/9b4d8313-8eb0-4a4f-a666-2853eb77deea)

las Leyes de corriente de Kircchoff establecen que la suma de las corrientes que entran en el nodo es igual a la suma de las corrientes que salen, por lo tanto, podemos escribir que:

$\sum I = 0$

$I_{inductancia} - I_{resistencia} - I_{capacitor} = 0$

De esta manera la ecuacion dinamia del sistema resultante del nodo A es:

$i_L(t) = i_R(t) + i_C(t)$ = $\frac{V_C(t)}{R} + C \frac{dV_C(t)}{dt}$

La ecuacion $I_L(t)$ describe la corriente en la inductancia.

$i_R(t)= \frac{Vc(t)}{R}$

corriente en la resistencia y en el capacitor

$i_C(t)=C\frac{dV_C(t)}{dt}$

# CIRCUITOS CON APLIFICADORES OPERACIONALES

Los circuitos con amplificadores operacioneales **(Op-Amps)** se analizan utilizando las **Leyes de Kirchoff** debido a su principio de funcionamiento basado en la conservacion e la energia y 
la distribucion de corrientes en un circuito electrico. Para simplificar el analisis se usa un modelo **idealizado** que facilita el diseño y prediccion del comportamiento del circuito 

![image](https://github.com/user-attachments/assets/b0e0561f-9c66-4b18-a5ec-384b22f86845)

**LEYES DE KIRCHOFF EN CIRCUITOS CON OP-AMPS**
**ley de kirchoff de voltajes (LVK)**:
  - La suma de las cidas de tension en un lazo cerrado es cero
  - Se usa para alalizar circuitod con retroalimentacion en Op.Amps
**ley de kirchoff de corriente (LKC)**
  - La suma de las corrientes que entran a un nodo es igual a la suma de las corrientes que salen.
  - En un Op-Amp ideal, la corriente en sus entradas es cero **$(I_+ = i_- = 0)$** debido a su impedancia de entrada infinita

**ANALISIS DE CIRCUITOS CON OP_AMPS**

**Amplificador No Inversor**

![image](https://github.com/user-attachments/assets/8d4100b1-9e8b-4b0f-bbbc-c8f69a1cef93)

$\frac{e_i - V}{R_1} + \frac{e_o - V}{R_2} = 0$

$e_o=e_i(1+\frac{R2}{R1})$

![image](https://github.com/user-attachments/assets/15f2f202-2fdc-4a8f-8234-35409ec964af)

$I_1+I_2-I_3-I_4=0$

$\frac{e_i-e_o}{R1} - \frac{e'-e_o}{R2} - \frac{Cd(e'-e_o)}{dt} - Cd(e_i-e')$

$e'=0$

$\frac{e_i}{R1} - \frac{-e_o}{R2} - \frac{C_2d(-e_o)}{dt} - \frac{c_1d(e'e)}{dt}$

$\frac{e_i}{R1} + \frac{C_1de_i}{dt} = \frac{C_2de}{dt} - \frac{e}{R2}$

**Amplificador Inversor**

   $$V_{\text{out}} = -\frac{R_f}{R_{\text{in}}} V_{\text{in}}$$

 **Sumador Inversor**

   $$V_{\text{out}} = -\left(\frac{R_f}{R_1} V_1 + \frac{R_f}{R_2} V_2 + \cdots\right)$$

 **Integrador**

   $$V_{\text{out}} = -\frac{1}{RC} \int V_{\text{in}} \, dt$$
   
**Diferenciador**

   $$V_{\text{out}} = -RC \frac{dV_{\text{in}}}{dt}$$
 
# SISTEMAS HIDRAULICOS 
Los sistemas de tanques son modelos fundamentales en ingeniería hidráulica y control de procesos, utilizados para almacenar y regular el flujo de líquidos en diversos sistemas industriales. 
Se pueden modelar como sistemas dinámicos, donde se aplican principios de mecánica de fluidos y las Leyes de Conservación.

**TOPIS DE SISTEMAS DE TANQUES:**
**TANQUE SIMPLE:** de un solo compartimiento.
**TANQUE EN SERIE:** dos tanques en cascada.
**TANQUE EN PARALELO:** dos tanques alineados.
tambien se puedes clasificas segun su entrada y salida (multiples entradas, multiples salidas, tanques interconectados)

**MODELADO MATEMATICO DE UN SISTEMA DE TANQUES**
En sistemas industriales de tanques es deseable mantener flujo o nivel constante, 
$p_1, q_2=$ flujo de entrada y salida del liquido 
$R_1=$ resistencia del flujo
$A_1=$ Area transversal del tanque.
$h_1=$ nivel del liquido.

**MODELO DE UN TANQUE**

**Flujo de salida**

$q_1=\frac{h_1}{R1}$

**Intercambio de Masa**

$A_1 \frac{dh_1}{dt}$ = $q_1-q_2$


**OBTENGA EL MODELO MATEMATICO PARA EL SIGUIENTE SISTEMA CON SALIDA $q_o$**


![image](https://github.com/user-attachments/assets/9a1ffa32-5f82-4689-aed4-2da6f2c7061c)


**Ley de la conservacion de la materia $q=\frac{h}{R}$**

**Ecuacion del sistema primer tanque (A_1)**

$A_1= \frac{dh_1}{dt} = q_1-q_d$

**donde**
**$a_1=$** Area del taque 1
**$q_d=$** Flujo de la salida del tanque.

**Flujo elacionado con la altura**

$q_d=\frac{h1}{R1}$

**SUSTITUCION:**

$A_1\frac{dh1}{dt} = q_1 - \frac{h1}{R1}$

**PARA EL TANQUE 2**

$R_1 Y R_2:$ Representan la resistencia de flujo en las tuberias de salida.

**balance de masa:**

$A_2\frac{dh²}{dt} = q_d-q_o$               


$q_o=\frac{h2}{R2}$


$A_2\frac{dh²}{dt} = \frac{h1}{R1} - \frac{h²}{R2}$ 

# TRANSFORMADA DE LAPLACE

La gtranformada de Laplace es una tecnica que transforma funciones que dependen del tiempo en una foprma mas simplificada y facil de manejar, especialmente cuando se trabaja con ecuaciones diferenciales, en vez 
de resolver estas ecuaciones directamente, la transformada de la`lace las convierte en ecuaciones algebraicas simples. Basicamente toma una funcion en el tiempo y la transforma en el dominio del tiempo donde se 
puede hace calculos mas sencillos.

$$\mathcal{L}\{f(t)\} = F(s) = \int_{0}^{\infty} e^{-st} f(t) \, dt$$

## Algunas propiedades
 ### 1. linealidad 
la transformada de laplace de una suma de funciones es igual a la suma de las transformadas de cada funcion

$$\mathcal{L}(\{a f(t) + b g(t)\} = a \mathcal{L}\{f(t)\} + b \mathcal{L}\{g(t)\})$$

donde a y b son constantes.

### 2. Transformada de la derivada
La transforma de laplace de la primera derivada de una funsion es:


 $$\mathcal{L}\{f'(t)\} = s F(s) - f(0)$$

Para la segunda derivada:

$$\mathcal{L}\{f''(t)\} = s^2 F(s) - s f(0) - f'(0)$$

## 3. escalon unitario
la transformada de laplas de la funcion escalon unitario es simplemente $1/s$ lo que es un util para analizar la respuesta de sistemas a entradas constantes.

$$u(t) = 
\begin{cases} 
0, & t < 0 \\
1, & t \geq 0
\end{cases}$$

$$\mathcal{L}\{u(t)\} = \int_0^{\infty} e^{-st} \cdot 1 \, dt = \frac{1}{s}, \quad \text{para} \, s > 0$$

## 4.funcion rampa
Nos ayuda a cconvertir una funcion que crece de forma lineal en el tiempo como $$r(t)=t$$, una expresion mas facil de manejar en el mundo de las ecuaciones y sistemas dinamicos 

$$\mathcal{L}\{r(t)\} = \mathcal{L}\{t\} = \int_0^{\infty} t e^{-st}dt$$

# TRANSFORMADA INVERSA DE LAPLACE
* Si las funsiones son simples, se puede usar directamente la tabla de las transformadas
 
* Si la función es una combinación o composición de varias funciones, es necesario:

- Calcular la integral de la definición de la transformada inversa.
- Usar una expansión en fracciones parciales para descomponer la función en términos más simples que se encuentren en la tabla de transformadas.

**la transformada inversa de laplace se define como:**

$f(t) = \mathcal{L}^{-1} \{F(s)\} = \frac{1}{2\pi j} \int_{\sigma - j\infty}^{\sigma + j\infty} F(s) e^{st} \, ds$

**Donde:**

- F(s) es la función en el dominio de la frecuencia
- f(t) es la función original en el dominio del tiempo
- La integral se evalúa a lo largo de una línea vertical en el plano complejo

  
En la práctica, en lugar de resolver esta integral, se utilizan tablas de transformadas de Laplace y técnicas algebraicas como la descomposición en fracciones parciales.

**Uso de Tablas de Transformadas**

Si F(s) coincide con una expresión conocida en las tablas de Laplace, simplemente se consulta su inversa.

$F(s)=\frac{1}{s+a} $

**Con la tabla**

![image](https://github.com/user-attachments/assets/5b6b6b0a-1209-4176-ab21-4ab9ed754f6f)

**entonces**

![image](https://github.com/user-attachments/assets/a94262ef-38f7-4d92-9da7-a6c1aab4cc1e)

# Función de transferencia:
La función de transferencia es una representación matemática utilizada en sistemas de control. Se obtiene a partir de la transformada de 
Laplace de una ecuación diferencial, considerando todas las condiciones iniciales en cero. Esta función es una herramienta 
fundamental en la teoría de control y en la dinámica de sistemas. Sirve para analizar y diseñar sistemas que procesan señales de entrada 
para producir una respuesta deseada en la salida.
## principales usos :
## 1. Modelado de sistemas:
   - Permite representar sistemas dinámicos lineales de tiempo invariante (LTI) en el dominio de la frecuencia.

   - Facilita el paso de las ecuaciones diferenciales del sistema al dominio de Laplace.
## 2. Análisis del Comportamiento del Sistema:

   - Respuesta transitoria: Describe cómo el sistema reacciona a cambios iniciales o perturbaciones.
   - Respuesta en estado estacionario: Muestra el comportamiento del sistema cuando alcanza una condición estable.
## 3. Diseño de Controladores:
   - Ayuda a diseñar controladores como PID (Proporcional, Integral y Derivativo) para mejorar la estabilidad, la precisión y la velocidad del sistema.

## clasificacion de las funciones de transferencia:

una funcion de transferencia se puede expresar como :
$$G(s) = \frac{Y(s)}{U(s)}$$
Donde:
   - Y(S):Salida en el dominio de laplace
   - U(S):Entrada en el dominio de laplace
## Clasificación:
   - Estrictamente propia: 𝑚>𝑛(grado del denominador mayor al numerador).
   - Bipropia: 𝑚=𝑛
   - Impropia: 𝑛>𝑚
## Polos y Zeros

   - Zeros: Valores de 𝑠 que anulan el numerador.
   - Polos: Valores de 𝑠 que anulan el denominador.
     
![image](https://github.com/user-attachments/assets/a48ffa60-af40-4f41-a340-b4c8a9aad4c0)

**Ejercicio**

$G_4(s) = \frac{-20(s-0.1)}{(s+1)(s+2)}$ 

**Numerador:**
-20(s-0.1)
s-0.1 = 0 
s = 0.1
**Ceros:** s = 0.1
**Denominador:** (s+1)(s+2)
**polos:** s = -1, s = -2

**solucion en matlab**

![image](https://github.com/user-attachments/assets/8d14a6bb-b521-486e-a92c-e37207697ef3)

![image](https://github.com/user-attachments/assets/2c139187-a802-41e6-832a-b65e551b1b71)

# Ecuaciones diferenciales de primer orden
## Funcion de transferencia
Las ecuaciones diferenciales de primer orden son las que hoy por lo general hoy la derivada de la función incógnita $y(x)$ aparece solo en la solución de su primera derivada

La estructura general de una ecuación de primer orden es la siguiente

$$a\dot{y}(t) + b y(t) = c u(t)$$

para hallar la solución defunción de transferencia tenemos que en primer paso aplicar Laplace teniendo así el siguiente resultado

$$asY(s) + bY(s) = cU(s)$$

Con esto podremos aplicar el concepto general de una función de transferencia la cual es despejar o tener todo en términos de la salida y la entrada

$$\frac{Y(s)}{U(s)} = \frac{c}{as + b}$$

Cómo podemos ver las funciones de transferencia de primer orden provienen de una ecuación diferencial de primer orden un ejemplo de ello sería el siguiente

$$\frac{Y(s)}{U(s)} = \frac{c}{as + b}$$

Dónde nos podemos dar cuenta que los parámetros a b y c hp son parámetros físicos del sistema que definen la dinámica del mismo
### Ejemplo
[![image.png](https://i.postimg.cc/fyPrbMrW/image.png)](https://postimg.cc/dZ8BHcFg)

Como podemos ver en el ejemplo primero hallaremos la ecuación general teniendo

$$a\dot{y}(t) + b y(t) = c u(t)$$

Luego de ello pasaremos a la forma general en la cual se hace una función transferencia

$$\frac{Y(s)}{U(s)} = \frac{c}{as + b}$$

A continuación veremos la ecuación que describe el sistema mostrado en la imagen el cual es un sistema hidráulico de un tanque con una resistencia o paso de agua

$$R_1 A_1 \frac{dh_1}{dt} = R_1 q_i - h_1$$

Con esto podemos darnos cuenta que deberíamos ser capaces de formar la función de transferencia del sistema teniendo en cuenta que
$$a = R_1 A_1$$
$$b = 1$$
$$c = R_1$$
Podemos reescribir la función de transferencia

$$\frac{H_1(s)}{Q_i(s)} = \frac{R_1}{R_1 A_1 s + 1}$$

## Forma canónica de los sistemas de primer orden
Ya sabemos en los apuntes anteriores como está definida la forma de transferencia de un sistema de primer orden, esta forma no permite identificar directamente los parámetros temporales del sistema para ello necesitamos el control que se prefiere de la forma canónica para ello necesitaremos hacer uno que otros cálculos los cuales son

$$\frac{Y(s)}{U(s)} = \frac{c}{as + b}$$

$$= \frac{\frac{c}{b}}{\frac{a}{b}s + 1}$$

Teniendo en cuenta esto consideramos que $\tau = \frac{a}{b}$ es una constante de tiempo y $K = \frac{c}{b}$ es la ganancia estática del sistema teniendo lo siguiente 

$$ \frac{Y(s)}{U(s)} = \frac{K}{\tau s + 1} $$

Con esto podremos retomar el ejemplo anterior y darnos cuenta que cambiando los parámetros podemos tener diferentes combinaciones que nos permiten evaluar características de la respuesta temporal del sistema
### Ejemplo 2 
Identificar el $\tau$ y $K$ del siguiente sistema 

$$\frac{Y(s)}{U(s)} = \frac{0.8}{s + 1}$$

Sabiendo lo anterior tenemos que $\tau=1$ segundo y la ganancia del sistema $K=0.8$

## Respuesta temporal de un sistema de primer orden 
Hay varias respuestas que podemos dar para un sistema de primer orden todo esto depende según la entrada la cual se le aplique al sistema así como hay varias salidas también tenemos varias entradas pues dependemos que el mismo tipo de entrada sea el mismo que el de salía para ello podremos comenzar aplicando uno de los estímulos más comunes el cual es la entrada tipo escalón

$$Y(s) = \frac{U(s)K}{\tau s + 1} = \frac{\frac{A}{s} K}{\tau s + 1}$$

para la gran mayoría de sistemas según su tipo de entrada deberemos darle solución en este caso aplicaremos fracciones parciales teniendo que al despejar C1 y C2 tenemos la siguiente solución

$$Y(s) = \frac{C_1}{s} + \frac{C_2}{s + \frac{1}{\tau}} = \frac{A K}{s} - \frac{A K}{s + \frac{1}{\tau}}$$

Para terminar necesitaremos aplicar la transformada inversa de Laplace teniendo como resultado el modelamiento y una ecuación para ver su comportamiento a través de ciertos tiempos

$$\mathcal{L}^{-1} \{ Y(s) \} = y(t) = AK \left( 1 - e^{\frac{-t}{\tau}} \right)$$

### Constante del tiempo del sistema
Sabiendo la respuesta de $y(t)$ podemos ver cómo actúa a través del tiempo la entrada y cuándo se estabiliza para un mejor análisis sabiendo que AK es una constante y va a ser el punto máximo al cual llegará nuestro sistema con esto podemos armar la siguiente tablita y ver cuál va a ser el tao o el tiempo de establecimiento mejor para aplicarlo

[![image.png](https://i.postimg.cc/rpdbv0nn/image.png)](https://postimg.cc/JyLPXnWZ)

Con esto podemos graficar y ver cómo actúa cada tiempo y así mismo vemos que por lo general desde los cuatro taos el sistema ya es completamente estable para analizarlo

[![image.png](https://i.postimg.cc/SsCPK0pc/image.png)](https://postimg.cc/WFp89Hz4)

Esta función es muy importante ya que con esta podemos analizar el tipo de respuesta para cualquier tipo de entrada en este caso daremos varios ejemplos como el de un sistema rampa y el sistema hipotético de impulso

El análisis dinámico de un sistema con respuesta a una entrada rampa veremos que dependemos siempre de la pendiente en la zona lineal del sistema más allá de sus tiempos ya que estos repercuten en que siempre van a ser constantes hacia el valor que vaya dependiendo de AK cómo lo veremos en la siguiente imagen

[![image.png](https://i.postimg.cc/ydmfHFFP/image.png)](https://postimg.cc/sQ2PPGHQ)

En el caso de un sistema el cual interprete la entrada de un pulso ya que es una medida la cual físicamente es imposible de hacer ya que requiere de una cantidad de energía y disipación de energía muy grande de igual manera se puede modelar una aproximación matemática por el medio de funciones ya sea una función gaussiana o combinaciones de escalones con un tiempo muy muy pequeño

[![image.png](https://i.postimg.cc/nL724vwJ/image.png)](https://postimg.cc/f3zYZ0N2)



