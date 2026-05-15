# 

# 

# 

# 

# 

# 

# 

# 

# UD07. Elaboración de documentación técnica y uso de aplicaciones de propósito general

## Sprint 1: El Marco Legal y la Estructura del "Relato"

# 

Nombre y Apellidos: Alba Durán Bernal  
Ciclo: DAM  
Fecha: 15/05/2026

# INDICE

[**ANEXO I: Plantilla y Ejemplo de Análisis de Necesidades	3**](#anexo-i:-plantilla-y-ejemplo-de-análisis-de-necesidades)

[1\. Análisis de Necesidades	3](#1.-análisis-de-necesidades)

[1.1. Contexto y Problemática Actual	3](#1.1.-contexto-y-problemática-actual)

[1.2. Solución Propuesta: Infraestructura Híbrida Docker-Guacamole	3](#1.2.-solución-propuesta:-infraestructura-híbrida-docker-guacamole)

[1.3. Justificación Técnica y Beneficios (TCO)	4](#1.3.-justificación-técnica-y-beneficios-\(tco\))

[**Webgrafia	4**](#webgrafia)

# ANEXO I: Plantilla y Ejemplo de Análisis de Necesidades {#anexo-i:-plantilla-y-ejemplo-de-análisis-de-necesidades}

## 1\. Análisis de Necesidades {#1.-análisis-de-necesidades}

### 1.1. Contexto y Problemática Actual {#1.1.-contexto-y-problemática-actual}

La empresa presentaba riesgos críticos de seguridad al depender de conexiones RDP y SSH directas, lo que obligaba a abrir múltiples puertos en el firewall y aumentaba la superficie de ataque. Según la ingeniería de software, un análisis de requisitos riguroso es vital para evitar fallos en producción.

### 1.2. Solución Propuesta: Infraestructura Híbrida Docker-Guacamole {#1.2.-solución-propuesta:-infraestructura-híbrida-docker-guacamole}

Se ha implementado una solución basada en \*\*Apache Guacamole\*\* sobre \*\*Docker Compose\*\*. Esta arquitectura permite la centralización del acceso vía web (puerto 8080/443), eliminando clientes externos pesados y permitiendo una auditoría centralizada.  
A diferencia de las conexiones RDP individuales, esta solución ofrece \*\*aislamiento\*\*, ya que cada servicio opera en contenedores estancos, evitando conflictos de dependencias. Además, garantiza un control de acceso unificado que simplifica la gestión técnica y refuerza la seguridad perimetral.

* **Centralización**. Un único punto de acceso vía web (puerto 8080/443) para todos los servicios internos.  
* **Aislamiento**. Gracias a los contenedores, cada servicio (PostgreSQL, Guacamole, SSH) y para evitar conflictos opera en su propio entorno  
* **Seguridad**. Se elimina la necesidad de clientes externos pesados, permitiendo una auditoría centralizada de las conexiones.

### 1.3. Justificación Técnica y Beneficios (TCO) {#1.3.-justificación-técnica-y-beneficios-(tco)}

La elección de esta tecnología optimiza el Coste Total de Propiedad (TCO) al utilizar software con licencias permisivas (Apache y PostgreSQL), evitando costes recurrentes de licenciamiento. Asimismo, la portabilidad de Docker asegura un Plan de Recuperación ante Desastres (DRP) mínimo, garantizando la disponibilidad profesional del sistema.

# Webgrafia {#webgrafia}

* Drake, J. M. (2008). **Análisis de requisitos y especificación de una aplicación** \[en línea\] Disponible en: https://www.ctr.unican.es/asignaturas/ingenieria\_software\_4\_f/doc/m3\_08\_especificacion-2011.pdf  
* García Notario, D. (2015). **Análisis de requisitos en el desarrollo del software**  \[en línea\] Disponible en: https://e-archivo.uc3m.es/rest/api/core/bitstreams/a66b0a2d-fa7c-483f-ac5e-1476ff2da8eb/content

