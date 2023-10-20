# Taller: Desarrollo de aplicaciones web SPA con el framework Angular

## Introducción

Bienvenido al taller de desarrollo de aplicaciones web con Angular. Este README file será la referencia necesaria para poder realizar el curso de una manera ordenada y sencilla. Todo el código que escribiremos en el taller estará reflejado en este archivo. Si en algún momento te quedas atrás o quieres repasar en un futuro lo aprendido, este es el sitio.

## Parte 1: Creando un nuevo proyecto de angular

Para poder comenzar con el desarrollo de nuestro curso, es importante que hayas instalado NodeJS y Angular en tu dispositivo (Esta instalación fue relizada presencialmente en el curso o previamente siguiendo la guía de instalación de las tecnologías que se requerían para el curso). Si aún no lo tienes instalado te invito a que pauses el aprendizaje de esta guía y los instales para poder proceder a partir de este punto.

### Versión de este proyecto

Antes que nada y para cuestiones de revisión y referencia, identificaremos las versiones con las que estamos trabajando (además de que verificaremos que todos tengamos los programas necesarios).

#### Revisar versión de nodeJS

Para identificar la versión sobre la cual estamos trabajando debemos de ejecutar el comando

```bash
node --version
```

Si la respuesta de este comando es un error, significa que no tienes NodeJS instalado o que no está bien instalado si es que ya lo realizaste. La respuesta correcta debería ser una versión. En el caso de este tutorial se está realizando con la version:

```bash
v16.20.0
```

**ATENCIÓN: No es necesario que tu versión sea exactamente la misma, puede ser superior o inferior. Solo funciona de referencia en caso de algún problema de compatibilidad.**

#### Revisar la versión de NPM

NPM es un manejador de paquetes que es instalado a la par de la instalación de NodeJS, es decir, en una sola instalación vienen ambos, y es el encargado de manejar y descargar las dependencias necesarias para que nuestro proyecto funcione de la forma en que esperamos.

Para revisar la versión de NPM que tenemos instalada deberemos de correr el comando:

```bash
npm --version
```

Esto nos dará la versión con la que contamos, en el caso de este tutorial la versión es:

```bash
8.19.4
```

#### Revisar la versión de Angular

Si no haz instalado angular, recuerda hacerlo con el comando:

```bash
npm install -g @angular/cli
```

Si ya lo tienes instalado, ejecuta el comando:

```bash
ng version
```

Para conocer la versión en la que te encuentras, en el caso de este tutorial, se está utilizando la versión:

```bash
16.2.9
```

**ATENCIÓN: Es necesario que estos tres comandos te hayan regresado alguna versión, esto nos asegura de que tienes todo instalado y listo para iniciar con el curso.**

## Creando nuestro primer proyecto en Angular.

Inicializar un proyecto desde la linea de comandos es muy sencillo y practivo, para ello utilizaremos el comando dedicado para la incialización de proyectos `ng new`. Este comando recibe como parametro el nombre de nuestra aplicación. Es importante que al nombrar nuestra aplicación sigamos los estandares de NodeJS para el nombre de los proyectos, lo recomendable es usar `kebab-case`. ¿Qué es kebab case? Es un tipo de nomenclatura (como si nombraras variables) donde cada palabra va separada por un `-`. Por ejemplo si tu aplicación que deseas crear fuera acerca de una tienda de ropa, la llamarías `proyecto-tienda-ropa`, este tipo de separación entre palabras de un nombre de proyecto se le llama `kebab-case`. Preferible no usar acentos, solo carácteres alfanúmericos y guiones.

Para el caso de nuestro proyecto utilizaremos un nombre bastante sencillo `taller-angular`. Simple y especifico para lo que vamos a realizar. Entonces para crear un nuevo proyecto sigamos los siguientes pasos:

1. Muevete a un folder que contendrá los proyectos de este taller, tiene que ser un folder donde vayas a guardar tus proyectos. **Aun no es el folder del proyecto, no lo vayas a llamar taller-angular para evitar confusiones**, puedes llamarlo `tutoriales`, `proyectos`, `aprendizaje`. Como gustes.

```bash
cd ./tu/carpeta/donde/quieres/guardar/tus/proyectos
```

2. Una vez dentro de tu carpeta de proyectos, aquí si ya realizaremos la creación de nuestro proyecto `taller-angular`. ¿Cómo le haremos entonces? Muy sencillo, ejecuta el comando `ng new` seguido del nombre de proyecto que acabamos de decir.

```bash
ng new taller-angular
```

y presiona Enter para ejecutar el comando.

Este `ng new taller-angular` te hará un par de preguntas:
1. ¿Quieres agregar angular routing a tu aplicación?: Le responderemos que no.
2. ¿Que tipo de estilos quieres agregar a tu aplicación?: CSS, si sabes manejar otro usa otro pero en este caso usaremos CSS para no complicarnos demasiado.

Una vez termine las preguntas comenzará a installar las dependencias finales de tu proyecto. Dejalo terminar de descargar y **no lo interrumpas**.

Una vez que termine de instalar las dependencias estamos listos con nuestro nuevo proyecto de angular, solo nos queda ingresar a el.

```bash
cd taller-angular
```

## Ejecutando el proyecto

Ya estamos listos para comenzar. Los comandos anteriormente ejecutados han sido para crear la aplicación como ya se menciono, esta aplicación ya contiene contenido pregenereado, para levantar el servidor en el cual vamos a visualizar los cambios que haremos, debemos ejecutar el siguiente comando:

```bash
ng serve
```

Esto, levantará un servidor de desarrollo en el cual estaremos visualizando lo que estemos trabajando, abre la ruta que te indica y deberías de poder visualizar la aplicación. Mantén esta pestaña de tu navegador abierta por que ahí estaremos trabajando.

Ahora, presta atención a tu instructor, o investiga si no estás en el taller, acerca de los siguientes temas:

- Que es Angular ng serve
- Que es hot reload en Angular
- Como hacer cambios en una aplicación de Angular
- Como se reflejan los cambios en Angular.

Es muy importante conocer estos conceptos antes de comenzar a desarrollar, debido a que tendremos en claro principios básicos de desarrollo de aplicaciones en Angular.

## Limpiando la aplicación por defecto.

Como podemos visualizar en nuestra aplicación, tenemos una gran cantidad de contenido pre-generado, presta atención a tu instructor o investiga en caso de que no te encuentres en el taller acerca de como está conformada la estructura de archivos de un proyecto de angular.

Una vez terminada la explicación continuemos.

### Limpiando la vista y haciendo un Hello World.

Para limpiar la vista de todo el contenido generado, deberemos de abrir el archivo que se encuentra en la ruta `src/app/app.component.html`. Este archivo es la vista predeterminada que estamos visualizando. Una vez abierto el archivo **Borra todo el contenido de este HTML**.

Una vez borrado **Todo el contenido** agrega una etiqueta `h1` a tu `src/app/app.component.html`. con el contenido `Hola mundo`

```html
<h1>Hola mundo</h1>
```

Listo, ya tenemos nuestra vista lista para comenzar a practicar. ¿Viste como se actualizó automaticamente? Eso es el hot reloading y es muy util cuando estamos desarrollando.

A continuación tu instructor explicará un poco acerca del concepto, funcionamineto y la relación de `template`, `styles ` y `component` que son conceptos basicos y muy importantes acerca de como funciona Angular. Presta atención.

## Ininiciando nuestra primera aplicación.

Nuestra primera aplicación será un sencillo contador. Una forma fácil y sencilla de comprender como funcionan las aplicaciones en Angular. Comenzaremos por darle una estructura sencilla. A partir de acá sigue muy de la mano la explicación, el código de esta guía está para que no te pierdas de nada y puedas acceder a el si te quedas atrás, pero la explicación es muy valiosa en este caso.

### Agregando estructura al template

En nuestro archivo `src/app/app.component.html` agregaremos la siguientre estructura:

```html
<div class="container">
    <div class="counter-container">
        <div class="counter">{{counter}}</div>
    </div>
</div>
```

En el archivo `src/app/app.component.ts` **agregaremos la siguiente variable dentro de la clase**:

```typescript
counter: number = 0;
```

Deberiamos de ver un 0 en nuestra vista.

Como este taller está pensado para aprender angular, los estilos ya están preparados para que no perdamos mucho tiempo diseñando y pasemos más tiempo aprendiendo Angular.

En tu archivo `src/app/app.component.css` agregaremos los siguientes estilos.

```css
.container {
    display: flex;
    height: 100vh;
    width: 100vw;
    justify-content: center;
    align-items: center;
}

.counter-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50vw;
}

.counter {
    font-size: 6rem;
    font-family: monospace;
    margin: 0 32px;
}
```

Ahora cambiemos el valor de nuestro counter, ¿Qué pasa en nuestra vista?

### Hagamos que nuestro counter cambie de manera dinamica

Para hacer que nuestro counter cambie debemos de darle al usuario una forma de hacer que cambie. Para esto necesitaremos agregar un par de botones para que cambie. Modifiquemos el `src/app/app.component.html` de la siguiente manera:

```html
<div class="container">
    <div class="counter-container">
        <button class="minus-button">-</button>
        <div class="counter">{{counter}}</div>
        <button class="plus-button">+</button>
    </div>
</div>
```

Y a nuestros estilos `src/app/app.component.css` agregaremos las siguientes clases:

```css
.minus-button {
    background-color: tomato;
    padding: 32px;
    font-size: 48px;
    color: white;
    font-weight: bold;
    border: none;
    border-radius: 16px;
    transition: 0.3s;
    margin: 8px;
}

.minus-button:hover {
    background-color: red;
    cursor: pointer;
}

.plus-button {
    background-color: springgreen;
    padding: 32px;
    font-size: 48px;
    color: white;
    font-weight: bold;
    border: none;
    border-radius: 16px;
    transition: 0.3s;
    margin: 8px;
}

.plus-button:hover {
    background-color: green;
    cursor: pointer;
}
```

Ahora, ya tenemos listos los botones con los cuales interactuará nuestro usuario. Nos hace falta agregar las funciones que manejen el cambio de valor de nuestro counter, para ello, crearemos las siguientes funciones dentro de nuestra clase en `src/app/app.component.ts`. Tendria que verse de la siguiente manera.

```typescript
export class AppComponent {

  counter: number = 0;

  add(): void {
    this.counter += 1;
  }

  substract(): void {
    this.counter -= 1;
  }

}
```

Y una vez más tendríamos que modificar nuestro `src/app/app.component.html`, agregando nuestras funcione para hacer click:

```html
<div class="container">
    <div class="counter-container">
        <button class="minus-button" (click)="substract()">-</button>
        <div class="counter">{{counter}}</div>
        <button class="plus-button" (click)="add()">+</button>
    </div>
</div>
```

## ¿Puedes hacer que el contador se reduzca y aumente de 5 en 5? Intentalo

Tomate el tiempo de realizar esta actividad.

¿Listo? Continuemos

## Guardando un historial

Ahora, una vez que tenemos un contador bastante sencillo, haremos la implementación de un registro/historial de los números a los que hay llegado el contado, será muy sencillo y nos ayudará a sentar las bases de más funcionalidades de Angular.

### Agregando el botón de guardar historial

Lo principal que debemos de realizar es permitirle al usuario realizar la acción de guardar dicho historial, para esto agregaremos un botón adicional al final de lo que ya hemos construido. En tu `src/app/app.component.html` agrega el botón de **Guardar historial**:

```html
<div class="container">
    <div class="counter-container">
        <button class="minus-button" (click)="substract(5)">-5</button>
        <button class="minus-button" (click)="substract(1)">-</button>
        <div class="counter">{{counter}}</div>
        <button class="plus-button" (click)="add(1)">+</button>
        <button class="plus-button" (click)="add(5)">+5</button>
        <button class="plus-button">Save</button>
    </div>
</div>
```

Como puedes notar aun no tiene ninguna funcionalidad (evento click) asignada, pero para eso modificaremos el componente, ahora en tu archivo `src/app/app.component.ts` agregaremos dos cosas.

Lo primero que declararemos es una interfaz para que el proyecto tenga una buena estructura. Esta debe declararse debajo de las importaciones de nuestra clase y por encima del decorador `@Component` de nuestro componente.

```typescript
interface historyRecord {
  count: number;
  date: String
}
```

Y ya que tenemos nuestra interaz podremos declarar una variable de este tipo en nuestro componente.

```typescript
history: historyRecord[] = [];
```

Y junto a esto, agregaremos una nueva función al final de nuestro componente que nos permitirá guardar dicha información utilizando la variable que hemos declarado.

```typescript
saveHistory(): void {
    this.history.push({
        count: this.counter,
        date: new Date().toLocaleString()
    });
    console.log(this.history)
}
```

Y como ya tenemos nuestra acción la agregaremos al botón correspondiente que creamos previamente.

```typescript
<button class="plus-button" (click)="saveHistory()">Save</button>
```

Con esto ya estamos almacenando la información de nuestro counter en una variable que usaremos más adelante.

## Creamos un nuevo componente para mostrar nuestro historial.

Para el siguiente paso deberemos de utilizar la terminal para generar un nuevo componente de Angular. Podemos bajar el servidor de nuestro proyecto con `CTRL + C` o simplemente abrir una nueva terminal, el resultado es indiferente, solo asegurate de que si bajas el servidor despues de terminar el proceso lo vuelvas a levantar con el comando `ng serve`. Bien para generar el componente usaremos:

```bash
ng g c components/list --skip-tests
```

¿Qué vemos aquí?

- "ng" se refiere al CLI de Angular.
- "g" es la abreviatura de `generate`, lo que significa que estamos generando un nuevo archivo o componente.
- "c" es la abreviatura de `component`, lo que significa que estamos generando un nuevo componente de Angular.
- "components/list" es el nombre del nuevo componente que se está generando. En este caso, el nombre del componente es `list` y se colocará en la carpeta `components`.
- `--skip-tests` es una opción que se puede agregar al comando para indicar que no se deben generar archivos de prueba para el componente.

El comando "ng g c components/list --skip-tests", entonces, genera un nuevo componente llamado "list" en la carpeta "components" y omite la generación de archivos de prueba para el mismo.

Utilizando el mismo método, generaremos un segundo componente, ahora llamado `list-item`, usando exactamente la misma estructura.

```bash
ng g c components/list-item --skip-tests
```

Presta atención a tu instructor para conocer cuales fueron las acciones que se ejecutaron y que archivos fueron creados.

Una vez la explicación haya finalizado, podemos continuar.

Ahora agregaremos los componentes que hemos agregado para que sean mostrados en pantalla, primero, en nuestro `src/app/app.component.ts` agregaremos nuestro `list` componente, como se muestra en el snippet inferior.

```html
<div class="container">
    <div class="counter-container">
        <button class="minus-button" (click)="substract(5)">-5</button>
        <button class="minus-button" (click)="substract(1)">-</button>
        <div class="counter">{{counter}}</div>
        <button class="plus-button" (click)="add(1)">+</button>
        <button class="plus-button" (click)="add(5)">+5</button>
        <button class="plus-button">Save</button>
    </div>
</div>
<app-list></app-list>
```

Y para mostrar nuestro elemento `list-item` deberemos de agregarlo dentro de `src/app/components/list/list.component.html` de la siguiente manera:

```html
<p>list works!</p>
<app-list-item></app-list-item>
```

¿Que cambió? ¿Porque vemos ese resultado? Presta atención nuevamente a tu instructor para conocer el porqué y comprender los conceptos detrás.

Bien ahora que la explicación ha finalizado, es momento de realizar algunos cambios dentro de `src/app/components/list-item`. Lo primero que haremos será modificar la estructura HTML de nuestro template, de una manera muy sencilla, modificamos el archivo `src/app/components/list-item/list-item.component.html`.

```html
<div class="item">
    <p>{{count}}</p>
    <p>{{date}}</p>
</div>
```

Para que no nos de error, agregaremos unas variables con un valor por defecto (más adelantes las haremos dinámicas), en nuestro `src/app/components/list-item/list-item.component.ts` agregaremos las siguientes variables:

```typescript
  count: number = 0;
  date: string = "12/12/2022, 12:12:12";
```

y los siguientes estilos en `src/app/components/list-item/list-item.component.css`.

```css
.item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    background-color: burlywood;
    margin: 16px auto;
    padding: 16px 32px;
    border-radius: 16px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: white;
}
```

Ahora nuestro componente se ve mucho mejor, realicemos una modificación a nuestro `src/app/components/list/list.component.html` de la siguiente manera:

```html
<h1 class="title">History</h1>
<div class="container">
    <app-list-item></app-list-item>
    <app-list-item></app-list-item>
    <app-list-item></app-list-item>
</div>
```

Y los siguientes estilos a `src/app/components/list/list.component.css`:

```css
.title {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    border-bottom: 6px solid black;
}

.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
```

Es momento de prestar especial atención a lo que acabamos de realizar, ¿que ha sucedido?.

## Haciendo el historial dinámico

Es momento de aprovechas las funcionalidades que nos proporciona Angular para hacer nuestros componentes dinámicos y darle vida a nuestra aplicación. Para ello iremos a nuestro componente `src/app/components/list/list.component.ts` y agregaremos la siguiente línea:

```ts
@Input() history: any[] = [];
```

No te olvides de importarlo en la parte superior de tu archivo usando:

```ts
import { Component, Input } from '@angular/core';
```

Y modificaremos la etiqueta `app-list` que se encuentra en `src/app/app.component.html` para pasarle el valor deseado, en este caso `history`:

<app-list [history]="history"></app-list>

Retiramos el console.log de la función de guardar el historial

```ts
saveHistory(): void {
    this.history.push({
        count: this.counter,
        date: new Date().toLocaleString()
    });
}
```

y modificamos la vista de `src/app/components/list/list.component.html`

```html
<h1 class="title">History</h1>
<div class="container">
    {{history | json}}
</div>
```

Observemos y entendamos el comportamiento.

## Haciendo las entradas del historial dinamicos

Lo que sigue es realizar cada uno de los elementos del historial de manera dinamica, para ello agregaremos primero dos variables a nuestro `src/app/components/list-item/list-item.component.ts` de la siguiente manera:

```ts
@Input() count: number = 0;
@Input() date: string = "";
```

Recuerda importarlo en la parte superior de tu archivo

```ts
import { Component, Input } from '@angular/core';
```

Y realizaremos la siguiente modiciación al `src/app/components/list/list.component.html` para que se renderice, presta atención a la explicación del instructor para que conozcas más acerca de `ngFor`.

```html
<h1 class="title">History</h1>
<div class="container">
    <app-list-item *ngFor="let element of history" [count]="element.count" [date]="element.date"></app-list-item>
</div>
```

Y listo, tenemos un proyecto que utiliza elementos basicos y herramientas que nos propociona Angular para el desarrollo de aplicaciones basadas en componentes de una manera sencilla y estructurada.

====================

# Los pipes

Continuemos con una práctica distinta a la anterior, sigamos los siguientes pasos:

1.- Iniciamos un nuevo proyecto de angular de la misma manera en que lo hicimos anteriormente.

```bash
ng new new-project

cd new-project

ng serve
```

2.- Limpiamos la vista de nuestro componente app

3.- Agregamos el siguiente código a la vista
```html
<div class="container">
  <div class="card">random text 1</div>
  <div class="card">random text 2</div>
  <div class="card">random text 3</div>
</div>
```

4.- Agregamos los siguientes estilos
```css
.container {
    display: flex;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    flex-wrap: wrap;
}

.card {
    border: 2px solid gray;
    border-radius: 8px;
    padding: 20px;
    font-size: 32px;
    width: 30%;
}
```

5.- Agregamos las siguientes variables a nuestro componente

```typescript
readonly name: string = "Soy francisco magana"
readonly age: number = 28;
readonly money: number = 12300.12;
```

6.- Las colocamos en los divs de la vista

```html
<div class="container">
  <div class="card">{{name}}</div>
  <div class="card">{{age}}</div>
  <div class="card">{{money}}</div>
</div>
```

7.- Agregamos nuestro primer pipe, como se muestra a continuación
```html
<div class="card">{{name | uppercase}}</div>
```
8.- ¿Qué está pasando?

En Angular, un "pipe" es una función que se utiliza para transformar los datos de un valor de entrada en otro valor de salida, de una forma determinada y predefinida.

Por ejemplo, puedes tener un valor numérico que quieres mostrar como una moneda, y para hacer esto puedes utilizar el pipe "currency". También puedes tener una fecha que quieres mostrar en un formato determinado, para lo que puedes utilizar el pipe "date".

Los pipes se utilizan en la plantilla HTML de Angular mediante el carácter "|" (pipe), seguido del nombre del pipe y, opcionalmente, de uno o varios argumentos entre paréntesis.

En resumen, un pipe en Angular te permite transformar datos de una forma fácil y eficiente para que se muestren de la forma que deseas en la interfaz de usuario.

9.- Agregamos los siguientes pipes para observar su comportamiento
```html
<div class="card">{{name | uppercase}}</div>
<div class="card">{{name | lowercase}}</div>
<div class="card">{{name | titlecase}}</div>
```

10.- Agregamos el siguiente pipe a los que ya tenemos
```html
<div class="card">{{age | percent}}</div>
```

11.- ¿Cómo hacemos que sea 20%? Intentalo

12.- Agregamos el siguiente pipe
```html
<div class="card">{{money | currency}}</div>
```

13.- Ahora agreguemos un cambio más y observemos que sucede ¿Son... parámetros?
```html
  <div class="card">{{money | currency:'USD'}}</div>
  <div class="card">{{money | currency:'EUR'}}</div>
  <div class="card">{{money | currency:'MXN'}}</div>
```

# Listo, fue muy sencillo ¿verdad?

Los pipes son herramientas muy útiles que nos ayudan a conseguir muchas cosas de manera sencilla y es un agregado de Angular que facilita el formateo de valores en la vista. Hay muchas cosas más que podemos hacer con los pipes, como el hecho de que podemos crear nuestros Pipes personalizados entre otras, sin embargo, no podemos abarcar todo en este taller, así que estás invitado a descubrir más acerca de los Pipes.

# Consumiendo una API con servicios

1.- Cerramos el servidor de angular con CTRL + C

2.- Ejecutamos el siguiente comando

```bash
ng g s services/using-api
```

3.- Arrancamos de nuevo el server

```bash
ng serve
```

4.- Importamos el HttpClientModule en el app.module
```typescript
import { HttpClientModule } from '@angular/common/http';
```

5.- Lo colocamos en los imports
```typescript
imports: [
    BrowserModule,
    HttpClientModule
  ],
```

¿Que acabamos de hacer? Escucha a tu instructor para una explicación detallada.

6.- Importamos el módulo `HttpClient` en el servicio que creamos

```typescript
import { HttpClient } from "@angular/common/http";
```

7.- Colocamos el módulo en el constructor
```typescript
constructor(public httpClient: HttpClient) { }
```

El parámetro "public httpClient" indica que se está inyectando el servicio HttpClient en la clase y se está declarando una variable llamada "httpClient" que puede ser utilizada en la misma.

HttpClient es un servicio proporcionado por Angular que permite realizar solicitudes HTTP, como GET, POST, PUT y DELETE, a un servidor remoto. Este servicio está diseñado para ser utilizado en aplicaciones web para recuperar datos de una API RESTful.

8.- Hacemos una función para hacer una request GET sencilla a una API pública de ejemplo
```typescript
makeRequest() {
    return this.httpClient.get('https://dummy.restapiexample.com/api/v1/employees');
  }
```

9.- Inyectamos el servicio en el app.component

```typescript
constructor(public api: UsingApiService) {}
```

10.- Ejecutamos la petición en el constructor de la siguiente manera
```typescript
constructor(public api: UsingApiService) {
    api.makeRequest().subscribe((res) => {
      console.log(res)
    })
  }
```
11.- ¿Qué está pasando?

Estamos realizando la llamada a la API mediante el servicio que hemos creado. Presta atención a tu instructor para poder comprender mejor cómo es que funcionan los observables en RXJS.

12.- Limpiemos la vista y agreguemos un botón para hacer la request

```html
<button (click)="request()">Make request</button>
```

13.- Actualicemos nuestro component

```typescript
  request() {
    this.api.makeRequest().subscribe((res) => {
      console.log(res)
    })
  }
  constructor(public api: UsingApiService) {}
```

14.- Detengamos el servidor con CTRL + C

15.- Creemos un nuevo componente para la tarjeta
```bash
ng g c components/card --skip-tests
```

16.- Arrancamos de nuevo el server
```bash
ng serve
```

17.- Modificamos la vista del componente que acabamos de crear
```html
<div class="card">
    <p>My name is {{name | titlecase}}</p>
    <p>My age is {{age}}</p>
    <p>My salary is {{salary | currency:'MXN'}}</p>
</div>
```

18.- Modificamos el componente
```typescript
@Input() name: string = "";
@Input() age: number = 0;
@Input() salary: number = 0;
```

19.- Modificamos los estilos
```css
.card {
    border: 2px solid black;
    border-radius: 8px;
    width: 30%;
}
```

20.- Modificamos el componente del app para obtener los resultados de la petición
```typescript
  results: any[] = [];

  request() {
    this.api.makeRequest().subscribe((res: any) => {
      this.results = res.data;
    })
  }
```

19.- La vista de app la dejaremos así
```html
<button (click)="request()">Make request</button>
<app-card *ngFor="let value of results" 
            [name]="value.employee_name" 
            [age]="value.employee_age"
        [salary]="value.employee_salary">
</app-card>
```

# Prestemos atención al instructor para terminar el taller y continuemos con ejemplos más sencillos con los conocimientos que hemos adquirido.