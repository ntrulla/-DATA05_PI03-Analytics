![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

# **PROYECTO INDIVIDUAL Nº3**

# <h1 align="center">**`Telecomunicaciones`**</h1>

¡Bienvenidos!  En esta ocasión, como ***Data Analyst*** realice un **análisis** completo que me permitió reconocer el comportamiento del sector a nivel nacional.

   <img src = 'https://user-images.githubusercontent.com/100374777/210778208-be2b22e0-105b-4eb8-93b8-98ae197cbdad.jpeg' height = 500>


### **Introducción**

La actual explosión tecnológica posibilitada por el procesamiento on line y casi simultaneo de millones de datos, solo es posible por el desarrollo de las telecomunicaciones. El desafío de mantener la tendencia de crecimiento en la transmisión de gigantescos volúmenes de datos, esta soportado por la infraestructura de las Telcos, y sus posibilidades reales de inversión.
En un entorno complejo en que las redes atraviesan un proceso que las convierte en un comodity, a la vez que la rentabilidad se traslada a empresas generadoras de contenidos, apareció la pandemia y su contexto de cuarentena. Esto ocasionó un incremento exponencial en el uso de las redes haciendo que los usuarios estén muchas más horas conectados, demandando mayor calidad de servicio. Acompañando la tendencia mundial que estima un adelanto entre 5 y 10 años en la adopción masiva de tecnologías (Plataformas de educación, reuniones a distancia, tramites on-line, comercio electrónico).
Esta nueva realidad obliga a pensar en términos de bienestar digital y a convertir el acceso a Internet en un Servicio Público Esencial, en coincidencia con la visión del Gobierno Nacional, que hace varios años tiene como objetivo mejorar la calidad de los servicios y las redes de telecomunicaciones en todo el territorio nacional. Adoptándolo como política de estado en las diferentes gestiones, e impulsando medidas orientadas a maximizar la eficiencia en la utilización de los recursos destinados a la prestación de Servicios de Tecnologías de la Información y las Comunicaciones. El sector privado tiene un rol clave y una participación fundamental, no solo por su infraestructura y capacidad de gestión, sino también porque es el que interactúa con millones de usuarios.
El despliegue de infraestructura es condición necesaria (aunque no suficiente), para el desarrollo de industrias de alto contenido tecnológico que promueva la diversificación productiva y la difusión de saberes, influyendo cotidianamente en los habitantes, los negocios y las empresas.
Aunque Argentina está a la vanguardia del desarrollo de las telecomunicaciones, teniendo para el 2020 un total de [62,12 millones conexiones](https://www.datosmundial.com/america/argentina/telecomunicacion.php) aún queda mucho trabajo por hacer!

### **Objetivo del análisis**

El objeto de este trabajo es analizar brevemente la evolución del mercado, sus procesos de transformación, la estructura de su situación actual, tratando de comprender el impacto generado por la pandemia, describir el estado de la industria pos pandemia y proyectar los principales desafíos que se plantean en el futuro cercano, en torno a las redes necesarias y su impacto en la sociedad. Para poder logarlo, vamos a:

•	Evaluar la evolución del acceso a Internet fijo desde el 2014 hasta el 2022 por trimestre y por provincia, investigando si efectivamente la Pandemia produjo un crecimiento en la utilización de Internet.
•	Comparar la velocidad del acceso a internet fijo de cada provincia para realizar una mejor distribución del acceso a internet según la velocidad categorizada por rangos.
•	Evaluar la evolución del tipo de tecnología se sigue utilizando en cada provincia, para saber dónde seguir extendiendo la red de fibra óptica (REFEFO) y así poder llegar a más hogares.
•	Determinar cuáles son las provincias con menor velocidad de bajada de Internet con el fin de poder aumentar la calidad del servicio y cubrir las necesidades de los usuarios.


## **Análisis exploratorio de los datos y transformaciones (EDA)**

Descargué los datos proporcionados por la plataforma del Enacom a través de la API directamente a Power Bi para realizar al instante la transformación necesaria con Power Query de las tablas que seleccioné con información entre los años 2014 y 2022:

	Acceso a Internet fijo por rango de velocidad por provincia
	Acceso a Internet fijo por tecnología y provincia
	Acceso a Internet, cada 100 hogares por provincia  
	Velocidad media de bajada por provincia

En las tablas identifiqué datos faltantes, inconsistentes y errores que fueron subsanados siguiendo los siguientes criterios:

1.	Acceso a Internet fijo por rango de velocidad por provincia 

	Encabezados Promovidos (los títulos se encontraban en la primera fila)
	Cambio del tipo de dato a tipo numérico de las columnas con Mbps
	Agregado de una columna personalizada con la fecha por año y trimestre (Query utilizada:"1/"&Number.ToText([Trimestre]*2+([Trimestre]-2))&"/"&Number.ToText([Año])]).

2.	Acceso a Internet fijo por tecnología y provincia 

	Encabezados Promovidos (los títulos se encontraban en la primera fila)
	Cambio del tipo de dato a tipo numérico
	Errores quitados y reemplazados de la columna año y trimestre.
	Agregado de una columna personalizada con la fecha por año y trimestre.

3.	Acceso a Internet, cada 100 hogares por provincia 

	Encabezados Promovidos (los títulos se encontraban en la primera fila)
	Cambio del tipo de dato a tipo numérico
	Agregado de una columna personalizada con la fecha por año y trimestre.

4.	Velocidad media de bajada por provincia

	Encabezados Promovidos (los títulos se encontraban en la primera fila)
	Cambio del tipo de dato a tipo numérico
	Agregado de una columna personalizada con la fecha por año y trimestre.

KPI´s

	Variación porcentual trimestral del acceso al servicio de internet, cada 100 hogares por provincia.
	Variación porcentual trimestral del acceso a Fibra Óptica por provincia.
	Variación porcentual trimestral de la velocidad de bajada + 30 Mbps por provincia.
	Promedio o velocidad media de bajada por provincia.

Elección de los gráficos

Gráfico de líneas: Fueron seleccionados para el análisis de la evolución de los datos en el paso del tiempo, así como para realizar una comparación entre los distintos ítems:
	Suma de Accesos por cada 100 hogares por año y trimestre.
	Accesos a Internet fijo por tecnología y provincia por año y trimestre.
	Tecnologías usadas en cada provincia.

Gráfico de Barras: Utilizado para ver el acceso a internet fijo por rango de velocidad de bajada y por provincia y así poder comparar las distintas tecnologías.

Mapa de Argentina: Se importó un mapa externo de Argentina con extensión .Json con el objetivo de visualizar geográficamente los datos por provincia analizados en todas las tablas.

Segmentación de datos: Todos los gráficos están filtrados por año, trimestre.

Tarjetas: Para el armado de los KPI´s.

### **Conclusiones**

El acceso a Internet fijo, ha aumentado progresivamente desde el año 2014 y se ha acrecentado especialmente en los últimos años. De todas formas, la pandemia del COVID-19 puso en relieve la importancia que tienen las redes de telecomunicaciones ya que contrarrestaron los efectos del aislamiento, difundieron y administraron las medidas de cuidado, posibilitaron la continuidad laboral, facilitaron el funcionamiento económico y dieron soporte al funcionamiento del estado.
Aunque la penetración de Internet fijo por cada 100 hogares fue en aumento, según el análisis realizado, en algunas provincias como: Buenos Aires, Córdoba, San Luis, La Pampa y Rio Negro. Entre los promedios más bajos se encuentran Formosa, La Rioja, Jujuy, Santa Cruz, Tierra del Fuego Y Santiago del Estero. Aún sigue siendo dispar la situación de las provincias en Argentina. Facilitar el acceso a internet en estas regiones, así como también mejorar la velocidad de bajada (es decir la calidad de internet) para que el servicio sea mejor en todo el país es una oportunidad para la empresa.
Si bien el gobierno conjunto con las empresas privadas están actualizando las placas de la Red Federal de Fibra Óptica. Argentina tiene un mercado de banda ancha con predominio del cable módem, con un crecimiento importante en fibra óptica. Durante el año 2020, la tendencia respecto a las tecnologías de acceso se mantuvo en línea con los años anteriores. En el primer trimestre del 2020 se registró una contracción en accesos ADSL en favor de una expansión de la fibra óptica. Esto va a permitir conectar a todos los hogares de forma más robusta y estable. 
Por último, queremos destacar los beneficios que tienen las organizaciones si se mantienen en la vanguardia: aumenta la eficiencia y productividad, mejora comunicación y relaciones con los usuarios, ya que las ofertas se pueden personalizar y generar un valor agregado. Las consecuencias de no mantenerse al día con la tecnología son perjudiciales ya que se puede perder la ventaja competitiva y las oportunidades de mejora. 

¡Así que los invitamos a quedarse y seguir avanzado en los tiempos actuales!






