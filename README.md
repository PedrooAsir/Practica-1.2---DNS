# Practica-1.2---DNS


# Instalación de bind9 en Ubuntu 22.04
Instalamos bind9 en la máquina virtual con “sudo apt install -y bind9”. Una vez instalado comprobamos su estado (bind9) y (named) con → “*systemctl status bind9*” y continuamente tenemos que ver que está activo (running).

Ahora procedemos a configurar los archivos creados en /etc/bind y /var/lib/bind (No nos olvidemos de poner mismas IP y red tanto en la máquina como en el host). 
Primero configuraremos los archivos de /etc/bind, poniendo y modificando los archivos de configuración. Una vez hecho esto iremos a /var/lib/bind y crearemos la base de datos para el DNS ya que la carpeta estará vacia. (Si los pasos anteriores se hicieron bien, la carpeta de dicha ruta var/lib/bind, debería estar vacía como se dijo anteriormente).

Continuamente, después de hacer esto, ponemos la máquina en adaptador puente, por ejemplo en Modo Promiscuo para que otras máquinas puedan detectarla o hacer (en nuestro caso), Digs. 

Entramos en la Terminal y tendremos que ver la IP de nuestra máquina y comprobar que está con el puerto 53 (el determinado). Lo haremos con la siguiente herramienta → “netstat -ptan” para ver nuestra interfaz DNS (IP) que se creó con “adaptador puente” con el puerto 53 (es el determinado).

Finalmente, ya solo hacemos dig @[Dicha IP] test.asircastelao.int (por ejemplo) y nos debería devolver (o solucionar) la dirección IP que haya en nuestra base de datos con ese dominio.
