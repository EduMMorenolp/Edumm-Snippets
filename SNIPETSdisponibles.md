# Snippets para Express en Node.js

Este documento contiene un conjunto de snippets que he creado para facilitar el desarrollo de aplicaciones Express utilizando ES6 en Visual Studio Code.

## Snippets Disponibles

### 1. Express Server

```javascript
import express from 'express';

const app = express();
const PORT = process.env.PORT || 3000;

app.get('/', (req, res) => res.send('Hello World!'));

app.listen(PORT, () => {
  console.log('\n==================================================');
  console.log(`🚀 Servidor corriendo en: http://localhost:${PORT}`);
  console.log('\n==================================================');
});
```
* Prefix: edumm-express-server-ES6
* Descripción: Configurar un servidor básico con Express.

### 2. Express Route

```javascript
app.${1:get}('${2:/ruta}', (req, res) => {
  res.send('${3:Respuesta}');
});
```

* Prefix: edumm-express-route
* Descripción: Crear una ruta básica en Express.

### 3. Express Routes CRUD
```javascript
import { Router } from 'express';
import { ${3} } from '../controllers/${2}';

const router = Router();

router.get('/${1}', ${4});
router.get('/${1}/:id', ${5});
router.post('/${1}', ${6});
router.put('/${1}/:id', ${7});
router.delete('/${1}/:id', ${8});
```
* Prefix: edumm-express-routes-crud-ES6
* Descripción: Crear rutas CRUD básicas en Express.

### 4. Express Middleware
```javascript
app.use((req, res, next) => {
  // Tu middleware aquí
  next();
});
```
* Prefix: edumm-express-middleware-base
* Descripción: Crear un middleware básico en Express.

### 5. Express Error Handling
```javascript
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Algo salió mal!');
});
```
* Prefix: edumm-express-error
* Descripción: Manejo de errores básico en Express.

### 6. Express Body Parser Middleware
```javascript
import { bodyParser } from 'body-parser';

app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: false }));
```
* Prefix: edumm-express-body-parser
* Descripción: Middleware para analizar el cuerpo de las solicitudes en Express.

### 7. Express Static Files
```javascript
app.use(express.static(path.join(__dirname, '${1:public}')));
```
* Prefix: edumm-express-static
* Descripción: Servir archivos estáticos en Express.

### 8. Express View Engine
```javascript
app.set('views', path.join(__dirname, '${1:views}'));
app.set('view engine', '${2:pug}');
```
* Prefix: edumm-express-view
* Descripción: Configurar vistas y motor de plantillas en Express.

### 9. Express CORS Configuration
```javascript
import cors from 'cors';

app.use(cors());
```
* Prefix: edumm-express-cors
* Descripción: Configurar CORS en Express.

### 10. Express Session Middleware
```javascript
import session from 'express-session';

app.use(session({
  secret: '${1:mySecret}',
  resave: false,
  saveUninitialized: true
}));
```
* Prefix: edumm-express-session
* Descripción: Middleware para manejar sesiones en Express.

### 11. Express Morgan Logging
```javascript
import morgan from 'morgan';

// Configurar Morgan para registrar las solicitudes HTTP
app.use(morgan('dev'));
```
* Prefix: edumm-express-morgan
* Descripción: Configurar Morgan para registrar solicitudes HTTP en Express usando ES6.

### 12. Controlador Básico

```javascript
// Importar el modelo necesario
import ${1:Model} from '../models/${2:modelName}.js';

// Obtener todos los elementos
export const getAll${1} = async (req, res) => {
  try {
    const items = await ${1:Model}.find();
    res.status(200).json(items);
  } catch (error) {
    res.status(500).json({ message: 'Error al obtener elementos' });
  }
};

// Obtener un elemento por ID
export const get${1}ById = async (req, res) => {
  try {
    const item = await ${1:Model}.findById(req.params.id);
    if (!item) return res.status(404).json({ message: 'Elemento no encontrado' });
    res.status(200).json(item);
  } catch (error) {
    res.status(500).json({ message: 'Error al obtener el elemento' });
  }
};

// Crear un nuevo elemento
export const create${1} = async (req, res) => {
  try {
    const newItem = new ${1:Model}(req.body);
    await newItem.save();
    res.status(201).json(newItem);
  } catch (error) {
    res.status(400).json({ message: 'Error al crear el elemento' });
  }
};

// Actualizar un elemento por ID
export const update${1} = async (req, res) => {
  try {
    const updatedItem = await ${1:Model}.findByIdAndUpdate(req.params.id, req.body, { new: true });
    if (!updatedItem) return res.status(404).json({ message: 'Elemento no encontrado' });
    res.status(200).json(updatedItem);
  } catch (error) {
    res.status(400).json({ message: 'Error al actualizar el elemento' });
  }
};

// Eliminar un elemento por ID
export const delete${1} = async (req, res) => {
  try {
    const deletedItem = await ${1:Model}.findByIdAndDelete(req.params.id);
    if (!deletedItem) return res.status(404).json({ message: 'Elemento no encontrado' });
    res.status(204).send();
  } catch (error) {
    res.status(500).json({ message: 'Error al eliminar el elemento' });
  }
};
```
* Prefix: edumm-express-controller-mongo
* Descripción: Estructura básica para un controlador que maneja operaciones CRUD en un modelo de Mongoose.* 