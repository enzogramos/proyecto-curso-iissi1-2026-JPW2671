# FitUS

## Miembros del grupo L8-AM-G1

1. Letrán Rodríguez, Julio
2. Baya Rodríguez, Mario
3. Ramos Andrés, Enzo

## 1. Introducción al problema

El gimnasio "FitUS" ha experimentado un crecimiento notable de clientes durante los últimos meses y ha decidido ampliar sus servicios. En estos momentos, la gestión de las inscripciones, el control de aforo de las clases dirigidas (como Aeróbic o Zumba) y la gestión de cobros y suscripciones se realiza mediante hojas de cálculo y documentos físicos que dificultan la organización.

### Situación actual y problemas:
La gestión manual del gimnasio está provocando una serie de problemas críticos en el día a día:
 - Sobrecarga en clases dirigidas: El aforo en las clases más populares se suele superar ya que los clientes no pueden reservar con antelación y entran por orden de llegada, generando quejas y problemas de espacio.

 - Descontrol en los planes de suscripción y ventajas: El gimnasio ofrece un plan "Básico" (acceso al gimnasio y a 2 clases a la semana) y un plan "Ultimate" (acceso ilimitado a todas las instalaciones). Recientemente se ha instalado una máquina dispensadora de bebidas isotónicas y se ha abierto una pequeña tienda de suplementación deportiva. La recepción está teniendo problemas para verificar qué clientes tienen el plan Ultimate para permitirles usar la máquina de bebidas sin coste o para aplicarles los descuentos exclusivos en la tienda, lo que ralentiza el servicio y provoca pérdidas económicas.

 - Conflictos con los Entrenadores Personales: Además de los monitores de clases grupales, el gimnasio ha incorporado entrenadores personales como un servicio añadido. Estas sesiones privadas no están incluidas en las cuotas habituales (Básico o Ultimate), sino que se abonan aparte. Actualmente, la gestión de estas agendas se realiza en papel, lo que está provocando dos problemas graves: por un lado, continuos solapamientos en los horarios de las citas; y por otro, una falta de control en la facturación, impartiéndose a menudo sesiones sin haber comprobado previamente si el cliente ha pagado por este servicio extra.

### Expectativas del sistema:
Se requiere el desarrollo de un sistema de información que permita digitalizar toda la gestión del club. El sistema debe permitir a los socios gestionar su plan (Básico o Ultimate) y realizar reservas tanto para clases dirigidas como para sesiones con entrenadores personales. Además, el software deberá integrar un módulo de punto de venta (TPV) para la tienda que aplique descuentos automáticamente según el plan del usuario, y gestionar de forma automatizada los permisos de acceso a las ventajas premium, como la máquina de bebidas.

<img width="1022" height="569" alt="imagen" src="https://github.com/user-attachments/assets/7fdbc06e-2f83-4790-a5da-d80a81777982" />

## 2. Glosario de términos
 - Aforo: Número máximo de personas permitidas en una instalación o en una clase dirigida específica.

 - Clase Dirigida: Actividad deportiva impartida por un monitor en un horario específico (ej. Aeróbic, Zumba) a la que los socios pueden asistir reservando previamente.

 - Monitor: Empleado del gimnasio encargado de impartir las clases dirigidas.

 - Plan Básico: Modalidad de suscripción básica que permite el uso de las instalaciones y un número limitado de 2 reservas en clases dirigidas a la semana.

 - Plan Ultimate: Modalidad de suscripción premium que permite el acceso ilimitado a las instalaciones y reservas ilimitadas en las clases, así como a la máquina de bebidas. Cuenta también con descuentos en la tienda.

 - Socio (o Cliente): Usuario registrado en el gimnasio que abona una cuota periódica mediante un plan de suscripción.
   
 - Entrenador Personal: Profesional del gimnasio que ofrece sesiones individuales y personalizadas a los socios, fuera del horario de las clases grupales.

 - Máquina de Bebidas: Dispensador automático de bebidas isotónicas cuyo uso gratuito está restringido a los socios con suscripción Ultimate.

 - TPV (Terminal de Punto de Venta): Módulo del sistema informático utilizado en la recepción para registrar las ventas de los productos de la tienda.

 - Tienda: Espacio físico en el gimnasio donde se venden productos como suplementación deportiva o accesorios.

## 3. Visión general del sistema

### 3.1. Requisitos generales

#### R.G.01. Gestión de socios, planes de suscripción y control de acceso

Como Administrador
quiero gestionar el alta de los socios, su modalidad de suscripción (Básico o Ultimate), el estado de sus cobros periódicos y su acceso mediante código QR
para digitalizar el control de miembros y asegurar que solo accedan a las instalaciones los usuarios activos y al corriente de pago.

#### R.G.02. Gestión del catálogo y reservas de clases dirigidas

Como Socio
quiero consultar la oferta de clases dirigidas y reservar plaza con antelación respetando el aforo de cada sala y las condiciones de mi plan
para asegurar mi asistencia a las actividades grupales evitando aglomeraciones.

#### R.G.03. Gestión de entrenadores personales y bonos de sesiones extra

Como Socio
quiero adquirir bonos de sesiones adicionales fuera de cuota y reservar citas individuales en la agenda de los entrenadores personales
para recibir entrenamientos personalizados sin solapamientos horarios y con un control exacto de mi saldo de sesiones pagadas.

#### R.G.04. Gestión de ventas en tienda (TPV) y ventajas del Plan Ultimate

Como Administrador
quiero registrar las ventas de productos en el TPV aplicando descuentos automáticos según el plan del socio y controlar el acceso automatizado a la máquina de bebidas isotónicas
para agilizar la atención en recepción, mantener actualizado el inventario y garantizar el uso exclusivo de los beneficios premium.


### 3.2. Usuarios del sistema

 - Socio: Interactúa con el sistema para ver el horario, reservar clases y gestionar su suscripción.

 - Monitor: Utiliza el sistema para consultar su calendario de clases asignadas y pasar lista de los asistentes.

 - Entrenador Personal: Utiliza el sistema para gestionar su disponibilidad, aceptar o rechazar reservas de sesiones individuales y consultar el historial de los socios a los que entrena.

 - Administrador: Encargado de dar de alta nuevas clases, gestionar monitores y supervisar el estado de los pagos y suscripciones.


## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Consulta de recaudación total en tienda por categoría de producto

Como Administrador
quiero consultar la suma total de ingresos generados en las ventas de la tienda agrupada por categoría de producto
para analizar qué líneas de suplementación y accesorios aportan mayor facturación al gimnasio.

#### R.F.02. Consulta del número total de socios por plan de suscripción

Como Administrador
quiero conocer el número total de socios registrados agrupados por su modalidad de plan de suscripción, Básico o Ultimate
para evaluar la distribución de la cartera de clientes entre los distintos planes ofertados.

#### R.F.03. Consulta de asistencia media por actividad en clases dirigidas

Como Administrador
quiero consultar el promedio de socios asistentes agrupado por cada tipo de actividad o clase dirigida
para identificar qué disciplinas tienen mayor demanda media y optimizar la planificación de horarios.

#### R.F.04. Consulta de precios mínimo y máximo de productos por categoría

Como Socio
quiero consultar el precio más bajo y el precio más alto de los artículos disponibles en la tienda agrupados por categoría
para conocer el rango de precios de los suplementos y accesorios antes de acudir a recepción.

#### R.F.05. Consulta del total de sesiones impartidas por cada entrenador personal

Como Administrador
quiero consultar la cantidad total de sesiones individuales realizadas agrupadas por cada entrenador personal
para supervisar la carga de trabajo y la productividad del equipo de entrenadores.

#### R.F.06. Consulta del gasto total y gasto medio en tienda por socio

Como Administrador
quiero obtener el importe total acumulado y el gasto medio por compra agrupado por cada socio
para identificar a los clientes con mayor volumen de compras en la tienda y evaluar el impacto de los descuentos aplicados.

#### R.F.07. Consulta de consumo total de bebidas isotónicas por socio

Como Administrador
quiero consultar el número total de dispensaciones realizadas y el volumen total en mililitros consumido en la máquina de bebidas agrupado por cada socio con Plan Ultimate
para monitorizar el uso del dispensador automático y planificar la reposición de bebidas.

#### R.F.08. Consulta de capacidad mínima y máxima de las salas por tipo de actividad

Como Monitor
quiero consultar el aforo mínimo y el aforo máximo de las salas asignadas agrupadas por cada modalidad de clase dirigida
para conocer los límites de capacidad de los espacios donde se imparte cada disciplina deportiva.

#### R.F.09. Consulta de facturación y cantidad de bonos vendidos por modalidad

Como Administrador
quiero consultar el número total de bonos adquiridos y el importe total recaudado agrupado por cada tipo de bono de entrenamiento personal
para llevar el control contable de los servicios contratados fuera de la cuota mensual.

#### R.F.10. Consulta de duración media, mínima y máxima de sesiones por entrenador

Como Entrenador Personal
quiero consultar la duración media , mínima y máxima en minutos de las sesiones privadas impartidas agrupadas por cada socio entrenado
para analizar la dedicación temporal y realizar un seguimiento de los entrenamientos personalizados.

#### 4.1.1. Requisitos de información

##### R.I.01. Información de socios y planes de suscripción

Como Administrador
quiero almacenar en la base de datos la información personal de cada socio (DNI, nombre, apellidos, fecha de nacimiento, email, teléfono, estado del socio y saldo disponible de sesiones de entrenamiento personal) junto con los detalles de su suscripción (identificador de suscripción, tipo de plan Básico o Ultimate, cuota mensual, fecha de alta, fecha de próxima renovación y estado de pago)
para gestionar de forma persistente los miembros del club y sus permisos.

##### R.I.02. Información de salas, clases dirigidas y reservas grupales

Como Administrador
quiero registrar en la base de datos las salas del gimnasio (identificador de sala, nombre y aforo máximo), las clases dirigidas programadas (identificador de clase, actividad, fecha, hora de inicio, duración, sala asignada y monitor responsable) y las reservas efectuadas (identificador de reserva, socio, clase dirigida, fecha de reserva y confirmación de asistencia)
para controlar la ocupación de las instalaciones y el historial de reservas grupales.

##### R.I.03. Información de personal deportivo (Monitores y Entrenadores Personales)

Como Administrador
quiero almacenar los datos de los empleados deportivos del centro (DNI, nombre completo, email, teléfono, especialidad y tipo de empleado: Monitor o Entrenador Personal)
para asignar responsables a las clases colectivas y gestionar las agendas de entrenamiento individual.

##### R.I.04. Información de bonos y sesiones de entrenamiento personal

Como Entrenador Personal
quiero que la base de datos registre las compras de bonos de entrenamiento (identificador de compra, socio, tipo de bono, número de sesiones incluidas, precio pagado y fecha de adquisición) y las sesiones individuales agendadas (identificador de sesión, entrenador personal, socio, fecha, hora de inicio, duración en minutos y estado de la cita)
para vincular cada cita reservada con el saldo de sesiones pagadas por el socio.

##### R.I.05. Información del catálogo de productos y ventas en tienda (TPV)

Como Administrador
quiero almacenar en la base de datos el inventario de productos de la tienda (código de producto, nombre, categoría, precio unitario y unidades en stock) y las ventas realizadas en el TPV (identificador de venta, fecha y hora, socio comprador, producto vendido, cantidad, porcentaje de descuento aplicado e importe total cobrado)
para mantener actualizado el stock y auditar todas las transacciones comerciales.

##### R.I.06. Información de dispensación de bebidas isotónicas y registros de acceso

Como Administrador
quiero registrar en la base de datos cada uso de la máquina de bebidas (identificador de dispensación, socio, tipo de bebida, volumen en mililitros y fecha/hora exacta) y los accesos por el torno de entrada (identificador de acceso, socio, código QR empleado, fecha/hora y estado de validación)
para auditar el cumplimiento de los tiempos de uso en servicios exclusivos y la seguridad de entrada al recinto.

#### 4.1.2. Reglas de negocio

##### R.N.01. Límite de reservas semanales por tipo de suscripción

Un socio con "Plan Básico" solo puede tener activas un máximo de 2 reservas a clases dirigidas por semana natural. Un socio con "Plan Ultimate" no tiene límite de reservas semanales, sujeto únicamente a la disponibilidad de aforo de la clase. Mediante un *trigger*, el sistema verificará el número de reservas semanales del socio antes de insertar una nueva reserva grupal.

**Prueba de aceptación**
- Comprobar que un socio con "Plan Básico" puede insertar correctamente hasta 2 reservas de clases dirigidas dentro de la misma semana natural.
- Comprobar que el *trigger* bloquea la inserción y lanza un error si un socio con "Plan Básico" intenta registrar una tercera reserva en esa misma semana.
- Comprobar que un socio con "Plan Ultimate" puede registrar más de 2 reservas en la misma semana sin que el *trigger* rechace la operación.

##### R.N.02. Control estricto de aforo máximo en clases dirigidas

Bajo ninguna circunstancia el sistema permitirá que el número de reservas activas para una clase dirigida supere el aforo máximo establecido para la sala física donde se imparte dicha actividad. Un *trigger* comprobará antes de cada inserción de reserva que el total de inscritos no iguale ni supere el aforo de la sala asignada.

**Prueba de aceptación**
- Comprobar que el sistema permite insertar la reserva de un socio cuando el número de reservas activas de la clase es inferior al aforo máximo de la sala.
- Comprobar que el *trigger* aborta la inserción y muestra un mensaje de error cuando el número de plazas reservadas ya ha alcanzado el aforo máximo de la sala.

##### R.N.03. Restricción y frecuencia de dispensación en máquina de bebidas

El acceso a la máquina de bebidas gratuitas está restringido exclusivamente a los socios con "Plan Ultimate" activo y al corriente de pago. Además, para evitar abusos, un mismo socio solo puede dispensar una bebida cada 45 minutos. Un *trigger* validará el plan del socio y el tiempo transcurrido desde su última dispensación antes de insertar un nuevo registro de consumo.

**Prueba de aceptación**
- Comprobar que el *trigger* impide registrar una dispensación si el socio pertenece al "Plan Básico" o tiene recibos impagados.
- Comprobar que el *trigger* bloquea el registro de una nueva dispensación para un socio con "Plan Ultimate" si han transcurrido menos de 45 minutos desde su consumo anterior.
- Comprobar que la dispensación se inserta correctamente cuando el socio tiene "Plan Ultimate" activo y han pasado al menos 45 minutos desde su última bebida.

##### R.N.04. Descuento automático en tienda por fidelidad y actualización de stock

El sistema verificará que exista stock suficiente antes de registrar una venta en tienda, aplicará de forma automática y obligatoria un 15% de descuento sobre el precio de venta al público si el comprador tiene una suscripción "Plan Ultimate" activa y al corriente de pago en el momento de la compra, y descontará del inventario las unidades vendidas mediante un *trigger*.

**Prueba de aceptación**
- Comprobar que el *trigger* impide registrar la venta si la cantidad solicitada supera el stock actual del producto.
- Comprobar que al insertar una venta asociada a un socio con "Plan Ultimate" activo se calcula automáticamente el importe aplicando el 15% de descuento y se reduce el stock del producto en la cantidad vendida.
- Comprobar que al insertar una venta para un socio con "Plan Básico" se cobra el precio estándar sin descuento y se descuenta igualmente el stock.

##### R.N.05. Saldo positivo y no solapamiento en reservas con Entrenador Personal

El sistema denegará mediante un *trigger* cualquier intento de reserva de una sesión con un Entrenador Personal si el socio no dispone de al menos una (1) sesión extra pagada y no consumida en su saldo, o si el entrenador personal ya tiene otra sesión reservada en esa misma fecha y franja horaria. Al confirmarse la inserción de la reserva, el *trigger* descontará automáticamente 1 sesión del saldo del socio.

**Prueba de aceptación**
- Comprobar que el *trigger* rechaza la inserción de la cita si el saldo de sesiones de entrenamiento personal del socio es igual a 0.
- Comprobar que el *trigger* rechaza la reserva si el entrenador personal ya tiene asignada otra sesión que se solapa en fecha y hora.
- Comprobar que, existiendo saldo positivo y disponibilidad horaria, la sesión se registra y el saldo de sesiones del socio disminuye automáticamente en 1 unidad.


### 4.2. Mapa de historias de usuario (opcional)

A continuación, se detallan los requisitos de información y funcionales asociados a cada una de las fases (requisitos generales) del sistema:

| R.G.01. Gestión de socios, planes y accesos | R.G.02. Gestión del catálogo y reservas de clases | R.G.03. Gestión de entrenadores y bonos extra | R.G.04. Gestión de ventas y ventajas Ultimate |
| :--- | :--- | :--- | :--- |
| **R.I.01.** Información de socios y planes | **R.I.02.** Información de salas, clases y reservas | **R.I.03.** Información de personal deportivo | **R.I.05.** Información de productos y ventas |
| **R.I.06.** Información de accesos en torno | **R.F.03.** Asistencia media por clase | **R.I.04.** Información de bonos y sesiones | **R.I.06.** Información de dispensación de bebidas |
| **R.F.02.** Total de socios por plan | **R.F.08.** Capacidad mín/máx de salas | **R.F.05.** Total de sesiones por entrenador | **R.F.01.** Recaudación en tienda por categoría |
| | | **R.F.09.** Facturación y cantidad de bonos | **R.F.04.** Precios mín/máx de productos |
| | | **R.F.10.** Duración de sesiones por entrenador | **R.F.06.** Gasto total y medio por socio |
| | | | **R.F.07.** Consumo de bebidas por socio |

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Tiempo de respuesta del código QR**

Como Socio
quiero que el sistema valide mi código QR en el torno en menos de 2 segundos
para evitar que se formen colas en la entrada de las instalaciones.

**R.N.F. 02. Disponibilidad del sistema de reservas**

Como Socio
quiero que la plataforma de reservas esté disponible 24/7
para poder gestionar mis clases en cualquier momento, incluso cuando el gimnasio está cerrado.

**R.N.F. 03. Adaptabilidad a dispositivos móviles**

Como Socio o Entrenador Personal
quiero que la interfaz web se adapte perfectamente a las pantallas de los teléfonos móviles
para poder reservar clases, fichar o consultar el horario sin necesidad de usar un ordenador de escritorio.

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1. Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias
