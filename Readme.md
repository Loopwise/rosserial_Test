# Notas sobre *rosserial_arduino*
Debemos subir el código a nuestro Arduino y ejecutamos:
```
rostopic list
```
Nos brinda la siguiente salida:
```
/rosout
/rosout_agg
```
Entonces, para obtener los tópicos que hemos creado en nuestro Arduino, debemos ejecutar siempre:
```
rosrun rosserial_python serial_node.py <Serial_Port>
```
