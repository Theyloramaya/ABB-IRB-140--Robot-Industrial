# ABB-IRB-140--Robot-Industrial
Presentado por Theylor Andres Amaya Villabon taamayav@unal.edu.co

En este repositorio, puedes acceder a todos los archivos esenciales que te serán útiles para llevar a cabo la primera práctica de la asignatura de Robótica en la Universidad Nacional de Colombia durante el semestre 2022-2. Esta práctica se enfoca en la creación de una herramienta adaptable para el Manipulador industrial ABB IRB 140. Su principal objetivo es permitir la ejecución de un proceso de escritura utilizando un marcador, siguiendo las trayectorias predefinidas en el programa en RAPID.

Además, es necesario que el robot escriba el nombre de los dos estudiantes encargados del proyecto como parte integral de la implementación práctica. Esto significa que la rutina de RAPID que se debe desarrollar surgirá como resultado de un proceso de simulación en Robot Studio. Durante este proceso, es crucial llevar a cabo una calibración precisa tanto de la herramienta como del Workobject. Esto garantizará la generación de una trayectoria segura y precisa que incluirá la escritura de los nombres de los estudiantes de manera precisa y legible.

# Diseño de la herramienta 

El objetivo fundamental es lograr que esta herramienta se ajuste de manera precisa y segura a la brida del eje 6 del Manipulador industrial ABB IRB 140. Esta adaptación permitirá que la herramienta funcione de manera estable y efectiva durante la ejecución de la tarea.

Una característica esencial de esta herramienta es su capacidad para mantener de manera constante un marcador en su extremo. El marcador, en este contexto, actuará como el efector final de la herramienta y será utilizado para escribir los nombres de los dos estudiantes encargados del proyecto.

![image](https://github.com/Theyloramaya/ABB-IRB-140--Robot-Industrial/assets/144027596/6621fd93-bc0d-45b5-9cae-a29e15b11c28)


En este proyecto, hemos aprovechado la ingeniosa funcionalidad de los marcadores, que se ajustan a su respectiva tapa en la parte posterior de los mismos. Esta característica nos ha servido como punto de partida para crear una solución ingeniosa. Aprovechando el archivo CAD de la brida del eje 6 del Manipulador industrial ABB IRB 140, hemos llevado a cabo un proceso de diseño y manufactura aditiva para desarrollar un acople específico. Una vez se tiene el modelo fisico se toman medidas y se crea un modelo CAD fiel a su morfologia.

# Diseño del Workobject
Se plantea la idea de llevar a cabo el trabajo en un tablero dispuesto horizontalmente, ubicado a una altura de 20 cm sobre la superficie del robot. Este enfoque permite establecer un entorno de trabajo óptimo para el Manipulador industrial ABB IRB 140. Además, se ha establecido que las dimensiones del objeto de trabajo serán de 308x270 mm.

Para comenzar, se ha creado un modelo que sigue estas dimensiones, lo cual sirve como punto de partida para posteriormente crear el objeto de trabajo en RobotStudio. 

![image](https://github.com/Theyloramaya/ABB-IRB-140--Robot-Industrial/assets/144027596/51679b1e-6fb4-4dcd-a7b1-41dd62f393fc)

# Robot Studio

**Creación de la herramienta** 

La creación de esta herramienta involucra un proceso esencial que comienza con la importación del modelo CAD. Esta importación es crucial ya que proporciona una representación del tamaño y estructura de la herramienta que estamos desarrollando. Sin embargo, más allá de la apariencia física, el aspecto más crítico y fundamental de esta herramienta es la posición y orientación de su Punto de Control de la Herramienta (TCP, por sus siglas en inglés).

La alineación precisa del TCP con respecto al modelo real de la herramienta es un componente vital de este proceso. El TCP es el punto en el extremo de la herramienta que el robot utiliza como referencia para ejecutar tareas específicas. Asegurar que la posición y la orientación del TCP coincidan perfectamente con las del modelo físico es de suma importancia, ya que esto garantiza que el robot funcione de manera precisa y efectiva en la tarea asignada.
![image](https://github.com/Theyloramaya/ABB-IRB-140--Robot-Industrial/assets/144027596/ad554d5a-c6f0-40e5-b133-aebd6e797364)

**Creación Workobject**

La creación del Workobject es un paso fundamental en este proyecto, ya que establece la base para la ejecución precisa de las trayectorias en el robot. En este proceso, hemos tomado como referencia el modelo del tablero que será utilizado en la tarea. Para lograr esto, hemos empleado un enfoque que se basa en la definición de tres puntos clave en el tablero. Estos puntos se utilizan para crear un sistema de referencia específico para el tablero.

Este sistema de referencia es esencial, ya que servirá como el marco de trabajo en el que se ejecutarán las trayectorias del robot. Cada punto en las trayectorias estará referenciado a este sistema, lo que garantiza que el robot se desplace de manera precisa y coherente en relación con el tablero.

![image](https://github.com/Theyloramaya/ABB-IRB-140--Robot-Industrial/assets/144027596/3c7711b5-eabc-4bdb-a9d9-505737d90229)

# Parametros de la trayectoria

# Simulación

La simulación desempeña un papel esencial en este proyecto, ya que nos permite observar y evaluar el comportamiento del robot en un entorno controlado antes de su implementación física. En esta fase de simulación, podemos destacar varios aspectos fundamentales que proporcionan una visión clara y detallada del proceso.

En primer lugar, es evidente que el robot sigue de manera precisa las trayectorias contenidas en el código RAPID. Esto es un logro significativo, ya que asegura que las letras y la decoración se coloquen exactamente donde se pretende en el objeto de trabajo, garantizando la legibilidad y la estética de la escritura.

Además, durante la simulación, se pueden observar las variaciones de velocidad que el robot experimenta a lo largo de la tarea. Esta información es esencial para ajustar y optimizar la velocidad de operación del robot, lo que puede ser importante para garantizar una escritura uniforme y de alta calidad.

La zona tolerable de error es otro aspecto destacado de la simulación. Este factor determina el margen de error aceptable en la ejecución de las trayectorias. Identificar y definir esta zona es crucial para garantizar que el robot pueda adaptarse a pequeñas desviaciones sin comprometer la calidad de la escritura.

Por último, la secuencia de rutinas definida es esencial en la simulación. El orden en el que se ejecutan las acciones, desde el retorno a la posición de inicio ("Home") hasta la escritura de las letras y la decoración, y luego nuevamente al retorno a la posición inicial, se ha planificado cuidadosamente para lograr una ejecución coherente y efectiva de la tarea en el siguiente orden:

Home

letras T-h-e-y

decoración (":v")

letras J-u-a-n

Home
![image](https://github.com/Theyloramaya/ABB-IRB-140--Robot-Industrial/assets/144027596/0c8dfb07-e0b1-42ad-84e8-45a9b387f49c)

# Implementación

# Conclusiones y aspectos a mejorar
