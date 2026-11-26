<div align="center">

![Ingeniería De Datos](https://img.shields.io/badge/INGENIER%C3%8DA_DE_DATOS-EF6C00?style=for-the-badge)

# Web scraping del registro de la flota pesquera

Extracción automatizada de los registros europeo y español de buques pesqueros con Selenium, Requests y BeautifulSoup, para construir un conjunto de datos de la flota española.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white) ![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4B8BBE?style=flat-square) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

</div>

---

## Descripción general

Los datos técnicos de cada buque están repartidos entre el registro de la flota de la Unión Europea (Fleet Register) y el registro nacional español, y solo se pueden consultar página a página. Este proyecto automatiza la navegación por ambos sitios y reúne la información en un CSV.

Es la primera fase de la serie sobre la flota pesquera, que continúa en [ml-flota-pesquera](https://github.com/JulioUQ/ml-flota-pesquera) y [app-dashboard-flota-pesquera](https://github.com/JulioUQ/app-dashboard-flota-pesquera).

## Funcionalidades

- Navegación automática por el buscador europeo: selección de país y tipo de buque, 100 resultados por página y recorrido de todas las páginas.
- Extracción de la lista de identificadores CFR de los buques españoles.
- Consulta de cada CFR en el registro español y construcción de un DataFrame con los datos técnicos.
- Exportación a CSV del resultado.

## Tecnologías y herramientas

| Ámbito | Herramientas |
| --- | --- |
| Navegación | Selenium |
| Peticiones y parseo | Requests, BeautifulSoup |
| Datos | pandas |

## Estructura del proyecto

```text
.
├── 1. Scripts/
│   ├── src/                # main.py, scrapping_fleet_EU.py, scrapping_fleet_ESP.py
│   └── notebook/           # Versión en cuaderno del proceso
├── 4. Solucion/
│   ├── data/               # CSV resultantes
│   └── memoria/            # Memoria del proyecto (PDF)
├── 0. Teoria/  ·  5. Literatura/  ·  6. Figura y graficos/
├── LICENSE.txt
└── requirements.txt
```

## Instalación y uso

```bash
pip install -r requirements.txt
cd "1. Scripts/src"
python main.py
```

En macOS, para ocultar los avisos de Qt: `QT_LOGGING_RULES="*.debug=false" python main.py`.

## Resultados

- [Caso de estudio en el portfolio](https://juliouq.github.io/Portfolio-Web---JulioUQ/es/casos/web-scraping-flota/): proceso, decisiones y publicación del conjunto de datos.

## Aspectos técnicos destacados

- Combinación de Selenium (sitio dinámico) y Requests con BeautifulSoup (fichas estáticas), cada uno donde rinde mejor.
- Paginación completa y escritura incremental de resultados.
- Proyecto en equipo con Lucas Zamora Vera; la memoria documenta el proceso.

## Autor

**Julio Úbeda Quesada** · Data Scientist

[![Portfolio](https://img.shields.io/badge/Portfolio-0B2545?style=flat-square&logo=astro&logoColor=white)](https://juliouq.github.io/Portfolio-Web---JulioUQ/es/) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/juliouq/) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/JulioUQ)

<sub>El conjunto de datos se distribuye con licencia Creative Commons Atribución-NoComercial 4.0 (ver LICENSE.txt). Proyecto realizado en el Máster Universitario en Ciencia de Datos.</sub>
