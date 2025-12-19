🧠 Regla de oro (GUÁRDALA)

  Se estudian los conceptos.
  Se consulta la documentación.
  Se aprende resolviendo problemas.

Conceptos Básicos

Qué es un programa: es una secuencia de instrucciones con sintaxis y reglas que se ejecutan para realizar una tarea o resolver un problema .
Qué es una app: es un programa de software con una interfaz en donde el usuario puede interactuar para resolver una necesidad o ejecutar una tarea.
Qué es una API: es un recurso que permite que diferentes app o sistemas se comuniquen entre sí, ejepmplo: el fron end con el back end.

Flujo: Usuario → Front → Backend → BD

Usuario: es una persona que utiliza una app de software para satisfacer una necesidad o resolver un problema.
FrontEnd: es la parte visual e interactiva de la aplicación que permite al usuario realizar acciones y enviar solicitudes al sistema. 
BackEnd: es la parte de la aplicación que maneja la lógica, validaciones, seguridad y la persistencia de los datos, y no está expuesta al usuario.
BD: Una base de datos es un sistema que almacena datos de forma organizada y permite consultarlos, insertarlos, modificarlos o eliminarlos.

Python: es un lenguage de programación, define como se escribe la lógica de un programa y puede usarse para múltiples propósitos.
VS Code: es un editor de código que permite escribir y editar código para frontend y backend e integrar librerías .
IDE: es un entorno de desarrollo integrado que incluye herramientas para escribir, ejecutar y depurar código, como un taller completo.
FrameWork: define una estructura y reglas base para construir una aplicación, facilitando el desarrollo del software. (plantilla determinada)
Lenguage de programación: es un medio para comunicarse con la computadora mediante instrucciones que permiten crear software.

Editor / IDE → (VS Code / Visual Studio)
Lenguaje     → (C#, Python, JS)
Framework    → (.NET, Django, React)
Capa         → (Frontend / Backend)

Recurrencia: algo que se repite en el tiempo (pagos recurrentes, mensual).
Concurrencia: es la existencia de múltiples peticiones o tareas activas al mismo tiempo que el sistema debe gestionar, aunque no se ejecuten exactamente al mismo instante.
Paralelismo: es la capacidad del sistema de ejecutar varias de esas tareas simultáneamente usando múltiples recursos (como núcleos del CPU).

El multihilo no hace el sistema más rápido, lo hace más eficiente. (El paralelismo sí lo hace más rápido.)

Las validaciones deciden si se puede intentar la operación. La transacción garantiza que los cambios no queden incompletos.

Nombrar esto formalmente (ACID): ACID NO es una tecnología, es un conjunto de garantías que debe cumplir una transacción.
🅐 Atomicidad: Todo o nada. Nada queda a medias.
  ejemplo: o se descuenta el dinero o no se descuenta nada
🅒 Consistencia: Los datos siempre cumplen las reglas. Después de la transacción, el sistema sigue siendo válido.
  ejemplo: el saldo no puede ser negativo, una cuenta no puede desaparecer.
🅘 Aislamiento: Las transacciones no se pisan entre sí.
  ejemplo: dos retiros al mismo tiempo, uno espera al otro, no se mezclan resultados.
🅓 Durabilidad: Una vez confirmado, no se pierde, aunque se caiga el sistema, aunque se reinicie el servidor.
  ejemplo: El dinero ya quedó guardado.

Arquitectura por capas: separar el sistema en capas con responsabilidades distintas.    Controller → Service → Repository → BD
Arquitectura por capas + servicios: Controller → Service → Domain → Repository → BD
Arquitectura hexagonal / limpia (avanzada): puertos, adaptadores, dominio independiente. Se usa cuando el sistema crece mucho.

🧩 Controlador (Controller): 
    Qué es: el punto de entrada del sistema.
    Qué hace: recibe la petición (ej: “retirar dinero”), valida formato básico, llama al servicio correcto, devuelve la respuesta
    Analogía: El recepcionista.
🧩 Servicio (Service)
    Qué es: Donde vive la lógica de negocio. No es API (Un API es la interfaz, no la lógica.)
    Qué hace: valida reglas, coordina procesos, maneja transacciones, decide qué pasa 
    Analogía: El gerente que toma decisiones.
🧩 Domain (reglas) 
    Qué es: el Domain aparece cuando la complejidad lo justifica, no por moda.
    Qué hace: reglas son complejas, hay muchas validaciones, lógica reutilizable
🧩 Repositorio (Repository)
    Qué es: la capa que habla con la base de datos.
    Qué hace: guarda datos, consulta datos, no tiene lógica de negocio.
    Analogía: El archivador.
🧩 Database

DTO (Data Transfer Object): es un objeto cuya única responsabilidad es transportar datos entre capas o sistemas, no decide, no valida reglas de negocio, no contiene lógica.
DOMINIO: El dominio es la realidad que el software intenta representar, no porque sea código, sino porque representa la realidad. 
DOMINIO WEB: nombre de una página
DOMINIO SOFTWARE: es una representación de una parte de la realidad del negocio, y las entidades son los elementos que viven dentro de ese dominio.
  Ejemplo (Bancario): La entidad no define el dominio, el dominio contiene a las entidades.
    Realidad: Personas → cuentas → dinero → retiros
    Dominio bancario: Reglas y conceptos sobre cuentas, clientes, saldos, transacciones, Entidades, Cliente, CuentaBancaria, Transaccion.
ENTIDAD: existe por sí mismo que puede cambiar con el tiempo pero sigue siendo “lo mismo” aunque cambie. Ejemplo (Una persona cambia cuando crece pero sige siendo persona)
ENTIDAD DE DOMINIO: es la versión en el software de algo importante del mundo real, que tiene identidad y reglas propias.

Las entidades piensan, los DTO solo viajan.

Documentación técnica SIN perderte

  🧠 La documentación no se estudia, se consulta. 
  🧠 El conocimiento se construye resolviendo problemas.

  🧠 Regla de oro para documentación: No se lee para aprender todo, se lee para resolver un problema puntual.
  ❌ Error común: leer todo, copiar código, saltar de página en página

  Paso 1: ¿QUÉ problema tengo?
    Ejemplo: “Quiero guardar datos en BD con transacciones”
  Paso 2: Identifica el concepto
    Ejemplo: transacciones, commit / rollback
  Paso 3: Busca SOLO eso
    Ejemplo: .NET transaction commit rollback
              NO: tutoriales gigantes, frameworks completos
  Paso 4: Lee solo estas secciones
    ✔️ Overview, ✔️ Examples, ✔️ Warnings / Notes
    🚫 Evita: APIs internas, configuraciones avanzadas.
  Paso 5: Traduce a tu sistema
    Pregúntate: “¿Dónde entra esto en MI arquitectura?”



