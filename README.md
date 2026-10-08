# Análisis básico de un caso real de Ciberseguridad.

Este repositorio contiene un análisis básico sobre el incidente de ciberseguridad que afectó a **Change Healthcare** en febrero de 2024, relacionando el caso real con conceptos fundamentales de ciberseguridad, administración de riesgos y roles profesionales.

---

## 📋 Tabla de Contenidos
- [1. ¿Qué ocurrió en el incidente?](#1-qué-ocurrió-en-el-incidente)
- [2. Impacto Operativo y de Negocio](#2-impacto-operativo-y-de-negocio)
- [3. Términos Técnicos del Caso](#3-términos-técnicos-del-caso)
- [4. Roles Profesionales Participantes](#4-roles-profesionales-participantes)
- [5. Evidencias del Material Revisado](#5-evidencias-del-material-revisado)
- [6. Conclusión Personal](#6-conclusión-personal)

---

## 1. ¿Qué pasó?

A finales de febrero de 2024, la empresa Change Healthcare sufrió un ciberataque realizado por un grupo de ciberdelincuentes los cuales se les conoce como **ALPHV/BlackCat**, ataque realizado con el uso de un modelo de *Ransomware-as-a-Service* _(RaaS)_.

* **Ingreso:** Los atacantes utilizaron **credenciales comprometidas** para ingresar a un portal de acceso remoto de Citrix. 
* **Vulnerabilidad:** El servidor fue penetrado dado que este _**no mantenía activa la Autenticación Multifactor (MFA)**_, lo cual les dio facilidad para obtener acceso directo con solo las contraseñas.
* **Desarrollo:** Con su ingreso lograron filtrar una cantidad masiva de datos confidenciales y desplegaron un **ransomware** que cifró los sistemas de procesamiento de pagos y operaciones.

---

## 2. Impacto Operativo y de Negocio

Este ataque no solo afectó al área de sistemas, sino que paralizó operaciones en el mundo real:

* **Ecosistema de Salud:** Se paralizó la cámara de compensación de pagos médicos más grande de EE. UU.
* **Farmacias y Hospitales:** Quedaron imposibilitados para verificar seguros de pacientes en tiempo real o procesar recetas y cobranzas.
* **Impacto Financiero:** Clínicas y pequeños proveedores de salud enfrentaron severas crisis de liquidez al no poder facturar durante semanas.
* **Privacidad de Datos:** Exfiltración de datos médicos e identificación de millones de personas.

---

## 3. Términos Técnicos del Caso

| Término | Significado dentro del contexto del ataque |
| :--- | :--- |
| **Ransomware** | Malware de ALPHV/BlackCat usado para cifrar los archivos y paralizar los servidores. |
| **Credenciales Comprometidas** | Usuarios y contraseñas filtrados que permitieron el ingreso de los atacantes. |
| **MFA (Autenticación de Múltiples Factores)** | Control de seguridad ausente en Citrix; su falta fue la vulnerabilidad que permitió la entrada. |
| **SOC (Centro de Operaciones de Seguridad)** | Equipo encargado de detectar alertas anómalas de tráfico e intrusión en la red. |
| **Respuesta a Incidentes (IR)** | Protocolo activado para aislar sistemas, detener el cifrado y solicitar auditoría forense externa. |
| **Infraestructura Crítica** | Change Healthcare actúa como motor financiero vital del sistema de salud estadounidense. |

---

## 4. Roles Profesionales Participantes

Durante y después del incidente, participaron diversos perfiles de TI y Ciberseguridad:

1. **Analistas SOC:** Encargados del monitoreo continuo y detección de anomalías en logs.
2. **Especialistas en Respuesta a Incidentes (Incident Responders):** Responsables de aislar endpoints y contener la propagación del malware.
3. **Investigadores Forenses Digitales (DFIR):** Encargados de analizar cómo entraron los atacantes y determinar la extensión del daño.
4. **Administradores de Infraestructura y Redes:** Aislación de redes y reconfiguración de servidores de identidades.
5. **Oficiales de Cumplimiento y Privacidad:** Reporte a entidades reguladoras sobre la fuga de datos de pacientes.

---

## 5. Evidencias del Material Revisado

Evidencia 1
![Evidencia del caso](evidencias/evidencia1.png)
* Extraído de [Jama Network](https://jamanetwork.com/journals/jama-health-forum/fullarticle/2823757)

Evidencia 2
![Evidencia del caso](evidencias/Evidencia2.png)
* Extraído de [IBM](https://www.ibm.com/mx-es/think/news/change-healthcare-22-million-ransomware-payment)
---

## 6. Conclusión Personal

Este caso me permitió comprender que la ciberseguridad no es solo un tema técnico, sino una pieza fundamental para la continuidad del negocio y el bienestar social. Una omisión simple en controles básicos, como no activar MFA en un acceso remoto, puede desencadenar consecuencias devastadoras en la vida real. Como aprendizaje clave, mantener una buena higiene de ciberseguridad y contar con planes de respuesta estructurados es imprescindible en cualquier organización moderna.