# Wazuh SIEM Lab – Blue Team 

![image alt](https://github.com/facundogranado/wazuh-siem-blue-team-lab/blob/7d558038fc2eb34dc4244e30823225a662a90b0a/Capturas/Screenshot%20from%202026-01-16%2001-35-50.png)


##  Descripción general

Este proyecto documenta el despliegue y uso inicial de **Wazuh como SIEM/XDR**, con el objetivo de simular tareas típicas de un **SOC / Blue Team**: monitoreo, análisis y triage básico de alertas de seguridad.

---

##  Objetivos del proyecto

* Implementar un SIEM funcional utilizando **Wazuh**
* Integrar endpoints **Windows y Linux**
* Analizar eventos de seguridad reales
* Realizar **triage básico de alertas**
* Documentar hallazgos de forma clara

---

##  Arquitectura del laboratorio

* **Wazuh Manager + Dashboard**
* **1 Endpoint Windows**
* **1 Endpoint Linux**


---

##  Tecnologías y herramientas utilizadas

* Wazuh (SIEM / XDR)
* Linux
* Windows
* Logs del sistema
* Dashboards y reglas de Wazuh

---

##  Casos de uso implementados

### 1. [Monitoreo de eventos de autenticación](https://github.com/facundogranado/wazuh-siem-blue-team-lab/tree/main/CasosDeUso/EventosDeAutenticaci%C3%B3n)
### 2. Cambios en configuración del sistema

### 3. Escaneos de puertos a un endpoint

### 4. Modificación en un archivo
---

##  Proceso de triage aplicado

Para cada alerta analizada se siguió el siguiente flujo:

1. Identificación del evento
2. Validación de la fuente
3. Evaluación de severidad e impacto
4. Decisión: monitoreo / escalamiento
5. Documentación del caso

---

##  Aprendizajes clave

* Comprensión práctica del funcionamiento de un SIEM
* Importancia del contexto al analizar alertas
* Diferencia entre eventos, alertas e incidentes
* Valor de la documentación clara en un entorno SOC

---

