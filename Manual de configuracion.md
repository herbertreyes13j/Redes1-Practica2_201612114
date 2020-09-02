# Practica 2 - Redes de computadoras 1

Esta practica consiste en que debe configurar y administrar los dispositivos de una nueva infraestructura de red. La empresa tiene operando 6 máquinas. Cada una de estas tendrá su propia subred para poder llevar una mejor gestión y control de cada departamento, pero también se necesitan que todas puedan comunicarse entre sí por medio de 1 router.


Las configuraciones necesarias para poder realizar esta practica, seran mostradasa continuacion paso a paso. 
## Configuración de la topologia
  - Paso 1
  Armamos la topologia como se muestra a continuacion, para luego poder ir realizando las diferentes configuraciones que se describiran. 
  ![alt text](imagenes/topo.PNG "Title")
  - Paso 2
  Procedemos con la configuracion del router, para esto vamos a configurar las interfaces. Los comandos a ingresar son:
    * conf t <--- para iniciar en modo de configuracion
    * int f0/0 <-------- Para seleccionar la interfaz a asignarle la ip
    * ip address 192.168.14.254 255.255.255.0 <---- definimos la direccion ip 
    * no shut
    * exit <------ salimos del modo de configuracion
    * rw <------ sirve para guardar todos los cambios
    * sh run 
![alt text](Imagenes/F0_0.png "Title")
  - Paso 3
  Realizamos lo mismo que en el paso 2, solamente que se cambia a int f0/1 y la direccion ip seria 192.168.11.254 255.255.255.0
![alt text](Imagenes/F0_1.png "Title")
  - Paso 4
  Procedemos a configurar la maquina virtual, solamente accedemos a panel de contorl luego network y en IP Address le asignamos la direccion IP: 192.168.14.30 y le damos en apply para ver que los cambios de han guardado. 
![alt text](Imagenes/Linux1.png "Title")

  - Paso 5
  Procedemos a configurar VPC2, el comando a  utilizar es: ip direccion_ip/mascara_subred gateway, en el caso de esta seria 192.168.14.15/24 192.168.14.254. 
![alt text](Imagenes/VPC2.png "Title")

  - Paso 6
  Procedemos a configurar VPC3, el comando a  utilizar es: ip direccion_ip/mascara_subred gateway, en el caso de esta seria 192.168.11.15/24 192.168.11.254. 
![alt text](Imagenes/VPC3.png "Title")

  - Paso 7
  Procedemos a configurar VPC4, el comando a  utilizar es: ip direccion_ip/mascara_subred gateway, en el caso de esta seria 192.168.11.30/24 192.168.11.254. 
![alt text](Imagenes/VPC4.png "Title")

  - Paso 8
 Finalmente procedemos al respectivo Ping, para comprobar que la configuracion fue hecha de forma correcta. 
![alt text](Imagenes/Ping.PNG "Title")
