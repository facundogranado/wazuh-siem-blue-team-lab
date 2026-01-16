# Detección de cambios en la configuración del sistema (Firewall)
![image alt](https://github.com/facundogranado/wazuh-siem-blue-team-lab/blob/43df01cb3813e20b824aec02b5b1d0b1209904a0/Capturas/Pasted%20image.png)
## Contexto

Durante el monitoreo continuo de eventos de seguridad mediante Wazuh, se detectó un cambio en la configuración del firewall de un endpoint Linux.
El objetivo fue identificar si el cambio correspondía a una acción administrativa legítima o a una modificación no autorizada.


## Fuente del evento

* Sistema operativo: Linux

* Componente monitoreado: UFW (Uncomplicated Firewall)

* Herramienta: Wazuh (agente + File Integrity Monitoring)

## Detección en Wazuh

Wazuh generó una alerta al detectar una modificación en archivos de configuración asociados al firewall.

Indicadores observados:

* Cambio en reglas de UFW

* Timestamp preciso del evento

* Usuario responsable del cambio

* Archivo afectado

## Proceso de triage

### 1-Validación de la alerta

Evento generado por FIM (File Integrity Monitoring)

### 2-Contexto del evento

Cambio realizado por usuario con privilegios

Horario laboral

No se observaron otros eventos sospechosos correlacionados

### 3-Evaluación de severidad

Servicio afectado: firewall

Alcance: endpoint individual

## Conclusión

El cambio fue clasificado como modificación administrativa legítima, realizada en el marco de tareas de mantenimiento.

No se evidenciaron indicadores de compromiso ni necesidad de escalamiento inmediato.

Se recomienda:

Registrar el cambio

Verificar alineación con políticas internas

Mantener monitoreo posterior

