---
title: "Tonometro de pulso"
date: 2026-02-05
categories:
  - Tutorial
tags:
  - jekyll
  - toc
  - guia
layout: single
toc: true
toc_sticky: true
---

Este articulo describe el desarrollo de un tonometro de pulso a acoplar con el BioAmp.

## ¿Que es un tonometro de pulso?

Un tonometro de pulso es un dispositivo que mide la presión arterial de forma no invasiva. 

## Introducción

Hace unos años se acercó al Laboratorio de Prototipado un médico con la inquietud de poder medir la presión arterial de forma no invasiva. La idea era poder incorporar esta funcionalidad al BioAmp, de manera de poder medir simultáneamente la presión arterial y la actividad eléctrica del corazón. Estas mediciones son utilizadas para evaluar la rigidez arterial. 
Inicialmente se itentó replicar un sistema con el que ya estaban trabajando que implicaba el uso de un sensor de presion invasivo. Las tubuladuras del sensor se llenaban con agua, un extremo de las mismas era modificado con una suerte de "membrana" (dedo de guante o globo) y se colocaba en la muñeca del paciente. La presion arterial movia la membrana flexible y la columna de agua se movia en consecuencia, permitiendo medir la presión arterial. El sensor se conectaba a uno de los canales diferenciales del BioAmp, la salida tipo puente de Wheatstone generaba una dierencia de potenical proporcional a la presión ejercida.
Este sistema no resulto muy efectivo, al menos en nuestra implementacion, con dificultades para el llenado de las tubuladuras, baja sensibilidad, aire dentro de las mismas.


## Rediseño

Decidimos rediseñar el sistema desde cero, modificando el transductor, buscando algo más facil de utilizar. Durante la investigacion bibliografioa que emprendemos cuando llevamos adelante un proyecto, una de las fuentes de busqueda son patentes. Una que nos resulto particularmnente interesante es la patente US20050177047A1 "Device for, and a method of, transcutaneous pressure waveform sensing of an artery and a related target apparatus".

![US20050177047A1-20050811-D00000][center](/assets/images/tonometro/US20050177047A1-20050811-D00000.png)

En la imagen del dispositvio se podia observar el sensor de presion, una suerte de cono de gel que transmitia la presion arterial desde la superficie exterior al sensor. Ya estabamos en la busqueda de sensores de presion invasiva para evaluar su reutilizacion, y de la imagen nos parecio reconocer el encapsulado del sensor utilizado, si bien no estamos 100% seguros se parece mucho al MPX2300DT1 de NXP (https://www.nxp.com/docs/en/data-sheet/MPX2300D.pdf)

![MPX2300DT1][center](/assets/images/tonometro/MPX2300DT1.png)



## Modelado CAD

Comenzamos el modelado CAD del dispositivo, buscando replicar la geometria de la patente. Para el cono de gel decidimos utilizar silicon, fabricando un molde en PLA. 
Pasamos por varias iteraciones para optimizar la geometria del cono de gel, buscando la menor superficie de contacto posible.

![prototipos][center](/assets/images/tonometro/prototipos.jpg)  

## Pruebas

![video_test][center](/assets/images/tonometro/video_test.mp4)  

## Conclusión
