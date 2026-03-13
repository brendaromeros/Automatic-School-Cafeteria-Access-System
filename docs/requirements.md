Proyecto: Automatic School Cafeteria Access System
Autor: Brenda Romero 

# Requerimientos del Sistema
## 1. Introducción

Este documento describe los requerimientos funcionales y no funcionales del sistema de control de acceso al comedor escolar basado en códigos QR.

El objetivo del sistema es mejorar el flujo de estudiantes durante el horario de almuerzo, evitar abusos del servicio y registrar datos de uso del comedor para análisis futuro.

---

## 2. Problemas Identificados

Durante el horario de almuerzo se han identificado los siguientes problemas operativos:

- Filas largas y desorganizadas.
- Estudiantes que repiten su porción de comida.
- Estudiantes sin beneficio del comedor que logran acceder al servicio.
- Falta de registro confiable de quienes ya utilizaron el servicio.
- Dificultad para controlar el acceso manualmente.
- Ausencia de datos históricos sobre el uso del comedor.

---

## 3. Requerimientos Funcionales

El sistema deberá cumplir con las siguientes funciones.

### 3.1 Identificación mediante QR

El sistema debe permitir identificar estudiantes y profesores mediante un código QR asociado a su credencial.

### 3.2 Verificación de autorización

El sistema debe verificar si la persona está autorizada a utilizar el servicio de comedor.

### 3.3 Control de repetición

El sistema debe evitar que un usuario utilice el servicio más de una vez por día, según las reglas definidas.

### 3.4 Registro de accesos

Cada acceso al comedor debe registrarse con:

- Identificador de la persona
- Fecha
- Hora
- Tipo de usuario (estudiante o profesor)

### 3.5 Detección de acceso sin autorización

El sistema debe detectar cuando una persona intenta ingresar sin escanear su código QR.

### 3.6 Detección de acceso múltiple

El sistema debe detectar situaciones en las que más de una persona intenta ingresar con una sola autorización.

### 3.7 Exportación de datos

El sistema debe permitir exportar los registros para análisis posterior.

---

## 4. Requerimientos No Funcionales

### 4.1 Funcionamiento sin conexión a internet

El sistema debe operar completamente offline.

### 4.2 Rapidez de procesamiento

El tiempo de procesamiento por usuario no debe superar los 2 segundos.

### 4.3 Bajo costo

El sistema debe ser implementado utilizando hardware económico.

### 4.4 Resistencia ambiental

El sistema debe tolerar condiciones de alta temperatura y humedad.

### 4.5 Facilidad de uso

La interfaz debe ser simple para personal no técnico.

---

## 5. Requerimientos de Datos

Los registros generados por el sistema deberán poder exportarse para:

- Análisis de uso del comedor
- Generación de reportes
- Desarrollo futuro de modelos de predicción de demanda de alimentos