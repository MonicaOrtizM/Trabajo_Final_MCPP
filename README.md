# Emprendimiento como Política Pública #

![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Word%20Art.png)

## Descripción del Proyecto y motivación: ##

En los últimos años, la línea de política pública ha concentrado sus esfuerzos en impulsar el emprendimiento, pues parece razonable pensar que más emprendedores crean nuevas empresas y estas nuevas empresas a su vez crean puestos de trabajo, intensifican la competencia e incluso pueden aumentar la productividad a través del cambio tecnológico y la innovación. Y lo anterior en conjunto puede generar un círculo virtuoso que impulsa el crecimiento de las regiones. 

En particular, el gobierno actual tiene como una de sus líneas de interés el emprendimiento, lo que, de acuerdo con el Plan Nacional de Desarrollo, “hará posible la transformación productiva que Colombia ha estado esperando y que permitirá reducir nuestra dependencia de la minería y de los hidrocarburos, aumentará la formalización laboral y empresarial y logrará un mayor aprovechamiento de las oportunidades que brindan los tratados de libre comercio.”

No obstante, en realidad pareciera no darse este resultado, pues el emprendimiento también usado como una salida de los individuos ante la imposibilidad de conseguir empleo y como forma de sustento/subsistencia deciden autoemplearse. Por lo que es posible preguntarse, si el emprendimiento en Colombia trae todos los beneficios que la línea de política ha estado enfatizando, o si más bien por su lado, el efecto ha sido sobreestimado. 

Es por ello que la intención de este proyecto es analizar cómo el emprendimiento ha sido discutido en los últimos 3 gobiernos y el actual, para luego contrastarlo con cifras del tejido empresarial y caracterizar los emprendimientos en Colombia en cinco dimensiones: 
1.	Dinámica de creación de empresas y tamaño de las mismas 
2.	Creación de empleo
3.	Sectores en los que se concentra 
4.	Regiones en las que más se crean empresas
5.	Supervivencia de los emprendimientos 


## Metodología ##

El análisis se realizó así: 
1.	Transformación de archivos PDF de los 4 planes nacionales de desarrollo: 
•	2006-2010: “Estado comunitario: desarrollo para todos”
•	2010-2014: “Prosperidad para todos”
•	2014-2018: “Todos por un nuevo país”
•	2018-2022: “Pacto por Colombia. Pacto por la equidad.”

Se extrajo el texto de cada uno de estos pdfs utilizando la librería de Python PyPdf2. Cada plan es un objeto de una lista.

2.	Limpieza del texto: Para cada Plan Nacional de Desarrollo ya convertido en formato texto. Este texto está en formato “bruto”, incluye saltos de línea, espacios, caracteres especiales que no son de interés para analizar. Para ello se dividen el texto en cadenas de palabras (“tokenization”). Para ello se utilizó la librería de Python NLTK. 

3.	Análisis de lenguaje: con la misma librería, se hizo análisis a través de diagramas de dispersión léxica utilizando palabras relacionadas al emprendimiento por Plan de Desarrollo, análisis de concordancia y similares. 

4. Unión de Planes: Dado que cada plan se encuentra en una lista diferente, se convierten en formato string para luego unirlos en su orden. A continuación, se realiza el análisis del punto 3. El código de los pasos 1-4 está ([aquí](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Trabajo%20Final_PND.zip)).

5.	Datos de extracción del RUES-PILA: con extracciones de las bases de datos para 2011-2018 en archivos cvs, se crean dataframes utilizando pandas en Python y se grafican. Con estos datos se hicieron gráficos más prolijos utilizando Tableau y un mapa en QGIS. El código se puede encontrar ([aquí](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Extracci%C3%B3n%20de%20Informaci%C3%B3n%20Empresarial.ipynb)). 

## ¿Qué encontré? ##

All code for analysis available here.
1. 	La palabra emprendimiento ha ido aumentando en su intensidad de uso, siendo 2018-2022 el periodo en el que se utilizó más. 

2. El emprendimiento se usa en contextos relacionados a innovación, vinculación laboral, productividad, generación de ingresos, acceso al financiamiento y fortalecimiento empresarial. 

3. Del análisis de “similar”, se encontró que ha evolucionado más la forma con la que se asocia el término, partiendo de un subprograma, estratégico a competitividad e investigación. 

4.	Al contrastar con el RUES-PILA se traducen los hallazgos anteriores a la identificación de 5 retos del emprendimiento. Cabe aclarar que estos hallazgos no son algo novedoso, sino que sigue la literatura y las recomendaciones de política que se han venido realizando dada la coyuntura. **Estos 5 retos más bien refuerzan lo ya encontrado**.

### Visualizaciones de los 5 retos: ###
1.	Creación de empresas vs. Tamaño 

![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Creaci%C3%B3n.png)

![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Tama%C3%B1o.png)
 
La mayoría de las empresas que se crean son microempresas. 
**Reto: Tipo de empresas sujetos de intervención.** 

2.	Tamaño de las empresas vs. Empleo 

 ![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Empleo.png)
 
Las microempresas son las que menos empleos formales generan. 
**Reto: Generación de empleo ≠ autoempleo**

3.	¿Dónde emprender?
 
El 80,1% de las empresas se crean en sectores de Comercio y Servicios
**Reto: Focalizar esfuerzos en sectores con creación de valor agregado**

 ![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Empleo.png)

4.	¿Dónde se concentra la creación de empresas?
La creación de empresas se concentra en: Bogotá, Antioquia, Valle, Cundinamarca y Santander. 
**Reto: Descentralización, regiones funcionales**

 ![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Mapa%20Colombia.PNG)

5.	Supervivencia de los emprendimientos (microempresas) 
 ![alt text](https://github.com/MonicaOrtizM/Trabajo_Final_MCPP/blob/master/Supervivencia%20Microempresas.png)
 
De cada 100 microempresas creadas, al cabo de 5 años sobreviven 34. **Reto: Apoyo en etapas tempranas (cumpliendo los 4 retos anteriores)**
