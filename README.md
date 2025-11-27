# 🔍 Trend Hunter - PCComponentes

Herramienta de análisis de tendencias de marcas en Google Trends para identificar oportunidades proactivas en el mercado de componentes tecnológicos.

## 🎯 Funcionalidades

- 📊 Análisis de tendencias de búsqueda (últimos 5 años)
- 📈 Cálculo de cambios porcentuales (mes, quarter, año)
- 🔍 Búsquedas relacionadas (TOP + RISING)
- 🏷️ Temas relacionados (TOP + RISING)
- 💾 Exportación de resultados a CSV
- 🌍 Análisis por país (actualmente: España)

## 🚀 Uso

### Online (Streamlit Cloud)

1. Accede a la app: [ENLACE_AQUÍ]
2. Sube tu CSV con marcas
3. Selecciona modo de análisis
4. ¡Analiza tendencias!

### Local

```bash
# Instalar dependencias
pip install -r requirements.txt

# Ejecutar app
streamlit run app.py
```

## 📋 Formato CSV

Tu archivo debe tener este formato:

```csv
Brand
ASUS
MSI
Gigabyte
Corsair
```

## 🔧 Configuración

### SerpAPI Key

La API key está configurada en el código. Para producción, se recomienda usar variables de entorno:

```python
import os
SERPAPI_KEY = os.getenv("SERPAPI_KEY")
```

### Países disponibles

Actualmente configurado para:
- 🇪🇸 España (ES)

Próximamente:
- 🇵🇹 Portugal (PT)
- 🇫🇷 Francia (FR)
- 🇮🇹 Italia (IT)
- 🇩🇪 Alemania (DE)

## 📊 Datos proporcionados

Para cada marca:

1. **Interest Over Time**: Gráfico de tendencia (5 años)
2. **Cambios %**:
   - Último mes
   - Último quarter
   - Último año
3. **Related Queries**: TOP 10 + RISING 10
4. **Related Topics**: TOP 10 + RISING 10

## ⚠️ Límites de la API

SerpAPI tiene límites de tasa:
- ~100 búsquedas/hora en plan gratuito
- Con 195 marcas, análisis completo tarda ~15-20 minutos
- Recomendación: Analizar en lotes de 20-30 marcas

## 🛠️ Stack Tecnológico

- **Frontend**: Streamlit
- **Visualización**: Plotly
- **Análisis**: Pandas
- **API**: SerpAPI (Google Trends)

## 📝 Roadmap

- [ ] Añadir más países
- [ ] Comparación entre países
- [ ] Dashboard con métricas consolidadas
- [ ] Integración con Google Sheets
- [ ] Alertas automáticas para marcas emergentes
- [ ] Análisis de estacionalidad

## 👨‍💻 Desarrollo

Desarrollado para PCComponentes por Pablo González.

---

**Powered by SerpAPI** 🔍
