# Requisito previo obligatorio:

# Tener encendida su máquina virtual (con Ubuntu en VMware, por ejemplo) y asegurarse de que su laptop esté conectada a la corriente (para que el rendimiento del procesador y el SSD no se estrangulen).

# 

# 

# Paso 1: Obtener la IP de la máquina virtual (Por si no la saben)

# Si arrancan la máquina virtual y no saben qué IP escribir en el navegador, deben hacer lo siguiente:

# Iniciar sesión en la terminal de Ubuntu dentro de la máquina virtual.

# Ejecutar el siguiente comando para ver su dirección IP:

# “ip a” (sin comillas)

# Buscar en el listado la interfaz de red (usualmente llamada ens33 o eth0) y anotar la dirección numérica que aparece al lado de inet (por ejemplo: 192.168.95.128). Esa es la IP que usarán en todo momento. 

# 

# 

# 

# 

# 

# Paso 2: Clonar el repositorio de Git

# No anden descargando archivos en ZIP como si fuera tarea de primaria. Se hace por terminal:

# En la misma terminal de Ubuntu escriban:

# git clone <URL-DEL-REPOSITORIO-GIT> enter

# cd nextcloud-stack-project enter

# (Si les dice que git no existe, instalenlo ejecutando: sudo apt update \&\& sudo apt install git -y y luego vuelven a tirar el comando de arriba). 

# 

# Paso 3: Entrar a Portainer (Y no asustarse con el navegador)

# Abran su navegador (Chrome, Brave, Firefox) ya sea en su Windows físico o dentro de la misma máquina virtual.

# Escriban la IP que anotaron en el Paso 1, pero agregando el puerto 9443 y asegurándose de poner https:// al inicio:https://<IP-DE-TU-MAQUINA>:9443 (Ejemplo: \[https://192.168.95.128:9443](https://192.168.95.128:9443))

# ¿El navegador les pone una pantalla roja de "Sitio no seguro"? No se pongan nerviosos. Denle clic en Avanzado y luego en el botoncito que dice Continuar a sitio no seguro (es por el certificado local, no hay virus).

# Inicien sesión con su usuario y contraseña de Portainer.

# 

# 

# 

# 

# Paso 4: Desplegar el Stack (El corazón del asunto)

# En el menú de la izquierda de Portainer, denle clic en Stacks.

# Arriba a la derecha, denle al botón azul + Add stack.

# En la cajita de Name, escriban textualmente: nextcloud-stack (ni una letra más ni una menos).

# Vayan al repositorio de Git, copien todo el contenido del archivo docker-compose.yml, regrésense a Portainer y péguenlo completito en el cuadro de texto grande (Web editor).

# Bajas hasta el fondo de la página y le dan clic al botón azul Deploy the stack.

# Paciencia: Tachen un par de minutos mientras Docker descarga e instala las cosas de internet.

# 

# 

# 

# 

# Paso 5: Revisar que el semáforo esté en verde

# En Portainer, váyanse al menú de la izquierda y denle clic en Containers.

# Tienen que ver obligatoriamente a los cuatro mosqueteros (nextcloud-app, nextcloud-db, nextcloud-redis, nextcloud-cron) con su etiqueta verde que dice running. Si alguno está en rojo, algo hicieron mal en el paso anterior.

# 

# 

# Paso 6: Entrar a la Nube y crear su cuenta

# Abran una nueva pestaña en el navegador.

# Escriban la IP de su máquina virtual, pero ahora con el puerto 8080 y con http:// (sin la 's'):http://<IP-DE-TU-MAQUINA>:8080 (Ejemplo: \[http://192.168.95.128:8080](http://192.168.95.128:8080))

# Les va a cargar la hermosa pantalla azul de Nextcloud avisándoles que detectó la base de datos.

# Inventen un Nombre de usuario y una Contraseña de administrador.

# Denle clic al botón azul Instalar y esperen 30 segundos.

# Cuando salga el menú de aplicaciones, denle clic a ¡Saltar! y listo, ya tienen su propia nube montada como profesionales.

# 

