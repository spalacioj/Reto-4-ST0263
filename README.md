# 1. Breve descripción de la actividad
Desplegar un CMS wordpress o elegido por ud, con su propio dominio y certificado SSL. El sitio lo llamará: reto3.sudominio.tld. En este reto3 utilizará un nginx COMO BALANCEADOR DE CARGAS (LB) de la capa de aplicación del wordpress o aplicación monolítica elegida. Además de lo anterior, se utilizarán 2 servidores adicionales, uno para BASE DE DATOS (DBServer) y otro para ARCHIVOS(FileServer). El DBServer podrá utilizar la BD en docker (recomendado) o nativa. Y el FileServer implementará un NFSServer. en un cluster de alta disponibilidad en Kubernetes.

## 1.1. Que aspectos cumplió o desarrolló de la actividad propuesta por el profesor (requerimientos funcionales y no funcionales)
Se realizo la implementacion de EKS en aws, se implemento la instalacion de un cluster de kubernetes con un servicio administrado en nube, Tambien se pudo implementar un balancedor de cargas de alta disponibilidad en la capa de aplicacion, alta disponibilidad en el base de datos y alta disponibilidad en la capa de almacenamiento, se desplego una base de datos dentro del cluster de kubernetes y se implemento el servicio de dominio pero en http

## 1.2. Que aspectos NO cumplió o desarrolló de la actividad propuesta por el profesor (requerimientos funcionales y no funcionales)
No se pudo implementar el servicio de archivos de nfs y tampoco se pudo implementar el https para el dominio

# 2. Información general de diseño de alto nivel, arquitectura, patrones, mejores prácticas utilizadas.
Como se ha observado a lo largo del curso, son varios los ambientes en los cuales se puede desplegar una aplicación, desde servidores en data centers propios (on-premise), servidores en nube con muchos servidores propios o administrados para mejorar su disponibilidad, menores costos, tiempos de despliegue de aplicaciones etc. En el reto 3, se desplegó una versión dockerizada de un CMS o LMS, con un balanceador simple de cargas, sin autoescalamiento y con dependencia de la base de datos y el sistema de archivos distribuido. En este reto 4, uds desplegarán la misma aplicación del reto 3, pero en un clúster Kubernetes en nube. Se utilizará un servicio administrado en nube como EKS de AWS o Kubernets de GCP.

# 3. Descripción del ambiente de desarrollo y técnico: lenguaje de programación, librerias, paquetes, etc, con sus numeros de versiones.
Se uso el academy learner lab de aws que se llama EKS. se uso la version de wordpress latest, la version de sql 5.7, version 1.9 de kubernetes, se uso la tecnologia kubectl para kubernetes en el cluster




