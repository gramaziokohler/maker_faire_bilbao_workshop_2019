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

Es recomendable crear un entorno virtual en conda para no afectar otras dependencias. Vamos a crear un entorno e instalar el framework en una sola linea:

    (base) conda create -n mfb19 compas_fab python=3.6

Verificar la instalación:

    (base) conda activate mfb19
    (mfb19) python
    >>> import compas_fab
    >>> compas_fab.__version
    '0.8.0'
    >>> exit()

Para habilitar el uso de COMPAS FAB dentro de Rhino/Grasshopper:

    (mfb19) python -m compas_rhino.install -v 6.0

## Documentación & Ejemplos

* Diapositivas de la presentación
* Documentación de [COMPAS](https://compas-dev.github.io/) & [COMPAS FAB](https://ramaziokohler.github.io/compas_fab/)
* [Configuración de ROS & MoveIt en docker](docker-panda/)
* [Abrir MoveIt! en tu navegador](http://localhost:8080/vnc.html?resize=scale&autoconnect=true) (una vez iniciado el docker compose del panda)
* Ejemplos básicos:
  * [Definir el modelo de un robot programáticamente](ejemplos/01_define_model.py)
  * [Cargar robots de Github](ejemplos/02_robot_from_github.py)
  * [Cargar robots de ROS](ejemplos/03_robot_from_ros.py)
  * [Visualizar robots en Rhino](ejemplos/04_robot_artist_rhino.py)
  * [Visualizar robots en Grasshopper](ejemplos/05_robot_artist_grasshopper.ghx)
* Ejemplos básicos con ROS:
  * [Verificar la conexión](ejemplos/06_check_connection.py)
  * El "Hello world" de ROS: nodos conversadores
    * [Nodo listener](ejemplos/07_ros_hello_world_listener.py)
    * [Node talker](ejemplos/08_ros_hello_world_talker.py)
* Ejemplos con ROS & MoveIt usando el robot Panda de Franka Emika:
  * [Cinemática directa](ejemplos/09_forward_kinematics_ros_loader.py)
  * [Cinemática inversa](ejemplos/10_inverse_kinematics_ros_loader.py)
  * [Planificación de recorridos en espacio cartesiano](ejemplos/11_plan_cartesian_motion_ros_loader.py)
  * [Planificación de recorridos en espacio libre](ejemplos/12_plan_motion_ros_loader.py)
  * Gestión de la escena de planificación:
    * [Agregar objetos a la escena](ejemplos/13_add_collision_mesh.py)
    * [Agregar objetos agrupados a la escena](ejemplos/14_append_collision_meshes.py)
    * [Eliminar objetos de la escena](ejemplos/15_remove_collision_mesh.py)
* [Playground de Grasshopper](ejemplos/16_robot_playground.ghx)
