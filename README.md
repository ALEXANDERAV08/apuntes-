# apuntes-
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




