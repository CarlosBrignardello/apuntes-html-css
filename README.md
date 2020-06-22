

# HTML

El siguiente repositorio contiene mis apuntes respecto a HTML y CSS. Respectivamente este primer `Readme.md` contiene todos los apuntes sobre HTML. El resto de material sobre CSS se encuentra en el resto del repositorio.





### Conceptos básicos

HTML se basa en etiquetas, estas generalmente **comienzan por una etiqueta de apertura y finalizan con una etiqueta de cierre**. **Dentro de ellas suelen tener un contenido** que puede tratarse de texto o incluso de otra etiqueta, algo así como etiquetas hijos. También **dentro de una etiqueta existen atributos** **que se tratan de datos adicionales que se le otorgan a la etiqueta**.



**Sintaxis de HTML**

```html
<h1 id="texto-materia" class="materias"> Clases de HTML </h1>
```

| Elemento         | Nombre               | Descripción                                                  |
| ---------------- | -------------------- | ------------------------------------------------------------ |
| `<h1>`           | Etiqueta de apertura | La etiqueta de apertura es la que declara la etiqueta en cuestión. Generalmente suele finalizar con una etiqueta de cierre. |
| `id="" class=""` | Atributos            | Los atributos permiten definir las propiedades o características que tendrá una etiqueta, en este caso las más usadas son `id` y `class` las cuales están pensadas por un lado manipular la página dinámicamente mediante programación y definir los estilos de la misma. |
| Clases de HTML   | Contenido            | El contenido es lo que va entre las etiquetas, es lo que vuelve visible a las etiquetas dotándolas de texto que es visible en la página. También el contenido pueden ser otras etiquetas. |
| `</h1>`          | Etiqueta de cierre   | La etiqueta de cierra finaliza la etiqueta. Aunque existen etiquetas que se cierran por ellas mismas, como por ejemplo: `<img />`. Estas únicamente contienen atributos. NO pueden tener contenido. |



##### Estructura básica

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset=”utf-8”>
        <title>Título</title>
    </head>
    <body>
        
    </body>
</html>
```

* `<!DOCTYPE html>` : Existen muchas versiones de HTML, al añadir esta línea le indicamos al navegador que estamos trabajando un documento html5. **No es necesario utilizarlo en la mayoría de los casos.**

* `<html></html>` :  Este es el elemento principal, el padre de todo, NO existe ningún elemento que este por sobre esta etiqueta. Dentro de HTML existen dos elementos internos `<head>` y `<body>`. 

* `<head></head>` : Es usado para poner metadatos, por ejemplo el título del documento, el fabicon, descripción para Google, etc. La metada son datos que el navegador no muestra pero que procesa de todas maneras para distintos usos concretos. **Esto resulta fundamental a la hora de trabajar en el SEO de una página. Pero para el desarrollo como tal no es lo más fundamental.**
* `<body></body>` : Es usado para agregar todo el contenido que es mostrado en pantalla.





### Etiquetas básicas



**Encabezados**

Los encabezados o headings son utilizados para denotar títulos y definir la jerarquía de una publicación. Pese a que existen seis etiquetas de encabezados y todas ellas van de mayor a menor los encabezados no tienen nada que ver con el tamaño. 

```html
<h1>Hola soy un encabezado</h1> 
<h2>Hey</h2> 
	...
<h6>Toy chiquito :c</h6>
```



**Parrafos**

Los párrafos suelen ser utilizados acompañados de los encabezados, estos simplemente son la fuente de texto principal de los sitios, existe una alternativa denominada `<span>` que es utilizada para manipular valores o variables en su interior. Aunque los párrafos pueden cumplir la misma función. 

```html
<h2>Presentación</h2>
<p>Hola soy Carlos.</p>
<p>lorem....</p>
```

> En editores de código como Visual Studio Code es posible generar texto en latín para utilizarlo como template. Se puede generar de las siguientes maneras: `lorem`, `lorem30`, `lorem*5`. 



**Etiquetas de sección:** Son aquellas que dividen la página en bloques. Por defecto siempre se ha utilizado la etiqueta  `<div>`. En si las etiquetas de sección son simplemente `<div>` con otros nombres para ayudar a mejorar la estructura y el desarrollo de los sitios. En si todos son contenedores.

```html
<html>
  <head>
    <meta charset=”utf-8”>
    <title>Título</title>
  </head>
  <body>
        
    <header>
      ...
    </header>
      
    <nav>
      ...  
    </nav>
      
    <main>
      ...  
    </main>
      
    <div>
      ...
    </div>
      
    <section>
      ...
	</section>
      
    <article>
	  ...
    </article>

    <aside>
	  ...
    </aside>

    <footer>
      ...
    </footer>
        
  </body>
</html>
```

> En si las secciones más utilizadas son: main, header, footer, nav y section. 

| Contenedor  | Uso                                                          |
| ----------- | ------------------------------------------------------------ |
| `<div>`     | Se trata del contenedor por defecto, es utilizado para definir estilos a un conjunto de etiquetas y ordenar el documento. |
| `<header>`  | Es utilizado para definir la zona superior de los sitios en general utilizada para generar una barra de navegación con los enlaces más importantes del sitio. |
| `<main>`    | Se utiliza para definir el contenido principal de una página. |
| `<nav>`     | Se utiliza para definir en su interior una barra de navegación con listas. |
| `<footer>`  | Se utiliza para trabajar el final de las páginas generalmente dedicado a incluir créditos y enlaces. |
| `<section>` | Se utiliza para definir secciones de una web.                |
| `<aside>`   | Se utiliza para contenido no relacionado con la página, como puede ser publicidad u otra información. |
| `<article>` | Es un elemento de contenido único, por ejemplo artículos de blogs, tutoriales, publicaciones, etc. |





### Listas

Las listas sirven para enumerar, un ejemplo sería una lista de tareas, las listas pueden ser de dos tipos:

* `<ul>`(Unordered list): Es un tipo de lista que por cada elemento interno agrega un bullet o punto.
* `<ol>`(Ordered list): Es un tipo de lista que cada elemento lo va numerando.
* `<li>`(List Item): Es el elemento interno de las listas, en el se indican el contenido de la lista.

```html
<ul>
    <li>Item de lista 1</li>
    <li> Item de lista 2
        <ol>
            <li>Sub item de lista 1</li>
            <li>Sub item de lista 2</li>
        </ol>
    </li>
    <li>Item de lista 3</li>
</ul>

<ol>
	<li>Carlos</li>
    <li>Damaris</li>
</o>
```

> Se puede cambiar la numeración por letras por ejemplo, o el diseño de la lista en si, esto se hace con CSS.
>



**Barras de navegación**

Las listas son usadas por ejemplo para crear barras de navegación acompañadas de varias otras etiquetas.

```html
<header>
	<nav>
        <h2>LOGOTIPO</h2>
        <ul>
            <li>
                <a class href="/home">Inicio</a>
            </li>
            <li>
                <a class href="/projects">Proyectos</a>
            </li>
            <li>
                <a class href="/contact">Contacto</a>
            </li>
        </ul>
    </nav>
</header>

```







### Rutas

Existen varios tipos de rutas, absolutas, relativas, relativa a la raíz, etc. Un enlace es un trozo de texto o incluso imagen, en todo caso se trata de un hipertexto que te lleva a otra parte. Todo eso se define con la ruta, primero se requiere del atributo **href** con ese atributo se indicara hacia donde va.

**Existen dos tipos de rutas:**

- Rutas absolutas: Son rutas únicas que no se repetirán nunca, estas siempre comienzan por un protolo(http, https, etc.).

* Rutas relativas: Las rutas relativas dependen de las carpetas, su ubicación, etc. Es aconsejable incluir “./” cuando se trata de una carpeta que se encuentra en el directorio actual, para acceder a carpetas superiores, sin necesidad de escribir su nombre usamos “../”.

```html
<!-- Ruta Absoluta -->
<a href="https://ed.team">Página de EdTeam</a>

<!-- Ruta relativa, misma carpeta -->
<a href="usuarios.html"Usuarios></a>
<a href="./usuarios.html"></a>

<!-- Ruta relativa, carpeta superior -->
<a href="../usuarios.html">Usuarios</a>

<!-- Ruta relativa, dos carpetas arriba y subcarpeta -->
<a href="../../usuarios/usuarios.html"></a>

<!-- Ruta relativa a la raiz -->
<a href="/usuarios.html">Usuarios</a>

```







### Imágenes y enlaces



**Imágenes**

Para declarar imágenes utilizamos la etiqueta `<img />` estas en su interior comprenden los atributos `src` y `alt`. Los cuales sirven para especificar la dirección de la imagen y el texto alternativo que se renderiza cuando la imagen no logra cargar.

```html
<img src="./img/yo.jpg" alt="Mi imagen" />
```

> Las imágenes pueden ser direcciones web.



**Enlaces**

Los enlaces permiten re enviar a sitios internos y externos al sitio web. También permiten diseñar botones gracias a su uso con imágenes o textos.

```html
<!-- Enlace convencional -->
<a href="https://www.google.cl">Ir a Google</a>

<!-- Enlace con etiqueta de contenido -->
<a href="https://www.google.cl">
  <img src="./img/google.jpg" alt="Google">
</a>
```





 

### Tablas

Las tablas se utilizan con el elemento `<table>`, existen varios otros elementos con los que interactuar entre ellos:

| Etiqueta    | Descripción                                           |
| ----------- | ----------------------------------------------------- |
| `<caption>` | Permite indicar un titulo a la tabla.                 |
| `<tr>`      | Define un fila.                                       |
| `<thead>`   | Define la parte superior de la tabla.                 |
| `<tbody>`   | Define el cuerpo de la tabla.                         |
| `<th>`      | Define el contenido de la parte superior de la tabla. |
| `<td>`      | Define el contenido de la parte inferior de la tabla. |

```html
  <table>
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Lunes</th>
            <th>Martes</th>
            <th>Miercoles</th>
            <th>Jueves</th>
            <th>Viernes</th>
            <th>Sabado</th>
            <th>Domingo</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Ejercicio</td>
            <td>x</td>
            <td>x</td>
            <td>x</td>
            <td></td>
            <td>x</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Estudio</td>
            <td>x</td>
            <td>x</td>
            <td></td>
            <td></td>
            <td>x</td>
            <td>x</td>
            <td></td>
        </tr>
    </tbody>
  </table>
```





### Formularios

Los formularios permiten enviar y recibir data del Usuario, hasta ahora hemos visto como marcar y estructurar contenido. Esos datos son recibidos y procesados por un servidor, mediante PHP o Javascript, por ejemplo y a la vez valida estos formularios. Es importante pues mediante programas se pueden rellenar formularios de forma fraudulenta.

HTML tiene algunas herramientas de validación pero estas son básicas y son fáciles de burlar, sin embargo de todas formas lo aprenderemos.

Primero tenemos la etiqueta `<form>`, esta misma tiene un atributo llamado action, este indica por DOM que archivo va a procesar este formulario. Por ejemplo `<form action="form.php">`. 

Adicionalmente dentro de los formularios tenemos campos, cada campo es cada elemento donde se reciben datos, el más básico de ellos es la etiqueta <input> que es donde el usuario pone datos. Existen muchos tipos de `<input>`, orientados a muchos tipos de valores, de ahí viene el detalle de la validación. Por ejemplo si se quiere que un usuario ponga un RUT, estableceremos en la validación que el valor obtenido debe ser solo numérico. 

El input más común es el de tipo texto, este se define así: `<input type="text">`
 Podemos añadir además un botón con: `<button>Enviar</button>`. Tenemos también la etiqueta `<label>`, la cual añade una información sobre lo que necesitamos enviar, generalmente está acompañado de un atributo for el cual conecta la etiqueta `<label>` con la etiqueta `<input>`.

Otra forma es introduciendo el `<input>` dentro del `<label>`, de esa forma evitamos el uso de los id y los for. A la hora de trabajar con servidores y bases de datos, es obligatorio declarar dentro del `<input>` el atributo name, el cual permite clasificar, llamar o identificar el elemento desde la base de datos.

Podemos añadir también otro formulario y que esta vez sea una entrada de tipo contraseña, con `<input type="password">`

**Nota**: Podemos corroborar que está relacionado un `<label>` con un `<input>`, haciendo clic en el texto del `<label>`, nos debería introducir al espacio de texto del `<input>`.

Si revisamos nuestro formulario veremos que ambos `<input>` están en una misma línea y no uno debajo del otro, existen muchas soluciones pero en este caso podemos utilizar la etiqueta `<div>`. También podríamos usar <br> pero esa última es una opción menos elegante.

Disponemos también de otro tipo de `<input>` el cual inmediatamente añade un botón, lo hacemos con: `<input type="submit" value="x">`.

**Nota**: En los `<input>` el atributo `value` es el dato que esta contenido, generalmente este se obvia pues es el usuario quien debe rellenarlo, aunque en ocasiones puede resultar útil, poner datos por el usuario, para hacer más cómoda su experiencia. Atravez del atributo value mediante JavaScript podemos leer lo que está escribiendo el usuario en tiempo real.

Para ello añadimos un script y ponemos:

```js
         document.getElementById('username')
        .addEventListener('keyup', e =>{
            console.log(e.target.value)
        })
```

Seleccionamos un elemento mediante su id y escuchamos un evento en este caso el evento sera “keyup”, que se acciona cada vez que un usuario suelta una tecla. Le asignamos nombre al evento y luego obtenemos el valor de ese evento.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Formularios</title>
</head>
<body>
    <h1>Formularios</h1>
    <form action="">

        <div>        
            <label>
                Input de Texto
                <input name="username" type="text" id="username" placeholder="Tú nombre">
            </label>
            <button>Enviar</button>
        </div>

        <div>
            <label>
                Input de Contraseña
                <input name="passwd" type="password" placeholder="*******">
            </label>
            <button>Enviar</button>
        </div>

        <div>
            <label>
                Input de email
                <input type="email" placeholder="example@gmail.com">
            </label>
            <button>Enviar</button>
        </div>

        <div>
            <label>
                Input de fecha
                <input type="date">
            </label>
            <button>Enviar</button>
        </div>

        <div>
            <label>
                Input de números
                <input type="number" placeholder="0">
            </label>
            <button>Enviar</button>
        </div>

        <script>
            document.getElementById('username')
            .addEventListener('keyup', e =>{
            console.log(e.target.value)
            })
        </script>

    </form>
</body>
</html>
```



**Otros tipos de Input**

Atributo placeholder: Con este atributo podemos agregar un texto de ejemplo dentro de cada input.

`<input type="email">`: Es un input utilizado para correos, de forma nativa algunos navegadores lanzaran una advertencia genérica si un usuario introduce un valor distinto al de un correo convencional.

`<input type="number">`: Input que incluye un layout de flechas para incrementar o decrementar la cantidad, por su aspecto basico, es recomendable no utilizarlo 

**Nota**: Recordemos que las validaciones con HTML son muy simples, básicamente son solo ayudas pues son muy fáciles de burlar. Desde un navegador se puede perfectamente modificar el elemento del formulario para convertir el input de tipo “email” a tipo “text” y de esa forma enviar la información de todas maneras.

**CONSEJO**: Recordemos que los `<input>` deben ser nombrados con el atributo name para que desde el backend se puedan gestionar dichos datos.



**Campos de selección y atributos**

Al diseñar web se debe pensar en la experiencia de usuario, con el fin de no confundir ni aburrir a un usuario.

* `<fieldset>`: permite introducir varios campos en una especie de contenedor o trazo.
* ` <legend>`: permite agregar una leyenda a la etiqueta `<fieldset>`, se ve muy atractivo.
* `<input type="checkbox">`: Se trata de un `<input>` para el uso de checklists.
* `<input type="radio">`: se trata de un cheklist circular. 
* `<select>`: Permite mostrar una lista desplegable de opciones. Podemos agregar el atributo multiple para permitir la selección de varias opciones al presionar Ctrl, no es muy recomendado, preferible el uso de un checkbox.
* `<optgroup>`: Permite segmentar las listas, es usado para ayudar al usuario.
* `<option>`: Se utiliza dentro de `<select>` para agregar elementos a la lista.

**Consejo**: Si queremos que un checklist pueda ser seleccionado solo una vez, debemos agregar en la etiqueta `<input>` el mismo atributo name para todos los elementos.



**Atributos importantes**

* **required**: Vuelve obligatorio un campo en específico, por ejemplo en el `<input>` de contraseña, es recomendable adicionarlo.

* **readonly**: Niega la opción de modificar un `<input>`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Formularios</title>
</head>
<body>
    <h1>Formularios</h1>
    <form action="">
        <fieldset>
            <legend>Tipos de formulario</legend>
            <div>        
                <label>
                    Input de Texto
                    <input name="username" type="text" id="username" placeholder="Tú nombre">
                </label>
            </div>

            <div>
                <label>
                    Input de Contraseña
                    <input name="passwd" type="password" placeholder="*******">
                </label>
            </div>

            <div>
                <label>
                    Input de email
                    <input type="email" placeholder="example@gmail.com">
                </label>
            </div>

            <div>
                <label>
                    Input de fecha
                    <input type="date">
                </label>
            </div>

            <div>
                <label>
                    Input de números
                    <input type="number" placeholder="0">
                </label>
            </div>

        </fieldset>

        <fieldset>
            <legend>Intereses</legend>
            <div>
                <label><input type="checkbox">Música</label>
                <label><input type="checkbox">Cursos</label>
                <label><input type="checkbox">Vida sana</label>
                <label><input type="checkbox">Arte</label>
            </div>
        </fieldset>

        <fieldset>
            <legend>Sexo</legend>
            <div>
                <label><input type="radio" name="gender">Mujer</label>
                <label><input type="radio" name="gender">Hombre</label>
                <label><input type="radio" name="gender">Prefiero No decirlo</label>
            </div>
        </fieldset>

        <fieldset>
            <legend>Nacionalidad</legend>
            <label for="country">Selecciona tu país</label>
            <select name="country" id="country">
                <optgroup label="America Latina">
                    <option value="cl">Chile</option>
                    <option value="mx">Mexico</option>
                    <option value="ar">Argentina</option>
                </optgroup>

                <optgroup label="Europa">
                    <option value="es">España</option>
                    <option value="it">Italia</option>
                    <option value="fr">Francia</option>
                </optgroup>

            </select>
        </fieldset>

        <button>Enviar</button>

        <script>
            document.getElementById('username')
            .addEventListener('keyup', e =>{
            console.log(e.target.value)
            })
        </script>

    </form>
</body>
</html>
```



































#### Otros elementos

La etiqueta `<main>` es posiblemente la más importante en una página web, es donde se guarda el contenido más importante, debe haber uno en cada página, en el ejemplo simplemente tenemos un párrafo y un `<hr>` o Horizontal rule que sirve para hacer un cambio de sección, de capitulo o de significado.

 

`<blockquote>` se utiliza para hacer citas un poco más destacadas, se puede utilizar para resaltar pedazos de artículos y demás.

```
<main>
    <p>Este es el contenido anterior, a continuación se utiliza un hr para hacer un salto de pagina.</p>
    <hr>
    <pre>
        Este texto se ve igual 
            a como fue escrito en el editor
                        que en el navegador.
    </pre>
    <blockquote>
        Se utiliza blockquote para destacar las citas.
    </blockquote>
</main>
```

`<div>`: se utiliza para dividir contenido ,es uno de los elementos más incomprendidos debido a que se suele caer en malas prácticas con él, como por ejemplo usarlo demasiado o usarlo muy poco. Se trata de una etiqueta que no significa nada, existen dos etiquetas que no significan
nada `<div>` y `<span>`, están hechas para ser contenedores para luego poder ser manipuladas pro JavaScript o CSS. 



En el ejemplo tenemos un código para imprimir un usuario, en una aplicación en la que quisiéramos mostrar a varias usuarios, cada uno de estos usuarios estarían contenidos en un archivo y serian mostrados al llamar al archivo. Los atributos `class` son utilizados posteriormente por CSS, para otorgar diseño. En general los `<div>` suelen ser usados para luego por CSS modificarlos. Si vas a utilizar CSS y JavaScript. Es aconsejable utilizar entonces `<div>`.

```html
<div class="user">
    <div class="user_name">
        <p>Carlos Brignardello</p>
    </div>
    <div class="user_image">
        <img src="cbrignardello.jpg" alt="Una foto de Carlos Brignardello">
    </div>
</div>
```

**CONSEJO:** Con la combinación `<alt>` + `<shift>` + `<flecha abajo>`, podemos
duplicar una línea completa automáticamente.


