<h1 align="center"> Laboratorio 4 Robótica </h1>

## Universidad Nacional de Colombia
-------------------------------------------------------------
> ## Autores

  > - Carlos Mario Jiménez Novoa. [cajimn](https://github.com/cajimn)
  > - Ivanna Lisette Medina Cruz. [IvannaMedinac](https://github.com/IvannaMedinaC)
  > - Juan Sebastian Rangel Araque. [juanBananin](https://github.com/juanBananin)


## Procedimiento

> ## Determinar parámetros DH
Se determina los TCP de todas lasartivulaciones de robot, como se ve en la imagen acontinuación
![WhatsApp Image 2022-10-14 at 4 14 28 PM](https://user-images.githubusercontent.com/68668422/196011269-9272b426-2255-4be2-a015-2875ad0d804b.jpeg)


> ## Programa Python.
Se realiza la conexión entre dinamyxel y el programa creado en python, el cuál ejecuta con teclas, cada una de las posiciones establecidas en la guía de laboratorio. 

Para la conexión con Python se debe realizar la siguiente configuración en la terminal:

Primero se crea el paquete de catkin, en este caso la carpeta ctakin_ws

```shell
cd ~
mkdir catkin_ws
cd catkin_ws
mkdir src
catkin build
```

Luego se clona el repositorio de px.robot, para tener una guía de los scrpits que se usan para mover el robot.
```shell
cd ~/catwin_ws/src
git clone https://github.com/felipeg17/px_robot
cd ..
source devel/setup.bash
```

Se debe verificar el puerto al que está conectado el robot:
```shell
lsusb
```
Luego, se dan los permisos respectivos al puerto USB0
```shell
ls /dev/tty*
sudo chmod 777 /dev/ttyUSB0
```
Antes de ejecutar el launch se corren las siguientes líneas de código:
```shell
catkin build dynamixel_one_motor
source devel/setup.bash
```
Se procede a ejcutar el launch
```shell
roslaunch px_robot px_controllers.launch
```
Por último se abre la aplicación vs Code para ejecutar el programa de Python [jointPub](scripts/jointPub.m)

> ## Resultado 





https://user-images.githubusercontent.com/68668422/196011297-8d86ad41-814a-4f38-b1d9-553ff0dfab27.mp4



https://user-images.githubusercontent.com/68668422/196011293-479089bc-00ba-41f3-8f41-30927088b858.mp4



