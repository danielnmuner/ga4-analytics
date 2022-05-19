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

  - **Selector de Matricas**:

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




