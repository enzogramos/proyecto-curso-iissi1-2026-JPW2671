# FitUS

## Miembros del grupo L8-AM-G1

1. Letrán Rodríguez, Julio
2. Baya Rodríguez, Mario
3. Ramos Andrés, Enzo

## 1. Introducción al problema

El gimnasio "FitUS" ha experimentado un crecimiento notable de clientes durante los últimos meses y ha decidido ampliar sus servicios. En estos momentos, la gestión de las inscripciones, el control de aforo de las clases dirigidas (como Aeróbic o Zumba) y la gestion de cobros y suscripciones se realiza mediante hojas de cálculo y documentos físicos que dificultan la organización.

### Situación actual y problemas:
La gestión manual del gimnasio está provocando una serie de problemas críticos en el día a día:
 - Sobrecarga en clases dirigidas: El aforo en las clases mas populares se suele superar ya que los clientes no pueden reservar con antelación y entran por orden de llegada, generando quejas y problemas de espacio.

 - Descontrol en los planes de suscripción y ventajas: El gimnasio ofrece un plan "Básico" (acceso al gimnasio y a 2 clases a la semana) y un plan "Ultimate" (acceso ilimitado a todas las instalaciones). Recientemente se ha instalado una máquina dispensadora de bebidas isotónicas y se ha abierto una pequeña tienda de suplementación deportiva. La recepción está teniendo problemas para verificar qué clientes tienen el plan Ultimate para permitirles usar la máquina de bebidas sin coste o para aplicarles los descuentos exclusivos en la tienda, lo que ralentiza el servicio y provoca pérdidas económicas.
 

 - Conflictos con los Entrenadores Personales: Además de los monitores de clases grupales, el gimnasio ha incorporado entrenadores personales como un servicio añadido. Estas sesiones privadas no están incluidas en las cuotas habituales (Básico o Ultimate), sino que se abonan aparte. Actualmente, la gestión de estas agendas se realiza en papel, lo que está provocando dos problemas graves: por un lado, continuos solapamientos en los horarios de las citas; y por otro, una falta de control en la facturación, impartiéndose a menudo sesiones sin haber comprobado previamente si el cliente ha pagado por este servicio extra.

### Expectativas del sistema:
Se requiere el desarrollo de un sistema de información que permita digitalizar toda la gestión del club. El sistema debe permitir a los socios gestionar su plan (Básico o Ultimate) y realizar reservas tanto para clases dirigidas como para sesiones con entrenadores personales. Además, el software deberá integrar un módulo de punto de venta (TPV) para la tienda que aplique descuentos automáticamente según el plan del usuario, y gestionar de forma automatizada los permisos de acceso a las ventajas premium, como la máquina de bebidas.

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
El sistema deberá gestionar el catálogo de clases ofertadas, permitir la inscripción y control de pagos de los socios, automatizar el proceso de reserva de plazas asegurando que no se supere el aforo, y proveer interfaces adaptadas a los distintos tipos de usuarios.

Además, el sistema deberá integrar un módulo de ventas para la tienda que calcule automáticamente descuentos según el tipo de suscripción. También gestionará la agenda individual de los entrenadores personales y el control de acceso lógico a la máquina de bebidas isotónicas.

El sistema también deberá gestionar un registro de cobros para servicios adicionales fuera de cuota, manteniendo un saldo de sesiones pagadas y pendientes de disfrutar para cada usuario.


### 3.2. Usuarios del sistema

 - Socio: Interactúa con el sistema para ver el horario, reservar clases y gestionar su suscripción.

 - Monitor: Utiliza el sistema para consultar su calendario de clases asignadas y pasar lista de los asistentes.

 - Entrenador Personal: Utiliza el sistema para gestionar su disponibilidad, aceptar o rechazar reservas de sesiones individuales y consultar el historial de los socios a los que entrena.

 - Administrador: Encargado de dar de alta nuevas clases, gestionar monitores y supervisar el estado de los pagos y suscripciones.


## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Reservar plaza en clase dirigida

Como Socio
quiero reservar una plaza en una clase dirigida
para asegurar mi asistencia y no quedarme sin espacio.

**Prueba de aceptación**
 - Comprobar que el sistema descuenta una plaza del aforo total disponible para esa clase concreta.
 - Comprobar que el sistema no permite la reserva si la clase ya ha alcanzado su aforo máximo.
 - Se deben aplicar las reglas de negocio R.N.01, R.N.02 y R.N.05. 

#### R.F.02. Reservar sesión con Entrenador Personal
Como Socio
quiero reservar una sesión individual con un entrenador personal en un tramo horario disponible
para recibir un entrenamiento adaptado a mis objetivos.

**Prueba de aceptación**
- Comprobar que el tramo horario seleccionado queda bloqueado.
- Comprobar que el sistema descuenta automáticamente una sesión del saldo de bonos pagados por el cliente.
- Se debe aplicar la regla de negocio R.N.08. 

#### R.F.03. Registrar venta en tienda

Como Administrador
quiero registrar la venta de un producto de la tienda asociándola a un socio
para llevar el control de ingresos y actualizar el stock del inventario.

**Prueba de aceptación**
- Comprobar que el stock del producto disminuye exactamente en la cantidad vendida.
- Comprobar que el precio final a cobrar se calcula correctamente.
- Se debe aplicar la regla de negocio R.N.04.  

#### R.F.04. Dispensar bebida isotónica

Como Socio
quiero identificarme en la máquina de bebidas del gimnasio
para obtener una consumición sin necesidad de pasar por recepción.

**Prueba de aceptación**
 - Comprobar que el sistema verifica el tipo de suscripción activa del usuario antes de habilitar el dispensador.
 - Se debe aplicar la regla de negocio R.N.03. 

#### R.F.05. Control de acceso a las instalaciones

Como Socio
quiero escanear mi código QR personal en el torno de entrada
para acceder a las instalaciones del gimnasio de forma autónoma.

**Prueba de aceptación**
- Comprobar que el torno se desbloquea si el código QR es válido y la suscripción está activa.
- Comprobar que el sistema deniega el acceso y muestra un aviso en recepción si el socio tiene recibos pendientes.
- Se debe aplicar la regla de negocio R.N.06 y R.N.07.

#### R.F.06. Comprar bono de sesiones de Entrenador Personal

Como Socio
quiero comprar de forma individual o en bonos sesiones de entrenamiento personal
para tener saldo disponible y poder agendar citas con los entrenadores.

**Prueba de aceptación**
- Comprobar que, tras registrarse el pago, el saldo de sesiones extra del socio aumenta en la cantidad comprada.

#### 4.1.1. Requisitos de información

##### R.I.01. Información de la suscripción del socio

Como Administrador
quiero ver los detalles del plan contratado por un socio
para comprobar su modalidad de suscripción y si está al corriente de pago.

**Prueba de aceptación**
- Comprobar que se muestra el tipo de plan (Normal o Pro), la fecha de inicio, y la fecha de próxima renovación.
- Comprobar que se muestran los datos personales básicos asociados al socio.  

##### R.I.02. Historial de compras del socio
Como Administrador
quiero consultar el historial de productos comprados por un socio en la tienda
para resolver dudas sobre facturación, garantías o devoluciones.

**Prueba de aceptación**
- Comprobar que se muestra una lista cronológica con la fecha, el producto, la cantidad y el precio final pagado.
- Comprobar que se indica claramente si en la compra se aplicó algún descuento especial por su tipo de suscripción. 

##### R.I.03. Calendario de clases y sesiones

Como Monitor / Entrenador Personal
quiero visualizar mi horario semanal de clases grupales y sesiones individuales
para preparar el material necesario y conocer a los asistentes con antelación.

**Prueba de aceptación**
- Comprobar que se muestran ordenadas cronológicamente las sesiones asignadas al empleado en la semana en curso.
- Comprobar que se puede acceder al listado actualizado de socios apuntados a cada clase o sesión.

##### R.I.04. Consulta del estado de la suscripción propia
Como Socio
quiero consultar los detalles de mi suscripción actual
para saber qué plan tengo activo, cuándo se me cobrará el próximo recibo y si tengo pagos pendientes.

**Prueba de aceptación**
- Comprobar que se muestra de forma clara el tipo de plan contratado (Normal o Pro).
- Comprobar que se indica la fecha del próximo cobro o renovación.
- Comprobar que el sistema avisa visualmente si existe algún recibo pendiente de pago.
- Comprobar que se muestra el saldo actual de sesiones de entrenador personal pagadas y pendientes de utilizar.


#### 4.1.2. Reglas de negocio

##### R.N.01. Límite de reservas por suscripción

Un socio con "Plan Normal" solo puede tener activas un máximo de 2 reservas a clases dirigidas por semana natural. Un socio con "Plan Pro" no tiene límite de reservas, sujeto únicamente a la disponibilidad de aforo de la clase.

##### R.N.02. Antelación de reserva

Ningún socio puede reservar una plaza en una clase dirigida con más de 7 días de antelación ni con menos de 1 hora antes del comienzo previsto para la misma.

##### R.N.03. Límite de dispensación de bebidas

El acceso a la máquina de bebidas gratuitas está restringido exclusivamente a los socios con "Plan Pro" activo. Para evitar abusos, un mismo socio solo puede dispensar una bebida cada 45 minutos.

##### R.N.04. Descuento en tienda por fidelidad

El sistema aplicará de forma automática y obligatoria un 15% de descuento sobre el precio de venta al público en todos los productos de la tienda si el comprador tiene una suscripción "Plan Pro" activa y al corriente de pago en el momento exacto de la compra.

##### R.N.05. Control de aforo estricto

Bajo ninguna circunstancia el sistema permitirá que el número de reservas activas para una clase dirigida supere el aforo máximo establecido para la sala física donde se imparte dicha actividad.

##### R.N.06. Restricción de acceso por impago

El sistema denegará automáticamente el acceso físico a las instalaciones a cualquier socio que tenga uno o más recibos devueltos o pendientes de pago, independientemente del tipo de plan (Normal o Pro) que tenga contratado.

##### R.N.07. Acceso intransferible

El código QR de acceso generado por el sistema es único e intransferible y se regenerará dinámicamente cada 30 segundos desde la app del gimnasio. Si el sistema detecta que un mismo QR intenta usarse en los tornos de entrada con una diferencia menor a 5 minutos, el segundo acceso será bloqueado por posible intento de fraude.

##### R.N.08. Saldo positivo para entrenamientos personales

El sistema denegará cualquier intento de reserva de una sesión con un Entrenador Personal si el socio no dispone de al menos una (1) sesión extra pagada y no consumida en su saldo, independientemente de si el usuario posee un Plan Básico o Plan Ultimate.


### 4.2. Mapa de historias de usuario (opcional)

A continuación, se detalla el flujo cronológico y lógico de interacción del socio con el sistema:

| FASE 1: Registro y Gestión | FASE 2: Acceso a Instalaciones | FASE 3: Reservas Deportivas | FASE 4: Consumo Premium y Tienda |
|:---|:---|:---|:---|
| **R.F.** Alta en el sistema y selección de plan (Básico/Ultimate) | **R.F.05.** Control de acceso por código QR | **R.F.01.** Reservar plaza en clase dirigida | **R.F.04.** Dispensar bebida isotónica |
| **R.I.04.** Consulta del estado de la suscripción propia | *Validación R.N.06 (Restricción por impago)* | **R.F.06.** Comprar bono de sesiones de Entrenador Personal | **R.F.03.** Registrar venta en tienda (TPV) |
| *Acciones administrativas de alta y cobro* | *Validación R.N.07 (Acceso intransferible)* | **R.F.02.** Reservar sesión con Entrenador Personal | *Validación R.N.03 (Límite de bebidas por tiempo)* |
| | | *Validación R.N.01 y R.N.05 (Aforos y límites de clases)* | *Validación R.N.04 (Descuento Pro en tienda)* |
| | | *Validación R.N.08 (Saldo positivo para entrenamientos)* | |
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

### 7.1.  Justificación de la estrategia de transformación de jerarquías

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


