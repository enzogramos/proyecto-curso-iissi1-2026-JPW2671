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
 

 - Conflictos con los Entrenadores Personales: Además de los monitores de las clases grupales, el gimnasio ha incorporado entrenadores personales como un servicio añadido. Llevar la agenda de estos entrenamientos privados en papel está provocando confusiones con los horarios y que a veces se olvide cobrar la sesión al cliente.

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

### 3.2. Usuarios del sistema

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

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


