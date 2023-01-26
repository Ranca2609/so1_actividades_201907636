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
<center> <h1>USER MODE VS KERNEL MODE</h1> </center>



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

# <a name="nothing"></a>USER MODE 

El sistema está en modo de usuario cuando el sistema operativo está ejecutando una aplicación de usuario, como el manejo de un editor de texto. La transición del modo usuario al modo kernel ocurre cuando la aplicación solicita la ayuda del sistema operativo o se produce una interrupción o una llamada al sistema.

El bit de modo se establece en 1 en el modo de usuario. Se cambia de 1 a 0 cuando se cambia del modo usuario al modo kernel.


# <a name="nothing"></a>KERNEL MODE 

El sistema se inicia en modo kernel cuando arranca y después de cargar el sistema operativo, ejecuta aplicaciones en modo usuario. Hay algunas instrucciones privilegiadas que solo se pueden ejecutar en modo kernel.

Estas son instrucciones de interrupción, gestión de entrada y salida, etc. Si las instrucciones privilegiadas se ejecutan en modo usuario, es ilegal y se genera una trampa.

El bit de modo se establece en 0 en el modo kernel. Se cambia de 0 a 1 cuando se cambia del modo kernel al modo usuario.

---

---

<p align="center">
User Mode vs Kernel Mode
  <a href="#"><img src="Usuario vs Kernel.png"/></a>
  Fuente: https://www.geeksforgeeks.org/difference-between-user-mode-and-kernel-mode/
</p>


## Diferencias


| Usuario | Kernel |
| ------ | ------ |
| En modo usuario, el programa de aplicación se ejecuta y se inicia. | En modo kernel, el programa tiene acceso directo y sin restricciones a los recursos del sistema. |
| En el modo de usuario, un solo proceso falla si ocurre una interrupción.  | En el modo Kernel, todo el sistema operativo puede dejar de funcionar si se produce una interrupción |
| El modo de usuario también se conoce como modo sin privilegios, modo restringido o modo esclavo. | El modo kernel también se conoce como modo maestro, modo privilegiado o modo de sistema.|
| En el modo de usuario, todos los procesos obtienen un espacio de direcciones virtuales separado. | En modo kernel, todos los procesos comparten un único espacio de direcciones virtuales. |
| Mientras está en modo usuario, las aplicaciones tienen menos privilegios. | 	En el modo kernel, las aplicaciones tienen más privilegios que en el modo usuario. |

