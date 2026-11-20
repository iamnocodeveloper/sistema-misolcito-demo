# sistema-misolcito-demo

Demo navegable del **sistema de gestión** de Mi Solcito, Jardín Maternal (Mendoza 435 Norte, San Juan, Argentina).

Es el complemento de la web pública: la web presenta el jardín y recibe consultas; este panel es lo que la dirección y las docentes usan todos los días.

## Qué incluye

Aplicación de una sola página (`index.html`, CSS y JS inline, sin backend ni dependencias externas salvo Google Fonts):

- **Entrada simulada**: usuario demo precargado y botón «Entrar en modo demostración» (sin autenticación real).
- **Escritorio**: resumen del día (niños presentes, salas activas, cuotas por cobrar, avisos por enviar, próxima visita de familias), avisos del jardín (inscripciones sin confirmar, cuotas vencidas, vacunas por vencer, comunicado sin enviar), próximas visitas, ocupación por sala, cuotas del mes y asistencia de la semana.
- **Inscripciones**: bandeja de pre-inscripciones con estados (pendiente, entrevista agendada, inscripto, lista de espera), alta real de una inscripción desde el formulario —la sala se sugiere por la fecha de nacimiento y se controla el cupo—, y cupos por sala con vacantes y lista de espera cuando la sala se completa.
- **Salas y niños**: nómina de 60 niños en 4 salas con buscador y ficha completa: datos, grupo sanguíneo, alergias, personas autorizadas a retirarlo, quién lo trae y quién lo busca, historial de asistencias de las últimas 4 semanas, cuota del mes y notas de evolución (se pueden agregar).
- **Asistencias**: planilla del día por sala con presente / ausente / retirado antes, totales y el porcentaje de asistencia del mes por niño y por sala.
- **Cuotas**: cobros por mes y por familia con monto, medio (efectivo, transferencia, tarjeta) y estado (pagada, pendiente, vencida); totales del mes arriba y recordatorios de pago con vista previa del mensaje.
- **Comunicados**: envío de avisos a todas las familias o a una sala, con historial de lo enviado y confirmaciones de lectura.
- **Informes**: niños por sala, asistencia por mes, cuotas cobradas vs. pendientes (dona y barras apiladas) e inscripciones por mes. Todo con SVG y CSS, sin librerías.
- **Ajustes**: catálogo de salas (edad, cupo y arancel editable en memoria), horarios de atención, configuración de recordatorios de cuota y datos del jardín.
- Menú de usuario con acceso a la web pública del jardín y pie con la nota de demo.

Los datos son de ejemplo y se generan en el navegador, relativos a la fecha en que se abre el demo: 60 niños, 45 familias, 135 cuotas de 3 meses, asistencias de las últimas 4 semanas, 12 pre-inscripciones y 8 comunicados enviados. Montos en pesos argentinos.

## Despliegue

`Dockerfile` de dos líneas (`nginx:alpine` + copia de los archivos) publicado desde este repositorio en EasyPanel:

- Sistema: https://clientes-sistema-misolcito.rddxeh.easypanel.host/
- Web pública del jardín: https://clientes-demo-misolcito.rddxeh.easypanel.host/

## Nota

Demo de referencia hecho por Nocodeveloper. No envía mensajes, no cobra nada, no guarda datos y no incluye información real de terceros; en el sistema real se cargan los datos del jardín.