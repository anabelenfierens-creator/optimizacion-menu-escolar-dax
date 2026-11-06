# Optimización Nutricional y Análisis de Costos en Comedores Escolares (España) 

## Introducción

Este proyecto de Ciencia de Datos realiza un análisis comparativo y descriptivo entre un Menú Escolar Tradicional y una propuesta de Menú Alternativo en escuelas concertadas de España.
Utilizando un modelo de datos relacional y medidas en DAX (Power BI), se evalúa el costo por ración y el cumplimiento de los estándares nutricionales fijados por la AESAN (Agencia Española de Seguridad Alimentaria y Nutrición), la Estrategia NAOS y el Programa PERSEO.

## Tecnologías y Fuentes de Información

*	**Herramientas de Análisis**: Power BI (DAX), Microsoft Excel.
*	**Bases de Datos Nutricionales**: BEDCA (Base de Datos Española de Composición de los Alimentos) y AESAN.
*	**Bases de Costos**: Precios mayoristas de distribución para colectividades (Canal HORECA / MAPA) y estudios comparativos de la OCU.

## Arquitectura del Dataset (Modelo Relacional)

Los datos se encuentran organizados en 3 tablas relacionales vinculadas por ID_Ingrediente:
1.	**Tabla_Ingredientes**: Precios por kg/L y desglose macro-nutricional (Kcal, Proteínas, Grasas, Carbohidratos).
2.	**Tabla_Recetas_Menu**: Gramajes por ración (alumnos de 6 a 12 años) y rotación de menús lectivos (20 días).
3.	**Tabla_Requerimientos**: Parámetros oficiales de ingesta diaria recomendada (30-35% de la IDR en el almuerzo).
   
## Métricas DAX e Indicadores Clave (KPIs)

Se desarrollaron medidas iterativas para automatizar el cálculo por escenario:
*	**Costo_Total_Racion**: Evaluó la diferencia de precio entre el Menú Tradicional (€1,16) y el Menú Alternativo (€1,45).
* **Kcal_Total_Racion**: Evaluó el aporte energético en total de cada menú (341 kcal vs. 562,6 kcal).
*	**Proteinas_Total_Racion**: Midió la ingesta proteica por ración (Menú tradicional 25,4 g vs. Menú alternativo 58,6 g).

## Conclusiones

1.	**Impacto Económico**: El menú alternativo representa un incremento de 0,29 € por ración debido a la selección de materias primas magras y pescados en el canal mayorista.
2.	**Validación Nutricional**: El menú alternativo cumple óptimamente el rango calórico de la Estrategia NAOS (30-35% IDR) y se excede con el aporte de proteínas, mientras que el tradicional resulta deficitario.
3.	**Crítica Metodológica**: Se identificó una desviación hiperproteica (58,6 g) en el escenario alternativo, demostrando clínicamente que el modelo lineal requiere incorporar restricciones de "techo proteico" en futuras iteraciones.
   
## Enlaces

*	[DATASET EXCEL] https://docs.google.com/spreadsheets/d/169qnviPLi7rLBFSgRTfAb6KR8r9lA_nq/edit?usp=sharing&ouid=113044224735481592742&rtpof=true&sd=true
*	[TABLERO INTERACTIVO]
https://drive.google.com/file/d/1jx74HxxYQZplLUG7icThdoye-T8BTT1J/view?usp=sharing

•	🎥 Video Demostrativo del Tablero (Pendiente de agregar enlace)
•	📄 Reporte Técnico Consolidado: PROYECTO_FINAL_DATA_SCIENCE.pdf

**Autora: Ana Belén Fierens Bayo**
**Técnica Superior en Dietética & Estudiante de Ciencia de Datos e IA** 
