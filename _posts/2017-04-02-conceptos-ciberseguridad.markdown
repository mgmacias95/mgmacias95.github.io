---
layout: post
title: "Conceptos básicos sobre ciberseguridad"
date: 2017-04-02
excerpt: "Algunas de las cosas que deberías saber para protegerte en Internet"
tags: [ciberseguridad]
comments: false
---

# Motivación

El otro día, navegando por Twitter me encontré con este estudio en el cual, habían preguntado a usuarios aleatorios de Internet sobre temas de ciberseguridad. Lo increíble de los resultados es que muchos de ellos no sabían lo que significa `https` o la autenticación en dos pasos o incluso un _phishing_.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">So about the cybersecurity quiz by <a href="https://twitter.com/pewresearch">@PewResearch</a> - the public results show a worrying lack of awareness in some areas<a href="https://t.co/SrO0iv7Evw">https://t.co/SrO0iv7Evw</a> <a href="https://t.co/89eW8pS3Sl">pic.twitter.com/89eW8pS3Sl</a></p>&mdash; DuckDuckGo (@duckduckgo) <a href="https://twitter.com/duckduckgo/status/847088151369728000">March 29, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

En mi caso, he hecho el test y sólo he fallado una pregunta. Pertenezco al 3% de usuarios de internet (según ese test). Por tanto, creo que es importante contribuir a que esa cifra aumente.

<figure>
    <img src="/assets/images/ciberseguridad/MiResultado.png">
    <figcaption>Resultado obtenido en el test.</figcaption>
</figure>

# Conceptos básicos sobre ciberseguridad

A continuación voy a exponer los conceptos que creo que todo usuario de Internet debería conocer, si crees que me ha faltado (o sobrado) alguno, estoy abierta a sugerencias!

## HTTPS y Certificados digitales
Una de las preguntas del test era sobre el significado de esa _S_ al final de _HTTP_: la respuesta es __seguro__. En la <a href="https://en.wikipedia.org/wiki/HTTPS" target="_blank">Wikipedia</a> encontramos una buena explicación sobre esto: no es más que el HTTP de toda la vida, pero encriptado. ¿Qué quiere decir esto? Que si alguien consigue capturar nuestro tráfico, no podrá interpretarlo.

Una vez comprendido esto, uno debe preguntarse ¿y cómo se encripta ese contenido? Y ahí es donde entran en juego los <a href="https://en.wikipedia.org/wiki/Public_key_certificate" target="_blank">__certificados__</a> y los algoritmos de cifrado. Los certificados sirven para poder identificar tanto el sitio web como su servidor. Son como el _carnet de identidad_, por así decirlo. Estos certificados nos permiten evitar ataques _Phishing_ o _Man-In-The-Middle_, ya que identifican de forma única al sitio web y a sus administradores. Además, los certificados llevan asociada una <a href="https://en.wikipedia.org/wiki/Public-key_cryptography" target="_blank">clave pública</a> que permite crear esta conexión segura (cifrada) con el usuario. 

## Ataques Phishing
De pronto recibes un correo electrónico de tu banco pidiéndote que entres corriendo a su banca online _a través de un enlace que te proporcionan en el correo_ o si no, tu cuenta será bloqueada en menos de 12 horas. Te pones muy nervioso y decides hacer click en dicho enlace y loguearte. ¡Craso error!

Estás leyendo el periódico y de pronto te sale un anuncio felicitándote, porque acabas de ganar un _iPad_ por la cara y para reclamar tu premio, sólo tienes que hacer click en un enlace. ¡Craso error!

En ambos casos, al entrar en dicho enlace o bien se instalará un _virus_ en nuestro ordenador o bien habrán robado nuestras credenciales. Sea lo que sea, has sido víctima de un <a href="https://en.wikipedia.org/wiki/Phishing" target="_blank">_phishing_</a>. 

¿Cómo identificar estos ataques? Simple: tu banco nunca va a mandarte ningún correo así, te mandarán un SMS o te llamarán por teléfono y nadie regala _iPads_ por la cara. Esto último se aplica también a las páginas de Facebook en las cuales tienes que dar like para entrar en el sorteo de algún producto súper caro.

¿Cómo evitar estos ataques? Con cabeza. No abriendo emails sospechosos y usando _AdBlock_ en páginas con __muchos anuncios__ en las cuales es bastante probable que sin querer hagas click en un anuncio, debido a que ocupan la mayor parte de la pantalla.

## Funciones resumen (hash)
Las <a href="https://en.wikipedia.org/wiki/Cryptographic_hash_function" target="_blank">Funciones hash</a> se usan en ciberseguridad para __identificar un archivo__. Son funciones que reciben como entrada un archivo, lee su contenido y, a través de una función matemática, dan como resultado una cadena de carácteres que __identifican unívocamente a ese archivo__. Si el archivo tiene el más mínimo de los cambios, obtendría un _hash_ completamente distinto.

Esa es la gracia de estas funciones, evitar que los usuarios descarguen archivos que hayan sido __modificados__. Por ejemplo, nadie quiere descargar _Skype_ y que al instalarlo se le instale un virus. Para eso, se usan estas funciones.

Junto al link de descarga de un archivo, se especifica su función hash, esta función puede ser __SHA-1__, __MD5__, __SHA-256__... Aunque __SHA-1__ <a href="http://www.infoworld.com/article/3173845/encryption/google-kills-sha-1-with-successful-collision-attack.html" target="_blank">se está dejando de usar</a>.

¿Cómo puedes verificar los archivos que descargas? En la <a href="https://www.ubuntu.com/download/how-to-verify" target="_blank">página de ubuntu</a> nos dan una guía muy útil para hacerlo desde Linux y en la <a href="https://www.openoffice.org/download/checksums.html" target="_blank">página de Apache OpenOffice</a> nos dan una guía algo más extensa en la que también se explica cómo hacerlo en Windows y Mac.

# Conclusión
Apenas he hablado sobre _privacidad_ en este post, a pesar de que está muy ligado a la ciberseguridad. No quería extender mucho la entrada y aburrir al lector, pero prometo escribir también sobre este tema.

Espero que con esta entrada hayas aclarado algo más algunos conceptos básicos sobre ciberseguridad y, a partir de ahora, actúes con más cuidado en la red.
