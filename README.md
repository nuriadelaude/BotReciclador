# BotReciclador

Este proyecto tiene como objetivo ayudar a todas las personas que deseen comenzar en el mundo del reciclaje o que tal vez ya lo hagan y necesiten ayuda. Así como también ayudar al problema mundial que tenemos con la cantidad de basura que genera cada persona. Tenemos que tener en cuenta que lo ideal es no utilizar materiales de un solo uso (bolsas, vasos descartables, cubiertos descartables) pero reciclando y separando estos materiales podemos hacer una diferencia importante.

A este bot puede acceder cualquier persona con una cuenta de Facebook. 

Para llevar a cabo este proyecto primero comenzamos con Watson Assistant, creamos un Skill y le enseñamos a interectuar con el usuario. Luego en Visual Recognition creamos un modelo que clasifica imagenes en cuatro categorías: inorganicos (reciclables), inorganicos (no reciclables), voluminosos (o manejo especial) y organicos. Le cargamos imagenes y definimos cada categoría hasta que pudimos obtener un resultado certero en cada prueba. 

<img src="/nuriadelaude/BotReciclador/raw/master/docs/imagen.png">

Luego creamos una base de datos (Cloudant) que nos permite guardar la información que nos provee el usuario por un corto periodo de tiempo, para poder recibir la imagen, enviarla a visual recognition, que nos devuelva el resultado y finalmente reenviarselo al usuario. Cuando el usuario termina de la conversación, el documento generado es eliminado de la base de datos. 

Esta es solo una de las funciones de nuestro bot. También cuenta con la capacidad de: si el usuario no quiere enviar una imagen puede ingresar su pregunta relacionada a reciclaje y el bot será capaz de diferenciar cada clase para luego brindarle información sobre ella, por ejemplo, ¿es el plástico reciclable?

<img src="/nuriadelaude/BotReciclador/raw/master/docs/preguntas_reciclaje_wa.png">

Por otro lado, si le brindamos nuestra ubicación (por ahora solo disponible para Capital Federal, Buenos Aires) nos puede decir que puntos de reciclaje tenemos cerca y su dirección.

<img src="/nuriadelaude/BotReciclador/raw/master/docs/punto_verde.png">

Así mismo también le podemos pedir información sobre los días de apertura y horarios del punto de reciclaje.

<img src="/nuriadelaude/BotReciclador/raw/master/docs/dias_y_horarios.png">

Finalmente integramos el asistente con Facebook para que sea accesible por cualquier usuario. 




Nuestro plan de mejoras a futuro contempla los siguientes puntos:

1) Geolocalización: con esto podremos brindarle al usuario la información en tiempo real de todos los puntos de reciclaje en su zona. 

2) Reconocimineto de imagen en tiempo real: para que el usuario no necesite sacarle una foto, solo con apuntar la cámara del teléfono al objeto podrá obtener una respuesta.

3) Agregar más plataformas donde funcione, para que más usuarios puedan utilizarla. Ahora solo contamos con Facebook pero podríamos integrarla con WhatsApp, Slack (para instituciones o empresas) y otras redes sociales. 

Nuestro plan de escalabilidad contempla los siguientes puntos:

1) Con los datos que tenemos más los que obtengamos de cada usuario (por ejemplo, ubicación y tipo de materiales que recicla, siempre manteniendo esto anónimo) crear estadísticas. A traves de las estadísticas poder generar vínculos con centros de reciclaje de la Ciudad o el Ministerio de Medio Ambiente a los fines de utilizar estos datos para: poner más puntos de reciclaje, alertas de llenado de puntos de reciclaje para hacer una recolección más eficiente y evitar la acumulación de basura en estos lugares. 

También lograr una alianza con organizaciones no gubernamentales dedicadas al reciclaje a los fines de que a traves de nuestra aplicación puedan brindar más concientización, información y capacitación. Podríamos generar alertas de cursos y capacitaciones brindadas por estas organizaciones. Y entre todos contribuir para lograr un Medio Ambiente más sano. 







