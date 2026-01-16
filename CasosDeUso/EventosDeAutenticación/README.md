# Detección de intentos de autenticación fallidos en endpoint Windows
## Contexto

Durante el monitoreo continuo de eventos de seguridad mediante Wazuh, se detectaron múltiples intentos de autenticación fallidos sobre un endpoint Windows perteneciente a un usuario válido del sistema.

## Fuente del evento

* Sistema operativo: Windows

* Origen del log: Windows Security Event Log

* Herramienta: Wazuh (agente + manager)

 ## Detección en Wazuh

Wazuh generó una alerta basada en eventos de seguridad relacionados con autenticación fallida.

Indicadores observados:

* Múltiples eventos de login fallido

* Usuario válido

* Origen local

* Intervalo de tiempo reducido

 ## Proceso de triage

Se aplicó el siguiente análisis:

### 1-Validación de la alerta

Evento proveniente de fuente confiable (Windows Security Log)

### 2-Contexto del evento

Usuario legítimo del sistema

### 3-Horario laboral

Sin cambios posteriores en privilegios

### 4-Evaluación de severidad

Impacto: bajo

Probabilidad: baja

## Conclusión

El evento fue clasificado como actividad legítima, posiblemente asociada a un error del usuario al ingresar credenciales.

No se evidenciaron indicadores adicionales de compromiso ni necesidad de escalamiento.

Se recomienda mantener monitoreo y correlacionar con otros eventos en caso de recurrencia.
