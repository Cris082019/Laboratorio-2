## Laboratorio-2

<p align="center"><img width="45%" height="588" alt="image" src="https://github.com/user-attachments/assets/e1d3fd27-8b22-4101-9471-816074e450ec" /><img width="45%" height="546" alt="image" src="https://github.com/user-attachments/assets/3dc906bd-bbfb-476c-8ffe-431cfdbc80a9" /><img width="45%" height="551" alt="image" src="https://github.com/user-attachments/assets/1691d649-b192-4952-840a-169bb1c69d1f" /></p> <br>

Se debe tener en cuenta que la maquina virtual va ser el servidor central, esta contendra, contenedores, maquinas virtuales (VM) y las herramientas de monitoreo para que las dos redes adicionales puedan verse entre si, validar el trafico y analizar el mismo. A continuación se detalla la instalación de programas, la herramienta de monitoreo y lo requerido en el servidor principal, adicional se muestra la herramienta de monitoreo Zabbix.En cada una de estas imágenes se puede evidenciar el paso a paso para configurar respectivamente.<br><br>

## ***DEBIAN*** <br>
<p align="center"><img width="45%" height="283" alt="image" src="https://github.com/user-attachments/assets/83762dd3-f07a-42d0-b931-a3b3e36e1bcb" /> <img width="45%" height="453" alt="image" src="https://github.com/user-attachments/assets/bac2e385-2eb9-4957-ad7d-c9260e4503e0" /><img width="45%" height="399" alt="image" src="https://github.com/user-attachments/assets/7e3b5269-ae97-4038-8e26-bd994092df9e" /><img width="45%" height="392" alt="image" src="https://github.com/user-attachments/assets/0c374865-139d-4ca6-aa1c-963676f2982d" /></p><br><br>

## ***ZABBIX*** <br>
<p align="center"><img width="45%" height="320" alt="image" src="https://github.com/user-attachments/assets/0c1c6b46-53bb-472f-a6de-b729f74064b9" /><img width="45%" height="321" alt="image" src="https://github.com/user-attachments/assets/13a06009-7ed1-4268-b19d-4f2c520026c7" /><img width="45%" height="272" alt="image" src="https://github.com/user-attachments/assets/c4a648e6-f974-442e-b02b-1236501e89d6" /><img width="45%" height="260" alt="image" src="https://github.com/user-attachments/assets/0c87c181-cf72-44f9-92b8-05af0d3a2b56" /><img width="45%" height="276" alt="image" src="https://github.com/user-attachments/assets/2e91da0f-bf54-49f8-99d1-5783bfc0ab77" /><img width="45%" height="253" alt="image" src="https://github.com/user-attachments/assets/08bfea04-27e8-4c2b-9ebc-de5a86582cfb" /></p><br><br>

## ***GRAFANA*** <br>
<p align="center"><img width="45%" height="270" alt="image" src="https://github.com/user-attachments/assets/1b930dbd-31fe-45fa-9ea0-950d1d27e696" /><img width="45%" height="285" alt="image" src="https://github.com/user-attachments/assets/fb049e46-2442-4714-82d3-bb9f6c8152bb" /><img width="45%" height="317" alt="image" src="https://github.com/user-attachments/assets/1cff2c39-d371-4098-bfab-335d8693d496" /><img width="45%" height="263" alt="image" src="https://github.com/user-attachments/assets/41057a9d-34ae-4404-889b-742eef54b871" /></p><br><br>

## ***TRAFICO EN ZABBIX*** <br>
<p align="center"><img width="45%" height="265" alt="image" src="https://github.com/user-attachments/assets/ea9a60ee-017f-4ef4-a543-0ea007866b4c" /><img width="45%" height="163" alt="image" src="https://github.com/user-attachments/assets/ab7bd185-524a-434a-bbb4-46265d2f7e2c" /><img width="45%" height="248" alt="image" src="https://github.com/user-attachments/assets/5931d1f0-0f94-40fd-b67d-2b8e28651aa9" /><img width="45%" height="210" alt="image" src="https://github.com/user-attachments/assets/f0040d01-f0e4-4c39-a445-3499f72a92d4" /><img width="593" height="45%" alt="image" src="https://github.com/user-attachments/assets/e8d42ee2-b1f3-4d46-8f1a-79a9f016444b" /></p><br><br>

***CONTENEDORES*** <br>
A continuación se explica en imagenes que se debe realizar para la descarga de los contenedores que se van ha utilizar como subredes, con el fin de enviar trafico desde la subred hacia el servidor administrador y viceversa, eso se debe evidenciar en la herramienta de monitoreo. Para ello desde Windows se debe abrir PowerShell y ejecutarlo como administrador, luego ejecutar el comando *wsl ---install* este comando es como tener una maquina virtual UBUNTU, después de instalar, ahora debemos ejecutar los comandos de instalación de docker, en este caso se realizo isntalación de DOCKER en el PC, para que al ejecutar un comando me trajiera desde el servidor los contenedores que requiero, en las imagenes se evidencia lo escrito.<br>

<p align="center"><img width="45%" height="656" alt="image" src="https://github.com/user-attachments/assets/13871096-695a-484d-bd79-06cd8fb4a901" /><img width="45%" height="508" alt="image" src="https://github.com/user-attachments/assets/6c1ab35a-0d7a-4efc-a3a1-181a7847af01" /><img width="45%" height="714" alt="image" src="https://github.com/user-attachments/assets/e33a765c-38fe-4cc5-897f-d03fbc70f076" /></p> <br>

Se crean las subredes con los siguientes comandos en UBUNTU <br>
***docker network connect subred2 nodo-alpine*** <br>
**docker network connect subred2 nodo-kali** <br><br>

Luego se valida que los dos conectenedores esten activos y que se puedan ejecutar como se muestra en la imagen
<img width="974" height="505" alt="image" src="https://github.com/user-attachments/assets/5a92c8e7-103f-469b-9116-94a0ee94547b" />

