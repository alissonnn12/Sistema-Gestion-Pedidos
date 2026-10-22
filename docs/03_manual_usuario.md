
# 3. Manual de Usuario Final

Bienvenido al sistema de gestión de pedidos. Esta guía te explicará cómo registrar tus compras en el sistema de forma sencilla.

## 3.1. Guía paso a paso: Registrar un nuevo pedido

Para registrar una compra, utilizaremos la interfaz de pruebas **Postman** (o cualquier herramienta similar) donde el sistema recibe los pedidos.

1. Abre la aplicación Postman.
2. En la barra superior, asegúrate de que el método seleccionado sea **POST**.
3. En el campo de la URL, escribe la dirección de nuestro sistema: `http://localhost:8080/api/pedidos`.
4. Haz clic en la pestaña **Body** (justo debajo de la URL).
5. Selecciona la opción **raw** y asegúrate de que el formato sea **JSON**.
6. En el cuadro de texto grande, copia y pega la siguiente plantilla para tu pedido:
   ```json
   {
       "usuario_id": 1,
       "descripcion": "Nombre de tu producto aquí",
       "total": 1500.50
   }