# Calculadora
En este proyecto encontraras una calculadora basica con diseño responsive
# Como crear una Calculadora responsive con HTML y css

Antes de iniciar te quiero informar que para un mejor desarrollo te recomiendo que tengas instalado vs code y su complemento live server para ver en tiempo real lo que estas realizando sin necesidad de actualizar la pagina.
A lo largo de este camino pondrás en practica los siguientes conceptos básicos:
- HTML semantico
- Resetear estilos css
- Medida relativa rem
- Modelo de cajas
- Display flex
- Selectores universales
- Selectores combinados
- Pseudo clases
- @media.

# Paso 1

Para empezar vamos a crear un archivo con nombre “calculadora.html”, una vez creado este archivo escribiremos html:5 y daremos enter para que nuestro editor se encargue de crearnos nuestra estructura base de HTML5.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```


# Paso 2

Dentro de nuestra etiqueta (body) crearemos una etiqueta (main) que nos representara el cuerpo físico de nuestra calculadora; luego dentro de main, crearemos dos etiquetas (header) para representar insertar el cuadro de texto donde realizaremos las operaciones y (section) que es donde insertaremos nuestros botones a la etiqueta section le agregaremos el atributo (class) con valor (botones) que usaremos mas adelante en nuestra hoja de estilos.
```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
</head>
<body>
    <main >
        <header>
        </header>
        <section class="botones">
            
        </section>
    </main>
</body>
</html>
```

# Paso 3

 Dentro de nuestro header crearemos un input de tipo (text) al cual le asignaremos do atributos (class) con valor (resultado) y (aria-label) en donde colocaremos una pequeña descripción de nuestro componente. NOTA: el atributo (aria-label) es usado para brindar un plus de accesibilidad a nuestra pagina tal como ocurre con el atributo (alt) que se usa en las imágenes para generar una descripción
```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
</head>
<body>
    <main >
        <header>
            <input type="text" readonly class="resultado" aria-label="Cuadro donde veremos las operaciones y resultados">
        </header>
        <section class="botones">
         
        </section>
    </main>
</body>
</html>
```
# Paso 4

Dentro de nuestra etiqueta section crearemos dos etiquetas (section)  con su atributo (class) donde la primera tendrá el valor de (numeros) y la segunda tendrá el valor de (operadores)
```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
</head>
<body>
    <main >
        <header>
            <input type="text" readonly class="resultado" aria-label="Cuadro donde veremos las operaciones y resultados">
        </header>
        <section class="botones">
            <section class="numeros">
            </section>
            <section class="operadores">
            </section>
        </section>
    </main>
</body>
</html>
```
# Paso 5

Dentro de la (section) de (class) numeros crearemos 15 botones en donde a cada uno de daremos un valor numérico del 0 al 9 y a su vez crearemos 5 botones que podremos usar para ajustar nuestras operaciones. Aplicando nuestro plus de accesibilidad, recomiendo usar el atributo (aria-label) para cada botón y asignarle su descripción especifica.
```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
</head>
<body>
    <main >
        <header>
            <input type="text" readonly class="resultado" aria-label="Cuadro donde veremos las operaciones y resultados">
        </header>
        <section class="botones">
            <section class="numeros">
                <button aria-label="boton numero cero">0</button>
                <button aria-label="boton punto separador">.</button>
                <button aria-label="boton para eliminar 1 caracter">C</button>
                <button aria-label="boton numero uno">1</button>
                <button aria-label="boton numero dos">2</button>
                <button aria-label="boton numero tres">3</button>
                <button aria-label="boton numero cuatro">4</button>
                <button aria-label="boton numero cinco">5</button>
                <button aria-label="boton numero seis">6</button>
                <button aria-label="boton numero siete">7</button>
                <button aria-label="boton numero ocho">8</button>
                <button aria-label="boton numero nueve">9</button>
                <button aria-label="boton numero para resetear la calculadora">AC</button>
                <button aria-label="boton para abrir y cerrar parentesis">( )</button>
                <button aria-label="boton de porcentaje">%</button>
            </section>
            <section class="operadores">
            </section>
        </section>
    </main>
</body>
</html>
```
# Paso 6

Dentro de nuestra etiqueta (section) con (class) operadores crearemos 5 botones los cuales serán nuestros operadores, recuerda utilizar el atributo (aria-label)
```
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
</head>
<body>
    <main >
        <header>
            <input type="text" readonly class="resultado" aria-label="Cuadro donde veremos las operaciones y resultados">
        </header>
        <section class="botones">
            <section class="numeros">
                <button aria-label="boton numero cero">0</button>
                <button aria-label="boton punto separador">.</button>
                <button aria-label="boton para eliminar 1 caracter">C</button>
                <button aria-label="boton numero uno">1</button>
                <button aria-label="boton numero dos">2</button>
                <button aria-label="boton numero tres">3</button>
                <button aria-label="boton numero cuatro">4</button>
                <button aria-label="boton numero cinco">5</button>
                <button aria-label="boton numero seis">6</button>
                <button aria-label="boton numero siete">7</button>
                <button aria-label="boton numero ocho">8</button>
                <button aria-label="boton numero nueve">9</button>
                <button aria-label="boton numero para resetear la calculadora">AC</button>
                <button aria-label="boton para abrir y cerrar parentesis">( )</button>
                <button aria-label="boton de porcentaje">%</button>
            </section>
            <section class="operadores">
                <button aria-label="boton para sumar">+</button>
                <button aria-label="boton para restar">-</button>
                <button aria-label="boton para multiplicar">*</button>
                <button aria-label="boton para dividir">/</button>
                <button aria-label="boton dar el resultado">=</button>
            </section>
        </section>
    </main>
</body>
</html>
```

Como puedes observar hasta el momento hemos construido nuestra calculadora básica con html semántico; pero visualmente no se parece a una, es por eso que a partir de ahora nos adentraremos en CSS para darle el retoque visual que deseamos. Como una buena practica para un diseño responsive te recomiendo iniciar la construcción de la visual por la pantalla mas pequeña (mobile), después realizaras pequeños ajustes para adaptar tu diseño a tablet y por ultimo lo realizaras para equipos de escritorio.

# Paso 7

Para crear nuestro diseño responsive es necesario que crees un archivo con el nombre (style.css) y dentro de nuestro archivo html agregue la siguiente etiqueta (<link rel="stylesheet" href="style.css”>) después de la etiqueta (title) con el fin de enlazar nuestra hoja de estilos. Antes de iniciar nuestra construcción de estilos es necesario un reset de los estilo por defecto que maneja el navegador, con este reset dejaremos el padding y margin con valor de 0 y asignaremos el atributo (box-sizing) con valor de border-box esto es usado con el fin de dar un tamaño fijo a nuestros componentes sin importar el valor de su padding, border y contenido.
Para el manejo de la medida relativa rem te recomiendo reestructurar el tamaño del Font-size raiz a 10px.
```
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
html{
    font-size: 62.5%;
}
```
# Paso 8

Usaremos selectores de tipo, combinados (tipo tipo), de clase y combinados (clase tipo)  para dar el diseño que tendrá nuestra calculadora en mobile, también usaremos la pseudo clase (:active) para dar un comportamiento a cada botón cuando se da clic.
```
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
html{
    font-size: 62.5%;
}
main{
    margin: auto;
    width: 100%;
    height: 100vh;
    padding: 1%;
    background: rgb(39, 39, 43);
}

section{
    gap:5%;
}
header{
    height: 20%;
    margin-bottom: 2%;
}
header input{
    height: 100%;
    width: 100%;
}
.botones{
    height: 78%;
    display: flex;
    padding: 5%;
}
button{
    font-size: 3rem;
    border-radius: 50%;
    flex-grow: 1;
}
.numeros{
    display: flex;
    flex-wrap: wrap-reverse;
    width: 75%;
}
.numeros button{
    width: 30%;
    background: rgb(98, 98, 100);
    color: white;
}

.numeros button:active,.operadores button:active{
    transform: scale(0.8);
}

.operadores{
    width: 25%;
    display: flex;
    flex-direction: column;
}
.operadores button{
    background: rgb(242, 163, 60);
    color: white;
}
```
En el código anterior veras que usamos: 
1. Medidas relativas como (% y rem)
2. Modelo de cajas añadiendo (width,height,border y padding)
3. Display flex con sus atributos:
    1. Gap (separador entre elementos hijos)
    2. Flex-wrap (ajuste de los elementos hijos al contenedor)
    3. Flex-direction (asigna la dirección en la cual se pintaran los hijos)
    4. Flex-grow (especifica el tamaño en proporción que tendrá el elemento hijo, en este caso todos serán iguales)
4. Pseudo clase active para dar un comportamiento a cada botón cuando se da click, para este caso usamos el atributo transform con un valor se scale 0.8 que le indica que el botón reducirá su tamaño un 20%

# Paso 9

Usando la etiqueta @media con su atributo (min-width) le vamos a especificar a nuestro css a partir de que tamaño en pixeles deberá cambiar su diseño, el mas pequeño indica un comportamiento en tablets y el mas grande en dispositivos de escritorio.
```
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
html{
    font-size: 62.5%;
}
main{
    margin: auto;
    width: 100%;
    height: 100vh;
    padding: 1%;
    background: rgb(39, 39, 43);
}

section{
    gap:5%;
}
header{
    height: 20%;
    margin-bottom: 2%;
}
header input{
    height: 100%;
    width: 100%;
}
.botones{
    height: 78%;
    display: flex;
    padding: 5%;
}
button{
    font-size: 3rem;
    border-radius: 50%;
    flex-grow: 1;
}
.numeros{
    display: flex;
    flex-wrap: wrap-reverse;
    width: 75%;
}
.numeros button{
    width: 30%;
    background: rgb(98, 98, 100);
    color: white;
}

.numeros button:active,.operadores button:active{
    transform: scale(0.8);
}
.operadores{
    width: 25%;
    display: flex;
    flex-direction: column;
}
.operadores button{
    background: rgb(242, 163, 60);
    color: white;
}
@media (min-width: 481px) {
   
    button{
        border-radius: 20%;
        font-size: 5rem;
    }
}
@media (min-width: 1025px) {
    .numeros button:hover, .operadores button:hover{
        transform: scale(1.2);
        cursor: pointer;
    }
    .numeros button:active,.operadores button:active{
        transform: scale(0.9);
    }
    section, .botones{
        gap:0%;
    }
    button{
        border-radius: 0%;
        font-size: 7rem;
    }
}
```
Cómo puedes observar en nuestro dispositivo de escritorio usamos la pseudo clase hover para generar un comportamiento visual cuando el mouse se encuentre sobre nuestros botones.  Quiero felicitarte por llegar al final de nuestro recorrido en donde pusiste en practica multiples conceptos de html y css que de a poco le fueron dando vida a tu calculadora, siempre ten presente que la practica hace al maestro y que los diseños pueden variar según tu creatividad esta fue solo una guía espero ver en tu practica diseños mejores y mas innovadores
