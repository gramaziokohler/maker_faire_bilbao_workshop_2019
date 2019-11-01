# Taller COMPAS FAB: Software de Fabrication Digital Robótica

> El objetivo de este taller es introducir conceptos básicos de robótica y demostrar la utilización de COMPAS FAB para resolver tareas de planificación y ejecución robótica en el contexto de fabricación digital.

:robot: :factory: :art:

## Preparación

Durante el taller, utilizaremos las siguientes herramientas:
 * Laptop con Windows 10 o Mac OS
 * [Anaconda 3](https://www.anaconda.com/distribution/)
 * [Docker Desktop](https://www.docker.com/products/docker-desktop):Si tienes Windows 10 Home Edition, puedes instalar Docker Toolbox en vez de Desktop._
  * [Visual Studio Code](https://code.visualstudio.com/): _Es recomendable instalar las extensiones de Python y de Docker._
  * [Rhino 6 & Grasshopper](https://www.rhino3d.com/download): (Opcional) _No es una herramienta de código abierto, pero puede utilizarse por 90 días en modo evaluación. No es un requisito fundamental, pero es muy útil en este contexto._


## Instalación

Es recomendable crear un entorno virtual en conda para no afectar otras dependencias:

    (base) conda create -n makerfairebilbao python=3.6
    (base) conda activate makerfairebilbao

Y luego instalar el framework:

    (makerfairebilbao) conda install compas_fab

Verificar la instalación:

    (makerfairebilbao) python
    >>> import compas_fab
    >>> compas_fab.__version
    '0.8.0'
    >>> exit()

Para habilitar el uso de COMPAS FAB dentro de Rhino/Grasshopper:

    (makerfairebilbao) python -m compas_rhino.install -v 6.0

## Documentación & Ejemplos

 * Diapositivas de la presentación
 * Documentación de [COMPAS](https://compas-dev.github.io/) & [COMPAS FAB](https://gramaziokohler.github.io/compas_fab/)
 * Configuración de ROS & MoveIt en docker
 * Ejemplos básicos:
   * Definir el modelo de un robot programáticamente
   * Cargar robots de Github
   * Cargar robots de ROS
   * Visualizar robots en Rhino 
   * Visualizar robots en Grasshopper
 * Ejemplos con ROS:  
   * Verificar la conexión
   * El "Hello world" de ROS: nodos listener & talker.
 * Ejemplos con ROS & MoveIt usando el robot Panda de Franka Emika
    * Cinemática directa
    * Cinemática inversa
    * Planificación de recorridos en espacio cartesiano
    * Planificación de recorridos en espacio libre
 
