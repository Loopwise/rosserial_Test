# Creando nuestro propio mensaje y usándolo en Arduino
Para este tutorial emplearemos un sensor MAG3110 (En realidad puede ser cualquiera que envíe al menos 1 valor al Arduino, de preferencia por I2C para que sea algo más directo).
## Tutoriales y pasos previos
### Pasos previos
- Conceptos básicos de ROS (Igual pueden leer los tutoriales que dejo para que recuerden algunas cosas ya que son muchas en ROS).
- Tener listas las conexiones electrónicas en nuestro Arduino y las librerías necesarias, en el caso del MAG3110 pueden encontrar la guía de conexiones y la respectiva librería [*aquí*](https://learn.sparkfun.com/tutorials/mag3110-magnetometer-hookup-guide-/all).
- Tener creado nuestro *catkin_ws* y entender cómo crear *ros_packages* y compilarlos.

Tutoriales:
- [Creating a Catking Workspace](http://wiki.ros.org/catkin/Tutorials/create_a_workspace)
- [Creating a ROS Packages](http://wiki.ros.org/ROS/Tutorials/CreatingPackage)
- [Building our ROS Package](http://wiki.ros.org/ROS/Tutorials/BuildingPackages)
- [ROS Messages Creation](http://wiki.ros.org/ROS/Tutorials/CreatingMsgAndSrv)

## ROS Package y Mensaje
1. We are going to create a *ROS Package* into our *catkin_ws* folder, to keep things simple; in my case, my *ROS Package* is called *serial_tests*.
2. Create _msg_ folder into out *ROS Package*.
3. Create an archive called _MAG3110.msg_ in _<ROS_Package>/msg_ folder and fill it as shown:
```
nano msg/MAG3110.msg
```
```
int16 X
int16 Y
int16 Z
```
4. Compile the _ROS Package_ and try the message using _rosmsg show <our_package>/MAG3110_:
```
loopwise@loopwise-ASUS-F15:~$ rosmsg show serial_tests/MAG3110 
int16 X
int16 Y
int16 Z
```