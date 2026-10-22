# 2. Manual Técnico y Documentación de la API

## 2.1. Diccionario de Datos

### Tabla: `usuarios`
| Campo | Tipo de Dato | Restricciones | Descripción |
| :--- | :--- | :--- | :--- |
| `id` | BIGINT | PRIMARY KEY, AUTO_INCREMENT | Identificador único del usuario. |
| `nombre` | VARCHAR(100) | NOT NULL | Nombre completo del usuario. |
| `email` | VARCHAR(150) | NOT NULL, UNIQUE | Correo electrónico de contacto. |
| `password` | VARCHAR(255) | NOT NULL | Contraseña de acceso. |

### Tabla: `pedidos`
| Campo | Tipo de Dato | Restricciones | Descripción |
| :--- | :--- | :--- | :--- |
| `id` | BIGINT | PRIMARY KEY, AUTO_INCREMENT | Identificador único del pedido. |
| `usuario_id` | BIGINT | FOREIGN KEY, NOT NULL | ID del usuario que realizó el pedido. |
| `descripcion` | VARCHAR(255) | NOT NULL | Detalle del producto o servicio comprado. |
| `total` | DECIMAL(10,2) | NOT NULL | Monto total del pedido. |
| `fecha_creacion`| TIMESTAMP | DEFAULT CURRENT_TIMESTAMP| Fecha y hora del registro. |

---

## 2.2. Documentación de Endpoints REST

### 1. Endpoint: Crear Usuario
*   **Método:** `POST`
*   **Ruta:** `/api/usuarios`
*   **Payload JSON de entrada:**
    ```json
    {
        "nombre": "Daniela Salguero",
        "email": "estudiante@test.com",
        "password": "123456"
    }