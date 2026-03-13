Proyecto: Automatic School Cafeteria Access System
Autor: Brenda Romero 

# Diseño del Sistema

## 1. Descripción General

El sistema de control de acceso al comedor escolar está diseñado como una arquitectura modular que permite identificar usuarios mediante códigos QR, verificar su autorización y registrar su acceso.

El sistema está diseñado para funcionar sin conexión a internet y utilizando hardware de bajo costo.

---

## 2. Arquitectura del Sistema

El sistema está dividido en los siguientes módulos principales:

### 2.1 Módulo de Lectura de QR

Responsable de capturar imágenes mediante una cámara y detectar códigos QR.

Funciones:

- Capturar imagen
- Detectar código QR
- Extraer identificador del usuario

---

### 2.2 Módulo de Verificación

Este módulo consulta la base de datos para verificar:

- Existencia del usuario
- Tipo de usuario
- Autorización de acceso
- Uso previo del servicio en el día actual

---

### 2.3 Módulo de Registro

Encargado de registrar cada acceso autorizado al comedor.

Datos registrados:

- ID de usuario
- Fecha
- Hora
- Tipo de usuario

---

### 2.4 Módulo de Seguridad

Supervisa sensores de acceso para detectar intentos de ingreso sin autorización.

Funciones:

- Monitoreo de sensores
- Detección de interrupción de barrera
- Activación de alertas

---

### 2.5 Módulo de Interfaz

Muestra información al operador del comedor.

Ejemplos de mensajes:

- Acceso permitido
- Usuario no autorizado
- Servicio ya utilizado

---

### 2.6 Módulo de Exportación de Datos

Permite exportar registros en formatos compatibles con herramientas de análisis de datos.

---

## 3. Estructura de Base de Datos

### Tabla: roles

Define los tipos de usuario del sistema.

| Campo | Descripción |
|------|-------------|
| id_rol | Identificador del rol |
| nombre_rol | Tipo de usuario (estudiante, profesor, administrador) |

---

### Tabla: personas

Almacena información de los usuarios que pueden interactuar con el sistema.

| Campo | Descripción |
|------|-------------|
| id_persona | Identificador único |
| nombre | Nombre del usuario |
| id_rol | Rol asociado |
| qr_id | Código QR del carnet |
| autorizado | Indica si puede acceder al comedor |

---

### Tabla: registros_comedor

Registra cada acceso autorizado al comedor.

| Campo | Descripción |
|------|-------------|
| id_registro | Identificador del registro |
| id_persona | Usuario que accede |
| fecha | Fecha del acceso |
| hora | Hora del acceso |

---

### Tabla: eventos_seguridad

Registra incidentes detectados por el sistema de seguridad.

| Campo | Descripción |
|------|-------------|
| id_evento | Identificador del evento |
| tipo_evento | Tipo de incidente |
| descripcion | Detalles del evento |
| fecha | Fecha del evento |
| hora | Hora del evento |