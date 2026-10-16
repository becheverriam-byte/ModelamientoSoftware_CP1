# ModelamientoSoftware_CP1

## Datos del estudiante
- **Nombre:** Echeverria Mora Bryan Jordano
- **Carrera:** Ingeniería de Software
- **Asignatura:** Modelamiento de Software
- **Docente:** MSC. Guevara Serrano Jorge Dumar
- **Período:** Abril 2024 – Agosto 2025
- **Fecha de entrega:** Jueves, 15 de octubre de 2026

## Caso de estudio
**TravelNow** – Plataforma de reservas y check-in de una cadena hotelera.

TravelNow es una cadena hotelera que requiere una plataforma para que los huéspedes reserven alojamiento y gestionen su estadía antes de llegar. El cliente consulta disponibilidad, selecciona una alternativa, realiza su reserva, paga electrónicamente mediante una pasarela externa y recibe una notificación por correo. Antes de la estadía puede modificar o cancelar la reserva (bajo condiciones), hacer pre check-in y solicitar servicios adicionales. Los empleados consultan y actualizan reservas, y el supervisor autoriza modificaciones excepcionales.

## Descripción breve del sistema
El sistema permite:
- Consultar disponibilidad por ciudad y fechas.
- Realizar reservas con registro de datos del cliente, comprobación de disponibilidad y cálculo del valor total.
- Procesar pagos electrónicos mediante pasarela externa.
- Enviar notificaciones de confirmación por correo electrónico.
- Modificar y cancelar reservas dentro de las condiciones definidas.
- Realizar pre check-in e incorporar servicios adicionales.
- Consultar y actualizar el estado de reservas (empleados).
- Autorizar modificaciones excepcionales (supervisor).

## Actores identificados
| Actor | Tipo | Justificación |
|-------|------|---------------|
| Cliente | Primario | Consulta, reserva, paga, modifica/cancela y hace pre check-in |
| Empleado | Primario | Consulta reservas y actualiza su estado |
| Supervisor | Primario | Funciones del empleado + autoriza modificaciones excepcionales |
| Pasarela de Pagos | Secundario (externo) | Procesa el pago electrónico |
| Servicio de Correo Electrónico | Secundario (externo) | Envía notificación de confirmación |

## Diagramas UML incluidos

### TPE1 – Diagramas de casos de uso y de interacción

| Diagrama | Archivo editable | Archivo exportado |
|----------|------------------|-------------------|
| Diagrama de casos de uso | `TPE1/editables/casos_de_uso.*` | `TPE1/exportados/casos_de_uso.png` |
| Diagrama de comunicación – CU-02 Realizar reserva | `TPE1/editables/comunicacion_CU02.*` | `TPE1/exportados/comunicacion_CU02.png` |
| Diagrama de secuencia – CU-02 Realizar reserva | `TPE1/editables/secuencia_CU02.*` | `TPE1/exportados/secuencia_CU02.png` |

**Casos de uso identificados (14):**
- CU-01 Consultar disponibilidad (Cliente)
- CU-02 Realizar reserva (Cliente)
- CU-03 Registrar datos del cliente (incluido en CU-02)
- CU-04 Comprobar disponibilidad (incluido en CU-02)
- CU-05 Calcular valor total (incluido en CU-02)
- CU-06 Procesar pago electrónico (Pasarela de Pagos, incluido en CU-02)
- CU-07 Enviar notificación de confirmación (Servicio de Correo, incluido en CU-02)
- CU-08 Modificar reserva (Cliente)
- CU-09 Cancelar reserva (Cliente)
- CU-10 Realizar pre check-in (Cliente)
- CU-11 Solicitar servicios adicionales (extiende CU-10)
- CU-12 Consultar reservas (Empleado)
- CU-13 Actualizar estado de reserva (Empleado)
- CU-14 Autorizar modificación excepcional (Supervisor, extiende CU-08)

**Relaciones clave:**
- «include» de Realizar reserva hacia Procesar pago electrónico.
- «extend» de Solicitar servicios adicionales hacia Realizar pre check-in.
- Generalización de Supervisor hacia Empleado.
