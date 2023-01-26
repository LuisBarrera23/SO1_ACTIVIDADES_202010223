
Luis Angel Barrera Velásquez		202010223
Sistemas Operativos 1	


**Actividad 1**



# Tipos de Kernel y sus Diferencias:

Dependiendo los sistemas operativos los Kernel se dividen en tres grupos de los cuales se explicara a continuación según lo investigado:

## Kernel monolítico
Un kernel grande para todas las tareas. Es el único responsable de la gestión de la memoria y de los procesos, de la comunicación entre procesos y proporciona funciones de soporte de drivers y hardware. Los sistemas operativos que usan el kernel monolítico son Linux, OS X y Windows.

## Kernel Microkernel
El microkernel se ha diseñado intencionadamente de un tamaño pequeño para que en caso de fallo no paralice todo el sistema operativo. No obstante, para que pueda asumir las mismas funciones que un kernel grande, está dividido en varios módulos. Como ejemplo de aplicación solo existe el componente Mach de OS X, ya que hasta ahora no hay ningún sistema operativo con microkernel.

## Kernel híbrido
La combinación del kernel monolítico y el microkernel se denomina kernel híbrido. En este caso, el kernel grande se hace más compacto y modulable. Otras partes del kernel pueden cargarse dinámicamente. Esto ya ocurre en cierta medida en Linux y OS X.



# User Mode vs Kernel Mode: 

## User mode
(modo usuario) cuando se inicia un programa en un sistema operativo, digamos Windows, se inicia el programa en modo de usuario. Y cuando un programa en modo usuario solicita ejecutarse, Windows crea un proceso y un espacio de direcciones virtuales (espacio de direcciones para ese proceso). Se sabe que las aplicaciones ejecutadas del lado del modo usuario tienen menos privilegios.

## Kernel Mode
(modo Kernel) El kernel es el programa central en el que se basan todos los demás componentes del sistema operativo, se utiliza para acceder a los componentes de hardware y programar qué procesos deben ejecutarse en un sistema informático y cuándo, y también administra la interacción entre el software y el hardware de la aplicación. A diferencia del modo usuario es que aquí las aplicaciones ejecutadas en el modo kernel tienen más privilegios y por lo tanto puede interactuar de manera mas directa con el hardware.