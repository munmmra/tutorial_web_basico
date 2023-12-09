# Tutorial básico de desarrollo web
Enlace del tutorial [Gettinng satarted whit the web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

# Estructura básica de archivos y carpetas
La estructura basica de un sitio web consta de
- el index o pagina de inicio <code>index.html</code>
- una carpeta para imagenes <code>images</code>
- una carpeta para estilos <code>styles</code>
- una carpeta para scripts <code>scripts</code>

## Estructura básica
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
# Elementos de una pagina web
Una página esta conformada por varios elementos estos pueden ser imagenes, texto, vinculos, videos, aduio, etc. estos elementos se define dentro de etiquetas que definel el tipo del que se trata.
## Imagenes
Las imagenes se muestran mediente la etiqueta ```<imag />``` dentro de esta se especifica la ubicación asi como otros atributos como puede ser el texto alternativo.
Ejemplo
``` html
    <img src="../images/fire-fox-icon.png" alt="Firefox logo: flaming fox wrapping the world" />
```
## Texto
### Encabezados
Los encabezados se especifican con las equetas ```<h1></h1>```(mas grabde) a la ```<h6><h6>``` (mas pequeña), y sirven para especificar títulos y subtítulos.
Ejemplo
``` html
<!-- 4 heading levels: -->
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
```
 ### Párafos
 Un párafo se especifica mediante la etiqueta ```<p></p>```, dentro especificamos el texto que contendra.  
 Ejemplo
 ``` html
 <p>Esto es un párafo</p>
```
 ### listas
Las listas se pueden definir de dos maneras ```<ul>``` (listas sin orden) o ```<ol></ol>```  
Ejemplo
``` html
<ul>
    <li>elemeto 1</li>
    <li>elemeto 2</li>
    <li>elemeto 3</li>
    <li>elemeto ..n</li>
</ul>    
<ol>
    <li>elemeto 1</li>
    <li>elemeto 2</li>
    <li>elemeto 3</li>
    <li>elemeto ..n</li>
</ol>
```
### vínculos
Los vínculos o enlaces a otras paginas se especifican medinate la etiqueta ```<a></a>```, en esta se 
deve de espcificar la ruta (local o externa), asi como el taxto que se mostrará.  
Ejemplo
``` html 
<a href="https://www.mozilla.org/en-US/about/manifesto/">Mozilla manifesto</a>
```
# Dando estilo, CSS básico
Los estilos se aplican a elemintos que son mostrados en la pagia estos se aplican mediante directivas CSS. Segun las buenas practicas
esto se hace en un archivo separado que contendrá toso los estyilos a aplicar.
## Añadiendo el archivo de estilos CSS
Para añadir el archivo que contendra los estilos se especifica una erferencia dentro de la etiqueta ```<head></head>.
Ejemplo
``` html
<head>
    ...
    <link href="styles/style.css" rel="stylesheet" />
    ...
</head>
```
## Anatomia de los estilos
Los estilos, tambien llamdos reglas se componen de:
- selector (define el elemento al que se le aplicara el estilo)
- declaración (define las propiedades y valores de estas propiedades que se aplicaran sobre los elemntos)
las estructura basica seria la siguiente.  
selector { propiedad1: valor; propiedad2: valor; ...} 

Ejemplo1 : establece todos los párafos de color rojo
``` css
p {
    color: red;
}
```
Ejemplo2 : establecer varias propiedades
``` css
p {
    color: red;
    width: 500x;
    border: 1px solid black
}
```
## Seleccionando multiples elementos
Para seleccionar multiples elementos, estos se deban agrupar en la parte del selctor separados por comas.  
Ejemplo
``` css
p,
li,
h1 {
  color: red;
}
```
## Diferentes tipos de sectores
Acontinuación se especifican algunos tipos de selectores  
| nombre del selector | función | ejemplo |
| ------------------: | :------| :------:|
| selector por elemento| selecciona todos los elementos del tipo especificado | p -> ```<p>``` |
| selector por id| selecciona el elementocon el ID especificado | #my-id -> ```<p id="my-id">``` |
| selector por clase | selecciona los elementos con la misma clase | .my-class -> ```<p class="my-class">``` |
| selector por clase | selecciona el o los elementos con el mismo atributo | img[src] ```<img src="myimage.png">``` |
| pseudo selector | selecciona el elemento pero solo cuando esta en un estado específico, por ejemplo cuando el raton esta sobre el | a:hover |

## Fuentes
Se pueden aplicar fuentes al texto, mediante un vínculo al archivo de la fuente, en la parte del ```<head></head>```  
Ejemplo
``` html
<head>
    ...
    <link
    href="https://fonts.googleapis.com/css?family=Open+Sans"
    rel="stylesheet" />
    ...
</head>
```
## Padding (relleno)
la distrubución en html se basa en un modelo tipo caja, por lo que cada elemento se puede visualizar como una caja con los siguientes atributos.  
- padding: el espacio entre la caja y el contenido de esta.
- border: el área de la caja
- margin: el espacio entre la caja y otras cajas o elementos


