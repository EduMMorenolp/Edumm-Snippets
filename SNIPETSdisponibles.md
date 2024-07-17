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