
# Sistema de gestión de stock

## Autores

- [@MarceloDanielToledo](https://github.com/MarceloDanielToledo)

## Contexto

Actualmente, la fábrica de productos se enfrenta a limitaciones significativas debido a su sistema de gestión de stock, que ha quedado obsoleto. Este sistema, además de ser rígido y difícil de adaptar, solo funciona en una versión antigua de Windows y no se integra adecuadamente con los procesos actuales de la fábrica. Estas deficiencias están generando ineficiencias en la gestión de inventarios, como rupturas de stock frecuentes, exceso de inventario y una visibilidad limitada del flujo de materiales, lo que impacta negativamente en la operación diaria y eleva los costos.

Es necesario implementar un nuevo sistema de gestión de stock que responda a las necesidades actuales y futuras de la fábrica. Este sistema debe ser flexible y multiplataforma, accesible desde cualquier dispositivo con un navegador web. Con él, se podrán obtener datos en tiempo real, integraciones fluidas con otros sistemas y la posibilidad de personalizar funciones según las necesidades específicas de la fábrica, facilitando así una mejor toma de decisiones.

Este sistema beneficiará a los gerentes de producción, responsables de almacén y al equipo de compras, al proporcionarles una herramienta más moderna y eficiente que acompañará el crecimiento y la evolución de la fábrica.

## Objetivos

- Mejorar la accesibilidad y flexibilidad: Facilitar el acceso al sistema desde cualquier dispositivo con navegador web.

- Integrar con otros sistemas: Asegurar sincronización fluida con el módulo de compras y otros sistemas existentes.

- Facilitar la toma de decisiones: Ofrecer reportes y análisis predictivos para una mejor planificación.

- Optimizar métricas de gestión: Mejorar tiempos de respuesta y eficiencia operativa en la gestión de inventarios.

## Límites

- El proyecto se centra únicamente en la gestión de stock y no incluirá módulos adicionales como contabilidad o gestión de recursos humanos.

- El sistema no abordará la actualización o reemplazo del hardware existente en la fábrica, solo se enfocará en el software de gestión de stock.

- No se crearán características adicionales que no estén relacionadas directamente con la gestión de stock, como nuevas funcionalidades para otros departamentos o procesos no definidos en el alcance.

- La formación será limitada a la capacitación básica para el uso del nuevo sistema; no se incluirán programas de formación extensivos ni soporte para otros procesos empresariales.

## Principales etapas

**Definición de requisitos** - 08/30/24

- Reunión para definir y acordar los requisitos del sistema con el cliente.

**Diseño y Prototipo** - 09/15/24

- Presentación del diseño y prototipo inicial para obtener feedback del cliente.

**Desarrollo de funcionalidades clave** - 10/15/24

- Entrega de las funcionalidades principales del sistema.

**Integración y Pruebas** - 11/15/24

- Integración del sistema con otros módulos y realización de pruebas. Reunión para revisar los resultados con el cliente.

**Despliegue y Capacitación** - 12/01/24

- Implementación del sistema y capacitación básica para los usuarios.

**Revisión final y Ajustes** - 12/15/24

- Revisión final con el cliente para hacer ajustes según feedback.


## Solución existente

Actualmente, la fábrica utiliza un sistema de gestión de stock desarrollado en FoxPro. Este sistema antiguo está limitado en términos de funcionalidad y flexibilidad, lo que dificulta su adaptación a las necesidades modernas de la fábrica. Los usuarios interactúan con el sistema a través de una interfaz gráfica que permite realizar operaciones básicas como el registro de entradas y salidas de inventario, la generación de reportes y la visualización del estado del stock.

Sin embargo, el sistema presenta varias deficiencias, incluyendo una integración limitada con otros procesos de la fábrica, la falta de soporte para actualizaciones y personalizaciones, y problemas de compatibilidad con versiones más recientes de sistemas operativos. Esta situación ha llevado a una gestión ineficiente del inventario y a una creciente necesidad de una solución más moderna y adaptable.


## Solución propuesta

La solución propuesta para el nuevo sistema de gestión de stock es una aplicación web basada en Blazor WebAssembly. Esta elección permite una plataforma moderna y flexible, accesible desde cualquier dispositivo con un navegador web. A continuación, se detalla la solución en términos de arquitectura, funcionalidades clave y flujo de trabajo.

### Visión general

El sistema estará compuesto por una aplicación web interactiva que se ejecuta en el navegador del usuario utilizando Blazor WebAssembly. Esto permite una experiencia de usuario rica y dinámica, con una interfaz moderna que facilita la gestión del inventario en tiempo real. La aplicación se conectará a una API backend para manejar todas las operaciones relacionadas con los datos de inventario.

### System Architecture

- **Interfaz de Usuario (UI):** La aplicación web se desarrollará utilizando Blazor WebAssembly, lo que permitirá una interfaz fluida y responsiva. Los usuarios podrán acceder al sistema desde cualquier dispositivo con navegador, ya sea en una computadora de escritorio, tablet o teléfono móvil.

- **API Backend:** La aplicación se conectará a una API RESTful que manejará todas las operaciones del sistema, incluyendo la gestión de inventario, generación de reportes y sincronización con otros módulos de la fábrica. Esta API estará construida con .NET, proporcionando robustez y escalabilidad.

- **Base de Datos:** La información de inventario se almacenará en una base de datos centralizada, que permitirá consultas eficientes y almacenamiento seguro de los datos. La base de datos se diseñará para integrarse fácilmente con la API y soportar las operaciones del sistema.

- **Autenticación y Seguridad:** La aplicación incluirá mecanismos de autenticación y autorización para garantizar que solo los usuarios autorizados puedan acceder y modificar los datos de inventario. Se implementarán medidas de seguridad para proteger la integridad y confidencialidad de los datos.


### Flujo de trabajo

- **Inicio de Sesión:** Los usuarios acceden al sistema mediante una página de inicio de sesión segura. Una vez autenticados, son dirigidos a la página principal donde pueden visualizar y gestionar el inventario.

- **Gestión de Inventario:** Los usuarios podrán registrar nuevas entradas y salidas de inventario, ajustar niveles de stock y generar reportes. La interfaz proporcionará una vista clara y actualizada de los niveles de inventario y alertas sobre posibles problemas.

- **Generación de Reportes:** El sistema permitirá la generación de reportes detallados sobre el estado del inventario, incluyendo históricos de movimientos y análisis de tendencias. Los reportes se podrán exportar en varios formatos para su revisión y análisis.

- **Sincronización con Otros Sistemas:** La aplicación estará integrada con otros módulos de la fábrica, como el sistema de compras, para asegurar que los datos de inventario estén siempre actualizados y sincronizados.


## Soluciones alternativas

### Solución de terceros

Consideramos la opción de adquirir un sistema de gestión de stock de un proveedor externo. Estas soluciones suelen ofrecer funcionalidades avanzadas y soporte continuo. Ejemplos incluyen sistemas como SAP Business One o NetSuite.

**Pros:**

- Implementación más rápida debido a la disponibilidad inmediata del software.
- Soporte y actualizaciones continuas proporcionadas por el proveedor.
- Funcionalidades ya probadas y confiables.

**Contras:**

- Costo elevado por licencia y suscripción.
- Menos flexibilidad para personalizar según las necesidades específicas de la fábrica.
- Puede requerir integración compleja con los sistemas existentes.


### Solución de código abierto

Evaluamos el uso de soluciones de gestión de inventario de código abierto, como Odoo o ERPNext. Estas plataformas ofrecen una base robusta que se puede adaptar y extender según las necesidades.

**Pros:**

- Costos iniciales reducidos o nulos.
- Flexibilidad para personalizar y adaptar el software.
- Comunidad activa que puede ofrecer soporte y mejoras.

**Contras:**

- Requiere conocimientos técnicos para la personalización y mantenimiento.
- Soporte limitado comparado con soluciones comerciales.
- Posible necesidad de desarrollo adicional para integrar con otros sistemas.

### Desarrollo interno

Desarrollar una solución interna personalizada, como la propuesta utilizando Blazor WebAssembly, adaptada a las necesidades específicas de la fábrica.

**Pros:**

- Total alineación con los requisitos y procesos de la fábrica.
- Flexibilidad para modificar y escalar el sistema según se necesite.
- Control completo sobre el diseño y las funcionalidades.

**Contras:**

- Tiempo de desarrollo más largo.
- Requiere recursos internos para el desarrollo y mantenimiento.
- Mayor inversión inicial en comparación con soluciones preexistentes.


## Pruebas, Monitoreo y Alertas

**Pruebas**

La solución se someterá a una serie de pruebas exhaustivas para asegurar su correcto funcionamiento antes de su despliegue. Esto incluirá pruebas de usabilidad para verificar que los usuarios puedan interactuar con el sistema sin problemas, y pruebas de integración para asegurar que todas las funciones operen correctamente con otros sistemas. También se realizarán pruebas de rendimiento para asegurar que el sistema maneje el volumen de datos esperado sin retrasos.

**Monitoreo**

Una vez implementado, el sistema será monitoreado continuamente para asegurar su estabilidad y rendimiento. Se utilizarán herramientas de monitoreo para supervisar el estado del sistema, el uso de recursos y el tiempo de respuesta. Esto permitirá detectar y solucionar problemas antes de que afecten a los usuarios.

**Alertas**

Se establecerán alertas automáticas para notificar al equipo de soporte sobre cualquier anomalía o fallo en el sistema, como problemas de rendimiento, errores críticos o caídas del sistema. Las alertas ayudarán a responder rápidamente a cualquier incidente y minimizar el impacto en las operaciones de la fábrica.

## Impacto entre Equipos

**Impacto en Soporte y Operaciones:**
El nuevo sistema requerirá más atención del equipo de operaciones inicialmente, ya que será crucial asegurar que todo funcione correctamente durante la transición. Sin embargo, una vez que el sistema esté en funcionamiento, el número de problemas debería ser menor en comparación con el sistema antiguo.

**Costo:**
Crear e implementar el nuevo sistema incurrirá en costos, especialmente al principio. Sin embargo, a largo plazo, debería ahorrar dinero porque será más fácil de administrar y mantendrá el inventario mejor controlado.

**Velocidad del Sistema:**
Como aplicación web, el nuevo sistema podría funcionar ligeramente más lento en áreas con mala conectividad a internet. Aún así, está diseñado para asegurar que esta diferencia no sea demasiado notable.

**Seguridad:**
Al ser una aplicación web, puede estar expuesto a nuevos riesgos de seguridad, como intentos de acceso no autorizado. Por lo tanto, se tomarán medidas para garantizar la protección de los datos y que solo el personal autorizado pueda acceder a ellos.

**Posibles Inconvenientes:**
Los usuarios podrían necesitar tiempo para acostumbrarse al nuevo sistema, lo que podría causar algunos inconvenientes iniciales. Además, durante la transición, podrían surgir algunos problemas temporales en las operaciones si no se planifican adecuadamente.

**Comunicación con los Clientes:**
El equipo de soporte deberá explicar claramente a los clientes por qué se está realizando el cambio y cómo les beneficiará. También será importante brindar asistencia y capacitación para que la transición sea lo más fluida posible.


## Preguntas Abiertas

**Integración con Sistemas Existentes**

¿Qué nivel de compatibilidad se requiere con los sistemas actuales de la fábrica? ¿Deberíamos considerar una migración completa o una integración gradual?

**Capacitación de Usuarios**

¿Cuál es la mejor manera de capacitar a los usuarios en el nuevo sistema? ¿Son suficientes los tutoriales en línea, o será necesario realizar capacitación presencial?

**Escalabilidad Futura**

¿Cómo debemos planificar la escalabilidad del sistema para futuras expansiones de la fábrica? ¿Hay áreas críticas que requieran más atención desde el principio?

**Opciones de Personalización**

¿Hasta qué punto debe ser personalizable el sistema para adaptarse a los cambios en los procesos de la fábrica? ¿Es mejor ofrecer un conjunto básico de opciones o permitir una personalización más extensa?

**Gestión de Datos Históricos**

¿Cómo manejaremos la transición de los datos históricos del sistema antiguo al nuevo? ¿Es necesario importar todos los datos o solo los relevantes para las operaciones actuales?


## Alcance Detallado y Cronograma

### Alcance Detallado:

**Fase 1: Análisis de Requisitos y Planificación (Fecha: 1ra semana)**

- Reuniones con partes interesadas para definir los requisitos específicos del sistema.
- Preparación del documento final de requisitos.

**Fase 2: Diseño del Sistema (Fecha: 2da-3ra semana)**

- Diseño de la arquitectura del sistema, incluyendo flujos de datos y estructura de la base de datos.
- Creación de maquetas para la interfaz de usuario.

**Fase 3: Desarrollo Inicial (Fecha: 4ta-8va semana)**

- Implementación de la estructura básica del sistema.
- Desarrollo de funcionalidades críticas, como gestión de inventario y seguimiento de stock.

**Fase 4: Integración y Pruebas (Fecha: 9na-11va semana)**

- Integración con sistemas existentes.
- Realización de pruebas unitarias e integradas para asegurar la calidad del sistema.

**Fase 5: Implementación Piloto (Fecha: 12va semana)**

- Implementación inicial en un entorno controlado.
- Recopilación de feedback y ajustes basados en la experiencia del usuario.

**Fase 6: Implementación Completa y Capacitación (Fecha: 13ra-14ta semana)**

- Implementación del sistema en toda la fábrica.
- Capacitación de los usuarios finales para asegurar una transición fluida.