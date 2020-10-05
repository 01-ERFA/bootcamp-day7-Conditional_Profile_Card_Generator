# Conditional Profile Card

Como desarrollador web, estarás creando muchos HTML dinámicos + CSS usando algoritmos de Javascript.

En este ejercicio, debes crear el código HTML necesario para renderizar una tarjeta de perfil en función de una serie de vaiables que podrían cambiar durante el tiempo de ejecución. Aquí hay un ejemplo de la tarjeta de perfil:

![Conditional Profile Card](https://github.com/breatheco-de/exercise-conditional-profile-card/raw/master/preview.gif?raw=true)

1. Dentro `src/index.js` hay una function llamada `render` que recibe un objeto `variables`.
2. Ese objeto `variables` contiene todos los valores asignados en el formulario de la apliación (redes sociales, nombre apellido, etc.).
3. La función render tiene la lógica necesaria para recibir los valores del objeto `variables` e incluirlos dentro del HTML de la pagina utilizando `innerHTML`.

```js
function render(variables = {}) {
  document.querySelector("#widget_content").innerHTML = `<div>Website code</div>`;
}
```

Puedes ver el contenido del objeto `variables` en cualquier momento imprimiento la variable variables en la consola.

```js
console.log(window.variables);
/*
{
    includeCover: true, // if includeCover is true the algorithm should
    background: "https://images.unsplash.com/photo-1511974035430-5de47d3b95da", // this is the url of the image that will used as background for the profile cover
    avatarURL: "https://randomuser.me/api/portraits/women/42.jpg", // this is the url for the profile avatar
    socialMediaPosition: "left", // social media bar position (left or right)
    
    twitter: null, // social media usernames
    github: "alesanchezr",
    linkedin: null,
    instagram: null,

    name: null,
    lastname: null,
    role: null,
    country: null,
    city: null
}
*/
```

## 📝Instrucciones

Revisa este video con las instrucciones para que entiendas mejor el ejercicio: https://youtu.be/gaVm8eyCqlM

1. Instala el proyecto como se indica en la sección "Instalación" más abajo.

2. Lee y comprende la función render y el valor de la variable `variables` que recibe.

3. Cambia el cotenido de la función render para que renderice todos los valores que llegan a traves de `variables`en la tarjeta de perfil.

## Valores de variables iniciales

| Nombre | Tipo | Valor por Defecto | Descripción |
| --- | --- | --- | --- |
| background | string | null | la url de la imagen que se utilizará como fondo para la portada del perfil |
| includeCover | boolean | true | Determina si debe mostrarse la portada o no. |
| avatarURL | string | null | la url para el avatar del perfil |
| socialMediaPosition | string | "right" | puede ser `left` o` right` y determina dónde colocar la barra de redes sociales |
| twitter | string | null | El nombre de usuario de Twitter que se mostrará en el perfil. |
| github | string | null | El nombre de usuario de Github que se mostrará en el perfil. |
| linkedin | string | null | El nombre de usuario de linkedin que se mostrará en el perfil. |
| instagram | string | null | El nombre de usuario de Instagram para ser mostrado en el perfil. |
| name | string | null | El nombre del usuario que se mostrará en el perfil.|
| lastname | string | null | El nombre del usuario que se mostrará en el perfil. |
| role | string | null | El nombre del título del trabajo que se mostrará en el perfil. |
| country | string | null | El país de residencia del usuario que se mostrará en el perfil. |
| city | string | null | La ciudad de residencia del usuario que se mostrará en el perfil.|

## Ejemplo de HTML codificado

Este es un ejemplo de un posible **resultado** HTML, debe reemplazar: 
  *name*,           //h1 
  *lastname*,       //h1
  *role*,           //h2
  *city*,           //h3
  *country*,        //h3
  *social networks*,//ul
  *photo*,          //img
  *background*,     //div->img

Con valores reales.

```html
<div class="widget">
  <div class="cover"><img src="https://the_url.com/for_the_background.png" /></div>
  <img src="https://the_url.com/for_the_image.png" class="photo" />
  <h1>Ryan Boylett</h1>
  <h2>Web Developer</h2>
  <h3>Miami, USA</h3>
  <ul class="position-right">
    <li><a href="https://twitter.com/alesanchezr"><i class="fa fa-twitter"></i></a></li>
    <li><a href="https://github.com/alesanchezr"><i class="fa fa-github"></i></a></li>
    <li><a href="https://linkedin.com/alesanchezr"><i class="fa fa-linkedin"></i></a></li>
    <li><a href="https://instagram.com/alesanchezr"><i class="fa fa-instagram"></i></a></li>
  </ul>
</div>
```

## Instalación

1. Clona este repositorio para descargar el boilerplate inicial: `git clone https://github.com/breatheco-de/exercise-conditional-profile-card`

2. Entra en la carpeta del proyecto:  `cd exercise-conditional-profile-card`

3. Instala los paquetes NPM (asegúrate de usar la última versión de node): `npm install`

4. Corre el proyecto utilizando:  `npm run start`

5. Actualiza la función `render` dentri del archivo index.js.

