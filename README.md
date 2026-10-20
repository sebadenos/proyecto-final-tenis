# Optimización de calendario y maximización de puntos ATP para tenistas profesionales argentinos

Proyecto Final · Licenciatura en Ciencia de Datos · Universidad CAECE  
Autor: Sebastian Losinno

El proyecto estima la probabilidad de victoria de cada partido con modelos de aprendizaje automático, la traduce a puntos ATP esperados con una simulación de Monte Carlo de los cuadros y recomienda el calendario de torneos que maximiza esos puntos para los jugadores argentinos de ranking 100–300.

## Notebooks

| Notebook | Contenido | Abrir |
|---|---|---|
| `01_EDA_y_preparacion.ipynb` | Ingesta, calidad del dato, EDA, Elo, baselines, decisión Go/No-Go, objetivos de desempeño y tablas de torneos, puntos, países y calendario 2026 | [Abrir en Colab](https://colab.research.google.com/github/sebadenos/proyecto-final-tenis/blob/main/notebooks/01_EDA_y_preparacion.ipynb) |
| `02_Modelado_y_simulacion.ipynb` | Atributos, modelos, evaluación, simulación de Monte Carlo y optimización del calendario | [Abrir en Colab](https://colab.research.google.com/github/sebadenos/proyecto-final-tenis/blob/main/notebooks/02_Modelado_y_simulacion.ipynb) |

Las dos notebooks corren de principio a fin en Google Colab y descargan sus insumos de este repositorio. Para ejecutarlas sobre una copia local, clonar el repositorio y asignar a `URL_REPO` la ruta de la carpeta.

## Datos

| Archivo | Contenido | Fuente |
|---|---|---|
| `data/raw/tennismylife_2026-10-19.zip` | Partidos ATP, Challenger y Qualy ATP, 2000–2026 (un CSV por circuito y temporada) | [TennisMyLife](https://stats.tennismylife.org), licencia MIT. Copia descargada el 19/10/2026 |
| `data/externos/atp_calendario_tour.json` y `atp_calendario_challenger.json` | Calendario 2026 de los circuitos ATP y Challenger: fechas, categoría, superficie, cuadro y país | [atptour.com](https://www.atptour.com), descargado el 19/10/2026 |
| `data/externos/tablas_torneos_puntos.xlsx` | Tablas de torneos (país y categoría), puntos por ronda y países (código IOC y región) | Elaboración propia a partir de la base, atptour.com y el Reglamento ATP 2026 |
| `data/procesados/` | Salidas de la notebook 01 que usa la notebook 02 | Generado por `01_EDA_y_preparacion.ipynb` |

La fuente de partidos se actualiza a diario y corrige datos históricos, por eso el análisis usa una copia fija con fecha de corte.
