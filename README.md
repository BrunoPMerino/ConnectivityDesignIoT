# IoT Connectivity Design – Air Quality Monitoring System

## Descripción del Proyecto

Este proyecto presenta el diseño y validación del componente de conectividad de un sistema IoT para el monitoreo de la calidad del aire en tiempo real en la región de Sabana Centro (Cundinamarca, Colombia).

El sistema utiliza una red de sensores inalámbrica (WSN) para recolectar datos ambientales como material particulado (PM2.5), gases contaminantes y variables climáticas, los cuales son transmitidos a un servidor IoT para su procesamiento y visualización.

---

## Objetivo

Diseñar e implementar una arquitectura de conectividad IoT que permita:

- Comunicación eficiente entre múltiples nodos sensores  
- Transmisión de datos en tiempo real  
- Escalabilidad del sistema  
- Integración con una plataforma IoT  

---

## Arquitectura del Sistema

El sistema está compuesto por:

-  Nodos sensores (PM2.5, MQ135, BME280)  
-  Red inalámbrica (WiFi - WSN)  
-  Router (Gateway)  
-  Servidor IoT  

 Flujo general:

1. Los nodos sensores capturan datos ambientales  
2. Los datos se transmiten vía WiFi  
3. El router actúa como gateway  
4. El servidor IoT procesa y almacena la información  

---

##  Protocolos de Comunicación

El sistema utiliza los siguientes protocolos:

- **WiFi** → Comunicación inalámbrica  
- **IP** → Direccionamiento de red  
- **MQTT** → Intercambio de datos IoT  

###  ¿Por qué MQTT?

Se eligió MQTT en lugar de HTTP debido a:

- Menor consumo de ancho de banda  
- Modelo publish/subscribe  
- Mayor eficiencia en sistemas distribuidos  
- Mejor desempeño en dispositivos con recursos limitados  

###  Implementación MQTT

- Nodos sensores → **Publishers**  
- Servidor IoT → **Broker**  
- Aplicaciones → **Subscribers**  

Ejemplo de flujo:
