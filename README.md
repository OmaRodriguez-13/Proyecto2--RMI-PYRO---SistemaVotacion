# Proyecto2--RMI(PYRO)--SistemaVotacion
 
 ## Descripción general

El proyecto consiste en un sistema de votación usando la arquitectura RMI (Remote Method Invocation) en PYRO (Python Remote Objects):

1. El servidor establece:
    - Tema de la votación.
    - Número de opciones.
    - Opciones.
2. El o los cliente(s) podrán ir seleccionando la opción(es) que más les convenga para votar.

## Instalación y Configuración

### Source code

Descargar el zip que contiene los archivos fuente del proyecto.

### Vía git 

```bash
git clone https://github.com/OmaRodriguez-13/Proyecto2--RMI-PYRO---SistemaVotacion
```

## Guía Rápida

### Requerimientos

- Importante: Conexión a la misma red.
- Desactivar Firewall de Windows para evitar cualquier error de conexión.
- Editor de código (por ejemplo: [Visual Studio Code]).
- Python 3.11.2

#### Pyro4:

```bash
pip install pyro4
```

### Instrucciones de uso

Cambie la linea 47 del archivo [system.py] con la direccón ip de su equipo servidor.

[![line47.png](https://i.postimg.cc/VLSSCx6F/line47.png)](https://postimg.cc/Tp6Y8Hny)

Si no conoce la dirección ip de su equipo, puede introducir el siguiente comando en el cmd.

```bash
ipconfig
```

## Ejecución

### Servidor

Abra un terminal y ejecute [system.py] con alguno de los siguiente comandos:

```bash
py system.py
```

```bash
python system.py
```

El servidor devolverá la URI creada.

[![system-py.png](https://i.postimg.cc/0NvrhrCt/system-py.png)](https://postimg.cc/YvXpWrZg)


### Cliente

En otra terminal, ejecute [voter.py] con alguno de los siguientes comandos:

```bash
py voter.py
```

```bash
python voter.py
```

En las ventanas siguientes deberá introducir la ip y el puerto del servidor, respectivamente.

[![ip.png](https://i.postimg.cc/fy1RCbLf/ip.png)](https://postimg.cc/sG9zDs5M)

[![port.png](https://i.postimg.cc/9X90XGNx/port.png)](https://postimg.cc/149sJNS6)

[![voter.png](https://i.postimg.cc/CLYhF981/voter.png)](https://postimg.cc/Dmjk6jBk)


## Testeo

### Servidor [system.py]

En el servidor el usuario deberá ingresar lo siguiente:

1. El tema de la votación:

[![tema.png](https://i.postimg.cc/nrNwhyRL/tema.png)](https://postimg.cc/hQb0C5qF)

2. El número de opciones para la votación:

[![nop.png](https://i.postimg.cc/VkqHzHjY/nop.png)](https://postimg.cc/NK0x4DJV)

3. Las opciones:

[![opciones.png](https://i.postimg.cc/DmVBTq0J/opciones.png)](https://postimg.cc/m1wQ31QB)

4. Además, el sistema le pedirá al usuario confirmar si desea o no agregar más opciones:

[![mas.png](https://i.postimg.cc/9Q2HP9bQ/mas.png)](https://postimg.cc/PPS7TP0g)


### Cliente [voter.py]

[![gui.png](https://i.postimg.cc/BQ9nyXpd/gui.png)](https://postimg.cc/z37NHD9j)

Ya iniciado el programa cliente, el usuario podrá seleccionar la opción que más le parezca conveniente de acuerdo al tema de la votación.

[![gui.png](https://i.postimg.cc/BQ9nyXpd/gui.png)](https://postimg.cc/z37NHD9j)

[![seleccion.png](https://i.postimg.cc/Kc95Dh5k/seleccion.png)](https://postimg.cc/w3mJ9PZg)

[![votacion.png](https://i.postimg.cc/BQkcR5kJ/votacion.png)](https://postimg.cc/ykhZZR7G)

Nota: El usuario tendrá la opción de eliminar votos, en caso de haber confusión. También en caso de haber más de 1 cliente conectado, será necesario utilizar el botón "Actualizar" para refrescar los resultados de la votación.
