# ⚠️ PROYECTO ARCHIVADO — LAB-APP-SYSTEM-PHP

> **Estado:** Archivado · Solo lectura · Sin mantenimiento activo
>
> Este repositorio ha sido archivado y ya no recibe nuevas funcionalidades, correcciones de errores, actualizaciones de dependencias ni soporte activo.
>
> Se conserva con fines **históricos, documentales y de referencia técnica**.

---

## 📋 Descripción

**LAB-APP-SYSTEM-PHP** fue un sistema de gestión integral desarrollado para laboratorios de **mecánica de suelos, materiales e ingeniería civil/construcción**.

La aplicación permitía gestionar gran parte del ciclo de vida de las muestras de laboratorio, incluyendo:

* Registro e inventario de muestras.
* Programación y asignación de ensayos.
* Captura de datos de laboratorio.
* Ejecución y procesamiento de diferentes tipos de ensayos.
* Revisión y validación de resultados.
* Generación de reportes en PDF.
* Gestión de información relacionada con clientes, proyectos y muestras.

El proyecto corresponde a una versión histórica del sistema y **no debe considerarse una versión actualmente soportada o recomendada para nuevos despliegues**.

---

## 🚦 Estado del proyecto

| Estado              | Descripción                                                          |
| ------------------- | -------------------------------------------------------------------- |
| 🔴 **Archivado**    | El desarrollo activo ha finalizado.                                  |
| 🔒 **Solo lectura** | No se esperan cambios funcionales.                                   |
| ❌ **Sin soporte**   | No se atienden incidencias ni solicitudes de nuevas funcionalidades. |
| 📚 **Referencia**   | Se conserva para consulta histórica y técnica.                       |

### Motivo del archivo

El proyecto fue archivado al finalizar su ciclo de desarrollo/mantenimiento activo. El repositorio se conserva para preservar el código fuente, la estructura del sistema, los procesos implementados y la información técnica asociada a la aplicación.

---

## 🛠️ Stack tecnológico

* **Backend:** PHP, utilizando una combinación de programación procedural y orientación a objetos (POO).
* **Frontend:** HTML5, CSS3 y JavaScript vanilla.
* **Comunicación asíncrona:** Peticiones AJAX para carga, actualización y almacenamiento de información sin recargar determinadas vistas.
* **Base de datos:** MySQL.
* **Generación de documentos:** TCPDF.
* **Gestión de dependencias:** Composer.
* **Arquitectura:** Aplicación PHP basada principalmente en páginas, scripts y endpoints directos.

> ⚠️ Las versiones exactas de PHP, MySQL, Composer y demás dependencias corresponden al entorno histórico del proyecto y pueden no ser compatibles con versiones modernas.

---

## 🧪 Módulos y ensayos implementados

El sistema incluía interfaces y lógica específica para diferentes ensayos y procesos de laboratorio.

### Granulometría

* Agregados finos.
* Agregados gruesos.
* Material rocoso.
* Tamizado.
* Hidrómetro.
* Doble hidrómetro.

### Contenido de humedad

* Horno.
* Microondas.
* Masa constante.
* Balanza.

### Densidades y peso volumétrico

* Peso volumétrico.
* Densidad de arena.
* Densidad bulk.
* Conteo y ensayo de gamma.

### Ensayos de resistencia

* Compresión Simple (UCS).
* Prueba de Carga Puntual (PLT).
* Dureza Leeb.

### Compactación

* Proctor Estándar.

### Otros ensayos y módulos

* Permeabilidad granular.
* Límites de Atterberg.
* Absorción y Gravedad Específica (SG).
* Desgaste Los Ángeles (LAA).
* Sanidad (Soundness).
* Pinhole.
* Consolidación.
* Grout.
* Photolog / registro fotográfico de perforaciones.

> La lista anterior representa los módulos y ensayos presentes durante el desarrollo histórico del sistema y no implica que todos continúen siendo funcionales en entornos actuales.

---

## 🔄 Flujo de trabajo

El sistema estaba diseñado alrededor del flujo operativo de un laboratorio:

```text
Registro de muestra
       ↓
Inventario
       ↓
Programación / preparación
       ↓
Asignación de ensayos
       ↓
Ejecución del ensayo
       ↓
Captura de resultados
       ↓
Revisión
       ↓
Aprobación
       ↓
Generación de reportes
       ↓
Entrega de resultados
```

### 1. Registro e inventario

Ingreso y administración de muestras alteradas e inalteradas.

Ejemplos históricos de archivos relacionados:

* `add_Inalteradedsample.php`
* `alteradedSample.php`

### 2. Programación y preparación

Asignación de ensayos y actividades a los técnicos correspondientes.

### 3. Ejecución

Captura de los datos obtenidos durante los ensayos de laboratorio.

### 4. Revisión

El sistema disponía de vistas específicas para revisar y validar los resultados de los diferentes ensayos.

Ejemplo de convención:

```text
Revision-*.php
```

### 5. Entrega

Generación de resultados y documentos PDF para su posterior entrega al cliente.

---

## 📁 Estructura general del proyecto

La estructura histórica incluía, entre otros, los siguientes directorios y archivos:

```text
/
├── css/
├── js/
├── Layouts/
├── db/
├── includes/
├── libs/
├── PDF/
├── uploads/
│
├── add_*.php
├── edit_*.php
├── delete_*.php
├── Revision-*.php
├── Ajax-*.php
├── ajax.php
└── *.php
```

### Directorios principales

| Directorio  | Propósito                                                       |
| ----------- | --------------------------------------------------------------- |
| `css/`      | Hojas de estilo.                                                |
| `js/`       | JavaScript del sistema.                                         |
| `Layouts/`  | Componentes y estructuras visuales.                             |
| `db/`       | Scripts y elementos relacionados con la base de datos.          |
| `includes/` | Archivos reutilizables, conexiones y componentes comunes.       |
| `libs/`     | Librerías y dependencias externas.                              |
| `PDF/`      | Clases, plantillas y lógica relacionada con documentos PDF.     |
| `uploads/`  | Archivos cargados por los usuarios, como imágenes y documentos. |

### Convenciones históricas de archivos

* `add_*.php` → creación de registros.
* `edit_*.php` → edición de registros.
* `delete_*.php` → eliminación de registros.
* `Revision-*.php` → revisión de resultados.
* `Ajax-*.php` / `ajax.php` → endpoints utilizados para operaciones AJAX.
* `*menu.php` → componentes de navegación.

---

## 📜 Reglas de desarrollo originales

Durante el desarrollo activo se utilizaba una estrategia de trabajo basada en ramas independientes para reducir el riesgo de introducir errores directamente en la versión considerada estable.

> "This is the project where the reviewed and tested files will be. To have integrity and that the final application has the fewest errors possible. Each developer has to work on a different Branching to avoid that the final application stops working due to some programming error."

Esta información se conserva únicamente como referencia histórica de la metodología utilizada durante el desarrollo.

---

## 💾 Base de datos

El proyecto utilizaba **MySQL**.

El esquema histórico de la base de datos se conserva en:

`./index_test_lab.sql`

> ⚠️ El archivo SQL debe considerarse una referencia histórica. Antes de utilizarlo en un entorno actual sería necesario revisar compatibilidad, estructura, credenciales, datos incluidos y posibles cambios requeridos.

---

## 📦 Dependencias

Las dependencias PHP del proyecto eran gestionadas mediante **Composer**.

Los archivos y directorios relacionados con dependencias pueden encontrarse dentro de:

```text
libs/
```

y/o en los archivos de configuración de Composer presentes en el repositorio.

> ⚠️ Las dependencias utilizadas por este proyecto pueden encontrarse obsoletas o presentar incompatibilidades y vulnerabilidades conocidas. No se recomienda utilizar este código directamente en producción sin una revisión y actualización de seguridad.

---

## 🔐 Consideraciones de seguridad

Este repositorio corresponde a un proyecto archivado.

Antes de ejecutar el sistema, se recomienda revisar especialmente:

* Credenciales de base de datos.
* Archivos de configuración.
* Variables de entorno.
* Archivos almacenados en `uploads/`.
* Permisos de escritura.
* Dependencias de Composer.
* Consultas SQL.
* Validación y sanitización de entradas.
* Autenticación y autorización.
* Endpoints AJAX.
* Generación y acceso a archivos PDF.
* Exposición de información sensible.

**No deben utilizarse credenciales reales ni datos sensibles históricos para realizar pruebas.**

---

## 🏗️ Instalación histórica

El proyecto fue desarrollado para ejecutarse en un entorno PHP/MySQL compatible con las versiones utilizadas durante su desarrollo.

Para reproducir el entorno histórico sería necesario, como mínimo:

1. Configurar una versión compatible de PHP.
2. Configurar MySQL.
3. Restaurar el esquema mediante `index_test_lab.sql`.
4. Configurar las credenciales de conexión.
5. Instalar las dependencias disponibles mediante Composer.
6. Configurar el servidor web.
7. Revisar permisos de `uploads/`.
8. Verificar la configuración de generación de PDFs.
9. Revisar las rutas y dependencias de archivos antes de ejecutar la aplicación.

> Esta sección describe una posible reproducción histórica y **no constituye una guía de instalación para un entorno de producción moderno**.

---

## ⚠️ Limitaciones

Debido a la antigüedad y al estado archivado del proyecto:

* Algunas funcionalidades pueden no funcionar en versiones modernas de PHP.
* Las dependencias pueden estar desactualizadas.
* Algunas rutas o integraciones pueden depender del entorno original.
* La estructura del código puede no seguir estándares modernos de arquitectura.
* Pueden existir errores conocidos o no documentados.
* No se garantiza compatibilidad con navegadores, servidores o sistemas operativos actuales.

---

## 📌 Información para futuros mantenedores

Si este proyecto vuelve a ser desarrollado en el futuro, se recomienda considerar una **modernización progresiva** antes de reactivarlo.

Entre los aspectos a evaluar:

* Actualización de PHP.
* Actualización de dependencias.
* Migración progresiva hacia una arquitectura más estructurada.
* Separación clara entre lógica, presentación y acceso a datos.
* Centralización de configuración.
* Uso de variables de entorno.
* Mejoras de seguridad.
* Validación y manejo de errores.
* Revisión de consultas SQL.
* Revisión de autenticación y autorización.
* Pruebas automatizadas.
* Documentación de API/endpoints.
* Revisión de los cálculos de los ensayos.
* Migración de módulos antiguos a una arquitectura mantenible.

---

## 📅 Información del archivo

**Proyecto:** LAB-APP-SYSTEM-PHP
**Estado:** Archivado
**Fecha de archivo:** 25 de agosto de 2026
**Mantenimiento activo:** No
**Soporte activo:** No
**Uso recomendado:** Referencia histórica y técnica

---

> **Aviso final**
>
> Este repositorio se conserva como registro histórico del sistema LAB-APP-SYSTEM-PHP. El código se proporciona tal como quedó en el momento de su archivo y no se garantiza su funcionamiento en entornos modernos.
>
> Cualquier reutilización del código debe realizarse después de una revisión técnica y de seguridad adecuada.

---

*Archivado el 25 de agosto de 2026.*
