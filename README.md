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
- **Express**: Los snippets para Express se encuentran en el archivo `javascript-snippets.code-snippets`.

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
npx vsce package
```
Esto generará un archivo .vsix en la carpeta raíz del repositorio, que puedes utilizar para instalar la extensión en Visual Studio Code.

# Instalación de la Extensión

A continuación, se detallan los pasos para instalar esta extensión en Visual Studio Code utilizando un archivo VSIX:

## Pasos

1. **Descarga del Archivo VSIX:**
   - Ve a la sección de "Install" en el repositorio de esta extensión en GitHub.
   - Encuentra la última versión de la extensión y descarga el archivo VSIX asociado.

2. **Instalación desde Visual Studio Code:**
   - Abre Visual Studio Code.
   - Ve a la pestaña de extensiones haciendo clic en el ícono de la caja en la barra lateral izquierda (o presionando `Ctrl+Shift+X`).
   - Haz clic en el icono de tres puntos en la esquina superior derecha de la pestaña de extensiones.
   - Selecciona "Instalar desde archivo VSIX" en el menú desplegable.
   - Navega hasta la ubicación donde descargaste el archivo VSIX y selecciónalo.
   - Confirma la instalación de la extensión cuando se te solicite.

3. **Comprobación de la Instalación:**
   - Una vez que la instalación esté completa, deberías ver un mensaje de confirmación en la esquina inferior derecha de Visual Studio Code.
   - Además, puedes comprobar si la extensión está instalada correctamente buscándola en la lista de extensiones instaladas en la pestaña de extensiones.

¡Listo! Ahora has instalado con éxito la extensión en Visual Studio Code utilizando un archivo VSIX.






