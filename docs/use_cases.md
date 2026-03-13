Proyecto: Automatic School Cafeteria Access System
Autor: Brenda Romero 

# Casos de Uso del Sistema

Este documento describe los principales escenarios de uso del sistema de control de acceso al comedor.

---

## Caso de Uso 1: Estudiante autorizado

1. El estudiante presenta su carnet frente a la cámara.
2. El sistema lee el código QR.
3. El sistema verifica que el estudiante está autorizado.
4. El sistema confirma que no ha utilizado el servicio ese día.
5. El sistema muestra un mensaje de acceso permitido.
6. El acceso queda registrado en la base de datos.

---

## Caso de Uso 2: Estudiante que ya utilizó el servicio

1. El estudiante intenta acceder nuevamente.
2. El sistema detecta que ya existe un registro de acceso para ese día.
3. El sistema muestra un mensaje indicando que el servicio ya fue utilizado.

---

## Caso de Uso 3: Estudiante no autorizado

1. El estudiante presenta su carnet.
2. El sistema consulta la base de datos.
3. El sistema detecta que el estudiante no posee el beneficio del comedor.
4. El sistema muestra un mensaje de acceso denegado.

---

## Caso de Uso 4: Acceso sin escaneo de QR

1. Una persona intenta ingresar sin escanear su código QR.
2. El sensor de acceso detecta el movimiento.
3. El sistema verifica que no existe una autorización activa.
4. Se activa una alarma y se registra el evento (En consideración)

---

## Caso de Uso 5: Acceso múltiple con una sola autorización

1. Un estudiante escanea su código QR.
2. Dos personas intentan cruzar la entrada.
3. El sensor detecta múltiples interrupciones.
4. El sistema detecta inconsistencia entre autorizaciones y accesos.
5. Se genera una alerta.

---

## Caso de Uso 6: Acceso de profesor

1. El profesor presenta su credencial con código QR.
2. El sistema identifica que se trata de un usuario tipo profesor.
3. El sistema verifica su autorización.
4. El acceso queda registrado en la base de datos.