# ChatBot
ChatBot creado para el proyecto 3 de administración de tecnologías.


### *Adderly Sinay 7690-13-7664*
### *Daniel Paniagua 7690-17-6640*
### *Mario Field 7690-17-20612*

## Cómo configurar un chatbot

Lo primero que va a necesitar tu chatbot es un nombre. Para poder configurar tu chatbot accede a Configuración > General y edita el nombre por defecto de tu bot.


![imagen](https://user-images.githubusercontent.com/38385565/120896147-79fcff80-c5dd-11eb-871f-f912b30ff1b4.png)


También puedes cambiar el mensaje de la notificación (burbuja emergente) a un mensaje personalizado para tu sitio que pueda atraer más clics e interacciones con tu bot.



![imagen](https://user-images.githubusercontent.com/38385565/120896164-8a14df00-c5dd-11eb-9a05-0774d14da11c.png)


## Personalizar tu Chatbot
Lo siguiente que querrás hacer es personalizar el estilo cambiándole el color e imagen a tu chatbot. Para eso debes acceder a Configuración > Personalización.
Puedes cambiar y probar distintos estilos hasta encontrar el que mejor se ajuste a tu sitio.


![imagen](https://user-images.githubusercontent.com/38385565/120896292-250db900-c5de-11eb-922e-62b05a01e926.png)

## Casos de Uso
En la sección ChatBots > Casos de Uso, puedes asignar un uso predefinido a tu bot. Tienes las siguientes opciones:

![imagen](https://user-images.githubusercontent.com/38385565/120896316-35259880-c5de-11eb-9c53-74839260fc55.png)

Puedes cargar chatbots con un propósito específico para luego instalarlos en tu sitio, aplicación o canal de comunicación preferido. Haz click en un caso de uso, edita el texto dentro de las componentes (cajas) y guarda.
Si deseas que este uso aparezca por defecto en tu Bot, ingresa un nombre único a ese guión y marca "Sí" en ¿Quieres hacer de este guión el componente inicial?.

![imagen](https://user-images.githubusercontent.com/38385565/120896351-5a1a0b80-c5de-11eb-853a-34c74d06a0c2.png)

## Cómo agregar tus respuestas
Para entrenar tu chatbot con tus respuestas tienes tres opciones.
•	Usa tus propios pares de preguntas y respuestas
•	Carga una Habilidad
•	Importa tus Preguntas y Respuestas


## Cómo crear un bot para Telegram

Debes tener una cuenta en Telegram. Se recomiendo utilizar el cliente web de Telegram para probar los conceptos básicos.

Abre la aplicación Telegram, busca @BotFather e inicie el chat. Envía el comando /newbot y sigue las instrucciones. Después de completar los pasos iniciales, obtendrás:

    Tu propio token
    URL de api de telegram - api.telegram.org/<tu token>
    enlace a la documentación

Por el momento el bot es 100% pasivo.


## Integración con Chatcompose

Para continuar vas a necesitar una cuenta ChatCompose.

Una vez registrado, accede a la sección Instalar>Integraciones. Allí verás la opción de integrar con Telegram.

Verás lo siguiente:

![imagen](https://user-images.githubusercontent.com/38385565/120896476-03610180-c5df-11eb-966a-41cd73ef11c5.png)


Ingresa el token que generaste con BotFather y guarda.

Una vez guardado, vamos a registrar nuestra ruta del bot sacada de la plataforma con telegram. Copia la ruta y pégala en esta url junto con tu token.

    api.telegram.org/bot<tu_token>/setWebHook?url=<la_ruta>

La url debería quedar algo así:

    api.telegram.org/bot000000:AAAAAAAAAAAAA/setWebHook?url=https://panel.chatcompose.com/telegram/tubot

Navega hasta esa ruta. La respuesta debería devolver lo siguiente:

    {"ok":true,"result":true,"description":"Webhook was set"}

Para probar si la configuración fue exitosa puedes navegar a:

    api.telegram.org/bot<tu_token>/getWebhookInfo

La llamada debería devolver la url de chatcompose que acabamos de configurar.

Si aún no has ingresado el token generado con BotFather dentro de ChatCompose házlo ahora.


## Próximos Pasos

Tu bot debería estar instalado y funcionando en Telegram. No olvides configurar tus respuestas automáticas dentro de ChatCompose en la sección Base de datos.

Haz click en la dirección de tu bot que generó BotFather (t.me/nombredetubot) y comienza a interactuar con él.

## Usa tus propios pares de preguntas y respuestas
Primero vamos a ver cómo entrenar tu chatbot con tus propias preguntas y Respuestas. Para empezar a entrenar tu chatbot visita la sección Base de Datos>Respuestas. En esta sección podrás ingresar los mensajes que deseas responder.
Tienes dos opciones:
1.	Responder con Texto
2.	Responder con componentes o guiones

![imagen](https://user-images.githubusercontent.com/38385565/120896768-24762200-c5e0-11eb-8a2c-1ebed95909d6.png)

## Respuestas de Texto
Para responder con Texto, ingresa el mensaje que te gustaría que tu chatbot respondiera. Por ej: "Cómo se llama la empresa".
Como respuesta ingresa "Mi empresa se llama X". Luego presiona Insertar.
Ahora tu chatbot estará entrenado para responder cómo se llama tu empresa. También será capaz de contestar variantes a ese mensaje como "cómo se llama la compañía" o "cómo llamo a la sociedad". Puedes probar tus respuestas haciendo clic en el botón de micrófono de la esquina.
También puedes usar el chatbot para que haga respuestas más amplias usando palabras claves. Por ejemplo puedes ingresar "precio" y cómo respuesta poner "Puedes ver los precios en....". Antes de Insertar, cambia la opción de "frase" a "palabra".

![imagen](https://user-images.githubusercontent.com/38385565/120896781-32c43e00-c5e0-11eb-80c5-738b3e68f3ce.png)

De esta manera cada vez que alguien ingrese la palabra "precio" dentro de su mensaje, recibirá "Puedes ver los precios en....". Por ej: "cuál es el precio" "dime el precio por favor" o "quiero saber el precio".
Para usar más de una palabra clave para una respuesta usa comas, Ej: "precio,planes,tarifas". El chatbot responderá a todas esas palabras con la misma respuesta.
Usar palabras en vez de frases es una buena táctica para ampliar la cantidad de preguntas a responder.

## Respuestas con Componentes o Guiones
Las respuestas con componentes funcionan de la misma manera que las respuestas con texto. La única diferencia es que la respuesta en vez de ser texto será un componente o guión.
Por ejemplo, puedes crear un guión conversacional que guarde los datos del usuario. (correo, teléfono etc.).
Luego como mensaje activador ingresa, "quiero que me contacten" y como componente ingresa el guión que creaste para guardar los datos del usuario.

##Ingresa múltiples mensajes
Para ingresar mútiples mensajes haz click en el ícono . Tendrás la opción de ingresar mensajes similares para respuestas específicas, y ahorrar tiempo en tu entrenamiento del chatbot.

![imagen](https://user-images.githubusercontent.com/38385565/120896801-4e2f4900-c5e0-11eb-9568-4bce10f40267.png)

## Monitorea Conversaciones para obtener nuevas ideas
La sección conversaciones mostrará los mensajes que recibe tu bot. Podrás ver los que ha podido reponder exitosamente y los mensajes que no ha podido responder.
Haz click en la columna Puntaje para ordenar las respuestas.

![imagen](https://user-images.githubusercontent.com/38385565/120896828-6dc67180-c5e0-11eb-9dc6-b1b5860019ad.png)


Ingresa las preguntas que tu bot no ha podido responder para ir mejorando continuamente el entrenamiento de tu bot.
Además, en la sección Sugerencias aparecerán sugerencias de nuevas respuestas que puedes agregar a tu bot.
Los registros tienen una función de anonimato de IP para los últimos dígitos, para cumplir con las leyes de privacidad. 

## Carga una Habilidad
Puedes entrenar tu chatbot ingresando respuestas a preguntas ya establecidas. Para eso Navega a Habilidades.
Allí puedes encontrar distintos temas de conversación.

![imagen](https://user-images.githubusercontent.com/38385565/120896873-b0884980-c5e0-11eb-8bb9-0dc1d9f99116.png)

Haz Click en uno de ellos para continuar.

![imagen](https://user-images.githubusercontent.com/38385565/120896879-b847ee00-c5e0-11eb-8404-4ac03dd59a9e.png)

En esta sección sólo necesitarás poner respuestas a los mensajes ya definidos para el chatbot. Guarda para terminar.
Tu chatbot estará entrenado para responder algunas de las preguntas más comunes de ciertos temas.

## Importa tus Preguntas y Respuestas
Puedes importar pares de Preguntas y Respuestas en la sección Base de Datos>Importar CSV.
En esta seción puedes cargar un archivo CSV, luego seleccionar la columna se Pregunta y Respuesta y continuar. Se cargarán los datos de tu archivo dentro de tu chatbot. Por favor usa sólo plantillas de 50 filas a la vez.


## ¿Qué son los guiones conversacionales?

Un guión es un mensaje / conjunto de mensajes almacenados previamente, o frases u oraciones escritas previamente que proporcionan una dirección en una conversación específica. Los guiones pueden incluir temas para el inicio de una conversación, contenido de un tema, respuestas a preguntas e ideas que conectan las conversaciones.
Los guiones pueden incluso ayudar a los chatbots a cambiar el tema de manera adecuada, hacer preguntas, liderar la conversación, ser el orador principal e incluso terminar las conversaciones.
Sobre el uso de guiones

Los guiones deben ser individualizados para tener en cuenta las características lingüísticas actuales del usuario, y sus temas de interés.
Los guiones también se pueden individualizar considerando situaciones específicas, guiadas por las conversaciones anteriores del usuario o sus elecciones hechas.

## Componentes reutilizables

La interfaz te permite mostrar componentes durante una conversación con tus usuarios. Algunas opciones son:
•	Mensaje: Muestra un mensaje simple de texto al usuario
•	Opción: Para mostrar opciones seleccionables por el usuario.
•	Formulario: Para captar datos importantes de tus usuarios.
•	HTML: Para mostrar elementos diseñados por ti.
•	Media: Envía fotos, videos y archivos a tus usuarios.
•	Pago: Te permite crear pagos a hacer para tus usuarios (con PayPal).
•	Reservas: Muestra tu disponibilidad que tus usuarios reserven.
•	ChatenVivo: Habla con tus usuarios en Vivo.
•	Conexión externa: Muestra datos de servicios externos.
•	Transferir: Transfiere la conversación a otro servicio.
•	Condición: Filtra y evalúa las respuestas de los usuarios.
Los componentes se ingresan de forma secuencial y en orden, por lo que tienes que decidir de antemano cómo vas a diseñar el guión.

## Cómo crear un guión conversacional

ChatCompose cuenta con una interfaz de creación de guiones, que te puede ayudar a crear el guión perfecto para tu venta, cualificar tus clientes o responder pedidos de soporte.

Tomemos el siguiente ejemplo. Tu sitio web o servicio es un sitio e-commerce que genera ventas de calzado.
Para modelar el guión, primero pregúntate ¿Qué vinieron a hacer los usuario a mi sitio?

La opciones pueden ser:
1.	Quieren calzado para una ocasión especial. 
2.	Quieren saber tus condiciones de envío. 
3.	Quieren hacer un pedido de atención al cliente. 
 
Para implementar este ejemplo usamos la interfaz para crear guiones. Navega a "Crear Guiones" dentro del panel.
Primero ingresas el identificador del guión y un una pequeña descripción. Al identificador lo vamos a llamar "ayudacompras", y a la descripción "guión para ayudar en compras".

![imagen](https://user-images.githubusercontent.com/38385565/120896936-fd6c2000-c5e0-11eb-8f47-625b80f26139.png)

Al hacer click en crear guion vamos a la interfaz gráfica de creación, aquí podrás ver un componente de mensaje con nombre start. Haz click sobre él, y modifica el texto a "¿Qué puedo hacer por ti?".
Se verá así:

![imagen](https://user-images.githubusercontent.com/38385565/120896948-065cf180-c5e1-11eb-8ef5-de90cfa470b7.png)

Para continuar, y dado que ya hemos definido las opciones, agregamos al diagrama el componente de opción haciéndole clic en el panel de la derecha.
En este paso se va a abrir la configuración del componente, dónde le ingresamos las opciones posibles que ya definimos antes.

![imagen](https://user-images.githubusercontent.com/38385565/120897031-7f5c4900-c5e1-11eb-9108-7849a6a75f43.png)

Tras hacer clic en crear, el componente se va a agregar en la interfaz. Listo, ya hemos creado las opciones.
Vas a ver también que el panel de la derecha se ha desactivado y te muestra el mensaje:

![imagen](https://user-images.githubusercontent.com/38385565/120897035-871bed80-c5e1-11eb-9be2-91f28f1f430b.png)

Esto significa que para continuar vas a tener que elegir una opción con la cual continuar.
Para elegir la opción dónde vas a continuar, pasa el mouse sobre ella para ver cuál es, y haz clic en ella para que se ponga roja. Una vez seleccionada, apreta el botón "Continuar".

![imagen](https://user-images.githubusercontent.com/38385565/120897038-8e42fb80-c5e1-11eb-85fc-37f6de5621ba.png)

Ahora que hemos seleccionado la opción dónde vamos a continuar, y el panel de componentes ha vuelto a aparecer, podemos ingresar más componentes.
Dado que hemos elegido la opción "Quiero saber las condiciones de envío", les puedes mostrar como respuesta un mensaje. Para responder en texto haz clic en mensaje y escribe el texto "las condiciones de envio son ......". Haz clic en crear.
Ahora que hemos terminado con esa opción podemos continuar con las otras opciones. Vamos a continuar con "Quiero hacer un pedido de atención al cliente".
Haz clic en la opción correspondiente y apreta continuar. Ahora ingresamos un componente mensaje con "Perfecto! Antes de contactarte con el equipo de soporte necesitamos algunos datos tuyos". Inmediatamente agregamos el componente formulario, que se encarga de captar el pedido y los datos del usuario.

![imagen](https://user-images.githubusercontent.com/38385565/120897048-98fd9080-c5e1-11eb-818f-563d01e69e05.png)

Ingresa un identificador para el formulario (aparecerá en la sección Leads, dónde podrás ver los datos captados), e ingresa las consulta que le vas a hacer al usuario. Nosotros vamos a ingresar las consultas. "Danos un correo dónde contactarte por favor" seguido con la pregunta "Por favor ingresa tu pedido de soporte".

El formulario aparecerá dentro de tu diagrama.
Para terminar con el guión también seguiremos la opción "Quisiera calzado para una ocasión especial". Haz clic en la opción y continúa.
En esta opción vamos a ingresar otro componente de mensaje con "Que bien! Puedo ayudarte. Dime para que ocasión te gustaría tu calzado". Inmediatamente ingresamos un componente de opción con las opciones "Una ocasión formal" y "Una ocasión informal". Apretamos crear.

En la opción "Una ocasión formal", vamos a ofrecerle al usuario un enlace a una página de nuestro sitio con zapatos formales de vestir. Apretamos la opción, continuamos e ingresamos un nuevo componente, llamado enlace.

Dentro del enlace vamos a llenar el título del enlace y su url. Ingresamos la url "https://github.com/adderlinho/ChatBot" con el título "Variedad de Zapatos formales". Creamos y continuamos con la otra opción.

![imagen](https://user-images.githubusercontent.com/38385565/120897062-a9ae0680-c5e1-11eb-847b-4891aae3c44d.png)

Ahora seguimos la opcion "Una ocación informal", hacemos clic, apretamos continuar y le ingresamos otro componente de enlace, esta vez con la url "https://github.com/adderlinho/ChatBot" con el título "Variedad de zapatos informales".
El diagrama se debería ver algo así:

![imagen](https://user-images.githubusercontent.com/38385565/120897065-b03c7e00-c5e1-11eb-9dc1-8bbd2b3fe108.png)

Para finalizar apretamos el botón "Guardar". Ahora tenermos el guión listo y guardado en el sistema.

## Implementar el guión

Para implementar el guión tenemos la opción de ingresarlo (1) como respuesta a una pregunta específica en Base de Datos, (2) como componente inicial en una página en específico en Configuración>Páginas y (3) como componente inicial del chatbot.
Vamos a elegir la alternativa 3 y lo vamos a establecer como componente inicial del chatbot.

![imagen](https://user-images.githubusercontent.com/38385565/120897088-bcc0d680-c5e1-11eb-9106-ad1682ce864b.png)

Puedes probar el guión que hemos hecho haciendo clic en el chatbot a la derecha.
Ahora estamos listos, y tenemos una noción general de cómo crear guiones conversacionales en ChatCompose.

## Funciones Avanzadas

La interfaz de creación también cuenta con algunas funciones avanzadas, las cuales puedes usar para mejorar tu proceso de creación de guiones.
Saltar a: Esta función te permite retroceder o saltar hacia otro componente dentro de tu guión. Debes tener cuidado al elegir esta función porque una vez elegida no podrás deshacerla.

Asegúrate que entre tu componente actual y el componente objetivo exista
1.	Opción
2.	Formulario
3.	Api
4.	Pago
5.	El componente este en otra opción

De otra manera podría ocurrir un loop o ciclo infinito.
Simular: Esta función te permite simular el guión a medida que lo vas creando.
Recuerda que para actualizar la simulación debes hacer click en "reset" y "start".
Condición : este componente le permitirá filtrar y dirigir la conversación en función de la entrada del usuario. 
Puede evaluar la respuesta y dirigir la conversación hacia un propósito específico. Por ejemplo, si pregunta "¿Está buscando zapatos?", puede verificar si la respuesta contiene las palabras clave "no", "No" y "después", y luego dirigir la conversación para la condición Verdadero o Falso. 

## Cargar y Editar Guiones

Para cargar y editar tus guiones navega a la sección "Cargar Guiones". Allí podrás cargar tus guiones hechos de una lista para editarlos. 
Puedes editar el contenido de tus guiones haciendo click en los componentes y cambiar el texto dentro de ellos. Para añadir o borrar componentes necesitas hacerlo a través de los componentes finales de tu guión (sin hijos).
 
Al hacer click en los componentes finales puedes comenzar a agregar más componentes en tu guión o borrar los que ya no deseas tener.
 
Si deseas borrar o añadir componentes más arriba del guión necesitas eliminar los componentes de esa rama hasta llegar al punto donde deseas continuar.

![imagen](https://user-images.githubusercontent.com/38385565/120897128-e548d080-c5e1-11eb-8670-096ba6cdc614.png)



## URL proyecto en git

https://github.com/adderlinho/ChatBot

[git hub] (https://github.com/adderlinho/ChatBot)

## URL prueba

https://admin.chatcompose.com/sharebot/asinayl-TecnoShop/ES/small

[chatbot tecnoshop] (https://admin.chatcompose.com/sharebot/asinayl-TecnoShop/ES/small)









