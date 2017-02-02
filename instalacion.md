# Instalando Julia

## Instalación desde un binario

La forma más sencilla de instalar Julia es usando un *binario*: descarga el instalador adecuado para tu sistema operativo desde [aquí](http://julialang.org/downloads/). Si te interesan opciones específicas para tu sistema operativo o distribución consulta [esto](http://julialang.org/downloads/platform.html).

Una guía accesible que explica como utilizar los binarios u otros métodos sencillos de instalación se encuentra [aquí](https://en.wikibooks.org/wiki/Introducing_Julia/Getting_started).

Si estás utilizando Windows, probablemente también querrás instalar [`git` para Windows](https://msysgit.github.io/), el cual proporciona una terminal estilo Unix.

Por el momento, hay que utilizar la versión 0.5 de Julia, que es la versión estable.

## Instalación desde el código fuente

La instalación desde el código fuente ( la cual requiere compilar Julia en tu maquina ) tarda aproximadamente una hora y puede no salir bien a la primera. Considérala como una opción más avanzada, no para principiantes.

Para que funcione se requiere tener otras herramientas previamente instaladas, en particular `cmake` y `m4`; puedes ver los detalles completos en el  README de Julia [aqui](https://github.com/JuliaLang/julia).

En la terminal ejecuta lo siguiente:

```
$ git clone git@github.com:JuliaLang/julia.git
$ cd julia
$ make -j 4
```
El “-j 4” en la ultima linea indica que se van a usar cuatro núcleos (procesadores) para compilar Julia.

# Juno

Juno es un IDE ( Entorno de Desarrollo Integrado, “ Integrated Development Environment “ ) para Julia. Consiste en una serie de paquetes específicos que complementan el editor de texto [Atom](https://atom.io/) para permitir una interacción dinámica con julia.

Las instrucciones se encuentran [aquí](http://junolab.org).

# IJulia

[IJulia](https://github.com/JuliaLang/IJulia.jl) es una interfaz de Julia para   [Jupyter](https://jupyter.org/), el cual estaremos usando extensivamente para el curso.

Para instalarlo, es suficiente hacer, desde Julia mismo,

```
Pkg.add("IJulia")
```
Esto instalará una copia de Jupyter local que se utiliza sólo por Julia.
Después de que varias cosas se hayan instalado, se debería ver un mensaje de que IJulia se haya instalado exitosamente.

Si algo no funcionó o quieres más detalles, los puedes encontrar [aquí](https://github.com/JuliaLang/IJulia.jl).

Para correr el notebook, se pone (desde Julia)
```
using IJulia
notebook()
```
