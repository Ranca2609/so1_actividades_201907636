<p>UNIVERSIDAD DE SAN CARLOS DE GUATEMALA</p>
<p>FACULTAD DE INGENIERIA</p>
<p>ESCUELA DE CIENCIAS Y SISTEMAS</p>
<p>SISTEMAS OPERATIVOS 1</p>
<p>PRIMER SEMESTRE 2022</p>

---


---


---


---


---


---


---

<center> <h1>ACTIVIDAD #1</h1> </center>
<center> <h1>TIPOS DE MODO KERNEL</h1> </center>



---


---


---


---




                        Carlos Roberto Rangel Castillo      201907636     


---


---


---


---




---


---


---


---


---

# <a name="nothing"></a>Microkernel

El enfoque micronúcleo consiste en definir una abstracción muy simple sobre el hardware, con un conjunto de primitivas o llamadas al sistema que implementan servicios del sistema operativo mínimos, como la gestión de hilos, el espacio de direccionamiento y la comunicación entre procesos.

El objetivo principal es la separación de la implementación de los servicios básicos y de la política de funcionamiento del sistema. Por ejemplo, el proceso de bloqueo de E/S se puede implementar con un servidor en espacio de usuario ejecutándose encima del micronúcleo. Estos servidores de usuario, utilizados para gestionar las partes de alto nivel del sistema, son muy modulares y simplifican la estructura y diseño del núcleo. Si falla uno de estos servidores, no se colgará el sistema entero, y se podrá reiniciar este módulo independientemente del resto. Sin embargo, la existencia de diferentes módulos independientes origina retardos en la comunicación debido a la copia de variables que se realiza en la comunicación entre módulos.

# <a name="nothing"></a>Kernel Monolitico

Los núcleos monolíticos suelen ser más fáciles de diseñar correctamente, y por lo tanto pueden crecer más rápidamente que un sistema basado en micronúcleo, pero hay casos de éxito en ambos bandos. Los micronúcleos suelen usarse en robótica embebida o computadoras médicas, ya que la mayoría de los componentes del sistema operativo residen en su propio espacio de memoria privado y protegido. Esto no sería posible con los núcleos monolíticos, ni siquiera con los modernos que permiten cargar módulos del núcleo.


# <a name="nothing"></a>Kernel Híbrido

Los núcleos híbridos fundamentalmente son micronúcleos que tienen algo de código «no esencial» en espacio de núcleo para que este se ejecute más rápido de lo que lo haría si estuviera en espacio de usuario. Este fue un compromiso que muchos desarrolladores de los primeros sistemas operativos con arquitectura basada en micronúcleo adoptaron antes de que se demostrara que los micronúcleos pueden tener muy buen rendimiento. La mayoría de sistemas operativos modernos pertenecen a esta categoría, siendo el más popular Microsoft Windows. XNU, el núcleo de Mac OS X, también es un micronúcleo modificado, debido a la inclusión de código del núcleo de FreeBSD en el núcleo basado en Mach. DragonFlyBSD es el primer sistema BSD que adopta una arquitectura de núcleo híbrido sin basarse en Mach.


# <a name="nothing"></a>Exonúcleos


Los exonúcleos, también conocidos como sistemas operativos verticalmente estructurados, representan una aproximación radicalmente nueva al diseño de sistemas operativos.

La idea subyacente es permitir que el desarrollador tome todas las decisiones relativas al rendimiento del hardware. Los exonúcleos son extremadamente pequeños, ya que limitan expresamente su funcionalidad a la protección y el multiplexado de los recursos. Se llaman así porque toda la funcionalidad deja de estar residente en memoria y pasa a estar fuera, en bibliotecas dinámicas.

Los diseños de núcleos clásicos (tanto el monolítico como el micronúcleo) abstraen el hardware, escondiendo los recursos bajo una capa de abstracción del hardware, o detrás de los controladores de dispositivo. En los sistemas clásicos, si se asigna memoria física, nadie puede estar seguro de cuál es su localización real.