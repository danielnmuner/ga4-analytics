# GA4-Analytics
![google](https://i0.wp.com/www.lalmendrodesign.com/wp-content/uploads/2021/03/Google-Analytics-Logo.png?fit=3636%2C2000&ssl=1)

Notes Learning Program about GA4 

- [x] [Introduccion](#introduccion)


### Introduccion

### ¿Que es GA4?
Es una herramienta para analizar tendencias de los que los usuarios hacen con sus dispositivos digitales. Captura interaciones y los almacena como Big Data. Dependiendo del departamento de la empresa habran diferentes intereses en las consultas realizadas a GA4

- **Marketing**: Grupos de anuncios, sesiones, conversiones para aumentar el proceso de captacion y reducir los costos durante el funnel de conversion para optimizar los procesos. 
- **SEO**: Sesiones, conversiones y tipo de trafico.
- **UX & Usabilidad**: Como son los flujos de los usuarios y como reaccionan frente a diferentes experiencias visuales.
- **IT**: Pueden evaluar cambios del flujo de usuarios y busquedas respecto a cambios tecnicos como velocidad, procesamiento, etc.
- **Alternativas a GA4**: Adobe Analytics, mixpanel, kissmetrics, cloudfare, gosquare y woopra.

### Informes de Vision General de Audiencia
---
- **Vision Genral de Audiencia**: #Usuarios, paginas visitadas en cada sesion, duracion media de las sesiones y el porcentaje de rebote. 
  - **Selector de periodos**: Periodo en el que queremos analizar el informe
  - **Selector de segmentos** Defaul(Todos los Usuarios): Permite filtrar los datos y realizar comparaciones.

![image](https://user-images.githubusercontent.com/60556632/169178745-13b8133e-363f-421f-9e6d-cd2df4a54c7e.png)
  - **Grafico de Lineas**: Muestra el numero de usuarios para un periodo y segmento dado.
  - **Selector de Intervalos**: Permite consultar los datos en periodos de tiempo mas detallados

![image](https://user-images.githubusercontent.com/60556632/169178961-5bae282c-80fb-4ace-a261-9e71f62da355.png)

  - **Selector de Metricas**:

![image](https://user-images.githubusercontent.com/60556632/169179105-dd0173d6-36a8-4b00-8595-1cfc0e4a8419.png)
  - **Anotador de Graficos**: Se encuentra en la parte inferior del grafico y nos permite crear notas para aclarar el contexto de los datos.
  - **Algunas metricas default**:

    - _Sesiones_: #Total de sesiones registradas.
    - _Ususarios_: Usuarios que han iniciado al menos una sesion.
    - _# de Paginas vistas_: Vistas incluso repetidas de las paginas con codigo de seguimiento.
    - _Pagina Sesion_: Promedio de paginas viscas en cada sesion incluso repetidas
    - _Duracion media de la sesion_: Duracion media de las sesiones
    - _Porcentaje de Rebote_: % de usuarios que abandonaron el sitio web despues de ver una sola pagina sin realizar ninguna accion.
    - _Datos demograficos_: Idioma, pais y cuidad.
  - **Algunas dimensiones default**:
    - _D. Datos demograficos_: Idioma, pais y cuidad.
    - _Dimensiones de Sistema_: Navegador, sistema operativo y proveedor de servicios.
    - _D. Dispositivos Moviles_: Sistema operativo y resolucion de pantalla.

- **Dimensiones y Metricas** [UA Dimensions & Metrics Explorer](https://ga-dev-tools.web.app/dimensions-metrics-explorer/)
  - Las **dimensiones** son atributos de los datos. Por ejemplo, la dimensión Ciudad indica la ciudad (como "Madrid" o "Nueva York") desde la que se origina una sesión. La dimensión Página indica la URL de una página vista.
  - Las **métricas** son dimensiones cuantitativas. La métrica Sesiones es el número total de sesiones. La métrica Páginas / sesión es el número medio de páginas vistas por sesión. [Documentacion](https://support.google.com/analytics/answer/1033861?hl=es#ValidDimensionMetricCombinations&zippy=%2Cen-este-art%C3%ADculo)

El informe default es `Audiencia` y en la parte inferior podemos encontrar la opcion `ver todo el informe` al seleccionar esta opcion se mostrara una tabla con datos relevantes de los informes de **Adquisicion**, **Comportamiento** y **Conversiones** sobre esta tabla tendremos la opcion de anadir `Dimension Secundaria` para añadir dimensiones. Ademas la opcion explorar cuenta con plantillas de dimensiones y metricas predeterminadas (Resumen - Uso del sitio - Conjunto de objetivos 1 - Comercio electrónico) y con la posibilidad de crear nuevas.


![image](https://user-images.githubusercontent.com/60556632/169194151-b6d449a7-3cc5-44bf-9d0e-da78d18d0a0d.png)

En la barra de busqueda podemos ser mas especifico con la dimension o por ejemplo a nievel de pais indicar ¿Cual?, ademas hay un conjunto de **graficos** donde indicamos la metrica y el grafico a usar para representarla. 

### Aclaracion de algunos terminos

> **Usuarios**: En condiciones normales es igual a la cantidad de dispositivos y no a la cantidad de personas. Una persona puede haberse conectado con 3 dispositivos personales diferentes luego GA4 cuenta 3 Usuarios en vez de uno. Incluso como incognito seria otro usuario.
> **Total Usuarios**: No es igual a la suma de usuarios puesto que la suma de usuarios tiene en cuenta usuarios recurrentes no solo nuevos. 
![image](https://user-images.githubusercontent.com/60556632/169399678-cc654608-3ddf-4506-8eb6-43607678a15e.png)

> **Tipo de usuarios** Esto nos permite entender porque no podemos decir que los usuarios totales es la suma de `usuarios nuevos + usuarios recurrentes`. La razon es porque para un periodo determinado el usuario nuevo se puede volver recurrente varias veces.

![image](https://user-images.githubusercontent.com/60556632/169401782-6a8d9f31-690d-486d-b722-2e9b379d243f.png)

> **Sesiones**: Es diferente a la interaccion entre paginas pero esta realacionado al tiempo de permanencia. En la siguiente _figura_ se observa cuantos intervalos de 30 min de permanencia se generaron durante las interacciones del usuario. 

![image](https://user-images.githubusercontent.com/60556632/169402329-8397e13e-6731-40ce-98a5-045895bf6974.png)

> **Visitas a paginas** Es igual a la cantidad total de paginas vistas incluso a quellas que se repitieron para tratar de acceder a otras. Esto se puede evitar usando la metrica de **paginas vistas unicas**.
> **Duracion media de la sesion**: Se calcula la diferencia de tiempo entre paginas sin embargo, esto no se puede realizar con la ultima pagina por lo cual GA4 asume no interactuo con la pagina. Para resolver esto se requiere codigo adicional donde se puede usar el scroll como referencia para saber cuanto tiempo duro el usuario en la pagina. 

![image](https://user-images.githubusercontent.com/60556632/169404454-839e1967-5d84-4f72-956c-28c0452f7079.png)

> **Porcentaje de Rebote**: Es importante tenerlo en cuenta cuando hay un volumen considelable de datos cuando conocemos la fuente y el contenido de la pagina de lo contrario podria guiar a malas interpretaciones.

![image](https://user-images.githubusercontent.com/60556632/169405510-41520148-2e89-498d-8d91-e6278ddb54c8.png)

### Cómo compartir informes
---
En cuanto hemos encontrado datos significativos podemos:  
![image](https://user-images.githubusercontent.com/60556632/169195247-19b567af-9e1a-4bc8-97a8-c6ef4c9c16a8.png)

- Para crear informes usamos la pestaña **Personalizacion** -> Panel(Dashboard) y luego lo creamos le damos un nombre ademas podemos **Añadir un widget** donde indicamos la metrica a usar y el tipo de grafico. Por cada vista podemos tener 20 Dashboards privados y 50 Dashboards publicos. 


### Informes Basicos

**Informes Audiencia**
Los [informes Audiencia](https://support.google.com/analytics/answer/1012034?hl=es#zippy=%2Csecciones-de-este-art%C3%ADculo) le ofrecen información valiosa sobre las características de su audiencia.

- **Usuarios activos**: En este informe podemos ver cuántos usuarios han estado activo en el rango de fecha que hayamos seleccionado. Útil para comparar el tipo de tráfico y que porcentaje de los usuarios totales supone.

- **Información geográfica**: En este apartado veremos la ubicación y el idioma que usan los usuarios que acceden a nuestra web. Esto es muy útil para analizar si nos interesaría ampliar nuestro público objetivo y traducir nuestro sitio a los idiomas más usados por nuestros usuarios.

- **Flujo de usuarios**: Este informe es muy importante ya que nos enseña en forma de mapa el flujo que han tenido los usuarios en nuestro sitio web, la página de destino y todas las interacciones que van haciendo y el sitio en el que van abandonando la web. Es útil para analizar las páginas con más abandonos, y saber si hay algún problema en ellas, o analizar el tipo de contenido que hay en dicha página.

La configuracion o incluso habilitacion de opciones no disponibles en el informa se puede establecer desde `configuracion de propiedades`.

**Informes Adquisición**
Los informes Adquisición pueden proporcionar información valiosa sobre cómo los usuarios llegan a su sitio web y el nivel de eficacia de su publicidad y marketing digital en los distintos canales como el correo electrónico, el buscador y los anuncios de display. Estos son algunos de los informes más importantes y útiles de Google Analytics.

**Medium/Medios**: Es el mecanismo por el cual llegan usuarios a nuestro sitio web:
- Organic: Google Search Bar
- CPC: Google Ads
- Referals: Other websites
- Email: Email Marketing Compaign
- None of the Above: Cuando la URL es escrita directamente. 
**Sourse/Fuente**: Se refiere a la fuente/Origen de la busqueda y nos da mas informacion hacerca del medio.
- Fuente Referals: URL del sitio que nos refiere.
- Organic: Browser donde se realizo la busqueda.

Esta informacion esta disponible en el informe de **Adquisicion** -> _All trafic_ -> **Source/Medium**. No es sufuciente identificar la fuente principal de datos es importante tambien conocer el **% de Rebote** para identificar la calidad del trafico. Ademas de utilizar filtros por mas detallados.

![image](https://user-images.githubusercontent.com/60556632/169389562-011b1eb6-ada2-46df-8b4e-7270bf88cb82.png)


- **Adquisicion** -> _All trafic_ -> **Channel** Podemos tabien encontrar los canales y cada uno con su respectiva fuente.

![image](https://user-images.githubusercontent.com/60556632/169388459-52901f29-0d80-489b-b8e2-e55783b9efe1.png)

- **Adquisicion** -> _All trafic_ -> **Referrals** Podemos investigar mas a detalle las paginas exactas de los referrals que nos estan trayendo trafico. Añadiendo la dimension secundaria `Landing Page` podemos ver donde estan aterrizando los referrals en nuestro website.
 
**Informes Comportamiento**
Los informes Comportamiento muestran cómo los usuarios interactúan con su sitio web. Pueden incluir diferente información, como el contenido que ven los usuarios o la forma en la que navegan por las páginas. Veamos algunos de los informes Comportamiento más útiles.

- **Informe de todas las paginas**: **Comportamiento** -> _OCntenido del Sitio_ -> **Todas las Paginas** Este informe permite ver las paginas mas populares entre nuestro usuarios. 
- **Comportamiento** -> _Contenido del Sitio_ -> **Desglose de Contenido** se basa en la estrutura de archivos de nuestro codigo y nos indica a nivel de archivos cuales son mas populares.
- **Comportamiento** -> _Contenido del Sitio_ -> **Landing Page** identificamos las metricas como porcentaje de rebote en nuestras landing pages.
- **Comportamiento** -> _Contenido del Sitio_ -> **Exit Pages** Paginas donde los usuarios dejaron el sitio web.
- **Comportamiento** -> _Eventos_ -> **Desglose de Contenido** Permite evaluar como interactuan los usuarios con objetos especificos del sitio web como botones o reproductor de video.

### Cómo medir las campañas personalizadas
Las campañas de publicidad pueden ser una manera eficaz de traer usuarios a su sitio web y ampliar su negocio. Puede usar Google Analytics para hacer el seguimiento de sus campañas de marketing de Google Ads o de otras plataformas. Si usa otras plataformas, puede añadir manualmente etiquetas de las campañas personalizadas a las URL de marketing para que Google Analytics haga un seguimiento de la repercusión de esas campañas.

[Recoger datos de campañas con URL personalizadas](https://support.google.com/analytics/answer/1033863?hl=es#zippy=%2Cen-este-art%C3%ADculo)

**Parámetros**
Hay 5 parámetros que se pueden añadir a las URL:

- `utm_source`: el anunciante, el sitio web, la publicación o la fuente que envía tráfico a su propiedad, por ejemplo, google, boletininformativo4, billboard.
- `utm_medium`: medio publicitario o de marketing, por ejemplo, cpc, banner o boletín informativo por correo electrónico.
- `utm_campaign`: el nombre de campaña, el eslogan, el código promocional u otra información de un producto determinado.
- `utm_term`: las palabras clave de búsqueda de pago. Si etiqueta campañas de palabra clave de pago de forma manual, también deberá usar utm_term para especificar el término en cuestión.
- `utm_content`: se usa para diferenciar el contenido o los enlaces similares del mismo anuncio. Por ejemplo, si tiene dos enlaces de llamada a la acción en un mismo mensaje de correo electrónico, puede utilizar - - - `utm_content` y establecer distintos valores para cada uno a fin de determinar qué versión es más eficaz.

Solo tenemos que añadir esta informacion a la URL **fuente/Medium** para que Google Analytics sea notificado hacerca de la campaña **Google Ads** o lo que sea que nos este generando trafico. Podemos los paremetros necesarios para ser tan especificos como deseemos. 

```sh
https://www.example.com/?utm_source=campaña_correo&utm_medium=correo&utm_campaign=rebajas-verano
```

### Realizar un seguimiento de las campañas con el [Creador de URLs](https://ga-dev-tools.web.app/campaign-url-builder/)
Google Analytics proporciona la herramienta Creador de URLs, que le facilita el proceso de agregar los parámetros de su campaña a las URL para realizar un seguimiento de las campañas personalizadas. Apesar de que existe el creador de URLs este solo permite crear una a la vez, por lo cual es mas practico usar `spreadsheet` y crear nuestro propio [template](https://docs.google.com/spreadsheets/d/1tf3_SczMMTTf-ZJ9Bkb70xps_DPGLBTd4wkHPyadKSA/edit?hl=es&;usp=sharing&hl=es#gid=1) para concatenar los valores indicados.

**Adquisición** -> _Campañas_ -> **Todas las Campañas** -> Usamos el buscador para filtrar por tipo de campaña. Seleccionamos la campaña y añadimos la dimension secundaria `Ad Content/Contenido del Anuncio`, entre otras como `palabra clave` o para identificar el contenido original de la URL y que tags estaba portando.

### Medir los objetivos de empresa con la función Objetivos
Objetivos de Google Analytics le permite asociar las métricas de sus informes con los objetivos empresariales específicos. Esta función puede ser una manera muy eficaz de utilizar los datos para ver si está cumpliendo los objetivos empresariales.

**Tipos de Objetivos**
- Objetivos de Negocio: Acciones que queremos que nuestro usuario ejecute o tambien conocidas como conversiones.
- Objetivos de Google Analytics: Es realmente un tracker de conversiones para crear un funnel de conversion. Podemos tener maximo 20 objetivos por vista en GA. Y la idea es monitoriear hasta que nivel de objetivo llega el usuario en el embudo. 

**Pasos a seguir para crear y visualizar un Goal**:
- **Administrar** -> Vista -> Objetivos -> Crear Objetivo ->Seguimos el [paso a paso](https://analytics.google.com/analytics/academy/course/6/unit/4/lesson/3)
- **Conversiones** -> Resumen
- **Conversiones** -> Grafico de embudo de conversion.

### Cómo medir campañas de Google Ads
Google Ads ofrece una manera muy eficaz de anunciarse en las plataformas web de Google. Puede vincular su cuenta de Analytics con Google Ads para medir la repercusión que tienen las campañas publicitarias en su empresa.

- Para enlazar Ads con Analytics **Administrar** -> _Propiedad_ -> **Vinculaciones con Google Ads** -> Indicamos el # de cuenta de Ads.

- Luego de realizar la comunicacion, vamos a **Adquisicion** -> _Google Ads_. Ahi podemos ver diferentes informes como **Campañas**, **Palabra Clave** ademas podemos utilizar dimensiones secundarias para ver los tipos de dispositivos usados. 
