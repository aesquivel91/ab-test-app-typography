<p align="center">
  <img src="tipografia-diseno-web.jpg" alt="AB Test Banner" width="800">
</p>

# 🅰️🅱️ A/B Test App Typography

## 🎯 Descripción del Proyecto
Este proyecto analiza los resultados de un experimento **A/A/B** en una aplicación móvil con el objetivo de evaluar si un **cambio en la tipografía** influye en el comportamiento de los usuarios y su progresión dentro del embudo de conversión.

Se estudiaron tres grupos experimentales:
- **Grupo 246 (Control A)**  
- **Grupo 247 (Control A)**  
- **Grupo 248 (Experimental B – nueva tipografía)**  

El análisis permite determinar si existen diferencias estadísticamente significativas en las tasas de conversión entre los grupos, garantizando que cualquier cambio visual se base en evidencia y no en suposiciones.

---

## 🧩 Objetivos
1. Evaluar la completitud y calidad de los datos.  
2. Analizar la distribución de usuarios y eventos entre grupos.  
3. Construir el embudo de conversión de la app.  
4. Aplicar pruebas estadísticas (Z-test de proporciones) para comparar conversiones entre grupos.  
5. Determinar si el cambio tipográfico impactó significativamente en la conversión.

---

## 📊 Dataset
El conjunto de datos incluye eventos de interacción de usuarios con la aplicación:

| Columna | Descripción |
|:--|:--|
| `event` | Tipo de evento (pantalla visitada o acción realizada) |
| `user_id` | Identificador único del usuario |
| `timestamp` | Fecha y hora del evento |
| `experiment` | Grupo experimental asignado (246, 247, 248) |

**Período analizado:** 1 al 7 de agosto de 2019  
**Usuarios totales:** 7,419  
**Eventos totales:** 240,887  

---

## 🔍 Metodología

### 1️⃣ Limpieza y preparación
- Conversión de `timestamp` a formato de fecha legible.  
- Renombrado de columnas.  
- Filtrado de datos incompletos previos al 1 de agosto de 2019.  

### 2️⃣ Exploración de datos
- Identificación de eventos frecuentes.  
- Verificación del equilibrio entre los grupos experimentales.  

### 3️⃣ Embudo de conversión
Secuencia de eventos clave:
1. `MainScreenAppear` – Pantalla principal  
2. `OffersScreenAppear` – Navegación por ofertas  
3. `CartScreenAppear` – Carrito de compras  
4. `PaymentScreenSuccessful` – Pago exitoso  

### 4️⃣ Análisis estadístico
- Cálculo de tasas de conversión entre etapas.  
- Aplicación de la **prueba Z de proporciones** para comparar resultados A/A y A/B.  

---

## 📈 Resultados Principales

| Etapa | Usuarios | Conversión desde anterior | Conversión total |
|:--|:--:|:--:|:--:|
| MainScreenAppear | 7,419 | - | 100% |
| OffersScreenAppear | 4,593 | 61.9% | 61.9% |
| CartScreenAppear | 3,734 | 81.3% | 50.3% |
| PaymentScreenSuccessful | 3,539 | 94.8% | **47.7%** |

- **Mayor pérdida:** entre la pantalla principal y la de ofertas (−38.1%).  
- **Conversión final total:** 47.7%.  
- No se detectaron diferencias estadísticamente significativas entre los grupos, lo que sugiere que **el cambio tipográfico no afectó el comportamiento del usuario**.

---

## 🧠 Conclusiones
- Los datos fueron consistentes y equilibrados entre los tres grupos experimentales.  
- El embudo de conversión muestra un rendimiento sólido, pero existe una oportunidad de mejora en la transición inicial (de la pantalla principal a las ofertas).  
- El experimento confirma que la **modificación tipográfica no generó cambios medibles en la conversión**, validando la hipótesis nula.  
- Este análisis refuerza la importancia de validar cualquier cambio de diseño con **pruebas controladas basadas en datos**.

---

## ⚙️ Tecnologías Utilizadas
- **Python:** pandas, numpy, matplotlib, seaborn, scipy, statsmodels  
- **Entorno:** Jupyter Notebook  

---

## 📂 Estructura del Repositorio
```
📁 AB-Test-App-Typography/
│
├── data/                         # Archivos CSV con los datos de eventos
├── AB Test App Typography.ipynb   # Notebook principal del análisis
├── README.md                      # Descripción del proyecto
└── images/                        # Gráficos del embudo y resultados
```

---

## 📎 Insights Adicionales
- Filtrar los primeros días del dataset mejora la calidad del análisis.  
- Las pruebas A/A fueron fundamentales para confirmar que el sistema de tracking no introducía sesgos.  
- La visualización del embudo facilita la identificación de las etapas críticas para optimizar la experiencia de usuario (UX/UI).  

---

## 👤 Autor
**Andrés Esquivel Díaz**  
📍 *Data Analyst | Python · SQL · Tableau · Power BI*  
🔗 [LinkedIn](https://www.linkedin.com/in/andres-esquivel-diaz-08691337) · [GitHub](https://github.com/aesquivel91)
