# 📘 **Descripción del Dataset de Especies Terrestres en Riesgo de Extinción**

En esta experiencia, trabajaremos con un dataset que contiene datos ecológicos, biológicos y geográficos sobre diversas especies terrestres. El objetivo es **clasificar el riesgo de extinción** de estas especies en categorías definidas por la **UICN** (Unión Internacional para la Conservación de la Naturaleza), utilizando una variedad de rasgos morfológicos y ambientales.

En este análisis, las especies se clasifican en **categorías de amenaza** que incluyen:  
- **En Peligro**
- **No en Peligro**

### **Transformación de la columna `Status`**:

La columna **`Status`** originalmente contenía las siguientes categorías: **LC**, **NT**, **VU**, **EN**, **CR**, **EW**, **EX**. Para simplificar la clasificación en el modelo predictivo, estas categorías se redujeron a **dos clases**:

- **En Peligro (1)**: Incluye las especies clasificadas como **VU (Vulnerable)**, **EN (En Peligro)**, **CR (En Peligro Crítico)**, **EW (Extinta en la Naturaleza)**, **EX (Extinta)**.
- **No en Peligro (0)**: Incluye las especies clasificadas como **LC (Preocupación Menor)**, **NT (Casi Amenazada)**.


### **Descripción de los atributos:**

| **Atributo**                   | **Tipo**        | **Unidades / Valores**   | **Descripción**                                                                                           |
|---------------------------------|-----------------|--------------------------|-----------------------------------------------------------------------------------------------------------|
| **Group**                       | Categórico      | Mamíferos, Aves, etc.     | Grupo taxonómico de la especie (e.g., Mamíferos, Aves, Reptiles).                                         |
| **Kingdom**                     | Categórico      | Animalia                 | Reino taxonómico (siempre Animalia en este caso).                                                           |
| **Phylum**                      | Categórico      | Chordata, Arthropoda      | Filo al que pertenece la especie.                                                                          |
| **Class**                       | Categórico      | Mamíferos, Aves, etc.     | Clase taxonómica.                                                                                         |
| **Order**                       | Categórico      | Primates, Carnivora      | Orden taxonómico de la especie.                                                                            |
| **Family**                      | Categórico      | Felidae, Canidae         | Familia biológica de la especie.                                                                           |
| **Genus**                       | Categórico      | Panthera, Canis          | Género taxonómico.                                                                                         |
| **IUCNName**                    | Categórico      | Nombre científico        | Nombre científico según la UICN.                                                                           |
| **NCBIName**                    | Categórico      | Nombre genético          | Nombre de la especie en la base de datos NCBI.                                                             |
| **Status**                      | Categórico      | LC, VU, EN, CR           | Estado de amenaza según la UICN (Preocupación Menor, Vulnerable, En Peligro, En Peligro Crítico, etc.).     |
| **CRITERIA**                    | Categórico      | A2cd, B1ab, etc.         | Criterios usados para clasificar la amenaza según la UICN.                                                 |
| **YEAR_PUB**                    | Numérico        | Año                      | Año de publicación de la evaluación UICN para la especie.                                                   |
| **Realm**                       | Categórico      | Neotropical, Afrotropical | Región biogeográfica global donde vive la especie.                                                        |
| **IUCN_THREATS_CATEG**          | Categórico      | Pérdida de hábitat, caza  | Categoría de amenaza UICN (e.g., pérdida de hábitat, caza ilegal, cambio climático).                     |
| **IUCN_N_THREATS**              | Numérico        | Número de amenazas       | Número de amenazas identificadas para la especie.                                                         |
| **BODY_SIZE**                   | Numérico        | Kilogramos (kg)          | Tamaño corporal de la especie (en kg o gramos).                                                           |
| **OFFSPRING_SIZE**              | Numérico        | Número de crías          | Número promedio de crías por ciclo reproductivo.                                                          |
| **FECUNDITY**                   | Numérico        | Crías por año            | Tasa de reproducción anual o número de crías por año.                                                     |
| **GENERATION_LENGTH**           | Numérico        | Años                     | Tiempo promedio entre generaciones.                                                                       |
| **DIET_BREADTH**                | Numérico        | Valor entre 0 y 1        | Amplitud de la dieta de la especie: cuántos tipos de alimentos consume (e.g., 0 = dieta muy específica).  |
| **TROPHIC_LEVEL**               | Numérico        | Valor entre 1 y 4        | Nivel trófico de la especie (Herbívoro = 1, Omnívoro = 2, Carnívoro = 3, etc.).                          |
| **DISPERSAL_ABILITY**           | Numérico        | Valor entre 0 y 1        | Capacidad de dispersión o movilidad de la especie.                                                        |
| **MICROHABITAT**                | Categórico      | Terrestre, Acuático       | Tipo de microhábitat en el que habita la especie (e.g., terrestre, acuático).                             |
| **HABITAT_BREADTH**             | Numérico        | Valor entre 0 y 1        | Amplitud del hábitat: cuántos tipos de hábitats ocupa la especie.                                          |
| **ALTITUDE_MIN**                | Numérico        | Metros (m.s.n.m.)        | Altitud mínima en el rango geográfico donde se encuentra la especie.                                       |
| **ALTITUDE_MAX**                | Numérico        | Metros (m.s.n.m.)        | Altitud máxima en el rango geográfico donde se encuentra la especie.                                       |
| **GEOGRAPHICAL_RANGE_SIZE**     | Numérico        | Kilómetros cuadrados     | Tamaño total del rango geográfico de la especie.                                                          |
| **HUMAN_FOOTPRINT**             | Numérico        | Índice (0-100)          | Índice de impacto humano en el hábitat de la especie.                                                     |
| **HABITAT_CONVERSION**          | Numérico        | Porcentaje (%)           | Porcentaje de hábitat convertido en áreas urbanas, agrícolas, etc.                                         |
| **Latitud**                     | Numérico        | Grados                   | Coordenada geográfica de latitud donde se encuentra la especie.                                            |
| **Longitud**                    | Numérico        | Grados                   | Coordenada geográfica de longitud donde se encuentra la especie.                                           |
| **Índice de pobreza**           | Numérico        | Valor numérico           | Índice socioeconómico de la región donde habita la especie (más alto = más pobreza).                     |
| **Contaminación aire**    | Numérico        | AQI (valor 0-500)        | Calidad del aire (AQI) en la región donde habita la especie.                                               |
| **Altitud**          | Numérico        | Metros                   | Altitud de la localización geográfica de la especie en metros sobre el nivel del mar.                     |
| **Uso del suelo**               | Categórico      | Urbano, Bosque, Agrícola  | Tipo de uso del suelo en el área donde habita la especie (urbano, agrícola, bosque, etc.).                |

---
