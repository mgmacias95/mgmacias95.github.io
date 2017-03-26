---
layout: post
title: "Cómo instalar paquetes en LaTeX"
date: 2017-03-26
excerpt: "Instalando paquetes en LaTeX de forma correcta"
tags: [latex]
comments: false
---

# Motivación
Muchos nos hemos descargado alguna vez algún `.sty` de internet para poder hacer unos documentos LaTeX más completos y, al no saber cómo instalarlos, los hemos dejado en la misma carpeta que nuestro documento. Esto está  bien si sólo vamos a usar dicho paquete una vez, pero si nuestra intención es empezar a usarlo más veces debemos considerar _instalar_ el paquete en nuestro sistema.

# Cómo se hace
En [Wikibooks](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages) nos explican cómo instalar paquetes. En mi caso, para instalar un `.sty` que he descargado de internet he tenido que seguir los siguientes pasos:

1. Crear una carpeta con el mismo nombre que el paquete en `/usr/local/share/texmf`:
    ```bash
    $ cd /usr/local/share/texfm
    $ mkdir paquete
    ```

2. Copiar el `.sty` que me he descargado a la carpeta:
    ```bash
    $ mv ~/Downloads/paquete.sty paquete/
    ```

3. Actualizar la base de datos de paquetes de LaTeX (en mi caso, _TeX Live_):
    ```bash
    $ sudo texhash
    ```

Y ya está! Espero que os haya servido de ayuda y que dejéis de hacer la ``chapuza'' de poner el `.sty` en el mismo directorio que el `.tex`.
