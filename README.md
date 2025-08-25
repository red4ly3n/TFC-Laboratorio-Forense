# TFC Laboratorio Forense

Este proyecto tiene como objetivo crear un laboratorio de análisis forense digital y ciberseguridad,
orientado a la formación y la investigación. 

El entorno se basa en un sistema operativo principal
que aloja directamente las herramientas clave para la monitorización, y se complementa con
máquinas virtuales dedicadas al análisis forense y dinámico de malware.

En el sistema anfitrión (Ubuntu) se instala Wazuh, que se encarga de monitorizar el sistema,
analizar logs y generar alertas de seguridad en tiempo real.

Para el análisis forense, se utiliza una máquina virtual con Windows 10 en la que se ha instalado Autopsy.

Esta herramienta permite realizar análisis forense sobre imágenes de disco que contienen archivos y programas maliciosos,
facilitando la recuperación de datos y la detección de amenazas.

Cuando se detectan archivos sospechosos, estos se transfieren automáticamente a una máquina
virtual con Cuckoo Sandbox, que los ejecuta en un entorno aislado para observar su comportamiento.

Para ello, Cuckoo utiliza una segunda máquina virtual con Windows 7 como entorno de detonación, donde analiza acciones como conexiones externas, modificaciones del
sistema o intentos de evasión.

Toda la actividad del laboratorio es registrada y visualizada mediante el visor de eventos de Wazuh, lo que permite mantener un control centralizado y detectar anomalías de forma eficiente.

Además, se ha automatizado el flujo entre Autopsy y Cuckoo, optimizando el proceso y reduciendo la intervención manual. En conjunto, el laboratorio ofrece un entorno seguro y
controlado para el estudio práctico del análisis forense y el comportamiento del malware.
