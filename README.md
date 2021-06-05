# ChatBot
ChatBot creado para el proyecto 3 de administración de tecnologías.



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


