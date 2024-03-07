# Conjunto de Snippets para Visual Studio Code

Este repositorio contiene un conjunto de snippets que he creado para facilitar el desarrollo en varios lenguajes de programación y tecnologías en Visual Studio Code.

## Snippets incluidos

- **JavaScript**: Los snippets para JavaScript se encuentran en el archivo `javascript-snippets.code-snippets`.
- **HTML**: Los snippets para HTML se encuentran en el archivo `html-snippets.code-snippets`.
- **CSS**: Los snippets para CSS se encuentran en el archivo `css-snippets.code-snippets`.
- **Java**: Los snippets para Java se encuentran en el archivo `java-snippets.code-snippets`.
- **Python**: Los snippets para Python se encuentran en el archivo `python-snippets.code-snippets`.
- **React**: Los snippets para React se encuentran en el archivo `react-snippets.code-snippets`.
- **Node.js**: Los snippets para Node.js se encuentran en el archivo `nodejs-snippets.code-snippets`.
- **Express**: Los snippets para Express se encuentran en el archivo `express-snippets.code-snippets`.

## Cómo utilizar este repositorio

### Clonar el repositorio

Puedes clonar este repositorio ejecutando el siguiente comando en tu terminal:

```bash
git clone https://github.com/tu-usuario/mi-conjunto-de-snippets.git
```

### Crear el archivo VSIX
Para empaquetar la extensión en un archivo VSIX, necesitas tener instalada la herramienta vsce. Si no la tienes instalada, puedes hacerlo mediante el siguiente comando:

```
npm install -g vsce
```

Una vez que vsce esté instalado, puedes crear el archivo VSIX ejecutando el siguiente comando en la raíz del repositorio:
```
vsce package
```
Esto generará un archivo .vsix en la carpeta raíz del repositorio, que puedes utilizar para instalar la extensión en Visual Studio Code.

### Instalación desde el archivo VSIX
Puedes instalar la extensión desde el archivo .vsix descargado de la carpeta "install" en este repositorio. Abre Visual Studio Code, ve a la pestaña de extensiones, haz clic en el icono de tres puntos en la esquina superior derecha y selecciona "Instalar desde archivo VSIX". Luego, elige el archivo .vsix descargado y la extensión se instalará en tu editor.

¡Disfruta de tus nuevos snippets!





