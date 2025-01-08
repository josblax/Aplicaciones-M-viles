# Aplicaciones Móviles

![50%](https://progress-bar.xyz/50)
____

## Mapa de aprendizaje

```bash
├──PARTE I: Introducción
    ├── Instalación de Android Studio
        ├── Instalación de Android Studio.
        ├── Instalación del Emulador para Android Estudio.
        ├── Fundamentos de una app
        ├── Componentes generales de una aplicación
        ├── Que es una actividad?
    ├── Crear un proyecto con Android Studio
        ├── Conocer el ambiente de desarrollo integrado
        ├── Conocer la interfase de usuario de Android Studio
        ├── Conocer los diferentes componentes que se integran al desarrollo de una app
        ├── Uso de dispositivos virtuales y fisicos para crear una app.
        ├── Uso del gradle y las dependencias que se pueden integrar para el desarrollo de una app
├── PARTE II Fundamentos de Programación.
    ├── Funciones principales de un lenguaje de programación.
    ├── Que es una palabra reservada?
    ├── Estructuras de Salida.
        ├── Instrucción de Salida cout
    ├── Nombres de Variables/Identificadores
    ├── Tipos de Variables
        ├── Enteros. Signed/Unsigned. Números sin punto decimal.
            ├── Como se declaran?
            ├── Como se asignan valores desde programa?
            ├── Como se asignan valores desde consola?
            ├── Como se imprimen en consola?
            ├── short
            ├── int
            ├── long long
            ├── unsigned
        ├── Fraccionarios/Decimales. Números con punto decimal
            ├── Como se declaran?
            ├── Como se asignan valores desde programa?
            ├── Como se asignan valores desde consola?
            ├── Como se imprimen en consola?
            ├── float. 7-8 decimales de precisión.
            ├── double. 15-16 decimales de precisión.
        ├── Booleanos. Valor lógico 0,1 {true, false}
            ├── bool
            ├── función boolalpha
        ├── Textos y caracteres
            ├── Como se declaran?
            ├── Como se asignan valores desde programa?
            ├── Como se asignan valores desde consola?
            ├── Como se imprimen en consola?
            ├── Como convertir un string a número.
            ├── string
            ├── char
        ├── Contenedores
            ├── Arreglos
            ├── Clase Arreglo <array>
            ├── Vectores <vector>
                ├── Iteradores
                ├── Modificadores
        ├── Clases y Objetos
            ├── Estructuras <struct>
            ├── Clases y Objetos
                ├── Encapsulación
                ├── Herencia
                ├── Polimorfismo
├── PARTE III Decisiones
    ├── Tipos de condiciones de if..else
        ├── if simple. solamente if.
        ├── if doble. if..else
        ├── if's anidados
        ├── instrucción switch
├── PARTE IV Instrucciones Cíclicas
    ├── Instrucción for
    ├── Instrucción do..while
    ├── Instrucción while.
```


## Que es Android?

* Android es un sistema operativo de código abierto, creado por Google específicamente para su uso en dispositivos móviles (teléfonos celulares y tabletas).
* Basado en Linux (kernel 6.1)
* Puede ser programado en C y C++ pero se hace más desarrollo de aplicaciones en Java (Java accesa a bibliotecas C vía JNI (Java native Interface). Google ha seleccionado Kotlin como el lenguaje predominante para que todas las aplicaciones lo usen en el futuro.
* Soporta Bluetooth, Wi-Fi y redes 3G, 4G y 5G.

 ## Android y Java

* Después de escribir un programa en Java o Kotlin para Android, hacemos clic en un botón y nuestro código se transforma en un nuevo código, el código que entiende Android. 

* Esta otra forma se denomina **dalvik bytecode** y el proceso de transformación se denomina compilación.  

* Luego, cuando el usuario instala nuestra aplicación, el código de **dalvik bytecode** es es traducido por otro proceso conocido como Android Runtime (ART) en código máquina.

* Este es el formato de ejecución más rápido posible, bytecode se cambia a código máquina que es rápido para el dispositivo. Este proceso de compilación añade a nuestra app la optimización necesaria para la administración de batería y memoria.

* El proceso correcto es **java byte code -> dalvik bytecode**

## Ecosistema de Android

Una plataforma abierta móvil, para dispositivos móviles, embebidos (ejemplo, dispositivo Android para autos, TV’s etc.) y usables en nuestro cuerpo.

* Google es el principal responsable de su actualización, aunque otras personas contribuyen al sistema.

* Cada fabricante de dispositivos móviles puede adaptar “customize” Android a sus necesidades.

## Situacion Actual de Android

* Android es el sistema operativo más utilizado en el mundo.  

* Incluso Windows está rezagado con respecto a la adopción generalizada de la plataforma funcional de teléfonos inteligentes propiedad de Google. iOS ni siquiera está cerca.  

* Cuando se trata de dispositivos móviles, Apple ha ganado algo de terreno en los últimos años, pero Android todavía impulsa alrededor del 75% de todos los teléfonos inteligentes y tabletas.

[fuente](https://techjury.net/blog/android-market-share/)

## Mercado Actual

* Android tiene una cuota del 71.77%, mientras que iOS representó el 27.6% del mercado de sistemas operativos móviles. 

* Hay más de 2,500 millones de usuarios activos de Android en más de 190 países. 

* Un total de 1,570 millones de dispositivos Android vendidos en 2022, frente a los 0.980 millones de 2021. 

* Android representó el 44.86% del mercado de sistemas operativos móviles, mientras que iOS representó el 54.74% en enero de 2023. 

* El 97% del malware para teléfonos inteligentes se dirige a teléfonos Android. 

* Las ventas de Android están aumentando en Estados Unidos, Europa, Japón, India y China. 

* La cuota de mercado de Samsung en Estados Unidos fue del 28.57% en 2023, frente al 26.45% de 2022. 

* La participación de Android en todos los dispositivos conocidos fue del 70.97%.

[fuente actualizada 2024](https://techjury.net/blog/android-market-share/)

## Arquitectura de Android

La arquitectura de Android está organizada en varias capas, cada una con su propia función específica:

* Aplicaciones: La capa más alta donde se encuentran las aplicaciones que los usuarios instalan y utilizan.

* Marco de Aplicaciones (Application Framework): Proporciona varias APIs que los desarrolladores pueden usar para construir sus aplicaciones. Aqui residen los siguientes sistemas: View System, Content Provider, Resoure Manager, Notification Manager, Activity Manager.

* Bibliotecas y Android Runtime: Incluye bibliotecas nativas escritas en C/C++ y la máquina virtual ART (Android Runtime) que ejecuta las aplicaciones.

* Dalvik Virtual Machine. Entorno en el que cada aplicación Android corre android cada aplicación se ejecuta en su propio proceso, con su propia instancia de la VM Dalvik.

* Dalvik ha sido escrito tal que un dispositivo puede correr múltiples máquinas virtuales eficientemente. Virtual machine basada en registros.


* Bibliotecas Principales: Ofrecen funcionalidades básicas como gráficos, bases de datos y navegación web.

* Kernel de Linux: La base del sistema operativo Android, que maneja la gestión de memoria, procesos, seguridad y controladores de hardware


![Arquitectura](https://source.android.com/static/images/android-stack.svg?hl=es-419)
