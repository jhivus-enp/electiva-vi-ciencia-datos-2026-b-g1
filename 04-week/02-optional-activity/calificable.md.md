## 1. Proceso y Pregunta de Datos

* **Área de Mecatrónica seleccionada:** Eficiencia Energética, Huella de Carbono e Inspección Automática de Calidad (*Green Mechatronics & Sustainable Manufacturing*).
* **Proceso real:** Monitoreo térmico, energético y de micro-defectos en un proceso automatizado de curado y tratamiento térmico de piezas mecánicas en hornos industriales mecatrónicos con inspección por visión artificial en línea.
* **Pregunta de datos:**  
  > *¿Cómo minimizar el consumo de energía eléctrica y las emisiones de CO2 en el horno de curado sin comprometer la tolerancia estructural ni la calidad estética de las piezas procesadas?*

---

## 2. Inventario de Datos

| Campo / Fuente | Descripción del Dato | Clasificación |
| :--- | :--- | :--- |
| **Consumo de potencia eléctrica (kWh / kW)** | Lecturas continuas desde multímetros digitales de red eléctrica inteligente integrados al controlador industrial (PLC). | **Estructurado** |
| **Perfil de temperatura y presión (°C, Bar)** | Registros numéricos continuos de sensores de presión y termocuplas tipo K en una base de datos de series temporales. | **Estructurado** |
| **Trazabilidad de lotes (ERP / MES)** | Archivos JSON exportados del sistema de manufactura con el identificador de lote, tipo de aleación, cliente y especificaciones del material. | **Semiestructurado** |
| **Lecturas de emisión de gases (CSV / JSON)** | Datos estructurados periódicos provenientes de analizadores IoT de calidad del aire (medición de CO2, NOx y Partículas en Suspensión). | **Semiestructurado** |
| **Imágenes de visión artificial de alta resolución** | Fotografías digitales (PNG/JPG) en luz visible y termográfica tomadas a la salida del horno para detectar fisuras, porosidades y deformaciones. | **No estructurado** |
| **Auditorías y normativas ambientales externas** | Documentos regulatorios, auditorías ambientales y reportes de cumplimiento en formato PDF o escaneados sin plantilla fija. | **No estructurado** |

---

## 3. Tipo de Analítica y Justificación Big Data

### Tipo de Analítica Aplicada: **Prescriptiva**

1. **Descriptiva:** Presenta en tiempo real la curva de temperatura del horno, el consumo térmico/eléctrico y el nivel de emisiones de CO2 generado en el turno actual.
2. **Predictiva:** Estima el impacto térmico en la pieza y la probabilidad de aparición de micro-defectos estructurales según la curva de enfriamiento aplicada al lote.
3. **Prescriptiva (Objetivo final):** Ajusta dinámicamente las consignas de potencia de las resistencias/quemadores y el flujo de aire para garantizar **cero defectos utilizando la mínima cantidad de energía eléctrica y gas por lote**.

### ¿Es un caso de Big Data? **SÍ, se justifica mediante las "V" del Big Data:**

* **Volumen:** La captura continua de imágenes térmicas e industriales de alta resolución sumada a la ingesta de parámetros físicos segundo a segundo genera cientos de Gigabytes por línea de producción.
* **Velocidad:** El sistema de visión artificial procesa piezas en microsegundos sobre la banda transportadora para realizar control en tiempo real sin frenar la velocidad mecatrónica de la línea.
* **Variedad:** Coexisten series temporales (consumo y temperatura), registros semiestructurados en JSON (sistema de manufactura), matrices de píxeles (imágenes térmicas) y texto sin formato (normativa ISO 14001).

---

## 4. Ciclo de Vida del Proyecto

```text
[1. Pregunta] ──► [2. Obtener] ──► [3. Limpiar] ──► [4. Analizar] ──► [5. Visualizar] ──► [6. Decidir]