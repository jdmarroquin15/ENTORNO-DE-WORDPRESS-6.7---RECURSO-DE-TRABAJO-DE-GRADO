
# Entorno de Pruebas de Penetración en plugins de WordPress 6.7

Este repositorio contiene un entorno controlado diseñado para la evaluación de seguridad de los plugins de WordPress 6.7 mediante pruebas de intrusión.


### Vulnerabilidades explotadas en los Plugins

- 🔴Fuerza bruta usuario administrador, contraseña debil
- 🔴 CVE-2025-8081 - Elementor Website Builder 3.29.0
- 🔴 CVE-2024-9162 - All-in-One WP Migration and Backup 7.86
- 🔴 CVE-2024–9944 - WooCommerce 9.0.2
- 🔴 CVE-2024-4984 - Yoast SEO 20.2

### USO VERSION VULNERABLE DEL ENTORNO

- Bajar el repositorio y entrar en la carpeta
- Devolver al commit primer commit con la version vulnerable

````bash
git clone https://github.com/jdmarroquin15/ENTORNO-DE-WORDPRESS-6.7---RECURSO-DE-TRABAJO-DE-GRADO.git
cd ENTORNO-DE-WORDPRESS-6.7---RECURSO-DE-TRABAJO-DE-GRADO.git
git checkout 0b00ad2
````

Antes de ejecutar el contenedor, se debe tener en cuenta que el puerto al que se realiza el PortForwarding esta configurado en el puerto 8080:80 (8080 host -> 80 contenedor). Por lo que, se debe verificar que el puerto 8080 no este ocupado previamente. Si es asi, se debe cambiar en el docker-compose.yml


### Ejecutar el contenedor

````bash
cd wordpress_tg
docker-compose up -d
````

### USO VERSION NO VULNERABLE DEL ENTORNO

- Detener el entorno vulnerable si se esta ejecutando
- Volver a la version actual del repositorio con el entorno No Vulnerable
- Ejecutar o correr el contenedor actual

````bash
docker-compose down
cd ../
git checkout master
cd wordpress_tg
docker-compose up -d
````

### INFORMACIÓN ADICIONAL

Entorno Vulnerable
- Usuario: admin
- Contraseña: adminpass123

Entorno no Vulnerable
- Usuario: seg_admin
- Contraseña: 8tw^u><3G65X


Este proyecto fue utilizado con fines educativos. Y se permite el uso externo para sus respectivas pruebas y proyectos.

### CREDITOS

Realizado por: 

- Juan Diego Marroquin
- Juan Pablo Rodriguez
