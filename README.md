# nasa-apod
En este proyecto utilizaremos la API de la Nasa para obtener imágenes aleatorias de su fichero de **Imagenes del día**. Obtendremos 10 imágenes con sus datos asociados que mostraremos en formato "tarjeta" (card). Al hacer clic sobre la imagen, la veremos en toda su resolución. Si queremos, podemos marcar una imagen como favorita (la almacenará en LOCALSTORAGE). Podemos renovar la página y cargar 10 nuevas imágenes. Para mejorar el rendimiento, la carga de imágenes se hará utilizando **lazy load** (las imágenes se cargan cuando se necesitan). La página será responsive
# Recursos utilizados
Aplicación que permite crear iconos SVG animados: (Loaf - Animated SVG Generator)[https://getloaf.io/]
API de la NASA: (NASA API)[https://api.nasa.gov]
(Muestra de lo que obtenemos - NASA API Demo)
[https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY]


(W3Schools - includes())[https://www.w3schools.com/jsref/jsref_includes.asp]

(W3Schools - JSON.stringify)[https://www.w3schools.com/js/js_json_stringify.asp]

Para volver al pricipio de la página: (window.scrollTo)[https://developer.mozilla.org/en-US/docs/Web/API/Window/scrollTo]

# Como se hizo
Tenemos 2 overlay, que harán que parezca que hay dos páginas, cuando en realidad solo hay una:
+ La página principal ()
+ La página de favoritos ()
Las dos están dentro del mismo contenedor (container)

Recordatorio: en el JavaScript, append permite añadir varios hijos a la vez, mientras que appendChild añade solo uno.


Lazy load:

''        // Image
        const image = document.createElement('img');
        image.src = result.url;
        image.alt = 'NASA picture of the day';
        image.loading = 'lazy';                 //lazy load
        image.classList.add('card-img-top'); ''

Una imagen que me gusta:
Stephane Vetter 2020-07-04
Meeting in the Mesosphere
https://apod.nasa.gov/apod/image/2007/msv1500crop.jpg
