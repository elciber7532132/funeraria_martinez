# FUNERARIA MARTÍNEZ — Sistema final limpio

Sistema empresarial para control de abastecimiento, kilometraje, combustible y flota.

## Incluye
- Frontend HTML/CSS/JavaScript.
- Backend Node.js + Express.
- PostgreSQL.
- Login de administrador.
- Alta, edición y eliminación de abastecimientos.
- Alta/baja de vehículos, conductores y combustibles.
- Importación desde Excel/CSV y plantilla de importación.
- Exportación Excel.
- Cálculo automático de KM anterior, recorrido, importe y consumo KM/galón.
- Promedios por vehículo: KM/día, gasto/día, galones/día y KM/galón.
- Estados Normal / Advertencia / Excesivo según el historial individual de cada vehículo.
- Márgenes configurables desde Configuración.
- Reporte diario y mensual con gráficos.
- Base inicial limpia: no se cargan vehículos, conductores ni abastecimientos.

## Instalación
1. Crear la base `funeraria_martinez` en PostgreSQL.
2. Ejecutar `database/schema.sql`.
3. Ejecutar `database/seeds.sql` (no inserta datos operativos).
4. Copiar `backend/.env.example` como `backend/.env` y completar `DATABASE_URL`, `JWT_SECRET` y `ADMIN_PASSWORD`.
5. En `backend`: `npm install` y `npm run dev`.
6. Abrir `http://localhost:3000`.

## Importación Excel
Desde **Abastecimientos → Importar Excel**. La plantilla se descarga con **Plantilla Excel**. Si una placa o conductor no existe, el sistema los crea automáticamente.

Columnas principales: Fecha, Hora, Placa, Conductor, KM actual, Combustible, Galones, Precio por galón, N° Ticket, N° Factura, N° Boleta, Descripción.
