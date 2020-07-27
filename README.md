                                 CONTADOR ASINCRONICO MEDIANTE LA IMPLEMENTACION DE FIP FLOPS TIPO D


1.PLANTEAMIENTO DEL PROBLEMA

Una de las aplicaciones de los flip flops son los contadores asincrónicos los cuales pueden ser implementados mediante el uso de flip flops tipo D, para ello deben estar conectados en cascada, así obtendremos
en cada salida de los flip flops un bit del conteo, esta implementación planea como reto principal la visualización de una secuencia no consecutiva de números decimales en dos Displays, para ello se deberá 
diseñar un circuito el cual nos permita observar en dos displays de 7 segmentos el conteo de 0 a 15,. Al añadir dicho circuito ¿Afectara el funcionamiento de nuestro contador?


2.OBJETIVOS

Objetivo general

-Implementar y comprobar el funcionamiento de un circuito contador ascendente asíncrono, implementado con flip-flop tipo D.

Objetivo específicos

-Investigar en funcionamiento de flip flops tipo D.

-Comprobar el funcionamiento del diseño del contador mediante la simulación en proteus e implementada en Tinkercad (laboratorio virtual).

-Convertir las salidas de cada flip flop de código BCD a decimal y mostrarlo en dos displays de 7 segmentos.


3.ESTADO DEL ARTE

El circuito asincrónico realizado por los Ingenieros Rubén González; Marco Bardón y José Antonio Salcines; primero nos define que es un contador de la siguiente manera: 
Un contador es un circuito en el que sus salidas siguen una secuencia fija que cuando acaba vuelve a empezar, o circuitos que reciben sus datos en forma serial ordenados en distintos intervalos de tiempo. Los pulsos de entrada pueden ser pulsos de reloj u originarse en una fuente externa y pueden ocurrir a intervalos de tiempo fijos o aleatorios. El número de salidas limita el máximo número que se puede contar. En nuestro estudio y para nuestro análisis se estudiará los contadores asincrónicos que en el contexto de los autores nos explica que son: Las salidas de cada flip-flop sirven de entrada CP para disparar otro flip-flop. El primer biestable tendrá una entrada de tipo asíncrono, es decir que se acertará de forma aleatoria y cuando lo haga el circuito realizará una cuenta. El resto del tiempo, los flip-flops no cambiarán su estado presente. En su diseño ellos pusieron como ejemplo lo siguiente; un contador asíncrono modulo 10: y los pasos para resolver son los siguientes. Paso 1: elegir un contador ascendente de 4 bits (de 0 a 15); paso 2: Detectar el 10 (1010 en binario) con una compuerta NAND y como ultimo paso Reset de todos los biestables cuando ocurra la detección.
(González, Bardón, & Salcines. (2019). Contadores. Manzanom. https://personales.unican.es/manzanom/Planantiguo/EDigitalI/CONTG5.pdf)

El sitio web Wilaeba Electrónica nos dan muchos puntos a tomar en cuenta además de ejemplos para lograr trabajar con distintos flip-flops incluido con el flip-flop que se desea trabajar que es el 74hc74. Los puntos a tomar que nos otorga este sitio web para nuestros diseños son los siguientes puntos: 
- Un contador asíncrono tiene como principal característica que cada flip flop que lo compone tiene diferente señal de reloj (clk).
- El temporizador 555 está configurado a una frecuencia de 1 Hz, es decir que el contador aumentará de valor cada segundo.
- Los integrados usados para los contadores con flip flops JK serán el cd4027 y 74hc112, y para los contadores con flip flops D serán el cd4013 y el 74hc74. Los integrados cd40 son tecnología cmos, y los integrados 74hc son tecnología ttl. Wilaeba Electrónica. (2017, 24 septiembre). Contador asíncrono de 4 bits ascendente.https://wilaebaelectronica.blogspot.com/2017/08/contador-asincrono-de-4-bits-ascendente.html

4.MARCO TEÓRICO


![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/marco%20teorico%201.png)

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/marco%20teorico%203.png)

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/marco%20teorico%202.png)

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/marco%20teorico%204.png)

5.DIAGRAMAS

Los diagramas hacen referencia a una representación visual de lo que se ha desarrollado enfocado al software y al hardware. Los diagramas son:
•Diagramas de bloques.
•Diagramas UML. (casos de uso-clase)
•Diagramas eléctricos.
•Diagramas esquemáticos.

Adicionalmente para el caso de diagramas eléctricos se debe hacer la explicación de los circuitos.






6.LISTA DE COMPONENTES

En este punto se indicará en una tabla todos los recursos que se han empleado para su desarrollo y todos los componentes electrónicos si fuera el caso.

7.MAPA DE VARIABLES

Este punto hace referencia a las variables que se emplean dentro de un programa, las cuales deben ser indicadas en la captura de una pantalla si son componentes visuales o especificados en una taba sin no son visibles en una interface. Se debe hacer referencia al tipo y la función que desempeñan en la aplicación.


8.EXPLICACIÓN DEL DISEÑO

Contador en código binario.
En esta etapa es necesario indicar que se utilizará un generador de señal de reloj (CLK) para los FLIP FLOP (FF), de igual forma usaremos una frecuencia aproximada de 1 Hz dados los valores de las resistencias R1 y R2 (330 Ohmios ).
Tomaremos en cuenta que:
- Un contador asíncrono tiene como principal característica que cada flip flop que lo compone tiene diferente señal de reloj (clk).
- El temporizador está configurado a una frecuencia de 1 Hz, es decir que el contador aumentará de valor cada segundo.
- Los integrados usados para los contadores con flip flops D serán el CD4013 y el 74hHC74. En nuestro caso usaremos el integrado 74HC74.

Para empezar nuestro análisis tendremos que plantear los estados, en este caso de 4 bits será de 0000 a 1111 es decir un conteo de de 0 a 15.

En esta parte vemos como se pasa de un estado al otro nuestra cuenta, lo que nos indica que las salidas de nuestros fip flops tendran una salida de 0 o 1. 

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/Tablas%20de%20transicion.PNG)

                       Tabla de verdad de cambio de estados 

Tabla de excitación del flip flop D

Ya que estamos usando un flip flop tipo D, tenemos la siguiente tabla, la cual nos muestra la respuesta a los cambios de estado que sufre el flip flop.

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/Tabla%20de%20exitacion.PNG)

 Tabla de exitacion de un flip flop tipo D
 
 Analizando el cambio de estado de cada columna tenemos el siguiente diagrama:
 
 ![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/Cambio%20de%20estados.png)
 
Una vez analisado los cambios de estado procedemos a implementar el circuito en el simulador proteus, para implementar nuestro circuito debemos tomar en cuenta lo siguiente:

-Necesitaremos 4 flip flops, uno por cada bit requerido en este caso seran 4 flip flops, seguido conectaremos la señal de reloj a nuestro primer flip flop, la salida de este significa el bit menos significativo de nuestro conteo.

-Cada entrada de reset y clear deberá estar conectada a Vcc, ya que se activan en bajo y nos las utilizaremos.

-Conectamos cada terminal D a Q’ y también a los clock’s. Con esto haremos que la salida anterior se duplique hacia la entrada del siguiente flip flop.

Implementación en proteus:

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/dise%C3%B1o%201.PNG)

                  Simulación en proteus
                  
Ahora veremos la implementación en tinkercad                 
                  
![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/dise%C3%B1o%202.png)

                  Simulación en Tinkercad
                
                 
9.- DESCRIPCIÓN DE PRERREQUISITOS Y CONFIGURACIÓN

En este punto se debe especificar las aplicaciones secundarias necesarias, la configuración del terminal, así como cualquier otra información necesaria para que pueda funcionar el proyecto, tanto en hardware como en software.

10.APORTACIONES

En este punto se indicará todo lo adicional fruto de lo investigado que se haya agregado al trabajo.

11.CONCLUSIONES

Se estable las conclusiones de cada asunto investigado, implicaciones para la teoría y resultados de las experiencias. Estos siempre estarán en relaciona los objetivos generales y específicos.

12.RECOMENDACIONES

Se establecen en función del proyecto y constituyen la base para un funcionamiento adecuado.

13.CRONOGRAMA

![alt text](https://github.com/Proyecto-Digitales/INFORME-N.2/blob/master/Img/Cronograma.PNG)


14.BIBLIOGRAFÍA

Emplear normas APA para el informe e IEEE para el artículo

15.ANEXOS

15.1 MANUAL DE USUARIO

Constituye un documento en el cual se ilustra con imágenes y un lenguaje claro cómo utilizar la aplicación, evitando mencionar código. Además debe presentar como armar, instalar o conectar la aplicación, evitando los esquemas circuitales.

15.2 HOJAS TÉCNICAS
