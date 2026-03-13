
Proyecto: Smart Cafeteria Access System  
Autor: Brenda Romero

# Flujo del Sistema

## Flujo de Operación

El siguiente diagrama describe el proceso desde que un usuario escanea su código QR hasta la autorización o denegación de acceso.

```mermaid
flowchart TD

A[Inicio] --> B[Esperar lectura de QR]

B --> C[Leer codigo QR]

C --> D[Buscar usuario en base de datos]

D --> E{Usuario existe}

E -->|No| F[Mostrar usuario no registrado]

E -->|Si| G{Usuario autorizado}

G -->|No| H[Mostrar acceso denegado]

G -->|Si| I{Ya utilizo el servicio}

I -->|Si| J[Mostrar servicio ya utilizado]

I -->|No| K[Registrar acceso]

K --> L[Permitir acceso]

L --> B
```