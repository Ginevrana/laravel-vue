<!-- Link TOP -->
<a name="top"></a>

<!-- Cabecera -->
<div align="center">

<!-- Logo <img> -->

<h1> Sidebar en proyecto Laravel con Vue </h1>

<h3>Prueba de Vue en última versión de Laravel</h3>
<span>
Versión 1.0 - PHP 8.1 - Laravel 10.37.3 - Vue 3
</span>

</div>

<!-- Tabla de contenidos -->
<details>
<summary><h2>Tabla de contenidos</h2></summary>
  <ol>
    <li>
      <a href="#empezando">Empezando</a>
      <ul>
        <li><a href="#prerrequisitos">Prerrequisitos</a></li>
        <li><a href="#instalación">Instalación</a></li>
        <li><a href="#configuración">Configuración</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contribuidores">Contribuidores</a></li>
    <li><a href="#contacto">Contacto</a></li>
    <li><a href="#documentación-adicional-y-reconocimienos">Documentación adicional y Reconocimientos</a></li>    
    <li><a href="#proyectos-relacionados">Proyectos relacionados</a></li>
  </ol>
</details>


<h2>Empezando</h2>
Este puede ser un ejemplo de como podrías dar las instrucciones para levantar tu proyecto localmente. Para tener una copia local hay que correr los siguientes pasos.
<h3>Prerrequisitos</h3>
Contar con php 8 o superior.

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>

<h3>Instalación</h3>

1. Crear nuevo proyecto Laravel
    ```
    composer create-project laravel/laravel nombre-aplicacion
    ```
2. Instalar Vue 3
   ```
   npm install
   npm install vue@next vue-loader@next
   ```
3. Instalar plugin de Vue desde Vite
   ```
   npm i @vitejs/plugin-vue
   ```
4. Editar el archivo `vite.config.js`
   ```
   // vite.config.js
    import { defineConfig } from 'vite';
    import laravel from 'laravel-vite-plugin';

    import vue from '@vitejs/plugin-vue'


    export default defineConfig({
        plugins: [
            vue(),

            laravel({
                input: ['resources/css/app.css', 'resources/js/app.js'],
                refresh: true,
            }),
        ],
    });
   ```
5. Editar el archivo `app.js` que esta dentro de la carpeta `resources/js`
    ```
    import {createApp} from 'vue'

    \import App from './App.vue'

    createApp(App).mount("#app")
    ```
6. Agregar al archivo `.blade.php` el componente de #app dentro de la carpeta `resources/views`
7. Crear archivo `App.vue` dentro de la carpeta `resources/js`
    ```
    <template>
    <h1>
        Tu componente de Vue
    </h1>
    </template>
    ```
8. Agregar ruta en el archivo `web.php` dentro de la carpeta `routes`
    ```
    <?php

    use Illuminate\Support\Facades\Route;

    Route::get('/', function () {
        return view('app');
    })
    ```
9. Correr servidor local de PHP
    ```
    php artisan serve
    ```
10. Correr servidor local de Node
    ```
    npm run dev
    ```

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>

<h3>Configuración</h3>
En este espacio se pueden mostrar ejemplos de cómo puede ser usado el proyecto. Adicionalmente agregar screenshots, ejemplos de código y demos de buen funcionamiento. Además agregar el link a la documentación para más recursos. 

_Para más ejemplos, por favor referirse a la [Documentación](https://example.com)_

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>

<h2>Roadmap</h2>
Aquí se indican las funcionalidades agregadas y las pendientes por agregar:

- [x] Agregar Tabla de contenidos
- [x] Agregar los links para volver arriba
- [ ] Agregar ejemplos adicionales
- [ ] Agregar componentes para fácilmente copiar y pegar en tu README
- [ ] Crear versiones en otros idiomas
    - [ ] Inglés
    - [ ] Francés
    - [ ] Portugués

Tambien podes ver los [issues abiertos](https://github.com/Ginevrana/ReadMe-Template/issues) para la lista completa de funcionalidades propuestas (e issues conocidos).

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>

<h2>Contribuidores</h2>
Se deja constancia de colaboradores en caso de necesitar aclarar alguna duda que no se encuentre en la documentación o hacer alguna consulta sobre el proyecto.

- Florencia Teresita Sanchez 
- Github - Email

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>


<h2>Documentación adicional y Reconocimienos</h2>
Listado de documentación adicional, plugins usados y recursos (tablero de trello, planner, etc.)

- Link 1
- Link 2
- Link 3

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>

<h2>Proyectos relacionados</h2>
Listado de repos o carpetas de proyectos que guarden relación o puedan resultar de interés

- Repo 1
- Sharepoint 1
- Repo 2

<strong><p align="right"><a href="#top">Volver 👆🏻</a></p></strong>