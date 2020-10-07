# TFG-ELASTEST-TEST
Dependencias para el despliegue y tests end-to-end realizados con RobotFramework, un framework de testing hecho en Python.

## Objetivos
Este repositorio tiene el objetivo de extraer archivos ajenos a las pruebas con RobotFramework
del repositorio principal [tfg-elastest-test-robotframework][tfg-elastest-test-robotframework]

Servirá para desplegar tanto appium como selenium grid para hacer pruebas sobre un móvil. Estos ficheros
se pueden desplegar solos, pero su cometido principal es para la ayuda al despliegue de la infrastructura
necesaria que necesitan los test para su ejecución.

Ver repositorio principal del proyecto donde se hace uso de estas funcionalidades [tfg-elastest][tfg-elastest]

## Componentes
El contenido de este repositorio se divide en dos partes.

### RobotFramework Tests
Este es el componenete principal del repositorio y donde se encuentran las pruebas end-to-end junto 
a archivos que le ayudarán a integrarse con Jenkins.

### Archivos para el despliegue de los tests
Fichero docker-compose con variables de entorno configuradas para ser usado por el módulo principal del
proyecto [tfg-elastest][tfg-elastest].

Este docker-compose despliega un Selenium Grid y un Appium para poder automatizar las pruebas de móvil 
realizadas en el repositorio de RobotFramework [tfg-elastest-test-robotframework][tfg-elastest-test-robotframework]


## Despliegue
En este módulo únicamente esta preparado para desplegar un Senium Grid y, conectado a él, un Appium:
```git clone --recurse-submodules https://github.com/DavidCorreas/tfg-elastest-test.git```
`docker-compose up --build`

Para desplegar las pruebas consultar el módulo de RobotFramework [tfg-elastest-test-robotframework][tfg-elastest-test-robotframework]


[tfg-elastest-test-robotframework]: https://github.com/DavidCorreas/tfg-elastest-test-robotframework
[tfg-elastest]: https://github.com/DavidCorreas/tfg-elastest
