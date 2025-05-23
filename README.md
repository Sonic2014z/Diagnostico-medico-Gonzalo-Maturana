# Diagnostico-medico-Gonzalo-Maturana
Desarrollo del ejercicio tipo prueba realizado el dia 23 de mayo de 2025.
# Diagnostico médico Gonzalo Maturana

> Nombre: Gonzalo Christian Andre Maturana Cruces |
> Sección: 1 (14:56 - 16:25)

## Desarrollo:

### 1. Corrección de Casos de Uso:

- Palabras `<<include>>` y `<<extend>>` faltantes, para una mejor lectura del caso de uso.
- No se utilizan los indicadores correctos para las relaciones dentro del caso de uso, en vez de eso, se utilizan relaciones de un diagrama de clases.
- La relación dirigida hacia "Agregar motivo de cancelación" debería ser un `<<extend>>`, ya que el motivo de la cancelación debe ser opcional.
- "Rechazar reserva" y "Aprobar reserva" deberían estar relacionados con un `<<include>>`, ya que se le debe notificar obligatoriamente al estudiante por cualquier cambio realizado a la reserva.
- "Ver historial de otras personas" no debería de existir dentro del caso de uso, ya que solo debería ser posible ver el historial del propio usuario, no de los demás.
- Al "Reservar sala" debería ser obligatorio consultar la disponibilidad de las salas, por ende, debería ir un `<<include>>`.
- No debería existir "Eliminar historial de reservas", ya que debería llevarse un registro que no se debe eliminar sobre las reservas del estudiante.

### 2. Corrección del Diagrama de Clases:

- La clase `Reserva` no tiene relación alguna dentro del diagrama.
- No se especifican bien las implementaciones, usos y relaciones.
- La clase `SistemaReserva` debería de usar la clase `Reserva`, ya que en teoría es un sistema que gestiona las reservas.
- Tanto `Usuario` como `Administrador` deberían de utilizar el `SistemaReservas`, para evitar que el usuario este relacionado con más de una clase que hace lo mismo.
- Cada función relacionada a la clase `Sala` debería tener dentro de los parametros utilizar la clase anteriormente mencionada.
- `Administrador` no posee atributos cuando debería poseer al menos uno, como por ejemplo, el nombre.
- `NotificadorCorreo` y `NotificadorSMS` no tienen atributos, como por ejemplo, el mensaje que debería entregar.
- No existen getters y setters dentro de `Reserva`.
- `GestorNotificaciones` debería ser una interfaz, la cual es implementada en cada notificador dentro del diagrama de clases.

### 3. Corrección del Diagrama de Implementación:

- Las especificaciones de los patrones deben estar en nodos fuera de los paquetes del diagrama de implementación, no dentro de los paquetes en cada uno de los nodos.
- Dentro de los paquetes, no tienen que estar todos los nodos relacionados entre sí con indicadores como las flechas que aparecen en el diagrama actual.
- Los nombres de los nodos no coinciden con los nombres vistos en el diagrama de clases, deberia ser `GestorNotificaciones` en vez de `Gestor de Notificaciones`.
- Se debe especificar el tipo de objeto dentro de los nodos aparte del nombre, como por ejemplo, `GestorNotificaciones <<Adapter>>`.

