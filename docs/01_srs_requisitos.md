# 1. Especificación de Requisitos de Software (SRS Ligera)

## 1.1. Requisitos Funcionales
*   **RF1:** El sistema debe permitir registrar nuevos usuarios en la base de datos (Nombre, Email, Password).
*   **RF2:** El sistema debe permitir crear un pedido asociado a un usuario existente (Descripción, Total).
*   **RF3:** El sistema debe permitir consultar la lista de todos los pedidos registrados en el sistema.

## 1.2. Requisitos No Funcionales
*   **RNF1:** La API debe estar construida utilizando el framework Spring Boot con Java 17.
*   **RNF2:** La persistencia de los datos debe realizarse en una base de datos relacional MySQL (gestionada mediante XAMPP).

---

## 1.3. Historias de Usuario y Criterios de Aceptación (Gherkin)

### Historia de Usuario 1: Registro de Usuario
**Como** administrador del sistema,
**Quiero** registrar un nuevo usuario en la base de datos,
**Para** que pueda realizar compras y tener un historial de pedidos.

**Criterios de Aceptación (BDD):**
*   **Escenario 1: Registro exitoso**
    *   **Dado** que el administrador ingresa los datos del usuario (nombre, email y contraseña) en la API.
    *   **Cuando** envía una petición POST a `/api/usuarios` con los datos correctos.
    *   **Entonces** el sistema guarda el usuario en la base de datos y retorna un código HTTP 200 con el ID del usuario generado.

### Historia de Usuario 2: Creación de Pedido
**Como** cliente registrado,
**Quiero** crear un pedido especificando el artículo y el costo,
**Para** que el sistema registre mi compra.

**Criterios de Aceptación (BDD):**
*   **Escenario 1: Creación exitosa de pedido**
    *   **Dado** que el cliente tiene un ID de usuario válido registrado en el sistema.
    *   **Cuando** envía una petición POST a `/api/pedidos` incluyendo el `usuario_id`, `descripcion` y `total` en el cuerpo de la petición.
    *   **Entonces** el sistema asocia el pedido al usuario y retorna un código HTTP 200 con los detalles del pedido creado.