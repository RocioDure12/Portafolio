# Observaciones

Ro, felicitaciones por tu trabajo. Que lindo quedó tu portfolio, qué hermosa combinación de colores e imágenes. Seguís casi a la perfección el modelo y tu web se ve muy completa y profesional. 

Como dije en clase, este trabajo no se hace para que constates conocimientos, sino para que aprendas: en ese sentido, mi intencion es que estos comentarios te sirvan para aprender, mejorar tu codigo a futuro e ir apreciando mejor qué se espera de nosotras como desarrolladoras front end.

## Estructura correcta de documento HTML

Tu HTML esta muy bien. Claro, prolijo, muy bien comentado e identado.

Utilizás ocasionalmente etiquetas `br` para separar las cosas: no llegué a comentarlo en clase, pero esto es incorrecto. Esa etiqueta es un resabio de viejas épocas en las cuales css no era tan poderoso como ahora, pero usarla hoy viola uno de los principios básicos de programación: la separación de responsabilidades. Los estilos se dan con css, la estructura se da con html. Una decisión de estilo como un espaciado entre dos elementos debe controlarse con css -flex, elementos en bloque, etc, no con `br`. 

## Respeta la consigna

- El portfolio cuenta con las secciones solicitadas
- Al clickear en los links de navegación, debe llevar a la sección correspondiente

Cumplido. 

- Al clickear en los links de contacto, debe llevar a la página externa correspondiente 

No cumplido. No es necesario que agregues tus propias redes si es algo que preferís no hacer, pero
cualquier link a una web externa hubiera servido para cumplir la consigna. En el footer tienen el href vacio, en el form ni siquiera tienen href asi que no se les puede hacer foco. 

- El portfolio debe tener un diseño responsivo y verse correctamente en distintos dispositivos 

Cumplido, con la excepcion de un scroll horizontal muy molesto en las menores resoluciones de movil. Quiza ni lo hayas notado, pero eso ocurre cuando hay un elemento que esta rebalsando el ancho del body. En este caso, se trata del div que contiene a la imagen principal:

```css
@media (max-width: 768px) {
.imagen-portada {
    display: flex;
    align-items: center;
    width: 350px;
    padding: 30px;
    }
}
```

Ese padding de 30px hace que rebalse en resoluciones menores a 350px. 

- El portfolio debe estar deployado y ser accesible desde una URL 

Cumplido. 

- El repositorio en GitHub debe tener un readme adecuado

Cumplido, aunque podría ser mucho más amable con el lector. El README es realmente muy importante! Ayuda mucho a quienes encuentran nuestro github, especialmente cuando estamos recién arrancando.

### Respeta el diseño dado

Cumplido.

### Buena estructura de proyecto

Usás muchas imágenes en tu proyecto, y viéndolo a primera vista en github no es tan fácil ver cuáles son los archivos principales. Siempre que uses imágenes locales, como en este caso, agregalas a una carpeta que se llame por ejemplo "imgs", "imagenes" o "assets". De esta manera solo los archivos principales - html, readme y css - son los que están en la carpeta principal. La excepción a esta regla es el favicon -ausente en tu portfolio-, que siempre debería ir en la carpeta principal. 

### Código bien indentado

A veces tu tabulado es confuso o erróneo - te lo dejo comentado en el archivo de HTML. 

Noto muy desprolijo tu CSS. Recordá que hay extensiones de VSCode que pueden ayudarte a dejarlo más prolijo, igual te menciono algunas cosas:

A veces no dejas el espaciado correcto en cada orden. En lugar de escribir por ejemplo `.name{`, deja un espacio entre el nombre de la clase y la llave: `.name {`

En CSS se cumplen las mismas reglas que en html, si dejas tabulado significa que estas adentro de otra cosa (por ejemplo una media query). Esto, por lo tanto, es erróneo, tendrian que estar todos al mismo nivel:

```css
.comillas>i{
     font-size: 90px;
     padding: 10px;
     color: white;
        
    }

    .contenedor-cita{
        width: 70%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .contenedor-cita>span{
        font-weight: 600;
        text-align: center;
    }
```

### Comentarios que permiten mejorar la legibilidad del código

Cumplido

### Uso correcto de etiquetas semánticas

- Me llama la atención que hayas usado `div` para las tarjetas de Mis Conocimientos y Mis Proyectos: yo diría que deberían ser `article`. Pero es el único detalle a comentar aquí (y hay quien podría discutirme que deberían ser divs)

### Buenos nombres de clases

Cumplido, un gran mérito en esta etapa, sé lo difícil que es pensar buenos nombres de clases. 

### Código CSS bien estructurado

Cumplido a nivel formal. Noto algunos estilos innecesarios o confusos, que te voy indicando en tu archivo de css.

### Reutilización de estilos

Cumplido en general. 

### Cumple con criterios básicos de accesibilidad

- Los colores tienen un contraste adecuado

Incumplido toda vez que tenes una combinacion de blanco y el verde, como en tus botones, el footer y la cita. Siempre recordá chequear tus colores con herramientas como https://webaim.org/resources/contrastchecker/

- Las imágenes tiene el atributo `alt` que corresponde

Incumplido. Si te pareció innecesario agregar `alt` para las imagenes de Mis Proyectos, correspondía un aria-hidden en lugar de dejar el alt vacío (que indica que la imagen es decorativa: aquí claramente es ilustrativa). Dejarlo vacía es decirle al usuario que depende del lector de pantalla "aquí hay una imagen y no te voy a decir qué es", lo que no es una buena experiencia. 

- Los íconos y elementos que no presentan texto agregan la información correspondiente por otros medios (etiquetas aria, texto oculto)

No cumplido, por ejemplo en los links a redes sociales de tu footer. Necesitan un aria.

- Los íconos y elementos que no necesitan ser anunciados por un lector de pantalla tienen la etiqueta aria
  correspondiente

No cumplido. 

- Commits con mensajes adecuados

Cumplido, noto muchos y buenos commits en tu proyecto, lo que siempre se agradece.

- Cuenta con un favicon

No cumplido. 

### Nota: 8
