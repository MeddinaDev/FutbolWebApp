# FutbolWebApp - Proyecto DataFlex

Este proyecto es una aplicación web para la gestión de una liga de fútbol, desarrollada como parte del grado en Desarrollo de Aplicaciones Multiplataforma.

## Características
* Conexión a base de datos MySQL mediante ODBC.
* Gestión de jugadores, equipos y ligas.
* Dashboard personalizado con acceso directo a las vistas.
* Listas de selección funcionales (Lookups).

## Tecnologías utilizadas
* DataFlex 2025 (25.0)
* MySQL






## Tarea 2 - Cuestiones de Navegación

-> Pregunta 1: From main-> Select-Zoom, ¿qué pasa con InvokingObject?
- Respuesta: Cuando la navegación es nfFromMain (por ejemplo, al abrir una vista desde el menú principal), el InvokingObject normalmente es 0 o el propio menú, ya que la vista no está siendo invocada desde otro formulario o registro de datos, sino desde el sistema general.

-> Pregunta 2: Undefined->Zoom jugador-Select posición: botón que lleve desde un jugador al Select posiciones ¿Hay relación entre ellas?
- Respuesta: No hay una relación directa padre-hijo estándar configurada en los Diccionarios de Datos de esa vista concreta (es una relación muchos a muchos a través de una tabla intermedia). Al no ser una relación directa nfFromParent o nfFromChild que DataFlex entienda de forma automática, el sistema lo clasifica como una navegación nfUndefined o personalizada.

-> Pregunta 3: Lista de TODOS los eventos que intervienen en una navegación de manera ordenada y de qué objetos son.
- Respuesta: El ciclo ordenado de eventos es:

A) OnGetNavigateForwardData: Pertenece al Invoking Object (el botón de origen).

B) OnNavigateForward: Pertenece a la Invoked View (la vista de destino que se abre).

C) OnLoad / OnBeforeShow / OnShow: Pertenecen a la Invoked View (al cargar en pantalla).

D) OnGetNavigateBackData: Pertenece al Invoked Object (cuando decidimos volver atrás).

E) OnNavigateBack: Pertenece al Invoking Object (la vista original que nos vuelve a recibir)
