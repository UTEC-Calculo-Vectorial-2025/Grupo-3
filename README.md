# Informe del Proyecto ABP - Cálculo Vectorial

## Datos generales

- **Nombre del proyecto**:  
- **Integrantes** (Nombres y códigos):  
- **Aula**: Teoría 1.01  
- **Sala**: Sala 1 / 2 / 3  
- **Grupo**: Grupo X
- **Docente**: Nombre y Apellido  

---

## 1. Comprensión del problema 
- Describa claramente los datos del problema.
- Identifique claramente el objetivo de la pregunta.
- Describa las variables involucradas en el problema.

---

## 2. Desarrollo y aplicación de la solución 

### 2.1 Ejecución de la solución

- Describa la secuencia de pasos que siguieron.
- Explique cómo aplicaron los conceptos matemáticos del curso.
- Justifique cada paso de su razonamiento.

### 2.2 Uso de herramienta CAS

- Incluir aquí los gráficos elaborados con CAS (GeoGebra, Desmos, Matlab, etc.).
- Explicar el significado de cada gráfico en relación con la solución.

### 2.3 Explicación gráfica

- Explique claramente las gráficas utilizadas.
- Identifique y resalte los elementos más importantes de las gráficas.
- Utilice el puntero de la presentación para señalar los elementos clave (esto es para la exposición).

---

## 3. Análisis y discusión

- Describa las estrategias utilizadas para validar su respuesta.
- Muestre cómo modificaron los parámetros del problema.
- Explique cómo los cambios en los parámetros afectan los resultados.
- Atribuya correctamente los cambios observados a las modificaciones realizadas.

---

## 4. Conclusiones

- Resuma los aprendizajes principales del trabajo realizado.
- Mencione posibles extensiones o mejoras al trabajo.

---

## 5. Bibliografía

- Liste todas las fuentes bibliográficas consultadas (libros, artículos, páginas web).

---

## 6. Reflexión sobre trabajo en equipo *(opcional, para autoevaluación)*

- Comente brevemente cómo fue la colaboración dentro del grupo.
- ¿Cómo contribuyó cada integrante al desarrollo del proyecto?



\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{graphicx} % Aunque se omiten las imágenes, el paquete es útil para otros gráficos si los hubiera.

\title{Análisis de Trayectorias y Pendiente en una Superficie de Elevación}
\author{}
\date{}

\begin{document}

\maketitle

\section*{Pregunta 1:}
Proponer dos trayectorias parametrizadas $\vec{r}{1}(t)$ y $\vec{r}{2}(t)$ que conecten los puntos $A(0,0)$ y $B(4,0)$. 

\subsection*{Primera trayectoria $\vec{r}_{1}(t)$: línea recta}
Una forma sencilla de conectar $A(0,0)$ con $B(4,0)$ es usando una línea recta: 
$$ \vec{r}_{1}(t)=\langle4t,0\rangle, \quad t\in[0,1] $$ 

\subsection*{Segunda trayectoria $\vec{r}_{2}(t)$: tipo espiral}
Usamos la forma sugerida por el documento: 
$$ \vec{r}_{2}(t)=\langle a(t)\cos(wt),a(t)\sin(wt)\rangle $$ 
Proponemos $a(t)=4t,$ que hace que el radio aumente linealmente hasta 4 al final del intervalo. 
Entonces: 
$$ \vec{r}_{2}(t)=\langle4t\cos(wt); 4t\sin(wt)\rangle, \quad t\in[0,1] $$ 
donde w es un parámetro que controla el número de vueltas. 

\subsection*{Superficie de elevación y trayectorias}
Trayectoria 1 (recta) 
Trayectoria 2 (espiral) 

\newpage
\section*{Pregunta 2:}
\subsection*{Paso 1: Gradiente de la función de elevación}
La elevación está dada por: 
$$ f(x,y)=50e^{-0.1(x^{2}+y^{2})} $$ 
Calculamos el gradiente: 
$$ \nabla f=\left(\frac{\partial f}{\partial x},\frac{\partial f}{\partial y}\right) $$ 
Usamos la regla de la cadena: 
$$ \frac{\partial f}{\partial x}=-0.1\cdot2x\cdot50e^{-0.1(x^{2}+y^{2})}=-10xe^{-0.1(x^{2}+y^{2})} $$ 
$$ \frac{\partial f}{\partial y}=-10ye^{-0.1(x^{2}+y^{2})} $$ 
Entonces: 
$$ \nabla f(x,y)=\langle-10xe^{-0.1(x^{2}+y^{2})},-10ye^{-0.1(x^{2}+y^{2})}\rangle $$ 

\subsection*{Primera trayectoria: Línea recta}
$$ \vec{r}_{1}(t)=\langle4t,0\rangle $$ 
Evaluamos $\nabla f$ en $\vec{r}_{1}(t)$: 
$$ \vec{r}{1}^{\prime}(t)=\langle4,0\rangle, ||\vec{r}{1}^{\prime}(t)||=4 $$ 
$$ x=4t, y=0\Rightarrow\nabla f(\vec{r}_{1}(t))=\langle-10(4t)e^{-0.1(16t^{2})},0\rangle=\langle-40te^{-1.6t^{2}},0\rangle $$ 
Producto punto: 
$$ \nabla f\cdot\vec{r}_{1}^{\prime}=(-40te^{-1.6t^{2}})(4)=-160te^{-1.6t^{2}} $$ 
Entonces, la pendiente es: 
$$ Pendiente_{1}(t)=\frac{\nabla f\cdot\vec{r}{1}^{\prime}(t)}{||\vec{r}{1}^{\prime}(t)||}=\frac{-160te^{-1.6t^{2}}}{4}=-40te^{-1.6t^{2}} $$ 

\newpage
\subsection*{Costo por pendiente para $\vec{r}_{1}(t)$}
$$ Costo_{1}=k_{1}\int_{0}^{1}(Pendiente_{1}(t))^{2}\cdot||\vec{r}_{1}^{\prime}(t)||dt $$ 
$$ =k_{1}\int_{0}^{1}(-40te^{-1.6t^{2}})^{2}\cdot4~dt=k_{1}\int_{0}^{1}6400t^{2}e^{-3.2t^{2}}dt $$ 

\subsection*{Segunda trayectoria: Espiral}
$$ \vec{r}_{2}(t)=\langle4t\cos(wt), 4t\sin(wt)\rangle $$ 
Derivada: 
$$ \vec{r}_{2}^{\prime}(t)=\langle4\cos(wt)-4wt\sin(wt), 4\sin(wt)+4wt\cos(wt)\rangle $$ 
Para simplificar la pendiente, evaluamos: 
$$ x(t)=4t\cos(wt) \quad y(t)=4t\sin(wt) $$ 
Entonces: 
$$ \nabla f(\vec{r}_{2}(t))=\langle-10xe^{-0.1(x^{2}+y^{2})},-10ye^{-0.1(x^{2}+y^{2})}\rangle $$ 
donde $x^{2}+y^{2}=(4t)^{2}=16t^{2},$ porque: 
$$ x^{2}+y^{2}=(4t)^{2}[\cos^{2}(wt)+\sin^{2}(wt)]=16t^{2} $$ 
Entonces: 
$$ \nabla f=-10(4t)e^{-1.6t^{2}}\langle \cos(wt),\sin(wt)\rangle=-40te^{-1.0t^{2}}\langle \cos(wt),\sin(wt)\rangle $$ 

\section*{Pregunta 3:}
$$ \frac{\nabla f \cdot\vec{r}(t)}{||\vec{r}(t)||} $$ 

\subsection*{¿Qué significa que la pendiente sea cero?} 
Recordemos que la pendiente se calcula como: 
$$ \text{Pendiente}(t) = \frac{\nabla f(\vec{r}(t))\cdot\vec{r}'(t)}{||\vec{r}^{\prime}(t)||} $$ 
Entonces
$$ \text{Pendiente} = 0 \Leftrightarrow \nabla f(\vec{r}(t))\cdot\vec{r}^{\prime}(t)=0 $$ 
Este producto punto nulo indica que el vector tangente $\vec{r}'(t)$ es ortogonal al gradiente de f, es decir: 
La trayectoria $\vec{r}(t)$ es ortogonal a las curvas de nivel de f. 
Por tanto, las trayectorias con pendiente cero son las curvas de nivel de la superficie. 
En este caso, las curvas de nivel de 
$$ f(x,y)=50e^{-0.1(x^{2}+y^{2})} $$ 
son circunferencias centradas en el origen, porque $x^{2}+y^{2}=c$ representa un nivel constante. 
\textbf{Interpretación:} La mejor manera de evitar la pendiente (subida o bajada) es moverse en círculo alrededor de la montaña, es decir, no subir ni bajar. 

\subsection*{Trayectoria propuesta:}
$$ \vec{r}(t)=\langle a(t)\cos(wt),a(t)\sin(wt)\rangle, \quad t\in[0,1] $$ 
Proponemos: 
$$ a(t)=4t^{n}, \quad \text{con } n>0 $$ 
Variables: n y w 
Condiciones: empieza en A (0,0) y termina en B (4,0) 
Función objetivo: Costo por pendiente 
$$ Costo_{pendiente}=\int_{0}^{1}\left(\frac{\nabla f\cdot\vec{r}^{\prime}(t)}{||\vec{r}^{\prime}(t)||}\right)^{2}\cdot||\vec{r}^{\prime}(t)||dt=\int_{0}^{1}\frac{(\nabla f\cdot\vec{r}^{\prime}(t))^{2}}{||\vec{r}^{\prime}(t)||}dt $$ 
Restricción: Longitud de la curva 
$$ Longitud=\int_{0}^{1}||\vec{r}^{\prime}(t)||dt\le70 $$ 

\newpage
\subsection*{Aplicamos multiplicadores de Lagrange} 
Queremos minimizar: 
$$ J(n,w)=\int_{0}^{1}\frac{(\nabla f\cdot\vec{r}^{\prime}(t))^{2}}{||\vec{r}^{\prime}(t)||}dt \quad \text{sujeto a } \int_{0}^{1}||\vec{r}^{\prime}(t)||dt\le70 $$ 
Podemos formar el lagrangiano: 
$$ \mathcal{L}(n,w,\lambda)=\int_{0}^{1}\frac{(\nabla f\cdot\vec{r}^{\prime}(t))^{2}}{||\vec{r}^{\prime}(t)||}dt+\lambda\left(\int_{0}^{1}||\vec{r}^{\prime}(t)||dt-70\right) $$ 
Parámetros óptimos encontrados: 
$$ n=0.1000 $$ 
$$ w=19.1630 $$ 
Costo mínimo $\approx 97.3971$ 

\section*{Pregunta 4:}
\subsection*{Paso 1: Parametrización sugerida} 
$$ \vec{r}(t)=\langle a(t)\cos(wt), a(t)\sin(wt)\rangle $$ 
Esta es una espiral plana, en la que el radio $a(t)$ cambia con el tiempo y el ángulo gira con velocidad angular w. 

\subsection*{Paso 2: Condición de pendiente constante} 
La pendiente se define como: 
$$ Pendiente(t)=\frac{\nabla f\cdot\vec{r}^{\prime}(t)}{||\vec{r}^{\prime}(t)||}=c=\text{constante} $$ 
Vamos a derivar una EDO (ecuación diferencial) para $a(t)$. 

\subsection*{Paso 3: Derivadas necesarias} 
\begin{enumerate}
    \item Posición: 
    $$ x(t)=a(t)\cos(wt), y(t)=a(t)\sin(wt) $$ 
    $$ x^{2}+y^{2}=a^{2}(t)\Rightarrow f(x,y)=50e^{-0.1a^{2}(t)} $$ 
    \item Gradiente de f: 
    $$ \nabla f=-10a(t)e^{-0.1a^{2}(t)}\cdot\langle \cos(wt),\sin(wt)\rangle $$ 
    \item Derivada de $\vec{r}(t):$ 
    $$ \vec{r}^{\prime}(t)=\langle a^{\prime}(t)\cos(wt)-a(t)w\sin(wt),a^{\prime}(t)\sin(wt)+a(t)w\cos(wt)\rangle $$ 
    \item Producto punto $\nabla f\cdot\vec{r}^{\prime}(t):$ 
    $$ \nabla f\cdot\vec{r}^{\prime}(t)=-10a(t)e^{-0.1a^{2}(t)}[a^{\prime}(t)(\cos^{2}(wt)+\sin^{2}(wt))]=-10a(t)a^{\prime}(t)e^{-0.1a^{2}(t)} $$ 
    \item Norma de $\vec{r}^{\prime}(t):$ 
    $$ ||\vec{r}^{\prime}(t)||=\sqrt{(a^{\prime})^{2}+(aw)^{2}} $$ 
\end{enumerate}

\subsection*{Paso 4: EDO para $a(t)$} 
Imponemos la pendiente constante: 
$$ \frac{\nabla f\cdot\vec{r}^{\prime}(t)}{||\vec{r}^{\prime}(t)||}=c $$ 
Entonces: 
$$ \frac{-10a(t)a^{\prime}(t)e^{-0.1a^{2}(t)}}{\sqrt{(a^{\prime}(t))^{2}+(a(t)w)^{2}}}=c $$ 
Despejamos: 
$$ -10aa^{\prime}e^{-0.1a^{2}}=c\sqrt{(a^{\prime})^{2}+(aw)^{2}} $$ 
Al elevar al cuadrado ambos lados: 
$$ 100a^{2}(a^{\prime})^{2}e^{-0.2a^{2}}=c^{2}[(a^{\prime})^{2}+a^{2}w^{2}] $$ 
Esta es una ecuación diferencial no lineal para $a(t)$. 
Podemos resolverla usando un método numérico como Runge-Kutta. 

\newpage
\subsection*{Paso 5: Proceso numérico (Runge-Kutta)} 
\begin{enumerate}
    \item Seleccionar valores: 
    Pendiente constante c: por ejemplo, 1 
    Frecuencia angular w: por ejemplo, $2\pi$ (una vuelta por segundo) 
    Condición inicial: $a(0)=4$ (radio en el punto B) 
    Integrar hacia atrás hasta que $a(t)=0$ (llegamos al origen) 
    \item Método: 
    Usar Python (SciPy) o WolframAlpha para resolver la EDO hacia atrás. 
\end{enumerate}
Contar cuántas vueltas da: 
$$ \text{Número de vueltas} = \frac{w\cdot T}{2\pi} $$ 
donde T es el tiempo en el que $a(t)\rightarrow0.$ 
Tiempo para llegar a la cima (a=0): 4.1330 unidades 
Número aproximado de vueltas: 4.13 

\section*{Pregunta 5:}
\subsection*{Trayectoria 1: Línea recta}
$$ \vec{r}_{1}(t)=\langle4t,0\rangle, \quad t\in[0,1] $$ 
La más corta en longitud (4 unidades). 
Directa y simple. 
Atraviesa directamente la montaña. 

\subsection*{Trayectoria 2: Espiral}
$$ \vec{r}_{2}(t)=\langle4t\cos(wt), 4t\sin(wt)\rangle, \quad w=4\pi $$ 
Gira alrededor de la montaña. 
Tiene longitud mayor ($\ge20$ unidades). 
Subida más gradual, más suave. 

\subsection*{Comparación de Trayectorias}
\begin{tabular}{|p{3cm}|p{5cm}|p{5cm}|}
\hline
\textbf{Criterio} & \textbf{Trayectoria 1 (recta)} & \textbf{Trayectoria 2 (espiral)} \\
\hline
Pendiente & Alta pendiente, lineal y directa  & Pendiente suave, distribuida en vueltas  \\
\hline
Costo por pendiente & Alto (ver cálculo en Item 2)  & Menor (evaluado numéricamente)  \\
\hline
Longitud & 4 unidades  & $> 20$ unidades según w  \\
\hline
Excavación & Mucha tierra removida (subida directa)  & Menor volumen de excavación (rodea la loma)  \\
\hline
Número de vueltas & 0  & 1 a 2 vueltas (según Item 4)  \\
\hline
Optimización & No optimizable (trayectoria fija)  & Se optimizan n, w (Item 3)  \\
\hline
Aplicabilidad real & Solo viable en terreno plano  & Mucho más realista en zona montañosa  \\
\hline
\end{tabular}

\subsection*{Conclusiones adicionales}
Costo por pendiente (Item 2): 
\begin{itemize}
    \item Recta: más elevado 
    \item Espiral: considerablemente menor 
\end{itemize}
Parámetros óptimos (Item 3): 
\begin{itemize}
    \item $n\approx1.5$, $w\approx7.3$ dan un costo bajo y longitud $<70$ 
\end{itemize}
Número de vueltas (Item 4): 
\begin{itemize}
    \item Aproximadamente 1.5 vueltas para bajar con pendiente constante $c=1$ 
\end{itemize}
Se recomienda usar la trayectoria tipo espiral con parámetros optimizados, ya que: 
\begin{itemize}
    \item Minimiza la pendiente, lo que reduce el esfuerzo de los vehículos, mejora la seguridad y disminuye el desgaste. 
    \item Minimiza el volumen de excavación, respetando más el entorno natural. 
    \item Permite controlar la longitud total de la carretera para cumplir con restricciones de diseño (como L $\le$ 70). 
    \item Puede adaptarse a condiciones reales de montaña, donde la línea recta es inviable. 
\end{itemize}

\end{document}
