# Conference Expense Planner

Aplicación web creada con React y Redux que permite planificar el presupuesto de un evento de conferencia. La pantalla inicial muestra una bienvenida y un botón para comenzar; al avanzar se puede elegir el recinto, añadir servicios audiovisuales y seleccionar comidas para los asistentes. Cada selección actualiza el costo total en tiempo real y ofrece un desglose detallado de los gastos.

## Resumen del código
- `src/App.jsx` muestra la portada con el botón **Get Started** y, tras activarlo, revela el flujo de selección y el componente de información inicial `AboutUs`. Usa estado local para controlar la visibilidad del planificador.【F:src/App.jsx†L1-L36】
- `src/ConferenceEvent.jsx` implementa el planificador principal: permite ajustar cantidades de salas (`venueSlice`), add-ons audiovisuales (`avSlice`) y comidas (`mealsSlice`), calcula subtotales por categoría y muestra un resumen detallado mediante `TotalCost`. También controla la lógica de navegación interna y la validación de cupos.【F:src/ConferenceEvent.jsx†L1-L205】【F:src/ConferenceEvent.jsx†L206-L285】
- `src/TotalCost.jsx` recibe los totales por sección y renderiza el monto combinado junto con la tabla detallada de selección proporcionada por `ConferenceEvent`.【F:src/TotalCost.jsx†L1-L22】
- `src/store.js` configura la tienda Redux combinando los reductores de sedes, servicios audiovisuales y comidas, centralizando el estado compartido de la aplicación.【F:src/store.js†L1-L12】

## Ejecución
1. Instala dependencias: `npm install`.
2. Ejecuta el entorno de desarrollo con Vite: `npm run dev`.
3. Construye la versión de producción: `npm run build`.

Con esto obtendrás una aplicación lista para estimar y visualizar los costos de tu próximo evento.
