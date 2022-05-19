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

### Informes de Vision General
- **Vision Genral de Audiencia**: #Usuarios, paginas visitadas en cada sesion, duracion media de las sesiones y el porcentaje de rebote. 
  - **Selector de periodos**: Periodo en el que queremos analizar el informe
  - **Selector de segmentos** Defaul(Todos los Usuarios): Permite filtrar los datos y realizar comparaciones
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

**Dimensiones y Metricas**
  - Las **dimensiones** son atributos de los datos. Por ejemplo, la dimensión Ciudad indica la ciudad (como "Madrid" o "Nueva York") desde la que se origina una sesión. La dimensión Página indica la URL de una página vista.
- Las **métricas** son dimensiones cuantitativas. La métrica Sesiones es el número total de sesiones. La métrica Páginas / sesión es el número medio de páginas vistas por sesión.

| DIMENSIÓN | MÉTRICA  | MÉTRICA          |
| --------- | -------- | ---------------- |
| Ciudad    | Sesiones | Páginas / sesión |
| Aranjuez  | 5000     | 3,74             |
| Berlín    | 4000     | 4,55             |

En la mayoría de informes de Analytics, puede modificar la dimensión y añadir una dimensión secundaria. Por ejemplo, si añadimos "Navegador" como dimensión secundaria a la tabla anterior, tendríamos lo siguiente:

| DIMENSIÓN | DIMENSIÓN | MÉTRICA  | MÉTRICA          |
| --------- | --------- | -------- | ---------------- |
|  |
| Ciudad    | Navegador | Sesiones | Páginas / sesión |
| Aranjuez  | Chrome    | 3000     | 3,5              |
| Aranjuez  | Firefox   | 2000     | 4,1              |
| Berlín    | Chrome    | 2000     | 5,5              |
| Berlín    | Safari    | 1000     | 2,5              |
| Berlín    | Firefox   | 1000     | 4,7              |
 
