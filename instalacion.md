# Instalando Julia

#### Instalación desde un binario

La forma más sencilla de instalar Julia es usando un *binario*: descarga el instalador adecuado para tu sistema operativo desde [aquí](http://julialang.org/downloads/). Si te interesan opciones específicas para tu sistema operativo o distribución consulta [esto](http://julialang.org/downloads/platform.html).

Si estás utilizando Windows, probablemente también querrás instalar [`git` para Windows](https://msysgit.github.io/), el cual proporciona una terminal estilo Unix.

#### Instalación desde el código fuente

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

# Ijulia

[IJulia](https://github.com/JuliaLang/IJulia.jl) es una interfaz de Julia para   [Jupyter](https://jupyter.org/) (antes IPython notebook), el cual estaremos usando extensivamente para nuestro curso.

#### Requisitos de Python

Primero necesitaras instalar IPython. [Actualmente las partes de Ipython que no se relacionan directamente con Python se están separando en un paquete llamdo Jupyter.] La manera mas sencilla de hacer esto es instalar la distribución gratuita de [Anaconda](http://continuum.io/downloads), la cual incluye IPython, la librería de graficación `matplotlib`, y varios paquetes útiles de Python.

Si prefieres algo más ligero y rápido, puedes usar `pip` ( un instalador de paquetes de Python ):

```
pip install --upgrade ipython[all]
```
En Ubuntu, primero necesitas ejecutar:
```
sudo apt-get install python-dev
sudo apt-get install python-pip
```
En Mac OSX también tendrás que agregar las siguientes lineas
```
export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```
al archivo `.bash_profile` el cual está en tu directorio “home” ( si este archivo no existe entonces necesitaras crearlo con esas dos lineas como contenido ).

#### Instando IJulia

Una vez que Ipython notebook este instalado, corre Julia en una terminal
```
julia
```

Si la instalación previa de julia fue exitosa, el aspecto de tu terminal cambia y aparece el logo de Julia. Este es un modo interactivo para trabajar llamado [REPL](https://en.wikibooks.org/wiki/Introducing_Julia/The_REPL) (read-eval-print loop). Desde aquí añade el paquete “IJulia” con el siguiente comando:

```
Pkg.add("IJulia")
```
Después de que varias cosas se hayan instalado, se debería de ver un mensaje de que Julia exitosamente encontró tu instalación de IPython y que se han creado todos los archivos necesarios.

Si algo no funcionó o quieres más detalles los puedes encontrar [aquí](https://github.com/JuliaLang/IJulia.jl).
