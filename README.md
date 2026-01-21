📊 Desafío: Análisis de Retención de Clientes — Andes Bank

![Estado del Proyecto](https://img.shields.io/badge/Estado-Finalizado-success)
![Tecnologías](https://img.shields.io/badge/Tecnologías-Python%20%7C%20Pandas%20%7C%20Seaborn-blue)

---

## 🎯 1. Objetivo del Proyecto

Andes Bank enfrenta una tasa de abandono estructural del **20.4%**. El objetivo de este análisis es identificar los **drivers críticos de churn** y generar un enfoque de retención proactiva basado en datos, priorizando la experiencia del cliente y la fidelización de segmentos de alto valor.

**Indicadores clave evaluados:**

1. **Magnitud del Churn:** Determinación de la línea base de pérdida.
2. **Perfil Demográfico Crítico:** Segmentos Senior y mercado alemán con mayor vulnerabilidad.
3. **Fricción por Multiproducto:** Riesgo asociado a la complejidad de la relación financiera.
4. **Causalidad por Experiencia:** Impacto de quejas y problemas operativos en la fuga de clientes.

---

## 🛠️ 2. Tecnologías y Estructura

| Librería                 | Propósito                                                                              |
| :----------------------- | :------------------------------------------------------------------------------------- |
| **pandas**               | ETL, limpieza de datos y segmentación por ciclo de vida (`age_group`, `tenure_group`). |
| **matplotlib / seaborn** | Visualizaciones de alto impacto para presentar hallazgos estratégicos.                 |

### 📂 Archivos Clave

- `analisis_churn_andes_bank.ipynb` — Notebook con pipeline completo: ETL, análisis exploratorio y causalidad.
- `assets/plot_churn_rate.png` — Magnitud global del abandono.
- `assets/plot_churn_by_age_group.png` — Churn por grupo de edad.
- `assets/plot_churn_by_number_of_products.png` — Churn según número de productos.
- `assets/plot_churn_by_complain.png` — Evidencia del impacto crítico de la experiencia.

---

## 📈 3. Visualizaciones e Insights Determinantes

| Nº  | Visualización                     | Archivo                                       | Insight de Negocio                                                                | Impacto          |
| :-: | :-------------------------------- | :-------------------------------------------- | :-------------------------------------------------------------------------------- | :--------------- |
|  1  | **Tasa de Churn**                 | `assets/plot_churn_rate.png`                  | 1 de cada 5 clientes abandona la entidad.                                         | **20.4% Churn**  |
|  2  | **Churn por Grupo de Edad**       | `assets/plot_churn_by_age_group.png`          | El segmento Senior (45-60 años) concentra la mayor volatilidad.                   | **51.1% Churn**  |
|  3  | **Churn por Número de Productos** | `assets/plot_churn_by_number_of_products.png` | Clientes con más de un producto presentan riesgo extremadamente alto de abandono. | **85.9% Riesgo** |
|  4  | **Causalidad: Quejas**            | `assets/plot_churn_by_complain.png`           | Una queja activa equivale a una pérdida casi segura del cliente.                  | **99.5% Riesgo** |

> Cada gráfico se acompaña de crosstabs y comentarios interpretativos en el notebook para facilitar la comprensión y la acción estratégica.

---

## 📊 4. Conclusiones Estratégicas

- **Queja como predictor absoluto:** El factor determinante no es el precio ni el producto, sino las **fricciones en la resolución de incidencias**. El 99.5% de los clientes con quejas abandonan el banco.
- **Vulnerabilidad Demográfica:** Alemania (32.4%) y el segmento Senior (51.1%) presentan la mayor sensibilidad a fallos operativos.
- **Programas de fidelización y productos:** Tipos de tarjeta, puntos y salario muestran neutralidad estadística frente al churn; la fuga no es un problema de oferta económica sino de experiencia.

### ✅ Recomendaciones Ejecutivas (Andes Bank 2026)

1. **Protocolo de Recuperación Crítica (PQRS):** Intervención humana proactiva en menos de 12 horas ante cualquier queja.
2. **Auditoría Operativa en Alemania:** Revisar procesos locales para reducir fricción y quejas recurrentes.
3. **Servicio "Gold" para Seniors:** Simplificar canales digitales y humanos para clientes de alto valor.
4. **Optimización de Cross-selling:** Priorizar calidad de post-venta sobre cantidad de productos contratados, asegurando soporte y seguimiento impecables.
5. **Sistema de Alerta Temprana:** Implementar analítica predictiva para identificar clientes en riesgo antes de la decisión de abandono.

---

## ⚙️ 5. Ejecución y Dependencias

### 5.1. Entorno Local (Windows / Linux / MacOS)

```bash
# Crear entorno virtual
python -m venv .venv

# Activar entorno (Windows)
.venv\Scripts\activate

# Activar entorno (Linux / MacOS)
source .venv/bin/activate

# Instalar dependencias
pip install -r requirements.txt
```
