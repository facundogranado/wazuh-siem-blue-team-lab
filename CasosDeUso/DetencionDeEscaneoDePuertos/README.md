# Detección de escaneo de puertos mediante Suricata
![image alt](https://github.com/facundogranado/wazuh-siem-blue-team-lab/blob/main/Capturas/Screenshot%20from%202026-02-07%2013-50-44.png)
## Contexto

Durante el monitoreo del tráfico de red en un entorno de laboratorio, el sistema de detección de intrusiones Suricata generó alertas asociadas a un posible escaneo de puertos dirigido a un host interno.

## Fuente del evento

* Herramienta de detección: Suricata (IDS)

* Tipo de tráfico: TCP, UDP, ICMP

* Origen del evento: Tráfico de red

* Integración: Alertas enviadas a SIEM (Wazuh / logs)

## Detección en Suricata

Suricata generó alertas basadas en reglas de detección de escaneo de puertos.

### Indicadores observados:

* Múltiples intentos de conexión TCP, UDP, ICMP

* Puertos de destino secuenciales

* Alta frecuencia de paquetes SYN

* Origen único hacia múltiples puertos del mismo host

## Proceso de triage
* 1-Validación de la alerta

Alerta generada por IDS confiable

Regla asociada a port scan detection

* 2-Análisis de contexto

IP origen: red interna del laboratorio

IP destino: endpoint Linux

No se detectaron payloads maliciosos

No hubo autenticaciones exitosas posteriores

* 3-Evaluación de impacto

Servicio afectado: red

Alcance: host individual

Impacto operativo: bajo

## Conclusión

El evento fue clasificado como escaneo de puertos detectado, sin evidencia de explotación posterior.

Dado que el origen corresponde a un entorno de laboratorio y no se observaron acciones adicionales, no se requirió escalamiento inmediato.

Se recomienda:

Mantener monitoreo

Correlacionar con logs de firewall y SIEM

Revisar reglas IDS para ajuste de sensibilidad


