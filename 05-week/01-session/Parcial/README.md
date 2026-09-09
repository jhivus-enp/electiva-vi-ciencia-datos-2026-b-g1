# Parcial Práctico - Corte 1

**Estudiante:** José Julián Bríñez Garzón  
**Caso de estudio:** Minimercado "El Vecino"

---

## 1. Clasificación de Tipos de Datos

* **Ventas diarias (Estructurado):** Tabla en Excel o base de datos relacional con campos de fecha, ID de producto, cantidad, precio unitario y total.
* **Inventario de proveedores (Estructurado):** Registro relacional con código de producto, proveedor, stock disponible y costo unitario.
* **Facturas electrónicas de compra (Semiestructurado):** Archivos XML/JSON emitidos por proveedores que contienen etiquetas organizadas pero con estructura flexible.
* **Mensajes y opiniones de clientes (No estructurado):** Textos libres recibidos por WhatsApp o notas en el buzón de sugerencias sin un formato fijo.

---

## 2. Preguntas de Analítica

* **Analítica descriptiva:** ¿Cuál fue el producto más vendido y el total de ingresos generados durante el mes pasado?
* **Analítica predictiva:** ¿Cuántas unidades de bebidas se deberán pedir al proveedor para el próximo fin de semana según las ventas históricas y la proyección del clima?

---

## 3. Diagrama del Flujo de Datos


[Caja registradora / XMLs / WhatsApp]
                 │
                 ▼
        1. Fuente de datos
                 │
                 ▼
   [Base de datos MySQL / Excel]
                 │
                 ▼
     2. Almacenamiento de datos
                 │
                 ▼
        [Consultas SQL / Python]
                 │
                 ▼
        3. Análisis de datos
                 │
                 ▼
     [Dashboard en Power BI]
                 │
                 ▼
        4. Visualización
        
## 4. Descriptive vs. Predictive Analytics
Descriptive Analytics: Descriptive analytics examines historical data to understand what has already happened in the business over a specific period.

Predictive Analytics: Predictive analytics uses historical data and statistical patterns to forecast future outcomes and trends.