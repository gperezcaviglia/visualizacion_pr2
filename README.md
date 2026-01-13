 Más allá de Harvard

**Lo que las películas no muestran del sistema universitario estadounidense**

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![D3.js](https://img.shields.io/badge/D3.js-v7-orange.svg)](https://d3js.org/)
[![R](https://img.shields.io/badge/R-4.x-blue.svg)](https://www.r-project.org/)

---

## Visualización en línea

**URL:** [https://gperezcaviglia.com/visualizacion_pr2/](https://gperezcaviglia.com/visualizacion_pr2/)

---

## Descripción del proyecto

Visualización interactiva tipo *scrollytelling* que analiza las desigualdades estructurales en el sistema de educación superior estadounidense. A través de cuatro dimensiones (costo, retorno, género y raza), el proyecto revela patrones que contradicen la narrativa del "sueño americano" universitario.

---

## Conjunto de datos

| Característica | Detalle |
|----------------|---------|
| **Fuente** | [U.S. Department of Education - College Scorecard](https://collegescorecard.ed.gov/data/) |
| **Instituciones analizadas** | 6,429 |
| **Variables seleccionadas** | 24 (de 3,567 disponibles) |
| **Tipos de institución** | Públicas, Privadas sin lucro, Privadas con lucro |
| **Fecha de datos** | Noviembre 2025 |

### Preparación de datos

El dataset original fue procesado en R para:
- Filtrar instituciones con datos completos
- Calcular métricas derivadas (retorno de inversión, brechas de género y raza)
- Estandarizar categorías institucionales

---

## Preguntas de investigación

| Dimensión | Pregunta | Hallazgo principal |
|-----------|----------|-------------------|
| **Costo** | ¿Cuánto cuesta realmente cada tipo de institución? | Privadas sin lucro: $44,773/año (2.5x más que públicas) |
| **Retorno** | ¿La inversión se traduce en mejores ingresos? | Públicas: 5.4x retorno vs Privadas: 3.7x |
| **Género** | ¿Existe brecha de género en la deuda estudiantil? | Las mujeres se endeudan hasta 9.7% más que los hombres |
| **Raza** | ¿Hay disparidades raciales en tasas de graduación? | 15 puntos porcentuales de brecha (blancos vs afrodescendientes) |

---

## Tecnologías utilizadas

### Análisis de datos
- **R / RStudio** - Análisis estadístico y exploratorio
- **tidyverse** - Manipulación de datos
- **ggplot2** - Visualizaciones exploratorias
- **scales, kableExtra** - Formateo y tablas

### Visualización web
- **D3.js v7** - Gráficos interactivos y bindeo de datos
- **HTML5 / CSS3** - Estructura y estilos responsivos
- **JavaScript ES6** - Lógica de interacción
- **CSS Custom Properties** - Sistema de diseño consistente

### Técnicas de visualización
- Scrollytelling con observadores de intersección
- Gráficos: Lollipop, Dot plot, Dumbbell chart, Barras agrupadas
- Animaciones con transiciones D3
- Tooltips interactivos

---

## Estructura del repositorio

```
visualizacion_pr2/
│
├── index.html                        # Visualización principal (archivo único)
├── college_scorecard_analisis.Rmd    # Análisis completo en R (documentado)
├── README.md                         # Este archivo
└── LICENSE                           # CC BY-SA 4.0
```

---

## Ejecución local

### Opción 1: Servidor local simple

```bash
# Clonar el repositorio
git clone https://github.com/gperezcaviglia/visualizacion_pr2.git
cd visualizacion_pr2

# Iniciar servidor local (elegir una opción)
python3 -m http.server 8000
# o
npx serve .

# Abrir en navegador
# http://localhost:8000
```

### Opción 2: Abrir directamente

El archivo `index.html` puede abrirse directamente en cualquier navegador moderno, ya que todas las dependencias se cargan desde CDNs públicos.

### Opción 3: Reproducir análisis R

```r
# Instalar dependencias
install.packages(c("tidyverse", "scales", "knitr", "kableExtra", "skimr"))

# Ejecutar análisis
rmarkdown::render("college_scorecard_analisis.Rmd")
```

---

## Interactividad

La visualización incluye los siguientes elementos interactivos:

- **Scroll narrativo**: Los gráficos se revelan progresivamente mientras el usuario navega
- **Tooltips**: Información detallada al pasar el cursor sobre elementos
- **Animaciones**: Transiciones suaves que guían la atención del usuario
- **Diseño responsivo**: Adaptación a diferentes tamaños de pantalla

### Accesibilidad

- Contraste de colores WCAG AA
- Textos alternativos en elementos visuales
- Navegación posible con teclado
- Fuentes legibles y escalables

---

## Referencias teóricas (entre otras)

- Bourdieu, P. & Passeron, J.C. (1977). *Reproduction in Education, Society and Culture*. Sage Publications.
- Bowles, S. & Gintis, H. (1976). *Schooling in Capitalist America*. Basic Books.
- AAUW (2023). *Deeper in Debt: Women and Student Loans*.
- Scott-Clayton, J. & Li, J. (2016). *Black-white disparity in student loan debt more than triples after graduation*. Brookings Institution.

---

## Autora

**Gabriela Pérez Caviglia**

Máster en Ciencia de Datos  
Universitat Oberta de Catalunya (UOC)  
Asignatura: Visualización de Datos  
Enero 2026

---

## Licencia

Este proyecto está licenciado bajo [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

Usted es libre de:
- **Compartir**: copiar y redistribuir el material en cualquier medio o formato
- **Adaptar**: remezclar, transformar y construir a partir del material

Bajo los siguientes términos:
- **Atribución**: Debe dar crédito apropiado
- **CompartirIgual**: Si remezcla o transforma, debe distribuir bajo la misma licencia

---
