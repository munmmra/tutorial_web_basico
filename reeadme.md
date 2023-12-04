# Tutorial básico de desarrollo web
## enlace del tutorial [Gettinng satarted whit the web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

# Estructura básica de archivos y carpetas
## La estructura basica de un sitio web consta de
- el index o pagina de inicio <code>index.html</code>
- una carpeta para imagenes <code>images</code>
- una carpeta para estilos <code>styles</code>
- una carpeta para scripts <code>scripts</code>

### Estructura básica
```
|-- index.html
|-- images
|-- styles
|-- scripts
```

# Estructura de una página web
Una página web esta compesta de etiquetas que de finien la estructura y los elementos que contiene
## Elementos básicos
los elementos básicos que debe contener una pagina web son, las etiquetas <code>```<!DOCTYPE html>```, ```<html></html>```, ```<head></head>``` y   ```<body></body>```</Code>.  
## La eqiqueta <code>```<doctype html>```</code>
Esta etiqueta especifica que el el archivo contendra código html dentro de el.
## La etiqueta <code>```<html></html>```</code>
Esta etiqueta marca el inicio de del contenido web, es qui donde tambien se especifica cual es el idioma que se usara en la pagina con el atributo ```lang```.  
ejemplo
```html
<html lang="en-US"></html>
```
pagina de referencia para los códigos de diferentes idiomas [lista](https://gist.github.com/JamieMason/3748498)  
## La Etiqueta ```<head></head>```
Esta etiqueta funciona como un contenedor para todos los elementos que no seran directamente visibles o desplegados en la página. Es aqui donde se cargan el tipo de caracteres que mostrara la página, el título de la página (el que semuestra en la pestaña del navegador), estilos de diseño o CSS que utilizará, el viewport (no se como traducirlo), entre otras cosas.  
Ejemplo
``` html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Test Page</title>
</head>
```
## La etiqueta ```<body></body>```
Esta etiqueta contiene todos los elementos que saran visibles en la página.
Ejemplo
``` html
<body>
    <img src="../images/firefox-icon.png" alt="Firefox logo: flaming fox wrapping the world" />
</body>
```
## Estructura completa
Ejemplo estructura basica de una página web
``` html
<!DOCTYPE html>
<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Test Page</title>
</head>
<body>
    <img src="../images/firefox-icon.png" alt="Firefox logo: flaming fox wrapping the world" />
</body>
</html>
```
